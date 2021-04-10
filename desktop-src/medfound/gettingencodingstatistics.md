---
description: 描述您可以從 Windows Media 編解碼器取出的統計資料。
ms.assetid: 86c029af-e0fb-436a-b758-3f7d10c8bdeb
title: '取得編碼統計資料 (Microsoft 媒體基礎) '
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 92fb298b35e9cd4114d1a5ba2f5badfad36c09c7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103689287"
---
# <a name="getting-encoding-statistics-microsoft-media-foundation"></a><span data-ttu-id="ba03a-103">取得編碼統計資料 (Microsoft 媒體基礎) </span><span class="sxs-lookup"><span data-stu-id="ba03a-103">Getting Encoding Statistics (Microsoft Media Foundation)</span></span>

<span data-ttu-id="ba03a-104">編碼會話中發生之情況的相關資訊，通常會立即以處理範例時傳回的錯誤碼形式提供。</span><span class="sxs-lookup"><span data-stu-id="ba03a-104">Information about what is happening in an encoding session is generally immediately available in the form of error codes returned when processing samples.</span></span> <span data-ttu-id="ba03a-105">不過，您可以從編解碼器取得有關各種編碼方面的統計資料。</span><span class="sxs-lookup"><span data-stu-id="ba03a-105">However, there are some statistics that you can retrieve from the codec about various encoding aspects.</span></span>

## <a name="video-frame-information"></a><span data-ttu-id="ba03a-106">影片畫面資訊</span><span class="sxs-lookup"><span data-stu-id="ba03a-106">Video Frame Information</span></span>

<span data-ttu-id="ba03a-107">您可以取出的部分影片統計資料會處理編碼器所處理的畫面格數。</span><span class="sxs-lookup"><span data-stu-id="ba03a-107">Some video statistics that you can retrieve deal with the number of frames processed by the encoder.</span></span> <span data-ttu-id="ba03a-108">您可以從影片編碼器讀取三個框架編號屬性：</span><span class="sxs-lookup"><span data-stu-id="ba03a-108">There are three frame number properties that you can read from the video encoder:</span></span>

-   <span data-ttu-id="ba03a-109">[MFPKEY \_TOTALFRAMES](mfpkey-totalframesproperty.md) 是透過輸入資料流程處理的框架數。</span><span class="sxs-lookup"><span data-stu-id="ba03a-109">[MFPKEY\_TOTALFRAMES](mfpkey-totalframesproperty.md) is the number of frames processed through the input stream of the DMO.</span></span>
-   <span data-ttu-id="ba03a-110">[MFPKEY \_CODEDFRAMES](mfpkey-codedframesproperty.md) 是已編碼的框架數目。</span><span class="sxs-lookup"><span data-stu-id="ba03a-110">[MFPKEY\_CODEDFRAMES](mfpkey-codedframesproperty.md) is the number of frames encoded.</span></span> <span data-ttu-id="ba03a-111">藉由從傳遞的框架總數減去此值，您可以判斷已卸載的框架數。</span><span class="sxs-lookup"><span data-stu-id="ba03a-111">By subtracting this value from the total number of frames passed, you can determine how many frames were dropped.</span></span>
-   <span data-ttu-id="ba03a-112">[MFPKEY \_ZEROBYTEFRAMES](mfpkey-zerobyteframesproperty.md) 是未編碼的框架數目，因為它們已包含重複的內容。</span><span class="sxs-lookup"><span data-stu-id="ba03a-112">[MFPKEY\_ZEROBYTEFRAMES](mfpkey-zerobyteframesproperty.md) is the number of frames not encoded because they duplicated content already included.</span></span> <span data-ttu-id="ba03a-113">此值不會從 < i 部所報告的編碼框架數目減去。</span><span class="sxs-lookup"><span data-stu-id="ba03a-113">This value is not subtracted from the number of coded frames reported by the DMO.</span></span>

