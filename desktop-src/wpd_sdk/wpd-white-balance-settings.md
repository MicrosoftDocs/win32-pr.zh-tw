---
description: WPD 的 \_ 白色 \_ 餘額 \_ 設定列舉類型會說明影片或影像裝置如何加權色彩，以達到適當的白色平衡。
ms.assetid: 7bc173dd-4fdd-4b03-994e-f0711c910618
title: 'WPD_WHITE_BALANCE_SETTINGS 列舉 (PortableDevice .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WPD_WHITE_BALANCE_SETTINGS
api_type:
- HeaderDef
api_location:
- PortableDevice.h
ms.openlocfilehash: 1b596dd6d8fbcc2b2a875b70d80e8eb4040c966590642a004c551ec159c9f5d0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117842045"
---
# <a name="wpd_white_balance_settings-enumeration"></a>WPD \_ 白色 \_ 餘額 \_ 設定列舉

**WPD 的 \_ 白色 \_ 餘額 \_ 設定** 列舉類型會說明影片或影像裝置如何加權色彩，以達到適當的白色平衡。

## <a name="syntax"></a>Syntax


```C++
typedef enum WPD_WHITE_BALANCE_SETTINGS { 
  WPD_WHITE_BALANCE_UNDEFINED           = 0,
  WPD_WHITE_BALANCE_MANUAL              = 1,
  WPD_WHITE_BALANCE_AUTOMATIC           = 2,
  WPD_WHITE_BALANCE_ONE_PUSH_AUTOMATIC  = 3,
  WPD_WHITE_BALANCE_DAYLIGHT            = 4,
  WPD_WHITE_BALANCE_TUNGSTEN            = 5,
  WPD_WHITE_BALANCE_FLASH               = 6
} ;
```



## <a name="constants"></a>常數

<dl> <dt>

<span id="WPD_WHITE_BALANCE_UNDEFINED"></span><span id="wpd_white_balance_undefined"></span>**\_未定義的 WPD 白色 \_ 餘額 \_**
</dt> <dd>

尚未定義此值。

</dd> <dt>

<span id="WPD_WHITE_BALANCE_MANUAL"></span><span id="wpd_white_balance_manual"></span>**WPD \_ 白色 \_ 餘額 \_ 手動**
</dt> <dd>

您可以使用 [WPD \_ 靜止 \_ 影像 \_ RGB \_ 增益](still-image-properties.md) 屬性來明確設定白色餘額，而且也不會自行變更。

</dd> <dt>

<span id="WPD_WHITE_BALANCE_AUTOMATIC"></span><span id="wpd_white_balance_automatic"></span>**\_自動 WPD 白色 \_ 餘額 \_**
</dt> <dd>

裝置會設定白色餘額。

</dd> <dt>

<span id="WPD_WHITE_BALANCE_ONE_PUSH_AUTOMATIC"></span><span id="wpd_white_balance_one_push_automatic"></span>**WPD \_ 白色 \_ 平衡 \_ 一個 \_ 推播 \_ 自動**
</dt> <dd>

裝置會設定白色餘額，但只有當使用者推送裝置的 [捕捉] 按鈕時，才會將裝置用於白色欄位。

</dd> <dt>

<span id="WPD_WHITE_BALANCE_DAYLIGHT"></span><span id="wpd_white_balance_daylight"></span>**WPD \_ 白色 \_ 餘額 \_ 日光**
</dt> <dd>

裝置將使用適用于大部分日光設定的白色餘額號碼。

</dd> <dt>

<span id="WPD_WHITE_BALANCE_TUNGSTEN"></span><span id="wpd_white_balance_tungsten"></span>**WPD \_ 白色 \_ 餘額 \_ TUNGSTEN**
</dt> <dd>

裝置將使用適用于大部分室內 incandescent 光源設定的白色餘額號碼。

</dd> <dt>

<span id="WPD_WHITE_BALANCE_FLASH"></span><span id="wpd_white_balance_flash"></span>**WPD \_ 白色 \_ 餘額 \_ FLASH**
</dt> <dd>

裝置將使用適合搭配 flash 使用的白色餘額號碼。

</dd> </dl>

## <a name="remarks"></a>備註

[WPD \_ 仍 \_ 影像的 \_ 白色 \_ 餘額](still-image-properties.md)屬性會使用這個列舉。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------|---------------------------------------------------------------------------------------------|
| 標頭<br/> | <dl> <dt>PortableDevice。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**結構和列舉類型**](structures-and-enumeration-types.md)
</dt> </dl>

 

 




