---
description: 若要在產品安裝期間套用自訂轉換，您必須將摘要資訊資料流程新增至產生自訂轉換時產生的轉換檔 MNPtrans。
ms.assetid: 586f6c43-7449-4d06-9201-9b4b4919871e
title: 將摘要資訊加入自訂轉換
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 64957fcf8f29ab8793517015c7018292ba9a6e69
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106974241"
---
# <a name="adding-summary-information-to-customization-transform"></a>將摘要資訊加入自訂轉換

若要在產品安裝期間套用自訂轉換，您必須將 [摘要資訊資料流程](summary-information-stream.md) 新增至產生 [自訂轉換](generating-a-customization-transform.md)時產生的轉換檔 MNPtrans。

您可以使用 [**MsiCreateTransformSummaryInfo**](/windows/desktop/api/Msiquery/nf-msiquery-msicreatetransformsummaryinfoa) 或 [**CreateTransformSummaryInfo 方法**](database-createtransformsummaryinfo.md)來產生轉換的摘要資訊。 下列程式碼片段（Sum.vbs）說明 [**CreateTransformSummaryInfo 方法**](database-createtransformsummaryinfo.md) ，並可用於 Windows Script Host。 請注意，此範例不會執行任何驗證，也不會隱藏任何錯誤狀況。


```VB
'Sum.vbs. Argument(0) is the original database. Argument(1) is the
'    customized database. Argument(2) is the transform file.
 
Option Explicit

' Check arguments
If WScript.Arguments.Count < 2 Then
    WScript.Echo "Usage is sum.vbs [original database] [customized database] [transform]"
    WScript.Quit(1)
End If

' Connect to Windows Installer object
On Error Resume Next
Dim installer : Set installer = Nothing
Set installer = Wscript.CreateObject("WindowsInstaller.Installer") 
 
' Open databases and transform 
Dim database1 : Set database1 =
    installer.OpenDatabase(Wscript.Arguments(0), 0) 
Dim database2 : Set database2 =
    installer.OpenDatabase(Wscript.Arguments(1), 0) 
Dim transform : transform = Wscript.Arguments(2)
 
' Create and add Summary Information
Dim transinfo : transinfo =
    Database2.CreateTransformSummaryInfo(Database1, transform,0,0)
```



若要建立摘要資訊，並將其新增至您在 [產生自訂轉換](generating-a-customization-transform.md)時建立的轉換檔案 MNPtrans，請將目錄變更為包含 Gen.vbs、原始資料庫、更新的資料庫和轉換的資料夾，然後輸入下列命令列。

**Cscript.exe Sum.vbs MNP2000.msi MNP2000t.msi MNPtrans**

按一下 MNP2000.msi 圖示以啟動安裝，或使用下列命令列。

**msiexec/i MNP2000.msi**

這會在沒有自訂專案的情況下安裝產品。 若要使用自訂安裝，請輸入下列命令列。 請注意，[ [**轉換**](transforms.md) ] 屬性的值是指位於來源的轉換檔案。

**msiexec/i MNP2000.msi 轉換 = MNPtrans .mst**

閘道功能不會出現在功能選取樹狀目錄中，而且即使在使用者介面中選取了完整的安裝類型，也不會安裝閘道功能的元件。

[繼續](embedding-customization-transforms-as-substorage.md)

 

 



