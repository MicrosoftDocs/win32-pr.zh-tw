---
description: 安裝資料庫的快捷方式資料表和相關資料表會保存安裝快捷方式所需的資訊。 請參閱「程式資訊資料表」群組和編輯安裝程式快捷方式。
ms.assetid: 0f3adf78-e650-414f-b85d-b53b986eafda
title: 指定快速鍵
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 29edf10a51827880a67826320d7f8415e70ea52a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106974405"
---
# <a name="specifying-shortcuts"></a><span data-ttu-id="44e61-104">指定快速鍵</span><span class="sxs-lookup"><span data-stu-id="44e61-104">Specifying Shortcuts</span></span>

<span data-ttu-id="44e61-105">安裝資料庫的 [快捷方式資料表](shortcut-table.md) 和相關資料表會保存安裝快捷方式所需的資訊。</span><span class="sxs-lookup"><span data-stu-id="44e61-105">The [Shortcut table](shortcut-table.md) and related tables of the installation database hold information needed to install shortcuts.</span></span> <span data-ttu-id="44e61-106">請參閱「 [程式資訊資料表」群組](program-information-tables-group.md) 和 [編輯安裝程式快捷方式](editing-installer-shortcuts.md)。</span><span class="sxs-lookup"><span data-stu-id="44e61-106">See the [Program Information Tables Group](program-information-tables-group.md) and [Editing Installer Shortcuts](editing-installer-shortcuts.md).</span></span>

<span data-ttu-id="44e61-107">在本節中，您會新增資訊，以指定「記事本」範例的公告和非公告快捷方式。</span><span class="sxs-lookup"><span data-stu-id="44e61-107">In this section you add information that specifies advertised and non-advertised shortcuts for the Notepad sample.</span></span>

<span data-ttu-id="44e61-108">使用您的資料庫編輯器開啟 MNP2000.msi，並在快捷方式資料表中輸入下列資料。</span><span class="sxs-lookup"><span data-stu-id="44e61-108">Use your database editor to open MNP2000.msi and enter the following data into the Shortcut table.</span></span>

[<span data-ttu-id="44e61-109">快速鍵資料表</span><span class="sxs-lookup"><span data-stu-id="44e61-109">Shortcut Table</span></span>](shortcut-table.md)



