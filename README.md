### Nemiro.OAuth.LoginForms

**Nemiro.OAuth.LoginForms** is a class library that contains ready-to-use **OAuth** authorization forms for **Windows Forms** projects (**.NET Framework**).

It is an independent part of the **[Nemiro.OAuth](https://github.com/alekseynemiro/nemiro.oauth.dll)** project. 

**Nemiro.OAuth.LoginForms** is licensed under the **Apache License Version 2.0**.

To install **Nemiro.OAuth.LoginForms**, run the following command in the **Package Manager Console**:

`PM> Install-Package Nemiro.OAuth.LoginForms`

### System Requirements

* [Nemiro.OAuth](https://github.com/alekseynemiro/nemiro.oauth.dll) v1.6 or later;
* Microsoft Windows XP, 7 or later with .NET Framework 4.0 or 4.5 or later;
* Microsoft Visual Studio 2010 (recommended Professional Edition with Service Pack 1) or later.

### How to use

**C#**
```C#
// create login form
var login = new DropboxLogin("5nkunr8uscwfoba", "n7x9icfwoe6dehq") { Owner = this };
// show login form
login.ShowDialog();
// authorization is success
if (login.IsSuccessfully)
{
  // use the access token for requests to API
  MessageBox.Show(login.AccessToken.Value);
}
```

**Visual Basic .NET**
```VBNet
' create login form
Dim login As New DropboxLogin("5nkunr8uscwfoba", "n7x9icfwoe6dehq") With { .Owner = Me }
' show login form
login.ShowDialog()
' authorization is success
If login.IsSuccessfully Then
  ' use the access token for requests to API
  MessageBox.Show(login.AccessToken.Value)
End If
```

### See Also

* https://github.com/alekseynemiro/nemiro.oauth.dll
* http://nemiro.net