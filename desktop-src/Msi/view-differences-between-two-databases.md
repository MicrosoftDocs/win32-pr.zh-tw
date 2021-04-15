---
description: Windows Installer 開發人員 Windows SDK 元件中提供了 VBScript 檔案 WiDiffDb.vbs。 此範例腳本會在兩個 Windows Installer 資料庫之間產生暫時的轉換檔案，並顯示轉換。
ms.assetid: 9750ddc6-de8d-48e9-a984-892f0cf4ac3b
title: 查看兩個資料庫之間的差異
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7b0c97afc0bd7145170209ed87497b6af90e64d6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104511244"
---
# <a name="view-differences-between-two-databases"></a><span data-ttu-id="ed36f-104">查看兩個資料庫之間的差異</span><span class="sxs-lookup"><span data-stu-id="ed36f-104">View Differences Between Two Databases</span></span>

<span data-ttu-id="ed36f-105">[Windows Installer 開發人員 Windows SDK 元件](platform-sdk-components-for-windows-installer-developers.md)中提供了 VBScript 檔案 WiDiffDb.vbs。</span><span class="sxs-lookup"><span data-stu-id="ed36f-105">The VBScript file WiDiffDb.vbs is provided in the [Windows SDK Components for Windows Installer Developers](platform-sdk-components-for-windows-installer-developers.md).</span></span> <span data-ttu-id="ed36f-106">此範例腳本會在兩個 Windows Installer 資料庫之間產生暫時的轉換檔案，並顯示轉換。</span><span class="sxs-lookup"><span data-stu-id="ed36f-106">This sample script generates a temporary transform file between two Windows Installer databases and displays the transform.</span></span>

<span data-ttu-id="ed36f-107">此範例將示範如何使用：</span><span class="sxs-lookup"><span data-stu-id="ed36f-107">The sample demonstrates the use of:</span></span>

-   [<span data-ttu-id="ed36f-108">**(安裝程式物件) 的 OpenDatabase 方法**</span><span class="sxs-lookup"><span data-stu-id="ed36f-108">**OpenDatabase method (Installer Object)**</span></span>](installer-opendatabase.md)
-   <span data-ttu-id="ed36f-109">[](installer-lasterrorrecord.md) [**安裝程式物件** 的 LastErrorRecord 方法](installer-object.md)</span><span class="sxs-lookup"><span data-stu-id="ed36f-109">[**LastErrorRecord method**](installer-lasterrorrecord.md) of the [**Installer object**](installer-object.md)</span></span>
-   [<span data-ttu-id="ed36f-110">**OpenView 方法**</span><span class="sxs-lookup"><span data-stu-id="ed36f-110">**OpenView method**</span></span>](database-openview.md)
-   [<span data-ttu-id="ed36f-111">**SummaryInformation 屬性 (資料庫物件)**</span><span class="sxs-lookup"><span data-stu-id="ed36f-111">**SummaryInformation property (Database Object)**</span></span>](database-summaryinformation.md)
-   [<span data-ttu-id="ed36f-112">**將方法**</span><span class="sxs-lookup"><span data-stu-id="ed36f-112">**GenerateTransform method**</span></span>](database-generatetransform.md)
-   [<span data-ttu-id="ed36f-113">**ApplyTransform 方法**</span><span class="sxs-lookup"><span data-stu-id="ed36f-113">**ApplyTransform method**</span></span>](database-applytransform.md)
-   [<span data-ttu-id="ed36f-114">**資料庫物件**</span><span class="sxs-lookup"><span data-stu-id="ed36f-114">**Database object**</span></span>](database-object.md)
-   <span data-ttu-id="ed36f-115">[](view-fetch.md) [ **View 物件** 的 Fetch 方法](view-object.md)</span><span class="sxs-lookup"><span data-stu-id="ed36f-115">[**Fetch method**](view-fetch.md) of the [**View object**](view-object.md)</span></span>
-   [<span data-ttu-id="ed36f-116">**IsNull 屬性**</span><span class="sxs-lookup"><span data-stu-id="ed36f-116">**IsNull property**</span></span>](record-isnull.md)
-   <span data-ttu-id="ed36f-117">[](record-stringdata.md) [ **Record 物件** 的至 convertfrom-stringdata 屬性](record-object.md)</span><span class="sxs-lookup"><span data-stu-id="ed36f-117">[**StringData property**](record-stringdata.md) of the [**Record object**](record-object.md)</span></span>
-   [<span data-ttu-id="ed36f-118">\_TransformView 資料表</span><span class="sxs-lookup"><span data-stu-id="ed36f-118">\_TransformView table</span></span>](-transformview-table.md)

