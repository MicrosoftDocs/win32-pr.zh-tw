---
description: IniLocator 資料表包含使用 .ini 檔搜尋檔案或目錄，或搜尋特定 .ini 專案本身所需的資訊。 .Ini 檔案必須存在於預設的 Microsoft Windows 目錄中。
ms.assetid: 5a3c6077-34ef-48c8-b4e6-ecb1deb40f96
title: IniLocator 資料表
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 89583a2d69fd88dd4b5624920e2374aa7e203103
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106989352"
---
# <a name="inilocator-table"></a><span data-ttu-id="69da2-104">IniLocator 資料表</span><span class="sxs-lookup"><span data-stu-id="69da2-104">IniLocator Table</span></span>

<span data-ttu-id="69da2-105">IniLocator 資料表包含使用 .ini 檔搜尋檔案或目錄，或搜尋特定 .ini 專案本身所需的資訊。</span><span class="sxs-lookup"><span data-stu-id="69da2-105">The IniLocator table holds the information needed to search for a file or directory using an .ini file or to search for a particular .ini entry itself.</span></span> <span data-ttu-id="69da2-106">.Ini 檔案必須存在於預設的 Microsoft Windows 目錄中。</span><span class="sxs-lookup"><span data-stu-id="69da2-106">The .ini file must be present in the default Microsoft Windows directory.</span></span>

<span data-ttu-id="69da2-107">IniLocator 資料表具有下列資料行。</span><span class="sxs-lookup"><span data-stu-id="69da2-107">The IniLocator table has the following columns.</span></span>



| <span data-ttu-id="69da2-108">Column</span><span class="sxs-lookup"><span data-stu-id="69da2-108">Column</span></span>      | <span data-ttu-id="69da2-109">類型</span><span class="sxs-lookup"><span data-stu-id="69da2-109">Type</span></span>                         | <span data-ttu-id="69da2-110">答案</span><span class="sxs-lookup"><span data-stu-id="69da2-110">Key</span></span> | <span data-ttu-id="69da2-111">Nullable</span><span class="sxs-lookup"><span data-stu-id="69da2-111">Nullable</span></span> |
|-------------|------------------------------|-----|----------|
| <span data-ttu-id="69da2-112">簽名\_</span><span class="sxs-lookup"><span data-stu-id="69da2-112">Signature\_</span></span> | [<span data-ttu-id="69da2-113">識別碼</span><span class="sxs-lookup"><span data-stu-id="69da2-113">Identifier</span></span>](identifier.md) | <span data-ttu-id="69da2-114">Y</span><span class="sxs-lookup"><span data-stu-id="69da2-114">Y</span></span>   | <span data-ttu-id="69da2-115">N</span><span class="sxs-lookup"><span data-stu-id="69da2-115">N</span></span>        |
| <span data-ttu-id="69da2-116">FileName</span><span class="sxs-lookup"><span data-stu-id="69da2-116">FileName</span></span>    | [<span data-ttu-id="69da2-117">FileName</span><span class="sxs-lookup"><span data-stu-id="69da2-117">FileName</span></span>](text.md)         | <span data-ttu-id="69da2-118">N</span><span class="sxs-lookup"><span data-stu-id="69da2-118">N</span></span>   | <span data-ttu-id="69da2-119">N</span><span class="sxs-lookup"><span data-stu-id="69da2-119">N</span></span>        |
| <span data-ttu-id="69da2-120">區段</span><span class="sxs-lookup"><span data-stu-id="69da2-120">Section</span></span>     | [<span data-ttu-id="69da2-121">Text</span><span class="sxs-lookup"><span data-stu-id="69da2-121">Text</span></span>](text.md)             | <span data-ttu-id="69da2-122">N</span><span class="sxs-lookup"><span data-stu-id="69da2-122">N</span></span>   | <span data-ttu-id="69da2-123">N</span><span class="sxs-lookup"><span data-stu-id="69da2-123">N</span></span>        |
| <span data-ttu-id="69da2-124">答案</span><span class="sxs-lookup"><span data-stu-id="69da2-124">Key</span></span>         | [<span data-ttu-id="69da2-125">Text</span><span class="sxs-lookup"><span data-stu-id="69da2-125">Text</span></span>](text.md)             | <span data-ttu-id="69da2-126">N</span><span class="sxs-lookup"><span data-stu-id="69da2-126">N</span></span>   | <span data-ttu-id="69da2-127">N</span><span class="sxs-lookup"><span data-stu-id="69da2-127">N</span></span>        |
| <span data-ttu-id="69da2-128">欄位</span><span class="sxs-lookup"><span data-stu-id="69da2-128">Field</span></span>       | [<span data-ttu-id="69da2-129">整數</span><span class="sxs-lookup"><span data-stu-id="69da2-129">Integer</span></span>](integer.md)       | <span data-ttu-id="69da2-130">N</span><span class="sxs-lookup"><span data-stu-id="69da2-130">N</span></span>   | <span data-ttu-id="69da2-131">Y</span><span class="sxs-lookup"><span data-stu-id="69da2-131">Y</span></span>        |
| <span data-ttu-id="69da2-132">類型</span><span class="sxs-lookup"><span data-stu-id="69da2-132">Type</span></span>        | [<span data-ttu-id="69da2-133">整數</span><span class="sxs-lookup"><span data-stu-id="69da2-133">Integer</span></span>](integer.md)       | <span data-ttu-id="69da2-134">N</span><span class="sxs-lookup"><span data-stu-id="69da2-134">N</span></span>   | <span data-ttu-id="69da2-135">Y</span><span class="sxs-lookup"><span data-stu-id="69da2-135">Y</span></span>        |



 

