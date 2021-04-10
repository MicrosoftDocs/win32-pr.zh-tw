---
description: IniFile 資料表包含應用程式需要在 .ini 檔中設定的 .ini 資訊。
ms.assetid: fdb1a627-da6b-4da1-87a7-7f1c94d3836e
title: IniFile 資料表
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0d63ae37f7c8ed5c50b9b425b0462b445f7acb5b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104026632"
---
# <a name="inifile-table"></a><span data-ttu-id="78eef-103">IniFile 資料表</span><span class="sxs-lookup"><span data-stu-id="78eef-103">IniFile Table</span></span>

<span data-ttu-id="78eef-104">IniFile 資料表包含應用程式需要在 .ini 檔中設定的 .ini 資訊。</span><span class="sxs-lookup"><span data-stu-id="78eef-104">The IniFile table contains the .ini information that the application needs to set in an .ini file.</span></span>

<span data-ttu-id="78eef-105">IniFile 資料表具有下列資料行。</span><span class="sxs-lookup"><span data-stu-id="78eef-105">The IniFile table has the following columns.</span></span>



| <span data-ttu-id="78eef-106">Column</span><span class="sxs-lookup"><span data-stu-id="78eef-106">Column</span></span>      | <span data-ttu-id="78eef-107">類型</span><span class="sxs-lookup"><span data-stu-id="78eef-107">Type</span></span>                         | <span data-ttu-id="78eef-108">答案</span><span class="sxs-lookup"><span data-stu-id="78eef-108">Key</span></span> | <span data-ttu-id="78eef-109">Nullable</span><span class="sxs-lookup"><span data-stu-id="78eef-109">Nullable</span></span> |
|-------------|------------------------------|-----|----------|
| <span data-ttu-id="78eef-110">IniFile</span><span class="sxs-lookup"><span data-stu-id="78eef-110">IniFile</span></span>     | [<span data-ttu-id="78eef-111">識別碼</span><span class="sxs-lookup"><span data-stu-id="78eef-111">Identifier</span></span>](identifier.md) | <span data-ttu-id="78eef-112">Y</span><span class="sxs-lookup"><span data-stu-id="78eef-112">Y</span></span>   | <span data-ttu-id="78eef-113">N</span><span class="sxs-lookup"><span data-stu-id="78eef-113">N</span></span>        |
| <span data-ttu-id="78eef-114">FileName</span><span class="sxs-lookup"><span data-stu-id="78eef-114">FileName</span></span>    | [<span data-ttu-id="78eef-115">FileName</span><span class="sxs-lookup"><span data-stu-id="78eef-115">FileName</span></span>](text.md)         | <span data-ttu-id="78eef-116">N</span><span class="sxs-lookup"><span data-stu-id="78eef-116">N</span></span>   | <span data-ttu-id="78eef-117">N</span><span class="sxs-lookup"><span data-stu-id="78eef-117">N</span></span>        |
| <span data-ttu-id="78eef-118">DirProperty</span><span class="sxs-lookup"><span data-stu-id="78eef-118">DirProperty</span></span> | [<span data-ttu-id="78eef-119">識別碼</span><span class="sxs-lookup"><span data-stu-id="78eef-119">Identifier</span></span>](identifier.md) | <span data-ttu-id="78eef-120">N</span><span class="sxs-lookup"><span data-stu-id="78eef-120">N</span></span>   | <span data-ttu-id="78eef-121">Y</span><span class="sxs-lookup"><span data-stu-id="78eef-121">Y</span></span>        |
| <span data-ttu-id="78eef-122">區段</span><span class="sxs-lookup"><span data-stu-id="78eef-122">Section</span></span>     | [<span data-ttu-id="78eef-123">格式 化</span><span class="sxs-lookup"><span data-stu-id="78eef-123">Formatted</span></span>](formatted.md)   | <span data-ttu-id="78eef-124">N</span><span class="sxs-lookup"><span data-stu-id="78eef-124">N</span></span>   | <span data-ttu-id="78eef-125">N</span><span class="sxs-lookup"><span data-stu-id="78eef-125">N</span></span>        |
| <span data-ttu-id="78eef-126">答案</span><span class="sxs-lookup"><span data-stu-id="78eef-126">Key</span></span>         | [<span data-ttu-id="78eef-127">格式 化</span><span class="sxs-lookup"><span data-stu-id="78eef-127">Formatted</span></span>](formatted.md)   | <span data-ttu-id="78eef-128">N</span><span class="sxs-lookup"><span data-stu-id="78eef-128">N</span></span>   | <span data-ttu-id="78eef-129">N</span><span class="sxs-lookup"><span data-stu-id="78eef-129">N</span></span>        |
| <span data-ttu-id="78eef-130">值</span><span class="sxs-lookup"><span data-stu-id="78eef-130">Value</span></span>       | [<span data-ttu-id="78eef-131">格式 化</span><span class="sxs-lookup"><span data-stu-id="78eef-131">Formatted</span></span>](formatted.md)   | <span data-ttu-id="78eef-132">N</span><span class="sxs-lookup"><span data-stu-id="78eef-132">N</span></span>   | <span data-ttu-id="78eef-133">N</span><span class="sxs-lookup"><span data-stu-id="78eef-133">N</span></span>        |
| <span data-ttu-id="78eef-134">動作</span><span class="sxs-lookup"><span data-stu-id="78eef-134">Action</span></span>      | [<span data-ttu-id="78eef-135">整數</span><span class="sxs-lookup"><span data-stu-id="78eef-135">Integer</span></span>](integer.md)       | <span data-ttu-id="78eef-136">N</span><span class="sxs-lookup"><span data-stu-id="78eef-136">N</span></span>   | <span data-ttu-id="78eef-137">N</span><span class="sxs-lookup"><span data-stu-id="78eef-137">N</span></span>        |
| <span data-ttu-id="78eef-138">元件\_</span><span class="sxs-lookup"><span data-stu-id="78eef-138">Component\_</span></span> | [<span data-ttu-id="78eef-139">識別碼</span><span class="sxs-lookup"><span data-stu-id="78eef-139">Identifier</span></span>](identifier.md) | <span data-ttu-id="78eef-140">N</span><span class="sxs-lookup"><span data-stu-id="78eef-140">N</span></span>   | <span data-ttu-id="78eef-141">N</span><span class="sxs-lookup"><span data-stu-id="78eef-141">N</span></span>        |



 

