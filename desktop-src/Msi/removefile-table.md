---
description: RemoveFile 資料表包含 RemoveFiles 動作要移除的檔案清單。 將此資料表的 FileName 資料行設定為 Null，可支援移除空的資料夾。
ms.assetid: 8b3cb0e3-ccc0-4030-8f57-aa124c3b5588
title: RemoveFile 資料表
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 723e42582821d79842686678c5b310e95cd1e944
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103850599"
---
# <a name="removefile-table"></a><span data-ttu-id="4bdfd-104">RemoveFile 資料表</span><span class="sxs-lookup"><span data-stu-id="4bdfd-104">RemoveFile Table</span></span>

<span data-ttu-id="4bdfd-105">RemoveFile 資料表包含 [RemoveFiles 動作](removefiles-action.md)要移除的檔案清單。</span><span class="sxs-lookup"><span data-stu-id="4bdfd-105">The RemoveFile table contains a list of files to be removed by the [RemoveFiles action](removefiles-action.md).</span></span> <span data-ttu-id="4bdfd-106">將此資料表的 FileName 資料行設定為 Null，可支援移除空的資料夾。</span><span class="sxs-lookup"><span data-stu-id="4bdfd-106">Setting the FileName column of this table to Null supports the removal of empty folders.</span></span>

<span data-ttu-id="4bdfd-107">RemoveFile 資料表具有下列資料行。</span><span class="sxs-lookup"><span data-stu-id="4bdfd-107">The RemoveFile table has the following columns.</span></span>



| <span data-ttu-id="4bdfd-108">Column</span><span class="sxs-lookup"><span data-stu-id="4bdfd-108">Column</span></span>      | <span data-ttu-id="4bdfd-109">類型</span><span class="sxs-lookup"><span data-stu-id="4bdfd-109">Type</span></span>                                     | <span data-ttu-id="4bdfd-110">答案</span><span class="sxs-lookup"><span data-stu-id="4bdfd-110">Key</span></span> | <span data-ttu-id="4bdfd-111">Nullable</span><span class="sxs-lookup"><span data-stu-id="4bdfd-111">Nullable</span></span> |
|-------------|------------------------------------------|-----|----------|
| <span data-ttu-id="4bdfd-112">FileKey</span><span class="sxs-lookup"><span data-stu-id="4bdfd-112">FileKey</span></span>     | [<span data-ttu-id="4bdfd-113">識別碼</span><span class="sxs-lookup"><span data-stu-id="4bdfd-113">Identifier</span></span>](identifier.md)             | <span data-ttu-id="4bdfd-114">Y</span><span class="sxs-lookup"><span data-stu-id="4bdfd-114">Y</span></span>   | <span data-ttu-id="4bdfd-115">N</span><span class="sxs-lookup"><span data-stu-id="4bdfd-115">N</span></span>        |
| <span data-ttu-id="4bdfd-116">元件\_</span><span class="sxs-lookup"><span data-stu-id="4bdfd-116">Component\_</span></span> | [<span data-ttu-id="4bdfd-117">識別碼</span><span class="sxs-lookup"><span data-stu-id="4bdfd-117">Identifier</span></span>](identifier.md)             | <span data-ttu-id="4bdfd-118">N</span><span class="sxs-lookup"><span data-stu-id="4bdfd-118">N</span></span>   | <span data-ttu-id="4bdfd-119">N</span><span class="sxs-lookup"><span data-stu-id="4bdfd-119">N</span></span>        |
| <span data-ttu-id="4bdfd-120">FileName</span><span class="sxs-lookup"><span data-stu-id="4bdfd-120">FileName</span></span>    | [<span data-ttu-id="4bdfd-121">WildCardFilename</span><span class="sxs-lookup"><span data-stu-id="4bdfd-121">WildCardFilename</span></span>](wildcardfilename.md) | <span data-ttu-id="4bdfd-122">N</span><span class="sxs-lookup"><span data-stu-id="4bdfd-122">N</span></span>   | <span data-ttu-id="4bdfd-123">Y</span><span class="sxs-lookup"><span data-stu-id="4bdfd-123">Y</span></span>        |
| <span data-ttu-id="4bdfd-124">DirProperty</span><span class="sxs-lookup"><span data-stu-id="4bdfd-124">DirProperty</span></span> | [<span data-ttu-id="4bdfd-125">識別碼</span><span class="sxs-lookup"><span data-stu-id="4bdfd-125">Identifier</span></span>](identifier.md)             | <span data-ttu-id="4bdfd-126">N</span><span class="sxs-lookup"><span data-stu-id="4bdfd-126">N</span></span>   | <span data-ttu-id="4bdfd-127">N</span><span class="sxs-lookup"><span data-stu-id="4bdfd-127">N</span></span>        |
| <span data-ttu-id="4bdfd-128">InstallMode</span><span class="sxs-lookup"><span data-stu-id="4bdfd-128">InstallMode</span></span> | [<span data-ttu-id="4bdfd-129">整數</span><span class="sxs-lookup"><span data-stu-id="4bdfd-129">Integer</span></span>](integer.md)                   | <span data-ttu-id="4bdfd-130">N</span><span class="sxs-lookup"><span data-stu-id="4bdfd-130">N</span></span>   | <span data-ttu-id="4bdfd-131">N</span><span class="sxs-lookup"><span data-stu-id="4bdfd-131">N</span></span>        |



 

