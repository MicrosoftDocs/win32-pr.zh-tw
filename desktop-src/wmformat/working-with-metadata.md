---
title: 使用中繼資料
description: 使用中繼資料
ms.assetid: 15d835c2-e227-4e69-a8b2-9b1c6d671022
keywords:
- Windows Media Format SDK，中繼資料總覽
- Advanced Systems Format (ASF) ，中繼資料總覽
- ASF (Advanced Systems Format) ，中繼資料總覽
- 中繼資料，關於
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 050336d18947059373ddccf3f18e5d4295834293
ms.sourcegitcommit: ad672d3a10192c5ccac619ad2524407109266e93
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 05/25/2020
ms.locfileid: "104374817"
---
# <a name="working-with-metadata"></a><span data-ttu-id="d224d-107">使用中繼資料</span><span class="sxs-lookup"><span data-stu-id="d224d-107">Working with Metadata</span></span>

<span data-ttu-id="d224d-108">中繼資料支援是由寫入器物件、讀取器和同步讀取器物件，以及中繼資料編輯器物件提供。</span><span class="sxs-lookup"><span data-stu-id="d224d-108">Metadata support is provided by the writer object, the reader and synchronous reader objects, and the metadata editor object.</span></span> <span data-ttu-id="d224d-109">如需中繼資料的一般資訊，請參閱 [中繼資料](metadata.md)。</span><span class="sxs-lookup"><span data-stu-id="d224d-109">For general information about metadata, see [Metadata](metadata.md).</span></span> <span data-ttu-id="d224d-110">如需有關在 Windows Media 格式 SDK 中支援中繼資料之功能的詳細資訊，請參閱 [中繼資料功能](metadata-features.md)。</span><span class="sxs-lookup"><span data-stu-id="d224d-110">For information about the features supporting metadata in the Windows Media Format SDK, see [Metadata Features](metadata-features.md).</span></span>

<span data-ttu-id="d224d-111">中繼資料編輯的介面是 [**IWMHeaderInfo3**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmheaderinfo3)，您可以藉由呼叫上述其中一個物件中任何介面的 **QueryInterface** 方法來取得該介面。</span><span class="sxs-lookup"><span data-stu-id="d224d-111">The interface for metadata editing is [**IWMHeaderInfo3**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmheaderinfo3), which you can obtain by calling the **QueryInterface** method of any interface in one of the objects listed above.</span></span> <span data-ttu-id="d224d-112">**IWMHeaderInfo3** 會繼承 [**IWMHeaderInfo**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmheaderinfo) 和 [**IWMHeaderInfo2**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmheaderinfo2)的方法。</span><span class="sxs-lookup"><span data-stu-id="d224d-112">**IWMHeaderInfo3** inherits the methods of [**IWMHeaderInfo**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmheaderinfo) and [**IWMHeaderInfo2**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmheaderinfo2).</span></span> <span data-ttu-id="d224d-113">處理中繼資料屬性的 **IWMHeaderInfo3** 方法代表存取中繼資料的不同方法，而不是 **IWMHeaderInfo** 方法所使用的方法。</span><span class="sxs-lookup"><span data-stu-id="d224d-113">The methods of **IWMHeaderInfo3** that deal with metadata attributes represent a different approach to accessing metadata than that used by the methods of **IWMHeaderInfo**.</span></span> <span data-ttu-id="d224d-114">您應該一律使用較新的方法。</span><span class="sxs-lookup"><span data-stu-id="d224d-114">You should always use the newer methods.</span></span>

<span data-ttu-id="d224d-115">ASF 檔案中的中繼資料是由索引和資料流程號碼來識別。</span><span class="sxs-lookup"><span data-stu-id="d224d-115">Metadata in an ASF file is identified by an index and a stream number.</span></span> <span data-ttu-id="d224d-116">檔案層級屬性會指派為0的資料流程編號。</span><span class="sxs-lookup"><span data-stu-id="d224d-116">File-level attributes are assigned a stream number of 0.</span></span> <span data-ttu-id="d224d-117">在舊版的 Windows Media Format SDK 中，可以依名稱來識別屬性。</span><span class="sxs-lookup"><span data-stu-id="d224d-117">In previous versions of the Windows Media Format SDK, attributes could be identified by name.</span></span> <span data-ttu-id="d224d-118">不過，因為您現在可以在資料流程中複製屬性名稱，所以無法再使用。</span><span class="sxs-lookup"><span data-stu-id="d224d-118">However, because you can now duplicate attribute names within a stream, this is no longer possible.</span></span> <span data-ttu-id="d224d-119">相反地，您可以取出所有符合名稱的索引。</span><span class="sxs-lookup"><span data-stu-id="d224d-119">Instead, you can retrieve all the indexes matching a name.</span></span> <span data-ttu-id="d224d-120">如需詳細資訊，請參閱 [取出中繼資料屬性](retrieving-metadata-attributes.md)。</span><span class="sxs-lookup"><span data-stu-id="d224d-120">For more information, see [Retrieving Metadata Attributes](retrieving-metadata-attributes.md).</span></span>