## <a name="columns"></a><span data-ttu-id="69da2-136">資料行</span><span class="sxs-lookup"><span data-stu-id="69da2-136">Columns</span></span>

<dl> <dt>

<span data-ttu-id="69da2-137"><span id="Signature_"></span><span id="signature_"></span><span id="SIGNATURE_"></span>簽名\_</span><span class="sxs-lookup"><span data-stu-id="69da2-137"><span id="Signature_"></span><span id="signature_"></span><span id="SIGNATURE_"></span>Signature\_</span></span>
</dt> <dd>

<span data-ttu-id="69da2-138">簽章 [資料表](signature-table.md)的第一個資料行中的外部索引鍵。</span><span class="sxs-lookup"><span data-stu-id="69da2-138">An external key into the first column of the [Signature table](signature-table.md).</span></span> <span data-ttu-id="69da2-139">簽章 \_ 代表唯一的簽章，而且也是在簽章資料表的第一個資料行中的外部索引鍵。</span><span class="sxs-lookup"><span data-stu-id="69da2-139">The Signature\_ represents a unique signature and is also the external key into column one of the Signature table.</span></span> <span data-ttu-id="69da2-140">如果簽章資料表中有這個簽章，則搜尋是用於檔案。</span><span class="sxs-lookup"><span data-stu-id="69da2-140">If this signature is present in the Signature table, then the search is for a file.</span></span> <span data-ttu-id="69da2-141">如果簽章資料表中沒有此索引鍵，且 [類型] 資料行的值是 **msidbLocatorTypeRawValue**，則搜尋是針對 IniLocator 資料表所指定的 .ini 專案。</span><span class="sxs-lookup"><span data-stu-id="69da2-141">If this key is absent from the Signature table, and the value of the Type column is **msidbLocatorTypeRawValue**, the search is for the .ini entry specified by the IniLocator table.</span></span> <span data-ttu-id="69da2-142">否則搜尋是針對 IniLocator 資料表所指定的目錄。</span><span class="sxs-lookup"><span data-stu-id="69da2-142">Otherwise the search is for a directory specified by the IniLocator table.</span></span>

</dd> <dt>

<span data-ttu-id="69da2-143"><span id="FileName"></span><span id="filename"></span><span id="FILENAME"></span>檔案名</span><span class="sxs-lookup"><span data-stu-id="69da2-143"><span id="FileName"></span><span id="filename"></span><span id="FILENAME"></span>FileName</span></span>
</dt> <dd>

