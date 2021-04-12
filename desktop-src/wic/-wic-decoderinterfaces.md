---
description: 解碼器介面
ms.assetid: b88517cc-06fe-4d83-a6a9-76e1f34293f4
title: 解碼器介面
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ef90ca2dd521c15460295505a6d5b7ea451c4dba
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104194781"
---
# <a name="decoder-interfaces"></a><span data-ttu-id="f2f4b-103">解碼器介面</span><span class="sxs-lookup"><span data-stu-id="f2f4b-103">Decoder Interfaces</span></span>

<span data-ttu-id="f2f4b-104">下表顯示 Windows 影像處理元件 (WIC) 的解碼器所實的介面，而類別圖表則顯示繼承階層。</span><span class="sxs-lookup"><span data-stu-id="f2f4b-104">The following tables show the interfaces implemented by Windows Imaging Component (WIC) decoders, and the class diagram shows the inheritance hierarchy.</span></span>

<span data-ttu-id="f2f4b-105">Container-Level 的解碼器介面</span><span class="sxs-lookup"><span data-stu-id="f2f4b-105">Container-Level Decoder Interfaces</span></span>



| <span data-ttu-id="f2f4b-106">介面</span><span class="sxs-lookup"><span data-stu-id="f2f4b-106">Interface</span></span>                                                                                       | <span data-ttu-id="f2f4b-107">職責</span><span class="sxs-lookup"><span data-stu-id="f2f4b-107">Responsibilities</span></span>                             | <span data-ttu-id="f2f4b-108">實作</span><span class="sxs-lookup"><span data-stu-id="f2f4b-108">Implementation</span></span>                                                             |
|-------------------------------------------------------------------------------------------------|----------------------------------------------|----------------------------------------------------------------------------|
| [<span data-ttu-id="f2f4b-109">IWICBitmapDecoder</span><span class="sxs-lookup"><span data-stu-id="f2f4b-109">IWICBitmapDecoder</span></span>](-wic-imp-iwicbitmapdecoder.md)                                             | <span data-ttu-id="f2f4b-110">容器層級服務</span><span class="sxs-lookup"><span data-stu-id="f2f4b-110">Container-level services</span></span>                     | <span data-ttu-id="f2f4b-111">必要</span><span class="sxs-lookup"><span data-stu-id="f2f4b-111">Required</span></span>                                                                   |
| [<span data-ttu-id="f2f4b-112">IWICBitmapCodecProgressNotification</span><span class="sxs-lookup"><span data-stu-id="f2f4b-112">IWICBitmapCodecProgressNotification</span></span>](-wic-imp-iwicbitmapcodecprogressnotification-decoder.md) | <span data-ttu-id="f2f4b-113">& 取消支援的進度通知</span><span class="sxs-lookup"><span data-stu-id="f2f4b-113">Progress notification & cancellation support</span></span> | <span data-ttu-id="f2f4b-114">建議</span><span class="sxs-lookup"><span data-stu-id="f2f4b-114">Recommended</span></span>                                                                |
| [<span data-ttu-id="f2f4b-115">IWICMetadataBlockReader</span><span class="sxs-lookup"><span data-stu-id="f2f4b-115">IWICMetadataBlockReader</span></span>](-wic-imp-iwicmetadatablockreader.md)                                 | <span data-ttu-id="f2f4b-116">中繼資料列舉</span><span class="sxs-lookup"><span data-stu-id="f2f4b-116">Metadata enumeration</span></span>                         | <span data-ttu-id="f2f4b-117">選擇性 (只有支援容器層級中繼資料的格式才需要) </span><span class="sxs-lookup"><span data-stu-id="f2f4b-117">Optional (Required only for formats that support container-level metadata)</span></span> |



 

<span data-ttu-id="f2f4b-118">Frame-Level 的解碼器介面</span><span class="sxs-lookup"><span data-stu-id="f2f4b-118">Frame-Level Decoder Interfaces</span></span>



