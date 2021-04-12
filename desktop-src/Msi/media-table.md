---
description: 媒體資料表描述組成安裝來源媒體的磁片集。
ms.assetid: f9789f1d-35bf-40d6-9724-d5a160a0d06d
title: 媒體資料表
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5a59cd8bf864aa890891873ed92a39225c6eebdf
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/03/2021
ms.locfileid: "104321479"
---
# <a name="media-table"></a><span data-ttu-id="02637-103">媒體資料表</span><span class="sxs-lookup"><span data-stu-id="02637-103">Media Table</span></span>

<span data-ttu-id="02637-104">媒體資料表描述組成安裝來源媒體的磁片集。</span><span class="sxs-lookup"><span data-stu-id="02637-104">The Media table describes the set of disks that make up the source media for the installation.</span></span>

<span data-ttu-id="02637-105">媒體資料表包含下表所示的資料行。</span><span class="sxs-lookup"><span data-stu-id="02637-105">The Media table contains the columns shown in the following table.</span></span>



| <span data-ttu-id="02637-106">Column</span><span class="sxs-lookup"><span data-stu-id="02637-106">Column</span></span>       | <span data-ttu-id="02637-107">類型</span><span class="sxs-lookup"><span data-stu-id="02637-107">Type</span></span>                     | <span data-ttu-id="02637-108">答案</span><span class="sxs-lookup"><span data-stu-id="02637-108">Key</span></span> | <span data-ttu-id="02637-109">Nullable</span><span class="sxs-lookup"><span data-stu-id="02637-109">Nullable</span></span> |
|--------------|--------------------------|-----|----------|
| <span data-ttu-id="02637-110">DiskId</span><span class="sxs-lookup"><span data-stu-id="02637-110">DiskId</span></span>       | [<span data-ttu-id="02637-111">整數</span><span class="sxs-lookup"><span data-stu-id="02637-111">Integer</span></span>](integer.md)   | <span data-ttu-id="02637-112">Y</span><span class="sxs-lookup"><span data-stu-id="02637-112">Y</span></span>   | <span data-ttu-id="02637-113">N</span><span class="sxs-lookup"><span data-stu-id="02637-113">N</span></span>        |
| <span data-ttu-id="02637-114">LastSequence</span><span class="sxs-lookup"><span data-stu-id="02637-114">LastSequence</span></span> | [<span data-ttu-id="02637-115">整數</span><span class="sxs-lookup"><span data-stu-id="02637-115">Integer</span></span>](integer.md)   | <span data-ttu-id="02637-116">N</span><span class="sxs-lookup"><span data-stu-id="02637-116">N</span></span>   | <span data-ttu-id="02637-117">N</span><span class="sxs-lookup"><span data-stu-id="02637-117">N</span></span>        |
| <span data-ttu-id="02637-118">DiskPrompt</span><span class="sxs-lookup"><span data-stu-id="02637-118">DiskPrompt</span></span>   | [<span data-ttu-id="02637-119">Text</span><span class="sxs-lookup"><span data-stu-id="02637-119">Text</span></span>](text.md)         | <span data-ttu-id="02637-120">N</span><span class="sxs-lookup"><span data-stu-id="02637-120">N</span></span>   | <span data-ttu-id="02637-121">Y</span><span class="sxs-lookup"><span data-stu-id="02637-121">Y</span></span>        |
| <span data-ttu-id="02637-122">內閣</span><span class="sxs-lookup"><span data-stu-id="02637-122">Cabinet</span></span>      | [<span data-ttu-id="02637-123">內閣</span><span class="sxs-lookup"><span data-stu-id="02637-123">Cabinet</span></span>](cabinet.md)   | <span data-ttu-id="02637-124">N</span><span class="sxs-lookup"><span data-stu-id="02637-124">N</span></span>   | <span data-ttu-id="02637-125">Y</span><span class="sxs-lookup"><span data-stu-id="02637-125">Y</span></span>        |
| <span data-ttu-id="02637-126">VolumeLabel</span><span class="sxs-lookup"><span data-stu-id="02637-126">VolumeLabel</span></span>  | [<span data-ttu-id="02637-127">Text</span><span class="sxs-lookup"><span data-stu-id="02637-127">Text</span></span>](text.md)         | <span data-ttu-id="02637-128">N</span><span class="sxs-lookup"><span data-stu-id="02637-128">N</span></span>   | <span data-ttu-id="02637-129">Y</span><span class="sxs-lookup"><span data-stu-id="02637-129">Y</span></span>        |
| <span data-ttu-id="02637-130">來源</span><span class="sxs-lookup"><span data-stu-id="02637-130">Source</span></span>       | [<span data-ttu-id="02637-131">屬性</span><span class="sxs-lookup"><span data-stu-id="02637-131">Property</span></span>](property.md) | <span data-ttu-id="02637-132">N</span><span class="sxs-lookup"><span data-stu-id="02637-132">N</span></span>   | <span data-ttu-id="02637-133">Y</span><span class="sxs-lookup"><span data-stu-id="02637-133">Y</span></span>        |



 

