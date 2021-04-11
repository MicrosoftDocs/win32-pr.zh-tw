---
description: Patch 資料表指定要接收特定修補程式的檔案，以及媒體映射上修補檔案的實體位置。
ms.assetid: 1b624702-de25-4b1a-9dac-21f359ee97f7
title: 修補資料表
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 061b2082f88a8c7c3967652900bb6bf6e1c29802
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103695408"
---
# <a name="patch-table"></a><span data-ttu-id="10a12-103">修補資料表</span><span class="sxs-lookup"><span data-stu-id="10a12-103">Patch Table</span></span>

<span data-ttu-id="10a12-104">Patch 資料表指定要接收特定修補程式的檔案，以及媒體映射上修補檔案的實體位置。</span><span class="sxs-lookup"><span data-stu-id="10a12-104">The Patch table specifies the file that is to receive a particular patch and the physical location of the patch files on the media images.</span></span>

<span data-ttu-id="10a12-105">Patch 資料表有下列資料行。</span><span class="sxs-lookup"><span data-stu-id="10a12-105">The Patch table has the following columns.</span></span>



| <span data-ttu-id="10a12-106">Column</span><span class="sxs-lookup"><span data-stu-id="10a12-106">Column</span></span>      | <span data-ttu-id="10a12-107">類型</span><span class="sxs-lookup"><span data-stu-id="10a12-107">Type</span></span>                               | <span data-ttu-id="10a12-108">答案</span><span class="sxs-lookup"><span data-stu-id="10a12-108">Key</span></span> | <span data-ttu-id="10a12-109">Nullable</span><span class="sxs-lookup"><span data-stu-id="10a12-109">Nullable</span></span> |
|-------------|------------------------------------|-----|----------|
| <span data-ttu-id="10a12-110">檔案\_</span><span class="sxs-lookup"><span data-stu-id="10a12-110">File\_</span></span>      | [<span data-ttu-id="10a12-111">識別碼</span><span class="sxs-lookup"><span data-stu-id="10a12-111">Identifier</span></span>](identifier.md)       | <span data-ttu-id="10a12-112">Y</span><span class="sxs-lookup"><span data-stu-id="10a12-112">Y</span></span>   | <span data-ttu-id="10a12-113">N</span><span class="sxs-lookup"><span data-stu-id="10a12-113">N</span></span>        |
| <span data-ttu-id="10a12-114">順序</span><span class="sxs-lookup"><span data-stu-id="10a12-114">Sequence</span></span>    | [<span data-ttu-id="10a12-115">整數</span><span class="sxs-lookup"><span data-stu-id="10a12-115">Integer</span></span>](integer.md)             | <span data-ttu-id="10a12-116">Y</span><span class="sxs-lookup"><span data-stu-id="10a12-116">Y</span></span>   | <span data-ttu-id="10a12-117">N</span><span class="sxs-lookup"><span data-stu-id="10a12-117">N</span></span>        |
| <span data-ttu-id="10a12-118">PatchSize</span><span class="sxs-lookup"><span data-stu-id="10a12-118">PatchSize</span></span>   | [<span data-ttu-id="10a12-119">DoubleInteger</span><span class="sxs-lookup"><span data-stu-id="10a12-119">DoubleInteger</span></span>](doubleinteger.md) | <span data-ttu-id="10a12-120">N</span><span class="sxs-lookup"><span data-stu-id="10a12-120">N</span></span>   | <span data-ttu-id="10a12-121">N</span><span class="sxs-lookup"><span data-stu-id="10a12-121">N</span></span>        |
| <span data-ttu-id="10a12-122">屬性</span><span class="sxs-lookup"><span data-stu-id="10a12-122">Attributes</span></span>  | [<span data-ttu-id="10a12-123">整數</span><span class="sxs-lookup"><span data-stu-id="10a12-123">Integer</span></span>](integer.md)             | <span data-ttu-id="10a12-124">N</span><span class="sxs-lookup"><span data-stu-id="10a12-124">N</span></span>   | <span data-ttu-id="10a12-125">N</span><span class="sxs-lookup"><span data-stu-id="10a12-125">N</span></span>        |
| <span data-ttu-id="10a12-126">標頭</span><span class="sxs-lookup"><span data-stu-id="10a12-126">Header</span></span>      | [<span data-ttu-id="10a12-127">二進位</span><span class="sxs-lookup"><span data-stu-id="10a12-127">Binary</span></span>](binary.md)               | <span data-ttu-id="10a12-128">N</span><span class="sxs-lookup"><span data-stu-id="10a12-128">N</span></span>   | <span data-ttu-id="10a12-129">Y</span><span class="sxs-lookup"><span data-stu-id="10a12-129">Y</span></span>        |
| <span data-ttu-id="10a12-130">StreamRef\_</span><span class="sxs-lookup"><span data-stu-id="10a12-130">StreamRef\_</span></span> | [<span data-ttu-id="10a12-131">識別碼</span><span class="sxs-lookup"><span data-stu-id="10a12-131">Identifier</span></span>](identifier.md)       | <span data-ttu-id="10a12-132">N</span><span class="sxs-lookup"><span data-stu-id="10a12-132">N</span></span>   | <span data-ttu-id="10a12-133">Y</span><span class="sxs-lookup"><span data-stu-id="10a12-133">Y</span></span>        |



 

