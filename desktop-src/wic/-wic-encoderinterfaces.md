---
description: 編碼器介面
ms.assetid: 02365401-8648-4be1-a447-fabd2cb77355
title: 編碼器介面
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5367a25f1a2a4caf486711f7569312a436f8f474
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104193562"
---
# <a name="encoder-interfaces"></a><span data-ttu-id="ee56c-103">編碼器介面</span><span class="sxs-lookup"><span data-stu-id="ee56c-103">Encoder Interfaces</span></span>


<span data-ttu-id="ee56c-104">下表顯示 Windows 影像處理元件 (WIC) 編碼器所執行的介面，而類別圖表會顯示繼承階層。</span><span class="sxs-lookup"><span data-stu-id="ee56c-104">The following tables show the interfaces implemented by Windows Imaging Component (WIC) encoders, and the class diagram shows the inheritance hierarchy.</span></span>

<span data-ttu-id="ee56c-105">Container-Level 編碼器介面</span><span class="sxs-lookup"><span data-stu-id="ee56c-105">Container-Level Encoder Interfaces</span></span>



| <span data-ttu-id="ee56c-106">介面</span><span class="sxs-lookup"><span data-stu-id="ee56c-106">Interface</span></span>                                                                                       | <span data-ttu-id="ee56c-107">職責</span><span class="sxs-lookup"><span data-stu-id="ee56c-107">Responsibilities</span></span>                             | <span data-ttu-id="ee56c-108">實作</span><span class="sxs-lookup"><span data-stu-id="ee56c-108">Implementation</span></span>                                                             |
|-------------------------------------------------------------------------------------------------|----------------------------------------------|----------------------------------------------------------------------------|
| [<span data-ttu-id="ee56c-109">IWICBitmapEncoder</span><span class="sxs-lookup"><span data-stu-id="ee56c-109">IWICBitmapEncoder</span></span>](-wic-imp-iwicbitmapencoder.md)                                             | <span data-ttu-id="ee56c-110">容器層級服務</span><span class="sxs-lookup"><span data-stu-id="ee56c-110">Container-level services</span></span>                     | <span data-ttu-id="ee56c-111">必要</span><span class="sxs-lookup"><span data-stu-id="ee56c-111">Required</span></span>                                                                   |
| [<span data-ttu-id="ee56c-112">IWICBitmapCodecProgressNotification</span><span class="sxs-lookup"><span data-stu-id="ee56c-112">IWICBitmapCodecProgressNotification</span></span>](-wic-imp-iwicbitmapcodecprogressnotification-encoder.md) | <span data-ttu-id="ee56c-113">& 取消支援的進度通知</span><span class="sxs-lookup"><span data-stu-id="ee56c-113">Progress notification & cancellation support</span></span> | <span data-ttu-id="ee56c-114">建議</span><span class="sxs-lookup"><span data-stu-id="ee56c-114">Recommended</span></span>                                                                |
| [<span data-ttu-id="ee56c-115">IWICMetadataBlockWriter</span><span class="sxs-lookup"><span data-stu-id="ee56c-115">IWICMetadataBlockWriter</span></span>](-wic-imp-iwicmetadatablockwriter.md)                                 | <span data-ttu-id="ee56c-116">中繼資料序列化服務</span><span class="sxs-lookup"><span data-stu-id="ee56c-116">Metadata serialization services</span></span>              | <span data-ttu-id="ee56c-117">選擇性 (只有支援容器層級中繼資料的格式才需要) </span><span class="sxs-lookup"><span data-stu-id="ee56c-117">Optional (Required only for formats that support container-level metadata)</span></span> |



 

<span data-ttu-id="ee56c-118">Frame-Level 編碼器介面</span><span class="sxs-lookup"><span data-stu-id="ee56c-118">Frame-Level Encoder Interfaces</span></span>