| <span data-ttu-id="f2f4b-119">介面</span><span class="sxs-lookup"><span data-stu-id="f2f4b-119">Interface</span></span>                                                           | <span data-ttu-id="f2f4b-120">職責</span><span class="sxs-lookup"><span data-stu-id="f2f4b-120">Responsibilities</span></span>          | <span data-ttu-id="f2f4b-121">實作</span><span class="sxs-lookup"><span data-stu-id="f2f4b-121">Implementation</span></span>                |
|---------------------------------------------------------------------|---------------------------|-------------------------------|
| [<span data-ttu-id="f2f4b-122">IWICBitmapFrameDecode</span><span class="sxs-lookup"><span data-stu-id="f2f4b-122">IWICBitmapFrameDecode</span></span>](-wic-imp-iwicbitmapframedecode.md)         | <span data-ttu-id="f2f4b-123">框架層級服務</span><span class="sxs-lookup"><span data-stu-id="f2f4b-123">Frame-level services</span></span>      | <span data-ttu-id="f2f4b-124">必要</span><span class="sxs-lookup"><span data-stu-id="f2f4b-124">Required</span></span>                      |
| [<span data-ttu-id="f2f4b-125">IWICMetadataBlockReader</span><span class="sxs-lookup"><span data-stu-id="f2f4b-125">IWICMetadataBlockReader</span></span>](-wic-imp-iwicmetadatablockreader.md)     | <span data-ttu-id="f2f4b-126">中繼資料列舉</span><span class="sxs-lookup"><span data-stu-id="f2f4b-126">Metadata enumeration</span></span>      | <span data-ttu-id="f2f4b-127">必要</span><span class="sxs-lookup"><span data-stu-id="f2f4b-127">Required</span></span>                      |
| [<span data-ttu-id="f2f4b-128">IWICBitmapSourceTransform</span><span class="sxs-lookup"><span data-stu-id="f2f4b-128">IWICBitmapSourceTransform</span></span>](-wic-imp-iwicbitmapsourcetransform.md) | <span data-ttu-id="f2f4b-129">原生解碼器轉換</span><span class="sxs-lookup"><span data-stu-id="f2f4b-129">Native decoder transforms</span></span> | <span data-ttu-id="f2f4b-130">建議</span><span class="sxs-lookup"><span data-stu-id="f2f4b-130">Recommended</span></span>                   |
| [<span data-ttu-id="f2f4b-131">IWICDevelopRaw</span><span class="sxs-lookup"><span data-stu-id="f2f4b-131">IWICDevelopRaw</span></span>](-wic-imp-iwicdevelopraw.md)                       | <span data-ttu-id="f2f4b-132">原始處理服務</span><span class="sxs-lookup"><span data-stu-id="f2f4b-132">Raw processing services</span></span>   | <span data-ttu-id="f2f4b-133">只有 Raw 格式的必要</span><span class="sxs-lookup"><span data-stu-id="f2f4b-133">Required for Raw formats only</span></span> |



 

![wic 介面繼承階層](graphics/wicinterfaces.png)

## <a name="related-topics"></a><span data-ttu-id="f2f4b-135">相關主題</span><span class="sxs-lookup"><span data-stu-id="f2f4b-135">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="f2f4b-136">**概念**</span><span class="sxs-lookup"><span data-stu-id="f2f4b-136">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="f2f4b-137">執行 WIC-Enabled 的解碼器</span><span class="sxs-lookup"><span data-stu-id="f2f4b-137">Implementing a WIC-Enabled Decoder</span></span>](-wic-implementingwicdecoder.md)
</dt> <dt>

[<span data-ttu-id="f2f4b-138">執行 IWICBitmapDecoder</span><span class="sxs-lookup"><span data-stu-id="f2f4b-138">Implementing IWICBitmapDecoder</span></span>](-wic-imp-iwicbitmapdecoder.md)
</dt> <dt>

[<span data-ttu-id="f2f4b-139">如何撰寫 WIC-Enabled 編解碼器</span><span class="sxs-lookup"><span data-stu-id="f2f4b-139">How to Write a WIC-Enabled CODEC</span></span>](-wic-howtowriteacodec.md)
</dt> <dt>

[<span data-ttu-id="f2f4b-140">Windows 影像處理元件總覽</span><span class="sxs-lookup"><span data-stu-id="f2f4b-140">Windows Imaging Component Overview</span></span>](-wic-about-windows-imaging-codec.md)
</dt> </dl>

 

 



