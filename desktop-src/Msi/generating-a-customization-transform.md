---
description: 您可以使用 MsiDatabaseGenerateTransform 或 Database 物件的產生器方法來產生轉換檔案。
ms.assetid: c016fcba-0d54-4b99-bcdd-36967b2c9da0
title: 產生自訂轉換
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b790917100cc06da97e09fd8aabf45b580e62008d23c9fc5065e6005112d8d4e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118635996"
---
# <a name="generating-a-customization-transform"></a>產生自訂轉換

您可以使用 [**MsiDatabaseGenerateTransform**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabasegeneratetransforma)或 [**Database 物件**](database-object.md)的產生器 [**方法**](database-generatetransform.md)來產生轉換檔案。 Windows Installer SDK 中提供的範例是公用程式 WiGenXfm.vbs。 下列程式碼片段（Gen.vbs）也會說明 **此表示** 法，並可搭配 Windows 腳本主機使用。


```VB
'Gen.vbs. Argument(0) is the original database. Argument(1) is the
'    customized database. Argument(2) is the transform file.
 
Option Explicit

' Check arguments
If WScript.Arguments.Count < 2 Then
    WScript.Echo "Usage is gen.vbs [original database] [customized database] [transform file]"
    WScript.Quit(1)
End If

' Connect to Windows Installer object
On Error Resume Next
Dim installer : Set installer = Nothing
Set installer = Wscript.CreateObject("WindowsInstaller.Installer") 
' Open databases
Dim database1 : Set database1 = 
    installer.OpenDatabase(Wscript.Arguments(0), 0) 
Dim database2 : Set database2 = 
    installer.OpenDatabase(Wscript.Arguments(1), 0) 
' Generate transform
Dim transform : transform = Database2.GenerateTransform(Database1,
    Wscript.Arguments(2))
```



若要從原始 MNP2000.msi 資料庫和您在 [自訂原始資料庫](customizing-an-original-database.md)中修改的 MNP2000t.msi 資料庫產生轉換檔案 MNPtrans，請將目錄變更為包含 Gen.vbs、原始資料庫和更新的安裝程式資料庫的資料夾，然後輸入下列命令列。

**Cscript.exe Gen.vbs MNP2000.msi MNP2000t.msi MNPtrans**

[繼續](adding-summary-information-to-customization-transform.md)

 

 



