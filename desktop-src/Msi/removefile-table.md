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
# <a name="removefile-table"></a><span data-ttu-id="56cda-104">RemoveFile 資料表</span><span class="sxs-lookup"><span data-stu-id="56cda-104">RemoveFile Table</span></span>

<span data-ttu-id="56cda-105">RemoveFile 資料表包含 [RemoveFiles 動作](removefiles-action.md)要移除的檔案清單。</span><span class="sxs-lookup"><span data-stu-id="56cda-105">The RemoveFile table contains a list of files to be removed by the [RemoveFiles action](removefiles-action.md).</span></span> <span data-ttu-id="56cda-106">將此資料表的 FileName 資料行設定為 Null，可支援移除空的資料夾。</span><span class="sxs-lookup"><span data-stu-id="56cda-106">Setting the FileName column of this table to Null supports the removal of empty folders.</span></span>

<span data-ttu-id="56cda-107">RemoveFile 資料表具有下列資料行。</span><span class="sxs-lookup"><span data-stu-id="56cda-107">The RemoveFile table has the following columns.</span></span>



| <span data-ttu-id="56cda-108">Column</span><span class="sxs-lookup"><span data-stu-id="56cda-108">Column</span></span>      | <span data-ttu-id="56cda-109">類型</span><span class="sxs-lookup"><span data-stu-id="56cda-109">Type</span></span>                                     | <span data-ttu-id="56cda-110">答案</span><span class="sxs-lookup"><span data-stu-id="56cda-110">Key</span></span> | <span data-ttu-id="56cda-111">Nullable</span><span class="sxs-lookup"><span data-stu-id="56cda-111">Nullable</span></span> |
|-------------|------------------------------------------|-----|----------|
| <span data-ttu-id="56cda-112">FileKey</span><span class="sxs-lookup"><span data-stu-id="56cda-112">FileKey</span></span>     | [<span data-ttu-id="56cda-113">識別碼</span><span class="sxs-lookup"><span data-stu-id="56cda-113">Identifier</span></span>](identifier.md)             | <span data-ttu-id="56cda-114">Y</span><span class="sxs-lookup"><span data-stu-id="56cda-114">Y</span></span>   | <span data-ttu-id="56cda-115">N</span><span class="sxs-lookup"><span data-stu-id="56cda-115">N</span></span>        |
| <span data-ttu-id="56cda-116">元件\_</span><span class="sxs-lookup"><span data-stu-id="56cda-116">Component\_</span></span> | [<span data-ttu-id="56cda-117">識別碼</span><span class="sxs-lookup"><span data-stu-id="56cda-117">Identifier</span></span>](identifier.md)             | <span data-ttu-id="56cda-118">N</span><span class="sxs-lookup"><span data-stu-id="56cda-118">N</span></span>   | <span data-ttu-id="56cda-119">N</span><span class="sxs-lookup"><span data-stu-id="56cda-119">N</span></span>        |
| <span data-ttu-id="56cda-120">FileName</span><span class="sxs-lookup"><span data-stu-id="56cda-120">FileName</span></span>    | [<span data-ttu-id="56cda-121">WildCardFilename</span><span class="sxs-lookup"><span data-stu-id="56cda-121">WildCardFilename</span></span>](wildcardfilename.md) | <span data-ttu-id="56cda-122">N</span><span class="sxs-lookup"><span data-stu-id="56cda-122">N</span></span>   | <span data-ttu-id="56cda-123">Y</span><span class="sxs-lookup"><span data-stu-id="56cda-123">Y</span></span>        |
| <span data-ttu-id="56cda-124">DirProperty</span><span class="sxs-lookup"><span data-stu-id="56cda-124">DirProperty</span></span> | [<span data-ttu-id="56cda-125">識別碼</span><span class="sxs-lookup"><span data-stu-id="56cda-125">Identifier</span></span>](identifier.md)             | <span data-ttu-id="56cda-126">N</span><span class="sxs-lookup"><span data-stu-id="56cda-126">N</span></span>   | <span data-ttu-id="56cda-127">N</span><span class="sxs-lookup"><span data-stu-id="56cda-127">N</span></span>        |
| <span data-ttu-id="56cda-128">InstallMode</span><span class="sxs-lookup"><span data-stu-id="56cda-128">InstallMode</span></span> | [<span data-ttu-id="56cda-129">整數</span><span class="sxs-lookup"><span data-stu-id="56cda-129">Integer</span></span>](integer.md)                   | <span data-ttu-id="56cda-130">N</span><span class="sxs-lookup"><span data-stu-id="56cda-130">N</span></span>   | <span data-ttu-id="56cda-131">N</span><span class="sxs-lookup"><span data-stu-id="56cda-131">N</span></span>        |



 