## <a name="columns"></a><span data-ttu-id="10a12-134">資料行</span><span class="sxs-lookup"><span data-stu-id="10a12-134">Columns</span></span>

<dl> <dt>

<span data-ttu-id="10a12-135"><span id="File_"></span><span id="file_"></span><span id="FILE_"></span>檔\_</span><span class="sxs-lookup"><span data-stu-id="10a12-135"><span id="File_"></span><span id="file_"></span><span id="FILE_"></span>File\_</span></span>
</dt> <dd>

<span data-ttu-id="10a12-136">此修補程式會套用至此資料行中的識別碼所指定的檔案。</span><span class="sxs-lookup"><span data-stu-id="10a12-136">The patch is applied to the file specified by the identifier in this column.</span></span> <span data-ttu-id="10a12-137">這是資料表的主鍵，而且它是 [File 資料表](file-table.md)的外鍵。</span><span class="sxs-lookup"><span data-stu-id="10a12-137">This is a primary key for the table and it is a foreign key to the [File table](file-table.md).</span></span>

</dd> <dt>

<span data-ttu-id="10a12-138"><span id="Sequence"></span><span id="sequence"></span><span id="SEQUENCE"></span>序列</span><span class="sxs-lookup"><span data-stu-id="10a12-138"><span id="Sequence"></span><span id="sequence"></span><span id="SEQUENCE"></span>Sequence</span></span>
</dt> <dd>

<span data-ttu-id="10a12-139">這是修補檔案的位置，以媒體映射上檔案的順序排列。</span><span class="sxs-lookup"><span data-stu-id="10a12-139">This is the position of the patch file in the sequence order of files on the media images.</span></span> <span data-ttu-id="10a12-140">順序必須對應至修補封裝封包檔中的檔案順序。</span><span class="sxs-lookup"><span data-stu-id="10a12-140">The sequence order must correspond to the order of the files in the patch package cabinet file.</span></span> <span data-ttu-id="10a12-141">這是此資料表的主要索引鍵。</span><span class="sxs-lookup"><span data-stu-id="10a12-141">This is a primary key for this table.</span></span> <span data-ttu-id="10a12-142">最大限制為32767個檔案，若要建立具有更多檔案的 Windows Installer 封裝，請參閱 [撰寫大型封裝](authoring-a-large-package.md)。</span><span class="sxs-lookup"><span data-stu-id="10a12-142">The maximum limit is 32767 files, to create a Windows Installer package with more files, see [Authoring a Large Package](authoring-a-large-package.md).</span></span>

</dd> <dt>

<span data-ttu-id="10a12-143"><span id="PatchSize"></span><span id="patchsize"></span><span id="PATCHSIZE"></span>PatchSize</span><span class="sxs-lookup"><span data-stu-id="10a12-143"><span id="PatchSize"></span><span id="patchsize"></span><span id="PATCHSIZE"></span>PatchSize</span></span>
</dt> <dd>

<span data-ttu-id="10a12-144">此資料行提供以長整數寫入的修補程式大小。</span><span class="sxs-lookup"><span data-stu-id="10a12-144">This column gives the size of the patch in bytes written as a long integer.</span></span>

</dd> <dt>

<span data-ttu-id="10a12-145"><span id="Attributes"></span><span id="attributes"></span><span id="ATTRIBUTES"></span>屬性</span><span class="sxs-lookup"><span data-stu-id="10a12-145"><span id="Attributes"></span><span id="attributes"></span><span id="ATTRIBUTES"></span>Attributes</span></span>
</dt> <dd>

<span data-ttu-id="10a12-146">包含代表 patch 屬性之位旗標的整數。</span><span class="sxs-lookup"><span data-stu-id="10a12-146">Integer containing bit flags representing patch attributes.</span></span> <span data-ttu-id="10a12-147">在此資料行中插入1的值，表示套用此修補程式的失敗不是嚴重錯誤。</span><span class="sxs-lookup"><span data-stu-id="10a12-147">Insert a value of 1 in this column to indicate that the failure to apply this patch is not a fatal error.</span></span>