## <a name="columns"></a><span data-ttu-id="78eef-142">資料行</span><span class="sxs-lookup"><span data-stu-id="78eef-142">Columns</span></span>

<dl> <dt>

<span data-ttu-id="78eef-143"><span id="IniFile"></span><span id="inifile"></span><span id="INIFILE"></span>IniFile</span><span class="sxs-lookup"><span data-stu-id="78eef-143"><span id="IniFile"></span><span id="inifile"></span><span id="INIFILE"></span>IniFile</span></span>
</dt> <dd>

<span data-ttu-id="78eef-144">此資料表的索引鍵。</span><span class="sxs-lookup"><span data-stu-id="78eef-144">The key for this table.</span></span>

</dd> <dt>

<span data-ttu-id="78eef-145"><span id="FileName"></span><span id="filename"></span><span id="FILENAME"></span>檔案名</span><span class="sxs-lookup"><span data-stu-id="78eef-145"><span id="FileName"></span><span id="filename"></span><span id="FILENAME"></span>FileName</span></span>
</dt> <dd>

<span data-ttu-id="78eef-146">要在其中寫入資訊之 .ini 檔案的可當地語系化名稱。</span><span class="sxs-lookup"><span data-stu-id="78eef-146">The localizable name of the .ini file in which to write the information.</span></span>

</dd> <dt>

<span data-ttu-id="78eef-147"><span id="DirProperty"></span><span id="dirproperty"></span><span id="DIRPROPERTY"></span>DirProperty</span><span class="sxs-lookup"><span data-stu-id="78eef-147"><span id="DirProperty"></span><span id="dirproperty"></span><span id="DIRPROPERTY"></span>DirProperty</span></span>
</dt> <dd>

