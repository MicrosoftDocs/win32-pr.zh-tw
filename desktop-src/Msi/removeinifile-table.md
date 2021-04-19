---
description: RemoveIniFile 資料表包含應用程式從 .ini 檔案刪除所需的資訊。
ms.assetid: 702cf86e-02f4-4ea7-8573-b500ac550aae
title: RemoveIniFile 資料表
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b57b4ba6f2c42ee636f1b9e21e798e27665f102a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106984248"
---
# <a name="removeinifile-table"></a><span data-ttu-id="23af1-103">RemoveIniFile 資料表</span><span class="sxs-lookup"><span data-stu-id="23af1-103">RemoveIniFile Table</span></span>

<span data-ttu-id="23af1-104">RemoveIniFile 資料表包含應用程式從 .ini 檔案刪除所需的資訊。</span><span class="sxs-lookup"><span data-stu-id="23af1-104">The RemoveIniFile table contains the information an application needs to delete from a .ini file.</span></span>

<span data-ttu-id="23af1-105">RemoveIniFile 資料表具有下列資料行。</span><span class="sxs-lookup"><span data-stu-id="23af1-105">The RemoveIniFile table has the following columns.</span></span>



| <span data-ttu-id="23af1-106">Column</span><span class="sxs-lookup"><span data-stu-id="23af1-106">Column</span></span>        | <span data-ttu-id="23af1-107">類型</span><span class="sxs-lookup"><span data-stu-id="23af1-107">Type</span></span>                         | <span data-ttu-id="23af1-108">答案</span><span class="sxs-lookup"><span data-stu-id="23af1-108">Key</span></span> | <span data-ttu-id="23af1-109">Nullable</span><span class="sxs-lookup"><span data-stu-id="23af1-109">Nullable</span></span> |
|---------------|------------------------------|-----|----------|
| <span data-ttu-id="23af1-110">RemoveIniFile</span><span class="sxs-lookup"><span data-stu-id="23af1-110">RemoveIniFile</span></span> | [<span data-ttu-id="23af1-111">識別碼</span><span class="sxs-lookup"><span data-stu-id="23af1-111">Identifier</span></span>](identifier.md) | <span data-ttu-id="23af1-112">Y</span><span class="sxs-lookup"><span data-stu-id="23af1-112">Y</span></span>   | <span data-ttu-id="23af1-113">N</span><span class="sxs-lookup"><span data-stu-id="23af1-113">N</span></span>        |
| <span data-ttu-id="23af1-114">FileName</span><span class="sxs-lookup"><span data-stu-id="23af1-114">FileName</span></span>      | [<span data-ttu-id="23af1-115">FileName</span><span class="sxs-lookup"><span data-stu-id="23af1-115">FileName</span></span>](text.md)         | <span data-ttu-id="23af1-116">N</span><span class="sxs-lookup"><span data-stu-id="23af1-116">N</span></span>   | <span data-ttu-id="23af1-117">N</span><span class="sxs-lookup"><span data-stu-id="23af1-117">N</span></span>        |
| <span data-ttu-id="23af1-118">DirProperty</span><span class="sxs-lookup"><span data-stu-id="23af1-118">DirProperty</span></span>   | [<span data-ttu-id="23af1-119">識別碼</span><span class="sxs-lookup"><span data-stu-id="23af1-119">Identifier</span></span>](identifier.md) | <span data-ttu-id="23af1-120">N</span><span class="sxs-lookup"><span data-stu-id="23af1-120">N</span></span>   | <span data-ttu-id="23af1-121">Y</span><span class="sxs-lookup"><span data-stu-id="23af1-121">Y</span></span>        |
| <span data-ttu-id="23af1-122">區段</span><span class="sxs-lookup"><span data-stu-id="23af1-122">Section</span></span>       | [<span data-ttu-id="23af1-123">格式 化</span><span class="sxs-lookup"><span data-stu-id="23af1-123">Formatted</span></span>](formatted.md)   | <span data-ttu-id="23af1-124">N</span><span class="sxs-lookup"><span data-stu-id="23af1-124">N</span></span>   | <span data-ttu-id="23af1-125">N</span><span class="sxs-lookup"><span data-stu-id="23af1-125">N</span></span>        |
| <span data-ttu-id="23af1-126">答案</span><span class="sxs-lookup"><span data-stu-id="23af1-126">Key</span></span>           | [<span data-ttu-id="23af1-127">格式 化</span><span class="sxs-lookup"><span data-stu-id="23af1-127">Formatted</span></span>](formatted.md)   | <span data-ttu-id="23af1-128">N</span><span class="sxs-lookup"><span data-stu-id="23af1-128">N</span></span>   | <span data-ttu-id="23af1-129">N</span><span class="sxs-lookup"><span data-stu-id="23af1-129">N</span></span>        |
| <span data-ttu-id="23af1-130">值</span><span class="sxs-lookup"><span data-stu-id="23af1-130">Value</span></span>         | [<span data-ttu-id="23af1-131">格式 化</span><span class="sxs-lookup"><span data-stu-id="23af1-131">Formatted</span></span>](formatted.md)   | <span data-ttu-id="23af1-132">N</span><span class="sxs-lookup"><span data-stu-id="23af1-132">N</span></span>   | <span data-ttu-id="23af1-133">Y</span><span class="sxs-lookup"><span data-stu-id="23af1-133">Y</span></span>        |
| <span data-ttu-id="23af1-134">動作</span><span class="sxs-lookup"><span data-stu-id="23af1-134">Action</span></span>        | [<span data-ttu-id="23af1-135">整數</span><span class="sxs-lookup"><span data-stu-id="23af1-135">Integer</span></span>](integer.md)       | <span data-ttu-id="23af1-136">N</span><span class="sxs-lookup"><span data-stu-id="23af1-136">N</span></span>   | <span data-ttu-id="23af1-137">N</span><span class="sxs-lookup"><span data-stu-id="23af1-137">N</span></span>        |
| <span data-ttu-id="23af1-138">元件\_</span><span class="sxs-lookup"><span data-stu-id="23af1-138">Component\_</span></span>   | [<span data-ttu-id="23af1-139">識別碼</span><span class="sxs-lookup"><span data-stu-id="23af1-139">Identifier</span></span>](identifier.md) | <span data-ttu-id="23af1-140">N</span><span class="sxs-lookup"><span data-stu-id="23af1-140">N</span></span>   | <span data-ttu-id="23af1-141">N</span><span class="sxs-lookup"><span data-stu-id="23af1-141">N</span></span>        |



 

