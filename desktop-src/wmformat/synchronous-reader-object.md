---
title: 同步讀取器物件
description: 同步讀取器物件
ms.assetid: 52a4891f-03bf-4d8a-ab7b-e9739db30bc3
keywords:
- Windows Media Format SDK，同步讀取器物件
- Advanced Systems Format (ASF) ，同步讀取器物件
- ASF (Advanced Systems Format) ，同步讀取器物件
- 物件、同步讀取器物件
- 同步讀取器，物件
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 491fed915a049dbfc52acc24d06a0344d8e3109c
ms.sourcegitcommit: ad672d3a10192c5ccac619ad2524407109266e93
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 05/25/2020
ms.locfileid: "106969094"
---
# <a name="synchronous-reader-object"></a><span data-ttu-id="df86d-108">同步讀取器物件</span><span class="sxs-lookup"><span data-stu-id="df86d-108">Synchronous Reader Object</span></span>

<span data-ttu-id="df86d-109">同步讀取器物件是用來讀取使用同步呼叫的數位媒體檔案。</span><span class="sxs-lookup"><span data-stu-id="df86d-109">The synchronous reader object is used to read digital media files by using synchronous calls.</span></span>

<span data-ttu-id="df86d-110">同步讀取器物件是由函式 [**WMCreateSyncReader**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreatesyncreader)所建立，它會將指標設定為 **IWMSyncReader** 介面。</span><span class="sxs-lookup"><span data-stu-id="df86d-110">The synchronous reader object is created by the function [**WMCreateSyncReader**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreatesyncreader), which sets a pointer to an **IWMSyncReader** interface.</span></span> <span data-ttu-id="df86d-111">同步讀取器介面所支援的其他介面可以藉由呼叫 **QueryInterface** 方法來取得。</span><span class="sxs-lookup"><span data-stu-id="df86d-111">The other interfaces supported by the synchronous reader interface can be obtained by calling the **QueryInterface** method.</span></span>

<span data-ttu-id="df86d-112">同步讀取器物件支援下列介面。</span><span class="sxs-lookup"><span data-stu-id="df86d-112">The following interfaces are supported by the synchronous reader object.</span></span>



