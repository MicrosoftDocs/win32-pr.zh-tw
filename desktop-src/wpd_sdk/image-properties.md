---
description: Windows 可攜式裝置支援下列影像屬性。
ms.assetid: fb1707a7-16b0-4073-b21d-2ba2f4fd76f7
title: '影像屬性 (PortableDevice .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Image
api_type:
- HeaderDef
api_location:
- PortableDevice.h
ms.openlocfilehash: 959a008d9c30991058226e52db6e45ed417ee6e4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "107001007"
---
# <a name="image-properties"></a><span data-ttu-id="f84fe-103">影像屬性</span><span class="sxs-lookup"><span data-stu-id="f84fe-103">Image Properties</span></span>

<span data-ttu-id="f84fe-104">Windows 可攜式裝置支援下列影像屬性。</span><span class="sxs-lookup"><span data-stu-id="f84fe-104">Windows Portable Devices supports the following image properties.</span></span>



| <span data-ttu-id="f84fe-105">屬性</span><span class="sxs-lookup"><span data-stu-id="f84fe-105">Property</span></span>                                                                                                                                       | <span data-ttu-id="f84fe-106">VarType</span><span class="sxs-lookup"><span data-stu-id="f84fe-106">VarType</span></span>     | <span data-ttu-id="f84fe-107">Description</span><span class="sxs-lookup"><span data-stu-id="f84fe-107">Description</span></span>                                                                                                                                                                                                                                                                                                                                     |
|------------------------------------------------------------------------------------------------------------------------------------------------|-------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f84fe-108">**WPD \_ 影像 \_ BITDEPTH**</span><span class="sxs-lookup"><span data-stu-id="f84fe-108">**WPD\_IMAGE\_BITDEPTH**</span></span>                                                                                                                       | <span data-ttu-id="f84fe-109">**VT \_ UI4**</span><span class="sxs-lookup"><span data-stu-id="f84fe-109">**VT\_UI4**</span></span> | <span data-ttu-id="f84fe-110">影像的位深度。</span><span class="sxs-lookup"><span data-stu-id="f84fe-110">The bit depth of the image.</span></span>                                                                                                                                                                                                                                                                                                                     |
| <span data-ttu-id="f84fe-111"><span id="wpd_image_color_corrected_status"></span><span id="WPD_IMAGE_COLOR_CORRECTED_STATUS"></span>**WPD \_ 影像 \_ 色彩已 \_ 更正 \_ 狀態**</span><span class="sxs-lookup"><span data-stu-id="f84fe-111"><span id="wpd_image_color_corrected_status"></span><span id="WPD_IMAGE_COLOR_CORRECTED_STATUS"></span>**WPD\_IMAGE\_COLOR\_CORRECTED\_STATUS**</span></span> | <span data-ttu-id="f84fe-112">**VT \_ UI4**</span><span class="sxs-lookup"><span data-stu-id="f84fe-112">**VT\_UI4**</span></span> | <span data-ttu-id="f84fe-113">[**WPD \_ 色彩更正 \_ 的 \_ 狀態值 \_**](wpd-color-corrected-status-values.md)列舉，指定檔案是否已進行色彩更正。這可防止多個裝置在進行後置處理時自動對影像進行色彩校正。</span><span class="sxs-lookup"><span data-stu-id="f84fe-113">A [**WPD\_COLOR\_CORRECTED\_STATUS\_VALUES**](wpd-color-corrected-status-values.md) enumeration that specifies whether the file has been color-corrected.This prevents multiple devices from automatically color-correcting the image during post-processing.</span></span><br/>                                                                       |
| <span data-ttu-id="f84fe-114">**WPD \_ 影像 \_ 裁剪 \_ 狀態**</span><span class="sxs-lookup"><span data-stu-id="f84fe-114">**WPD\_IMAGE\_CROPPED\_STATUS**</span></span>                                                                                                                | <span data-ttu-id="f84fe-115">**VT \_ UI4**</span><span class="sxs-lookup"><span data-stu-id="f84fe-115">**VT\_UI4**</span></span> | <span data-ttu-id="f84fe-116">[**WPD \_ 裁剪的 \_ 狀態值 \_**](wpd-cropped-status-values.md)列舉，這個值會指定檔案是否已裁剪。這可防止多個裝置在後續處理期間自動裁剪影像。</span><span class="sxs-lookup"><span data-stu-id="f84fe-116">A [**WPD\_CROPPED\_STATUS\_VALUES**](wpd-cropped-status-values.md) enumeration that specifies whether the file has been cropped.This prevents multiple devices from automatically cropping the image during post-processing.</span></span><br/>                                                                                                        |
| <span data-ttu-id="f84fe-117">**WPD \_ 影像 \_ 曝光 \_ 索引**</span><span class="sxs-lookup"><span data-stu-id="f84fe-117">**WPD\_IMAGE\_EXPOSURE\_INDEX**</span></span>                                                                                                                | <span data-ttu-id="f84fe-118">**VT \_ UI4**</span><span class="sxs-lookup"><span data-stu-id="f84fe-118">**VT\_UI4**</span></span> | <span data-ttu-id="f84fe-119">值，這個值會識別在捕獲此映射時的電影速度設定。這些設定會對應至 ASA/等的 ISO 指派。</span><span class="sxs-lookup"><span data-stu-id="f84fe-119">A value that identifies the film speed settings when this image was captured.The settings correspond to the ISO designations of ASA/DIN.</span></span><br/> <span data-ttu-id="f84fe-120">通常，裝置支援離散列舉值，但可能會持續控制範圍。</span><span class="sxs-lookup"><span data-stu-id="f84fe-120">Typically, a device supports discrete enumerated values, but continuous control over a range is possible.</span></span><br/> <span data-ttu-id="f84fe-121">0xFFFFFFFF 的值對應到自動 ISO 設定。</span><span class="sxs-lookup"><span data-stu-id="f84fe-121">A value of 0xFFFFFFFF corresponds to automatic ISO setting.</span></span><br/> |
| <span data-ttu-id="f84fe-122">**WPD \_ 影像 \_ 曝光 \_ 時間**</span><span class="sxs-lookup"><span data-stu-id="f84fe-122">**WPD\_IMAGE\_EXPOSURE\_TIME**</span></span>                                                                                                                 | <span data-ttu-id="f84fe-123">**VT \_ UI4**</span><span class="sxs-lookup"><span data-stu-id="f84fe-123">**VT\_UI4**</span></span> | <span data-ttu-id="f84fe-124">識別在捕獲此映射時裝置的快門速度。單位以秒為單位，以10000來調整。</span><span class="sxs-lookup"><span data-stu-id="f84fe-124">Identifies the shutter speed of the device when this image was captured.Units are in seconds scaled by 10000.</span></span><br/>                                                                                                                                                                                                                        |
| <span data-ttu-id="f84fe-125">**WPD \_ 影像 \_ FNUMBER**</span><span class="sxs-lookup"><span data-stu-id="f84fe-125">**WPD\_IMAGE\_FNUMBER**</span></span>                                                                                                                        | <span data-ttu-id="f84fe-126">**VT \_ UI4**</span><span class="sxs-lookup"><span data-stu-id="f84fe-126">**VT\_UI4**</span></span> | <span data-ttu-id="f84fe-127">識別在捕獲此影像時的鏡頭光圈設定。單位等於以100調整的 f 數位。</span><span class="sxs-lookup"><span data-stu-id="f84fe-127">Identifies the aperture setting of the lens when this image was captured.Units are equal to the f-number scaled by 100.</span></span><br/>                                                                                                                                                                                                              |
| <span data-ttu-id="f84fe-128">**WPD \_ 影像 \_ 水準 \_ 解析度**</span><span class="sxs-lookup"><span data-stu-id="f84fe-128">**WPD\_IMAGE\_HORIZONTAL\_RESOLUTION**</span></span>                                                                                                         | <span data-ttu-id="f84fe-129">**VT \_ R8**</span><span class="sxs-lookup"><span data-stu-id="f84fe-129">**VT\_R8**</span></span>  | <span data-ttu-id="f84fe-130">指出影像的水準解析度，以每英寸的點為單位， (DPI) 。</span><span class="sxs-lookup"><span data-stu-id="f84fe-130">Indicates the horizontal resolution of an image, in dots per inch (DPI) .</span></span>                                                                                                                                                                                                                                                                       |
| <span data-ttu-id="f84fe-131">**WPD \_ 影像 \_ 垂直 \_ 解析度**</span><span class="sxs-lookup"><span data-stu-id="f84fe-131">**WPD\_IMAGE\_VERTICAL\_RESOLUTION**</span></span>                                                                                                           | <span data-ttu-id="f84fe-132">**VT \_ R8**</span><span class="sxs-lookup"><span data-stu-id="f84fe-132">**VT\_R8**</span></span>  | <span data-ttu-id="f84fe-133">指出影像的垂直解析度（以每英寸的點為單位）， (DPI) 。</span><span class="sxs-lookup"><span data-stu-id="f84fe-133">Indicates the vertical resolution of an image, in dots per inch (DPI) .</span></span>                                                                                                                                                                                                                                                                         |



 

## <a name="requirements"></a><span data-ttu-id="f84fe-134">規格需求</span><span class="sxs-lookup"><span data-stu-id="f84fe-134">Requirements</span></span>



| <span data-ttu-id="f84fe-135">需求</span><span class="sxs-lookup"><span data-stu-id="f84fe-135">Requirement</span></span> | <span data-ttu-id="f84fe-136">值</span><span class="sxs-lookup"><span data-stu-id="f84fe-136">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="f84fe-137">標頭</span><span class="sxs-lookup"><span data-stu-id="f84fe-137">Header</span></span><br/> | <dl> <span data-ttu-id="f84fe-138"><dt>PortableDevice。h</dt></span><span class="sxs-lookup"><span data-stu-id="f84fe-138"><dt>PortableDevice.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f84fe-139">另請參閱</span><span class="sxs-lookup"><span data-stu-id="f84fe-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f84fe-140">**WPD 屬性和屬性**</span><span class="sxs-lookup"><span data-stu-id="f84fe-140">**WPD Properties and Attributes**</span></span>](properties-and-attributes.md)
</dt> </dl>

 

 




