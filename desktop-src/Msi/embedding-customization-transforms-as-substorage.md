---
description: 您可以將自訂轉換儲存在 Windows Installer 套件的儲存體中，以保證當安裝套件可用時，一律可使用轉換。
ms.assetid: d4c022d2-a8c4-4b4e-8a6c-b14e1bc6effe
title: 將自訂轉換內嵌為 Substorage
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bfd275d36b37b2e29ae166a2a464a62495d2ca9c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106993188"
---
# <a name="embedding-customization-transforms-as-substorage"></a>將自訂轉換內嵌為 Substorage

您可以將自訂轉換儲存在 Windows Installer 套件的儲存體中，以保證當安裝套件可用時，一律可使用轉換。 請參閱 [內嵌轉換](embedded-transforms.md)。 Windows Installer SDK 中提供的範例是公用程式 WiSubStg.vbs。 下列程式碼片段 Emb.vbs，也會說明如何使用 [ [儲存體] 資料表](-storages-table.md) 來新增內嵌的轉換，並可用於 Windows Script Host。


```VB
'Emb.vbs. Argument(0) is the original database. Argument(1) is the
'    path to the transform file. Argument(2) is the name of the storage.
'
Option Explicit

' Check arguments
If WScript.Arguments.Count < 2 Then
 WScript.Echo "Usage is emb.vbs [original database] [transform] [storage name]"
 WScript.Quit(1)
End If

' Connect to Windows Installer object
On Error Resume Next
Dim installer : Set installer = Nothing
Set installer = Wscript.CreateObject("WindowsInstaller.Installer")
 
' Evaluate command-line arguments and set open and update modes
Dim databasePath: databasePath = Wscript.Arguments(0)
Dim importPath  : importPath = Wscript.Arguments(1)
Dim storageName : storageName = Wscript.Arguments(2)
 
' Open database and create a view on the _Storages table
Dim sqlQuery : sqlQuery = "SELECT `Name`,`Data` FROM _Storages"
Dim database : Set database = installer.OpenDatabase(databasePath, 1)
Dim view     : Set view = database.OpenView(sqlQuery)
 
'Create and Insert the row.
Dim record   : Set record = installer.CreateRecord(2)
record.StringData(1) = storageName
view.Execute record
 
'Insert storage - copy data into stream
record.SetStream 2, importPath
view.Modify 3, record
database.Commit
Set view = Nothing
Set database = Nothing
```



若要將名為 MNPtrans1 的儲存體新增至 MNP2000.msi，並包含您在 [將摘要資訊新增至自訂轉換](adding-summary-information-to-customization-transform.md)時所建立的轉換，請將目錄變更為包含 Emb.vbs、原始資料庫和轉換檔案的資料夾，然後輸入下列命令列。

**Cscript.exe Emb.vbs MNP2000.msi MNPtrans .mst MNPtrans1**

這樣就完成了自訂轉換範例。 在 MNPtrans 中內嵌轉換之後，安裝套件一律會提供轉換。 MNPtrans 檔案不需要位於來源，以套用轉換。

從包含範例安裝套件的資料夾中移除 MNPtrans。 按一下 MNP2000.msi 圖示以啟動安裝，或使用下列命令列。

**msiexec/i MNP2000.msi**

請注意，這會在沒有自訂專案的情況下安裝產品。 若要使用自訂安裝，請輸入下列命令列。 您可以使用冒號來指出 [ [**轉換**](transforms.md) ] 屬性的值是指內嵌的轉換。

msiexec/i MNP2000.msi 轉換 =： MNPtrans1

請注意，[閘道] 功能不會出現在功能選取樹狀目錄中，而且即使在使用者介面中選取了完整的安裝類型，也不會安裝閘道功能的元件。

## <a name="next-example"></a>下一個範例

[小型更新修補範例](a-small-update-patching-example.md)

 

 



