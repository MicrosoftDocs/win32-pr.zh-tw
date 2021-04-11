---
description: '執行 IWICBitmapCodecProgressNotification (編碼器) '
ms.assetid: d470ec93-d329-48c0-9556-0c15daece491
title: '執行 IWICBitmapCodecProgressNotification (編碼器) '
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 260fac41068de0695813d569881e4a71938eb83d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103851220"
---
# <a name="implementing-iwicbitmapcodecprogressnotification-encoder"></a><span data-ttu-id="76ee4-103">執行 IWICBitmapCodecProgressNotification (編碼器) </span><span class="sxs-lookup"><span data-stu-id="76ee4-103">Implementing IWICBitmapCodecProgressNotification (Encoder)</span></span>

## <a name="iwicbitmapcodecprogressnotification"></a><span data-ttu-id="76ee4-104">IWICBitmapCodecProgressNotification</span><span class="sxs-lookup"><span data-stu-id="76ee4-104">IWICBitmapCodecProgressNotification</span></span>

<span data-ttu-id="76ee4-105">雖然 [**IWICBitmapCodecProgressNotification**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapcodecprogressnotification) 介面是選擇性的，但建議在容器層級編碼器類別上執行。</span><span class="sxs-lookup"><span data-stu-id="76ee4-105">Although the [**IWICBitmapCodecProgressNotification**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapcodecprogressnotification) interface is optional, it is recommended that it be implemented on the container-level encoder class.</span></span> <span data-ttu-id="76ee4-106">此介面會在 [執行 IWICBitmapCodecProgressNotification () ](-wic-imp-iwicbitmapcodecprogressnotification-decoder.md)的詳細資料中討論。</span><span class="sxs-lookup"><span data-stu-id="76ee4-106">This interface is discussed in more details in [Implementing IWICBitmapCodecProgressNotification (Decoder)](-wic-imp-iwicbitmapcodecprogressnotification-decoder.md).</span></span> <span data-ttu-id="76ee4-107">此實作為解碼器和編碼器的相同。</span><span class="sxs-lookup"><span data-stu-id="76ee4-107">The implementation is the same for either the decoder and the encoder.</span></span>

## <a name="related-topics"></a><span data-ttu-id="76ee4-108">相關主題</span><span class="sxs-lookup"><span data-stu-id="76ee4-108">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="76ee4-109">**概念**</span><span class="sxs-lookup"><span data-stu-id="76ee4-109">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="76ee4-110">執行 IWICBitmapEncoder</span><span class="sxs-lookup"><span data-stu-id="76ee4-110">Implementing IWICBitmapEncoder</span></span>](-wic-imp-iwicbitmapencoder.md)
</dt> <dt>

[<span data-ttu-id="76ee4-111">執行 IWICBitmapFrameEncode</span><span class="sxs-lookup"><span data-stu-id="76ee4-111">Implementing IWICBitmapFrameEncode</span></span>](-wic-imp-iwicbitmapframeencode.md)
</dt> <dt>

[<span data-ttu-id="76ee4-112">如何撰寫 WIC-Enabled 編解碼器</span><span class="sxs-lookup"><span data-stu-id="76ee4-112">How to Write a WIC-Enabled CODEC</span></span>](-wic-howtowriteacodec.md)
</dt> <dt>

[<span data-ttu-id="76ee4-113">Windows 影像處理元件總覽</span><span class="sxs-lookup"><span data-stu-id="76ee4-113">Windows Imaging Component Overview</span></span>](-wic-about-windows-imaging-codec.md)
</dt> <dt>

[<span data-ttu-id="76ee4-114">執行 IWICBitmapCodecProgressNotification (解碼器) </span><span class="sxs-lookup"><span data-stu-id="76ee4-114">Implementing IWICBitmapCodecProgressNotification (Decoder)</span></span>](-wic-imp-iwicbitmapcodecprogressnotification-decoder.md)
</dt> </dl>

 

 