<span data-ttu-id="78eef-148">具有值的屬性名稱，這個屬性的值會解析為包含 .ini 檔案之資料夾的完整路徑。</span><span class="sxs-lookup"><span data-stu-id="78eef-148">Name of a property having a value that resolves to the full path of the folder containing the .ini file.</span></span> <span data-ttu-id="78eef-149">屬性可以是 [目錄資料表](directory-table.md)中目錄的名稱、 [AppSearch 資料表](appsearch-table.md)所設定的屬性，或是表示完整路徑的任何其他屬性。</span><span class="sxs-lookup"><span data-stu-id="78eef-149">The property can be the name of a directory in the [Directory table](directory-table.md), a property set by the [AppSearch table](appsearch-table.md), or any other property that represents a full path.</span></span> <span data-ttu-id="78eef-150">如果此欄位保留空白，則會在具有 [**WindowsFolder**](windowsfolder.md) 屬性指定完整路徑的資料夾中建立 .ini 檔案。</span><span class="sxs-lookup"><span data-stu-id="78eef-150">If this field is left blank, the .ini file is created in the folder having the full path specified by the [**WindowsFolder**](windowsfolder.md) property.</span></span>

</dd> <dt>

<span data-ttu-id="78eef-151"><span id="Section"></span><span id="section"></span><span id="SECTION"></span>部分</span><span class="sxs-lookup"><span data-stu-id="78eef-151"><span id="Section"></span><span id="section"></span><span id="SECTION"></span>Section</span></span>
</dt> <dd>

<span data-ttu-id="78eef-152">可當地語系化的 .ini 檔案區段。</span><span class="sxs-lookup"><span data-stu-id="78eef-152">The localizable .ini file section.</span></span>

</dd> <dt>

<span data-ttu-id="78eef-153"><span id="Key"></span><span id="key"></span><span id="KEY"></span>關鍵</span><span class="sxs-lookup"><span data-stu-id="78eef-153"><span id="Key"></span><span id="key"></span><span id="KEY"></span>Key</span></span>
</dt> <dd>

<span data-ttu-id="78eef-154">區段內的可當地語系化 .ini 檔案索引鍵。</span><span class="sxs-lookup"><span data-stu-id="78eef-154">The localizable .ini file key within the section.</span></span>

</dd> <dt>

<span data-ttu-id="78eef-155"><span id="Value"></span><span id="value"></span><span id="VALUE"></span>價值</span><span class="sxs-lookup"><span data-stu-id="78eef-155"><span id="Value"></span><span id="value"></span><span id="VALUE"></span>Value</span></span>
</dt> <dd>

<span data-ttu-id="78eef-156">要寫入的可當地語系化值。</span><span class="sxs-lookup"><span data-stu-id="78eef-156">The localizable value to be written.</span></span>

</dd> <dt>

<span data-ttu-id="78eef-157"><span id="Action"></span><span id="action"></span><span id="ACTION"></span>行動</span><span class="sxs-lookup"><span data-stu-id="78eef-157"><span id="Action"></span><span id="action"></span><span id="ACTION"></span>Action</span></span>
</dt> <dd>

<span data-ttu-id="78eef-158">要進行的修改類型。</span><span class="sxs-lookup"><span data-stu-id="78eef-158">The type of modification to be made.</span></span>



| <span data-ttu-id="78eef-159">常數</span><span class="sxs-lookup"><span data-stu-id="78eef-159">Constant</span></span>                         | <span data-ttu-id="78eef-160">十六進位</span><span class="sxs-lookup"><span data-stu-id="78eef-160">Hexadecimal</span></span> | <span data-ttu-id="78eef-161">Decimal</span><span class="sxs-lookup"><span data-stu-id="78eef-161">Decimal</span></span> | <span data-ttu-id="78eef-162">修改</span><span class="sxs-lookup"><span data-stu-id="78eef-162">Modification</span></span>                                                                     |
|----------------------------------|-------------|---------|----------------------------------------------------------------------------------|
| <span data-ttu-id="78eef-163">**msidbIniFileActionAddLine**</span><span class="sxs-lookup"><span data-stu-id="78eef-163">**msidbIniFileActionAddLine**</span></span>    | <span data-ttu-id="78eef-164">0x000</span><span class="sxs-lookup"><span data-stu-id="78eef-164">0x000</span></span>       | <span data-ttu-id="78eef-165">0</span><span class="sxs-lookup"><span data-stu-id="78eef-165">0</span></span>       | <span data-ttu-id="78eef-166">建立或更新 .ini 專案。</span><span class="sxs-lookup"><span data-stu-id="78eef-166">Creates or updates a .ini entry.</span></span>                                                 |
| <span data-ttu-id="78eef-167">**msidbIniFileActionCreateLine**</span><span class="sxs-lookup"><span data-stu-id="78eef-167">**msidbIniFileActionCreateLine**</span></span> | <span data-ttu-id="78eef-168">0x001</span><span class="sxs-lookup"><span data-stu-id="78eef-168">0x001</span></span>       | <span data-ttu-id="78eef-169">1</span><span class="sxs-lookup"><span data-stu-id="78eef-169">1</span></span>       | <span data-ttu-id="78eef-170">只有在專案不存在時，才會建立 .ini 專案。</span><span class="sxs-lookup"><span data-stu-id="78eef-170">Creates a .ini entry only if the entry does not already exist.</span></span>                   |
| <span data-ttu-id="78eef-171">**msidbIniFileActionAddTag**</span><span class="sxs-lookup"><span data-stu-id="78eef-171">**msidbIniFileActionAddTag**</span></span>     | <span data-ttu-id="78eef-172">0x003</span><span class="sxs-lookup"><span data-stu-id="78eef-172">0x003</span></span>       | <span data-ttu-id="78eef-173">3</span><span class="sxs-lookup"><span data-stu-id="78eef-173">3</span></span>       | <span data-ttu-id="78eef-174">建立新的專案，或將新的逗號分隔值附加至現有的專案。</span><span class="sxs-lookup"><span data-stu-id="78eef-174">Creates a new entry or appends a new comma-separated value to an existing entry.</span></span> |



 

