---
title: " (Windows Media Format 11 SDK) 的屬性"
description: 深入瞭解 Windows Media Format 11 SDK 中的屬性。 屬性是中繼資料的個別專案。
ms.assetid: 1e9392b4-4fff-41ad-9d80-23c1c7f9e9a4
keywords:
- Windows Media Format SDK，屬性
- Advanced Systems Format (ASF) 、屬性
- ASF (Advanced 系統格式) ，屬性
- 屬性，關於
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 23738e20df2c6360b20b7c3da005cde6b3942d44
ms.sourcegitcommit: d0eb44d0a95f5e5efbfec3d3e9c143f5cba25bc3
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 06/17/2021
ms.locfileid: "112262190"
---
# <a name="attributes-windows-media-format-11-sdk"></a><span data-ttu-id="0ffd9-108"> (Windows Media Format 11 SDK) 的屬性</span><span class="sxs-lookup"><span data-stu-id="0ffd9-108">Attributes (Windows Media Format 11 SDK)</span></span>

<span data-ttu-id="0ffd9-109">屬性是中繼資料的個別專案。</span><span class="sxs-lookup"><span data-stu-id="0ffd9-109">An attribute is an individual item of metadata.</span></span> <span data-ttu-id="0ffd9-110">大部分的屬性都可以由您的應用程式設定，並寫入至 ASF 檔案的標頭。</span><span class="sxs-lookup"><span data-stu-id="0ffd9-110">Most of the attributes can be set by your application and are written to the header of an ASF file.</span></span>

<span data-ttu-id="0ffd9-111">某些預先定義的屬性是編碼屬性。</span><span class="sxs-lookup"><span data-stu-id="0ffd9-111">Some of the predefined attributes are coded attributes.</span></span> <span data-ttu-id="0ffd9-112">這些屬性不會儲存在 ASF 檔案的標頭中，而是在載入檔案時由 Windows Media Format SDK 的物件所計算。</span><span class="sxs-lookup"><span data-stu-id="0ffd9-112">These attributes are not stored in the header of an ASF file, but are computed by the objects of the Windows Media Format SDK when the file is loaded.</span></span> <span data-ttu-id="0ffd9-113">因為程式碼屬性一律會進行計算，所以它們本質上是唯讀的。</span><span class="sxs-lookup"><span data-stu-id="0ffd9-113">Because coded attributes are always computed, they are inherently read-only.</span></span>

<span data-ttu-id="0ffd9-114">此 SDK 包含許多您可以使用的屬性定義。</span><span class="sxs-lookup"><span data-stu-id="0ffd9-114">This SDK includes many attribute definitions that you can use.</span></span> <span data-ttu-id="0ffd9-115">您也可以建立自己的屬性來描述內容。</span><span class="sxs-lookup"><span data-stu-id="0ffd9-115">You can also create attributes of your own to describe content.</span></span>

<span data-ttu-id="0ffd9-116">下列各節說明預先定義的屬性。</span><span class="sxs-lookup"><span data-stu-id="0ffd9-116">The following sections describe the predefined attributes.</span></span>



| <span data-ttu-id="0ffd9-117">區段</span><span class="sxs-lookup"><span data-stu-id="0ffd9-117">Section</span></span>                                                                | <span data-ttu-id="0ffd9-118">描述</span><span class="sxs-lookup"><span data-stu-id="0ffd9-118">Description</span></span>                                                                                                                                                                                           |
|------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="0ffd9-119">屬性清單</span><span class="sxs-lookup"><span data-stu-id="0ffd9-119">Attribute List</span></span>](attribute-list.md)                                   | <span data-ttu-id="0ffd9-120">提供所有預先定義之屬性的字母順序清單。</span><span class="sxs-lookup"><span data-stu-id="0ffd9-120">Provides an alphabetical list of all of the predefined attributes.</span></span> <span data-ttu-id="0ffd9-121">在清單之後，每個屬性都會個別描述。</span><span class="sxs-lookup"><span data-stu-id="0ffd9-121">After the list, each attribute is described individually.</span></span>                                                                          |
| [<span data-ttu-id="0ffd9-122">具有多個值的屬性</span><span class="sxs-lookup"><span data-stu-id="0ffd9-122">Attributes with Multiple Values</span></span>](attributes-with-multiple-values.md) | <span data-ttu-id="0ffd9-123">列出可以新增至檔案一次以上的屬性。</span><span class="sxs-lookup"><span data-stu-id="0ffd9-123">Lists the attributes that can be added to a file more than once.</span></span>                                                                                                                                      |
| [<span data-ttu-id="0ffd9-124">依類型的屬性</span><span class="sxs-lookup"><span data-stu-id="0ffd9-124">Attributes By Type</span></span>](attributes-by-type.md)                           | <span data-ttu-id="0ffd9-125">包含依類型排序的屬性清單。</span><span class="sxs-lookup"><span data-stu-id="0ffd9-125">Contains lists of attributes sorted by type.</span></span> <span data-ttu-id="0ffd9-126">這些屬性包括特殊用途的屬性清單 (例如處理數位版權管理) 的屬性，以及依內容類型的建議屬性清單。</span><span class="sxs-lookup"><span data-stu-id="0ffd9-126">These include lists of special-purpose attributes (like those dealing with digital rights management) and lists of suggested attributes by content type.</span></span> |
| [<span data-ttu-id="0ffd9-127">ID3 標記支援</span><span class="sxs-lookup"><span data-stu-id="0ffd9-127">ID3 Tag Support</span></span>](id3-tag-support.md)                                 | <span data-ttu-id="0ffd9-128">列出與 ID3 標記相容的屬性。</span><span class="sxs-lookup"><span data-stu-id="0ffd9-128">Lists the attributes that are compatible with ID3 tags.</span></span>                                                                                                                                               |



 

## <a name="related-topics"></a><span data-ttu-id="0ffd9-129">相關主題</span><span class="sxs-lookup"><span data-stu-id="0ffd9-129">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0ffd9-130">**IWMHeaderInfo::GetAttributeByIndex**</span><span class="sxs-lookup"><span data-stu-id="0ffd9-130">**IWMHeaderInfo::GetAttributeByIndex**</span></span>](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmheaderinfo-getattributebyindex)
</dt> <dt>

[<span data-ttu-id="0ffd9-131">**IWMHeaderInfo::GetAttributeByName**</span><span class="sxs-lookup"><span data-stu-id="0ffd9-131">**IWMHeaderInfo::GetAttributeByName**</span></span>](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmheaderinfo-getattributebyname)
</dt> <dt>

[<span data-ttu-id="0ffd9-132">**IWMHeaderInfo：： SetAttribute**</span><span class="sxs-lookup"><span data-stu-id="0ffd9-132">**IWMHeaderInfo::SetAttribute**</span></span>](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmheaderinfo-setattribute)
</dt> <dt>

[<span data-ttu-id="0ffd9-133">**使用中繼資料**</span><span class="sxs-lookup"><span data-stu-id="0ffd9-133">**Working with Metadata**</span></span>](working-with-metadata.md)
</dt> </dl>

 

 