## <a name="columns"></a><span data-ttu-id="02637-134">資料行</span><span class="sxs-lookup"><span data-stu-id="02637-134">Columns</span></span>

<dl> <dt>

<span data-ttu-id="02637-135"><span id="DiskId"></span><span id="diskid"></span><span id="DISKID"></span>DiskId</span><span class="sxs-lookup"><span data-stu-id="02637-135"><span id="DiskId"></span><span id="diskid"></span><span id="DISKID"></span>DiskId</span></span>
</dt> <dd>

<span data-ttu-id="02637-136">決定資料表的排序次序。</span><span class="sxs-lookup"><span data-stu-id="02637-136">Determines the sort order for the table.</span></span> <span data-ttu-id="02637-137">此數位必須等於或大於1。</span><span class="sxs-lookup"><span data-stu-id="02637-137">This number must be equal to or greater than 1.</span></span>

</dd> <dt>

<span data-ttu-id="02637-138"><span id="LastSequence"></span><span id="lastsequence"></span><span id="LASTSEQUENCE"></span>LastSequence</span><span class="sxs-lookup"><span data-stu-id="02637-138"><span id="LastSequence"></span><span id="lastsequence"></span><span id="LASTSEQUENCE"></span>LastSequence</span></span>
</dt> <dd>

<span data-ttu-id="02637-139">此媒體之最後一個檔案的檔案序號。</span><span class="sxs-lookup"><span data-stu-id="02637-139">File sequence number for the last file for this media.</span></span> <span data-ttu-id="02637-140">LastSequence 資料行中的數位會指定 [檔案資料表中的哪些](file-table.md) 檔案是在特定的來源磁片上找到。</span><span class="sxs-lookup"><span data-stu-id="02637-140">The numbers in the LastSequence column specify which of the files in the [File](file-table.md) table are found on a particular source disk.</span></span> <span data-ttu-id="02637-141">每個來源磁片都包含序號 (的所有檔案，如 [檔案] 資料表的 [順序] 資料行中所示) 小於或等於 [LastSequence] 資料行中的值，以及大於前一個磁片 (或大於0的 LastSequence 值（針對媒體資料表) 中的第一個專案）。</span><span class="sxs-lookup"><span data-stu-id="02637-141">Each source disk contains all files with sequence numbers (as shown in the Sequence column of the File table) less than or equal to the value in the LastSequence column, and greater than the LastSequence value of the previous disk (or greater than 0, for the first entry in the Media table).</span></span> <span data-ttu-id="02637-142">此數位必須為非負數;最大限制為32767個檔案。</span><span class="sxs-lookup"><span data-stu-id="02637-142">This number must be non-negative; the maximum limit is 32767 files.</span></span> <span data-ttu-id="02637-143">如需有關使用更多檔案建立 Windows Installer 套件的詳細資訊，請參閱 [撰寫大型封裝](authoring-a-large-package.md)。</span><span class="sxs-lookup"><span data-stu-id="02637-143">For more information about creating a Windows Installer package with more files, see [Authoring a Large Package](authoring-a-large-package.md).</span></span>

