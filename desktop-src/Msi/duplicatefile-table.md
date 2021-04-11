---
description: DuplicateFile 資料表包含要複製的檔案清單，可能會複製到與原始檔案不同的目錄，或是與相同的目錄不同的名稱。 原始檔案必須是 InstallFiles 動作所安裝的檔案。
ms.assetid: 7fe1b52d-4b06-48cd-afe5-2bd5495bb55e
title: DuplicateFile 資料表
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 766f28b7984aedfc682a2bf23378d46ee0519c65
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104026881"
---
# <a name="duplicatefile-table"></a><span data-ttu-id="0d3d5-104">DuplicateFile 資料表</span><span class="sxs-lookup"><span data-stu-id="0d3d5-104">DuplicateFile Table</span></span>

<span data-ttu-id="0d3d5-105">DuplicateFile 資料表包含要複製的檔案清單，可能會複製到與原始檔案不同的目錄，或是與相同的目錄不同的名稱。</span><span class="sxs-lookup"><span data-stu-id="0d3d5-105">The DuplicateFile table contains a list of files that are to be duplicated, either to a different directory than the original file or to the same directory but with a different name.</span></span> <span data-ttu-id="0d3d5-106">原始檔案必須是 [InstallFiles 動作](installfiles-action.md)所安裝的檔案。</span><span class="sxs-lookup"><span data-stu-id="0d3d5-106">The original file must be a file installed by the [InstallFiles action](installfiles-action.md).</span></span>

<span data-ttu-id="0d3d5-107">DuplicateFile 資料表具有下列資料行。</span><span class="sxs-lookup"><span data-stu-id="0d3d5-107">The DuplicateFile table has the following columns.</span></span>



| <span data-ttu-id="0d3d5-108">Column</span><span class="sxs-lookup"><span data-stu-id="0d3d5-108">Column</span></span>      | <span data-ttu-id="0d3d5-109">類型</span><span class="sxs-lookup"><span data-stu-id="0d3d5-109">Type</span></span>                         | <span data-ttu-id="0d3d5-110">答案</span><span class="sxs-lookup"><span data-stu-id="0d3d5-110">Key</span></span> | <span data-ttu-id="0d3d5-111">Nullable</span><span class="sxs-lookup"><span data-stu-id="0d3d5-111">Nullable</span></span> |
|-------------|------------------------------|-----|----------|
| <span data-ttu-id="0d3d5-112">FileKey</span><span class="sxs-lookup"><span data-stu-id="0d3d5-112">FileKey</span></span>     | [<span data-ttu-id="0d3d5-113">識別碼</span><span class="sxs-lookup"><span data-stu-id="0d3d5-113">Identifier</span></span>](identifier.md) | <span data-ttu-id="0d3d5-114">Y</span><span class="sxs-lookup"><span data-stu-id="0d3d5-114">Y</span></span>   | <span data-ttu-id="0d3d5-115">N</span><span class="sxs-lookup"><span data-stu-id="0d3d5-115">N</span></span>        |
| <span data-ttu-id="0d3d5-116">元件\_</span><span class="sxs-lookup"><span data-stu-id="0d3d5-116">Component\_</span></span> | [<span data-ttu-id="0d3d5-117">識別碼</span><span class="sxs-lookup"><span data-stu-id="0d3d5-117">Identifier</span></span>](identifier.md) | <span data-ttu-id="0d3d5-118">N</span><span class="sxs-lookup"><span data-stu-id="0d3d5-118">N</span></span>   | <span data-ttu-id="0d3d5-119">N</span><span class="sxs-lookup"><span data-stu-id="0d3d5-119">N</span></span>        |
| <span data-ttu-id="0d3d5-120">檔案\_</span><span class="sxs-lookup"><span data-stu-id="0d3d5-120">File\_</span></span>      | [<span data-ttu-id="0d3d5-121">識別碼</span><span class="sxs-lookup"><span data-stu-id="0d3d5-121">Identifier</span></span>](identifier.md) | <span data-ttu-id="0d3d5-122">N</span><span class="sxs-lookup"><span data-stu-id="0d3d5-122">N</span></span>   | <span data-ttu-id="0d3d5-123">N</span><span class="sxs-lookup"><span data-stu-id="0d3d5-123">N</span></span>        |
| <span data-ttu-id="0d3d5-124">DestName</span><span class="sxs-lookup"><span data-stu-id="0d3d5-124">DestName</span></span>    | [<span data-ttu-id="0d3d5-125">檔案名稱</span><span class="sxs-lookup"><span data-stu-id="0d3d5-125">Filename</span></span>](filename.md)     | <span data-ttu-id="0d3d5-126">N</span><span class="sxs-lookup"><span data-stu-id="0d3d5-126">N</span></span>   | <span data-ttu-id="0d3d5-127">Y</span><span class="sxs-lookup"><span data-stu-id="0d3d5-127">Y</span></span>        |
| <span data-ttu-id="0d3d5-128">DestFolder</span><span class="sxs-lookup"><span data-stu-id="0d3d5-128">DestFolder</span></span>  | [<span data-ttu-id="0d3d5-129">識別碼</span><span class="sxs-lookup"><span data-stu-id="0d3d5-129">Identifier</span></span>](identifier.md) | <span data-ttu-id="0d3d5-130">N</span><span class="sxs-lookup"><span data-stu-id="0d3d5-130">N</span></span>   | <span data-ttu-id="0d3d5-131">Y</span><span class="sxs-lookup"><span data-stu-id="0d3d5-131">Y</span></span>        |



 

## <a name="columns"></a><span data-ttu-id="0d3d5-132">資料行</span><span class="sxs-lookup"><span data-stu-id="0d3d5-132">Columns</span></span>

<dl> <dt>

