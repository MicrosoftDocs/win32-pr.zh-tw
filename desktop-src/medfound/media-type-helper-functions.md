---
description: 下列是媒體類型物件的相關函數。
ms.assetid: 7d4f3581-8cb9-4d31-b2f7-c8fbde24cf2a
title: 媒體類型 Helper 函式
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d7e5edb9748bad8ee16903eb9ff1ada50c1c043b
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/03/2021
ms.locfileid: "104514348"
---
# <a name="media-type-helper-functions"></a><span data-ttu-id="88b53-103">媒體類型 Helper 函式</span><span class="sxs-lookup"><span data-stu-id="88b53-103">Media Type Helper Functions</span></span>

<span data-ttu-id="88b53-104">下列是媒體類型物件的相關函數。</span><span class="sxs-lookup"><span data-stu-id="88b53-104">The following functions pertain to media type objects.</span></span>



| <span data-ttu-id="88b53-105">函式</span><span class="sxs-lookup"><span data-stu-id="88b53-105">Function</span></span>                                                                     | <span data-ttu-id="88b53-106">描述</span><span class="sxs-lookup"><span data-stu-id="88b53-106">Description</span></span>                                                           |
|------------------------------------------------------------------------------|-----------------------------------------------------------------------|
| [<span data-ttu-id="88b53-107">**MFAverageTimePerFrameToFrameRate**</span><span class="sxs-lookup"><span data-stu-id="88b53-107">**MFAverageTimePerFrameToFrameRate**</span></span>](/windows/desktop/api/mfapi/nf-mfapi-mfaveragetimeperframetoframerate) | <span data-ttu-id="88b53-108">計算影片框架平均持續時間的畫面播放速率。</span><span class="sxs-lookup"><span data-stu-id="88b53-108">Calculates the frame rate from the average duration of a video frame.</span></span> |
| [<span data-ttu-id="88b53-109">**MFCalculateImageSize**</span><span class="sxs-lookup"><span data-stu-id="88b53-109">**MFCalculateImageSize**</span></span>](/windows/desktop/api/mfapi/nf-mfapi-mfcalculateimagesize)                         | <span data-ttu-id="88b53-110">抓取未壓縮影片格式的影像大小。</span><span class="sxs-lookup"><span data-stu-id="88b53-110">Retrieves the image size for an uncompressed video format.</span></span>            |
| [<span data-ttu-id="88b53-111">**MFCompareFullToPartialMediaType**</span><span class="sxs-lookup"><span data-stu-id="88b53-111">**MFCompareFullToPartialMediaType**</span></span>](/windows/desktop/api/mfapi/nf-mfapi-mfcomparefulltopartialmediatype)   | <span data-ttu-id="88b53-112">將完整媒體類型與部分媒體類型進行比較。</span><span class="sxs-lookup"><span data-stu-id="88b53-112">Compares a full media type to a partial media type.</span></span>                   |
| [<span data-ttu-id="88b53-113">**MFCreateMediaType**</span><span class="sxs-lookup"><span data-stu-id="88b53-113">**MFCreateMediaType**</span></span>](/windows/desktop/api/mfapi/nf-mfapi-mfcreatemediatype)                               | <span data-ttu-id="88b53-114">建立空的媒體類型。</span><span class="sxs-lookup"><span data-stu-id="88b53-114">Creates an empty media type.</span></span>                                          |
| [<span data-ttu-id="88b53-115">**MFFrameRateToAverageTimePerFrame**</span><span class="sxs-lookup"><span data-stu-id="88b53-115">**MFFrameRateToAverageTimePerFrame**</span></span>](/windows/desktop/api/mfapi/nf-mfapi-mfframeratetoaveragetimeperframe) | <span data-ttu-id="88b53-116">將影片畫面播放速率轉換成框架持續時間。</span><span class="sxs-lookup"><span data-stu-id="88b53-116">Converts a video frame rate into a frame duration.</span></span>                    |
| [<span data-ttu-id="88b53-117">**MFGetStrideForBitmapInfoHeader**</span><span class="sxs-lookup"><span data-stu-id="88b53-117">**MFGetStrideForBitmapInfoHeader**</span></span>](/windows/desktop/api/mfapi/nf-mfapi-mfgetstrideforbitmapinfoheader)     | <span data-ttu-id="88b53-118">捕獲影片格式的最小表面 stride。</span><span class="sxs-lookup"><span data-stu-id="88b53-118">Retrieves the minimum surface stride for a video format.</span></span>              |
| [<span data-ttu-id="88b53-119">**MFIsFormatYUV**</span><span class="sxs-lookup"><span data-stu-id="88b53-119">**MFIsFormatYUV**</span></span>](/windows/desktop/api/mfapi/nf-mfapi-mfisformatyuv)                                       | <span data-ttu-id="88b53-120">查詢 FOURCC 碼或 **D3DFORMAT** 值是否為 YUV 格式。</span><span class="sxs-lookup"><span data-stu-id="88b53-120">Queries whether a FOURCC code or **D3DFORMAT** value is a YUV format.</span></span> |
| [<span data-ttu-id="88b53-121">**MFValidateMediaTypeSize**</span><span class="sxs-lookup"><span data-stu-id="88b53-121">**MFValidateMediaTypeSize**</span></span>](/windows/desktop/api/mfapi/nf-mfapi-mfvalidatemediatypesize)                   | <span data-ttu-id="88b53-122">驗證影片格式區塊的緩衝區大小。</span><span class="sxs-lookup"><span data-stu-id="88b53-122">Validates the size of a buffer for a video format block.</span></span>              |
| [<span data-ttu-id="88b53-123">**MFWrapMediaType**</span><span class="sxs-lookup"><span data-stu-id="88b53-123">**MFWrapMediaType**</span></span>](/windows/desktop/api/mfapi/nf-mfapi-mfwrapmediatype)                                   | <span data-ttu-id="88b53-124">建立包裝另一個媒體類型的媒體類型。</span><span class="sxs-lookup"><span data-stu-id="88b53-124">Creates a media type that wraps another media type.</span></span>                   |



 

## <a name="related-topics"></a><span data-ttu-id="88b53-125">相關主題</span><span class="sxs-lookup"><span data-stu-id="88b53-125">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="88b53-126">**IMFMediaType**</span><span class="sxs-lookup"><span data-stu-id="88b53-126">**IMFMediaType**</span></span>](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype)
</dt> <dt>

[<span data-ttu-id="88b53-127">媒體類型轉換</span><span class="sxs-lookup"><span data-stu-id="88b53-127">Media Type Conversions</span></span>](media-type-conversions.md)
</dt> <dt>

[<span data-ttu-id="88b53-128">媒體類型</span><span class="sxs-lookup"><span data-stu-id="88b53-128">Media Types</span></span>](media-types.md)
</dt> </dl>

 

 



