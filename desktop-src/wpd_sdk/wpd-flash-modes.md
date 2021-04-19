---
description: WPD \_ FLASH \_ 模式列舉類型描述使用裝置來捕捉映射時，所要使用的閃爍模式。
ms.assetid: 4e92c86d-2f35-4bc6-8d37-ec1ab5c518b2
title: 'WPD_FLASH_MODES 列舉 (PortableDevice .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WPD_FLASH_MODES
api_type:
- HeaderDef
api_location:
- PortableDevice.h
ms.openlocfilehash: 09a2a5b95e86d9d17267cafcfbf723e734ffc74f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106977552"
---
# <a name="wpd_flash_modes-enumeration"></a><span data-ttu-id="08e1e-103">WPD \_ FLASH \_ 模式列舉</span><span class="sxs-lookup"><span data-stu-id="08e1e-103">WPD\_FLASH\_MODES enumeration</span></span>

<span data-ttu-id="08e1e-104">**WPD \_ FLASH \_ 模式** 列舉類型描述使用裝置來捕捉映射時，所要使用的閃爍模式。</span><span class="sxs-lookup"><span data-stu-id="08e1e-104">The **WPD\_FLASH\_MODES** enumeration type describes a flash mode to use when capturing images with a device.</span></span>

## <a name="syntax"></a><span data-ttu-id="08e1e-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="08e1e-105">Syntax</span></span>


```C++
typedef enum WPD_FLASH_MODES { 
  WPD_FLASH_MODE_UNDEFINED      = 0,
  WPD_FLASH_MODE_AUTO           = 1,
  WPD_FLASH_MODE_OFF            = 2,
  WPD_FLASH_MODE_FILL           = 3,
  WPD_FLASH_MODE_RED_EYE_AUTO   = 4,
  WPD_FLASH_MODE_RED_EYE_FILL   = 5,
  WPD_FLASH_MODE_EXTERNAL_SYNC  = 6
} ;
```



## <a name="constants"></a><span data-ttu-id="08e1e-106">常數</span><span class="sxs-lookup"><span data-stu-id="08e1e-106">Constants</span></span>

<dl> <dt>

<span data-ttu-id="08e1e-107"><span id="WPD_FLASH_MODE_UNDEFINED"></span><span id="wpd_flash_mode_undefined"></span>**\_ \_ 未定義 WPD 閃光燈模式 \_**</span><span class="sxs-lookup"><span data-stu-id="08e1e-107"><span id="WPD_FLASH_MODE_UNDEFINED"></span><span id="wpd_flash_mode_undefined"></span>**WPD\_FLASH\_MODE\_UNDEFINED**</span></span>
</dt> <dd>

<span data-ttu-id="08e1e-108">未指定任何閃爍模式。</span><span class="sxs-lookup"><span data-stu-id="08e1e-108">No flash mode has been specified.</span></span>

</dd> <dt>

<span data-ttu-id="08e1e-109"><span id="WPD_FLASH_MODE_AUTO"></span><span id="wpd_flash_mode_auto"></span>**\_自動 WPD 閃光燈 \_ 模式 \_**</span><span class="sxs-lookup"><span data-stu-id="08e1e-109"><span id="WPD_FLASH_MODE_AUTO"></span><span id="wpd_flash_mode_auto"></span>**WPD\_FLASH\_MODE\_AUTO**</span></span>
</dt> <dd>

<span data-ttu-id="08e1e-110">指定應在自動模式中使用 flash （如裝置所指定）。</span><span class="sxs-lookup"><span data-stu-id="08e1e-110">Specifies that the flash should be used in the automatic mode, as specified by the device.</span></span>

</dd> <dt>

<span data-ttu-id="08e1e-111"><span id="WPD_FLASH_MODE_OFF"></span><span id="wpd_flash_mode_off"></span>**WPD \_ 閃光燈 \_ 模式 \_ 關閉**</span><span class="sxs-lookup"><span data-stu-id="08e1e-111"><span id="WPD_FLASH_MODE_OFF"></span><span id="wpd_flash_mode_off"></span>**WPD\_FLASH\_MODE\_OFF**</span></span>
</dt> <dd>

<span data-ttu-id="08e1e-112">指定不應使用任何 flash。</span><span class="sxs-lookup"><span data-stu-id="08e1e-112">Specifies that no flash should be used.</span></span>

</dd> <dt>

<span data-ttu-id="08e1e-113"><span id="WPD_FLASH_MODE_FILL"></span><span id="wpd_flash_mode_fill"></span>**WPD \_ 閃光燈 \_ 模式 \_ 填滿**</span><span class="sxs-lookup"><span data-stu-id="08e1e-113"><span id="WPD_FLASH_MODE_FILL"></span><span id="wpd_flash_mode_fill"></span>**WPD\_FLASH\_MODE\_FILL**</span></span>
</dt> <dd>