</dd> <dt>

<span data-ttu-id="02637-144"><span id="DiskPrompt"></span><span id="diskprompt"></span><span id="DISKPROMPT"></span>DiskPrompt</span><span class="sxs-lookup"><span data-stu-id="02637-144"><span id="DiskPrompt"></span><span id="diskprompt"></span><span id="DISKPROMPT"></span>DiskPrompt</span></span>
</dt> <dd>

<span data-ttu-id="02637-145">磁片名稱，通常是列印在磁片上的可見文字。</span><span class="sxs-lookup"><span data-stu-id="02637-145">The disk name, which is usually the visible text printed on the disk.</span></span> <span data-ttu-id="02637-146">這個可當地語系化的文字是用來在需要插入磁片時提示使用者。</span><span class="sxs-lookup"><span data-stu-id="02637-146">This localizable text is used to prompt the user when this disk needs to be inserted.</span></span>

</dd> <dt>

<span data-ttu-id="02637-147"><span id="Cabinet"></span><span id="cabinet"></span><span id="CABINET"></span>內閣</span><span class="sxs-lookup"><span data-stu-id="02637-147"><span id="Cabinet"></span><span id="cabinet"></span><span id="CABINET"></span>Cabinet</span></span>
</dt> <dd>

<span data-ttu-id="02637-148">如果儲存在媒體上的部分或所有檔案壓縮成封包檔，則為封包的名稱。</span><span class="sxs-lookup"><span data-stu-id="02637-148">The name of the cabinet if some or all of the files stored on the media are compressed into a cabinet file.</span></span> <span data-ttu-id="02637-149">如果未使用任何封包，則此資料行必須為空白。</span><span class="sxs-lookup"><span data-stu-id="02637-149">If no cabinets are used, this column must be blank.</span></span> <span data-ttu-id="02637-150">封包的名稱必須使用封 [包](cabinet.md) 資料類型的語法。</span><span class="sxs-lookup"><span data-stu-id="02637-150">The name of the cabinet must use the syntax of the [Cabinet](cabinet.md) data type.</span></span> <span data-ttu-id="02637-151">Windows Installer 一律需要有效的來源，才能修復內嵌封包檔中包含的檔案。</span><span class="sxs-lookup"><span data-stu-id="02637-151">Windows Installer always requires a valid source to repair files included in embedded cabinet files.</span></span> <span data-ttu-id="02637-152">當 Windows Installer 安裝包含內嵌封包檔的封裝時，系統會儲存封包檔的複本。</span><span class="sxs-lookup"><span data-stu-id="02637-152">When Windows Installer installs a package containing an embedded cabinet file, a copy of the cabinet file can be saved by the system.</span></span> <span data-ttu-id="02637-153">此複本無法用來修復封包檔。</span><span class="sxs-lookup"><span data-stu-id="02637-153">This copy cannot be used to repair the cabinet file.</span></span> <span data-ttu-id="02637-154">若要節省磁碟空間，請使用外部封包檔，而不是內嵌的封包檔。</span><span class="sxs-lookup"><span data-stu-id="02637-154">To conserve disk space, use external cabinet files instead of embedded cabinet files.</span></span>

</dd> <dt>

<span data-ttu-id="02637-155"><span id="VolumeLabel"></span><span id="volumelabel"></span><span id="VOLUMELABEL"></span>VolumeLabel</span><span class="sxs-lookup"><span data-stu-id="02637-155"><span id="VolumeLabel"></span><span id="volumelabel"></span><span id="VOLUMELABEL"></span>VolumeLabel</span></span>
</dt> <dd>

