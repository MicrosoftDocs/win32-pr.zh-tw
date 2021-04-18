---
title: 影片輸入格式
description: 影片輸入格式
ms.assetid: 0f1ec15d-328e-4c07-bf58-fd4ecb483549
keywords:
- Windows Media Format SDK、影片輸入格式
- Advanced Systems Format (ASF) 、影片輸入格式
- ASF (Advanced 系統格式) 、影片輸入格式
- 影片輸入格式
- Windows Media Format SDK、影片格式
- Advanced Systems Format (ASF) 、影片格式
- ASF (Advanced Systems Format) 、影片格式
- 影片格式
- Windows Media 視訊9編解碼器、影片輸入格式
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3c5113ee3cbd9c9235104f858968db20ebc29e3a
ms.sourcegitcommit: ad672d3a10192c5ccac619ad2524407109266e93
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 05/25/2020
ms.locfileid: "106965224"
---
# <a name="video-input-formats"></a><span data-ttu-id="ee531-112">影片輸入格式</span><span class="sxs-lookup"><span data-stu-id="ee531-112">Video Input Formats</span></span>

<span data-ttu-id="ee531-113">寫入器接受下列影片格式，做為使用 Windows Media 視訊9編解碼器壓縮的輸入：</span><span class="sxs-lookup"><span data-stu-id="ee531-113">The writer accepts the following video formats as input to be compressed using the Windows Media Video 9 codec:</span></span>

-   <span data-ttu-id="ee531-114">WMMEDIASUBTYPE \_ IYUV</span><span class="sxs-lookup"><span data-stu-id="ee531-114">WMMEDIASUBTYPE\_IYUV</span></span>
-   <span data-ttu-id="ee531-115">WMMEDIASUBTYPE \_ I420</span><span class="sxs-lookup"><span data-stu-id="ee531-115">WMMEDIASUBTYPE\_I420</span></span>
-   <span data-ttu-id="ee531-116">WMMEDIASUBTYPE \_ YV12</span><span class="sxs-lookup"><span data-stu-id="ee531-116">WMMEDIASUBTYPE\_YV12</span></span>
-   <span data-ttu-id="ee531-117">WMMEDIASUBTYPE \_ YUY2</span><span class="sxs-lookup"><span data-stu-id="ee531-117">WMMEDIASUBTYPE\_YUY2</span></span>
-   <span data-ttu-id="ee531-118">WMMEDIASUBTYPE \_ UYVY</span><span class="sxs-lookup"><span data-stu-id="ee531-118">WMMEDIASUBTYPE\_UYVY</span></span>
-   <span data-ttu-id="ee531-119">WMMEDIASUBTYPE \_ YVYU</span><span class="sxs-lookup"><span data-stu-id="ee531-119">WMMEDIASUBTYPE\_YVYU</span></span>
-   <span data-ttu-id="ee531-120">WMMEDIASUBTYPE \_ YVU9</span><span class="sxs-lookup"><span data-stu-id="ee531-120">WMMEDIASUBTYPE\_YVU9</span></span>
-   <span data-ttu-id="ee531-121">WMMEDIASUBTYPE \_ RGB32</span><span class="sxs-lookup"><span data-stu-id="ee531-121">WMMEDIASUBTYPE\_RGB32</span></span>
-   <span data-ttu-id="ee531-122">WMMEDIASUBTYPE \_ RGB24</span><span class="sxs-lookup"><span data-stu-id="ee531-122">WMMEDIASUBTYPE\_RGB24</span></span>
-   <span data-ttu-id="ee531-123">WMMEDIASUBTYPE \_ RGB565</span><span class="sxs-lookup"><span data-stu-id="ee531-123">WMMEDIASUBTYPE\_RGB565</span></span>
-   <span data-ttu-id="ee531-124">WMMEDIASUBTYPE \_ RGB555</span><span class="sxs-lookup"><span data-stu-id="ee531-124">WMMEDIASUBTYPE\_RGB555</span></span>
-   <span data-ttu-id="ee531-125">WMMEDIASUBTYPE \_ RGB8</span><span class="sxs-lookup"><span data-stu-id="ee531-125">WMMEDIASUBTYPE\_RGB8</span></span>

<span data-ttu-id="ee531-126">您應該一律使用 [**IWMWriter：： GetInputFormatCount**](/previous-versions/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmwriter-getinputformatcount) 和 [**IWMWriter：： GetInputFormat**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-getinputformat) 來列舉可用的輸入格式，並取得所需格式的輸入媒體屬性物件。</span><span class="sxs-lookup"><span data-stu-id="ee531-126">You should always use [**IWMWriter::GetInputFormatCount**](/previous-versions/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmwriter-getinputformatcount) and [**IWMWriter::GetInputFormat**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-getinputformat) to enumerate the available input formats and to obtain the input media properties object for the desired format.</span></span> <span data-ttu-id="ee531-127">您必須變更影片輸入媒體屬性物件，以反映輸入媒體的框架大小和畫面播放速率。</span><span class="sxs-lookup"><span data-stu-id="ee531-127">Video input media properties objects must be changed to reflect the frame size and frame rate of your input media.</span></span>

## <a name="related-topics"></a><span data-ttu-id="ee531-128">相關主題</span><span class="sxs-lookup"><span data-stu-id="ee531-128">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ee531-129">**媒體類型識別碼**</span><span class="sxs-lookup"><span data-stu-id="ee531-129">**Media Type Identifiers**</span></span>](media-type-identifiers.md)
</dt> <dt>

[<span data-ttu-id="ee531-130">**媒體類型**</span><span class="sxs-lookup"><span data-stu-id="ee531-130">**Media Types**</span></span>](media-types.md)
</dt> </dl>

 

 




