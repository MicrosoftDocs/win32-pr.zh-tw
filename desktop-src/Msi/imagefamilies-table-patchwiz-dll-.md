---
description: 映射家族是已更新為最新版本之產品的一或多個已升級映射的群組。
ms.assetid: 06a77b35-b593-47e6-9083-46a6b65b7481
title: 'ImageFamilies 資料表 (Patchwiz.dll) '
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 33ece99e3c42626eb2155f16f2198703dc31b682
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103943717"
---
# <a name="imagefamilies-table-patchwizdll"></a><span data-ttu-id="11e86-103">ImageFamilies 資料表 (Patchwiz.dll) </span><span class="sxs-lookup"><span data-stu-id="11e86-103">ImageFamilies Table (Patchwiz.dll)</span></span>

<span data-ttu-id="11e86-104">映射家族是已更新為最新版本之產品的一或多個已升級映射的群組。</span><span class="sxs-lookup"><span data-stu-id="11e86-104">An image family is a group of one or more upgraded images of a product that have been updated to the most recent version.</span></span> <span data-ttu-id="11e86-105">每個升級的映射只能屬於一個系列。</span><span class="sxs-lookup"><span data-stu-id="11e86-105">Each upgraded image can belong to only one family.</span></span> <span data-ttu-id="11e86-106">屬於映射系列的已升級映射會共用一或多個檔案。</span><span class="sxs-lookup"><span data-stu-id="11e86-106">Upgraded images belonging to an image family share one or more files.</span></span> <span data-ttu-id="11e86-107">每個映射系列在 .msp 檔中都有自己的封包檔，其中包含更新目標和升級檔案之間差異所需的二進位修補程式和新檔案。</span><span class="sxs-lookup"><span data-stu-id="11e86-107">Each image family has its own cabinet file in the .msp file containing the binary patches and new files needed to update the differences between target and upgraded files.</span></span> <span data-ttu-id="11e86-108">封包檔不會複寫共用檔案所使用的二進位修補程式和新檔案。</span><span class="sxs-lookup"><span data-stu-id="11e86-108">The cabinet file does not replicate the binary patches and new files used by the shared files.</span></span>

<span data-ttu-id="11e86-109">在每個修補程式建立資料庫中都必須包含至少一筆記錄的 ImageFamilies 資料表， ( pcp 檔案) 。</span><span class="sxs-lookup"><span data-stu-id="11e86-109">An ImageFamilies table containing at least one record is required in every patch creation database (.pcp file).</span></span> <span data-ttu-id="11e86-110">此資料表是由 [UiCreatePatchPackageEx](uicreatepatchpackageex--patchwiz-dll-.md) 函數所使用。</span><span class="sxs-lookup"><span data-stu-id="11e86-110">This table is used by the [UiCreatePatchPackageEx](uicreatepatchpackageex--patchwiz-dll-.md) function.</span></span>

<span data-ttu-id="11e86-111">ImageFamilies 資料表包含要新增至 [媒體資料表](media-table.md)的修補資訊。</span><span class="sxs-lookup"><span data-stu-id="11e86-111">The ImageFamilies table contains the patching information that is to be added to the [Media table](media-table.md).</span></span> <span data-ttu-id="11e86-112">修補程式會將一個專案新增至媒體資料表。</span><span class="sxs-lookup"><span data-stu-id="11e86-112">A patch adds one entry to the Media table.</span></span> <span data-ttu-id="11e86-113">ImageFamilies 資料表中的每一筆記錄都會參考一組已更新為最新產品版本的相關產品影像。</span><span class="sxs-lookup"><span data-stu-id="11e86-113">Each record in the ImageFamilies tables refers to a group of related product images that have been updated to the most recent version of the product.</span></span>

<span data-ttu-id="11e86-114">ImageFamilies 資料表具有下列資料行。</span><span class="sxs-lookup"><span data-stu-id="11e86-114">The ImageFamilies table has the following columns.</span></span> <span data-ttu-id="11e86-115">如果 MediaSrcPropName、MediaDiskId 和 FileSequenceStart 資料行套用修補程式與 Windows Installer 和 Patchwiz.dll 2.0 版，則可以在、和資料行中使用 null 值。</span><span class="sxs-lookup"><span data-stu-id="11e86-115">A null value can be used in the MediaSrcPropName, MediaDiskId, and FileSequenceStart columns if the patch is applied with Windows Installer and Patchwiz.dll version 2.0.</span></span>



