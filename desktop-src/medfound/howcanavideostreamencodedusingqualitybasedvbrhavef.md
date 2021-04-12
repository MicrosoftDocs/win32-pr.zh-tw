---
description: 使用以品質為基礎的 VBR 編碼的影片資料流程如何比原始串流更少的框架？
ms.assetid: acce9c88-2ee1-4628-9fd5-ccb441f8b43e
title: 使用以品質為基礎的 VBR 編碼的影片資料流程如何比原始串流更少的框架？
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ad2af2775882155ed7ef2b0cfffdddeb30b2066e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104192317"
---
# <a name="how-can-a-video-stream-encoded-using-quality-based-vbr-have-fewer-frames-than-the-original-stream"></a><span data-ttu-id="b134b-103">使用以品質為基礎的 VBR 編碼的影片資料流程如何比原始串流更少的框架？</span><span class="sxs-lookup"><span data-stu-id="b134b-103">How can a video stream encoded using quality-based VBR have fewer frames than the original stream?</span></span>

<span data-ttu-id="b134b-104">編碼資料流程的框架計數可以低於原始的框架計數，原因有兩種：重複的畫面格和已卸載的畫面格。</span><span class="sxs-lookup"><span data-stu-id="b134b-104">The frame count of an encoded stream can be lower than the frame count of the original for one of two reasons: duplicate frames and dropped frames.</span></span>

<span data-ttu-id="b134b-105">編碼器通常不會產生與前一個框架完全相同的畫面格。</span><span class="sxs-lookup"><span data-stu-id="b134b-105">The encoder does not normally produce frames that are exact duplicates of the previous frame.</span></span> <span data-ttu-id="b134b-106">如果您需要每個框架的範例 (這是某些容器所需的範例，例如) ，您可以將 [MFPKEY \_ PRODUCEDUMMYFRAMES](mfpkey-producedummyframesproperty.md) 屬性設定為 VARIANT TRUE，以將編碼器設定為產生「虛擬」畫面格 \_ 。</span><span class="sxs-lookup"><span data-stu-id="b134b-106">If you need to have a sample for every frame (this is required by some containers, for example), you can configure the encoder to produce "dummy" frames by setting the [MFPKEY\_PRODUCEDUMMYFRAMES](mfpkey-producedummyframesproperty.md) property to VARIANT\_TRUE.</span></span>

<span data-ttu-id="b134b-107">當編碼器無法編碼所有框架，而不會溢出緩衝區時，就會卸載框架。</span><span class="sxs-lookup"><span data-stu-id="b134b-107">The encoder drops frames when it cannot encode all of the frames without overflowing the buffer.</span></span> <span data-ttu-id="b134b-108">捨棄的框架會影響資料流程的品質，而不會有重複的畫面格。</span><span class="sxs-lookup"><span data-stu-id="b134b-108">Dropped frames affect the quality of the stream, duplicate frames do not.</span></span>

<span data-ttu-id="b134b-109">您可以從編碼器取得畫面格統計資料，以判斷是否已卸載框架。</span><span class="sxs-lookup"><span data-stu-id="b134b-109">You can get frame statistics from the encoder to determine whether frames have been dropped.</span></span> <span data-ttu-id="b134b-110">如需詳細資訊，請參閱 [取得編碼統計資料](gettingencodingstatistics.md)。</span><span class="sxs-lookup"><span data-stu-id="b134b-110">For more information, see [Getting Encoding Statistics](gettingencodingstatistics.md).</span></span>

<span data-ttu-id="b134b-111">通常，如果有重複的框架 (，以品質為基礎的 VBR 串流將只有較原始的框架較少，因為位元速率不受限制) 。</span><span class="sxs-lookup"><span data-stu-id="b134b-111">Typically, quality-based VBR streams will only have fewer frames than the original if there are duplicate frames (because the bit rate is not constrained).</span></span>

## <a name="related-topics"></a><span data-ttu-id="b134b-112">相關主題</span><span class="sxs-lookup"><span data-stu-id="b134b-112">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b134b-113">常見問題集</span><span class="sxs-lookup"><span data-stu-id="b134b-113">Frequently Asked Questions</span></span>](frequentlyaskedquestions.md)
</dt> </dl>

 

 



