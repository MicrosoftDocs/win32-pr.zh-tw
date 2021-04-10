---
description: WPD \_ 資料流程 \_ 單位列舉會指定要用於 IPortableDeviceUnitsStream 作業的單位類型。
ms.assetid: BE668696-7AF3-44AA-891A-9BFF67FB5544
title: 'WPD_STREAM_UNITS 列舉 (PortableDeviceTypes .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WPD_STREAM_UNITS
api_type:
- HeaderDef
api_location:
- PortableDeviceTypes.h
ms.openlocfilehash: 8e70455402a49673b574a0c696b6dda30cc6a884
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103694532"
---
# <a name="wpd_stream_units-enumeration"></a><span data-ttu-id="92a51-103">WPD \_ 串流 \_ 單位列舉</span><span class="sxs-lookup"><span data-stu-id="92a51-103">WPD\_STREAM\_UNITS enumeration</span></span>

<span data-ttu-id="92a51-104">**WPD \_ 資料流程 \_ 單位** 列舉會指定要用於 [**IPortableDeviceUnitsStream**](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledeviceunitsstream)作業的單位類型。</span><span class="sxs-lookup"><span data-stu-id="92a51-104">The **WPD\_STREAM\_UNITS** enumeration specifies the unit types to be used for [**IPortableDeviceUnitsStream**](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledeviceunitsstream) operations.</span></span>

## <a name="syntax"></a><span data-ttu-id="92a51-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="92a51-105">Syntax</span></span>


```C++
typedef enum _WPD_STREAM_UNITS { 
  WPD_STREAM_UNITS_BYTES         = 0,
  WPD_STREAM_UNITS_FRAMES        = 1,
  WPD_STREAM_UNITS_ROWS          = 2,
  WPD_STREAM_UNITS_MILLISECONDS  = 3,
  WPD_STREAM_UNITS_MICROSECONDS  = 4
} WPD_STREAM_UNITS;
```



## <a name="constants"></a><span data-ttu-id="92a51-106">常數</span><span class="sxs-lookup"><span data-stu-id="92a51-106">Constants</span></span>

<dl> <dt>

<span data-ttu-id="92a51-107"><span id="WPD_STREAM_UNITS_BYTES"></span><span id="wpd_stream_units_bytes"></span>**WPD \_ 資料流程 \_ 單位 \_ 位元組**</span><span class="sxs-lookup"><span data-stu-id="92a51-107"><span id="WPD_STREAM_UNITS_BYTES"></span><span id="wpd_stream_units_bytes"></span>**WPD\_STREAM\_UNITS\_BYTES**</span></span>
</dt> <dd>

<span data-ttu-id="92a51-108">資料流程單位是以位元組為單位來指定。</span><span class="sxs-lookup"><span data-stu-id="92a51-108">The stream units are specified in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="92a51-109"><span id="WPD_STREAM_UNITS_FRAMES"></span><span id="wpd_stream_units_frames"></span>**WPD \_ 資料流程 \_ 單位 \_ 畫面格**</span><span class="sxs-lookup"><span data-stu-id="92a51-109"><span id="WPD_STREAM_UNITS_FRAMES"></span><span id="wpd_stream_units_frames"></span>**WPD\_STREAM\_UNITS\_FRAMES**</span></span>
</dt> <dd>

<span data-ttu-id="92a51-110">資料流程單位是在框架中指定。</span><span class="sxs-lookup"><span data-stu-id="92a51-110">The stream units are specified in frames.</span></span>

</dd> <dt>

<span data-ttu-id="92a51-111"><span id="WPD_STREAM_UNITS_ROWS"></span><span id="wpd_stream_units_rows"></span>**WPD \_ 資料流程 \_ 單位資料 \_ 列**</span><span class="sxs-lookup"><span data-stu-id="92a51-111"><span id="WPD_STREAM_UNITS_ROWS"></span><span id="wpd_stream_units_rows"></span>**WPD\_STREAM\_UNITS\_ROWS**</span></span>
</dt> <dd>