<span data-ttu-id="69da2-144">.Ini 檔案名。</span><span class="sxs-lookup"><span data-stu-id="69da2-144">The .ini file name.</span></span>

</dd> <dt>

<span data-ttu-id="69da2-145"><span id="Section"></span><span id="section"></span><span id="SECTION"></span>部分</span><span class="sxs-lookup"><span data-stu-id="69da2-145"><span id="Section"></span><span id="section"></span><span id="SECTION"></span>Section</span></span>
</dt> <dd>

<span data-ttu-id="69da2-146">.Ini 檔案內的區段名稱。</span><span class="sxs-lookup"><span data-stu-id="69da2-146">Section name within the .ini file.</span></span>

</dd> <dt>

<span data-ttu-id="69da2-147"><span id="Key"></span><span id="key"></span><span id="KEY"></span>關鍵</span><span class="sxs-lookup"><span data-stu-id="69da2-147"><span id="Key"></span><span id="key"></span><span id="KEY"></span>Key</span></span>
</dt> <dd>

<span data-ttu-id="69da2-148">區段內的索引鍵值。</span><span class="sxs-lookup"><span data-stu-id="69da2-148">Key value within the section.</span></span>

</dd> <dt>

<span data-ttu-id="69da2-149"><span id="Field"></span><span id="field"></span><span id="FIELD"></span>領域</span><span class="sxs-lookup"><span data-stu-id="69da2-149"><span id="Field"></span><span id="field"></span><span id="FIELD"></span>Field</span></span>
</dt> <dd>

<span data-ttu-id="69da2-150">.Ini 行中的欄位。</span><span class="sxs-lookup"><span data-stu-id="69da2-150">The field in the .ini line.</span></span> <span data-ttu-id="69da2-151">如果欄位為 Null 或0，則會讀取整行。</span><span class="sxs-lookup"><span data-stu-id="69da2-151">If Field is Null or 0, then the entire line is read.</span></span> <span data-ttu-id="69da2-152">此值必須是非負數。</span><span class="sxs-lookup"><span data-stu-id="69da2-152">This must be a non-negative number.</span></span>

</dd> <dt>

<span data-ttu-id="69da2-153"><span id="Type"></span><span id="type"></span><span id="TYPE"></span>類型</span><span class="sxs-lookup"><span data-stu-id="69da2-153"><span id="Type"></span><span id="type"></span><span id="TYPE"></span>Type</span></span>
</dt> <dd>

<span data-ttu-id="69da2-154">值，決定 .ini 值是否為檔案位置、目錄位置或原始 .ini 值。</span><span class="sxs-lookup"><span data-stu-id="69da2-154">A value that determines whether the .ini value is a file location, a directory location, or raw .ini value.</span></span>

<span data-ttu-id="69da2-155">下表列出有效的值。</span><span class="sxs-lookup"><span data-stu-id="69da2-155">The following table lists valid values.</span></span> <span data-ttu-id="69da2-156">如果不存在，則類型會設定為1。</span><span class="sxs-lookup"><span data-stu-id="69da2-156">If absent, Type is set to be 1.</span></span>