| <span data-ttu-id="44e61-110">快速鍵</span><span class="sxs-lookup"><span data-stu-id="44e61-110">Shortcut</span></span>  | <span data-ttu-id="44e61-111">目錄\_</span><span class="sxs-lookup"><span data-stu-id="44e61-111">Directory\_</span></span> | <span data-ttu-id="44e61-112">Name</span><span class="sxs-lookup"><span data-stu-id="44e61-112">Name</span></span>         | <span data-ttu-id="44e61-113">元件\_</span><span class="sxs-lookup"><span data-stu-id="44e61-113">Component\_</span></span> | <span data-ttu-id="44e61-114">目標</span><span class="sxs-lookup"><span data-stu-id="44e61-114">Target</span></span>             | <span data-ttu-id="44e61-115">引數</span><span class="sxs-lookup"><span data-stu-id="44e61-115">Arguments</span></span> | <span data-ttu-id="44e61-116">描述</span><span class="sxs-lookup"><span data-stu-id="44e61-116">Description</span></span> | <span data-ttu-id="44e61-117">熱鍵</span><span class="sxs-lookup"><span data-stu-id="44e61-117">Hotkey</span></span> | <span data-ttu-id="44e61-118">圖示\_</span><span class="sxs-lookup"><span data-stu-id="44e61-118">Icon\_</span></span>         | <span data-ttu-id="44e61-119">>iconindex</span><span class="sxs-lookup"><span data-stu-id="44e61-119">IconIndex</span></span> | <span data-ttu-id="44e61-120">ShowCmd</span><span class="sxs-lookup"><span data-stu-id="44e61-120">ShowCmd</span></span> | <span data-ttu-id="44e61-121">WkDir</span><span class="sxs-lookup"><span data-stu-id="44e61-121">WkDir</span></span> |
|-----------|-------------|--------------|-------------|--------------------|-----------|-------------|--------|----------------|-----------|---------|-------|
| <span data-ttu-id="44e61-122">sBaseball</span><span class="sxs-lookup"><span data-stu-id="44e61-122">sBaseball</span></span> | <span data-ttu-id="44e61-123">MENUDIR</span><span class="sxs-lookup"><span data-stu-id="44e61-123">MENUDIR</span></span>     | <span data-ttu-id="44e61-124">Baseball.txt</span><span class="sxs-lookup"><span data-stu-id="44e61-124">Baseball.txt</span></span> | <span data-ttu-id="44e61-125">棒球</span><span class="sxs-lookup"><span data-stu-id="44e61-125">Baseball</span></span>    | <span data-ttu-id="44e61-126">棒球</span><span class="sxs-lookup"><span data-stu-id="44e61-126">Baseball</span></span>           |           |             |        | <span data-ttu-id="44e61-127">orca \_icon.exe</span><span class="sxs-lookup"><span data-stu-id="44e61-127">orca\_icon.exe</span></span> |           |         |       |
| <span data-ttu-id="44e61-128">sConcert</span><span class="sxs-lookup"><span data-stu-id="44e61-128">sConcert</span></span>  | <span data-ttu-id="44e61-129">MENUDIR</span><span class="sxs-lookup"><span data-stu-id="44e61-129">MENUDIR</span></span>     | <span data-ttu-id="44e61-130">Concert.txt</span><span class="sxs-lookup"><span data-stu-id="44e61-130">Concert.txt</span></span>  | <span data-ttu-id="44e61-131">演唱會</span><span class="sxs-lookup"><span data-stu-id="44e61-131">Concert</span></span>     | <span data-ttu-id="44e61-132">\[\#Concert.txt\]</span><span class="sxs-lookup"><span data-stu-id="44e61-132">\[\#Concert.txt\]</span></span>  |           |             |        |                |           |         |       |
| <span data-ttu-id="44e61-133">sDance</span><span class="sxs-lookup"><span data-stu-id="44e61-133">sDance</span></span>    | <span data-ttu-id="44e61-134">MENUDIR</span><span class="sxs-lookup"><span data-stu-id="44e61-134">MENUDIR</span></span>     | <span data-ttu-id="44e61-135">Dance.txt</span><span class="sxs-lookup"><span data-stu-id="44e61-135">Dance.txt</span></span>    | <span data-ttu-id="44e61-136">舞蹈</span><span class="sxs-lookup"><span data-stu-id="44e61-136">Dance</span></span>       | <span data-ttu-id="44e61-137">\[\#Dance.txt\]</span><span class="sxs-lookup"><span data-stu-id="44e61-137">\[\#Dance.txt\]</span></span>    |           |             |        |                |           |         |       |
| <span data-ttu-id="44e61-138">sFootball</span><span class="sxs-lookup"><span data-stu-id="44e61-138">sFootball</span></span> | <span data-ttu-id="44e61-139">MENUDIR</span><span class="sxs-lookup"><span data-stu-id="44e61-139">MENUDIR</span></span>     | <span data-ttu-id="44e61-140">Football.txt</span><span class="sxs-lookup"><span data-stu-id="44e61-140">Football.txt</span></span> | <span data-ttu-id="44e61-141">足球</span><span class="sxs-lookup"><span data-stu-id="44e61-141">Football</span></span>    | <span data-ttu-id="44e61-142">\[\#Football.txt\]</span><span class="sxs-lookup"><span data-stu-id="44e61-142">\[\#Football.txt\]</span></span> |           |             |        |                |           |         |       |
| <span data-ttu-id="44e61-143">現成</span><span class="sxs-lookup"><span data-stu-id="44e61-143">sHelp</span></span>     | <span data-ttu-id="44e61-144">MENUDIR</span><span class="sxs-lookup"><span data-stu-id="44e61-144">MENUDIR</span></span>     | <span data-ttu-id="44e61-145">Help.txt</span><span class="sxs-lookup"><span data-stu-id="44e61-145">Help.txt</span></span>     | <span data-ttu-id="44e61-146">Help</span><span class="sxs-lookup"><span data-stu-id="44e61-146">Help</span></span>        | <span data-ttu-id="44e61-147">\[\#Help.txt\]</span><span class="sxs-lookup"><span data-stu-id="44e61-147">\[\#Help.txt\]</span></span>     |           |             |        |                |           |         |       |
| <span data-ttu-id="44e61-148">sJanuary</span><span class="sxs-lookup"><span data-stu-id="44e61-148">sJanuary</span></span>  | <span data-ttu-id="44e61-149">MENUDIR</span><span class="sxs-lookup"><span data-stu-id="44e61-149">MENUDIR</span></span>     | <span data-ttu-id="44e61-150">January.txt</span><span class="sxs-lookup"><span data-stu-id="44e61-150">January.txt</span></span>  | <span data-ttu-id="44e61-151">一月</span><span class="sxs-lookup"><span data-stu-id="44e61-151">January</span></span>     | <span data-ttu-id="44e61-152">\[\#January.txt\]</span><span class="sxs-lookup"><span data-stu-id="44e61-152">\[\#January.txt\]</span></span>  |           |             |        |                |           |         |       |
| <span data-ttu-id="44e61-153">sNewYears</span><span class="sxs-lookup"><span data-stu-id="44e61-153">sNewYears</span></span> | <span data-ttu-id="44e61-154">MENUDIR</span><span class="sxs-lookup"><span data-stu-id="44e61-154">MENUDIR</span></span>     | <span data-ttu-id="44e61-155">NewYears.txt</span><span class="sxs-lookup"><span data-stu-id="44e61-155">NewYears.txt</span></span> | <span data-ttu-id="44e61-156">NewYears</span><span class="sxs-lookup"><span data-stu-id="44e61-156">NewYears</span></span>    | <span data-ttu-id="44e61-157">\[\#NewYears.txt\]</span><span class="sxs-lookup"><span data-stu-id="44e61-157">\[\#NewYears.txt\]</span></span> |           |             |        |                |           |         |       |
| <span data-ttu-id="44e61-158">sNotepad</span><span class="sxs-lookup"><span data-stu-id="44e61-158">sNotepad</span></span>  | <span data-ttu-id="44e61-159">MENUDIR</span><span class="sxs-lookup"><span data-stu-id="44e61-159">MENUDIR</span></span>     | <span data-ttu-id="44e61-160">Redpark.exe</span><span class="sxs-lookup"><span data-stu-id="44e61-160">Redpark.exe</span></span>  | <span data-ttu-id="44e61-161">[記事本]</span><span class="sxs-lookup"><span data-stu-id="44e61-161">Notepad</span></span>     | <span data-ttu-id="44e61-162">\[\#Redpark.exe\]</span><span class="sxs-lookup"><span data-stu-id="44e61-162">\[\#Redpark.exe\]</span></span>  |           |             |        |                |           |         |       |
| <span data-ttu-id="44e61-163">sReadme</span><span class="sxs-lookup"><span data-stu-id="44e61-163">sReadme</span></span>   | <span data-ttu-id="44e61-164">MENUDIR</span><span class="sxs-lookup"><span data-stu-id="44e61-164">MENUDIR</span></span>     | <span data-ttu-id="44e61-165">Readme.txt</span><span class="sxs-lookup"><span data-stu-id="44e61-165">Readme.txt</span></span>   | <span data-ttu-id="44e61-166">[記事本]</span><span class="sxs-lookup"><span data-stu-id="44e61-166">Notepad</span></span>     | <span data-ttu-id="44e61-167">\[\#Readme.txt\]</span><span class="sxs-lookup"><span data-stu-id="44e61-167">\[\#Readme.txt\]</span></span>   |           |             |        |                |           |         |       |



 

<span data-ttu-id="44e61-168">範例安裝需要啟用針對棒球功能所公告的快捷方式安裝。</span><span class="sxs-lookup"><span data-stu-id="44e61-168">The sample installation needs to enable installation of an advertised shortcut for the Baseball feature.</span></span> <span data-ttu-id="44e61-169">這需要在快捷方式資料表的圖示資料行中，指定圖示資料表的索引鍵 \_ 。</span><span class="sxs-lookup"><span data-stu-id="44e61-169">This requires specifying a key to the Icon table in the Icon\_ column of the Shortcut table.</span></span> <span data-ttu-id="44e61-170">基於此範例的目的，您可以複製 Windows Installer SDK 所提供的 Orca 資料庫編輯器圖示。</span><span class="sxs-lookup"><span data-stu-id="44e61-170">For the purposes of this example you may copy the icon for the Orca database editor provided with the Windows Installer SDK.</span></span> <span data-ttu-id="44e61-171">從 Orca.msi 匯出 [圖示資料表](icon-table.md) ，然後使用 Orca 或其他合併工具，將此資料表合併到 MNP2000.msi 資料庫中。</span><span class="sxs-lookup"><span data-stu-id="44e61-171">Export the [Icon table](icon-table.md) from Orca.msi and then merge this table into the MNP2000.msi database using Orca or another merge tool.</span></span> <span data-ttu-id="44e61-172">Orca 也會在包含 MNP2000.msi 的目錄中建立名為 Icon 的目錄，並將圖示二進位資料檔案 orca \_icon.exe ibd。</span><span class="sxs-lookup"><span data-stu-id="44e61-172">Orca also creates a directory named Icon in the directory containing MNP2000.msi, and adds the icon binary data file orca\_icon.exe.ibd.</span></span> <span data-ttu-id="44e61-173">請參閱圖示表格中的資料行。</span><span class="sxs-lookup"><span data-stu-id="44e61-173">See the Data column in Icon table.</span></span> <span data-ttu-id="44e61-174">在 Orca 中觀看時，已完成的圖示資料表看起來應該如下所示。</span><span class="sxs-lookup"><span data-stu-id="44e61-174">The completed Icon table should look as follows when viewed in Orca.</span></span>

[<span data-ttu-id="44e61-175">圖示表</span><span class="sxs-lookup"><span data-stu-id="44e61-175">Icon Table</span></span>](icon-table.md)



| <span data-ttu-id="44e61-176">Name</span><span class="sxs-lookup"><span data-stu-id="44e61-176">Name</span></span>           | <span data-ttu-id="44e61-177">資料</span><span class="sxs-lookup"><span data-stu-id="44e61-177">Data</span></span>            |
|----------------|-----------------|
| <span data-ttu-id="44e61-178">orca \_icon.exe</span><span class="sxs-lookup"><span data-stu-id="44e61-178">orca\_icon.exe</span></span> | <span data-ttu-id="44e61-179">\[Binary Data\]</span><span class="sxs-lookup"><span data-stu-id="44e61-179">\[Binary Data\]</span></span> |



 

[<span data-ttu-id="44e61-180">繼續</span><span class="sxs-lookup"><span data-stu-id="44e61-180">Continue</span></span>](specifying-properties.md)

## <a name="related-topics"></a><span data-ttu-id="44e61-181">相關主題</span><span class="sxs-lookup"><span data-stu-id="44e61-181">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="44e61-182">編輯安裝程式快捷方式</span><span class="sxs-lookup"><span data-stu-id="44e61-182">Editing Installer Shortcuts</span></span>](editing-installer-shortcuts.md)
</dt> </dl>

 

 



