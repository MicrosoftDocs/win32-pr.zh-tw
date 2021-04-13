---
title: 中繼資料功能
description: 中繼資料會在 ASF 檔案中用來描述檔案內容和屬性。
ms.assetid: 01ba09d7-11be-46b1-a0f2-4e35ca5502a8
keywords:
- Windows Media Format SDK，中繼資料功能
- Windows Media Format SDK，功能
- Advanced Systems Format (ASF) ，中繼資料功能
- ASF (Advanced Systems Format) ，中繼資料功能
- Advanced Systems Format (ASF) ，功能
- ASF (Advanced Systems Format) ，功能
- 中繼資料，功能
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 80ea31885a1c1635ee4778683858876572e32262
ms.sourcegitcommit: ad672d3a10192c5ccac619ad2524407109266e93
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 05/25/2020
ms.locfileid: "104374801"
---
# <a name="metadata-features"></a><span data-ttu-id="33b57-110">中繼資料功能</span><span class="sxs-lookup"><span data-stu-id="33b57-110">Metadata Features</span></span>

<span data-ttu-id="33b57-111">中繼資料會在 ASF 檔案中用來描述檔案內容和屬性。</span><span class="sxs-lookup"><span data-stu-id="33b57-111">Metadata is used in ASF files to describe file contents and properties.</span></span> <span data-ttu-id="33b57-112">您建立的所有 ASF 檔案都應該包含適當的中繼資料。</span><span class="sxs-lookup"><span data-stu-id="33b57-112">All ASF files you create should include appropriate metadata.</span></span> <span data-ttu-id="33b57-113"> (如需總覽，請參閱 [中繼資料](metadata.md)。 ) Windows MEDIA 格式 SDK 支援透過寫入器物件、中繼資料編輯器物件，以及讀取器和同步讀取器物件來編輯中繼資料。</span><span class="sxs-lookup"><span data-stu-id="33b57-113">(For an overview, see [Metadata](metadata.md).) The Windows Media Format SDK includes support for metadata editing through the writer object, the metadata editor object, and both the reader and synchronous reader objects.</span></span> <span data-ttu-id="33b57-114">包含各種中繼資料屬性的原生支援。</span><span class="sxs-lookup"><span data-stu-id="33b57-114">Native support for a wide variety of metadata attributes is included.</span></span> <span data-ttu-id="33b57-115">如需預先定義的屬性清單，請參閱 [屬性](attributes.md) 。</span><span class="sxs-lookup"><span data-stu-id="33b57-115">See [Attributes](attributes.md) for a list of the predefined attributes.</span></span>

<span data-ttu-id="33b57-116">Windows Media Format SDK 的各種物件所提供的中繼資料支援有彈性且功能強大。</span><span class="sxs-lookup"><span data-stu-id="33b57-116">The metadata support provided by the various objects of the Windows Media Format SDK is flexible and powerful.</span></span> <span data-ttu-id="33b57-117">下列清單摘要說明主要的中繼資料功能：</span><span class="sxs-lookup"><span data-stu-id="33b57-117">The main metadata features are summarized in the following list:</span></span>