</dd> <dt>

<span data-ttu-id="78eef-175"><span id="Component_"></span><span id="component_"></span><span id="COMPONENT_"></span>元件\_</span><span class="sxs-lookup"><span data-stu-id="78eef-175"><span id="Component_"></span><span id="component_"></span><span id="COMPONENT_"></span>Component\_</span></span>
</dt> <dd>

<span data-ttu-id="78eef-176">在 [元件資料表](component-table.md) 的第一個資料行中，外部索引鍵會參考用來控制 .ini 值安裝的元件。</span><span class="sxs-lookup"><span data-stu-id="78eef-176">External key into the first column of the [Component table](component-table.md) referencing the component that controls the installation of the .ini value.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="78eef-177">備註</span><span class="sxs-lookup"><span data-stu-id="78eef-177">Remarks</span></span>

<span data-ttu-id="78eef-178">當對應的元件已選取要安裝為本機或從來源執行時，就會寫出 .ini 檔資訊。</span><span class="sxs-lookup"><span data-stu-id="78eef-178">The .ini file information is written out when the corresponding component has been selected to be installed as local or run from source.</span></span>

<span data-ttu-id="78eef-179">當執行 [WriteIniValues 動作](writeinivalues-action.md) 或 [RemoveIniValues 動作](removeinivalues-action.md) 時，就會參考此資料表。</span><span class="sxs-lookup"><span data-stu-id="78eef-179">This table is referred to when the [WriteIniValues action](writeinivalues-action.md) or the [RemoveIniValues action](removeinivalues-action.md) is executed.</span></span>

## <a name="validation"></a><span data-ttu-id="78eef-180">驗證</span><span class="sxs-lookup"><span data-stu-id="78eef-180">Validation</span></span>

<dl>

[<span data-ttu-id="78eef-181">ICE03</span><span class="sxs-lookup"><span data-stu-id="78eef-181">ICE03</span></span>](ice03.md)  
[<span data-ttu-id="78eef-182">ICE06</span><span class="sxs-lookup"><span data-stu-id="78eef-182">ICE06</span></span>](ice06.md)  
[<span data-ttu-id="78eef-183">ICE32</span><span class="sxs-lookup"><span data-stu-id="78eef-183">ICE32</span></span>](ice32.md)  
[<span data-ttu-id="78eef-184">ICE46</span><span class="sxs-lookup"><span data-stu-id="78eef-184">ICE46</span></span>](ice46.md)  
[<span data-ttu-id="78eef-185">ICE69</span><span class="sxs-lookup"><span data-stu-id="78eef-185">ICE69</span></span>](ice69.md)  
[<span data-ttu-id="78eef-186">ICE88</span><span class="sxs-lookup"><span data-stu-id="78eef-186">ICE88</span></span>](ice88.md)  
[<span data-ttu-id="78eef-187">ICE91</span><span class="sxs-lookup"><span data-stu-id="78eef-187">ICE91</span></span>](ice91.md)  
</dl>

 

 