<span data-ttu-id="ba03a-114">在編碼期間，您可以隨時讀取影片畫面的屬性。</span><span class="sxs-lookup"><span data-stu-id="ba03a-114">You can read video frame properties at any time during encoding.</span></span> <span data-ttu-id="ba03a-115">這有助於判斷編碼設定是否適用于您的內容;如果總畫面格和程式碼框架之間有很大的差異，則壓縮的內容可能不符合您的品質需求。</span><span class="sxs-lookup"><span data-stu-id="ba03a-115">This can be useful in determining if the encoding settings are appropriate for your content; if there is a large difference between total frames and coded frames, the compressed content might not meet your quality requirements.</span></span> <span data-ttu-id="ba03a-116">完成編碼之後，您可以讀取最終的值。</span><span class="sxs-lookup"><span data-stu-id="ba03a-116">You can read the final values after you finish encoding.</span></span>

## <a name="vbr-buffer-statistics"></a><span data-ttu-id="ba03a-117">VBR 緩衝區統計資料</span><span class="sxs-lookup"><span data-stu-id="ba03a-117">VBR Buffer Statistics</span></span>

<span data-ttu-id="ba03a-118">根據所使用的編碼模式而定，部分或全部的緩衝區設定可能會在編碼期間決定 (例如，在將內容編碼) 之前，不知道以品質為基礎之 VBR 的位元速率。</span><span class="sxs-lookup"><span data-stu-id="ba03a-118">Depending upon the encoding mode used, some or all of the buffer settings may be determined during encoding (for example, the bit rate of quality based VBR is not known until the content is encoded).</span></span> <span data-ttu-id="ba03a-119">您可以使用 **IPropertyBag：： Read** 方法取得四個 VBR 緩衝區屬性：</span><span class="sxs-lookup"><span data-stu-id="ba03a-119">There are four VBR buffer properties that you can get using the **IPropertyBag::Read** method:</span></span>

-   <span data-ttu-id="ba03a-120">[MFPKEY \_RAVG](mfpkey-ravgproperty.md) 是 VBR 內容的平均位元速率。</span><span class="sxs-lookup"><span data-stu-id="ba03a-120">[MFPKEY\_RAVG](mfpkey-ravgproperty.md) is the average bit rate of the VBR content.</span></span>
-   <span data-ttu-id="ba03a-121">[MFPKEY \_BAVG](mfpkey-bavgproperty.md) 是平均位元速率的緩衝區視窗。</span><span class="sxs-lookup"><span data-stu-id="ba03a-121">[MFPKEY\_BAVG](mfpkey-bavgproperty.md) is the buffer window for the average bit rate.</span></span>
-   <span data-ttu-id="ba03a-122">[MFPKEY \_RMAX](mfpkey-rmaxproperty.md) 是 VBR 內容的尖峰位元速率。</span><span class="sxs-lookup"><span data-stu-id="ba03a-122">[MFPKEY\_RMAX](mfpkey-rmaxproperty.md) is the peak bit rate of the VBR content.</span></span>
-   <span data-ttu-id="ba03a-123">[MFPKEY \_BMAX](mfpkey-bmaxproperty.md) 是尖峰緩衝區視窗。</span><span class="sxs-lookup"><span data-stu-id="ba03a-123">[MFPKEY\_BMAX](mfpkey-bmaxproperty.md) is the peak buffer window.</span></span>

<span data-ttu-id="ba03a-124">開始處理範例之後，除非您已完成串流的編碼，否則不應讀取任何 VBR 屬性。</span><span class="sxs-lookup"><span data-stu-id="ba03a-124">After you begin processing samples, you should not read any of the VBR properties until you are finished encoding the stream.</span></span> <span data-ttu-id="ba03a-125">如果您這樣做，編碼器會將您的要求視為編碼完成的信號來解讀。</span><span class="sxs-lookup"><span data-stu-id="ba03a-125">If you do, the encoder interprets your request as a signal that the encoding is complete.</span></span> <span data-ttu-id="ba03a-126">您處理的下一個範例會被視為新的編碼會話。</span><span class="sxs-lookup"><span data-stu-id="ba03a-126">The next sample that you process is treated as a new encoding session.</span></span>

## <a name="related-topics"></a><span data-ttu-id="ba03a-127">相關主題</span><span class="sxs-lookup"><span data-stu-id="ba03a-127">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ba03a-128">Windows Media 轉碼器</span><span class="sxs-lookup"><span data-stu-id="ba03a-128">Windows Media Codecs</span></span>](windows-media-codecs.md)
</dt> </dl>

 

 