| <span data-ttu-id="11e86-116">Column</span><span class="sxs-lookup"><span data-stu-id="11e86-116">Column</span></span>            | <span data-ttu-id="11e86-117">類型</span><span class="sxs-lookup"><span data-stu-id="11e86-117">Type</span></span>    | <span data-ttu-id="11e86-118">答案</span><span class="sxs-lookup"><span data-stu-id="11e86-118">Key</span></span> | <span data-ttu-id="11e86-119">Nullable</span><span class="sxs-lookup"><span data-stu-id="11e86-119">Nullable</span></span> |
|-------------------|---------|-----|----------|
| <span data-ttu-id="11e86-120">系列</span><span class="sxs-lookup"><span data-stu-id="11e86-120">Family</span></span>            | <span data-ttu-id="11e86-121">text</span><span class="sxs-lookup"><span data-stu-id="11e86-121">text</span></span>    | <span data-ttu-id="11e86-122">Y</span><span class="sxs-lookup"><span data-stu-id="11e86-122">Y</span></span>   | <span data-ttu-id="11e86-123">N</span><span class="sxs-lookup"><span data-stu-id="11e86-123">N</span></span>        |
| <span data-ttu-id="11e86-124">MediaSrcPropName</span><span class="sxs-lookup"><span data-stu-id="11e86-124">MediaSrcPropName</span></span>  | <span data-ttu-id="11e86-125">text</span><span class="sxs-lookup"><span data-stu-id="11e86-125">text</span></span>    |     | <span data-ttu-id="11e86-126">Y</span><span class="sxs-lookup"><span data-stu-id="11e86-126">Y</span></span>        |
| <span data-ttu-id="11e86-127">MediaDiskId</span><span class="sxs-lookup"><span data-stu-id="11e86-127">MediaDiskId</span></span>       | <span data-ttu-id="11e86-128">整數</span><span class="sxs-lookup"><span data-stu-id="11e86-128">integer</span></span> |     | <span data-ttu-id="11e86-129">Y</span><span class="sxs-lookup"><span data-stu-id="11e86-129">Y</span></span>        |
| <span data-ttu-id="11e86-130">FileSequenceStart</span><span class="sxs-lookup"><span data-stu-id="11e86-130">FileSequenceStart</span></span> | <span data-ttu-id="11e86-131">整數</span><span class="sxs-lookup"><span data-stu-id="11e86-131">integer</span></span> |     | <span data-ttu-id="11e86-132">Y</span><span class="sxs-lookup"><span data-stu-id="11e86-132">Y</span></span>        |
| <span data-ttu-id="11e86-133">DiskPrompt</span><span class="sxs-lookup"><span data-stu-id="11e86-133">DiskPrompt</span></span>        | <span data-ttu-id="11e86-134">text</span><span class="sxs-lookup"><span data-stu-id="11e86-134">text</span></span>    |     | <span data-ttu-id="11e86-135">Y</span><span class="sxs-lookup"><span data-stu-id="11e86-135">Y</span></span>        |
| <span data-ttu-id="11e86-136">VolumeLabel</span><span class="sxs-lookup"><span data-stu-id="11e86-136">VolumeLabel</span></span>       | <span data-ttu-id="11e86-137">text</span><span class="sxs-lookup"><span data-stu-id="11e86-137">text</span></span>    |     | <span data-ttu-id="11e86-138">Y</span><span class="sxs-lookup"><span data-stu-id="11e86-138">Y</span></span>        |



 

## <a name="columns"></a><span data-ttu-id="11e86-139">資料行</span><span class="sxs-lookup"><span data-stu-id="11e86-139">Columns</span></span>

<dl> <dt>

<span data-ttu-id="11e86-140"><span id="Family"></span><span id="family"></span><span id="FAMILY"></span>家庭</span><span class="sxs-lookup"><span data-stu-id="11e86-140"><span id="Family"></span><span id="family"></span><span id="FAMILY"></span>Family</span></span>
</dt> <dd>

