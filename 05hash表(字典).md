这里的hash表，其实和java、python中的字典是一样的。可以理解成同一个概念。

# 创建hash表

之前使用@()创建数组，现在使用@{}创建哈希表，使用哈希表的键访问对应的值。

```powershell
PS C:Powershell> $stu=@{ Name = "小明";Age="12";sex="男" }
PS C:Powershell> $stu

Name                           Value
----                           -----
Name                           小明
Age                            12
sex                            男

PS C:Powershell> $stu["Name"]
小明
PS C:Powershell> $stu["age"]
12
PS C:Powershell> $stu.Count
3
PS C:Powershell> $stu.Keys
Name
Age
sex
PS C:Powershell> $stu.Values
小明
12
男
```

# hash表中存放数组

```
PS C:\Users\wujiashuai> $stu=@{name="小米";age="12";books="三国演义","哈姆雷特","33333333"}
PS C:\Users\wujiashuai> $stu

Name                           Value
----                           -----
books                          {三国演义, 哈姆雷特, 33333333}
name                           小米
age                            12
```

# 插入

```
PS C:Powershell> $Student=@{}
PS C:Powershell> $Student.Name="令狐冲"
PS C:Powershell> $Student.School="华山派"
PS C:Powershell> $Student

```

# 哈希表值的更新和删除

```
PS C:Powershell> $stu

Name                           Value
----                           -----
Books                          {三国演义, 围城, 哈姆雷特}
Name                           小明
Age                            12
sex                            男

PS C:Powershell> $stu.Name="赵强"
PS C:Powershell> $stu.Name
赵强
PS C:Powershell> $stu.Remove("Name")
PS C:Powershell> $stu

Name                           Value
----                           -----
Books                          {三国演义, 围城, 哈姆雷特}
Age                            12
sex                            男
```

# 格式化输出

```
PS C:Powershell> Dir | Format-Table

    Directory: C:Powershell

Mode                LastWriteTime     Length Name
----                -------------     ------ ----
d----        2011/11/23     17:25            ABC
d----        2011/11/29     18:21            myscript

PS C:Powershell> Dir | Format-Table FullName,Mode

FullName                                                    Mode
--------                                                    ----
C:PowershellABC                                           d----
C:Powershellmyscript                                      d----
```

