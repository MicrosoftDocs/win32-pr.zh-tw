---
description: WPD \_ 曝光 \_ 程式 \_ 模式列舉型別描述使用裝置來捕捉映射時，所要使用的曝光模式。
ms.assetid: 68b76294-6ad3-4f4a-bf02-bc31c9e8ac62
title: 'WPD_EXPOSURE_PROGRAM_MODES 列舉 (PortableDevice .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WPD_EXPOSURE_PROGRAM_MODES
api_type:
- HeaderDef
api_location:
- PortableDevice.h
ms.openlocfilehash: a88ce90bb9e776cd45245b32a363635c2ccf0560
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106993373"
---
# <a name="wpd_exposure_program_modes-enumeration"></a><span data-ttu-id="6866d-103">WPD \_ 公開 \_ 程式 \_ 模式列舉</span><span class="sxs-lookup"><span data-stu-id="6866d-103">WPD\_EXPOSURE\_PROGRAM\_MODES enumeration</span></span>

<span data-ttu-id="6866d-104">**WPD \_ 曝光 \_ 程式 \_ 模式** 列舉型別描述使用裝置來捕捉映射時，所要使用的曝光模式。</span><span class="sxs-lookup"><span data-stu-id="6866d-104">The **WPD\_EXPOSURE\_PROGRAM\_MODES** enumeration type describes an exposure mode to use when capturing images with a device.</span></span>

## <a name="syntax"></a><span data-ttu-id="6866d-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="6866d-105">Syntax</span></span>


```C++
typedef enum WPD_EXPOSURE_PROGRAM_MODES { 
  WPD_EXPOSURE_PROGRAM_MODE_UNDEFINED          = 0,
  WPD_EXPOSURE_PROGRAM_MODE_MANUAL             = 1,
  WPD_EXPOSURE_PROGRAM_MODE_AUTO               = 2,
  WPD_EXPOSURE_PROGRAM_MODE_APERTURE_PRIORITY  = 3,
  WPD_EXPOSURE_PROGRAM_MODE_SHUTTER_PRIORITY   = 4,
  WPD_EXPOSURE_PROGRAM_MODE_CREATIVE           = 5,
  WPD_EXPOSURE_PROGRAM_MODE_ACTION             = 6,
  WPD_EXPOSURE_PROGRAM_MODE_PORTRAIT           = 7
} ;
```



## <a name="constants"></a><span data-ttu-id="6866d-106">常數</span><span class="sxs-lookup"><span data-stu-id="6866d-106">Constants</span></span>

<dl> <dt>

<span data-ttu-id="6866d-107"><span id="WPD_EXPOSURE_PROGRAM_MODE_UNDEFINED"></span><span id="wpd_exposure_program_mode_undefined"></span>**\_未定義 WPD 曝光 \_ 程式 \_ 模式 \_**</span><span class="sxs-lookup"><span data-stu-id="6866d-107"><span id="WPD_EXPOSURE_PROGRAM_MODE_UNDEFINED"></span><span id="wpd_exposure_program_mode_undefined"></span>**WPD\_EXPOSURE\_PROGRAM\_MODE\_UNDEFINED**</span></span>
</dt> <dd>

<span data-ttu-id="6866d-108">尚未指定曝光模式。</span><span class="sxs-lookup"><span data-stu-id="6866d-108">The exposure mode has not been specified.</span></span>

</dd> <dt>

<span data-ttu-id="6866d-109"><span id="WPD_EXPOSURE_PROGRAM_MODE_MANUAL"></span><span id="wpd_exposure_program_mode_manual"></span>**WPD \_ 曝光 \_ 程式 \_ 模式 \_ 手冊**</span><span class="sxs-lookup"><span data-stu-id="6866d-109"><span id="WPD_EXPOSURE_PROGRAM_MODE_MANUAL"></span><span id="wpd_exposure_program_mode_manual"></span>**WPD\_EXPOSURE\_PROGRAM\_MODE\_MANUAL**</span></span>
</dt> <dd>

