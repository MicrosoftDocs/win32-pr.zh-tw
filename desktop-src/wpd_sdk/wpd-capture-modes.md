---
description: WPD \_ CAPTURE \_ 模式列舉型別描述靜止影像捕捉的「捕捉計時模式」。
ms.assetid: bfe96176-d018-4b39-a938-035757111784
title: 'WPD_CAPTURE_MODES 列舉 (PortableDevice .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WPD_CAPTURE_MODES
api_type:
- HeaderDef
api_location:
- PortableDevice.h
ms.openlocfilehash: e56e3e66cd20abaeb1daf0a674633a36b57a9575
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106984007"
---
# <a name="wpd_capture_modes-enumeration"></a><span data-ttu-id="c1e89-103">WPD \_ CAPTURE \_ 模式列舉</span><span class="sxs-lookup"><span data-stu-id="c1e89-103">WPD\_CAPTURE\_MODES enumeration</span></span>

<span data-ttu-id="c1e89-104">**WPD \_ CAPTURE \_ 模式** 列舉型別描述靜止影像捕捉的「捕捉計時模式」。</span><span class="sxs-lookup"><span data-stu-id="c1e89-104">The **WPD\_CAPTURE\_MODES** enumeration type describes the capture timing mode of a still image capture.</span></span>

## <a name="syntax"></a><span data-ttu-id="c1e89-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="c1e89-105">Syntax</span></span>


```C++
typedef enum WPD_CAPTURE_MODES { 
  WPD_CAPTURE_MODE_UNDEFINED  = 0,
  WPD_CAPTURE_MODE_NORMAL     = 1,
  WPD_CAPTURE_MODE_BURST      = 2,
  WPD_CAPTURE_MODE_TIMELAPSE  = 3
} ;
```



## <a name="constants"></a><span data-ttu-id="c1e89-106">常數</span><span class="sxs-lookup"><span data-stu-id="c1e89-106">Constants</span></span>

<dl> <dt>

<span data-ttu-id="c1e89-107"><span id="WPD_CAPTURE_MODE_UNDEFINED"></span><span id="wpd_capture_mode_undefined"></span>**WPD \_ 捕捉 \_ 模式 \_ 未定義**</span><span class="sxs-lookup"><span data-stu-id="c1e89-107"><span id="WPD_CAPTURE_MODE_UNDEFINED"></span><span id="wpd_capture_mode_undefined"></span>**WPD\_CAPTURE\_MODE\_UNDEFINED**</span></span>
</dt> <dd>

<span data-ttu-id="c1e89-108">尚未定義 capture 模式。</span><span class="sxs-lookup"><span data-stu-id="c1e89-108">The capture mode has not been defined.</span></span>

</dd> <dt>

<span data-ttu-id="c1e89-109"><span id="WPD_CAPTURE_MODE_NORMAL"></span><span id="wpd_capture_mode_normal"></span>**WPD \_ CAPTURE \_ 模式 \_ 正常**</span><span class="sxs-lookup"><span data-stu-id="c1e89-109"><span id="WPD_CAPTURE_MODE_NORMAL"></span><span id="wpd_capture_mode_normal"></span>**WPD\_CAPTURE\_MODE\_NORMAL**</span></span>
</dt> <dd>

<span data-ttu-id="c1e89-110">不應使用延遲或高載模式。</span><span class="sxs-lookup"><span data-stu-id="c1e89-110">No delay or burst mode should be used.</span></span>

</dd> <dt>

<span data-ttu-id="c1e89-111"><span id="WPD_CAPTURE_MODE_BURST"></span><span id="wpd_capture_mode_burst"></span>**WPD \_ CAPTURE \_ 模式高載 \_**</span><span class="sxs-lookup"><span data-stu-id="c1e89-111"><span id="WPD_CAPTURE_MODE_BURST"></span><span id="wpd_capture_mode_burst"></span>**WPD\_CAPTURE\_MODE\_BURST**</span></span>
</dt> <dd>

