---
description: WPD \_ 曝光 \_ 計量 \_ 模式列舉類型會描述在裝置上評估仍有影像捕捉的風險時，所要使用的計量模式。
ms.assetid: 5e92013c-600d-4128-ab59-1cfa8953db67
title: 'WPD_EXPOSURE_METERING_MODES 列舉 (PortableDevice .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WPD_EXPOSURE_METERING_MODES
api_type:
- HeaderDef
api_location:
- PortableDevice.h
ms.openlocfilehash: 76c2594339c6fa4997e4d646fc89e8c30dcdf8fa
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106987160"
---
# <a name="wpd_exposure_metering_modes-enumeration"></a><span data-ttu-id="19911-103">WPD \_ 公開 \_ 計量 \_ 模式列舉</span><span class="sxs-lookup"><span data-stu-id="19911-103">WPD\_EXPOSURE\_METERING\_MODES enumeration</span></span>

<span data-ttu-id="19911-104">**WPD \_ 曝光 \_ 計量 \_ 模式** 列舉類型會描述在裝置上評估仍有影像捕捉的風險時，所要使用的計量模式。</span><span class="sxs-lookup"><span data-stu-id="19911-104">The **WPD\_EXPOSURE\_METERING\_MODES** enumeration type describes the metering mode to use when estimating exposure for still image capture by a device.</span></span>

## <a name="syntax"></a><span data-ttu-id="19911-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="19911-105">Syntax</span></span>


```C++
typedef enum WPD_EXPOSURE_METERING_MODES { 
  WPD_EXPOSURE_METERING_MODE_UNDEFINED                = 0,
  WPD_EXPOSURE_METERING_MODE_AVERAGE                  = 1,
  WPD_EXPOSURE_METERING_MODE_CENTER_WEIGHTED_AVERAGE  = 2,
  WPD_EXPOSURE_METERING_MODE_MULTI_SPOT               = 3,
  WPD_EXPOSURE_METERING_MODE_CENTER_SPOT              = 4
} ;
```



## <a name="constants"></a><span data-ttu-id="19911-106">常數</span><span class="sxs-lookup"><span data-stu-id="19911-106">Constants</span></span>

<dl> <dt>

<span data-ttu-id="19911-107"><span id="WPD_EXPOSURE_METERING_MODE_UNDEFINED"></span><span id="wpd_exposure_metering_mode_undefined"></span>**\_未定義 WPD 曝光 \_ 計量 \_ 模式 \_**</span><span class="sxs-lookup"><span data-stu-id="19911-107"><span id="WPD_EXPOSURE_METERING_MODE_UNDEFINED"></span><span id="wpd_exposure_metering_mode_undefined"></span>**WPD\_EXPOSURE\_METERING\_MODE\_UNDEFINED**</span></span>
</dt> <dd>

<span data-ttu-id="19911-108">計量模式未定義。</span><span class="sxs-lookup"><span data-stu-id="19911-108">The metering mode is undefined.</span></span>

</dd> <dt>

<span data-ttu-id="19911-109"><span id="WPD_EXPOSURE_METERING_MODE_AVERAGE"></span><span id="wpd_exposure_metering_mode_average"></span>**WPD \_ 曝光 \_ 計量 \_ 模式 \_ 平均**</span><span class="sxs-lookup"><span data-stu-id="19911-109"><span id="WPD_EXPOSURE_METERING_MODE_AVERAGE"></span><span id="wpd_exposure_metering_mode_average"></span>**WPD\_EXPOSURE\_METERING\_MODE\_AVERAGE**</span></span>
</dt> <dd>

<span data-ttu-id="19911-110">使用整個影像的平均曝光量。</span><span class="sxs-lookup"><span data-stu-id="19911-110">Use averaged exposure across the full image.</span></span>

</dd> <dt>