| <span data-ttu-id="ee56c-119">介面</span><span class="sxs-lookup"><span data-stu-id="ee56c-119">Interface</span></span>                                                       | <span data-ttu-id="ee56c-120">職責</span><span class="sxs-lookup"><span data-stu-id="ee56c-120">Responsibilities</span></span>                | <span data-ttu-id="ee56c-121">實作</span><span class="sxs-lookup"><span data-stu-id="ee56c-121">Implementation</span></span> |
|-----------------------------------------------------------------|---------------------------------|----------------|
| [<span data-ttu-id="ee56c-122">IWICBitmapFrameEncode</span><span class="sxs-lookup"><span data-stu-id="ee56c-122">IWICBitmapFrameEncode</span></span>](-wic-imp-iwicbitmapframeencode.md)     | <span data-ttu-id="ee56c-123">框架層級服務</span><span class="sxs-lookup"><span data-stu-id="ee56c-123">Frame-level services</span></span>            | <span data-ttu-id="ee56c-124">必要</span><span class="sxs-lookup"><span data-stu-id="ee56c-124">Required</span></span>       |
| [<span data-ttu-id="ee56c-125">IWICMetadataBlockWriter</span><span class="sxs-lookup"><span data-stu-id="ee56c-125">IWICMetadataBlockWriter</span></span>](-wic-imp-iwicmetadatablockwriter.md) | <span data-ttu-id="ee56c-126">中繼資料序列化服務</span><span class="sxs-lookup"><span data-stu-id="ee56c-126">Metadata serialization services</span></span> | <span data-ttu-id="ee56c-127">必要</span><span class="sxs-lookup"><span data-stu-id="ee56c-127">Required</span></span>       |



 

![wic 編碼器介面繼承階層](graphics/wicencoderinterfaces.png)

<span data-ttu-id="ee56c-129">您會發現編碼器介面幾乎是解碼介面的鏡像影像，而且這些介面上的大部分方法都對應至相關的解碼器介面上的方法。</span><span class="sxs-lookup"><span data-stu-id="ee56c-129">You'll notice that the encoder interfaces are almost mirror images of the decoder interfaces, and that most of the methods on these interfaces correspond to methods on the related decoder interfaces.</span></span> <span data-ttu-id="ee56c-130">既然您已熟悉啟用 WIC 的解碼器，您現在也會熟悉啟用 WIC 的編碼器。</span><span class="sxs-lookup"><span data-stu-id="ee56c-130">Now that you're familiar with the implementation of a WIC-enabled decoder, the implementation of a WIC-enabled encoder will seem familiar as well.</span></span>

## <a name="related-topics"></a><span data-ttu-id="ee56c-131">相關主題</span><span class="sxs-lookup"><span data-stu-id="ee56c-131">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="ee56c-132">**概念**</span><span class="sxs-lookup"><span data-stu-id="ee56c-132">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="ee56c-133">執行 WIC-Enabled 編碼器</span><span class="sxs-lookup"><span data-stu-id="ee56c-133">Implementing a WIC-Enabled Encoder</span></span>](-wic-implementingwicencoder.md)
</dt> <dt>

[<span data-ttu-id="ee56c-134">執行 IWICBitmapEncoder</span><span class="sxs-lookup"><span data-stu-id="ee56c-134">Implementing IWICBitmapEncoder</span></span>](-wic-imp-iwicbitmapencoder.md)
</dt> <dt>

[<span data-ttu-id="ee56c-135">如何撰寫 WIC-Enabled 編解碼器</span><span class="sxs-lookup"><span data-stu-id="ee56c-135">How to Write a WIC-Enabled CODEC</span></span>](-wic-howtowriteacodec.md)
</dt> <dt>

[<span data-ttu-id="ee56c-136">Windows 影像處理元件總覽</span><span class="sxs-lookup"><span data-stu-id="ee56c-136">Windows Imaging Component Overview</span></span>](-wic-about-windows-imaging-codec.md)
</dt> </dl>

 

 



