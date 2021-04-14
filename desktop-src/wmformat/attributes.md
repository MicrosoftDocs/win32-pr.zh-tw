---
title: " (Windows Media Format 11 SDK) 的屬性"
description: 屬性
ms.assetid: 1e9392b4-4fff-41ad-9d80-23c1c7f9e9a4
keywords:
- Windows Media Format SDK，屬性
- Advanced Systems Format (ASF) 、屬性
- ASF (Advanced 系統格式) ，屬性
- 屬性，關於
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c209558ed4803fee96e9b482302af1864cbf988b
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/10/2020
ms.locfileid: "104383686"
---
# <a name="attributes-windows-media-format-11-sdk"></a><span data-ttu-id="b531e-107"> (Windows Media Format 11 SDK) 的屬性</span><span class="sxs-lookup"><span data-stu-id="b531e-107">Attributes (Windows Media Format 11 SDK)</span></span>

<span data-ttu-id="b531e-108">屬性是中繼資料的個別專案。</span><span class="sxs-lookup"><span data-stu-id="b531e-108">An attribute is an individual item of metadata.</span></span> <span data-ttu-id="b531e-109">大部分的屬性都可以由您的應用程式設定，並寫入至 ASF 檔案的標頭。</span><span class="sxs-lookup"><span data-stu-id="b531e-109">Most of the attributes can be set by your application and are written to the header of an ASF file.</span></span>

<span data-ttu-id="b531e-110">某些預先定義的屬性是編碼屬性。</span><span class="sxs-lookup"><span data-stu-id="b531e-110">Some of the predefined attributes are coded attributes.</span></span> <span data-ttu-id="b531e-111">這些屬性不會儲存在 ASF 檔案的標頭中，而是在載入檔案時由 Windows Media Format SDK 的物件所計算。</span><span class="sxs-lookup"><span data-stu-id="b531e-111">These attributes are not stored in the header of an ASF file, but are computed by the objects of the Windows Media Format SDK when the file is loaded.</span></span> <span data-ttu-id="b531e-112">因為程式碼屬性一律會進行計算，所以它們本質上是唯讀的。</span><span class="sxs-lookup"><span data-stu-id="b531e-112">Because coded attributes are always computed, they are inherently read-only.</span></span>

<span data-ttu-id="b531e-113">此 SDK 包含許多您可以使用的屬性定義。</span><span class="sxs-lookup"><span data-stu-id="b531e-113">This SDK includes many attribute definitions that you can use.</span></span> <span data-ttu-id="b531e-114">您也可以建立自己的屬性來描述內容。</span><span class="sxs-lookup"><span data-stu-id="b531e-114">You can also create attributes of your own to describe content.</span></span>

<span data-ttu-id="b531e-115">下列各節說明預先定義的屬性。</span><span class="sxs-lookup"><span data-stu-id="b531e-115">The following sections describe the predefined attributes.</span></span>



| <span data-ttu-id="b531e-116">區段</span><span class="sxs-lookup"><span data-stu-id="b531e-116">Section</span></span>                                                                | <span data-ttu-id="b531e-117">描述</span><span class="sxs-lookup"><span data-stu-id="b531e-117">Description</span></span>                                                                                                                                                                                           |
|------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="b531e-118">屬性清單</span><span class="sxs-lookup"><span data-stu-id="b531e-118">Attribute List</span></span>](attribute-list.md)                                   | <span data-ttu-id="b531e-119">提供所有預先定義之屬性的字母順序清單。</span><span class="sxs-lookup"><span data-stu-id="b531e-119">Provides an alphabetical list of all of the predefined attributes.</span></span> <span data-ttu-id="b531e-120">在清單之後，每個屬性都會個別描述。</span><span class="sxs-lookup"><span data-stu-id="b531e-120">After the list, each attribute is described individually.</span></span>                                                                          |
| [<span data-ttu-id="b531e-121">具有多個值的屬性</span><span class="sxs-lookup"><span data-stu-id="b531e-121">Attributes with Multiple Values</span></span>](attributes-with-multiple-values.md) | <span data-ttu-id="b531e-122">列出可以新增至檔案一次以上的屬性。</span><span class="sxs-lookup"><span data-stu-id="b531e-122">Lists the attributes that can be added to a file more than once.</span></span>                                                                                                                                      |
| [<span data-ttu-id="b531e-123">依類型的屬性</span><span class="sxs-lookup"><span data-stu-id="b531e-123">Attributes By Type</span></span>](attributes-by-type.md)                           | <span data-ttu-id="b531e-124">包含依類型排序的屬性清單。</span><span class="sxs-lookup"><span data-stu-id="b531e-124">Contains lists of attributes sorted by type.</span></span> <span data-ttu-id="b531e-125">這些屬性包括特殊用途的屬性清單 (例如處理數位版權管理) 的屬性，以及依內容類型的建議屬性清單。</span><span class="sxs-lookup"><span data-stu-id="b531e-125">These include lists of special-purpose attributes (like those dealing with digital rights management) and lists of suggested attributes by content type.</span></span> |
| [<span data-ttu-id="b531e-126">ID3 標記支援</span><span class="sxs-lookup"><span data-stu-id="b531e-126">ID3 Tag Support</span></span>](id3-tag-support.md)                                 | <span data-ttu-id="b531e-127">列出與 ID3 標記相容的屬性。</span><span class="sxs-lookup"><span data-stu-id="b531e-127">Lists the attributes that are compatible with ID3 tags.</span></span>                                                                                                                                               |



 

## <a name="related-topics"></a><span data-ttu-id="b531e-128">相關主題</span><span class="sxs-lookup"><span data-stu-id="b531e-128">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b531e-129">**IWMHeaderInfo::GetAttributeByIndex**</span><span class="sxs-lookup"><span data-stu-id="b531e-129">**IWMHeaderInfo::GetAttributeByIndex**</span></span>](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmheaderinfo-getattributebyindex)
</dt> <dt>

[<span data-ttu-id="b531e-130">**IWMHeaderInfo::GetAttributeByName**</span><span class="sxs-lookup"><span data-stu-id="b531e-130">**IWMHeaderInfo::GetAttributeByName**</span></span>](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmheaderinfo-getattributebyname)
</dt> <dt>

[<span data-ttu-id="b531e-131">**IWMHeaderInfo：： SetAttribute**</span><span class="sxs-lookup"><span data-stu-id="b531e-131">**IWMHeaderInfo::SetAttribute**</span></span>](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmheaderinfo-setattribute)
</dt> <dt>

[<span data-ttu-id="b531e-132">**使用中繼資料**</span><span class="sxs-lookup"><span data-stu-id="b531e-132">**Working with Metadata**</span></span>](working-with-metadata.md)
</dt> </dl>

 

 