-   <span data-ttu-id="33b57-118">彈性的屬性大小。</span><span class="sxs-lookup"><span data-stu-id="33b57-118">Flexible attribute size.</span></span> <span data-ttu-id="33b57-119">中繼資料屬性的大小不限。</span><span class="sxs-lookup"><span data-stu-id="33b57-119">Metadata attributes are not limited in size.</span></span>
-   <span data-ttu-id="33b57-120">資料流程層級屬性。</span><span class="sxs-lookup"><span data-stu-id="33b57-120">Stream-level attributes.</span></span> <span data-ttu-id="33b57-121">ASF 檔案中的中繼資料可以指派給整個檔案，或指派給特定的資料流程。</span><span class="sxs-lookup"><span data-stu-id="33b57-121">Metadata in ASF files can be assigned to the file as a whole, or to a particular stream.</span></span>
-   <span data-ttu-id="33b57-122">重複的屬性。</span><span class="sxs-lookup"><span data-stu-id="33b57-122">Duplicated attributes.</span></span> <span data-ttu-id="33b57-123">您可以在相同的檔案中多次使用命名屬性。</span><span class="sxs-lookup"><span data-stu-id="33b57-123">A named attribute can be used multiple times in the same file.</span></span> <span data-ttu-id="33b57-124">這項功能在指派內容描述性屬性時特別使用。</span><span class="sxs-lookup"><span data-stu-id="33b57-124">This feature is of particular use when assigning content descriptive attributes.</span></span> <span data-ttu-id="33b57-125">例如，某首歌可能會有多位作者，而每位作者在檔案中都需要個別的 **Author** 屬性。</span><span class="sxs-lookup"><span data-stu-id="33b57-125">For example, a song may have several authors, each requiring a separate **Author** attribute in the file.</span></span>
-   <span data-ttu-id="33b57-126">多種語言。</span><span class="sxs-lookup"><span data-stu-id="33b57-126">Multiple languages.</span></span> <span data-ttu-id="33b57-127">每個屬性都有相關聯的語言。</span><span class="sxs-lookup"><span data-stu-id="33b57-127">Every attribute has a language associated with it.</span></span> <span data-ttu-id="33b57-128">您可以設定支援的語言，然後將它指派給您所撰寫的每個屬性。</span><span class="sxs-lookup"><span data-stu-id="33b57-128">You can set the supported languages and then assign one to each attribute you write.</span></span> <span data-ttu-id="33b57-129">由於您可以複製屬性，因此您可以使用數種語言提供最重要的屬性來觸及較大的物件。</span><span class="sxs-lookup"><span data-stu-id="33b57-129">Because you can duplicate attributes, you can provide the most important attributes in several languages to reach a larger audience.</span></span> <span data-ttu-id="33b57-130">如果您未指定語言，則會使用從執行應用程式之電腦的作業系統取得的預設語言 () 。</span><span class="sxs-lookup"><span data-stu-id="33b57-130">If you do not specify a language, the default language (obtained from the operating system of the computer running your application) will be used.</span></span>
-   <span data-ttu-id="33b57-131">複雜屬性。</span><span class="sxs-lookup"><span data-stu-id="33b57-131">Complex attributes.</span></span> <span data-ttu-id="33b57-132">某些預先定義的屬性支援結構化資料。</span><span class="sxs-lookup"><span data-stu-id="33b57-132">Some of the predefined attributes support structured data.</span></span> <span data-ttu-id="33b57-133">針對這些屬性，資料類型為 binary，但值為此 SDK 中定義的結構。</span><span class="sxs-lookup"><span data-stu-id="33b57-133">For these attributes, the data type is binary, but the value is a structure defined in this SDK.</span></span>

<span data-ttu-id="33b57-134">下列主題將討論其他支援的中繼資料功能。</span><span class="sxs-lookup"><span data-stu-id="33b57-134">The following topics discuss the other supported metadata features.</span></span>



| <span data-ttu-id="33b57-135">主題</span><span class="sxs-lookup"><span data-stu-id="33b57-135">Topic</span></span>                                  | <span data-ttu-id="33b57-136">描述</span><span class="sxs-lookup"><span data-stu-id="33b57-136">Description</span></span>                                                                             |
|----------------------------------------|-----------------------------------------------------------------------------------------|
| [<span data-ttu-id="33b57-137">ID3 支援</span><span class="sxs-lookup"><span data-stu-id="33b57-137">ID3 Support</span></span>](id3.md)                 | <span data-ttu-id="33b57-138">討論如何使用 Windows Media Format SDK 的物件來支援 ID3 框架。</span><span class="sxs-lookup"><span data-stu-id="33b57-138">Discusses the support for ID3 frames using the objects of the Windows Media Format SDK.</span></span> |
| [<span data-ttu-id="33b57-139">自訂中繼資料</span><span class="sxs-lookup"><span data-stu-id="33b57-139">Custom Metadata</span></span>](custom-metadata.md) | <span data-ttu-id="33b57-140">討論使用自訂中繼資料的含意。</span><span class="sxs-lookup"><span data-stu-id="33b57-140">Discusses the implications of using custom metadata.</span></span>                                    |



 

## <a name="related-topics"></a><span data-ttu-id="33b57-141">相關主題</span><span class="sxs-lookup"><span data-stu-id="33b57-141">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="33b57-142">**功能**</span><span class="sxs-lookup"><span data-stu-id="33b57-142">**Features**</span></span>](features.md)
</dt> <dt>

[<span data-ttu-id="33b57-143">**IWMHeaderInfo 介面**</span><span class="sxs-lookup"><span data-stu-id="33b57-143">**IWMHeaderInfo Interface**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmheaderinfo)
</dt> <dt>

[<span data-ttu-id="33b57-144">**IWMHeaderInfo2 介面**</span><span class="sxs-lookup"><span data-stu-id="33b57-144">**IWMHeaderInfo2 Interface**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmheaderinfo2)
</dt> <dt>

[<span data-ttu-id="33b57-145">**IWMHeaderInfo3 介面**</span><span class="sxs-lookup"><span data-stu-id="33b57-145">**IWMHeaderInfo3 Interface**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmheaderinfo3)
</dt> <dt>

[<span data-ttu-id="33b57-146">**中繼資料**</span><span class="sxs-lookup"><span data-stu-id="33b57-146">**Metadata**</span></span>](metadata.md)
</dt> </dl>

 

 