<span data-ttu-id="6866d-110">應用程式應指定所有的公開設定。</span><span class="sxs-lookup"><span data-stu-id="6866d-110">The application should specify all exposure settings.</span></span>

</dd> <dt>

<span data-ttu-id="6866d-111"><span id="WPD_EXPOSURE_PROGRAM_MODE_AUTO"></span><span id="wpd_exposure_program_mode_auto"></span>**\_自動 WPD 曝光 \_ 程式 \_ 模式 \_**</span><span class="sxs-lookup"><span data-stu-id="6866d-111"><span id="WPD_EXPOSURE_PROGRAM_MODE_AUTO"></span><span id="wpd_exposure_program_mode_auto"></span>**WPD\_EXPOSURE\_PROGRAM\_MODE\_AUTO**</span></span>
</dt> <dd>

<span data-ttu-id="6866d-112">使用裝置定義的自動曝光模式。</span><span class="sxs-lookup"><span data-stu-id="6866d-112">Use a device-defined automatic exposure mode.</span></span>

</dd> <dt>

<span data-ttu-id="6866d-113"><span id="WPD_EXPOSURE_PROGRAM_MODE_APERTURE_PRIORITY"></span><span id="wpd_exposure_program_mode_aperture_priority"></span>**WPD \_ 曝光 \_ 程式 \_ 模式 \_ 光圈 \_ 優先順序**</span><span class="sxs-lookup"><span data-stu-id="6866d-113"><span id="WPD_EXPOSURE_PROGRAM_MODE_APERTURE_PRIORITY"></span><span id="wpd_exposure_program_mode_aperture_priority"></span>**WPD\_EXPOSURE\_PROGRAM\_MODE\_APERTURE\_PRIORITY**</span></span>
</dt> <dd>

<span data-ttu-id="6866d-114">自動曝光模式，表示鏡頭光圈值應該保持固定，但是快門速度應該由裝置決定。</span><span class="sxs-lookup"><span data-stu-id="6866d-114">An automated exposure mode that indicates that the lens aperture value should remain fixed, but shutter speed should be determined by the device.</span></span>

</dd> <dt>

<span data-ttu-id="6866d-115"><span id="WPD_EXPOSURE_PROGRAM_MODE_SHUTTER_PRIORITY"></span><span id="wpd_exposure_program_mode_shutter_priority"></span>**WPD \_ 曝光 \_ 計畫 \_ 模式 \_ 快門 \_ 優先順序**</span><span class="sxs-lookup"><span data-stu-id="6866d-115"><span id="WPD_EXPOSURE_PROGRAM_MODE_SHUTTER_PRIORITY"></span><span id="wpd_exposure_program_mode_shutter_priority"></span>**WPD\_EXPOSURE\_PROGRAM\_MODE\_SHUTTER\_PRIORITY**</span></span>
</dt> <dd>

<span data-ttu-id="6866d-116">自動曝光模式，表示快門速度應該保持固定，但該鏡頭光圈應由裝置決定。</span><span class="sxs-lookup"><span data-stu-id="6866d-116">An automated exposure mode that indicates that the shutter speed should remain fixed, but that lens aperture should be determined by the device.</span></span>

</dd> <dt>

<span data-ttu-id="6866d-117"><span id="WPD_EXPOSURE_PROGRAM_MODE_CREATIVE"></span><span id="wpd_exposure_program_mode_creative"></span>**WPD \_ 公開 \_ 程式 \_ 模式 \_ 創意**</span><span class="sxs-lookup"><span data-stu-id="6866d-117"><span id="WPD_EXPOSURE_PROGRAM_MODE_CREATIVE"></span><span id="wpd_exposure_program_mode_creative"></span>**WPD\_EXPOSURE\_PROGRAM\_MODE\_CREATIVE**</span></span>
</dt> <dd>