<span data-ttu-id="11e86-141">在此欄位中輸入的值是已更新為產品最新版本之相關產品影像群組的識別碼。</span><span class="sxs-lookup"><span data-stu-id="11e86-141">The value entered in this field is an identifier for a group of related product images that have been updated to the most recent version of the product.</span></span> <span data-ttu-id="11e86-142">限制為總共8個英數位元或底線。</span><span class="sxs-lookup"><span data-stu-id="11e86-142">Limited to a total of 8 alphanumeric characters or underscores.</span></span> <span data-ttu-id="11e86-143">安裝程式會在 Windows Installer 修補檔中，為數據表中的每個系列內嵌一個封包資料流程 ( .msp 檔) 。</span><span class="sxs-lookup"><span data-stu-id="11e86-143">The installer embeds a cabinet stream in the Windows Installer patch file (.msp file) for each family in the table.</span></span> <span data-ttu-id="11e86-144">此封包包含二進位修補程式，以及將目標映射更新為產品的升級映射時所需的新檔案。</span><span class="sxs-lookup"><span data-stu-id="11e86-144">The cabinet contains the binary patches and new files required to update a target image into an upgraded image of the product.</span></span> <span data-ttu-id="11e86-145">安裝程式會在 PCW CAB 的系列名稱前加上前置詞， \_ \_ 以產生封包在新 [媒體資料表](media-table.md) 專案的 [封包] 欄位中輸入的資料流程名稱。</span><span class="sxs-lookup"><span data-stu-id="11e86-145">The installer prefixes the family name with PCW\_CAB\_ to generate the cabinet's stream name it enters into the Cabinet field of the new [Media table](media-table.md) entry.</span></span>

</dd> <dt>

<span data-ttu-id="11e86-146"><span id="MediaSrcPropName"></span><span id="mediasrcpropname"></span><span id="MEDIASRCPROPNAME"></span>MediaSrcPropName</span><span class="sxs-lookup"><span data-stu-id="11e86-146"><span id="MediaSrcPropName"></span><span id="mediasrcpropname"></span><span id="MEDIASRCPROPNAME"></span>MediaSrcPropName</span></span>
</dt> <dd>

<span data-ttu-id="11e86-147">在已升級影像的新 [媒體資料表](media-table.md) 專案的 [來源] 欄位中輸入的值。</span><span class="sxs-lookup"><span data-stu-id="11e86-147">The value entered into the Source field of the new [Media table](media-table.md) entry of the upgraded image.</span></span> <span data-ttu-id="11e86-148">只有當您使用2.0 版的 Patchwiz.dll，以及屬性工作表中的 MinimumRequiredMsiVersion [ (Patchwiz.dll) ](properties-table-patchwiz-dll-.md) 設定為200時，此欄位才可以是 null。</span><span class="sxs-lookup"><span data-stu-id="11e86-148">This field can be null only if you are using version 2.0 of Patchwiz.dll and if the MinimumRequiredMsiVersion in the [Properties table (Patchwiz.dll)](properties-table-patchwiz-dll-.md) is set to 200.</span></span>

</dd> <dt>

<span data-ttu-id="11e86-149"><span id="MediaDiskId"></span><span id="mediadiskid"></span><span id="MEDIADISKID"></span>MediaDiskId</span><span class="sxs-lookup"><span data-stu-id="11e86-149"><span id="MediaDiskId"></span><span id="mediadiskid"></span><span id="MEDIADISKID"></span>MediaDiskId</span></span>
</dt> <dd>

