---
description: 您可以使用 MsiDatabaseGenerateTransform 或 Database 物件的產生器方法來產生轉換檔案。
ms.assetid: c016fcba-0d54-4b99-bcdd-36967b2c9da0
title: 產生自訂轉換
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9f73609b7be60dbfe236d31ed5a865e86ff6e310
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106978019"
---
# <a name="generating-a-customization-transform"></a><span data-ttu-id="46178-103">產生自訂轉換</span><span class="sxs-lookup"><span data-stu-id="46178-103">Generating a Customization Transform</span></span>

<span data-ttu-id="46178-104">您可以使用 [**MsiDatabaseGenerateTransform**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabasegeneratetransforma)或 [**Database 物件**](database-object.md)的產生器 [**方法**](database-generatetransform.md)來產生轉換檔案。</span><span class="sxs-lookup"><span data-stu-id="46178-104">You may generate a transform file by using [**MsiDatabaseGenerateTransform**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabasegeneratetransforma) or the [**GenerateTransform method**](database-generatetransform.md) of the [**Database object**](database-object.md).</span></span> <span data-ttu-id="46178-105">Windows Installer SDK 中提供的範例是公用程式 WiGenXfm.vbs。</span><span class="sxs-lookup"><span data-stu-id="46178-105">An example of this is provided in the Windows Installer SDK as the utility WiGenXfm.vbs.</span></span> <span data-ttu-id="46178-106">下列程式碼片段（Gen.vbs）也會說明 **此提供** 器方法，並可用於 Windows Script Host。</span><span class="sxs-lookup"><span data-stu-id="46178-106">The following snippet, Gen.vbs, also illustrates the **GenerateTransform** method and is for use with Windows Script Host.</span></span>


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



<span data-ttu-id="46178-107">若要從原始 MNP2000.msi 資料庫和您在 [自訂原始資料庫](customizing-an-original-database.md)中修改的 MNP2000t.msi 資料庫產生轉換檔案 MNPtrans，請將目錄變更為包含 Gen.vbs、原始資料庫和更新的安裝程式資料庫的資料夾，然後輸入下列命令列。</span><span class="sxs-lookup"><span data-stu-id="46178-107">To generate the transform file MNPtrans.mst from the original MNP2000.msi database and the MNP2000t.msi database you modified in [Customizing an Original Database](customizing-an-original-database.md), change directories to the folder containing Gen.vbs, the original database, and the updated installer database and enter the following command line.</span></span>

<span data-ttu-id="46178-108">**Cscript.exe Gen.vbs MNP2000.msi MNP2000t.msi MNPtrans**</span><span class="sxs-lookup"><span data-stu-id="46178-108">**Cscript.exe Gen.vbs MNP2000.msi MNP2000t.msi MNPtrans.mst**</span></span>

[<span data-ttu-id="46178-109">繼續</span><span class="sxs-lookup"><span data-stu-id="46178-109">Continue</span></span>](adding-summary-information-to-customization-transform.md)

 

 



