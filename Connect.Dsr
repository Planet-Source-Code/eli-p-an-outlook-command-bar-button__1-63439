VERSION 5.00
Begin {AC0714F6-3D04-11D1-AE7D-00A0C90F26F4} Connect 
   ClientHeight    =   9945
   ClientLeft      =   1740
   ClientTop       =   1545
   ClientWidth     =   6585
   _ExtentX        =   11615
   _ExtentY        =   17542
   _Version        =   393216
   Description     =   "Add-In Project Template"
   DisplayName     =   "My Add-In"
   AppName         =   "Microsoft Outlook"
   AppVer          =   "Microsoft Outlook 11.0"
   LoadName        =   "Startup"
   LoadBehavior    =   3
   RegLocation     =   "HKEY_CURRENT_USER\Software\Microsoft\Office\Outlook"
End
Attribute VB_Name = "Connect"
Attribute VB_GlobalNameSpace = False
Attribute VB_Creatable = True
Attribute VB_PredeclaredId = False
Attribute VB_Exposed = True
Dim OL As Outlook.Application
Dim WithEvents objButton As Office.CommandBarButton
Attribute objButton.VB_VarHelpID = -1

Private Sub AddinInstance_OnConnection(ByVal Application As Object, _
   ByVal ConnectMode As AddInDesignerObjects.ext_ConnectMode, _
   ByVal AddInInst As Object, custom() As Variant)

   Dim objBar As Office.CommandBar
   Set OL = Application
   Set objBar = OL.ActiveExplorer.CommandBars.Item("Standard")
   Set objButton = objBar.Controls.Add(, , , 1, True)
   With objButton
      .FaceId = 2646
      .Caption = "My Button"
      .Style = msoButtonIconAndCaption

      ' The OnAction property is optional but recommended.
      ' It should be set to the ProgID of the add-in, such that if
      ' the add-in is not loaded when a user presses the button,
      ' Outlook loads the add-in automatically and then raises
      ' the Click event for the add-in to handle.

      .OnAction = "!<" & AddInInst.ProgId & ">"
   End With

End Sub

Private Sub objButton_Click(ByVal Ctrl As Office.CommandBarButton, _
   CancelDefault As Boolean)

  Form1.Show

End Sub
        

