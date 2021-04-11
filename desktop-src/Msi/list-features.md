---
description: Windows Installer 開發人員 Windows SDK 元件中提供了 VBScript 檔案 WiFeatur.vbs。
ms.assetid: 797cb383-22c0-42b4-82c1-d5bcc3a8bafb
title: 列出功能
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 67e166401b514f1beec9c14c74aba7ca0601f446
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104318999"
---
# <a name="list-features"></a><span data-ttu-id="022ac-103">列出功能</span><span class="sxs-lookup"><span data-stu-id="022ac-103">List Features</span></span>

<span data-ttu-id="022ac-104">[Windows Installer 開發人員 Windows SDK 元件](platform-sdk-components-for-windows-installer-developers.md)中提供了 VBScript 檔案 WiFeatur.vbs。</span><span class="sxs-lookup"><span data-stu-id="022ac-104">The VBScript file WiFeatur.vbs is provided in the [Windows SDK Components for Windows Installer Developers](platform-sdk-components-for-windows-installer-developers.md).</span></span> <span data-ttu-id="022ac-105">此範例說明如何使用腳本來列出 Windows Installer 資料庫中的功能。</span><span class="sxs-lookup"><span data-stu-id="022ac-105">This sample shows how script is used to list the features in a Windows Installer database.</span></span> <span data-ttu-id="022ac-106">這個範例示範如何將暫存資料行新增至唯讀的 Windows Installer 資料庫。</span><span class="sxs-lookup"><span data-stu-id="022ac-106">This sample demonstrates adding temporary columns to a read-only Windows Installer database.</span></span>

<span data-ttu-id="022ac-107">此範例示範：</span><span class="sxs-lookup"><span data-stu-id="022ac-107">This sample demonstrates:</span></span>

-   <span data-ttu-id="022ac-108">[**OpenDatabase 方法 (安裝程式物件)**](installer-opendatabase.md)、 [**CreateRecord 方法**](installer-createrecord.md)，以及 [**安裝程式物件**](installer-object.md)的 [**LastErrorRecord 方法**](installer-lasterrorrecord.md)</span><span class="sxs-lookup"><span data-stu-id="022ac-108">[**OpenDatabase method (Installer Object)**](installer-opendatabase.md), the [**CreateRecord method**](installer-createrecord.md), and the [**LastErrorRecord method**](installer-lasterrorrecord.md) of the [**Installer Object**](installer-object.md)</span></span>
-   <span data-ttu-id="022ac-109">[**Execute 方法**](view-execute.md)和 [**View 物件**](view-object.md)的 [**Fetch 方法**](view-fetch.md)</span><span class="sxs-lookup"><span data-stu-id="022ac-109">[**Execute method**](view-execute.md) and the [**Fetch method**](view-fetch.md) of the [**View Object**](view-object.md)</span></span>
-   <span data-ttu-id="022ac-110">[**OpenView 方法**](database-openview.md)、 [**TablePersistent 屬性**](database-tablepersistent.md)，以及 [**資料庫物件**](database-object.md)的 [**PrimaryKeys 屬性**](database-primarykeys.md)</span><span class="sxs-lookup"><span data-stu-id="022ac-110">[**OpenView method**](database-openview.md), the [**TablePersistent property**](database-tablepersistent.md), and the [**PrimaryKeys property**](database-primarykeys.md) of the [**Database Object**](database-object.md)</span></span>
-   <span data-ttu-id="022ac-111">[**FieldCount 屬性**](record-fieldcount.md)、 [**IntegerData 屬性**](record-integerdata.md)，以及 [**Record 物件**](record-object.md)的 [**至 convertfrom-stringdata 屬性**](record-stringdata.md)</span><span class="sxs-lookup"><span data-stu-id="022ac-111">[**FieldCount property**](record-fieldcount.md), [**IntegerData property**](record-integerdata.md), and the [**StringData property**](record-stringdata.md) of the [**Record Object**](record-object.md)</span></span>

