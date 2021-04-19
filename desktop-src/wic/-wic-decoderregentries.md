---
description: Decoder-Specific 登錄專案
ms.assetid: 64ef260a-ed7f-4253-a644-bd3352b0ee41
title: Decoder-Specific 登錄專案
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 17485e7adca62abd31643d84d371a0002724ea9f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106980067"
---
# <a name="decoder-specific-registry-entries"></a><span data-ttu-id="18fdb-103">Decoder-Specific 登錄專案</span><span class="sxs-lookup"><span data-stu-id="18fdb-103">Decoder-Specific Registry Entries</span></span>


<span data-ttu-id="18fdb-104">除了所有編碼器和解碼器所需的登錄專案之外，還需要下列登錄專案，特別是針對該解碼器。</span><span class="sxs-lookup"><span data-stu-id="18fdb-104">In addition to the registry entries required for all encoders and decoders, the following registry entries are required specifically for decoders.</span></span>

<span data-ttu-id="18fdb-105">這些專案會將您的解碼器註冊在 Windows 影像處理元件 (WIC) 解碼器的類別中。</span><span class="sxs-lookup"><span data-stu-id="18fdb-105">These entries register your decoder under the category of Windows Imaging Component (WIC) decoders.</span></span> <span data-ttu-id="18fdb-106">這些專案中的第一個 GUID 是 [**WICBitmapDecoders**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder))  (CATID 的分類識別碼。</span><span class="sxs-lookup"><span data-stu-id="18fdb-106">The first GUID in these entries is the category identifier (CATID) for [**WICBitmapDecoders**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder).</span></span>

```
HKEY_CLASSES_ROOT
   CLSID
      {7ED96837-96F0-4812-B211-F13C24117ED3}
         Instance
            {Decoder CLSID}
               CLSID = {Decoder CLSID}
               FriendlyName = {Name of Decoder}
```

<span data-ttu-id="18fdb-107">如同 Windows 影像處理元件運作方式的 [探索和仲裁](-wic-howwicworks.md) 一節中所述，在執行時間針對特定映射啟用適當的解碼器的機制，是以比對影像檔案中的識別模式與在解碼器登錄專案中指定的模式來進行。</span><span class="sxs-lookup"><span data-stu-id="18fdb-107">As noted in [Discovery and Arbitration](-wic-howwicworks.md) section of How The Windows Imaging Component Works, the mechanism that enables an appropriate decoder for a specific image to be discovered at run time is based on matching an identifying pattern embedded in the image file with a pattern specified in the decoder’s registry entry.</span></span> <span data-ttu-id="18fdb-108">若要啟用以執行時間探索的解碼器，您必須為映射格式註冊唯一的識別模式，如下所示。</span><span class="sxs-lookup"><span data-stu-id="18fdb-108">To enable run-time discovery of decoders, you must register the unique identifying pattern for your image format as follows.</span></span> <span data-ttu-id="18fdb-109">除了 **EndOfStream** 專案之外，所有的登錄專案都是必要專案，這是選擇性的，如下表所述。</span><span class="sxs-lookup"><span data-stu-id="18fdb-109">All of these registry entries are required except for the **EndOfStream** entry, which is optional, as described in the following table.</span></span>

```
HKEY_CLASSES_ROOT
   CLSID
      {Decoder CLSID}
         Patterns
            {0}
               Position = Offset in block
               Length = Length of pattern
               Pattern = Pattern to match
               Mask = FF FF FF FF
               EndOfStream = 0|1
```



| <span data-ttu-id="18fdb-110">值</span><span class="sxs-lookup"><span data-stu-id="18fdb-110">Value</span></span>       | <span data-ttu-id="18fdb-111">描述</span><span class="sxs-lookup"><span data-stu-id="18fdb-111">Description</span></span>                                                                                                                                                                                                                                                                                                                     |
|-------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="18fdb-112">位置</span><span class="sxs-lookup"><span data-stu-id="18fdb-112">Position</span></span>    | <span data-ttu-id="18fdb-113">可以在檔案中找到模式的位移。</span><span class="sxs-lookup"><span data-stu-id="18fdb-113">The offset into the file where the pattern can be found.</span></span>                                                                                                                                                                                                                                                                        |
| <span data-ttu-id="18fdb-114">長度</span><span class="sxs-lookup"><span data-stu-id="18fdb-114">Length</span></span>      | <span data-ttu-id="18fdb-115">模式的長度。</span><span class="sxs-lookup"><span data-stu-id="18fdb-115">The length of the pattern.</span></span>                                                                                                                                                                                                                                                                                                      |
| <span data-ttu-id="18fdb-116">模式</span><span class="sxs-lookup"><span data-stu-id="18fdb-116">Pattern</span></span>     | <span data-ttu-id="18fdb-117">構成模式的實際位。</span><span class="sxs-lookup"><span data-stu-id="18fdb-117">The actual bits that make up the pattern.</span></span> <span data-ttu-id="18fdb-118">這些是在探索期間針對影像檔案中的識別模式比對的位。</span><span class="sxs-lookup"><span data-stu-id="18fdb-118">These are the bits that are matched against the identifying pattern in an image file during discovery.</span></span>                                                                                                                                                                                |
| <span data-ttu-id="18fdb-119">Mask</span><span class="sxs-lookup"><span data-stu-id="18fdb-119">Mask</span></span>        | <span data-ttu-id="18fdb-120">在模式中允許萬用字元值。</span><span class="sxs-lookup"><span data-stu-id="18fdb-120">Allows for wildcard values in patterns.</span></span> <span data-ttu-id="18fdb-121">遮罩的套用方式是在模式和遮罩上執行邏輯 AND 運算。</span><span class="sxs-lookup"><span data-stu-id="18fdb-121">The mask is applied by performing a logical AND operation on the pattern and the mask.</span></span> <span data-ttu-id="18fdb-122">在模式中，對應至遮罩中位（值為0）的任何位都會被忽略。</span><span class="sxs-lookup"><span data-stu-id="18fdb-122">Any bit in the pattern that corresponds to a bit in the mask with a value of 0 is ignored.</span></span>                                                                                                       |
| <span data-ttu-id="18fdb-123">EndOfStream</span><span class="sxs-lookup"><span data-stu-id="18fdb-123">EndOfStream</span></span> | <span data-ttu-id="18fdb-124">識別模式的位移應從資料流程的結尾，而不是從開頭算起。</span><span class="sxs-lookup"><span data-stu-id="18fdb-124">The offset of the identifying pattern should be calculated from the end of the stream, rather than the beginning.</span></span> <span data-ttu-id="18fdb-125">某些影像格式會將識別模式放在檔案結尾或附近。</span><span class="sxs-lookup"><span data-stu-id="18fdb-125">Some image formats place the identifying pattern at or near the end of the file.</span></span> <span data-ttu-id="18fdb-126">由於預設是從開頭開始搜尋，除非您的模式接近檔案結尾，否則您可以省略此專案。</span><span class="sxs-lookup"><span data-stu-id="18fdb-126">Because the default is to seek from the beginning, unless your pattern is near the end of the file, you can omit this entry.</span></span> |



 

<span data-ttu-id="18fdb-127">編解碼器可支援一個以上的識別模式。</span><span class="sxs-lookup"><span data-stu-id="18fdb-127">A codec can support more than one identifying pattern.</span></span> <span data-ttu-id="18fdb-128">在這種情況下，您會在 **HKEY \_ 類別的 \_ 根 \\ CLSID \\ {解碼器 clsid} \\ 模式** 下重複所有的金鑰，並在範例) 中使用 (0 的數位鍵來區別不同的模式。</span><span class="sxs-lookup"><span data-stu-id="18fdb-128">In that case, you would repeat all of the keys under **HKEY\_CLASSES\_ROOT\\CLSID\\{Decoder CLSID}\\Patterns**, and use the numerical key (0 in the example) to distinguish between the different patterns.</span></span> <span data-ttu-id="18fdb-129">您必須在每個模式的索引鍵下包含四個值。</span><span class="sxs-lookup"><span data-stu-id="18fdb-129">You must include each of the four values under the key for each pattern.</span></span>

## <a name="registering-a-container-format-with-metadata-readers"></a><span data-ttu-id="18fdb-130">使用中繼資料讀取器註冊容器格式</span><span class="sxs-lookup"><span data-stu-id="18fdb-130">Registering a Container Format with Metadata Readers</span></span>

<span data-ttu-id="18fdb-131">如果您為編解碼器建立新的容器格式，您也必須建立登錄專案，以支援針對影像中的中繼資料區塊探索中繼資料讀取器，就像您針對中繼資料寫入器所做的一樣。</span><span class="sxs-lookup"><span data-stu-id="18fdb-131">If you create a new container format for your codec, you must also create registry entries to support discovery of metadata readers for the metadata blocks in your images, just as you did for the metadata writers.</span></span> <span data-ttu-id="18fdb-132">您必須根據容器格式所支援的每個元資料格式，在中繼資料讀取器 (CLSID) 的類別識別碼底下建立下列專案。</span><span class="sxs-lookup"><span data-stu-id="18fdb-132">The following entries need to be created under the class identifier (CLSID) of the metadata reader for each metadata format your container format supports.</span></span> <span data-ttu-id="18fdb-133"> (請注意，如果您的編解碼器使用標記的影像檔案格式 (TIFF) 容器，則這項資訊已在登錄中。 ) </span><span class="sxs-lookup"><span data-stu-id="18fdb-133">(Note that, if your codec uses a Tagged Image File Format (TIFF) container, then this information is already in the registry.)</span></span>

```
HKEY_CLASSES_ROOT
   CLSID
      {Metadata Reader CLSID}
         Containers
            {Container Format GUID}
               
                  Position = Offset relative to its container
                  Pattern = Pattern used for metadata header
                  Mask = FF FF FF FF
                  DataOffset = Offset from beginning of header
```

<span data-ttu-id="18fdb-134">因為中繼資料讀取器的專案也用來進行探索，所以它們非常類似于「解碼器」的專案。</span><span class="sxs-lookup"><span data-stu-id="18fdb-134">Because the entries for metadata readers are also used for discovery, they are very similar to the entries for decoders.</span></span> <span data-ttu-id="18fdb-135">元件 factory 會使用這些專案來尋找您的容器所支援的中繼資料讀取器，並在您的 [**IWICMetadataBlockReader**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatablockreader) 執行要求中繼資料讀取器時，選取適當的專案。</span><span class="sxs-lookup"><span data-stu-id="18fdb-135">These entries are used by the component factory to find the metadata readers supported by your container, and to select the appropriate one, when your [**IWICMetadataBlockReader**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatablockreader) implementation requests a metadata reader.</span></span>



| <span data-ttu-id="18fdb-136">值</span><span class="sxs-lookup"><span data-stu-id="18fdb-136">Value</span></span>      | <span data-ttu-id="18fdb-137">描述</span><span class="sxs-lookup"><span data-stu-id="18fdb-137">Description</span></span>                                                                                                                                                                                                                                                                 |
|------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="18fdb-138">位置</span><span class="sxs-lookup"><span data-stu-id="18fdb-138">Position</span></span>   | <span data-ttu-id="18fdb-139">中繼資料區塊容器中可以找到中繼資料標頭的位移。</span><span class="sxs-lookup"><span data-stu-id="18fdb-139">The offset in the metadata block’s container where the metadata header can be found.</span></span> <span data-ttu-id="18fdb-140">針對最上層的中繼資料區塊，這是檔案資料流程中的位移。</span><span class="sxs-lookup"><span data-stu-id="18fdb-140">For top-level metadata blocks, this is the offset in the file stream.</span></span> <span data-ttu-id="18fdb-141">針對其他中繼資料區塊中嵌套的中繼資料區塊，它是相對於包含中繼資料區塊的位移。</span><span class="sxs-lookup"><span data-stu-id="18fdb-141">For metadata blocks nested in other metadata blocks, it is the offset relative to the containing metadata block.</span></span> |
| <span data-ttu-id="18fdb-142">模式</span><span class="sxs-lookup"><span data-stu-id="18fdb-142">Pattern</span></span>    | <span data-ttu-id="18fdb-143">構成模式的實際位。</span><span class="sxs-lookup"><span data-stu-id="18fdb-143">The actual bits that make up the pattern.</span></span> <span data-ttu-id="18fdb-144">這些是在探索期間針對影像檔案中的識別模式比對的位。</span><span class="sxs-lookup"><span data-stu-id="18fdb-144">These are the bits that are matched against the identifying pattern in an image file during discovery.</span></span>                                                                                                                            |
| <span data-ttu-id="18fdb-145">Mask</span><span class="sxs-lookup"><span data-stu-id="18fdb-145">Mask</span></span>       | <span data-ttu-id="18fdb-146">中繼資料標頭通常是由元資料處理程式所定義。</span><span class="sxs-lookup"><span data-stu-id="18fdb-146">The metadata header is generally defined by the metadata handler.</span></span> <span data-ttu-id="18fdb-147">您應該針對每個讀取器使用標準中繼資料標頭，除非基於某些原因，此模式在您的容器中必須有不同的格式。</span><span class="sxs-lookup"><span data-stu-id="18fdb-147">You should use the standard metadata header for each reader unless, for some reason, the pattern must have a different format in your container.</span></span>                                                          |
| <span data-ttu-id="18fdb-148">DataOffset</span><span class="sxs-lookup"><span data-stu-id="18fdb-148">DataOffset</span></span> | <span data-ttu-id="18fdb-149">中繼資料標頭開頭的位移，實際的資料會從此處開始。</span><span class="sxs-lookup"><span data-stu-id="18fdb-149">The offset from the beginning of the metadata header at which the actual data begins.</span></span> <span data-ttu-id="18fdb-150">如果中繼資料不是位於標頭的特定位移，則可以省略此專案。</span><span class="sxs-lookup"><span data-stu-id="18fdb-150">In cases where the metadata isn’t located at a specific offset from the header, this entry can be omitted.</span></span>                                                                            |



 

## <a name="related-topics"></a><span data-ttu-id="18fdb-151">相關主題</span><span class="sxs-lookup"><span data-stu-id="18fdb-151">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="18fdb-152">**概念**</span><span class="sxs-lookup"><span data-stu-id="18fdb-152">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="18fdb-153">編碼器特定的登錄專案</span><span class="sxs-lookup"><span data-stu-id="18fdb-153">Encoder-Specific Registry Entries</span></span>](-wic-encoderregentries.md)
</dt> <dt>

[<span data-ttu-id="18fdb-154">與 Windows 影像中心和 Windows 檔案總管整合</span><span class="sxs-lookup"><span data-stu-id="18fdb-154">Integration with Windows Photo Gallery and Windows Explorer</span></span>](-wic-integrationregentries.md)
</dt> <dt>

[<span data-ttu-id="18fdb-155">如何撰寫 WIC-Enabled 編解碼器</span><span class="sxs-lookup"><span data-stu-id="18fdb-155">How to Write a WIC-Enabled CODEC</span></span>](-wic-howtowriteacodec.md)
</dt> <dt>

[<span data-ttu-id="18fdb-156">Windows 影像處理元件總覽</span><span class="sxs-lookup"><span data-stu-id="18fdb-156">Windows Imaging Component Overview</span></span>](-wic-about-windows-imaging-codec.md)
</dt> </dl>

 

 



