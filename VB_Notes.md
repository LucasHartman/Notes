# VB_Notes

Source: [https://www.vbtutor.net/index.php/visual-basic-2017-lesson-6-using-list-box-combo-box/]

Sourece: [https://www.tutorialspoint.com/vb.net/vb.net_button.htm]

# ------------------------------
# Syntax
# ------------------------------

# Variable
- Declare:
- Dim keyword to declare the data
    Dim MyName As String
    Dim Num1 As Integer
    Dim Num2 As Single
    Dim Sum As Integer
    Dim StartDate As Date
- Initilize
    Dim YourName as String="George"
    Dim VarNum as Interger=100
- Expression
    Dim num1 As Single = Val(TxtNum1.Text)
    Dim num2 As Single = Val(TxtNum2.Text)
    Dim Sum As Single = num1 + num2
- Scope:
    Private VariableName as Datatype
    Static VariableName as Datatype
    Public VariableName as Datatype
- Constant
    Const Pi As Single = 3.142
- Declare multiply
    Dim i, n As Integer
    Dim str1 = "Visual ", str2 = "Basic ", str3 = "2017", str As String

# Data Types
Long:           130890&        
Single          1.3089!
Double:         1.3089#
Currency:       1.3089@

# 1D Array
- Declare
- n indicates the last index
    Dim arrayName(n) as dataType
    Dim CusName(10) as String
    Dim arr() As Integer = {1, 2, 3, 4}
- Array Length
    CusName.Length

# 2D Array
- Declare:
    Dim CusName(5,6) As String

# Dynamic Array
- Store during runtime
- Declare without dimension list:
    Dim myArray() As Integer
    Dim i, n As Integer
    n = InputBox("Enter the upper bound of array")
    ListBox1.Items.Clear()

    For i = 1 To n
        ReDim myArray(i) 'resize at each iteration
        myArray(i) = i ^ 2
        ListBox1.Items.Add(myArray(i))

    Next ' output: 1 4 9 16 25 36...

# Get Item from Array
Dim val As Integer = arr(1) 'get value index 1

#Foreach
For Each name As String In names
      Console.WriteLine(name)
    Next

# Index of Item
Console.WriteLine(array.IndexOf(animals, "bunny").ToString)

# Print Array
Console.WriteLine(String.Join(" ", arr))


Source: [https://www.vbtutor.net/index.php/visual-basic-2017-lesson-12-working-strings/]

# Strings
- Declare
    Dim MyText As String
    MyText="Visual Basic"
- String Length
    Len(MyText)
- subString (right side)
    Dim MyText As String
    MyText="Visual Basic"
    MsgBox(Microsoft.VisualBasic.Right(MyText, 4))

# Conditional Operators
    Dim Mark As Integer
    Dim Grade As String
    Mark = TxtMark.Text
    
    If Mark >= 80 And Mark <= 100 Then
        Grade = "A"
    ElseIf Mark >= 60 And Mark < 80 Then
        Grade = "B"
    ElseIf Mark >= 40 And Mark < 60
        Grade = "C"
    ElseIf Mark >= 0 And Mark < 40
        Grade = "D"
    Else
        Grade = "Out of Range"
    End If
    MsgBox("You Grade is " & Grade)

# Select Case (Switch)
    Dim mark As Single
    mark = TextBox1.Text
    
    Select Case mark
    Case 0 To 49
        LblGrade.Text = “E”
    Case 50 To 59
        LblGrade.Text = “D”
    Case 60 To 69
        LblGrade.Text = “C”
    Case 70 To 79
        LblGrade.Text = “B”
    Case 80 To 100
        LblGrade.Text = “A”
    Case Else
        LblGrade.Text = “Error, please re-enter the mark”
    End Select
    End Sub

# For Loop
    Dim counter as Integer
    For counter=1 to 10
        ListBox1.Items.Add (counter)

        If n>6 then
            Exit For
            End If
        
            Next '1 2 3 4 5 6

# Do while
    Do while counter <=1000
        TextBox1.Text=counter
        counter +=1
        Loop

# Do
    Do
        TextBox1.Text=counter
        counter+=1
        Loop until counter>1000

# Sub Procedures (Constructor)
    Private Sub Form1_Load(sender As Object, e As EventArgs) Handles MyBase.Load
    
    sum(5, 6) 
    End Sub 

    Sub sum(a As Single, b As Single)
    MsgBox("sum="& a + b)
    End Sub 

# Functions
- Declare
    Private Function BMI(Height As Single, weight As Single) As Double
        BMI = weight / Height ^ 2
        End Function
- Initilize
    Dim h As Single, w As Single
    h = Val(TextBox1.Text)
    w = Val(TextBox2.Text)
    LblBMI.Text = BMI(h, w)

# Format (Convert)
    Label1.Text = Format(8972.234, "General Number")
    Label2.Text = Format(8972.2, "Fixed")
    Label3.Text = Format(6648972.265, "Standard")
    Label4.Text = Format(6648972.265, "Currency")
    Label5.Text = Format(0.56324, "Percent")
- User-Defined Format
    Label1.Text = Format(8972.234, "0.0")
    Label2.Text = Format(8972.2345, "0.00")
    Label3.Text = Format(6648972.265, "#,##0.00")
    Label4.Text = Format(6648972.265, "$#,##0.00")
    Label5.Text = Format(0.56324, "0%")
- Date
    Label1.Text = Format(Now, "General Date")
    Label2.Text = Format(Now, "Long Date")
    Label3.Text = Format(Now, "short Date")
    Label4.Text = Format(Now, "Long Time") Label5.Text = Format(Now, "Short Time")
-  Formatting Date and time
    Label1.Text = Format(Now, "m")
    Label2.Text = Format(Now, "mm")
    Label3.Text = Format(Now, "mmm")
    Label4.Text = Format(Now, "mmmm")
    Label5.Text = Format(Now, "dd/mm/yyyy")
    Label6.Text = Format(Now, "mmm,d,yyyy")
    Label7.Text = Format(Now, "h:mm:ss tt")
    Label8.Text = Format(Now, "MM/dd/yyyy h:mm:ss tt")

    # String to HashSet
    Dim hash As HashSet(Of Char) = New HashSet(Of Char)("fish")

    # HashSet to Array
    Dim arr() As Char
    arr = hash.ToArray()
    Console.WriteLine(String.Join(" ", arr))

# ------------------------------
# Setup
# ------------------------------

# Compile & Run
vbc myScript.vb 
myScript

# Create Project
1. Visual Studio > Create New Project > Visual Basic > Windows Desktop > DevExpress > Ribbon Based Application
2. Build an UI:
- Start with a Table als Container, fill cells with flowPanel or Table if you want to build a list of item
3. Build action code inside the button method

# Change window properties (Visual Studio)
1. Visual Studio > Properties Panel
- the properties window displays all properties

# Screen Sizes (Rezolution)
SmartPhone      320, 480
Tables          1024, 768
Laptop          1280, 800
Desktop         1680, 1050

# Start Window Code
    Dim defWindowSize As Point = New Point(1024, 768)
    Dim minWindowSize As Point = New Point(320, 480)
    Dim maxWindowSize As Point = New Point(1680, 1050)

    Private Sub Form1_Load(sender As Object, e As EventArgs) Handles MyBase.Load
        Me.Width = defWindowSize.X
        Me.Width = defWindowSize.Y
        Me.AutoSize = True
        Me.AutoSizeMode = AutoSizeMode.GrowOnly
        Me.MinimumSize = minWindowSize
        Me.MaximumSize = maxWindowSize
        Me.Text = "Template"
        Me.BackColor = primaryColor
    End Sub

# Change form properties (code)
Private Sub Form1_Load(sender As Object, e As EventArgs) Handles MyBase.Load
    ' add Form properties here:
    Me.Text = “My First VB2017 Program”
    Me.BackColor = Color.Cyan
    Me.MaximizeBox=False
    Me.MinimizeBox = True
End Sub
 
# Add Controller(Objects)
1. Visual Studio > View > Toolbox
2. Select controllers from DX.16.2
3. Drag to Form [Design]



# ------------------------------
# Event-Driven Programming
# ------------------------------

# Create Pop-up Window
1. click on any part of the form to enter the code window
- This is the structure of an event procedure
2. insert the statement:
- MsgBox (“Hello World″)
- this wil create a pop-up message box at button click
3. Me.Close()
- this action create a close button on the pop-up window


# ------------------------------
# Build UI Elements
# ------------------------------

# TextBox (input user data)
1. MsgBox("The sum is "& Val(TextBox1.Text) + Val(TextBox2.Text))

# Label (static text)
LblAns.Text = Sum.ToString

# List Box
1. Create List: Insert a list box on the form
2. add Item:    Properties Panel > Data > Item: Collection...
3. add() method:
-       Dim myitem
        myitem = InputBox(“Enter your Item”)
        ListBox1.Items.Add(myitem)
- Declare variable
- Init variable with a input box
- add variable to list
4. Remove() method:
        Dim myitem
        myitem = InputBox(“Enter your Item for Deletion”)
        ListBox1.Items.Remove(myitem)
5. Remove All
        Handles Button2.Click
        ListBox1.Items.Clear()

# Combo Box (drop-down list)
1. Create Combo Box: Insert a combo box on the form
2. add Item:    Properties Panel > Data > Item: Collection...
3. add() method:
-       Dim myitem
        myitem = InputBox(“Enter your Item”)
        ComboBox1.Items.Add(myitem)
- Declare variable
- Init variable with a input box
- add variable to list
4. Remove() method:
        Button2.Click
        ComboBox1.Items.Remove(“Visual Basic 6”)
5. Remove All
        Handles Button2.Click
        ComboBox1.Items.Clear()

# Change Tab Name
Properties > Behavior > TabPages > (Collection)...

# ------------------------------
# Build UI Advanced
# ------------------------------

# UI Setup 
1. FlowLayoutPanel LeftSide
- Dock: Left

# Table Form
1. Create TableLayout
    - Toolbox > TableLayout > Drag to Form 
2. TableLayout > RMB > Remove Row
3. Dock TableLayout
    - TableLayout > Properties > Layout > Dock > Top
4. Edit Columns Scaling
    - TableLayout > RMB > Edit Row & Column
    - Select Column percentage or Absolute
5. Set all object in Column below each other
    - Add FlowLayoutPanels to each Column 
    - FlowLayoutPanels > Properties > Layout > FlowDirection: TopDown

# Text Align Center
Properties > Dock > Fill
Properties > Appearance > TextAlign: TopCenter

# Center Button
Anchor: None
MaximumSize
MinimumSize

# Auto Stretch Text Box
1. Create a table with a number of rows and one column
2. place in each cell a Textbox
3.  Dock > Top

# TabControl size with parent
1. Create TabControl
2. Set the size to the border of the parent 
3. Turn all Anchor, so its stretches with the parent


# Fill total area
Dock > Fill

# Object below each other
- Create A FlowLayout with some objects insides
- Properties > Layout > FlowDirection: TopDown

# Top Menu Bar
1. Properties > Window Style > MainMenuStrip
2. ToolBox > TooStripMenuItem > Drag To Design

# Create New Window From
1. Solution Explorer > rmb[projectName] > Add > Windows From: Windows Form  
- A new form.vb is created

# Form in Form Setup
1. From1 Properties > Window Style > IsMdiContainer: True
2. Create MenuStrip
2. Create new Form: Solution Explorer > rmb[projectName] > Add > Windows From: Windows Form 
3. Form 1 Code 

    Public Class Form1
        Private Sub Form2ToolStripMenuItem_Click(sender As Object, e As EventArgs) Handles Form2ToolStripMenuItem.Click
            Form2.Show()
        End Sub
End Class

4. From 2 Code

    Public Class Form2
        Private Sub Form2_Load(sender As Object, e As EventArgs) Handles MyBase.Load
            MdiParent = Form1
        End Sub
    End Class


# ------------------------------
# Mods
# ------------------------------

# Create Time-Count
1. input Time Controller, and a label or textbox
    - set timer seconds:    Properties > Interval
    - activate time:        Properties >Enabled: True
    - enable counter:       labal.Text: 0
2. Create time method:      Double click Timer1
3. Input:

        TextBox1.Text = TextBox1.Text + 1   'view time in textbox
        Label1.Text = Label1.Text + 1       'view time in label

        If Label1.Text = 3 Then             'show message at 3 second
            MsgBox("Hello:" + Me.Width.ToString())
        End If
    End Sub

# React to Window Resize
        If Me.Width < 700 Then
            MsgBox("ola:" + Me.Width.ToString())
        End If

# Property react to change in Time
        Label1.Text = Label1.Text + 1
        Label2.Text = Label1.Text Mod 2

        If Label2.Text = 1 And Me.Width < 320 Or Label2.Text = 0 And Me.Width < 320 Then
            tableContainerLeft.BackColor = Color.Red
        Else
            tableContainerLeft.BackColor = Color.Blue
        End If


# Dynamic Split Panel (Version 1)
  Private Function dynamicSplitPanel(panelSwitch As Integer)
        'This Method creates a Dynamic Split Panel. 
        'Switch between Left/Right Split View & Stacked View,
        'by dragging the window horizontally.
        'Determine the switch by setting the 'PanelSwitch' parameter

        'Preparation:
        'TableLayoutPanel named: tableContainerLeft
        'TableLayoutPanel named: tableContainerRight
        'Label named: countLabel
        'Label named: remainderLabel
        'Time Controller named: Timer1
        'Initialize dynamicSplitPanel(x) inside Time1

        'Utility
        Dim leftHeight As Integer = 500
        Dim rightHeight As Integer = 500
        Time1.Enabled = True
        Time1.Interval = 100
        countLabel.Location = New Point(Me.Width, 0)
        countLabel.Visible = False
        countLabel.Text = countLabel.Text + 1
        remainderLabel.Location = New Point(Me.Width, 10)
        remainderLabel.Visible = False
        remainderLabel.Text = countLabel.Text Mod 2
        'Dynamic Container Layout
        If remainderLabel.Text = 1 And
            Me.Width > panelSwitch Or
            remainderLabel.Text = 0 And Me.Width > panelSwitch Then
            VScrollBar.Visible = False
            'Left Container
            tableContainerLeft.BackColor = Color.Red
            tableContainerLeft.Location = New Point(0, 0)
            tableContainerLeft.Width = (Me.Width / 2) - 10
            tableContainerLeft.Height = leftHeight
            'Right Container
            tableContainerRight.BackColor = Color.Blue
            tableContainerRight.Width = (Me.Width / 2) - 10
            tableContainerRight.Height = rightHeight
            tableContainerRight.Location = New Point(Me.Width / 2 - 10, 0)
        Else
            'Top Container
            tableContainerLeft.BackColor = Color.Red
            tableContainerLeft.Location = New Point(0, -VScrollBar.Value)
            tableContainerLeft.Width = Me.Width - 35
            tableContainerLeft.Height = leftHeight
            'Bottum Container
            tableContainerRight.BackColor = Color.Blue
            tableContainerRight.Location = New Point(0,
            tableContainerLeft.Height - (VScrollBar.Value))
            tableContainerRight.Width = (Me.Width) - 35
            tableContainerRight.Height = rightHeight
            'ScrollBar
            VScrollBar.Height = Me.Height - 40
            VScrollBar.Width = 15
            VScrollBar.Location = New Point(Me.Width - 33, 0)
            VScrollBar.Visible = True
        End If
    End Function