---
description: Orca.exe 是用來建立和編輯 Windows Installer 封裝和合併模組的資料庫資料表編輯器。
ms.assetid: 4dddc262-1271-4e00-a986-53380b957b17
title: Orca.exe
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e3f17874e08fcdbfdbab38c480219579897b9896
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104026162"
---
# <a name="orcaexe"></a><span data-ttu-id="46e0f-103">Orca.exe</span><span class="sxs-lookup"><span data-stu-id="46e0f-103">Orca.exe</span></span>

<span data-ttu-id="46e0f-104">Orca.exe 是用來建立和編輯 Windows Installer 封裝和合併模組的資料庫資料表編輯器。</span><span class="sxs-lookup"><span data-stu-id="46e0f-104">Orca.exe is a database table editor for creating and editing Windows Installer packages and merge modules.</span></span> <span data-ttu-id="46e0f-105">此工具會提供用於驗證的圖形化介面，並反白顯示驗證錯誤或警告發生的特定專案。</span><span class="sxs-lookup"><span data-stu-id="46e0f-105">The tool provides a graphical interface for validation, highlighting the particular entries where validation errors or warnings occur.</span></span>

<span data-ttu-id="46e0f-106">此工具僅適用于 [Windows Installer 開發人員的 Windows SDK 元件](platform-sdk-components-for-windows-installer-developers.md)。</span><span class="sxs-lookup"><span data-stu-id="46e0f-106">This tool is only available in the [Windows SDK Components for Windows Installer Developers](platform-sdk-components-for-windows-installer-developers.md).</span></span> <span data-ttu-id="46e0f-107">它是以 Orca.msi 檔案的形式提供。</span><span class="sxs-lookup"><span data-stu-id="46e0f-107">It is provided as an Orca.msi file.</span></span> <span data-ttu-id="46e0f-108">安裝適用于 Windows Installer 開發人員的 Windows SDK 元件之後，請按兩下 Orca.msi 以安裝 Orca.exe 檔。</span><span class="sxs-lookup"><span data-stu-id="46e0f-108">After installing the Windows SDK Components for Windows Installer Developers, double click Orca.msi to install the Orca.exe file.</span></span>

## <a name="syntax"></a><span data-ttu-id="46e0f-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="46e0f-109">Syntax</span></span>

<span data-ttu-id="46e0f-110">\**orca\*\*\*\[<options>\]\[<source file>\]*</span><span class="sxs-lookup"><span data-stu-id="46e0f-110">**orca** *\[<options>\]\[<source file>\]*</span></span>

## <a name="command-line-options"></a><span data-ttu-id="46e0f-111">命令列選項</span><span class="sxs-lookup"><span data-stu-id="46e0f-111">Command Line Options</span></span>

<span data-ttu-id="46e0f-112">Orca.exe 會使用下列不區分大小寫的命令列選項。</span><span class="sxs-lookup"><span data-stu-id="46e0f-112">Orca.exe uses the following case-insensitive command line options.</span></span> <span data-ttu-id="46e0f-113">斜線分隔符號也可以用來取代虛線。</span><span class="sxs-lookup"><span data-stu-id="46e0f-113">A slash delimiter may also be used in place of a dash.</span></span>



| <span data-ttu-id="46e0f-114">選項</span><span class="sxs-lookup"><span data-stu-id="46e0f-114">Option</span></span> | <span data-ttu-id="46e0f-115">Description</span><span class="sxs-lookup"><span data-stu-id="46e0f-115">Description</span></span>                                                 |
|--------|-------------------------------------------------------------|
| <span data-ttu-id="46e0f-116">-Q</span><span class="sxs-lookup"><span data-stu-id="46e0f-116">-q</span></span>     | <span data-ttu-id="46e0f-117">無訊息模式</span><span class="sxs-lookup"><span data-stu-id="46e0f-117">Quiet mode</span></span>                                                  |
| <span data-ttu-id="46e0f-118">-S</span><span class="sxs-lookup"><span data-stu-id="46e0f-118">-s</span></span>     | <span data-ttu-id="46e0f-119"><*database*> 架構資料庫 \[ "orca"-預設\]</span><span class="sxs-lookup"><span data-stu-id="46e0f-119"><*database*> Schema database \["orca.dat" - default\]</span></span> |
| <span data-ttu-id="46e0f-120">-?</span><span class="sxs-lookup"><span data-stu-id="46e0f-120">-?</span></span>     | <span data-ttu-id="46e0f-121">說明對話方塊</span><span class="sxs-lookup"><span data-stu-id="46e0f-121">Help dialog</span></span>                                                 |



 

<span data-ttu-id="46e0f-122">Orca.exe 在合併模組中使用下列不區分大小寫的命令列選項。</span><span class="sxs-lookup"><span data-stu-id="46e0f-122">Orca.exe uses the following case-insensitive command line options with merge modules.</span></span> <span data-ttu-id="46e0f-123">斜線分隔符號也可以用來取代虛線。</span><span class="sxs-lookup"><span data-stu-id="46e0f-123">A slash delimiter may also be used in place of a dash.</span></span> <span data-ttu-id="46e0f-124">執行 merge 時，-f、-m 和 <*sourcefile*> 全部都是必要的。</span><span class="sxs-lookup"><span data-stu-id="46e0f-124">When performing a merge the -f, -m and <*sourcefile*> are all required.</span></span>