<span data-ttu-id="11e86-150">安裝程式會在新的 [媒體資料表](media-table.md) 記錄的 DiskId 欄位中輸入此值。</span><span class="sxs-lookup"><span data-stu-id="11e86-150">The installer enters this value into the DiskId field of the new [Media table](media-table.md) record.</span></span> <span data-ttu-id="11e86-151">DiskID 值必須大於目標套件中的任何目前 DiskID。</span><span class="sxs-lookup"><span data-stu-id="11e86-151">The DiskID value must be greater than any current DiskID in the target package.</span></span> <span data-ttu-id="11e86-152">MediaDiskId 的限制為32767。</span><span class="sxs-lookup"><span data-stu-id="11e86-152">The limit for MediaDiskId is 32767.</span></span> <span data-ttu-id="11e86-153">只有當您使用2.0 版的 Patchwiz.dll，以及屬性工作表中的 MinimumRequiredMsiVersion [ (Patchwiz.dll) ](properties-table-patchwiz-dll-.md) 設定為200時，此欄位才可以是 null。</span><span class="sxs-lookup"><span data-stu-id="11e86-153">This field can be null only if you are using version 2.0 of Patchwiz.dll and if the MinimumRequiredMsiVersion in the [Properties table (Patchwiz.dll)](properties-table-patchwiz-dll-.md) is set to 200.</span></span>

</dd> <dt>

<span data-ttu-id="11e86-154"><span id="FileSequenceStart"></span><span id="filesequencestart"></span><span id="FILESEQUENCESTART"></span>FileSequenceStart</span><span class="sxs-lookup"><span data-stu-id="11e86-154"><span id="FileSequenceStart"></span><span id="filesequencestart"></span><span id="FILESEQUENCESTART"></span>FileSequenceStart</span></span>
</dt> <dd>

<span data-ttu-id="11e86-155">此欄位是起始檔案的序號。</span><span class="sxs-lookup"><span data-stu-id="11e86-155">This field is the sequence number for the starting file.</span></span> <span data-ttu-id="11e86-156">相同產品的兩個修補程式中不能有相同的檔案序號。</span><span class="sxs-lookup"><span data-stu-id="11e86-156">This same file sequence number must not exist in two patches for the same product.</span></span> <span data-ttu-id="11e86-157">為確保這一點，此欄位中的值必須大於先前修補或原始安裝套件中使用的所有序號。</span><span class="sxs-lookup"><span data-stu-id="11e86-157">To ensure this, the value in this field must be greater than all sequence numbers used in previous patches or in the original installation package.</span></span> <span data-ttu-id="11e86-158">您可以藉由將修補程式封包檔中的專案總數新增至該修補程式的 FileSequenceStart 號碼，來判斷修補程式中的最大序號。</span><span class="sxs-lookup"><span data-stu-id="11e86-158">The greatest sequence number in a patch can be determined by adding the total number of entries in the patch cabinet file to the FileSequenceStart number for that patch.</span></span> <span data-ttu-id="11e86-159">判斷這一點的其中一種方式，是查看在建立修補程式期間 [Patchwiz.dll](patchwiz-dll.md) 所產生的 ddf 檔案。</span><span class="sxs-lookup"><span data-stu-id="11e86-159">One way to determine this is to look at the .ddf file generated by [Patchwiz.dll](patchwiz-dll.md) during the creation of the patch.</span></span> <span data-ttu-id="11e86-160">FileSequenceStart 的限制為32767。</span><span class="sxs-lookup"><span data-stu-id="11e86-160">The limit for FileSequenceStart is 32767.</span></span> <span data-ttu-id="11e86-161">只有當您使用2.0 版的 Patchwiz.dll，以及屬性工作表中的 MinimumRequiredMsiVersion [ (Patchwiz.dll) ](properties-table-patchwiz-dll-.md) 設定為200時，此欄位才可以是 null。</span><span class="sxs-lookup"><span data-stu-id="11e86-161">This field can be null only if you are using version 2.0 of Patchwiz.dll and if the MinimumRequiredMsiVersion in the [Properties table (Patchwiz.dll)](properties-table-patchwiz-dll-.md) is set to 200.</span></span>

</dd> <dt>

<span data-ttu-id="11e86-162"><span id="DiskPrompt"></span><span id="diskprompt"></span><span id="DISKPROMPT"></span>DiskPrompt</span><span class="sxs-lookup"><span data-stu-id="11e86-162"><span id="DiskPrompt"></span><span id="diskprompt"></span><span id="DISKPROMPT"></span>DiskPrompt</span></span>
</dt> <dd>

<span data-ttu-id="11e86-163">安裝程式會在新的 [媒體資料表](media-table.md) 記錄的 DiskPrompt 欄位中輸入此值。</span><span class="sxs-lookup"><span data-stu-id="11e86-163">The installer enters this value into the DiskPrompt field of the new [Media table](media-table.md) record.</span></span>

