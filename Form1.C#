Public Class Form1
    Dim firstNumber As Double = 0
    Dim secondNumber As Double = 0
    Dim operation As String = ""
    Dim isNewEntry As Boolean = True


    Private Sub TextBox1_TextChanged(ByVal sender As System.Object, ByVal e As System.EventArgs) Handles txtDisplay.TextChanged
        
    End Sub

    Private Sub Number_Click(ByVal sender As System.Object, ByVal e As System.EventArgs) Handles btn0.Click, btn1.Click, btn2.Click, btn3.Click, btn4.Click, btn5.Click, btn6.Click, btn7.Click, btn8.Click, btn9.Click
        Dim btn As Button = CType(sender, Button)

        If isNewEntry Or txtDisplay.Text = "0" Then
            txtDisplay.Text = btn.Text
            isNewEntry = False
        Else
            txtDisplay.Text &= btn.Text
        End If
    End Sub

    Private Sub Operator_Click(ByVal sender As System.Object, ByVal e As System.EventArgs) _
    Handles btnPlus.Click, btnMinus.Click, btnMultiply.Click, btnDivide.Click

        Dim btn As Button = CType(sender, Button)
        firstNumber = Val(txtDisplay.Text)
        operation = btn.Text
        isNewEntry = True
    End Sub

    Private Sub btnEqual_Click(ByVal sender As System.Object, ByVal e As System.EventArgs) Handles btnEqual.Click
        secondNumber = Val(txtDisplay.Text)
        Dim result As Double = 0

        Select Case operation
            Case "+"
                result = firstNumber + secondNumber
            Case "-"
                result = firstNumber - secondNumber
            Case "*"
                result = firstNumber * secondNumber
            Case "/"
                If secondNumber <> 0 Then
                    result = firstNumber / secondNumber
                Else
                    MessageBox.Show("Cannot divide by zero")
                    Exit Sub
                End If
        End Select

        txtDisplay.Text = result.ToString()
        isNewEntry = True
        lblOperation.Text = firstNumber & "" & operation & "" & secondNumber & " ="
    End Sub


    Private Sub btnC_Click(ByVal sender As System.Object, ByVal e As System.EventArgs) Handles btnC.Click
        txtDisplay.Text = "0"
        firstNumber = 0
        secondNumber = 0
        operation = ""
    End Sub

    Private Sub btnCE_Click(ByVal sender As System.Object, ByVal e As System.EventArgs) Handles btnCE.Click
        txtDisplay.Text = "0"
    End Sub

    Private Sub Button15_Click(ByVal sender As System.Object, ByVal e As System.EventArgs) Handles btn0.Click

    End Sub

    Private Sub btnDot_Click(ByVal sender As System.Object, ByVal e As System.EventArgs) Handles btnDot.Click
        If isNewEntry Then
            txtDisplay.Text = "0."
            isNewEntry = False
        ElseIf Not txtDisplay.Text.Contains(".") Then
            txtDisplay.Text &= "."
        End If
    End Sub

   
    Private Sub lblOperation_Click(ByVal sender As System.Object, ByVal e As System.EventArgs)

    End Sub

    Private Sub lblOperation_Click_1(ByVal sender As System.Object, ByVal e As System.EventArgs) Handles btnPlus.Click, btnMinus.Click, btnMultiply.Click, btnDivide.Click

        Dim btn As Button = CType(sender, Button)
        firstNumber = Val(txtDisplay.Text)
        operation = btn.Text
        lblOperation.Text = txtDisplay.Text & "" & operation
        isNewEntry = True
    End Sub
End Class
