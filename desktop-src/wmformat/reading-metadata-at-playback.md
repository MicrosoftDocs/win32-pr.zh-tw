---
title: 在播放時讀取中繼資料
description: 在播放時讀取中繼資料
ms.assetid: 48d37a9e-5e22-4298-abc4-b69998906dcb
keywords:
- Windows Media Format SDK，讀取中繼資料
- Windows Media Format SDK，非同步讀取器
- Windows Media Format SDK，同步讀取器
- Advanced Systems Format (ASF) ，讀取中繼資料
- ASF (Advanced Systems Format) ，讀取中繼資料
- Advanced Systems Format (ASF) 、非同步讀取器
- ASF (Advanced 系統格式) 、非同步讀取器
- Advanced Systems Format (ASF) 、同步讀取器
- ASF (Advanced Systems Format) ，同步讀取器
- 非同步讀取器，讀取中繼資料
- 同步讀取器，讀取中繼資料
- 中繼資料，在播放時讀取
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 42a2515dd62092d02a45b0261fe2b501e0833a31
ms.sourcegitcommit: ad672d3a10192c5ccac619ad2524407109266e93
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 05/25/2020
ms.locfileid: "104023158"
---
# <a name="reading-metadata-at-playback"></a><span data-ttu-id="82835-115">在播放時讀取中繼資料</span><span class="sxs-lookup"><span data-stu-id="82835-115">Reading Metadata at Playback</span></span>

<span data-ttu-id="82835-116">非同步讀取器物件和同步讀取器物件都可以從已載入之 ASF 檔案的標頭讀取中繼資料。</span><span class="sxs-lookup"><span data-stu-id="82835-116">Both the asynchronous reader object and the synchronous reader object can read the metadata from the header of a loaded ASF file.</span></span> <span data-ttu-id="82835-117">讀取檔案時，中繼資料屬性都是唯讀的。</span><span class="sxs-lookup"><span data-stu-id="82835-117">When reading files, the metadata attributes are all read-only.</span></span> <span data-ttu-id="82835-118">這兩個讀取器物件都可以針對 [**IWMHeaderInfo**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmheaderinfo) 和 [**IWMHeaderInfo2**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmheaderinfo2) 介面進行查詢。</span><span class="sxs-lookup"><span data-stu-id="82835-118">Both reader objects can be queried for the [**IWMHeaderInfo**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmheaderinfo) and [**IWMHeaderInfo2**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmheaderinfo2) interfaces.</span></span>

<span data-ttu-id="82835-119">如需存取中繼資料的詳細資訊，請參閱 [使用中繼資料](working-with-metadata.md)。</span><span class="sxs-lookup"><span data-stu-id="82835-119">For more information about accessing metadata, see [Working with Metadata](working-with-metadata.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="82835-120">相關主題</span><span class="sxs-lookup"><span data-stu-id="82835-120">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="82835-121">**讀取 ASF 檔案**</span><span class="sxs-lookup"><span data-stu-id="82835-121">**Reading ASF Files**</span></span>](reading-asf-files.md)
</dt> </dl>

 

 




