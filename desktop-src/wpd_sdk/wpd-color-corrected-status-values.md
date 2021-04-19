---
description: WPD \_ 色彩 \_ 更正的 \_ 狀態值 \_ 列舉類型描述影像或影片檔案的色彩更正狀態。
ms.assetid: af129a1b-7760-4339-adf7-3f3c17cebde2
title: 'WPD_COLOR_CORRECTED_STATUS_VALUES 列舉 (PortableDevice .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WPD_COLOR_CORRECTED_STATUS_VALUES
api_type:
- HeaderDef
api_location:
- PortableDevice.h
ms.openlocfilehash: ec6bfcaa3933bb70c3064f829e701509e3ff32f7
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106981650"
---
# <a name="wpd_color_corrected_status_values-enumeration"></a><span data-ttu-id="fdd59-103">WPD \_ 色彩 \_ 更正的 \_ 狀態值 \_ 列舉</span><span class="sxs-lookup"><span data-stu-id="fdd59-103">WPD\_COLOR\_CORRECTED\_STATUS\_VALUES enumeration</span></span>

<span data-ttu-id="fdd59-104">**WPD \_ 色彩更正 \_ 的 \_ 狀態值 \_** 列舉類型描述影像或影片檔案的色彩更正狀態。</span><span class="sxs-lookup"><span data-stu-id="fdd59-104">The **WPD\_COLOR\_CORRECTED\_STATUS\_VALUES** enumeration type describes the color correction status of an image or video file.</span></span>

## <a name="syntax"></a><span data-ttu-id="fdd59-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="fdd59-105">Syntax</span></span>


```C++
typedef enum WPD_COLOR_CORRECTED_STATUS_VALUES { 
  WPD_COLOR_CORRECTED_STATUS_NOT_CORRECTED            = 0,
  WPD_COLOR_CORRECTED_STATUS_CORRECTED                = 1,
  WPD_COLOR_CORRECTED_STATUS_SHOULD_NOT_BE_CORRECTED  = 2
} ;
```



## <a name="constants"></a><span data-ttu-id="fdd59-106">常數</span><span class="sxs-lookup"><span data-stu-id="fdd59-106">Constants</span></span>

<dl> <dt>

<span data-ttu-id="fdd59-107"><span id="WPD_COLOR_CORRECTED_STATUS_NOT_CORRECTED"></span><span id="wpd_color_corrected_status_not_corrected"></span>**\_ \_ \_ \_ 未更正 WPD 色彩更正 \_ 狀態**</span><span class="sxs-lookup"><span data-stu-id="fdd59-107"><span id="WPD_COLOR_CORRECTED_STATUS_NOT_CORRECTED"></span><span id="wpd_color_corrected_status_not_corrected"></span>**WPD\_COLOR\_CORRECTED\_STATUS\_NOT\_CORRECTED**</span></span>
</dt> <dd>

<span data-ttu-id="fdd59-108">尚未校正影像的色彩。</span><span class="sxs-lookup"><span data-stu-id="fdd59-108">The image has not been color corrected.</span></span>

</dd> <dt>

<span data-ttu-id="fdd59-109"><span id="WPD_COLOR_CORRECTED_STATUS_CORRECTED"></span><span id="wpd_color_corrected_status_corrected"></span>**已 \_ 更正 WPD 色彩 \_ 更正 \_ 狀態 \_**</span><span class="sxs-lookup"><span data-stu-id="fdd59-109"><span id="WPD_COLOR_CORRECTED_STATUS_CORRECTED"></span><span id="wpd_color_corrected_status_corrected"></span>**WPD\_COLOR\_CORRECTED\_STATUS\_CORRECTED**</span></span>
</dt> <dd>

<span data-ttu-id="fdd59-110">影像已經過色彩校正。</span><span class="sxs-lookup"><span data-stu-id="fdd59-110">The image has been color corrected.</span></span>

</dd> <dt>

<span data-ttu-id="fdd59-111"><span id="WPD_COLOR_CORRECTED_STATUS_SHOULD_NOT_BE_CORRECTED"></span><span id="wpd_color_corrected_status_should_not_be_corrected"></span>**\_ \_ \_ \_ \_ 不應 \_ \_ 更正 WPD 色彩更正狀態**</span><span class="sxs-lookup"><span data-stu-id="fdd59-111"><span id="WPD_COLOR_CORRECTED_STATUS_SHOULD_NOT_BE_CORRECTED"></span><span id="wpd_color_corrected_status_should_not_be_corrected"></span>**WPD\_COLOR\_CORRECTED\_STATUS\_SHOULD\_NOT\_BE\_CORRECTED**</span></span>
</dt> <dd>

<span data-ttu-id="fdd59-112">影像尚未經過修正，因此不應校正色彩。</span><span class="sxs-lookup"><span data-stu-id="fdd59-112">The image has not been, and should not be, color corrected.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="fdd59-113">備註</span><span class="sxs-lookup"><span data-stu-id="fdd59-113">Remarks</span></span>

<span data-ttu-id="fdd59-114">指出影像的色彩更正狀態。</span><span class="sxs-lookup"><span data-stu-id="fdd59-114">Indicates the color corrected status of an image.</span></span> <span data-ttu-id="fdd59-115">此列舉是由 [WPD \_ IMAGE \_ COLOR \_ 校正 \_ STATUS](image-properties.md) 屬性所使用。</span><span class="sxs-lookup"><span data-stu-id="fdd59-115">This enumeration is used by the [WPD\_IMAGE\_COLOR\_CORRECTED\_STATUS](image-properties.md) property.</span></span>

## <a name="requirements"></a><span data-ttu-id="fdd59-116">規格需求</span><span class="sxs-lookup"><span data-stu-id="fdd59-116">Requirements</span></span>



| <span data-ttu-id="fdd59-117">需求</span><span class="sxs-lookup"><span data-stu-id="fdd59-117">Requirement</span></span> | <span data-ttu-id="fdd59-118">值</span><span class="sxs-lookup"><span data-stu-id="fdd59-118">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="fdd59-119">標頭</span><span class="sxs-lookup"><span data-stu-id="fdd59-119">Header</span></span><br/> | <dl> <span data-ttu-id="fdd59-120"><dt>PortableDevice。h</dt></span><span class="sxs-lookup"><span data-stu-id="fdd59-120"><dt>PortableDevice.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fdd59-121">另請參閱</span><span class="sxs-lookup"><span data-stu-id="fdd59-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fdd59-122">**結構和列舉類型**</span><span class="sxs-lookup"><span data-stu-id="fdd59-122">**Structures and Enumeration Types**</span></span>](structures-and-enumeration-types.md)
</dt> </dl>

 

 




