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
ms.openlocfilehash: d2419453beac6b493ddd1bbbe1281b1596ce00456599074b3872fecb003550c5
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119440758"
---
# <a name="wpd_stream_units-enumeration"></a>WPD \_ 串流 \_ 單位列舉

**WPD \_ 資料流程 \_ 單位** 列舉會指定要用於 [**IPortableDeviceUnitsStream**](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledeviceunitsstream)作業的單位類型。

## <a name="syntax"></a>Syntax


```C++
typedef enum _WPD_STREAM_UNITS { 
  WPD_STREAM_UNITS_BYTES         = 0,
  WPD_STREAM_UNITS_FRAMES        = 1,
  WPD_STREAM_UNITS_ROWS          = 2,
  WPD_STREAM_UNITS_MILLISECONDS  = 3,
  WPD_STREAM_UNITS_MICROSECONDS  = 4
} WPD_STREAM_UNITS;
```



## <a name="constants"></a>常數

<dl> <dt>

<span id="WPD_STREAM_UNITS_BYTES"></span><span id="wpd_stream_units_bytes"></span>**WPD \_ 資料流程 \_ 單位 \_ 位元組**
</dt> <dd>

資料流程單位是以位元組為單位來指定。

</dd> <dt>

<span id="WPD_STREAM_UNITS_FRAMES"></span><span id="wpd_stream_units_frames"></span>**WPD \_ 資料流程 \_ 單位 \_ 畫面格**
</dt> <dd>

資料流程單位是在框架中指定。

</dd> <dt>

<span id="WPD_STREAM_UNITS_ROWS"></span><span id="wpd_stream_units_rows"></span>**WPD \_ 資料流程 \_ 單位資料 \_ 列**
</dt> <dd>

資料流程單位是以資料列來指定。

</dd> <dt>

<span id="WPD_STREAM_UNITS_MILLISECONDS"></span><span id="wpd_stream_units_milliseconds"></span>**WPD \_ 資料流程 \_ 單位 \_ 毫秒**
</dt> <dd>

資料流程單位是以毫秒為單位來指定。

</dd> <dt>

<span id="WPD_STREAM_UNITS_MICROSECONDS"></span><span id="wpd_stream_units_microseconds"></span>**WPD \_ 資料流程 \_ 單位 \_ 微秒**
</dt> <dd>

資料流程單位是以微秒為單位來指定。

</dd> </dl>

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|--------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 8 \[僅限桌面應用程式\]<br/>                                                       |
| 最低支援的伺服器<br/> | 都不支援<br/>                                                                        |
| 標頭<br/>                   | <dl> <dt>PortableDeviceTypes。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**IPortableDeviceUnitsStream**](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledeviceunitsstream)
</dt> <dt>

[**IPortableDeviceUnitsStream::SeekInUnits**](/windows/desktop/api/PortableDeviceAPI/nf-portabledeviceapi-iportabledeviceunitsstream-seekinunits)
</dt> </dl>

 

 




