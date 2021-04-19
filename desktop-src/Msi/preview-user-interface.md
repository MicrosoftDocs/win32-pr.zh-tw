---
description: Windows Installer 開發人員 Windows SDK 元件中提供了 VBScript 檔案 WiDialog.vbs。 此範例說明如何使用腳本來預覽 Windows Installer 資料庫中的對話方塊。
ms.assetid: b3d72ba1-1d19-4460-8b9b-94f72214e8b1
title: 預覽消費者介面
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7736c442cdfcb22034326ff459eb89fc28b0c9af
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106989455"
---
# <a name="preview-user-interface"></a><span data-ttu-id="26650-104">預覽消費者介面</span><span class="sxs-lookup"><span data-stu-id="26650-104">Preview User Interface</span></span>

<span data-ttu-id="26650-105">[Windows Installer 開發人員 Windows SDK 元件](platform-sdk-components-for-windows-installer-developers.md)中提供了 VBScript 檔案 WiDialog.vbs。</span><span class="sxs-lookup"><span data-stu-id="26650-105">The VBScript file WiDialog.vbs is provided in the [Windows SDK Components for Windows Installer Developers](platform-sdk-components-for-windows-installer-developers.md).</span></span> <span data-ttu-id="26650-106">此範例說明如何使用腳本來預覽 Windows Installer 資料庫中的對話方塊。</span><span class="sxs-lookup"><span data-stu-id="26650-106">This sample shows how script is used to preview dialogs in a Windows Installer database.</span></span>

<span data-ttu-id="26650-107">此範例示範：</span><span class="sxs-lookup"><span data-stu-id="26650-107">This sample demonstrates:</span></span>

-   <span data-ttu-id="26650-108">[**OpenDatabase 方法 (安裝程式物件)**](installer-opendatabase.md)、 [**CreateRecord 方法**](installer-createrecord.md)，以及 [**安裝程式物件**](installer-object.md)的 [**LastErrorRecord 方法**](installer-lasterrorrecord.md)</span><span class="sxs-lookup"><span data-stu-id="26650-108">[**OpenDatabase method (Installer Object)**](installer-opendatabase.md), the [**CreateRecord method**](installer-createrecord.md), and the [**LastErrorRecord method**](installer-lasterrorrecord.md) of the [**Installer Object**](installer-object.md)</span></span>
-   <span data-ttu-id="26650-109">[**OpenView 方法**](database-openview.md)和 [**資料庫物件**](database-object.md)的 [**EnableUIpreview 方法**](database-enableuipreview.md)</span><span class="sxs-lookup"><span data-stu-id="26650-109">[**OpenView method**](database-openview.md) and the [**EnableUIpreview method**](database-enableuipreview.md) of the [**Database Object**](database-object.md)</span></span>
-   <span data-ttu-id="26650-110">[**Execute 方法**](view-execute.md)和 [**View 物件**](view-object.md)的 [**Fetch 方法**](view-fetch.md)</span><span class="sxs-lookup"><span data-stu-id="26650-110">[**Execute method**](view-execute.md) and the [**Fetch method**](view-fetch.md) of the [**View Object**](view-object.md)</span></span>
-   <span data-ttu-id="26650-111">[**至 convertfrom-stringdata 屬性**](record-stringdata.md) Propertyof [**記錄物件**](record-object.md)</span><span class="sxs-lookup"><span data-stu-id="26650-111">[**StringData property**](record-stringdata.md) propertyof the [**Record Object**](record-object.md)</span></span>

<span data-ttu-id="26650-112">此範例需要 Windows Script Host 的 CScript.exe 或 WScript.exe 版本。</span><span class="sxs-lookup"><span data-stu-id="26650-112">This sample requires the CScript.exe or WScript.exe version of Windows Script Host.</span></span> <span data-ttu-id="26650-113">若要使用此範例的 CScript.exe，請使用下列語法在命令提示字元中輸入命令。</span><span class="sxs-lookup"><span data-stu-id="26650-113">To use CScript.exe for this sample, type a command at the command prompt using the following syntax.</span></span> <span data-ttu-id="26650-114">如果第一個引數是/？，則會顯示說明</span><span class="sxs-lookup"><span data-stu-id="26650-114">Help is displayed if the first argument is /?</span></span> <span data-ttu-id="26650-115">或者，如果指定的引數太少。</span><span class="sxs-lookup"><span data-stu-id="26650-115">or if too few arguments are specified.</span></span> <span data-ttu-id="26650-116">若要將輸出重新導向至檔案，請以 VBS > 路徑結束命令列 \[  \] 。</span><span class="sxs-lookup"><span data-stu-id="26650-116">To redirect the output to a file, end the command line with VBS > \[*path to file*\].</span></span> <span data-ttu-id="26650-117">此範例會傳回值0表示成功，如果叫用說明，則傳回 1; 如果腳本失敗，則傳回2。</span><span class="sxs-lookup"><span data-stu-id="26650-117">The sample returns a value of 0 for success, 1 if help is invoked, and 2 if the script fails.</span></span>

<span data-ttu-id="26650-118">**cscript WiDialog.vbs** *\[ 資料庫 \] \[ 對話方塊名稱 \] 的路徑*</span><span class="sxs-lookup"><span data-stu-id="26650-118">**cscript WiDialog.vbs** *\[path to database\]\[Dialog names\]*</span></span>

<span data-ttu-id="26650-119">指定 Windows Installer 資料庫的路徑。</span><span class="sxs-lookup"><span data-stu-id="26650-119">Specify the path to a Windows Installer database.</span></span> <span data-ttu-id="26650-120">指定對話方塊的名稱。</span><span class="sxs-lookup"><span data-stu-id="26650-120">Specify the name of a dialog.</span></span> <span data-ttu-id="26650-121">這個名稱必須列在 [對話方塊資料表](dialog-table.md)的對話方塊資料行中。</span><span class="sxs-lookup"><span data-stu-id="26650-121">This name must be listed in the Dialog column of the [Dialog table](dialog-table.md).</span></span> <span data-ttu-id="26650-122">若要觀看佈告欄，請 [以控制項的](control-table.md) 名稱附加對話名稱，並將其附加至 [佈告欄資料表](billboard-table.md)中的佈告欄名稱。</span><span class="sxs-lookup"><span data-stu-id="26650-122">To view a billboard, append the dialog's name with the control's name from the [Control table](control-table.md) and append this to the name of the billboard in the [Billboard table](billboard-table.md).</span></span> <span data-ttu-id="26650-123">如果未指定對話方塊，則會依序顯示對話方塊資料表中的所有對話方塊。</span><span class="sxs-lookup"><span data-stu-id="26650-123">If no dialogs are specified, all dialogs in Dialog table are displayed sequentially.</span></span>

<span data-ttu-id="26650-124">如需其他腳本範例，請參閱 [Windows Installer 腳本範例](windows-installer-scripting-examples.md)。</span><span class="sxs-lookup"><span data-stu-id="26650-124">For additional scripting examples, see [Windows Installer Scripting Examples](windows-installer-scripting-examples.md).</span></span> <span data-ttu-id="26650-125">如需不需要 Windows Script Host 的範例公用程式，請參閱 [Windows Installer 開發工具](windows-installer-development-tools.md)。</span><span class="sxs-lookup"><span data-stu-id="26650-125">For sample utilities that do not require Windows Script Host, see [Windows Installer Development Tools](windows-installer-development-tools.md).</span></span>

 

 