<span data-ttu-id="d224d-121">為了協助快速尋找屬性，您可以使用特殊的串流號碼0xFFFF。</span><span class="sxs-lookup"><span data-stu-id="d224d-121">To aid in finding attributes quickly, you can use a special stream number, 0xFFFF.</span></span> <span data-ttu-id="d224d-122">您可以使用此資料流程號碼來識別整個檔案，而不是特定的資料流程或檔案層級的屬性。</span><span class="sxs-lookup"><span data-stu-id="d224d-122">Use this stream number to identify the file as a whole, rather than a specific stream or the file-level attributes.</span></span> <span data-ttu-id="d224d-123">Windows Media Format SDK 的物件會針對每個資料流程和檔案層級屬性維護不同的索引。</span><span class="sxs-lookup"><span data-stu-id="d224d-123">The objects of the Windows Media Format SDK maintain separate indexes for each stream and for the file-level attributes.</span></span> <span data-ttu-id="d224d-124">使用 stream 0xFFFF 時，索引與您指定特定資料流程時所用的索引不同。</span><span class="sxs-lookup"><span data-stu-id="d224d-124">When using stream 0xFFFF, the indexes are different from those you use when specifying a specific stream.</span></span> <span data-ttu-id="d224d-125">例如，資料流程0的索引0屬性不會與 stream 0xFFFF 的索引0屬性相同。</span><span class="sxs-lookup"><span data-stu-id="d224d-125">For example, the attribute that is index 0 for stream 0 will not be the same as the attribute that is index 0 for stream 0xFFFF.</span></span>

<span data-ttu-id="d224d-126">下列各節會更詳細地說明中繼資料的使用方式。</span><span class="sxs-lookup"><span data-stu-id="d224d-126">The following sections describe the use of metadata in greater detail.</span></span>



| <span data-ttu-id="d224d-127">區段</span><span class="sxs-lookup"><span data-stu-id="d224d-127">Section</span></span>                                                                    | <span data-ttu-id="d224d-128">描述</span><span class="sxs-lookup"><span data-stu-id="d224d-128">Description</span></span>                                                                       |
|----------------------------------------------------------------------------|-----------------------------------------------------------------------------------|
| [<span data-ttu-id="d224d-129">正在抓取中繼資料屬性</span><span class="sxs-lookup"><span data-stu-id="d224d-129">Retrieving Metadata Attributes</span></span>](retrieving-metadata-attributes.md)       | <span data-ttu-id="d224d-130">說明如何從檔案標頭讀取中繼資料屬性。</span><span class="sxs-lookup"><span data-stu-id="d224d-130">Describes how to read metadata attributes from a file header.</span></span>                     |
| [<span data-ttu-id="d224d-131">設定中繼資料屬性</span><span class="sxs-lookup"><span data-stu-id="d224d-131">Setting Metadata Attributes</span></span>](setting-metadata-attributes.md)             | <span data-ttu-id="d224d-132">說明如何將新的中繼資料屬性加入至檔案標頭。</span><span class="sxs-lookup"><span data-stu-id="d224d-132">Describes how to add new metadata attributes to a file header.</span></span>                    |
| [<span data-ttu-id="d224d-133">編輯中繼資料屬性</span><span class="sxs-lookup"><span data-stu-id="d224d-133">Editing Metadata Attributes</span></span>](editing-metadata-attributes.md)             | <span data-ttu-id="d224d-134">描述如何編輯現有的中繼資料屬性。</span><span class="sxs-lookup"><span data-stu-id="d224d-134">Describes how to edit existing metadata attributes.</span></span>                               |
| [<span data-ttu-id="d224d-135">移除中繼資料屬性</span><span class="sxs-lookup"><span data-stu-id="d224d-135">Removing Metadata Attributes</span></span>](removing-metadata-attributes.md)           | <span data-ttu-id="d224d-136">描述如何移除現有的中繼資料屬性。</span><span class="sxs-lookup"><span data-stu-id="d224d-136">Describes how to remove existing metadata attributes.</span></span>                             |
| [<span data-ttu-id="d224d-137">使用複雜的中繼資料屬性</span><span class="sxs-lookup"><span data-stu-id="d224d-137">Using Complex Metadata Attributes</span></span>](using-complex-metadata-attributes.md) | <span data-ttu-id="d224d-138">描述如何使用其值以結構表示的屬性。</span><span class="sxs-lookup"><span data-stu-id="d224d-138">Describes how to work with attributes whose values are represented by structures.</span></span> |



 

<span data-ttu-id="d224d-139">數個範例應用程式會示範如何取出和編輯中繼資料。</span><span class="sxs-lookup"><span data-stu-id="d224d-139">Several of the sample applications show how to retrieve and edit metadata.</span></span> <span data-ttu-id="d224d-140">尤其是，請參閱 MetadataEdit 範例，這會同時隨附于 c + + 和 c # 版本。</span><span class="sxs-lookup"><span data-stu-id="d224d-140">In particular, see the MetadataEdit sample, which comes in both C++ and C# versions.</span></span>

## <a name="related-topics"></a><span data-ttu-id="d224d-141">相關主題</span><span class="sxs-lookup"><span data-stu-id="d224d-141">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d224d-142">**屬性**</span><span class="sxs-lookup"><span data-stu-id="d224d-142">**Attributes**</span></span>](attributes.md)
</dt> <dt>

[<span data-ttu-id="d224d-143">**程式設計指南**</span><span class="sxs-lookup"><span data-stu-id="d224d-143">**Programming Guide**</span></span>](programming-guide.md)
</dt> <dt>

[<span data-ttu-id="d224d-144">**範例應用程式**</span><span class="sxs-lookup"><span data-stu-id="d224d-144">**Sample Applications**</span></span>](sample-applications.md)
</dt> </dl>

 

 




