---
description: Windows Installer 開發人員 Windows SDK 元件中提供了 VBScript 檔案 WiCompon.vbs。 這個範例腳本可以用來列出 Windows Installer 資料庫中的元件。
ms.assetid: 4e6cc6f4-821a-4a10-a897-5c6aace1f702
title: 列出元件
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b79fa34f62374632ec7fdf52a13c6da8ddbfd82a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103690528"
---
# <a name="list-components"></a><span data-ttu-id="d474b-104">列出元件</span><span class="sxs-lookup"><span data-stu-id="d474b-104">List Components</span></span>

<span data-ttu-id="d474b-105">[Windows Installer 開發人員 Windows SDK 元件](platform-sdk-components-for-windows-installer-developers.md)中提供了 VBScript 檔案 WiCompon.vbs。</span><span class="sxs-lookup"><span data-stu-id="d474b-105">The VBScript file WiCompon.vbs is provided in the [Windows SDK Components for Windows Installer Developers](platform-sdk-components-for-windows-installer-developers.md).</span></span> <span data-ttu-id="d474b-106">這個範例腳本可以用來列出 Windows Installer 資料庫中的元件。</span><span class="sxs-lookup"><span data-stu-id="d474b-106">This sample script can be used to list the components in a Windows Installer database.</span></span>

<span data-ttu-id="d474b-107">這個範例會示範如何在 [元件資料表](component-table.md)中使用不同的主要索引鍵。</span><span class="sxs-lookup"><span data-stu-id="d474b-107">This sample demonstrates using the various primary key in the [Component table](component-table.md).</span></span>

<span data-ttu-id="d474b-108">此範例也會示範：</span><span class="sxs-lookup"><span data-stu-id="d474b-108">The sample also demonstrates:</span></span>

-   <span data-ttu-id="d474b-109">[**OpenDatabase 方法 (安裝程式物件)**](installer-opendatabase.md)、 [**CreateRecord 方法**](installer-createrecord.md)，以及 [**安裝程式物件**](installer-object.md)的 [**LastErrorRecord 方法**](installer-lasterrorrecord.md)。</span><span class="sxs-lookup"><span data-stu-id="d474b-109">[**OpenDatabase method (Installer Object)**](installer-opendatabase.md), the [**CreateRecord method**](installer-createrecord.md), and the [**LastErrorRecord method**](installer-lasterrorrecord.md) of the [**Installer Object**](installer-object.md).</span></span>
-   <span data-ttu-id="d474b-110">[**OpenView 方法**](database-openview.md)、 [**TablePersistent 屬性**](database-tablepersistent.md)，以及 [**資料庫物件**](database-object.md)的 [**PrimaryKeys 屬性**](database-primarykeys.md)。</span><span class="sxs-lookup"><span data-stu-id="d474b-110">[**OpenView method**](database-openview.md), the [**TablePersistent property**](database-tablepersistent.md), and the [**PrimaryKeys property**](database-primarykeys.md) of the [**Database Object**](database-object.md).</span></span>
-   <span data-ttu-id="d474b-111">[**Execute 方法**](view-execute.md)和 [**View 物件**](view-object.md)的 [**Fetch 方法**](view-fetch.md)。</span><span class="sxs-lookup"><span data-stu-id="d474b-111">[**Execute method**](view-execute.md) and the [**Fetch method**](view-fetch.md) of the [**View Object**](view-object.md).</span></span>
-   <span data-ttu-id="d474b-112">[**Record 物件**](record-object.md)的 [**至 convertfrom-stringdata 屬性**](record-stringdata.md)（property）屬性（property）。</span><span class="sxs-lookup"><span data-stu-id="d474b-112">[**StringData property**](record-stringdata.md) property of the [**Record Object**](record-object.md).</span></span>