<span data-ttu-id="02637-156">屬於磁片區的標籤。</span><span class="sxs-lookup"><span data-stu-id="02637-156">The label attributed to the volume.</span></span> <span data-ttu-id="02637-157">這是 [**GetVolumeInformation**](/windows/win32/api/fileapi/nf-fileapi-getvolumeinformationa) 函式所傳回的磁片區標籤。</span><span class="sxs-lookup"><span data-stu-id="02637-157">This is the volume label returned by the [**GetVolumeInformation**](/windows/win32/api/fileapi/nf-fileapi-getvolumeinformationa) function.</span></span> <span data-ttu-id="02637-158">如果 [**SourceDir**](sourcedir.md) 內容參考可移動 (磁片或 cd-rom) 磁片區，則會使用此磁片區標籤來確認磁片磁碟機中是否有適當的磁片，然後再嘗試安裝檔案。</span><span class="sxs-lookup"><span data-stu-id="02637-158">If the [**SourceDir**](sourcedir.md) property refers to a removable (floppy or CD-ROM) volume, then this volume label is used to verify that the proper disk is in the drive before attempting to install files.</span></span> <span data-ttu-id="02637-159">此資料行中的專案必須符合實體媒體的磁片區標籤。</span><span class="sxs-lookup"><span data-stu-id="02637-159">The entry in this column must match the volume label of the physical media.</span></span>

</dd> <dt>

<span data-ttu-id="02637-160"><span id="Source"></span><span id="source"></span><span id="SOURCE"></span>源</span><span class="sxs-lookup"><span data-stu-id="02637-160"><span id="Source"></span><span id="source"></span><span id="SOURCE"></span>Source</span></span>
</dt> <dd>

<span data-ttu-id="02637-161">此欄位僅供修補使用，否則會保留空白。</span><span class="sxs-lookup"><span data-stu-id="02637-161">This field is only used by patching and is otherwise left blank.</span></span> <span data-ttu-id="02637-162">修補程式轉換可以在這裡輸入內容，這是包含修補檔案的封包檔的位置，或修補程式所加入的任何新檔案。</span><span class="sxs-lookup"><span data-stu-id="02637-162">A patch transform can enter a property here that is the location of the cabinet file containing the patch files or any new files added by the patch.</span></span> <span data-ttu-id="02637-163">您必須為這些檔案指定不同的來源，因為修補套件的來源可以與產品的來源分開儲存。</span><span class="sxs-lookup"><span data-stu-id="02637-163">A different source needs to be specified for these files because the source of the patch package can be stored separately from the product's source.</span></span> <span data-ttu-id="02637-164">如果 [封包] 欄位是空的，安裝程式會忽略此資料行中的值。</span><span class="sxs-lookup"><span data-stu-id="02637-164">If the Cabinet field is empty, the installer ignores the value in this column.</span></span> <span data-ttu-id="02637-165">如果這個欄位是空的，安裝程式會使用 [**SourceDir**](sourcedir.md) 屬性的值做為封包的來源。</span><span class="sxs-lookup"><span data-stu-id="02637-165">If this field is empty, the installer uses the value of the [**SourceDir**](sourcedir.md) property as the source of the cabinet.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="02637-166">備註</span><span class="sxs-lookup"><span data-stu-id="02637-166">Remarks</span></span>

