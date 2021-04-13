---
title: 存取應用程式中的中繼資料和屬性
description: 取得及設定應用程式中的中繼資料和屬性
ms.assetid: 308a722d-1c65-41eb-a0e2-21171eb410d5
keywords:
- Windows Media 裝置管理員，中繼資料
- 裝置管理員，中繼資料
- 程式設計指南，中繼資料
- 桌面應用程式，中繼資料
- 建立 Windows Media 裝置管理員應用程式，中繼資料
- 中繼資料
- Windows Media 裝置管理員，屬性
- 裝置管理員，屬性
- 程式設計指南，屬性
- 桌面應用程式，屬性
- 建立 Windows Media 裝置管理員應用程式，屬性
- 屬性
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6a78dbb31ebcc5ec99b1db3503b386b09b5a3c05
ms.sourcegitcommit: b95a94ffffda33f9ebbdd41787c01866444b4cf4
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 11/27/2019
ms.locfileid: "104313851"
---
# <a name="accessing-metadata-and-attributes-in-the-app"></a><span data-ttu-id="ba410-115">存取應用程式中的中繼資料和屬性</span><span class="sxs-lookup"><span data-stu-id="ba410-115">Accessing metadata and attributes in the app</span></span>

<span data-ttu-id="ba410-116">中繼資料和屬性的一般討論可以 [取得和設定中繼資料和屬性](getting-and-setting-metadata-and-attributes.md)。</span><span class="sxs-lookup"><span data-stu-id="ba410-116">A general discussion of metadata and attributes is available in [Getting and Setting Metadata and Attributes](getting-and-setting-metadata-and-attributes.md).</span></span> <span data-ttu-id="ba410-117">本章節涵蓋取得或設定值的特定應用程式方法呼叫。</span><span class="sxs-lookup"><span data-stu-id="ba410-117">This section covers specific application method calls to retrieve or set values.</span></span>

<span data-ttu-id="ba410-118">應用程式可以藉由呼叫 [**IWMDMStorage：： GetAttributes**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstorage-getattributes)、 [**IWMDMStorage2：： GetAttributes2**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstorage2-getattributes2)、 [**IWMDMStorage3：： GetMetadata**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstorage3-getmetadata) 或 [**IWMDMStorage4：： GetSpecifiedMetadata**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstorage4-getspecifiedmetadata)，來取得特定儲存體的屬性或中繼資料。</span><span class="sxs-lookup"><span data-stu-id="ba410-118">Applications can retrieve attributes or metadata about a specific storage by calling [**IWMDMStorage::GetAttributes**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstorage-getattributes), [**IWMDMStorage2::GetAttributes2**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstorage2-getattributes2), [**IWMDMStorage3::GetMetadata**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstorage3-getmetadata) or [**IWMDMStorage4::GetSpecifiedMetadata**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstorage4-getspecifiedmetadata).</span></span> <span data-ttu-id="ba410-119">**GetMetadata** 會抓取所有與儲存體相關聯之中繼資料的完整集合，然後應用程式可以列舉所有值或要求集合中的特定值。</span><span class="sxs-lookup"><span data-stu-id="ba410-119">**GetMetadata** retrieves a full collection of all the metadata associated with a storage, and the application can then enumerate through all values or request specific values from the collection.</span></span> <span data-ttu-id="ba410-120">**GetSpecifiedMetadata** 會代表呼叫者建立中繼資料物件。</span><span class="sxs-lookup"><span data-stu-id="ba410-120">**GetSpecifiedMetadata** creates a metadata object on behalf of the caller.</span></span> <span data-ttu-id="ba410-121">呼叫端可能會藉由在 *ppwszPropNames* 參數中填入所需 Windows Media 裝置管理員屬性字串的陣列，以及該陣列的計數，來要求可用資料的子集。</span><span class="sxs-lookup"><span data-stu-id="ba410-121">The caller may request a subset of the available data by filling in the *ppwszPropNames* parameter with an array of the desired Windows Media Device Manager property strings, and the count of that array.</span></span> <span data-ttu-id="ba410-122">傳回的中繼資料物件將會填入可抓取的屬性。</span><span class="sxs-lookup"><span data-stu-id="ba410-122">The returned metadata object will be filled with those properties that could be retrieved.</span></span> <span data-ttu-id="ba410-123">無法取出的屬性將不存在。</span><span class="sxs-lookup"><span data-stu-id="ba410-123">Those properties that couldn't be retrieved will be absent.</span></span> <span data-ttu-id="ba410-124">中繼資料會以最佳方式傳回。</span><span class="sxs-lookup"><span data-stu-id="ba410-124">Metadata is returned on a best-effort basis.</span></span>

<span data-ttu-id="ba410-125">裝置可以藉由呼叫 [**IWMDMStorage：： SetAttributes**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstorage-setattributes)、 [**IWMDMStorage2：： SetAttributes2**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstorage2-setattributes2)或 [**IWMDMStorage3：： >setmetadata**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstorage3-setmetadata)來設定儲存體上的屬性或中繼資料。</span><span class="sxs-lookup"><span data-stu-id="ba410-125">A device can set attributes or metadata on a storage by calling [**IWMDMStorage::SetAttributes**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstorage-setattributes), [**IWMDMStorage2::SetAttributes2**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstorage2-setattributes2), or [**IWMDMStorage3::SetMetadata**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstorage3-setmetadata).</span></span> <span data-ttu-id="ba410-126">請注意，不保證任何設定的值都會保存，因為它們可能儲存在非持續性的外部檔案存放區中、可能不支援這些值，或是裝置可能不支援將屬性支援為可寫入。</span><span class="sxs-lookup"><span data-stu-id="ba410-126">Note that there is no guarantee that any values set will persist, because they may be stored in a non-persistent external file store, the values may not be supported, or, the device may not support the properties as writeable.</span></span>

<span data-ttu-id="ba410-127">您也可以藉由呼叫 [**IWMDMDevice3：： GetProperty**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmdevice3-getproperty) 或 [**IWMDMDevice3：： SetProperty**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmdevice3-setproperty)來取得或設定裝置的相關中繼資料。</span><span class="sxs-lookup"><span data-stu-id="ba410-127">You can also get or set metadata about a device by calling [**IWMDMDevice3::GetProperty**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmdevice3-getproperty) or [**IWMDMDevice3::SetProperty**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmdevice3-setproperty).</span></span> <span data-ttu-id="ba410-128">[中繼資料常數](metadata-constants.md)的結尾會列出不同的裝置中繼資料常數表格。</span><span class="sxs-lookup"><span data-stu-id="ba410-128">There is a separate table of device metadata constants listed at the end of [Metadata Constants](metadata-constants.md).</span></span>

<span data-ttu-id="ba410-129">每個方法的參考檔中都會提供使用這些方法的範例。</span><span class="sxs-lookup"><span data-stu-id="ba410-129">Examples of using these methods are given in each method's reference documentation.</span></span>

## <a name="related-topics"></a><span data-ttu-id="ba410-130">相關主題</span><span class="sxs-lookup"><span data-stu-id="ba410-130">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ba410-131">**建立 Windows Media 裝置管理員應用程式**</span><span class="sxs-lookup"><span data-stu-id="ba410-131">**Creating a Windows Media Device Manager Application**</span></span>](creating-a-windows-media-device-manager-application.md)
</dt> <dt>

[<span data-ttu-id="ba410-132">**取得和設定中繼資料和屬性**</span><span class="sxs-lookup"><span data-stu-id="ba410-132">**Getting and Setting Metadata and Attributes**</span></span>](getting-and-setting-metadata-and-attributes.md)
</dt> </dl>

 

 