<span data-ttu-id="d474b-113">使用此範例需要 Windows Script Host 的 CScript.exe 或 WScript.exe 版本。</span><span class="sxs-lookup"><span data-stu-id="d474b-113">Using this sample requires the CScript.exe or WScript.exe version of Windows Script Host.</span></span> <span data-ttu-id="d474b-114">若要使用 CScript.exe 執行此範例，請使用下列語法在命令提示字元中輸入命令。</span><span class="sxs-lookup"><span data-stu-id="d474b-114">To use CScript.exe to run this sample, type a command at the command prompt using the following syntax.</span></span> <span data-ttu-id="d474b-115">如果第一個引數是/？，則會顯示說明</span><span class="sxs-lookup"><span data-stu-id="d474b-115">Help is displayed if the first argument is /?</span></span> <span data-ttu-id="d474b-116">或者，如果指定的引數太少。</span><span class="sxs-lookup"><span data-stu-id="d474b-116">or if too few arguments are specified.</span></span> <span data-ttu-id="d474b-117">若要將輸出重新導向至檔案，請以 VBS > 路徑結束命令列 \[  \] 。</span><span class="sxs-lookup"><span data-stu-id="d474b-117">To redirect the output to a file, end the command line with VBS > \[*path to file*\].</span></span> <span data-ttu-id="d474b-118">此範例會傳回值0表示成功，如果叫用說明，則傳回 1; 如果腳本失敗，則傳回2。</span><span class="sxs-lookup"><span data-stu-id="d474b-118">The sample returns a value of 0 for success, 1 if help is invoked, and 2 if the script fails.</span></span>

<span data-ttu-id="d474b-119">**cscript WiCompon.vbs \[ 資料庫 \] \[ 元件名稱的路徑\]**</span><span class="sxs-lookup"><span data-stu-id="d474b-119">**cscript WiCompon.vbs \[path to database\]\[component name\]**</span></span>

<span data-ttu-id="d474b-120">指定 Windows Installer 資料庫的路徑。</span><span class="sxs-lookup"><span data-stu-id="d474b-120">Specify path to the Windows Installer database.</span></span> <span data-ttu-id="d474b-121">指定元件的名稱。</span><span class="sxs-lookup"><span data-stu-id="d474b-121">Specify the name of the component.</span></span> <span data-ttu-id="d474b-122">此名稱必須列在 [元件資料表](component-table.md)的元件資料行中。</span><span class="sxs-lookup"><span data-stu-id="d474b-122">The name must be listed in the Component column of the [Component table](component-table.md).</span></span> <span data-ttu-id="d474b-123">如果省略元件的名稱，則會列出所有的元件。</span><span class="sxs-lookup"><span data-stu-id="d474b-123">If the name of the component is omitted all the components are listed.</span></span> <span data-ttu-id="d474b-124">如果使用星號 (\*) 作為元件名稱，WiCompon.vbs 會列出所有元件的組合。</span><span class="sxs-lookup"><span data-stu-id="d474b-124">If an asterisk (\*) is used as the component name, WiCompon.vbs lists the composition of all components.</span></span> <span data-ttu-id="d474b-125">請注意，使用 CScript 而非 Wscript.echo，可以更妥善地顯示大型資料庫。</span><span class="sxs-lookup"><span data-stu-id="d474b-125">Note that large databases are better displayed using CScript rather than WScript.</span></span>

<span data-ttu-id="d474b-126">如需其他腳本範例，請參閱 [Windows Installer 腳本範例](windows-installer-scripting-examples.md)。</span><span class="sxs-lookup"><span data-stu-id="d474b-126">For additional scripting examples, see [Windows Installer Scripting Examples](windows-installer-scripting-examples.md).</span></span> <span data-ttu-id="d474b-127">如需不需要 Windows Script Host 的範例公用程式，請參閱 [Windows Installer 開發工具](windows-installer-development-tools.md)。</span><span class="sxs-lookup"><span data-stu-id="d474b-127">For sample utilities that do not require Windows Script Host, see [Windows Installer Development Tools](windows-installer-development-tools.md).</span></span>

 

 