<span data-ttu-id="92a51-112">資料流程單位是以資料列來指定。</span><span class="sxs-lookup"><span data-stu-id="92a51-112">The stream units are specified in rows.</span></span>

</dd> <dt>

<span data-ttu-id="92a51-113"><span id="WPD_STREAM_UNITS_MILLISECONDS"></span><span id="wpd_stream_units_milliseconds"></span>**WPD \_ 資料流程 \_ 單位 \_ 毫秒**</span><span class="sxs-lookup"><span data-stu-id="92a51-113"><span id="WPD_STREAM_UNITS_MILLISECONDS"></span><span id="wpd_stream_units_milliseconds"></span>**WPD\_STREAM\_UNITS\_MILLISECONDS**</span></span>
</dt> <dd>

<span data-ttu-id="92a51-114">資料流程單位是以毫秒為單位來指定。</span><span class="sxs-lookup"><span data-stu-id="92a51-114">The stream units are specified in milliseconds.</span></span>

</dd> <dt>

<span data-ttu-id="92a51-115"><span id="WPD_STREAM_UNITS_MICROSECONDS"></span><span id="wpd_stream_units_microseconds"></span>**WPD \_ 資料流程 \_ 單位 \_ 微秒**</span><span class="sxs-lookup"><span data-stu-id="92a51-115"><span id="WPD_STREAM_UNITS_MICROSECONDS"></span><span id="wpd_stream_units_microseconds"></span>**WPD\_STREAM\_UNITS\_MICROSECONDS**</span></span>
</dt> <dd>

<span data-ttu-id="92a51-116">資料流程單位是以微秒為單位來指定。</span><span class="sxs-lookup"><span data-stu-id="92a51-116">The stream units are specified in microseconds.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="92a51-117">規格需求</span><span class="sxs-lookup"><span data-stu-id="92a51-117">Requirements</span></span>



| <span data-ttu-id="92a51-118">需求</span><span class="sxs-lookup"><span data-stu-id="92a51-118">Requirement</span></span> | <span data-ttu-id="92a51-119">值</span><span class="sxs-lookup"><span data-stu-id="92a51-119">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------------|
| <span data-ttu-id="92a51-120">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="92a51-120">Minimum supported client</span></span><br/> | <span data-ttu-id="92a51-121">\[僅 Windows 8 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="92a51-121">Windows 8 \[desktop apps only\]</span></span><br/>                                                       |
| <span data-ttu-id="92a51-122">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="92a51-122">Minimum supported server</span></span><br/> | <span data-ttu-id="92a51-123">都不支援</span><span class="sxs-lookup"><span data-stu-id="92a51-123">None supported</span></span><br/>                                                                        |
| <span data-ttu-id="92a51-124">標頭</span><span class="sxs-lookup"><span data-stu-id="92a51-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="92a51-125"><dt>PortableDeviceTypes。h</dt></span><span class="sxs-lookup"><span data-stu-id="92a51-125"><dt>PortableDeviceTypes.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="92a51-126">另請參閱</span><span class="sxs-lookup"><span data-stu-id="92a51-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="92a51-127">**IPortableDeviceUnitsStream**</span><span class="sxs-lookup"><span data-stu-id="92a51-127">**IPortableDeviceUnitsStream**</span></span>](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledeviceunitsstream)
</dt> <dt>

[<span data-ttu-id="92a51-128">**IPortableDeviceUnitsStream::SeekInUnits**</span><span class="sxs-lookup"><span data-stu-id="92a51-128">**IPortableDeviceUnitsStream::SeekInUnits**</span></span>](/windows/desktop/api/PortableDeviceAPI/nf-portabledeviceapi-iportabledeviceunitsstream-seekinunits)
</dt> </dl>

 

 