<span data-ttu-id="022ac-112">使用此範例需要 Windows Script Host 的 CScript.exe 或 WScript.exe 版本。</span><span class="sxs-lookup"><span data-stu-id="022ac-112">Using this sample requires the CScript.exe or WScript.exe version of Windows Script Host.</span></span> <span data-ttu-id="022ac-113">若要使用 CScript.exe 執行此範例，請使用下列語法在命令提示字元中輸入命令。</span><span class="sxs-lookup"><span data-stu-id="022ac-113">To use CScript.exe to run this sample, type a command at the command prompt using the following syntax.</span></span> <span data-ttu-id="022ac-114">如果第一個引數是/？，則會顯示說明</span><span class="sxs-lookup"><span data-stu-id="022ac-114">Help is displayed if the first argument is /?</span></span> <span data-ttu-id="022ac-115">或者，如果指定的引數太少。</span><span class="sxs-lookup"><span data-stu-id="022ac-115">or if too few arguments are specified.</span></span> <span data-ttu-id="022ac-116">若要將輸出重新導向至檔案，請以 VBS > 路徑結束命令列 \[  \] 。</span><span class="sxs-lookup"><span data-stu-id="022ac-116">To redirect the output to a file, end the command line with VBS > \[*path to file*\].</span></span> <span data-ttu-id="022ac-117">此範例會傳回值0表示成功，如果叫用說明，則傳回 1; 如果腳本失敗，則傳回2。</span><span class="sxs-lookup"><span data-stu-id="022ac-117">The sample returns a value of 0 for success, 1 if help is invoked, and 2 if the script fails.</span></span>

<span data-ttu-id="022ac-118">**cscript WiFeatur.vbs \[ 資料庫 \] \[ 功能名稱的路徑\]**</span><span class="sxs-lookup"><span data-stu-id="022ac-118">**cscript WiFeatur.vbs \[path to database\]\[feature name\]**</span></span>

<span data-ttu-id="022ac-119">指定 Windows Installer 資料庫的路徑。</span><span class="sxs-lookup"><span data-stu-id="022ac-119">Specify path to the Windows Installer database.</span></span> <span data-ttu-id="022ac-120">指定功能的名稱。</span><span class="sxs-lookup"><span data-stu-id="022ac-120">Specify the name of the feature.</span></span> <span data-ttu-id="022ac-121">這必須列在 [功能資料表](feature-table.md)的 [功能] 資料行中。</span><span class="sxs-lookup"><span data-stu-id="022ac-121">This must be listed in the Feature column of the [Feature table](feature-table.md).</span></span> <span data-ttu-id="022ac-122">如果省略功能的名稱，則會將所有功能列為功能樹狀目錄。</span><span class="sxs-lookup"><span data-stu-id="022ac-122">If the name of the feature is omitted, all the features are listed as a feature tree.</span></span> <span data-ttu-id="022ac-123">如果使用星號 (\*) 做為功能名稱，WiFeatur.vbs 會列出所有功能的組合。</span><span class="sxs-lookup"><span data-stu-id="022ac-123">If an asterisk (\*) is used as the feature name, WiFeatur.vbs lists the composition of all features.</span></span> <span data-ttu-id="022ac-124">請注意，使用 CScript 而非 Wscript.echo，可以更妥善地顯示大型資料庫。</span><span class="sxs-lookup"><span data-stu-id="022ac-124">Note that large databases are better displayed using CScript rather than WScript.</span></span>

<span data-ttu-id="022ac-125">如需詳細資訊，請參閱 [Windows Installer 腳本範例](windows-installer-scripting-examples.md) ，以取得其他腳本範例。</span><span class="sxs-lookup"><span data-stu-id="022ac-125">For more information, see [Windows Installer Scripting Examples](windows-installer-scripting-examples.md) for additional scripting examples.</span></span> <span data-ttu-id="022ac-126">針對不需要 Windows Script Host 的範例公用程式，請參閱 [Windows Installer 開發工具](windows-installer-development-tools.md)。</span><span class="sxs-lookup"><span data-stu-id="022ac-126">For sample utilities that do not require Windows Script Host see [Windows Installer Development Tools](windows-installer-development-tools.md).</span></span>

 

 