<span data-ttu-id="02637-167">如果封包名稱前面加上數位記號 (\#) ，則參考此媒體資料表記錄的檔案會封裝在以個別資料流程形式儲存在資料庫中的封包檔中。</span><span class="sxs-lookup"><span data-stu-id="02637-167">If the cabinet name is preceded by a number sign (\#), then the files referencing this Media table record are packed in a cabinet file that is stored within the database as a separate stream.</span></span>

<span data-ttu-id="02637-168">如需如何將封包新增至檔案資料表和媒體資料表的詳細資訊，請參閱 [使用封包和壓縮的來源](using-cabinets-and-compressed-sources.md)。</span><span class="sxs-lookup"><span data-stu-id="02637-168">For more information about how to add cabinets to the File tables and Media tables, see [Using Cabinets and Compressed Sources](using-cabinets-and-compressed-sources.md).</span></span>

<span data-ttu-id="02637-169">Windows Installer 要求 .msi 檔案必須位於卸載式媒體的第一個磁片上， (CD、DVD 或磁片) 用於產品的安裝。</span><span class="sxs-lookup"><span data-stu-id="02637-169">Windows Installer requires that the .msi file be on the first disk of removable media (CD, DVD or floppy) used for the product's installation.</span></span>

<span data-ttu-id="02637-170">**判斷 SourceMode**</span><span class="sxs-lookup"><span data-stu-id="02637-170">**Determining the SourceMode**</span></span>

<span data-ttu-id="02637-171">[ [**字數統計摘要**](word-count-summary.md) ] 屬性會決定目前安裝的來源模式。</span><span class="sxs-lookup"><span data-stu-id="02637-171">The [**Word Count Summary**](word-count-summary.md) property determines the source mode for the current install.</span></span> <span data-ttu-id="02637-172">如果這個屬性設定為2或3，則會假設為封包安裝。</span><span class="sxs-lookup"><span data-stu-id="02637-172">If this property is set to 2 or 3, a cabinet install is assumed.</span></span> <span data-ttu-id="02637-173">在此模式中，會假設封包檔存在於 [**SourceDir**](sourcedir.md) 屬性所指示的目錄中。</span><span class="sxs-lookup"><span data-stu-id="02637-173">In this mode, the cabinet files are assumed to exist in the directory indicated by the [**SourceDir**](sourcedir.md) property.</span></span> <span data-ttu-id="02637-174">如果來源類型值為0或1，則會假設所有原始程式檔都存在於樹狀結構中，其根目錄會以 **SourceDir** 屬性工作表示。</span><span class="sxs-lookup"><span data-stu-id="02637-174">If the Source Type value is 0 or 1, all source files are assumed to exist in the tree whose root is indicated by the **SourceDir** property.</span></span>

<span data-ttu-id="02637-175">請注意，這只適用于檔案資料表中，未在 [屬性] 資料行中設定壓縮或未壓縮位的檔案。</span><span class="sxs-lookup"><span data-stu-id="02637-175">Note that this only applies to files in the File table that do not have either the Compressed or Uncompressed bits set in the attributes column.</span></span> <span data-ttu-id="02637-176">判斷特定檔案是否已壓縮或未壓縮時，這些位會覆寫 [ [**字數統計摘要**](word-count-summary.md) ] 屬性的值。</span><span class="sxs-lookup"><span data-stu-id="02637-176">These bits override the value of the [**Word Count Summary**](word-count-summary.md) property when determining if a particular file is compressed or uncompressed.</span></span>

## <a name="validation"></a><span data-ttu-id="02637-177">驗證</span><span class="sxs-lookup"><span data-stu-id="02637-177">Validation</span></span>

<dl>

[<span data-ttu-id="02637-178">ICE03</span><span class="sxs-lookup"><span data-stu-id="02637-178">ICE03</span></span>](ice03.md)  
[<span data-ttu-id="02637-179">ICE04</span><span class="sxs-lookup"><span data-stu-id="02637-179">ICE04</span></span>](ice04.md)  
[<span data-ttu-id="02637-180">ICE06</span><span class="sxs-lookup"><span data-stu-id="02637-180">ICE06</span></span>](ice06.md)  
[<span data-ttu-id="02637-181">ICE35</span><span class="sxs-lookup"><span data-stu-id="02637-181">ICE35</span></span>](ice35.md)  
[<span data-ttu-id="02637-182">ICE58</span><span class="sxs-lookup"><span data-stu-id="02637-182">ICE58</span></span>](ice58.md)  
[<span data-ttu-id="02637-183">ICE71</span><span class="sxs-lookup"><span data-stu-id="02637-183">ICE71</span></span>](ice71.md)  
[<span data-ttu-id="02637-184">ICE81</span><span class="sxs-lookup"><span data-stu-id="02637-184">ICE81</span></span>](ice81.md)  
</dl>

 

 
