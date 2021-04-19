---
description: WPD \_ 效果 \_ 模式列舉型別描述可套用至影像的各種視覺效果。
ms.assetid: 7624fccb-e416-4db4-978e-410c4c236328
title: 'WPD_EFFECT_MODES 列舉 (PortableDevice .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WPD_EFFECT_MODES
api_type:
- HeaderDef
api_location:
- PortableDevice.h
ms.openlocfilehash: 7e29f89207a74d335fbe1c2561f8dcf9cec3e923
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106993947"
---
# <a name="wpd_effect_modes-enumeration"></a><span data-ttu-id="c03c8-103">WPD \_ 效果 \_ 模式列舉</span><span class="sxs-lookup"><span data-stu-id="c03c8-103">WPD\_EFFECT\_MODES enumeration</span></span>

<span data-ttu-id="c03c8-104">**WPD \_ 效果 \_ 模式** 列舉型別描述可套用至影像的各種視覺效果。</span><span class="sxs-lookup"><span data-stu-id="c03c8-104">The **WPD\_EFFECT\_MODES** enumeration type describes various visual effects that can be applied to an image.</span></span>

## <a name="syntax"></a><span data-ttu-id="c03c8-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="c03c8-105">Syntax</span></span>


```C++
typedef enum WPD_EFFECT_MODES { 
  WPD_EFFECT_MODE_UNDEFINED        = 0,
  WPD_EFFECT_MODE_COLOR            = 1,
  WPD_EFFECT_MODE_BLACK_AND_WHITE  = 2,
  WPD_EFFECT_MODE_SEPIA            = 3
} ;
```



## <a name="constants"></a><span data-ttu-id="c03c8-106">常數</span><span class="sxs-lookup"><span data-stu-id="c03c8-106">Constants</span></span>

<dl> <dt>

<span data-ttu-id="c03c8-107"><span id="WPD_EFFECT_MODE_UNDEFINED"></span><span id="wpd_effect_mode_undefined"></span>**\_ \_ 未定義 WPD 效果模式 \_**</span><span class="sxs-lookup"><span data-stu-id="c03c8-107"><span id="WPD_EFFECT_MODE_UNDEFINED"></span><span id="wpd_effect_mode_undefined"></span>**WPD\_EFFECT\_MODE\_UNDEFINED**</span></span>
</dt> <dd>

<span data-ttu-id="c03c8-108">未指定任何效果。</span><span class="sxs-lookup"><span data-stu-id="c03c8-108">No effect has been specified.</span></span>

</dd> <dt>

<span data-ttu-id="c03c8-109"><span id="WPD_EFFECT_MODE_COLOR"></span><span id="wpd_effect_mode_color"></span>**WPD \_ 效果 \_ 模式 \_ 色彩**</span><span class="sxs-lookup"><span data-stu-id="c03c8-109"><span id="WPD_EFFECT_MODE_COLOR"></span><span id="wpd_effect_mode_color"></span>**WPD\_EFFECT\_MODE\_COLOR**</span></span>
</dt> <dd>

<span data-ttu-id="c03c8-110">影像應該為色彩。</span><span class="sxs-lookup"><span data-stu-id="c03c8-110">The image should be color.</span></span>

</dd> <dt>

<span data-ttu-id="c03c8-111"><span id="WPD_EFFECT_MODE_BLACK_AND_WHITE"></span><span id="wpd_effect_mode_black_and_white"></span>**WPD \_ 效果 \_ 模式 \_ 黑色 \_ 和 \_ 白色**</span><span class="sxs-lookup"><span data-stu-id="c03c8-111"><span id="WPD_EFFECT_MODE_BLACK_AND_WHITE"></span><span id="wpd_effect_mode_black_and_white"></span>**WPD\_EFFECT\_MODE\_BLACK\_AND\_WHITE**</span></span>
</dt> <dd>

<span data-ttu-id="c03c8-112">影像應該是黑色和白色。</span><span class="sxs-lookup"><span data-stu-id="c03c8-112">The image should be black and white.</span></span>

</dd> <dt>

<span data-ttu-id="c03c8-113"><span id="WPD_EFFECT_MODE_SEPIA"></span><span id="wpd_effect_mode_sepia"></span>**WPD \_ 效果 \_ 模式 \_ 棕褐色**</span><span class="sxs-lookup"><span data-stu-id="c03c8-113"><span id="WPD_EFFECT_MODE_SEPIA"></span><span id="wpd_effect_mode_sepia"></span>**WPD\_EFFECT\_MODE\_SEPIA**</span></span>
</dt> <dd>

<span data-ttu-id="c03c8-114">影像應該是棕褐色。</span><span class="sxs-lookup"><span data-stu-id="c03c8-114">The image should be sepia.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="c03c8-115">備註</span><span class="sxs-lookup"><span data-stu-id="c03c8-115">Remarks</span></span>

<span data-ttu-id="c03c8-116">此列舉是由 [ [WPD \_ 仍然 \_ 影像 \_ 效果 \_ 模式]](still-image-properties.md) 屬性所使用。</span><span class="sxs-lookup"><span data-stu-id="c03c8-116">This enumeration is used by the [WPD\_STILL\_IMAGE\_EFFECT\_MODE](still-image-properties.md) property.</span></span>

## <a name="requirements"></a><span data-ttu-id="c03c8-117">規格需求</span><span class="sxs-lookup"><span data-stu-id="c03c8-117">Requirements</span></span>



| <span data-ttu-id="c03c8-118">需求</span><span class="sxs-lookup"><span data-stu-id="c03c8-118">Requirement</span></span> | <span data-ttu-id="c03c8-119">值</span><span class="sxs-lookup"><span data-stu-id="c03c8-119">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="c03c8-120">標頭</span><span class="sxs-lookup"><span data-stu-id="c03c8-120">Header</span></span><br/> | <dl> <span data-ttu-id="c03c8-121"><dt>PortableDevice。h</dt></span><span class="sxs-lookup"><span data-stu-id="c03c8-121"><dt>PortableDevice.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c03c8-122">另請參閱</span><span class="sxs-lookup"><span data-stu-id="c03c8-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c03c8-123">**結構和列舉類型**</span><span class="sxs-lookup"><span data-stu-id="c03c8-123">**Structures and Enumeration Types**</span></span>](structures-and-enumeration-types.md)
</dt> </dl>

 

 




