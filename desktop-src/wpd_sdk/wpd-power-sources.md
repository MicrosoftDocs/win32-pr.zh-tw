---
description: WPD \_ 電源 \_ 來源列舉類型會描述裝置使用的電源來源。
ms.assetid: feebf213-052d-4315-84db-2109cab5f179
title: 'WPD_POWER_SOURCES 列舉 (PortableDevice .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WPD_POWER_SOURCES
api_type:
- HeaderDef
api_location:
- PortableDevice.h
ms.openlocfilehash: bf9a153d4d41a64b639f796ea2ba0eeb9e567a32
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106987024"
---
# <a name="wpd_power_sources-enumeration"></a>WPD \_ 電源 \_ 來源列舉

**WPD \_ 電源 \_ 來源** 列舉類型會描述裝置使用的電源來源。

## <a name="syntax"></a>Syntax


```C++
typedef enum WPD_POWER_SOURCES { 
  WPD_POWER_SOURCE_BATTERY   = 0,
  WPD_POWER_SOURCE_EXTERNAL  = 1
} ;
```



## <a name="constants"></a>常數

<dl> <dt>

<span id="WPD_POWER_SOURCE_BATTERY"></span><span id="wpd_power_source_battery"></span>**WPD \_ 電源 \_ 來源 \_ 電池**
</dt> <dd>

裝置電源來源為電池。

</dd> <dt>

<span id="WPD_POWER_SOURCE_EXTERNAL"></span><span id="wpd_power_source_external"></span>**WPD \_ 電源 \_ 來源 \_ 外部**
</dt> <dd>

裝置使用外部電源來源。

</dd> </dl>

## <a name="remarks"></a>備註

此列舉是由 [WPD \_ 裝置 \_ 電源 \_ 來源](device-properties.md) 屬性所使用。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------|---------------------------------------------------------------------------------------------|
| 標頭<br/> | <dl> <dt>PortableDevice。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**結構和列舉類型**](structures-and-enumeration-types.md)
</dt> </dl>

 

 