## <a name="columns"></a><span data-ttu-id="23af1-142">資料行</span><span class="sxs-lookup"><span data-stu-id="23af1-142">Columns</span></span>

<dl> <dt>

<span data-ttu-id="23af1-143"><span id="RemoveIniFile"></span><span id="removeinifile"></span><span id="REMOVEINIFILE"></span>RemoveIniFile</span><span class="sxs-lookup"><span data-stu-id="23af1-143"><span id="RemoveIniFile"></span><span id="removeinifile"></span><span id="REMOVEINIFILE"></span>RemoveIniFile</span></span>
</dt> <dd>

<span data-ttu-id="23af1-144">此資料表的索引鍵。</span><span class="sxs-lookup"><span data-stu-id="23af1-144">The key for this table.</span></span>

</dd> <dt>

<span data-ttu-id="23af1-145"><span id="FileName"></span><span id="filename"></span><span id="FILENAME"></span>檔案名</span><span class="sxs-lookup"><span data-stu-id="23af1-145"><span id="FileName"></span><span id="filename"></span><span id="FILENAME"></span>FileName</span></span>
</dt> <dd>

<span data-ttu-id="23af1-146">要在其中刪除資訊的 .ini 檔案名。</span><span class="sxs-lookup"><span data-stu-id="23af1-146">The .ini file name in which to delete the information.</span></span>

</dd> <dt>

<span data-ttu-id="23af1-147"><span id="DirProperty"></span><span id="dirproperty"></span><span id="DIRPROPERTY"></span>DirProperty</span><span class="sxs-lookup"><span data-stu-id="23af1-147"><span id="DirProperty"></span><span id="dirproperty"></span><span id="DIRPROPERTY"></span>DirProperty</span></span>
</dt> <dd>