## <a name="columns"></a><span data-ttu-id="56cda-132">資料行</span><span class="sxs-lookup"><span data-stu-id="56cda-132">Columns</span></span>

<dl> <dt>

<span data-ttu-id="56cda-133"><span id="FileKey"></span><span id="filekey"></span><span id="FILEKEY"></span>FileKey</span><span class="sxs-lookup"><span data-stu-id="56cda-133"><span id="FileKey"></span><span id="filekey"></span><span id="FILEKEY"></span>FileKey</span></span>
</dt> <dd>

<span data-ttu-id="56cda-134">用來識別這個特定資料表專案的主要索引鍵。</span><span class="sxs-lookup"><span data-stu-id="56cda-134">Primary key used to identify this particular table entry.</span></span>

</dd> <dt>

<span data-ttu-id="56cda-135"><span id="Component_"></span><span id="component_"></span><span id="COMPONENT_"></span>元件\_</span><span class="sxs-lookup"><span data-stu-id="56cda-135"><span id="Component_"></span><span id="component_"></span><span id="COMPONENT_"></span>Component\_</span></span>
</dt> <dd>

<span data-ttu-id="56cda-136">[元件資料表](component-table.md)的第一個資料行的外部索引鍵。</span><span class="sxs-lookup"><span data-stu-id="56cda-136">External key the first column of the [Component table](component-table.md).</span></span> <span data-ttu-id="56cda-137">此欄位會參考控制要移除之檔案的元件。</span><span class="sxs-lookup"><span data-stu-id="56cda-137">This field references the component that controls the file to be removed.</span></span>

</dd> <dt>

<span data-ttu-id="56cda-138"><span id="FileName"></span><span id="filename"></span><span id="FILENAME"></span>檔案名</span><span class="sxs-lookup"><span data-stu-id="56cda-138"><span id="FileName"></span><span id="filename"></span><span id="FILENAME"></span>FileName</span></span>
</dt> <dd>

<span data-ttu-id="56cda-139">此資料行包含要移除之檔案的可當地語系化名稱。</span><span class="sxs-lookup"><span data-stu-id="56cda-139">This column contains the localizable name of the file to be removed.</span></span> <span data-ttu-id="56cda-140">如果這個資料行是 null，則如果指定的資料夾是空的，則會將它移除。</span><span class="sxs-lookup"><span data-stu-id="56cda-140">If this column is null, then the specified folder will be removed if it is empty.</span></span> <span data-ttu-id="56cda-141">所有符合萬用字元的檔案都將從指定的目錄中移除。</span><span class="sxs-lookup"><span data-stu-id="56cda-141">All of the files that match the wildcard will be removed from the specified directory.</span></span>

</dd> <dt>

<span data-ttu-id="56cda-142"><span id="DirProperty"></span><span id="dirproperty"></span><span id="DIRPROPERTY"></span>DirProperty</span><span class="sxs-lookup"><span data-stu-id="56cda-142"><span id="DirProperty"></span><span id="dirproperty"></span><span id="DIRPROPERTY"></span>DirProperty</span></span>
</dt> <dd>

<span data-ttu-id="56cda-143">屬性的名稱，其值會被假設解析為要移除之檔案資料夾的完整路徑。</span><span class="sxs-lookup"><span data-stu-id="56cda-143">Name of a property whose value is assumed to resolve to the full path to the folder of the file to be removed.</span></span> <span data-ttu-id="56cda-144">屬性可以是 [目錄資料表](directory-table.md)中目錄的名稱、 [AppSearch 資料表](appsearch-table.md)所設定的屬性，或是表示完整路徑的任何其他屬性。</span><span class="sxs-lookup"><span data-stu-id="56cda-144">The property can be the name of a directory in the [Directory table](directory-table.md), a property set by the [AppSearch table](appsearch-table.md), or any other property that represents a full path.</span></span>

</dd> <dt>

<span data-ttu-id="56cda-145"><span id="InstallMode"></span><span id="installmode"></span><span id="INSTALLMODE"></span>InstallMode</span><span class="sxs-lookup"><span data-stu-id="56cda-145"><span id="InstallMode"></span><span id="installmode"></span><span id="INSTALLMODE"></span>InstallMode</span></span>
</dt> <dd>

<span data-ttu-id="56cda-146">必須是下列其中一個值。</span><span class="sxs-lookup"><span data-stu-id="56cda-146">Must be one of the following values.</span></span>



