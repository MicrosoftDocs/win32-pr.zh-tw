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
ms.openlocfilehash: dc64012c4f13f84abef55d2426c856b931eb447e61df4f04c69781c089857930
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119083272"
---
# <a name="wpd_exposure_program_modes-enumeration"></a>WPD \_ 公開 \_ 程式 \_ 模式列舉

**WPD \_ 曝光 \_ 程式 \_ 模式** 列舉型別描述使用裝置來捕捉映射時，所要使用的曝光模式。

## <a name="syntax"></a>Syntax


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



## <a name="constants"></a>常數

<dl> <dt>

<span id="WPD_EXPOSURE_PROGRAM_MODE_UNDEFINED"></span><span id="wpd_exposure_program_mode_undefined"></span>**\_未定義 WPD 曝光 \_ 程式 \_ 模式 \_**
</dt> <dd>

尚未指定曝光模式。

</dd> <dt>

<span id="WPD_EXPOSURE_PROGRAM_MODE_MANUAL"></span><span id="wpd_exposure_program_mode_manual"></span>**WPD \_ 曝光 \_ 程式 \_ 模式 \_ 手冊**
</dt> <dd>

應用程式應指定所有的公開設定。

</dd> <dt>

<span id="WPD_EXPOSURE_PROGRAM_MODE_AUTO"></span><span id="wpd_exposure_program_mode_auto"></span>**\_自動 WPD 曝光 \_ 程式 \_ 模式 \_**
</dt> <dd>

使用裝置定義的自動曝光模式。

</dd> <dt>

<span id="WPD_EXPOSURE_PROGRAM_MODE_APERTURE_PRIORITY"></span><span id="wpd_exposure_program_mode_aperture_priority"></span>**WPD \_ 曝光 \_ 程式 \_ 模式 \_ 光圈 \_ 優先順序**
</dt> <dd>

自動曝光模式，表示鏡頭光圈值應該保持固定，但是快門速度應該由裝置決定。

</dd> <dt>

<span id="WPD_EXPOSURE_PROGRAM_MODE_SHUTTER_PRIORITY"></span><span id="wpd_exposure_program_mode_shutter_priority"></span>**WPD \_ 曝光 \_ 計畫 \_ 模式 \_ 快門 \_ 優先順序**
</dt> <dd>

自動曝光模式，表示快門速度應該保持固定，但該鏡頭光圈應由裝置決定。

</dd> <dt>

<span id="WPD_EXPOSURE_PROGRAM_MODE_CREATIVE"></span><span id="wpd_exposure_program_mode_creative"></span>**WPD \_ 公開 \_ 程式 \_ 模式 \_ 創意**
</dt> <dd>

自動曝光模式，可嘗試最大化欄位的深度。

</dd> <dt>

<span id="WPD_EXPOSURE_PROGRAM_MODE_ACTION"></span><span id="wpd_exposure_program_mode_action"></span>**WPD \_ 曝光 \_ 程式 \_ 模式 \_ 動作**
</dt> <dd>

自動曝光模式，可嘗試最大化快門速度。

</dd> <dt>

<span id="WPD_EXPOSURE_PROGRAM_MODE_PORTRAIT"></span><span id="wpd_exposure_program_mode_portrait"></span>**WPD \_ 曝光 \_ 程式 \_ 模式 \_ 縱向**
</dt> <dd>

指定相對淺之欄位深度的自動化曝光模式。

</dd> </dl>

## <a name="remarks"></a>備註

指出裝置的曝光程式模式。 此列舉是由 [WPD 仍為 \_ \_ 影像 \_ 曝光 \_ 程式 \_ 模式](still-image-properties.md) 屬性所使用。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------|---------------------------------------------------------------------------------------------|
| 標頭<br/> | <dl> <dt>PortableDevice。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**結構和列舉類型**](structures-and-enumeration-types.md)
</dt> </dl>

 

 




