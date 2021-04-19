---
description: Windows Installer 開發人員 Windows SDK 元件中提供了 VBScript 檔案 WiLstScr.vbs。 此範例腳本示範 Windows Installer 腳本檢視器。
ms.assetid: 18989c16-e0c8-4d11-b915-730951b6845b
title: 查看安裝程式腳本
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 56888f478bb7cdd43ebcee817c86f6f9f163840e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106979021"
---
# <a name="view-installer-script"></a><span data-ttu-id="3758d-104">查看安裝程式腳本</span><span class="sxs-lookup"><span data-stu-id="3758d-104">View Installer Script</span></span>

<span data-ttu-id="3758d-105">[Windows Installer 開發人員 Windows SDK 元件](platform-sdk-components-for-windows-installer-developers.md)中提供了 VBScript 檔案 WiLstScr.vbs。</span><span class="sxs-lookup"><span data-stu-id="3758d-105">The VBScript file WiLstScr.vbs is provided in the [Windows SDK Components for Windows Installer Developers](platform-sdk-components-for-windows-installer-developers.md).</span></span> <span data-ttu-id="3758d-106">此範例腳本示範 Windows Installer 腳本檢視器。</span><span class="sxs-lookup"><span data-stu-id="3758d-106">This sample script demonstrates the Windows Installer script viewer.</span></span>

<span data-ttu-id="3758d-107">此範例將示範如何使用：</span><span class="sxs-lookup"><span data-stu-id="3758d-107">The sample demonstrates the use of:</span></span>

-   [<span data-ttu-id="3758d-108">**(安裝程式物件) 的 OpenDatabase 方法**</span><span class="sxs-lookup"><span data-stu-id="3758d-108">**OpenDatabase method (Installer Object)**</span></span>](installer-opendatabase.md)
-   <span data-ttu-id="3758d-109">[**安裝程式**](installer-object.md)物件的 [**LastErrorRecord**](installer-lasterrorrecord.md)方法</span><span class="sxs-lookup"><span data-stu-id="3758d-109">[**LastErrorRecord**](installer-lasterrorrecord.md) method of the [**Installer**](installer-object.md) object</span></span>
-   <span data-ttu-id="3758d-110">[**資料庫**](database-object.md)物件的 [**OpenView**](database-openview.md)方法</span><span class="sxs-lookup"><span data-stu-id="3758d-110">[**OpenView**](database-openview.md) method of the [**Database**](database-object.md) object</span></span>
-   <span data-ttu-id="3758d-111">[**View**](view-object.md)物件的 [**Fetch**](view-fetch.md)方法</span><span class="sxs-lookup"><span data-stu-id="3758d-111">[**Fetch**](view-fetch.md) method of the [**View**](view-object.md) object</span></span>
-   <span data-ttu-id="3758d-112">[**FormatText**](record-formattext.md) 方法</span><span class="sxs-lookup"><span data-stu-id="3758d-112">[**FormatText**](record-formattext.md) method</span></span>
-   <span data-ttu-id="3758d-113">[**FieldCount**](record-fieldcount.md) 屬性</span><span class="sxs-lookup"><span data-stu-id="3758d-113">[**FieldCount**](record-fieldcount.md) property</span></span>
-   <span data-ttu-id="3758d-114">[**Record**](record-object.md)物件的 [**至 convertfrom-stringdata**](record-stringdata.md)屬性</span><span class="sxs-lookup"><span data-stu-id="3758d-114">[**StringData**](record-stringdata.md) property of the [**Record**](record-object.md) object</span></span>
-   [<span data-ttu-id="3758d-115">\_TransformView 資料表</span><span class="sxs-lookup"><span data-stu-id="3758d-115">\_TransformView table</span></span>](-transformview-table.md)

<span data-ttu-id="3758d-116">使用此範例需要 CScript.exe 版本的 Windows Script Host。</span><span class="sxs-lookup"><span data-stu-id="3758d-116">Using this sample requires the CScript.exe version of Windows Script Host.</span></span> <span data-ttu-id="3758d-117">若要使用 CScript.exe 執行此範例，請使用下列語法在命令提示字元中輸入命令。</span><span class="sxs-lookup"><span data-stu-id="3758d-117">To use CScript.exe to run this sample, type a command at the command prompt using the following syntax.</span></span> <span data-ttu-id="3758d-118">如果第一個引數是/？，則會顯示說明</span><span class="sxs-lookup"><span data-stu-id="3758d-118">Help is displayed if the first argument is /?</span></span> <span data-ttu-id="3758d-119">或者，如果指定的引數太少。</span><span class="sxs-lookup"><span data-stu-id="3758d-119">or if too few arguments are specified.</span></span> <span data-ttu-id="3758d-120">若要將輸出重新導向至檔案，請以 VBS > 路徑結束命令列 \[  \] 。</span><span class="sxs-lookup"><span data-stu-id="3758d-120">To redirect the output to a file, end the command line with VBS > \[*path to file*\].</span></span> <span data-ttu-id="3758d-121">此範例會傳回值0表示成功，如果叫用說明，則傳回 1; 如果腳本失敗，則傳回2。</span><span class="sxs-lookup"><span data-stu-id="3758d-121">The sample returns a value of 0 for success, 1 if help is invoked, and 2 if the script fails.</span></span>

<span data-ttu-id="3758d-122">*\[ Windows Installer 執行腳本 \] 的* **cscript WiLstScr.vbs** 路徑</span><span class="sxs-lookup"><span data-stu-id="3758d-122">**cscript WiLstScr.vbs** *\[path to Windows Installer execution script\]*</span></span>

<span data-ttu-id="3758d-123">指定安裝程式執行腳本的路徑。</span><span class="sxs-lookup"><span data-stu-id="3758d-123">Specify the path to the installer execution script.</span></span>

<span data-ttu-id="3758d-124">如需其他腳本範例，請參閱 [Windows Installer 腳本範例](windows-installer-scripting-examples.md)。</span><span class="sxs-lookup"><span data-stu-id="3758d-124">For additional scripting examples, see [Windows Installer Scripting Examples](windows-installer-scripting-examples.md).</span></span> <span data-ttu-id="3758d-125">如需不需要 Windows Script Host 的範例公用程式，請參閱 [Windows Installer 開發工具](windows-installer-development-tools.md)。</span><span class="sxs-lookup"><span data-stu-id="3758d-125">For sample utilities that do not require Windows Script Host, see [Windows Installer Development Tools](windows-installer-development-tools.md).</span></span>

 

 