<span data-ttu-id="ed36f-119">使用此範例需要 CScript.exe 版本的 Windows Script Host。</span><span class="sxs-lookup"><span data-stu-id="ed36f-119">Using this sample requires the CScript.exe version of Windows Script Host.</span></span> <span data-ttu-id="ed36f-120">若要使用 CScript.exe 執行此範例，請使用下列語法在命令提示字元中輸入命令。</span><span class="sxs-lookup"><span data-stu-id="ed36f-120">To use CScript.exe to run this sample, type a command at the command prompt using the following syntax.</span></span> <span data-ttu-id="ed36f-121">如果第一個引數是/？，則會顯示說明</span><span class="sxs-lookup"><span data-stu-id="ed36f-121">Help is displayed if the first argument is /?</span></span> <span data-ttu-id="ed36f-122">或者，如果指定的引數太少。</span><span class="sxs-lookup"><span data-stu-id="ed36f-122">or if too few arguments are specified.</span></span> <span data-ttu-id="ed36f-123">若要將輸出重新導向至檔案，請以 VBS > 路徑結束命令列 \[  \] 。</span><span class="sxs-lookup"><span data-stu-id="ed36f-123">To redirect the output to a file, end the command line with VBS > \[*path to file*\].</span></span> <span data-ttu-id="ed36f-124">此範例會傳回值0表示成功，如果叫用說明，則傳回 1; 如果腳本失敗，則傳回2。</span><span class="sxs-lookup"><span data-stu-id="ed36f-124">The sample returns a value of 0 for success, 1 if help is invoked, and 2 if the script fails.</span></span>

<span data-ttu-id="ed36f-125">**cscript WiDiffDb.vbs** *\[ 原始資料庫 \] \[ 路徑的軌跡，以修改 \] 資料庫*</span><span class="sxs-lookup"><span data-stu-id="ed36f-125">**cscript WiDiffDb.vbs** *\[path to original database\]\[path to revised database\]*</span></span>

<span data-ttu-id="ed36f-126">指定原始 Windows Installer 資料庫的路徑。</span><span class="sxs-lookup"><span data-stu-id="ed36f-126">Specify the path to the original Windows Installer database.</span></span> <span data-ttu-id="ed36f-127">指定已修改之資料庫的路徑。</span><span class="sxs-lookup"><span data-stu-id="ed36f-127">Specify the path to the revised database.</span></span> <span data-ttu-id="ed36f-128">範例腳本會顯示轉換。</span><span class="sxs-lookup"><span data-stu-id="ed36f-128">The sample script will display the transform.</span></span>

<span data-ttu-id="ed36f-129">如需其他腳本範例，請參閱 [Windows Installer 腳本範例](windows-installer-scripting-examples.md)。</span><span class="sxs-lookup"><span data-stu-id="ed36f-129">For additional scripting examples, see [Windows Installer Scripting Examples](windows-installer-scripting-examples.md).</span></span> <span data-ttu-id="ed36f-130">如需不需要 Windows Script Host 的範例公用程式，請參閱 [Windows Installer 開發工具](windows-installer-development-tools.md)。</span><span class="sxs-lookup"><span data-stu-id="ed36f-130">For sample utilities that do not require Windows Script Host, see [Windows Installer Development Tools](windows-installer-development-tools.md).</span></span>

 

 