</dd> <dt>

<span data-ttu-id="11e86-164"><span id="VolumeLabel"></span><span id="volumelabel"></span><span id="VOLUMELABEL"></span>VolumeLabel</span><span class="sxs-lookup"><span data-stu-id="11e86-164"><span id="VolumeLabel"></span><span id="volumelabel"></span><span id="VOLUMELABEL"></span>VolumeLabel</span></span>
</dt> <dd>

<span data-ttu-id="11e86-165">安裝程式會在新媒體記錄的 VolumeLabel 欄位中輸入此值。</span><span class="sxs-lookup"><span data-stu-id="11e86-165">The installer enters this value into the VolumeLabel field of the new Media record.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="11e86-166">備註</span><span class="sxs-lookup"><span data-stu-id="11e86-166">Remarks</span></span>

<span data-ttu-id="11e86-167">修補程式會將 .msp 檔中的封包名稱新增至新增至 [媒體資料表](media-table.md)的新記錄的 [封包] 欄位中。</span><span class="sxs-lookup"><span data-stu-id="11e86-167">The patch adds the name of the cabinet in the .msp file to the Cabinet field of the new record added to the [Media table](media-table.md).</span></span> <span data-ttu-id="11e86-168">因為它是內嵌的封包，所以名稱前面會加上 ' \# ' 字元。</span><span class="sxs-lookup"><span data-stu-id="11e86-168">Because it is an embedded cabinet, the name is prefixed with a '\#' character.</span></span> <span data-ttu-id="11e86-169">修補程式會將屬性新增至媒體資料表中新記錄的來源欄位。</span><span class="sxs-lookup"><span data-stu-id="11e86-169">The patch adds a property to the Source field of the new record in the Media table.</span></span> <span data-ttu-id="11e86-170">沒有兩個修補程式可能具有相同的來源屬性。</span><span class="sxs-lookup"><span data-stu-id="11e86-170">No two patches may have the same source property.</span></span>

<span data-ttu-id="11e86-171">在映射系列內共用的檔案，在每個升級的系列映射中都必須具有相同的檔案資料表索引鍵。</span><span class="sxs-lookup"><span data-stu-id="11e86-171">The files that are shared within the image family must have the same file table key in each upgraded image of the family.</span></span> <span data-ttu-id="11e86-172">在升級的映射之間共用的任何檔案資料表索引鍵都必須代表相同的檔案，而且在所有升級的映射中都必須相同。</span><span class="sxs-lookup"><span data-stu-id="11e86-172">Any file table keys shared among the upgraded images must represent the same file and must be identical in all the upgraded images.</span></span> <span data-ttu-id="11e86-173">File 資料表索引鍵是在 [file 資料表](file-table.md)的 file 資料行中輸入的值。</span><span class="sxs-lookup"><span data-stu-id="11e86-173">The file table key is the value entered in the File column of the [File table](file-table.md).</span></span>

<span data-ttu-id="11e86-174">MediaDiskId 和 FileSequenceStart 的限制為32767。</span><span class="sxs-lookup"><span data-stu-id="11e86-174">The limit for MediaDiskId and FileSequenceStart is 32767.</span></span> <span data-ttu-id="11e86-175">若要增加此限制，請使用 [Msidb.exe](msidb-exe.md) 將 ImageFamilies 資料表匯出至 idt 檔案，並將資料行類型從 i2 變更為 i4，或從 i2 變更為 i4，然後將 idt 檔案匯回 pcp 資料庫。</span><span class="sxs-lookup"><span data-stu-id="11e86-175">To increase this limit export the ImageFamilies table to an .idt file with [Msidb.exe](msidb-exe.md) and change the column type from i2 to i4, or from I2 to I4, and then import the .idt file back into the .pcp database.</span></span> <span data-ttu-id="11e86-176">無法在具有不同資料行類型的兩個封裝之間建立轉換和修補程式。</span><span class="sxs-lookup"><span data-stu-id="11e86-176">Transforms and patches cannot be created between two packages having different column types.</span></span>

 

 



