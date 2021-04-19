---
description: WPD \_ 焦點 \_ 計量 \_ 模式列舉類型會說明裝置應該如何決定要使用的框架部分來設定焦點。
ms.assetid: 0e68d0e8-2ce3-4994-99c2-2ff2293d8a20
title: 'WPD_FOCUS_METERING_MODES 列舉 (PortableDevice .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WPD_FOCUS_METERING_MODES
api_type:
- HeaderDef
api_location:
- PortableDevice.h
ms.openlocfilehash: f59d6a2f1cabbbe7b072a87caa3e5d74d012fc49
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106999257"
---
# <a name="wpd_focus_metering_modes-enumeration"></a><span data-ttu-id="da448-103">WPD \_ 焦點 \_ 計量 \_ 模式列舉</span><span class="sxs-lookup"><span data-stu-id="da448-103">WPD\_FOCUS\_METERING\_MODES enumeration</span></span>

<span data-ttu-id="da448-104">**WPD \_ 焦點 \_ 計量 \_ 模式** 列舉類型會說明裝置應該如何決定要使用的框架部分來設定焦點。</span><span class="sxs-lookup"><span data-stu-id="da448-104">The **WPD\_FOCUS\_METERING\_MODES** enumeration type describes how a device should decide what part of a frame to use to set focus.</span></span>

## <a name="syntax"></a><span data-ttu-id="da448-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="da448-105">Syntax</span></span>


```C++
typedef enum WPD_FOCUS_METERING_MODES { 
  WPD_FOCUS_METERING_MODE_UNDEFINED    = 0,
  WPD_FOCUS_METERING_MODE_CENTER_SPOT  = 1,
  WPD_FOCUS_METERING_MODE_MULTI_SPOT   = 2
} ;
```



## <a name="constants"></a><span data-ttu-id="da448-106">常數</span><span class="sxs-lookup"><span data-stu-id="da448-106">Constants</span></span>

<dl> <dt>

<span data-ttu-id="da448-107"><span id="WPD_FOCUS_METERING_MODE_UNDEFINED"></span><span id="wpd_focus_metering_mode_undefined"></span>**\_未定義 WPD 焦點 \_ 計量 \_ 模式 \_**</span><span class="sxs-lookup"><span data-stu-id="da448-107"><span id="WPD_FOCUS_METERING_MODE_UNDEFINED"></span><span id="wpd_focus_metering_mode_undefined"></span>**WPD\_FOCUS\_METERING\_MODE\_UNDEFINED**</span></span>
</dt> <dd>

<span data-ttu-id="da448-108">指出未指定任何焦點模式。</span><span class="sxs-lookup"><span data-stu-id="da448-108">Indicates that no focusing mode has been specified.</span></span>

</dd> <dt>

<span data-ttu-id="da448-109"><span id="WPD_FOCUS_METERING_MODE_CENTER_SPOT"></span><span id="wpd_focus_metering_mode_center_spot"></span>**WPD \_ 焦點 \_ 計量 \_ 模式 \_ 中心 \_ 點**</span><span class="sxs-lookup"><span data-stu-id="da448-109"><span id="WPD_FOCUS_METERING_MODE_CENTER_SPOT"></span><span id="wpd_focus_metering_mode_center_spot"></span>**WPD\_FOCUS\_METERING\_MODE\_CENTER\_SPOT**</span></span>
</dt> <dd>

<span data-ttu-id="da448-110">將焦點放在框架區域的中央。</span><span class="sxs-lookup"><span data-stu-id="da448-110">Focuses on the center of the framed area.</span></span>

</dd> <dt>

<span data-ttu-id="da448-111"><span id="WPD_FOCUS_METERING_MODE_MULTI_SPOT"></span><span id="wpd_focus_metering_mode_multi_spot"></span>**WPD \_ 焦點 \_ 計量 \_ 模式 \_ 多 \_ 點**</span><span class="sxs-lookup"><span data-stu-id="da448-111"><span id="WPD_FOCUS_METERING_MODE_MULTI_SPOT"></span><span id="wpd_focus_metering_mode_multi_spot"></span>**WPD\_FOCUS\_METERING\_MODE\_MULTI\_SPOT**</span></span>
</dt> <dd>

<span data-ttu-id="da448-112">藉由分析框架區域的多個部分來決定焦點。</span><span class="sxs-lookup"><span data-stu-id="da448-112">Determine focus by analyzing multiple parts of the framed area.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="da448-113">備註</span><span class="sxs-lookup"><span data-stu-id="da448-113">Remarks</span></span>

<span data-ttu-id="da448-114">此列舉是由 [ [WPD \_ 靜止 \_ 影像 \_ 焦點 \_ ] 計量 \_ 模式](still-image-properties.md) 屬性指定。</span><span class="sxs-lookup"><span data-stu-id="da448-114">This enumeration is specified by the [WPD\_STILL\_IMAGE\_FOCUS\_METERING\_MODE](still-image-properties.md) property.</span></span>

## <a name="requirements"></a><span data-ttu-id="da448-115">規格需求</span><span class="sxs-lookup"><span data-stu-id="da448-115">Requirements</span></span>



| <span data-ttu-id="da448-116">需求</span><span class="sxs-lookup"><span data-stu-id="da448-116">Requirement</span></span> | <span data-ttu-id="da448-117">值</span><span class="sxs-lookup"><span data-stu-id="da448-117">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="da448-118">標頭</span><span class="sxs-lookup"><span data-stu-id="da448-118">Header</span></span><br/> | <dl> <span data-ttu-id="da448-119"><dt>PortableDevice。h</dt></span><span class="sxs-lookup"><span data-stu-id="da448-119"><dt>PortableDevice.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="da448-120">另請參閱</span><span class="sxs-lookup"><span data-stu-id="da448-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="da448-121">**結構和列舉類型**</span><span class="sxs-lookup"><span data-stu-id="da448-121">**Structures and Enumeration Types**</span></span>](structures-and-enumeration-types.md)
</dt> </dl>

 

 




