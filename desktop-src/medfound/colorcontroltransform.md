---
description: 調整影片資料流程的色彩特性。
ms.assetid: 738c1f0c-8417-4b12-a7f1-9bbf3c7e9dd3
title: '色彩控制轉換 DSP (Wmcodecdsp .h) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0b94c8314bfd2be85a3bbc392bfa0e83767ff0b0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103689351"
---
# <a name="color-control-transform-dsp"></a><span data-ttu-id="8df45-103">色彩控制轉換 DSP</span><span class="sxs-lookup"><span data-stu-id="8df45-103">Color Control Transform DSP</span></span>

<span data-ttu-id="8df45-104">調整影片資料流程的色彩特性。</span><span class="sxs-lookup"><span data-stu-id="8df45-104">Adjusts the color characteristics of a video stream.</span></span>

## <a name="clsid"></a><span data-ttu-id="8df45-105">CLSID</span><span class="sxs-lookup"><span data-stu-id="8df45-105">CLSID</span></span>

<span data-ttu-id="8df45-106">CLSID \_ CColorControlDmo</span><span class="sxs-lookup"><span data-stu-id="8df45-106">CLSID\_CColorControlDmo</span></span>

## <a name="interfaces"></a><span data-ttu-id="8df45-107">介面</span><span class="sxs-lookup"><span data-stu-id="8df45-107">Interfaces</span></span>

-   <span data-ttu-id="8df45-108">**IMediaObject**</span><span class="sxs-lookup"><span data-stu-id="8df45-108">**IMediaObject**</span></span>
-   <span data-ttu-id="8df45-109">**IMFTransform**</span><span class="sxs-lookup"><span data-stu-id="8df45-109">**IMFTransform**</span></span>
-   <span data-ttu-id="8df45-110">**IPropertyStore**</span><span class="sxs-lookup"><span data-stu-id="8df45-110">**IPropertyStore**</span></span>

## <a name="formats"></a><span data-ttu-id="8df45-111">格式</span><span class="sxs-lookup"><span data-stu-id="8df45-111">Formats</span></span>

-   <span data-ttu-id="8df45-112">RGB 24</span><span class="sxs-lookup"><span data-stu-id="8df45-112">RGB 24</span></span>
-   <span data-ttu-id="8df45-113">RGB 32</span><span class="sxs-lookup"><span data-stu-id="8df45-113">RGB 32</span></span>
-   <span data-ttu-id="8df45-114">RGB 555</span><span class="sxs-lookup"><span data-stu-id="8df45-114">RGB 555</span></span>
-   <span data-ttu-id="8df45-115">RGB 565</span><span class="sxs-lookup"><span data-stu-id="8df45-115">RGB 565</span></span>
-   <span data-ttu-id="8df45-116">AYUV</span><span class="sxs-lookup"><span data-stu-id="8df45-116">AYUV</span></span>
-   <span data-ttu-id="8df45-117">UYVY</span><span class="sxs-lookup"><span data-stu-id="8df45-117">UYVY</span></span>
-   <span data-ttu-id="8df45-118">YUY2</span><span class="sxs-lookup"><span data-stu-id="8df45-118">YUY2</span></span>
-   <span data-ttu-id="8df45-119">YV12</span><span class="sxs-lookup"><span data-stu-id="8df45-119">YV12</span></span>

## <a name="properties"></a><span data-ttu-id="8df45-120">屬性</span><span class="sxs-lookup"><span data-stu-id="8df45-120">Properties</span></span>

-   [<span data-ttu-id="8df45-121">MFPKEY \_ 色彩 \_ 亮度</span><span class="sxs-lookup"><span data-stu-id="8df45-121">MFPKEY\_COLOR\_BRIGHTNESS</span></span>](mfpkey-color-brightness.md)
-   [<span data-ttu-id="8df45-122">MFPKEY \_ 色彩 \_ 對比</span><span class="sxs-lookup"><span data-stu-id="8df45-122">MFPKEY\_COLOR\_CONTRAST</span></span>](mfpkey-color-contrast.md)
-   [<span data-ttu-id="8df45-123">MFPKEY \_ 色彩 \_ 色調</span><span class="sxs-lookup"><span data-stu-id="8df45-123">MFPKEY\_COLOR\_HUE</span></span>](mfpkey-color-hue.md)
-   [<span data-ttu-id="8df45-124">MFPKEY \_ 色彩 \_ 飽和度</span><span class="sxs-lookup"><span data-stu-id="8df45-124">MFPKEY\_COLOR\_SATURATION</span></span>](mfpkey-color-saturation.md)

## <a name="remarks"></a><span data-ttu-id="8df45-125">備註</span><span class="sxs-lookup"><span data-stu-id="8df45-125">Remarks</span></span>

<span data-ttu-id="8df45-126">此 DSP 會修改影片資料流程的內容。</span><span class="sxs-lookup"><span data-stu-id="8df45-126">This DSP modifies the contents of the video stream.</span></span> <span data-ttu-id="8df45-127">針對播放，您可以使用 **IMFVideoProcessor** 介面（可控制圖形配接器的影片處理），更有效率地達成類似效果。</span><span class="sxs-lookup"><span data-stu-id="8df45-127">For playback, you might be able to achieve similar effects more efficiently by using the **IMFVideoProcessor** interface, which controls video processing in the graphics card.</span></span>

## <a name="requirements"></a><span data-ttu-id="8df45-128">規格需求</span><span class="sxs-lookup"><span data-stu-id="8df45-128">Requirements</span></span>



| <span data-ttu-id="8df45-129">需求</span><span class="sxs-lookup"><span data-stu-id="8df45-129">Requirement</span></span> | <span data-ttu-id="8df45-130">值</span><span class="sxs-lookup"><span data-stu-id="8df45-130">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="8df45-131">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="8df45-131">Minimum supported client</span></span><br/> | <span data-ttu-id="8df45-132">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="8df45-132">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="8df45-133">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="8df45-133">Minimum supported server</span></span><br/> | <span data-ttu-id="8df45-134">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="8df45-134">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="8df45-135">標頭</span><span class="sxs-lookup"><span data-stu-id="8df45-135">Header</span></span><br/>                   | <dl> <span data-ttu-id="8df45-136"><dt>Wmcodecdsp。h</dt></span><span class="sxs-lookup"><span data-stu-id="8df45-136"><dt>Wmcodecdsp.h</dt></span></span> </dl> |
| <span data-ttu-id="8df45-137">DLL</span><span class="sxs-lookup"><span data-stu-id="8df45-137">DLL</span></span><br/>                      | <dl> <span data-ttu-id="8df45-138"><dt>Mfvdsp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="8df45-138"><dt>Mfvdsp.dll</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="8df45-139">另請參閱</span><span class="sxs-lookup"><span data-stu-id="8df45-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8df45-140">數位訊號處理器</span><span class="sxs-lookup"><span data-stu-id="8df45-140">Digital Signal Processors</span></span>](windowsmediadigitalsignalprocessors.md)
</dt> </dl>

 

 