| <span data-ttu-id="10a12-148">常數</span><span class="sxs-lookup"><span data-stu-id="10a12-148">Constant</span></span>                         | <span data-ttu-id="10a12-149">十六進位</span><span class="sxs-lookup"><span data-stu-id="10a12-149">Hexadecimal</span></span> | <span data-ttu-id="10a12-150">Decimal</span><span class="sxs-lookup"><span data-stu-id="10a12-150">Decimal</span></span> | <span data-ttu-id="10a12-151">Description</span><span class="sxs-lookup"><span data-stu-id="10a12-151">Description</span></span>                                                          |
|----------------------------------|-------------|---------|----------------------------------------------------------------------|
| <span data-ttu-id="10a12-152">(無)</span><span class="sxs-lookup"><span data-stu-id="10a12-152">(none)</span></span>                           | <span data-ttu-id="10a12-153">0x000</span><span class="sxs-lookup"><span data-stu-id="10a12-153">0x000</span></span>       | <span data-ttu-id="10a12-154">0</span><span class="sxs-lookup"><span data-stu-id="10a12-154">0</span></span>       | <span data-ttu-id="10a12-155">無法套用此修補程式是嚴重錯誤。</span><span class="sxs-lookup"><span data-stu-id="10a12-155">Failure to apply this patch is a fatal error.</span></span>                        |
| <span data-ttu-id="10a12-156">**msidbPatchAttributesNonVital**</span><span class="sxs-lookup"><span data-stu-id="10a12-156">**msidbPatchAttributesNonVital**</span></span> | <span data-ttu-id="10a12-157">0x001</span><span class="sxs-lookup"><span data-stu-id="10a12-157">0x001</span></span>       | <span data-ttu-id="10a12-158">1</span><span class="sxs-lookup"><span data-stu-id="10a12-158">1</span></span>       | <span data-ttu-id="10a12-159">指出套用此修補程式的失敗不是嚴重錯誤。</span><span class="sxs-lookup"><span data-stu-id="10a12-159">Indicates that the failure to apply this patch is not a fatal error.</span></span> |



 

</dd> <dt>

<span data-ttu-id="10a12-160"><span id="Header"></span><span id="header"></span><span id="HEADER"></span>頭</span><span class="sxs-lookup"><span data-stu-id="10a12-160"><span id="Header"></span><span id="header"></span><span id="HEADER"></span>Header</span></span>
</dt> <dd>

<span data-ttu-id="10a12-161">此資料行是用於修補驗證的二進位資料流程修補程式標頭。</span><span class="sxs-lookup"><span data-stu-id="10a12-161">This column is the binary stream patch header used for patch validation.</span></span> <span data-ttu-id="10a12-162">如果 StreamRef 資料 \_ 行不是 null，這個資料行應該是 null。</span><span class="sxs-lookup"><span data-stu-id="10a12-162">This column should be null if the StreamRef\_ column is not null.</span></span> <span data-ttu-id="10a12-163">在此情況下，patch 標頭資料流程會儲存在 [MsiPatchHeaders 資料表](msipatchheaders-table.md) 中，以克服 [OLE 限制對資料流程](ole-limitations-on-streams.md)所述的資料流程名稱限制。</span><span class="sxs-lookup"><span data-stu-id="10a12-163">In this case, the patch header stream is stored in the [MsiPatchHeaders table](msipatchheaders-table.md) to overcome the stream name limitation described in [OLE Limitations on Streams](ole-limitations-on-streams.md).</span></span>

</dd> <dt>

<span data-ttu-id="10a12-164"><span id="StreamRef_"></span><span id="streamref_"></span><span id="STREAMREF_"></span>StreamRef\_</span><span class="sxs-lookup"><span data-stu-id="10a12-164"><span id="StreamRef_"></span><span id="streamref_"></span><span id="STREAMREF_"></span>StreamRef\_</span></span>
</dt> <dd>

<span data-ttu-id="10a12-165">MsiPatchHeaders 資料表中的外部索引鍵，指定包含 patch 標頭資料流程的資料列。</span><span class="sxs-lookup"><span data-stu-id="10a12-165">External key into the MsiPatchHeaders table specifying the row that contains the patch header stream.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="10a12-166">備註</span><span class="sxs-lookup"><span data-stu-id="10a12-166">Remarks</span></span>

<span data-ttu-id="10a12-167">此資料表是由 [PatchFiles 動作](patchfiles-action.md)處理。</span><span class="sxs-lookup"><span data-stu-id="10a12-167">This table is processed by the [PatchFiles action](patchfiles-action.md).</span></span> <span data-ttu-id="10a12-168">它通常會透過修補套件的轉換新增至安裝套件。</span><span class="sxs-lookup"><span data-stu-id="10a12-168">It is usually added to the install package by a transform from a patch package.</span></span> <span data-ttu-id="10a12-169">它通常不會直接撰寫到安裝套件中。</span><span class="sxs-lookup"><span data-stu-id="10a12-169">It is usually not authored directly into an install package.</span></span>

## <a name="validation"></a><span data-ttu-id="10a12-170">驗證</span><span class="sxs-lookup"><span data-stu-id="10a12-170">Validation</span></span>

<dl>

[<span data-ttu-id="10a12-171">ICE03</span><span class="sxs-lookup"><span data-stu-id="10a12-171">ICE03</span></span>](ice03.md)  
[<span data-ttu-id="10a12-172">ICE06</span><span class="sxs-lookup"><span data-stu-id="10a12-172">ICE06</span></span>](ice06.md)  
[<span data-ttu-id="10a12-173">ICE29</span><span class="sxs-lookup"><span data-stu-id="10a12-173">ICE29</span></span>](ice29.md)  
[<span data-ttu-id="10a12-174">ICE45</span><span class="sxs-lookup"><span data-stu-id="10a12-174">ICE45</span></span>](ice45.md)  
</dl>

 

 