<span data-ttu-id="08e1e-114">指定填滿型別 flash。</span><span class="sxs-lookup"><span data-stu-id="08e1e-114">Specifies a fill-type flash.</span></span>

</dd> <dt>

<span data-ttu-id="08e1e-115"><span id="WPD_FLASH_MODE_RED_EYE_AUTO"></span><span id="wpd_flash_mode_red_eye_auto"></span>**\_自動 WPD 閃光燈 \_ 模式的 \_ \_ 紅眼 \_**</span><span class="sxs-lookup"><span data-stu-id="08e1e-115"><span id="WPD_FLASH_MODE_RED_EYE_AUTO"></span><span id="wpd_flash_mode_red_eye_auto"></span>**WPD\_FLASH\_MODE\_RED\_EYE\_AUTO**</span></span>
</dt> <dd>

<span data-ttu-id="08e1e-116">指定應該使用紅眼降低 flash。</span><span class="sxs-lookup"><span data-stu-id="08e1e-116">Specifies that the red eye reduction flash should be used.</span></span>

</dd> <dt>

<span data-ttu-id="08e1e-117"><span id="WPD_FLASH_MODE_RED_EYE_FILL"></span><span id="wpd_flash_mode_red_eye_fill"></span>**WPD \_ 閃光燈 \_ 模式的紅眼 \_ \_ \_ 填滿**</span><span class="sxs-lookup"><span data-stu-id="08e1e-117"><span id="WPD_FLASH_MODE_RED_EYE_FILL"></span><span id="wpd_flash_mode_red_eye_fill"></span>**WPD\_FLASH\_MODE\_RED\_EYE\_FILL**</span></span>
</dt> <dd>

<span data-ttu-id="08e1e-118">指定應該使用 red 眼睛填滿 flash。</span><span class="sxs-lookup"><span data-stu-id="08e1e-118">Specifies that the red eye fill flash should be used.</span></span>

</dd> <dt>

<span data-ttu-id="08e1e-119"><span id="WPD_FLASH_MODE_EXTERNAL_SYNC"></span><span id="wpd_flash_mode_external_sync"></span>**WPD \_ FLASH \_ 模式 \_ 外部 \_ 同步處理**</span><span class="sxs-lookup"><span data-stu-id="08e1e-119"><span id="WPD_FLASH_MODE_EXTERNAL_SYNC"></span><span id="wpd_flash_mode_external_sync"></span>**WPD\_FLASH\_MODE\_EXTERNAL\_SYNC**</span></span>
</dt> <dd>

<span data-ttu-id="08e1e-120">指定應該與其他外部 flash 裝置同步 flash。</span><span class="sxs-lookup"><span data-stu-id="08e1e-120">Specifies that the flash should be synchronized with other external flash devices.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="08e1e-121">備註</span><span class="sxs-lookup"><span data-stu-id="08e1e-121">Remarks</span></span>

<span data-ttu-id="08e1e-122">[WPD \_ 仍然是 \_ IMAGE \_ FLASH \_ 模式](still-image-properties.md)屬性使用此列舉。</span><span class="sxs-lookup"><span data-stu-id="08e1e-122">This enumeration is used by the [WPD\_STILL\_IMAGE\_FLASH\_MODE](still-image-properties.md) property.</span></span>

## <a name="requirements"></a><span data-ttu-id="08e1e-123">規格需求</span><span class="sxs-lookup"><span data-stu-id="08e1e-123">Requirements</span></span>



| <span data-ttu-id="08e1e-124">需求</span><span class="sxs-lookup"><span data-stu-id="08e1e-124">Requirement</span></span> | <span data-ttu-id="08e1e-125">值</span><span class="sxs-lookup"><span data-stu-id="08e1e-125">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="08e1e-126">標頭</span><span class="sxs-lookup"><span data-stu-id="08e1e-126">Header</span></span><br/> | <dl> <span data-ttu-id="08e1e-127"><dt>PortableDevice。h</dt></span><span class="sxs-lookup"><span data-stu-id="08e1e-127"><dt>PortableDevice.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="08e1e-128">另請參閱</span><span class="sxs-lookup"><span data-stu-id="08e1e-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="08e1e-129">**結構和列舉類型**</span><span class="sxs-lookup"><span data-stu-id="08e1e-129">**Structures and Enumeration Types**</span></span>](structures-and-enumeration-types.md)
</dt> </dl>

 

 