## <a name="columns"></a><span data-ttu-id="4bdfd-132">資料行</span><span class="sxs-lookup"><span data-stu-id="4bdfd-132">Columns</span></span>

<dl> <dt>

<span data-ttu-id="4bdfd-133"><span id="FileKey"></span><span id="filekey"></span><span id="FILEKEY"></span>FileKey</span><span class="sxs-lookup"><span data-stu-id="4bdfd-133"><span id="FileKey"></span><span id="filekey"></span><span id="FILEKEY"></span>FileKey</span></span>
</dt> <dd>

<span data-ttu-id="4bdfd-134">用來識別這個特定資料表專案的主要索引鍵。</span><span class="sxs-lookup"><span data-stu-id="4bdfd-134">Primary key used to identify this particular table entry.</span></span>

</dd> <dt>

<span data-ttu-id="4bdfd-135"><span id="Component_"></span><span id="component_"></span><span id="COMPONENT_"></span>元件\_</span><span class="sxs-lookup"><span data-stu-id="4bdfd-135"><span id="Component_"></span><span id="component_"></span><span id="COMPONENT_"></span>Component\_</span></span>
</dt> <dd>

<span data-ttu-id="4bdfd-136">[元件資料表](component-table.md)的第一個資料行的外部索引鍵。</span><span class="sxs-lookup"><span data-stu-id="4bdfd-136">External key the first column of the [Component table](component-table.md).</span></span> <span data-ttu-id="4bdfd-137">此欄位會參考控制要移除之檔案的元件。</span><span class="sxs-lookup"><span data-stu-id="4bdfd-137">This field references the component that controls the file to be removed.</span></span>

</dd> <dt>

<span data-ttu-id="4bdfd-138"><span id="FileName"></span><span id="filename"></span><span id="FILENAME"></span>檔案名</span><span class="sxs-lookup"><span data-stu-id="4bdfd-138"><span id="FileName"></span><span id="filename"></span><span id="FILENAME"></span>FileName</span></span>
</dt> <dd>

<span data-ttu-id="4bdfd-139">此資料行包含要移除之檔案的可當地語系化名稱。</span><span class="sxs-lookup"><span data-stu-id="4bdfd-139">This column contains the localizable name of the file to be removed.</span></span> <span data-ttu-id="4bdfd-140">如果這個資料行是 null，則如果指定的資料夾是空的，則會將它移除。</span><span class="sxs-lookup"><span data-stu-id="4bdfd-140">If this column is null, then the specified folder will be removed if it is empty.</span></span> <span data-ttu-id="4bdfd-141">所有符合萬用字元的檔案都將從指定的目錄中移除。</span><span class="sxs-lookup"><span data-stu-id="4bdfd-141">All of the files that match the wildcard will be removed from the specified directory.</span></span>

</dd> <dt>

<span data-ttu-id="4bdfd-142"><span id="DirProperty"></span><span id="dirproperty"></span><span id="DIRPROPERTY"></span>DirProperty</span><span class="sxs-lookup"><span data-stu-id="4bdfd-142"><span id="DirProperty"></span><span id="dirproperty"></span><span id="DIRPROPERTY"></span>DirProperty</span></span>
</dt> <dd>

<span data-ttu-id="4bdfd-143">屬性的名稱，其值會被假設解析為要移除之檔案資料夾的完整路徑。</span><span class="sxs-lookup"><span data-stu-id="4bdfd-143">Name of a property whose value is assumed to resolve to the full path to the folder of the file to be removed.</span></span> <span data-ttu-id="4bdfd-144">屬性可以是 [目錄資料表](directory-table.md)中目錄的名稱、 [AppSearch 資料表](appsearch-table.md)所設定的屬性，或是表示完整路徑的任何其他屬性。</span><span class="sxs-lookup"><span data-stu-id="4bdfd-144">The property can be the name of a directory in the [Directory table](directory-table.md), a property set by the [AppSearch table](appsearch-table.md), or any other property that represents a full path.</span></span>

</dd> <dt>

<span data-ttu-id="4bdfd-145"><span id="InstallMode"></span><span id="installmode"></span><span id="INSTALLMODE"></span>InstallMode</span><span class="sxs-lookup"><span data-stu-id="4bdfd-145"><span id="InstallMode"></span><span id="installmode"></span><span id="INSTALLMODE"></span>InstallMode</span></span>
</dt> <dd>

<span data-ttu-id="4bdfd-146">必須是下列其中一個值。</span><span class="sxs-lookup"><span data-stu-id="4bdfd-146">Must be one of the following values.</span></span>



