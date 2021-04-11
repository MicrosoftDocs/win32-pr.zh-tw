---
description: 編碼器和解碼器開發
ms.assetid: 075aaf0f-63c6-4286-966e-fdc72d0acb6e
title: 編碼器和解碼器開發
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dbe45fc726338e33205831959986178f4527673a
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "104109204"
---
# <a name="encoder-and-decoder-development"></a><span data-ttu-id="16e13-103">編碼器和解碼器開發</span><span class="sxs-lookup"><span data-stu-id="16e13-103">Encoder and Decoder Development</span></span>

<span data-ttu-id="16e13-104">本章節包含適用于 DirectShow 的編碼器和解碼器開發的相關文章。</span><span class="sxs-lookup"><span data-stu-id="16e13-104">This section contains articles about encoder and decoder development for DirectShow.</span></span> <span data-ttu-id="16e13-105">這些主題與應用程式開發人員無關。</span><span class="sxs-lookup"><span data-stu-id="16e13-105">These topics are not relevant for application developers.</span></span>

<span data-ttu-id="16e13-106">支援 DirectX Video 加速 (VA) 的軟體解碼器必須實作為 DirectShow 複製轉換篩選。</span><span class="sxs-lookup"><span data-stu-id="16e13-106">A software decoder that supports DirectX Video Acceleration (VA) must be implemented as a DirectShow copy transform filter.</span></span> <span data-ttu-id="16e13-107">如果此解碼器不支援 DirectX VA，也可以將它實作為 DirectX 媒體物件 (的) 。</span><span class="sxs-lookup"><span data-stu-id="16e13-107">If the decoder does not support DirectX VA, it can also be implemented as a DirectX Media Object (DMO).</span></span> <span data-ttu-id="16e13-108">連接至影片轉譯器的解碼器不應該實作為就地篩選，因為這樣會導致效能大幅降低。</span><span class="sxs-lookup"><span data-stu-id="16e13-108">A decoder that connects to a video renderer should not be implemented as a trans-in-place filter, because this will result in significant performance degradation.</span></span> <span data-ttu-id="16e13-109">如需如何撰寫複製轉換篩選的相關資訊，請參閱 [寫入轉換篩選](writing-transform-filters.md)。</span><span class="sxs-lookup"><span data-stu-id="16e13-109">For information on how to write a copy transform filter, see [Writing Transform Filters](writing-transform-filters.md).</span></span>

<span data-ttu-id="16e13-110">軟體編碼器可以實作為轉換篩選或 DMOs。</span><span class="sxs-lookup"><span data-stu-id="16e13-110">Software encoders can be implemented as either transform filters or DMOs.</span></span> <span data-ttu-id="16e13-111">編碼器不會使用 DirectX VA，因為 DirectX VA 目前僅用於解壓縮。</span><span class="sxs-lookup"><span data-stu-id="16e13-111">Encoders do not use DirectX VA, since DirectX VA currently is only used for decompression.</span></span> <span data-ttu-id="16e13-112">本節所述的編碼器 API 規格與硬體和軟體編碼器有關。</span><span class="sxs-lookup"><span data-stu-id="16e13-112">The Encoder API specification described in this section is relevant for both hardware and software encoders.</span></span>

<span data-ttu-id="16e13-113">本節包含下列主題：</span><span class="sxs-lookup"><span data-stu-id="16e13-113">This section contains the following topics:</span></span>

-   [<span data-ttu-id="16e13-114">編碼器 API</span><span class="sxs-lookup"><span data-stu-id="16e13-114">Encoder API</span></span>](encoder-api.md)
-   [<span data-ttu-id="16e13-115">解碼器介面和規格</span><span class="sxs-lookup"><span data-stu-id="16e13-115">Decoder Interfaces and Specifications</span></span>](decoder-interfaces-and-specifications.md)
-   [<span data-ttu-id="16e13-116">Windows Media Center Edition 的解碼器設定</span><span class="sxs-lookup"><span data-stu-id="16e13-116">Decoder Settings for Windows Media Center Edition</span></span>](decoder-settings-for-windows-media-center-edition.md)

## <a name="related-topics"></a><span data-ttu-id="16e13-117">相關主題</span><span class="sxs-lookup"><span data-stu-id="16e13-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="16e13-118">使用 VMR 來進行 DirectShow 篩選器開發人員</span><span class="sxs-lookup"><span data-stu-id="16e13-118">Using the VMR for DirectShow Filter Developers</span></span>](using-the-vmr-for-directshow-filter-developers.md)
</dt> </dl>

 

 