<span data-ttu-id="23af1-148">屬性的名稱，這個屬性的值會被假設解析為要移除之 .ini 檔案資料夾的完整路徑。</span><span class="sxs-lookup"><span data-stu-id="23af1-148">Name of a property whose value is assumed to resolve to the full path to the folder of the .ini file to be removed.</span></span> <span data-ttu-id="23af1-149">屬性可以是 [目錄資料表](directory-table.md)中目錄的名稱、 [AppSearch 資料表](appsearch-table.md)所設定的屬性，或是表示完整路徑的任何其他屬性。</span><span class="sxs-lookup"><span data-stu-id="23af1-149">The property can be the name of a directory in the [Directory table](directory-table.md), a property set by the [AppSearch table](appsearch-table.md), or any other property that represents a full path.</span></span>

</dd> <dt>

<span data-ttu-id="23af1-150"><span id="Section"></span><span id="section"></span><span id="SECTION"></span>部分</span><span class="sxs-lookup"><span data-stu-id="23af1-150"><span id="Section"></span><span id="section"></span><span id="SECTION"></span>Section</span></span>
</dt> <dd>

<span data-ttu-id="23af1-151">可當地語系化的 .ini 檔案區段。</span><span class="sxs-lookup"><span data-stu-id="23af1-151">The localizable .ini file section.</span></span>

</dd> <dt>

<span data-ttu-id="23af1-152"><span id="Key"></span><span id="key"></span><span id="KEY"></span>關鍵</span><span class="sxs-lookup"><span data-stu-id="23af1-152"><span id="Key"></span><span id="key"></span><span id="KEY"></span>Key</span></span>
</dt> <dd>

<span data-ttu-id="23af1-153">區段底下的可當地語系化 .ini 檔案索引鍵。</span><span class="sxs-lookup"><span data-stu-id="23af1-153">The localizable .ini file key below the section.</span></span>

</dd> <dt>

<span data-ttu-id="23af1-154"><span id="Value"></span><span id="value"></span><span id="VALUE"></span>價值</span><span class="sxs-lookup"><span data-stu-id="23af1-154"><span id="Value"></span><span id="value"></span><span id="VALUE"></span>Value</span></span>
</dt> <dd>

<span data-ttu-id="23af1-155">要刪除的可當地語系化值。</span><span class="sxs-lookup"><span data-stu-id="23af1-155">The localizable value to be deleted.</span></span> <span data-ttu-id="23af1-156">當 Action 為4時，此值為必要項。</span><span class="sxs-lookup"><span data-stu-id="23af1-156">The value is required when Action is 4.</span></span>

</dd> <dt>

<span data-ttu-id="23af1-157"><span id="Action"></span><span id="action"></span><span id="ACTION"></span>行動</span><span class="sxs-lookup"><span data-stu-id="23af1-157"><span id="Action"></span><span id="action"></span><span id="ACTION"></span>Action</span></span>
</dt> <dd>

<span data-ttu-id="23af1-158">要進行的修改類型。</span><span class="sxs-lookup"><span data-stu-id="23af1-158">The type of modification to be made.</span></span>



| <span data-ttu-id="23af1-159">常數</span><span class="sxs-lookup"><span data-stu-id="23af1-159">Constant</span></span>                         | <span data-ttu-id="23af1-160">十六進位</span><span class="sxs-lookup"><span data-stu-id="23af1-160">Hexadecimal</span></span> | <span data-ttu-id="23af1-161">Decimal</span><span class="sxs-lookup"><span data-stu-id="23af1-161">Decimal</span></span> | <span data-ttu-id="23af1-162">意義</span><span class="sxs-lookup"><span data-stu-id="23af1-162">Meaning</span></span>                          |
|----------------------------------|-------------|---------|----------------------------------|
| <span data-ttu-id="23af1-163">**msidbIniFileActionRemoveLine**</span><span class="sxs-lookup"><span data-stu-id="23af1-163">**msidbIniFileActionRemoveLine**</span></span> | <span data-ttu-id="23af1-164">0x002</span><span class="sxs-lookup"><span data-stu-id="23af1-164">0x002</span></span>       | <span data-ttu-id="23af1-165">2</span><span class="sxs-lookup"><span data-stu-id="23af1-165">2</span></span>       | <span data-ttu-id="23af1-166">刪除 .ini 專案。</span><span class="sxs-lookup"><span data-stu-id="23af1-166">Deletes .ini entry.</span></span>              |
| <span data-ttu-id="23af1-167">**msidbIniFileActionRemoveTag**</span><span class="sxs-lookup"><span data-stu-id="23af1-167">**msidbIniFileActionRemoveTag**</span></span>  | <span data-ttu-id="23af1-168">0x004</span><span class="sxs-lookup"><span data-stu-id="23af1-168">0x004</span></span>       | <span data-ttu-id="23af1-169">4</span><span class="sxs-lookup"><span data-stu-id="23af1-169">4</span></span>       | <span data-ttu-id="23af1-170">從 .ini 專案中刪除標記。</span><span class="sxs-lookup"><span data-stu-id="23af1-170">Deletes a tag from a .ini entry.</span></span> |



 

