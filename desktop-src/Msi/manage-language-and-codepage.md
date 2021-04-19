---
description: Windows Installer 開發人員 Windows SDK 元件中提供了 VBScript 檔案 WiLangID.vbs。
ms.assetid: 319e9ffd-ff9f-4b4c-913e-2c571f2ec9ee
title: 管理語言和字碼頁
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3cbfb96f04d75ed79f32c8a49fe58b8dcc86f184
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106996968"
---
# <a name="manage-language-and-codepage"></a><span data-ttu-id="b3343-103">管理語言和字碼頁</span><span class="sxs-lookup"><span data-stu-id="b3343-103">Manage Language and Codepage</span></span>

<span data-ttu-id="b3343-104">[Windows Installer 開發人員 Windows SDK 元件](platform-sdk-components-for-windows-installer-developers.md)中提供了 VBScript 檔案 WiLangID.vbs。</span><span class="sxs-lookup"><span data-stu-id="b3343-104">The VBScript file WiLangID.vbs is provided in the [Windows SDK Components for Windows Installer Developers](platform-sdk-components-for-windows-installer-developers.md).</span></span> <span data-ttu-id="b3343-105">此範例說明如何使用腳本來存取套件的語言資訊和字碼頁。</span><span class="sxs-lookup"><span data-stu-id="b3343-105">This sample shows how script is used to access a package's language information and codepage.</span></span> <span data-ttu-id="b3343-106">如需詳細資訊，請參閱 (Windows Installer) [當地語系化 Windows Installer 封裝](localizing-a-windows-installer-package.md) 和 [字碼頁處理 ](code-page-handling-windows-installer-.md)。</span><span class="sxs-lookup"><span data-stu-id="b3343-106">For more information, see [Localizing a Windows Installer Package](localizing-a-windows-installer-package.md) and [Code Page Handling (Windows Installer)](code-page-handling-windows-installer-.md).</span></span>

<span data-ttu-id="b3343-107">此範例將示範如何使用：</span><span class="sxs-lookup"><span data-stu-id="b3343-107">The sample demonstrates the use of:</span></span>

-   [<span data-ttu-id="b3343-108">**(安裝程式物件) 的 OpenDatabase 方法**</span><span class="sxs-lookup"><span data-stu-id="b3343-108">**OpenDatabase method (Installer Object)**</span></span>](installer-opendatabase.md)
-   [<span data-ttu-id="b3343-109">**CreateRecord 方法**</span><span class="sxs-lookup"><span data-stu-id="b3343-109">**CreateRecord method**</span></span>](installer-createrecord.md)
-   <span data-ttu-id="b3343-110">[](installer-lasterrorrecord.md) [**安裝程式物件** 的 LastErrorRecord 方法](installer-object.md)</span><span class="sxs-lookup"><span data-stu-id="b3343-110">[**LastErrorRecord method**](installer-lasterrorrecord.md) of the [**Installer object**](installer-object.md)</span></span>
-   [<span data-ttu-id="b3343-111">**OpenView 方法**</span><span class="sxs-lookup"><span data-stu-id="b3343-111">**OpenView method**</span></span>](database-openview.md)
-   <span data-ttu-id="b3343-112">資料庫物件的 [**SummaryInformation 屬性 (資料庫物件)**](database-summaryinformation.md) [](database-object.md)</span><span class="sxs-lookup"><span data-stu-id="b3343-112">[**SummaryInformation property (Database Object)**](database-summaryinformation.md) of the [**Database object**](database-object.md)</span></span>

<span data-ttu-id="b3343-113">使用此範例需要 Windows Script Host 的 CScript.exe 或 WScript.exe 版本。</span><span class="sxs-lookup"><span data-stu-id="b3343-113">Using this sample requires the CScript.exe or WScript.exe version of Windows Script Host.</span></span> <span data-ttu-id="b3343-114">若要使用 CScript.exe 執行此範例，請使用下列語法在命令提示字元中輸入命令。</span><span class="sxs-lookup"><span data-stu-id="b3343-114">To use CScript.exe to run this sample, type a command at the command prompt using the following syntax.</span></span> <span data-ttu-id="b3343-115">如果第一個引數是/？，則會顯示說明</span><span class="sxs-lookup"><span data-stu-id="b3343-115">Help is displayed if the first argument is /?</span></span> <span data-ttu-id="b3343-116">或者，如果指定的引數太少。</span><span class="sxs-lookup"><span data-stu-id="b3343-116">or if too few arguments are specified.</span></span> <span data-ttu-id="b3343-117">若要將輸出重新導向至檔案，請以 VBS > 路徑結束命令列 \[  \] 。</span><span class="sxs-lookup"><span data-stu-id="b3343-117">To redirect the output to a file, end the command line with VBS > \[*path to file*\].</span></span> <span data-ttu-id="b3343-118">此範例會傳回值0表示成功，如果叫用說明，則傳回 1; 如果腳本失敗，則傳回2。</span><span class="sxs-lookup"><span data-stu-id="b3343-118">The sample returns a value of 0 for success, 1 if help is invoked, and 2 if the script fails.</span></span>