| <span data-ttu-id="df86d-113">介面</span><span class="sxs-lookup"><span data-stu-id="df86d-113">Interface</span></span>                                | <span data-ttu-id="df86d-114">描述</span><span class="sxs-lookup"><span data-stu-id="df86d-114">Description</span></span>                                                                                                                                                        |
|------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="df86d-115">**IWMHeaderInfo**</span><span class="sxs-lookup"><span data-stu-id="df86d-115">**IWMHeaderInfo**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmheaderinfo)   | <span data-ttu-id="df86d-116">設定和抓取標頭資訊，例如中繼資料、 [*標記*](wmformat-glossary.md)等等。</span><span class="sxs-lookup"><span data-stu-id="df86d-116">Sets and retrieves header information, such as metadata, [*markers*](wmformat-glossary.md), and so on.</span></span>                                            |
| [<span data-ttu-id="df86d-117">**IWMHeaderInfo2**</span><span class="sxs-lookup"><span data-stu-id="df86d-117">**IWMHeaderInfo2**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmheaderinfo2) | <span data-ttu-id="df86d-118">列舉可用的編解碼器資訊。</span><span class="sxs-lookup"><span data-stu-id="df86d-118">Enumerates the available codec information.</span></span> <span data-ttu-id="df86d-119">繼承 **IWMHeaderInfo** 的所有方法。</span><span class="sxs-lookup"><span data-stu-id="df86d-119">Inherits all of the methods of **IWMHeaderInfo**.</span></span>                                                                      |
| [<span data-ttu-id="df86d-120">**IWMHeaderInfo3**</span><span class="sxs-lookup"><span data-stu-id="df86d-120">**IWMHeaderInfo3**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmheaderinfo3) | <span data-ttu-id="df86d-121">支援大型屬性大小、重複的屬性名稱，以及多語言支援。</span><span class="sxs-lookup"><span data-stu-id="df86d-121">Supports large attribute sizes, duplicate attribute names, and multiple language support.</span></span> <span data-ttu-id="df86d-122">繼承 **IWMHeaderInfo** 和 **IWMHeaderInfo2** 的所有方法。</span><span class="sxs-lookup"><span data-stu-id="df86d-122">Inherits all of the methods of **IWMHeaderInfo** and **IWMHeaderInfo2**.</span></span> |
| [<span data-ttu-id="df86d-123">**IWMProfile**</span><span class="sxs-lookup"><span data-stu-id="df86d-123">**IWMProfile**</span></span>](iwmprofile.md)         | <span data-ttu-id="df86d-124">提供對載入至讀取器之 Windows Media 檔案的設定檔資訊的存取。</span><span class="sxs-lookup"><span data-stu-id="df86d-124">Provides access to the profile information of the Windows Media file loaded into the reader.</span></span>                                                                       |
| [<span data-ttu-id="df86d-125">**IWMProfile2**</span><span class="sxs-lookup"><span data-stu-id="df86d-125">**IWMProfile2**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmprofile2)       | <span data-ttu-id="df86d-126">抓取與設定檔相關聯 (GUID) 的全域唯一識別碼（如果有的話）。</span><span class="sxs-lookup"><span data-stu-id="df86d-126">Retrieves the globally unique identifier (GUID), if any, associated with the profile.</span></span> <span data-ttu-id="df86d-127">繼承 **IWMProfile** 的所有方法。</span><span class="sxs-lookup"><span data-stu-id="df86d-127">Inherits all of the methods of **IWMProfile**.</span></span>                               |
| [<span data-ttu-id="df86d-128">**IWMProfile3**</span><span class="sxs-lookup"><span data-stu-id="df86d-128">**IWMProfile3**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmprofile3)       | <span data-ttu-id="df86d-129">支援設定檔中的頻寬共用和串流優先順序資訊。</span><span class="sxs-lookup"><span data-stu-id="df86d-129">Supports bandwidth sharing and stream prioritization information in the profile.</span></span> <span data-ttu-id="df86d-130">繼承 **IWMProfile** 和 **IWMProfile2** 的所有方法。</span><span class="sxs-lookup"><span data-stu-id="df86d-130">Inherits all of the methods of **IWMProfile** and **IWMProfile2**.</span></span>                |
| [<span data-ttu-id="df86d-131">**IWMSyncReader**</span><span class="sxs-lookup"><span data-stu-id="df86d-131">**IWMSyncReader**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmsyncreader)   | <span data-ttu-id="df86d-132">提供數位媒體檔案的同步讀取功能。</span><span class="sxs-lookup"><span data-stu-id="df86d-132">Provides synchronous reading capabilities for digital media files.</span></span>                                                                                                 |
| [<span data-ttu-id="df86d-133">**IWMSyncReader2**</span><span class="sxs-lookup"><span data-stu-id="df86d-133">**IWMSyncReader2**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmsyncreader2) | <span data-ttu-id="df86d-134">提供搜尋至 SMPTE 時間碼以及手動設定樣本的支援。</span><span class="sxs-lookup"><span data-stu-id="df86d-134">Provides support for seeking to SMPTE time codes and for allocating samples manually.</span></span> <span data-ttu-id="df86d-135">繼承 **IWMSyncReader** 的所有方法。</span><span class="sxs-lookup"><span data-stu-id="df86d-135">Inherits all of the methods of **IWMSyncReader**.</span></span>                            |



 

## <a name="related-topics"></a><span data-ttu-id="df86d-136">相關主題</span><span class="sxs-lookup"><span data-stu-id="df86d-136">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="df86d-137">**物件**</span><span class="sxs-lookup"><span data-stu-id="df86d-137">**Objects**</span></span>](objects.md)
</dt> <dt>

[<span data-ttu-id="df86d-138">**讀取器物件**</span><span class="sxs-lookup"><span data-stu-id="df86d-138">**Reader Object**</span></span>](reader-object.md)
</dt> <dt>

[<span data-ttu-id="df86d-139">**使用同步讀取器讀取檔案**</span><span class="sxs-lookup"><span data-stu-id="df86d-139">**Reading Files with the Synchronous Reader**</span></span>](reading-files-with-the-synchronous-reader.md)
</dt> </dl>

 

 




