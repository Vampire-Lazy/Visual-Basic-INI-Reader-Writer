# Visual-Basic-INI
A class file to read/write INI files to store application configurations.
## Usage :

**Example ini file:**

```
[MAIN]
Setting_1=something
```

Instantiate the class:
```
Dim objIniFile As New InIFile("path_of_your_file")
```

Get the setting:

```
Dim x As String
x = objIniFile.GetString("MAIN", "Setting_1", "")
```

Update / Create a setting:

```
objIniFile.WriteString("MAIN", "Setting_1", "new_setting")
```

This is what it looks like:
```
Private Sub Form1_Load(ByVal sender As System.Object, ByVal e As System.EventArgs) Handles MyBase.Load
    Dim objIniFile As New InIFile("D:\WorldInfo.ini")
    Label1.Text = objIniFile.GetString("CATEGORYNAME", "Value_1", "")
    Label2.Text = objIniFile.GetString("CATEGORYNAME", "Value_2", "")
End Sub
```