<span data-ttu-id="0d3d5-133"><span id="FileKey"></span><span id="filekey"></span><span id="FILEKEY"></span>FileKey</span><span class="sxs-lookup"><span data-stu-id="0d3d5-133"><span id="FileKey"></span><span id="filekey"></span><span id="FILEKEY"></span>FileKey</span></span>
</dt> <dd>

<span data-ttu-id="0d3d5-134">主要索引鍵、非當地語系化的 token，識別唯一的 DuplicateFile 記錄。</span><span class="sxs-lookup"><span data-stu-id="0d3d5-134">A primary key, a non-localized token, identifying a unique DuplicateFile record.</span></span>

</dd> <dt>

<span data-ttu-id="0d3d5-135"><span id="Component_"></span><span id="component_"></span><span id="COMPONENT_"></span>元件\_</span><span class="sxs-lookup"><span data-stu-id="0d3d5-135"><span id="Component_"></span><span id="component_"></span><span id="COMPONENT_"></span>Component\_</span></span>
</dt> <dd>

<span data-ttu-id="0d3d5-136">[元件資料表](component-table.md)第一個資料行的外部索引鍵。</span><span class="sxs-lookup"><span data-stu-id="0d3d5-136">An external key to the first column of the [Component table](component-table.md).</span></span> <span data-ttu-id="0d3d5-137">如果未選取索引鍵所識別的元件來進行安裝或移除，則不會在此 DuplicateFile 記錄上採取任何動作。</span><span class="sxs-lookup"><span data-stu-id="0d3d5-137">If the component identified by the key is not selected for installation or removal, then no action is taken on this DuplicateFile record.</span></span>

</dd> <dt>

<span data-ttu-id="0d3d5-138"><span id="File_"></span><span id="file_"></span><span id="FILE_"></span>檔\_</span><span class="sxs-lookup"><span data-stu-id="0d3d5-138"><span id="File_"></span><span id="file_"></span><span id="FILE_"></span>File\_</span></span>
</dt> <dd>

<span data-ttu-id="0d3d5-139">代表要複製之原始檔案的檔案 [資料表](file-table.md) 中的外鍵。</span><span class="sxs-lookup"><span data-stu-id="0d3d5-139">Foreign key into the [File table](file-table.md) representing the original file that is to be duplicated.</span></span>

</dd> <dt>

<span data-ttu-id="0d3d5-140"><span id="DestName"></span><span id="destname"></span><span id="DESTNAME"></span>DestName</span><span class="sxs-lookup"><span data-stu-id="0d3d5-140"><span id="DestName"></span><span id="destname"></span><span id="DESTNAME"></span>DestName</span></span>
</dt> <dd>

<span data-ttu-id="0d3d5-141">要提供給重複檔案的可當地語系化名稱。</span><span class="sxs-lookup"><span data-stu-id="0d3d5-141">Localizable name to be given to the duplicate file.</span></span> <span data-ttu-id="0d3d5-142">如果這個欄位是空白的，則會為目的地檔案提供與原始檔案相同的名稱。</span><span class="sxs-lookup"><span data-stu-id="0d3d5-142">If this field is blank, then the destination file is given the same name as the original file.</span></span>

</dd> <dt>

<span data-ttu-id="0d3d5-143"><span id="DestFolder"></span><span id="destfolder"></span><span id="DESTFOLDER"></span>DestFolder</span><span class="sxs-lookup"><span data-stu-id="0d3d5-143"><span id="DestFolder"></span><span id="destfolder"></span><span id="DESTFOLDER"></span>DestFolder</span></span>
</dt> <dd>

<span data-ttu-id="0d3d5-144">屬性的名稱，這個屬性是複製複製之檔案的完整路徑。</span><span class="sxs-lookup"><span data-stu-id="0d3d5-144">Name of a property that is the full path to where the duplicate file is to be copied.</span></span> <span data-ttu-id="0d3d5-145">如果這個目錄與包含原始檔案的目錄相同，且建議的重複檔案名稱與原始檔案相同，則不會進行任何動作。</span><span class="sxs-lookup"><span data-stu-id="0d3d5-145">If this directory is the same as the directory containing the original file and the name for the proposed duplicate file is the same as the original, then no action takes place.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="0d3d5-146">備註</span><span class="sxs-lookup"><span data-stu-id="0d3d5-146">Remarks</span></span>

<span data-ttu-id="0d3d5-147">資料表是由 [DuplicateFiles 動作](duplicatefiles-action.md) 和 [RemoveDuplicateFiles 動作](removeduplicatefiles-action.md)來處理。</span><span class="sxs-lookup"><span data-stu-id="0d3d5-147">The table is processed by the [DuplicateFiles action](duplicatefiles-action.md) and the [RemoveDuplicateFiles action](removeduplicatefiles-action.md).</span></span>

## <a name="validation"></a><span data-ttu-id="0d3d5-148">驗證</span><span class="sxs-lookup"><span data-stu-id="0d3d5-148">Validation</span></span>

<dl>

[<span data-ttu-id="0d3d5-149">ICE03</span><span class="sxs-lookup"><span data-stu-id="0d3d5-149">ICE03</span></span>](ice03.md)  
[<span data-ttu-id="0d3d5-150">ICE06</span><span class="sxs-lookup"><span data-stu-id="0d3d5-150">ICE06</span></span>](ice06.md)  
[<span data-ttu-id="0d3d5-151">ICE18</span><span class="sxs-lookup"><span data-stu-id="0d3d5-151">ICE18</span></span>](ice18.md)  
[<span data-ttu-id="0d3d5-152">ICE32</span><span class="sxs-lookup"><span data-stu-id="0d3d5-152">ICE32</span></span>](ice32.md)  
</dl>

 

 