| <span data-ttu-id="56cda-147">常數</span><span class="sxs-lookup"><span data-stu-id="56cda-147">Constant</span></span>                                | <span data-ttu-id="56cda-148">十六進位</span><span class="sxs-lookup"><span data-stu-id="56cda-148">Hexadecimal</span></span> | <span data-ttu-id="56cda-149">Decimal</span><span class="sxs-lookup"><span data-stu-id="56cda-149">Decimal</span></span> | <span data-ttu-id="56cda-150">Description</span><span class="sxs-lookup"><span data-stu-id="56cda-150">Description</span></span>                                                                                                   |
|-----------------------------------------|-------------|---------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="56cda-151">**msidbRemoveFileInstallModeOnInstall**</span><span class="sxs-lookup"><span data-stu-id="56cda-151">**msidbRemoveFileInstallModeOnInstall**</span></span> | <span data-ttu-id="56cda-152">0x001</span><span class="sxs-lookup"><span data-stu-id="56cda-152">0x001</span></span>       | <span data-ttu-id="56cda-153">1</span><span class="sxs-lookup"><span data-stu-id="56cda-153">1</span></span>       | <span data-ttu-id="56cda-154">只有在 (msiInstallStateLocal 或 msiInstallStateSource) 安裝相關聯的元件時，才移除。</span><span class="sxs-lookup"><span data-stu-id="56cda-154">Remove only when the associated component is being installed (msiInstallStateLocal or msiInstallStateSource).</span></span> |
| <span data-ttu-id="56cda-155">**msidbRemoveFileInstallModeOnRemove**</span><span class="sxs-lookup"><span data-stu-id="56cda-155">**msidbRemoveFileInstallModeOnRemove**</span></span>  | <span data-ttu-id="56cda-156">0x002</span><span class="sxs-lookup"><span data-stu-id="56cda-156">0x002</span></span>       | <span data-ttu-id="56cda-157">2</span><span class="sxs-lookup"><span data-stu-id="56cda-157">2</span></span>       | <span data-ttu-id="56cda-158">只有在 (msiInstallStateAbsent) 移除相關聯的元件時，才移除。</span><span class="sxs-lookup"><span data-stu-id="56cda-158">Remove only when the associated component is being removed (msiInstallStateAbsent).</span></span>                           |
| <span data-ttu-id="56cda-159">**msidbRemoveFileInstallModeOnBoth**</span><span class="sxs-lookup"><span data-stu-id="56cda-159">**msidbRemoveFileInstallModeOnBoth**</span></span>    | <span data-ttu-id="56cda-160">0x003</span><span class="sxs-lookup"><span data-stu-id="56cda-160">0x003</span></span>       | <span data-ttu-id="56cda-161">3</span><span class="sxs-lookup"><span data-stu-id="56cda-161">3</span></span>       | <span data-ttu-id="56cda-162">在上述任一情況下移除。</span><span class="sxs-lookup"><span data-stu-id="56cda-162">Remove in either of the above cases.</span></span>                                                                          |



 

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="56cda-163">備註</span><span class="sxs-lookup"><span data-stu-id="56cda-163">Remarks</span></span>

<span data-ttu-id="56cda-164">此資料表中的檔案參考是由 [RemoveFiles 動作](removefiles-action.md)處理。</span><span class="sxs-lookup"><span data-stu-id="56cda-164">The file references in this table are processed by the [RemoveFiles action](removefiles-action.md).</span></span>

## <a name="validation"></a><span data-ttu-id="56cda-165">驗證</span><span class="sxs-lookup"><span data-stu-id="56cda-165">Validation</span></span>

<dl>

[<span data-ttu-id="56cda-166">ICE03</span><span class="sxs-lookup"><span data-stu-id="56cda-166">ICE03</span></span>](ice03.md)  
[<span data-ttu-id="56cda-167">ICE06</span><span class="sxs-lookup"><span data-stu-id="56cda-167">ICE06</span></span>](ice06.md)  
[<span data-ttu-id="56cda-168">ICE18</span><span class="sxs-lookup"><span data-stu-id="56cda-168">ICE18</span></span>](ice18.md)  
[<span data-ttu-id="56cda-169">ICE32</span><span class="sxs-lookup"><span data-stu-id="56cda-169">ICE32</span></span>](ice32.md)  
[<span data-ttu-id="56cda-170">ICE45</span><span class="sxs-lookup"><span data-stu-id="56cda-170">ICE45</span></span>](ice45.md)  
[<span data-ttu-id="56cda-171">ICE64</span><span class="sxs-lookup"><span data-stu-id="56cda-171">ICE64</span></span>](ice64.md)  
</dl>

 

 



