---
description: ASF 編碼類型
ms.assetid: ffa99c6b-3b62-4068-96d5-ad57c340d088
title: ASF 編碼類型
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1c6187f4bbf49eafaf50a46a8af92b71b4e72885
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104111892"
---
# <a name="asf-encoding-types"></a><span data-ttu-id="90948-103">ASF 編碼類型</span><span class="sxs-lookup"><span data-stu-id="90948-103">ASF Encoding Types</span></span>

<span data-ttu-id="90948-104">編碼方法全都專注于編碼器所使用的緩衝區，以管理未壓縮的輸入資料。</span><span class="sxs-lookup"><span data-stu-id="90948-104">The encoding methods all focus on the buffer used by the encoder to manage uncompressed input data.</span></span> <span data-ttu-id="90948-105">這個緩衝區是以資料流程的位元速率（每秒位數）和緩衝區視窗（以毫秒為單位）來定義。</span><span class="sxs-lookup"><span data-stu-id="90948-105">This buffer is defined by the bit rate of the stream, in bits per second, and the buffer window, in milliseconds.</span></span> <span data-ttu-id="90948-106">編碼為 ASF 檔案時，Windows Media 編碼器會遵守緩衝區的限制。</span><span class="sxs-lookup"><span data-stu-id="90948-106">When encoding to ASF files, the Windows Media encoders abide by the constraints of the buffer.</span></span> <span data-ttu-id="90948-107">如需有關緩衝區視窗的詳細資訊，請參閱 [有漏洞 Bucket 緩衝區模型](the-leaky-bucket-buffer-model.md)。</span><span class="sxs-lookup"><span data-stu-id="90948-107">For more information about the buffer window, see [The Leaky Bucket Buffer Model](the-leaky-bucket-buffer-model.md).</span></span> <span data-ttu-id="90948-108">瞭解每個方法的使用方式和時機，可以協助您建立高品質的壓縮內容。</span><span class="sxs-lookup"><span data-stu-id="90948-108">Knowing how and when to use each method can help you create high-quality compressed content.</span></span> <span data-ttu-id="90948-109">下表包含每個可用編碼方法的相關主題連結，可供應用程式用來將媒體資料編碼為 ASF。</span><span class="sxs-lookup"><span data-stu-id="90948-109">The following table contains links to topics about each of the available encoding methods that an application can use to encode media data to ASF.</span></span>



| <span data-ttu-id="90948-110">編碼方法</span><span class="sxs-lookup"><span data-stu-id="90948-110">Encoding method</span></span>                                                                                      | <span data-ttu-id="90948-111">Description</span><span class="sxs-lookup"><span data-stu-id="90948-111">Description</span></span>                                                                                                                                                                                              |
|------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="90948-112">常數位元速率編碼</span><span class="sxs-lookup"><span data-stu-id="90948-112">Constant Bit Rate Encoding</span></span>](constant-bit-rate-encoding.md)                                         | <span data-ttu-id="90948-113">編碼器會將資料壓縮成指定的位元速率。</span><span class="sxs-lookup"><span data-stu-id="90948-113">The encoder compresses data to a specified bit rate.</span></span>                                                                                                                                                     |
| [<span data-ttu-id="90948-114">以品質為基礎的變數位元速率編碼</span><span class="sxs-lookup"><span data-stu-id="90948-114">Quality-Based Variable Bit Rate Encoding</span></span>](quality-based-variable-bit-rate--vbr--encoding.md)       | <span data-ttu-id="90948-115">編碼器會將資料壓縮成特定的品質值，讓編碼媒體的品質在整個持續期間都一致，不論產生的資料流程是否有緩衝區需求。</span><span class="sxs-lookup"><span data-stu-id="90948-115">The encoder compresses data to a particular quality value so that the quality of the encoded media is consistent throughout its duration, regardless of the buffer requirements of the resulting stream.</span></span> |
| [<span data-ttu-id="90948-116">不受限制的變數位速率編碼</span><span class="sxs-lookup"><span data-stu-id="90948-116">Unconstrained Variable Bit Rate Encoding</span></span>](unconstrained-variable-bit-rate--vbr--encoding.md)       | <span data-ttu-id="90948-117">編碼器會將資料壓縮成可能的最高品質，同時維持指定的位元速率。</span><span class="sxs-lookup"><span data-stu-id="90948-117">The encoder compresses data to the highest possible quality while maintaining a specified bit rate.</span></span> <span data-ttu-id="90948-118">這種模式也稱為2傳遞變數位元速率 (VBR) 編碼。</span><span class="sxs-lookup"><span data-stu-id="90948-118">This mode is also called 2-pass variable bit rate (VBR) encoding.</span></span>                                    |
| [<span data-ttu-id="90948-119">尖峰限制的可變位速率編碼</span><span class="sxs-lookup"><span data-stu-id="90948-119">Peak-Constrained Variable Bit Rate Encoding</span></span>](peak-constrained-variable-bit-rate--vbr--encoding.md) | <span data-ttu-id="90948-120">編碼器會將資料壓縮成指定的位元速率，同時將緩衝區值保留在指定的最大緩衝區視窗和位元速率。</span><span class="sxs-lookup"><span data-stu-id="90948-120">The encoder compresses data to a specified bit rate while keeping the buffer values under the specified maximum buffer window and bit rate.</span></span> <span data-ttu-id="90948-121">這種模式也稱為雙通路尖峰的 VBR。</span><span class="sxs-lookup"><span data-stu-id="90948-121">This mode is also called 2-pass peak VBR.</span></span>                    |



 

## <a name="related-topics"></a><span data-ttu-id="90948-122">相關主題</span><span class="sxs-lookup"><span data-stu-id="90948-122">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="90948-123">媒體基礎中的 ASF 支援</span><span class="sxs-lookup"><span data-stu-id="90948-123">ASF Support in Media Foundation</span></span>](asf-support-in-media-foundation.md)
</dt> <dt>

[<span data-ttu-id="90948-124">Windows Media 編碼器</span><span class="sxs-lookup"><span data-stu-id="90948-124">Windows Media Encoders</span></span>](windows-media-encoders.md)
</dt> </dl>

 

 