<span data-ttu-id="19911-111"><span id="WPD_EXPOSURE_METERING_MODE_CENTER_WEIGHTED_AVERAGE"></span><span id="wpd_exposure_metering_mode_center_weighted_average"></span>**WPD \_ 曝光 \_ 計量 \_ 模式 \_ 中心 \_ 加權 \_ 平均**</span><span class="sxs-lookup"><span data-stu-id="19911-111"><span id="WPD_EXPOSURE_METERING_MODE_CENTER_WEIGHTED_AVERAGE"></span><span id="wpd_exposure_metering_mode_center_weighted_average"></span>**WPD\_EXPOSURE\_METERING\_MODE\_CENTER\_WEIGHTED\_AVERAGE**</span></span>
</dt> <dd>

<span data-ttu-id="19911-112">使用平均曝光，並以影像的中心提供更多權數。</span><span class="sxs-lookup"><span data-stu-id="19911-112">Use an averaged exposure, with the center of the image given more weight.</span></span>

</dd> <dt>

<span data-ttu-id="19911-113"><span id="WPD_EXPOSURE_METERING_MODE_MULTI_SPOT"></span><span id="wpd_exposure_metering_mode_multi_spot"></span>**WPD \_ 曝光 \_ 計量 \_ 模式 \_ 多 \_ 點**</span><span class="sxs-lookup"><span data-stu-id="19911-113"><span id="WPD_EXPOSURE_METERING_MODE_MULTI_SPOT"></span><span id="wpd_exposure_metering_mode_multi_spot"></span>**WPD\_EXPOSURE\_METERING\_MODE\_MULTI\_SPOT**</span></span>
</dt> <dd>

<span data-ttu-id="19911-114">使用多點平均技巧。</span><span class="sxs-lookup"><span data-stu-id="19911-114">Use a multi-spot averaging technique.</span></span>

</dd> <dt>

<span data-ttu-id="19911-115"><span id="WPD_EXPOSURE_METERING_MODE_CENTER_SPOT"></span><span id="wpd_exposure_metering_mode_center_spot"></span>**WPD \_ 曝光 \_ 計量 \_ 模式 \_ 中心 \_ 點**</span><span class="sxs-lookup"><span data-stu-id="19911-115"><span id="WPD_EXPOSURE_METERING_MODE_CENTER_SPOT"></span><span id="wpd_exposure_metering_mode_center_spot"></span>**WPD\_EXPOSURE\_METERING\_MODE\_CENTER\_SPOT**</span></span>
</dt> <dd>

<span data-ttu-id="19911-116">使用中央點平均技巧。</span><span class="sxs-lookup"><span data-stu-id="19911-116">Use a center-spot averaging technique.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="19911-117">備註</span><span class="sxs-lookup"><span data-stu-id="19911-117">Remarks</span></span>

<span data-ttu-id="19911-118">指出裝置的計量模式。</span><span class="sxs-lookup"><span data-stu-id="19911-118">Indicates the metering mode of the device.</span></span> <span data-ttu-id="19911-119">[WPD \_ 仍 \_ 影像 \_ 曝光 \_ 計量 \_ 模式](still-image-properties.md)屬性會使用這個列舉。</span><span class="sxs-lookup"><span data-stu-id="19911-119">This enumeration is used by the [WPD\_STILL\_IMAGE\_EXPOSURE\_METERING\_MODE](still-image-properties.md) property.</span></span>

## <a name="requirements"></a><span data-ttu-id="19911-120">規格需求</span><span class="sxs-lookup"><span data-stu-id="19911-120">Requirements</span></span>



| <span data-ttu-id="19911-121">需求</span><span class="sxs-lookup"><span data-stu-id="19911-121">Requirement</span></span> | <span data-ttu-id="19911-122">值</span><span class="sxs-lookup"><span data-stu-id="19911-122">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="19911-123">標頭</span><span class="sxs-lookup"><span data-stu-id="19911-123">Header</span></span><br/> | <dl> <span data-ttu-id="19911-124"><dt>PortableDevice。h</dt></span><span class="sxs-lookup"><span data-stu-id="19911-124"><dt>PortableDevice.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="19911-125">另請參閱</span><span class="sxs-lookup"><span data-stu-id="19911-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="19911-126">**結構和列舉類型**</span><span class="sxs-lookup"><span data-stu-id="19911-126">**Structures and Enumeration Types**</span></span>](structures-and-enumeration-types.md)
</dt> </dl>

 

 




