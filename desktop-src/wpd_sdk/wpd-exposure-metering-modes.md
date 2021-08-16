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
ms.openlocfilehash: 2a165493142fc25ea64adc2678e8bc4ccbeace32e245422f0fcea419063a26ee
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117842278"
---
# <a name="wpd_exposure_metering_modes-enumeration"></a>WPD \_ 公開 \_ 計量 \_ 模式列舉

**WPD \_ 曝光 \_ 計量 \_ 模式** 列舉類型會描述在裝置上評估仍有影像捕捉的風險時，所要使用的計量模式。

## <a name="syntax"></a>Syntax


```C++
typedef enum WPD_EXPOSURE_METERING_MODES { 
  WPD_EXPOSURE_METERING_MODE_UNDEFINED                = 0,
  WPD_EXPOSURE_METERING_MODE_AVERAGE                  = 1,
  WPD_EXPOSURE_METERING_MODE_CENTER_WEIGHTED_AVERAGE  = 2,
  WPD_EXPOSURE_METERING_MODE_MULTI_SPOT               = 3,
  WPD_EXPOSURE_METERING_MODE_CENTER_SPOT              = 4
} ;
```



## <a name="constants"></a>常數

<dl> <dt>

<span id="WPD_EXPOSURE_METERING_MODE_UNDEFINED"></span><span id="wpd_exposure_metering_mode_undefined"></span>**\_未定義 WPD 曝光 \_ 計量 \_ 模式 \_**
</dt> <dd>

計量模式未定義。

</dd> <dt>

<span id="WPD_EXPOSURE_METERING_MODE_AVERAGE"></span><span id="wpd_exposure_metering_mode_average"></span>**WPD \_ 曝光 \_ 計量 \_ 模式 \_ 平均**
</dt> <dd>

使用整個影像的平均曝光量。

</dd> <dt>

<span id="WPD_EXPOSURE_METERING_MODE_CENTER_WEIGHTED_AVERAGE"></span><span id="wpd_exposure_metering_mode_center_weighted_average"></span>**WPD \_ 曝光 \_ 計量 \_ 模式 \_ 中心 \_ 加權 \_ 平均**
</dt> <dd>

使用平均曝光，並以影像的中心提供更多權數。

</dd> <dt>

<span id="WPD_EXPOSURE_METERING_MODE_MULTI_SPOT"></span><span id="wpd_exposure_metering_mode_multi_spot"></span>**WPD \_ 曝光 \_ 計量 \_ 模式 \_ 多 \_ 點**
</dt> <dd>

使用多點平均技巧。

</dd> <dt>

<span id="WPD_EXPOSURE_METERING_MODE_CENTER_SPOT"></span><span id="wpd_exposure_metering_mode_center_spot"></span>**WPD \_ 曝光 \_ 計量 \_ 模式 \_ 中心 \_ 點**
</dt> <dd>

使用中央點平均技巧。

</dd> </dl>

## <a name="remarks"></a>備註

指出裝置的計量模式。 [WPD \_ 仍 \_ 影像 \_ 曝光 \_ 計量 \_ 模式](still-image-properties.md)屬性會使用這個列舉。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------|---------------------------------------------------------------------------------------------|
| 標頭<br/> | <dl> <dt>PortableDevice。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**結構和列舉類型**](structures-and-enumeration-types.md)
</dt> </dl>

 

 