| <span data-ttu-id="46e0f-125">選項</span><span class="sxs-lookup"><span data-stu-id="46e0f-125">Option</span></span>     | <span data-ttu-id="46e0f-126">描述</span><span class="sxs-lookup"><span data-stu-id="46e0f-126">Description</span></span>                                                                |
|------------|----------------------------------------------------------------------------|
| <span data-ttu-id="46e0f-127">-c</span><span class="sxs-lookup"><span data-stu-id="46e0f-127">-c</span></span>         | <span data-ttu-id="46e0f-128">如果沒有錯誤，請將 merge 認可至資料庫。</span><span class="sxs-lookup"><span data-stu-id="46e0f-128">Commit merge to database if no errors.</span></span>                                     |
| <span data-ttu-id="46e0f-129">-!</span><span class="sxs-lookup"><span data-stu-id="46e0f-129">-!</span></span>         | <span data-ttu-id="46e0f-130">即使發生錯誤，也會將合併認可至資料庫。</span><span class="sxs-lookup"><span data-stu-id="46e0f-130">Commit merge to a database even if there are errors.</span></span>                       |
| <span data-ttu-id="46e0f-131">-M</span><span class="sxs-lookup"><span data-stu-id="46e0f-131">-m</span></span>         | <span data-ttu-id="46e0f-132"><*模組*> 合併模組以合併到資料庫。</span><span class="sxs-lookup"><span data-stu-id="46e0f-132"><*module*> Merge Module to merge into database.</span></span>                      |
| <span data-ttu-id="46e0f-133">-f</span><span class="sxs-lookup"><span data-stu-id="46e0f-133">-f</span></span>         | <span data-ttu-id="46e0f-134">功能 \[ ： Feature2 \] 功能 (s) 連接到合併模組。</span><span class="sxs-lookup"><span data-stu-id="46e0f-134">Feature\[:Feature2\] Feature(s) to connect to Merge Module.</span></span>                |
| <span data-ttu-id="46e0f-135">-r</span><span class="sxs-lookup"><span data-stu-id="46e0f-135">-r</span></span>         | <span data-ttu-id="46e0f-136"><模組根重新導向的 *目錄識別碼*> 目錄專案。</span><span class="sxs-lookup"><span data-stu-id="46e0f-136"><*directory id*> Directory entry for the module root redirection.</span></span>    |
| <span data-ttu-id="46e0f-137">-X</span><span class="sxs-lookup"><span data-stu-id="46e0f-137">-x</span></span>         | <span data-ttu-id="46e0f-138"><*目錄*> 將檔案解壓縮至目錄下的映射。</span><span class="sxs-lookup"><span data-stu-id="46e0f-138"><*directory*> Extract files to an image under the directory.</span></span>         |
| <span data-ttu-id="46e0f-139">-g</span><span class="sxs-lookup"><span data-stu-id="46e0f-139">-g</span></span>         | <span data-ttu-id="46e0f-140"><用來開啟模組的 *語言*> 語言。</span><span class="sxs-lookup"><span data-stu-id="46e0f-140"><*language*> Language used to open a module.</span></span>                         |
| <span data-ttu-id="46e0f-141">-l</span><span class="sxs-lookup"><span data-stu-id="46e0f-141">-l</span></span>         | <span data-ttu-id="46e0f-142"><*記錄* 檔> 要作為記錄檔的檔案，如果已經存在，則附加。</span><span class="sxs-lookup"><span data-stu-id="46e0f-142"><*log file*> File to use as a log, append if it already exists.</span></span>      |
| <span data-ttu-id="46e0f-143">-i</span><span class="sxs-lookup"><span data-stu-id="46e0f-143">-i</span></span>         | <span data-ttu-id="46e0f-144"><*目錄*> 將檔案解壓縮至目錄下的來源映射。</span><span class="sxs-lookup"><span data-stu-id="46e0f-144"><*directory*> Extract files to the source image under the directory.</span></span> |
| <span data-ttu-id="46e0f-145">-cab</span><span class="sxs-lookup"><span data-stu-id="46e0f-145">-cab</span></span>       | <span data-ttu-id="46e0f-146"><*檔案名*> 將 .msm 封包解壓縮至檔案。</span><span class="sxs-lookup"><span data-stu-id="46e0f-146"><*filename*> Extract the MSM cabinet to file.</span></span>                        |
| <span data-ttu-id="46e0f-147">-lfn</span><span class="sxs-lookup"><span data-stu-id="46e0f-147">-lfn</span></span>       | <span data-ttu-id="46e0f-148">在解壓縮期間使用長檔名。</span><span class="sxs-lookup"><span data-stu-id="46e0f-148">Use Long File Names during the extraction.</span></span>                                 |
| <span data-ttu-id="46e0f-149">-設定</span><span class="sxs-lookup"><span data-stu-id="46e0f-149">-configure</span></span> | <span data-ttu-id="46e0f-150"><*檔案名*> 使用檔案中的資料來設定模組。</span><span class="sxs-lookup"><span data-stu-id="46e0f-150"><*filename*> Configure the module using data from a file.</span></span>            |



 

## <a name="related-topics"></a><span data-ttu-id="46e0f-151">相關主題</span><span class="sxs-lookup"><span data-stu-id="46e0f-151">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="46e0f-152">Windows Installer 開發工具</span><span class="sxs-lookup"><span data-stu-id="46e0f-152">Windows Installer Development Tools</span></span>](windows-installer-development-tools.md)
</dt> <dt>

[<span data-ttu-id="46e0f-153">已發行的版本、工具和可轉散發套件</span><span class="sxs-lookup"><span data-stu-id="46e0f-153">Released Versions, Tools, and Redistributables</span></span>](released-versions-tools-and-redistributables.md)
</dt> </dl>

 

 