<span data-ttu-id="6866d-118">自動曝光模式，可嘗試最大化欄位的深度。</span><span class="sxs-lookup"><span data-stu-id="6866d-118">An automated exposure mode that tries to maximize the depth of field.</span></span>

</dd> <dt>

<span data-ttu-id="6866d-119"><span id="WPD_EXPOSURE_PROGRAM_MODE_ACTION"></span><span id="wpd_exposure_program_mode_action"></span>**WPD \_ 曝光 \_ 程式 \_ 模式 \_ 動作**</span><span class="sxs-lookup"><span data-stu-id="6866d-119"><span id="WPD_EXPOSURE_PROGRAM_MODE_ACTION"></span><span id="wpd_exposure_program_mode_action"></span>**WPD\_EXPOSURE\_PROGRAM\_MODE\_ACTION**</span></span>
</dt> <dd>

<span data-ttu-id="6866d-120">自動曝光模式，可嘗試最大化快門速度。</span><span class="sxs-lookup"><span data-stu-id="6866d-120">An automated exposure mode that tries to maximize the shutter speed.</span></span>

</dd> <dt>

<span data-ttu-id="6866d-121"><span id="WPD_EXPOSURE_PROGRAM_MODE_PORTRAIT"></span><span id="wpd_exposure_program_mode_portrait"></span>**WPD \_ 曝光 \_ 程式 \_ 模式 \_ 縱向**</span><span class="sxs-lookup"><span data-stu-id="6866d-121"><span id="WPD_EXPOSURE_PROGRAM_MODE_PORTRAIT"></span><span id="wpd_exposure_program_mode_portrait"></span>**WPD\_EXPOSURE\_PROGRAM\_MODE\_PORTRAIT**</span></span>
</dt> <dd>

<span data-ttu-id="6866d-122">指定相對淺之欄位深度的自動化曝光模式。</span><span class="sxs-lookup"><span data-stu-id="6866d-122">An automated exposure mode that specifies a relatively shallow depth of field.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="6866d-123">備註</span><span class="sxs-lookup"><span data-stu-id="6866d-123">Remarks</span></span>

<span data-ttu-id="6866d-124">指出裝置的曝光程式模式。</span><span class="sxs-lookup"><span data-stu-id="6866d-124">Indicates the exposure program mode of the device.</span></span> <span data-ttu-id="6866d-125">此列舉是由 [WPD 仍為 \_ \_ 影像 \_ 曝光 \_ 程式 \_ 模式](still-image-properties.md) 屬性所使用。</span><span class="sxs-lookup"><span data-stu-id="6866d-125">This enumeration is used by the [WPD\_STILL\_IMAGE\_EXPOSURE\_PROGRAM\_MODE](still-image-properties.md) property.</span></span>

## <a name="requirements"></a><span data-ttu-id="6866d-126">規格需求</span><span class="sxs-lookup"><span data-stu-id="6866d-126">Requirements</span></span>



| <span data-ttu-id="6866d-127">需求</span><span class="sxs-lookup"><span data-stu-id="6866d-127">Requirement</span></span> | <span data-ttu-id="6866d-128">值</span><span class="sxs-lookup"><span data-stu-id="6866d-128">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="6866d-129">標頭</span><span class="sxs-lookup"><span data-stu-id="6866d-129">Header</span></span><br/> | <dl> <span data-ttu-id="6866d-130"><dt>PortableDevice。h</dt></span><span class="sxs-lookup"><span data-stu-id="6866d-130"><dt>PortableDevice.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6866d-131">另請參閱</span><span class="sxs-lookup"><span data-stu-id="6866d-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6866d-132">**結構和列舉類型**</span><span class="sxs-lookup"><span data-stu-id="6866d-132">**Structures and Enumeration Types**</span></span>](structures-and-enumeration-types.md)
</dt> </dl>

 

 