| <span data-ttu-id="69da2-157">常數</span><span class="sxs-lookup"><span data-stu-id="69da2-157">Constant</span></span>                      | <span data-ttu-id="69da2-158">十六進位</span><span class="sxs-lookup"><span data-stu-id="69da2-158">Hexadecimal</span></span> | <span data-ttu-id="69da2-159">Decimal</span><span class="sxs-lookup"><span data-stu-id="69da2-159">Decimal</span></span> | <span data-ttu-id="69da2-160">Description</span><span class="sxs-lookup"><span data-stu-id="69da2-160">Description</span></span>           |
|-------------------------------|-------------|---------|-----------------------|
| <span data-ttu-id="69da2-161">**msidbLocatorTypeDirectory**</span><span class="sxs-lookup"><span data-stu-id="69da2-161">**msidbLocatorTypeDirectory**</span></span> | <span data-ttu-id="69da2-162">0x000</span><span class="sxs-lookup"><span data-stu-id="69da2-162">0x000</span></span>       | <span data-ttu-id="69da2-163">0</span><span class="sxs-lookup"><span data-stu-id="69da2-163">0</span></span>       | <span data-ttu-id="69da2-164">目錄位置。</span><span class="sxs-lookup"><span data-stu-id="69da2-164">A directory location.</span></span> |
| <span data-ttu-id="69da2-165">**msidbLocatorTypeFileName**</span><span class="sxs-lookup"><span data-stu-id="69da2-165">**msidbLocatorTypeFileName**</span></span>  | <span data-ttu-id="69da2-166">0x001</span><span class="sxs-lookup"><span data-stu-id="69da2-166">0x001</span></span>       | <span data-ttu-id="69da2-167">1</span><span class="sxs-lookup"><span data-stu-id="69da2-167">1</span></span>       | <span data-ttu-id="69da2-168">檔案位置。</span><span class="sxs-lookup"><span data-stu-id="69da2-168">A file location.</span></span>      |
| <span data-ttu-id="69da2-169">**msidbLocatorTypeRawValue**</span><span class="sxs-lookup"><span data-stu-id="69da2-169">**msidbLocatorTypeRawValue**</span></span>  | <span data-ttu-id="69da2-170">0x002</span><span class="sxs-lookup"><span data-stu-id="69da2-170">0x002</span></span>       | <span data-ttu-id="69da2-171">2</span><span class="sxs-lookup"><span data-stu-id="69da2-171">2</span></span>       | <span data-ttu-id="69da2-172">原始 .ini 值。</span><span class="sxs-lookup"><span data-stu-id="69da2-172">A raw .ini value.</span></span>     |



 

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="69da2-173">備註</span><span class="sxs-lookup"><span data-stu-id="69da2-173">Remarks</span></span>

<span data-ttu-id="69da2-174">此資料表與 [AppSearch 資料表](appsearch-table.md)搭配使用。</span><span class="sxs-lookup"><span data-stu-id="69da2-174">This table is used with the [AppSearch Table](appsearch-table.md).</span></span>

<span data-ttu-id="69da2-175">此資料表的資料行通常不會當地語系化。</span><span class="sxs-lookup"><span data-stu-id="69da2-175">This table's columns are generally not localized.</span></span> <span data-ttu-id="69da2-176">如果作者決定搜尋多種語言的產品，則每種語言的表格中都可以有個別的專案。</span><span class="sxs-lookup"><span data-stu-id="69da2-176">If an author decides to search for products in multiple languages, then there can be a separate entry included in the table for each language.</span></span>

<span data-ttu-id="69da2-177">進度顯示或記錄的相關當地語系化文字會在 [ActionText 資料表](actiontext-table.md)中指定。</span><span class="sxs-lookup"><span data-stu-id="69da2-177">Associated localized text for progress display or logging is specified in the [ActionText table](actiontext-table.md).</span></span>

<span data-ttu-id="69da2-178">請參閱 [搜尋現有的應用程式、檔案、登錄專案或 .ini 檔專案](searching-for-existing-applications-files-registry-entries-or--ini-file-entries.md)。</span><span class="sxs-lookup"><span data-stu-id="69da2-178">See [Searching for Existing Applications, Files, Registry Entries or .ini File Entries](searching-for-existing-applications-files-registry-entries-or--ini-file-entries.md).</span></span>

## <a name="validation"></a><span data-ttu-id="69da2-179">驗證</span><span class="sxs-lookup"><span data-stu-id="69da2-179">Validation</span></span>

<dl>

[<span data-ttu-id="69da2-180">ICE03</span><span class="sxs-lookup"><span data-stu-id="69da2-180">ICE03</span></span>](ice03.md)  
[<span data-ttu-id="69da2-181">ICE06</span><span class="sxs-lookup"><span data-stu-id="69da2-181">ICE06</span></span>](ice06.md)  
</dl>

 

 



