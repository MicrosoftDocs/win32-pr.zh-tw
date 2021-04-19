---
description: 錯誤資料表和 ActionText 資料表的當地語系化語言版本是由 Windows Installer SDK 提供。 這些資料表的法文語言版本法文和 ActionTe 法文，都位於 Windows Installer SDK 的 [國際] 資料夾中。
ms.assetid: 8de687c8-c7da-497e-8a90-2404096ad100
title: 匯入當地語系化的錯誤和 ActionText 資料表
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 15d48a68ca1053a1a1c66899a17802ac337c3ba2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106981012"
---
# <a name="importing-localized-error-and-actiontext-tables"></a><span data-ttu-id="8809d-104">匯入當地語系化的錯誤和 ActionText 資料表</span><span class="sxs-lookup"><span data-stu-id="8809d-104">Importing Localized Error and ActionText Tables</span></span>

<span data-ttu-id="8809d-105">[錯誤資料表](error-table.md)和[ActionText 資料表](actiontext-table.md)的當地語系化語言版本是由 Windows Installer SDK 提供。</span><span class="sxs-lookup"><span data-stu-id="8809d-105">Localized language versions of the [Error table](error-table.md) and [ActionText table](actiontext-table.md) are provided by the Windows Installer SDK.</span></span> <span data-ttu-id="8809d-106">這些資料表的法文語言版本法文和 ActionTe 法文，都位於 Windows Installer SDK 的 [國際] 資料夾中。</span><span class="sxs-lookup"><span data-stu-id="8809d-106">The French language versions of these tables, Error.FRA and ActionTe.FRA, are located in the Intl folder of the Windows Installer SDK.</span></span>

<span data-ttu-id="8809d-107">您可以使用資料表編輯器 Orca 或 SDK 隨附的公用程式 Msidb.exe，將這些資料表的法文版本匯入資料庫中。</span><span class="sxs-lookup"><span data-stu-id="8809d-107">You may use the table editor Orca or the utility Msidb.exe provided with the SDK to import the French versions of these tables into the database.</span></span>

<span data-ttu-id="8809d-108">使用 [**MsiDatabaseImport**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabaseimporta)的範例和 [**資料庫物件**](database-object.md)的匯 [**入方法**](database-import.md)，會以公用程式 WiImport.vbs 的形式在 Windows Installer SDK 中提供。</span><span class="sxs-lookup"><span data-stu-id="8809d-108">An example of using [**MsiDatabaseImport**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabaseimporta) and the [**Import Method**](database-import.md) of the [**Database object**](database-object.md) is provided in the Windows Installer SDK as the utility WiImport.vbs.</span></span> <span data-ttu-id="8809d-109">下列程式碼片段 Imp.vbs 也說明了匯入方法的使用方式，並可用於 Windows Script Host。</span><span class="sxs-lookup"><span data-stu-id="8809d-109">The following snippet, Imp.vbs, also illustrates the use of the Import method and is for use with Windows Script Host.</span></span>


```VB
'Imp.vbs. Argument(0) is the original database. Argument(1) is the
'    path of the folder containing the file to be imported. Argument(2) is the name of the file to be imported.
'
Option Explicit

' Check arguments
If WScript.Arguments.Count < 2 Then
    WScript.Echo "Usage is imp.vbs [original database] [folder path] [import file]"
    WScript.Quit(1)
End If

' Connect to Windows Installer object
On Error Resume Next
Dim installer : Set installer = Wscript.CreateObject("WindowsInstaller.Installer")
Dim databasePath : databasePath = Wscript.Arguments(0)
Dim folder : folder = Wscript.Arguments(1)
 
' Open database and process file
Dim database : Set database = installer.OpenDatabase(databasePath, 1)
Dim table : table = Wscript.Arguments(2)
database.Import folder, table 
 
' Commit database changes
database.Commit 'commit changes
Wscript.Quit 0
```



<span data-ttu-id="8809d-110">若要匯入並將錯誤資料表取代為 Error。法文您可以使用如下所示的命令列。</span><span class="sxs-lookup"><span data-stu-id="8809d-110">To import and replace the Error table with Error.FRA you may use a command line such as the following.</span></span>

<span data-ttu-id="8809d-111">**Cscript Imp.vbs MNPFren.msi C： \\ Note \_ 安裝程式 \\ 法文 Error. 法文**</span><span class="sxs-lookup"><span data-stu-id="8809d-111">**Cscript Imp.vbs MNPFren.msi C:\\Note\_Installer\\French Error.FRA**</span></span>

<span data-ttu-id="8809d-112">若要匯入並以 ActionTe 取代 ActionText 資料表，您可以使用如下所示的命令列。</span><span class="sxs-lookup"><span data-stu-id="8809d-112">To import and replace the ActionText table with ActionTe.FRA you may use a command line such as the following.</span></span>

<span data-ttu-id="8809d-113">**Cscript Imp.vbs MNPFren.msi C： \\ Note \_ 安裝程式 \\ 法文 ActionTe. 法文**</span><span class="sxs-lookup"><span data-stu-id="8809d-113">**Cscript Imp.vbs MNPFren.msi C:\\Note\_Installer\\French ActionTe.FRA**</span></span>

<span data-ttu-id="8809d-114">在 MNPFren.msi 上重新執行驗證，如 [驗證安裝升級](validating-an-installation-upgrade.md)中所述。</span><span class="sxs-lookup"><span data-stu-id="8809d-114">Rerun validation on MNPFren.msi as described in [Validating an Installation Upgrade](validating-an-installation-upgrade.md).</span></span>

[<span data-ttu-id="8809d-115">繼續</span><span class="sxs-lookup"><span data-stu-id="8809d-115">Continue</span></span>](localizing-database-columns.md)

 

 