| <span data-ttu-id="4bdfd-147">常數</span><span class="sxs-lookup"><span data-stu-id="4bdfd-147">Constant</span></span>                                | <span data-ttu-id="4bdfd-148">十六進位</span><span class="sxs-lookup"><span data-stu-id="4bdfd-148">Hexadecimal</span></span> | <span data-ttu-id="4bdfd-149">Decimal</span><span class="sxs-lookup"><span data-stu-id="4bdfd-149">Decimal</span></span> | <span data-ttu-id="4bdfd-150">Description</span><span class="sxs-lookup"><span data-stu-id="4bdfd-150">Description</span></span>                                                                                                   |
|-----------------------------------------|-------------|---------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4bdfd-151">**msidbRemoveFileInstallModeOnInstall**</span><span class="sxs-lookup"><span data-stu-id="4bdfd-151">**msidbRemoveFileInstallModeOnInstall**</span></span> | <span data-ttu-id="4bdfd-152">0x001</span><span class="sxs-lookup"><span data-stu-id="4bdfd-152">0x001</span></span>       | <span data-ttu-id="4bdfd-153">1</span><span class="sxs-lookup"><span data-stu-id="4bdfd-153">1</span></span>       | <span data-ttu-id="4bdfd-154">只有在 (msiInstallStateLocal 或 msiInstallStateSource) 安裝相關聯的元件時，才移除。</span><span class="sxs-lookup"><span data-stu-id="4bdfd-154">Remove only when the associated component is being installed (msiInstallStateLocal or msiInstallStateSource).</span></span> |
| <span data-ttu-id="4bdfd-155">**msidbRemoveFileInstallModeOnRemove**</span><span class="sxs-lookup"><span data-stu-id="4bdfd-155">**msidbRemoveFileInstallModeOnRemove**</span></span>  | <span data-ttu-id="4bdfd-156">0x002</span><span class="sxs-lookup"><span data-stu-id="4bdfd-156">0x002</span></span>       | <span data-ttu-id="4bdfd-157">2</span><span class="sxs-lookup"><span data-stu-id="4bdfd-157">2</span></span>       | <span data-ttu-id="4bdfd-158">只有在 (msiInstallStateAbsent) 移除相關聯的元件時，才移除。</span><span class="sxs-lookup"><span data-stu-id="4bdfd-158">Remove only when the associated component is being removed (msiInstallStateAbsent).</span></span>                           |
| <span data-ttu-id="4bdfd-159">**msidbRemoveFileInstallModeOnBoth**</span><span class="sxs-lookup"><span data-stu-id="4bdfd-159">**msidbRemoveFileInstallModeOnBoth**</span></span>    | <span data-ttu-id="4bdfd-160">0x003</span><span class="sxs-lookup"><span data-stu-id="4bdfd-160">0x003</span></span>       | <span data-ttu-id="4bdfd-161">3</span><span class="sxs-lookup"><span data-stu-id="4bdfd-161">3</span></span>       | <span data-ttu-id="4bdfd-162">在上述任一情況下移除。</span><span class="sxs-lookup"><span data-stu-id="4bdfd-162">Remove in either of the above cases.</span></span>                                                                          |



 

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="4bdfd-163">備註</span><span class="sxs-lookup"><span data-stu-id="4bdfd-163">Remarks</span></span>

<span data-ttu-id="4bdfd-164">此資料表中的檔案參考是由 [RemoveFiles 動作](removefiles-action.md)處理。</span><span class="sxs-lookup"><span data-stu-id="4bdfd-164">The file references in this table are processed by the [RemoveFiles action](removefiles-action.md).</span></span>

## <a name="validation"></a><span data-ttu-id="4bdfd-165">驗證</span><span class="sxs-lookup"><span data-stu-id="4bdfd-165">Validation</span></span>

<dl>

[<span data-ttu-id="4bdfd-166">ICE03</span><span class="sxs-lookup"><span data-stu-id="4bdfd-166">ICE03</span></span>](ice03.md)  
[<span data-ttu-id="4bdfd-167">ICE06</span><span class="sxs-lookup"><span data-stu-id="4bdfd-167">ICE06</span></span>](ice06.md)  
[<span data-ttu-id="4bdfd-168">ICE18</span><span class="sxs-lookup"><span data-stu-id="4bdfd-168">ICE18</span></span>](ice18.md)  
[<span data-ttu-id="4bdfd-169">ICE32</span><span class="sxs-lookup"><span data-stu-id="4bdfd-169">ICE32</span></span>](ice32.md)  
[<span data-ttu-id="4bdfd-170">ICE45</span><span class="sxs-lookup"><span data-stu-id="4bdfd-170">ICE45</span></span>](ice45.md)  
[<span data-ttu-id="4bdfd-171">ICE64</span><span class="sxs-lookup"><span data-stu-id="4bdfd-171">ICE64</span></span>](ice64.md)  
</dl>

 

 