<span data-ttu-id="b3343-119">**cscript WiLangID.vbs \[ 資料庫 \] \[ 關鍵字 \] \[ 值的路徑\]**</span><span class="sxs-lookup"><span data-stu-id="b3343-119">**cscript WiLangID.vbs \[path to database\]\[keyword\]\[value\]**</span></span>

<span data-ttu-id="b3343-120">指定 Windows Installer 資料庫的路徑。</span><span class="sxs-lookup"><span data-stu-id="b3343-120">Specify the path to the Windows Installer database.</span></span> <span data-ttu-id="b3343-121">若要變更值，請指定下列其中一個關鍵字，並在後面加上新值。</span><span class="sxs-lookup"><span data-stu-id="b3343-121">To change a value specify one of the following keywords followed by the new value.</span></span> <span data-ttu-id="b3343-122">如果未指定任何值，此範例會傳回目前的值。</span><span class="sxs-lookup"><span data-stu-id="b3343-122">If no value is specified the sample returns the current value.</span></span>



| <span data-ttu-id="b3343-123">關鍵字</span><span class="sxs-lookup"><span data-stu-id="b3343-123">Keyword</span></span>      | <span data-ttu-id="b3343-124">描述</span><span class="sxs-lookup"><span data-stu-id="b3343-124">Description</span></span>                                                                                                                                                                                |
|--------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b3343-125">**套件**</span><span class="sxs-lookup"><span data-stu-id="b3343-125">**Package**</span></span>  | <span data-ttu-id="b3343-126">資料庫所支援的語言版本。</span><span class="sxs-lookup"><span data-stu-id="b3343-126">The language versions supported by the database.</span></span> <span data-ttu-id="b3343-127">如需詳細資訊，請參閱 [**範本摘要**](template-summary.md) 屬性。</span><span class="sxs-lookup"><span data-stu-id="b3343-127">For information, see [**Template Summary**](template-summary.md) property.</span></span>                                                               |
| <span data-ttu-id="b3343-128">**產品**</span><span class="sxs-lookup"><span data-stu-id="b3343-128">**Product**</span></span>  | <span data-ttu-id="b3343-129">安裝程式應針對使用者介面中未撰寫至資料庫的任何字串使用的語言。</span><span class="sxs-lookup"><span data-stu-id="b3343-129">Language the installer should use for any strings in the user interface that are not authored into the database.</span></span> <span data-ttu-id="b3343-130">如需詳細資訊，請參閱 [**ProductLanguage**](productlanguage.md) 屬性。</span><span class="sxs-lookup"><span data-stu-id="b3343-130">For information, see [**ProductLanguage**](productlanguage.md) property.</span></span> |
| <span data-ttu-id="b3343-131">**Codepage**</span><span class="sxs-lookup"><span data-stu-id="b3343-131">**Codepage**</span></span> | <span data-ttu-id="b3343-132">字串集區的單一 ANSI 字碼頁。</span><span class="sxs-lookup"><span data-stu-id="b3343-132">Single ANSI code page for the string pool.</span></span> <span data-ttu-id="b3343-133">如需詳細資訊，請參閱 [字碼頁處理 (Windows Installer) ](code-page-handling-windows-installer-.md)。</span><span class="sxs-lookup"><span data-stu-id="b3343-133">For information, see [Code Page Handling (Windows Installer)](code-page-handling-windows-installer-.md).</span></span>                                       |



 

<span data-ttu-id="b3343-134">如需其他腳本範例，請參閱 [Windows Installer 腳本範例](windows-installer-scripting-examples.md)。</span><span class="sxs-lookup"><span data-stu-id="b3343-134">For additional scripting examples, see [Windows Installer Scripting Examples](windows-installer-scripting-examples.md).</span></span> <span data-ttu-id="b3343-135">針對不需要 Windows Script Host 的範例公用程式，請參閱 [Windows Installer 開發工具](windows-installer-development-tools.md)。</span><span class="sxs-lookup"><span data-stu-id="b3343-135">For sample utilities that do not require Windows Script Host see [Windows Installer Development Tools](windows-installer-development-tools.md).</span></span>

<span data-ttu-id="b3343-136">如需詳細資訊，請參閱 [判斷安裝資料庫的字碼頁](determining-an-installation-database-s-code-page.md) 和 [設定資料庫的字碼頁](setting-the-code-page-of-a-database.md)。</span><span class="sxs-lookup"><span data-stu-id="b3343-136">For more information, see [Determining an Installation Database's Code Page](determining-an-installation-database-s-code-page.md) and [Setting the Code Page of a Database](setting-the-code-page-of-a-database.md).</span></span>

 

 



