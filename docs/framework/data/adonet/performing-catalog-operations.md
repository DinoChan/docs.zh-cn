---
title: 执行目录操作
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
ms.assetid: e60f542f-6271-495b-a9e4-48553481c2a3
ms.openlocfilehash: 7588b2b4592a5298a69eb4adfbc06edb6913ef76
ms.sourcegitcommit: 2eceb05f1a5bb261291a1f6a91c5153727ac1c19
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/04/2018
ms.locfileid: "43519091"
---
# <a name="performing-catalog-operations"></a>执行目录操作
若要执行的命令来修改数据库或目录，如 CREATE TABLE 或 CREATE PROCEDURE 语句创建**命令**对象使用相应的 SQL 语句和一个**连接**对象。 使用执行命令**ExecuteNonQuery**方法**命令**对象。  
  
 以下代码示例在 Microsoft SQL Server 数据库中创建一个存储过程。  
  
```vb  
' Assumes connection is a valid SqlConnection.  
Dim queryString As String = "CREATE PROCEDURE InsertCategory " & _  
    "@CategoryName nchar(15), " & _  
    "@Identity int OUT " & _  
    "AS " & _  
    "INSERT INTO Categories (CategoryName) VALUES(@CategoryName) " & _  
    "SET @Identity = @@Identity " & _  
    "RETURN @@ROWCOUNT"  
  
Dim command As SqlCommand = New SqlCommand(queryString, connection)  
command.ExecuteNonQuery()  
```  
  
```csharp  
// Assumes connection is a valid SqlConnection.  
string queryString = "CREATE PROCEDURE InsertCategory  " +   
    "@CategoryName nchar(15), " +  
    "@Identity int OUT " +  
    "AS " +   
    "INSERT INTO Categories (CategoryName) VALUES(@CategoryName) " +   
    "SET @Identity = @@Identity " +  
    "RETURN @@ROWCOUNT";  
  
SqlCommand command = new SqlCommand(queryString, connection);  
command.ExecuteNonQuery();  
```  
  
## <a name="see-also"></a>请参阅  
 [使用命令修改数据](../../../../docs/framework/data/adonet/using-commands-to-modify-data.md)  
 [命令和参数](../../../../docs/framework/data/adonet/commands-and-parameters.md)  
 [ADO.NET 托管提供程序和数据集开发人员中心](https://go.microsoft.com/fwlink/?LinkId=217917)