</dd> <dt>

<span data-ttu-id="23af1-171"><span id="Component_"></span><span id="component_"></span><span id="COMPONENT_"></span>元件\_</span><span class="sxs-lookup"><span data-stu-id="23af1-171"><span id="Component_"></span><span id="component_"></span><span id="COMPONENT_"></span>Component\_</span></span>
</dt> <dd>

<span data-ttu-id="23af1-172">[元件資料表](component-table.md)的第一個資料行中的外部索引鍵，該元件會參考用來控制刪除 .ini 值的元件。</span><span class="sxs-lookup"><span data-stu-id="23af1-172">External key into first column of the [Component table](component-table.md) referencing the component that controls the deletion of the .ini value.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="23af1-173">備註</span><span class="sxs-lookup"><span data-stu-id="23af1-173">Remarks</span></span>

<span data-ttu-id="23af1-174">當已選取要安裝的對應元件時，就會刪除 .ini 檔案資訊，不論是在本機或從來源執行。</span><span class="sxs-lookup"><span data-stu-id="23af1-174">The .ini file information is deleted when the corresponding Component has been selected to be installed, either locally or run from source.</span></span>

<span data-ttu-id="23af1-175">當 [RemoveIniValues 動作](removeinivalues-action.md) 執行時，就會參考此資料表。</span><span class="sxs-lookup"><span data-stu-id="23af1-175">This table is referred to when the [RemoveIniValues action](removeinivalues-action.md) is executed.</span></span>

<span data-ttu-id="23af1-176">如果目錄資料 \_ 行指定為 null，則 ini 檔案的位置是標準的 windows ini 位置，預設為 windows 目錄。</span><span class="sxs-lookup"><span data-stu-id="23af1-176">If the Directory\_ column is specified as null, the ini file location is the standard Windows ini location which is the Windows directory by default.</span></span>

<span data-ttu-id="23af1-177">從區段移除最後一個值會刪除該區段。</span><span class="sxs-lookup"><span data-stu-id="23af1-177">Removing the last value from a section deletes that section.</span></span> <span data-ttu-id="23af1-178">除了移除所有的值以外，沒有其他方法可刪除整個區段。</span><span class="sxs-lookup"><span data-stu-id="23af1-178">There is no other way to delete an entire section other than removing all its values.</span></span>

## <a name="validation"></a><span data-ttu-id="23af1-179">驗證</span><span class="sxs-lookup"><span data-stu-id="23af1-179">Validation</span></span>

<dl>

[<span data-ttu-id="23af1-180">ICE03</span><span class="sxs-lookup"><span data-stu-id="23af1-180">ICE03</span></span>](ice03.md)  
[<span data-ttu-id="23af1-181">ICE06</span><span class="sxs-lookup"><span data-stu-id="23af1-181">ICE06</span></span>](ice06.md)  
[<span data-ttu-id="23af1-182">ICE32</span><span class="sxs-lookup"><span data-stu-id="23af1-182">ICE32</span></span>](ice32.md)  
[<span data-ttu-id="23af1-183">ICE40</span><span class="sxs-lookup"><span data-stu-id="23af1-183">ICE40</span></span>](ice40.md)  
[<span data-ttu-id="23af1-184">ICE46</span><span class="sxs-lookup"><span data-stu-id="23af1-184">ICE46</span></span>](ice46.md)  
[<span data-ttu-id="23af1-185">ICE69</span><span class="sxs-lookup"><span data-stu-id="23af1-185">ICE69</span></span>](ice69.md)  
</dl>

 

 