<span data-ttu-id="c1e89-112">指定應以定義的間隔來捕捉定義的影像數目。</span><span class="sxs-lookup"><span data-stu-id="c1e89-112">Specifies that a defined number of images should be captured with a defined interval between them.</span></span> <span data-ttu-id="c1e89-113">要捕捉的映射數目以及兩者之間的時間延遲，是由 [WPD \_ 仍為 \_ 影像 \_ \_ ](still-image-properties.md) 高載數目和 [WPD 仍為影像高載 \_ \_ \_ \_ 間隔](still-image-properties.md) 屬性所指定。</span><span class="sxs-lookup"><span data-stu-id="c1e89-113">The number of images to capture and time delay between them are specified by the [WPD\_STILL\_IMAGE\_BURST\_NUMBER](still-image-properties.md) and [WPD\_STILL\_IMAGE\_BURST\_INTERVAL](still-image-properties.md) properties.</span></span>

</dd> <dt>

<span data-ttu-id="c1e89-114"><span id="WPD_CAPTURE_MODE_TIMELAPSE"></span><span id="wpd_capture_mode_timelapse"></span>**WPD \_ CAPTURE \_ 模式 \_ TIMELAPSE**</span><span class="sxs-lookup"><span data-stu-id="c1e89-114"><span id="WPD_CAPTURE_MODE_TIMELAPSE"></span><span id="wpd_capture_mode_timelapse"></span>**WPD\_CAPTURE\_MODE\_TIMELAPSE**</span></span>
</dt> <dd>

<span data-ttu-id="c1e89-115">影像捕捉應使用時間間隔攝影。</span><span class="sxs-lookup"><span data-stu-id="c1e89-115">Image capture should use time lapse photography.</span></span> <span data-ttu-id="c1e89-116">[WPD \_ 仍 \_ 影像 \_ TIMELAPSE \_ 號碼](still-image-properties.md)和[WPD \_ 仍是 \_ 影像 \_ TIMELAPSE \_ 間隔](still-image-properties.md)屬性描述的影像和間隔數目。</span><span class="sxs-lookup"><span data-stu-id="c1e89-116">The number of images and interval between them are described by the [WPD\_STILL\_IMAGE\_TIMELAPSE\_NUMBER](still-image-properties.md) and [WPD\_STILL\_IMAGE\_TIMELAPSE\_INTERVAL](still-image-properties.md) properties.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="c1e89-117">備註</span><span class="sxs-lookup"><span data-stu-id="c1e89-117">Remarks</span></span>

<span data-ttu-id="c1e89-118">[WPD \_ 仍然是 \_ 影像 \_ 捕捉 \_ 模式](still-image-properties.md)屬性使用此列舉。</span><span class="sxs-lookup"><span data-stu-id="c1e89-118">This enumeration is used by the [WPD\_STILL\_IMAGE\_CAPTURE\_MODE](still-image-properties.md) property.</span></span>

## <a name="requirements"></a><span data-ttu-id="c1e89-119">規格需求</span><span class="sxs-lookup"><span data-stu-id="c1e89-119">Requirements</span></span>



| <span data-ttu-id="c1e89-120">需求</span><span class="sxs-lookup"><span data-stu-id="c1e89-120">Requirement</span></span> | <span data-ttu-id="c1e89-121">值</span><span class="sxs-lookup"><span data-stu-id="c1e89-121">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="c1e89-122">標頭</span><span class="sxs-lookup"><span data-stu-id="c1e89-122">Header</span></span><br/> | <dl> <span data-ttu-id="c1e89-123"><dt>PortableDevice。h</dt></span><span class="sxs-lookup"><span data-stu-id="c1e89-123"><dt>PortableDevice.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c1e89-124">另請參閱</span><span class="sxs-lookup"><span data-stu-id="c1e89-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c1e89-125">**WPD 屬性和屬性**</span><span class="sxs-lookup"><span data-stu-id="c1e89-125">**WPD Properties and Attributes**</span></span>](properties-and-attributes.md)
</dt> <dt>

[<span data-ttu-id="c1e89-126">**結構和列舉類型**</span><span class="sxs-lookup"><span data-stu-id="c1e89-126">**Structures and Enumeration Types**</span></span>](structures-and-enumeration-types.md)
</dt> </dl>

 

 




