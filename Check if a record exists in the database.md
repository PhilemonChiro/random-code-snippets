```C#
SqlCommand check_User_Name = new SqlCommand("SELECT * FROM Table WHERE ([user] = @user)" , conn);
check_User_Name.Parameters.AddWithValue("@user", txtBox_UserName.Text);
SqlDataReader reader = check_User_Name.ExecuteReader();
if(reader.HasRows)
{
   //User Exists
}
else
{
   //User NOT Exists
}
```
