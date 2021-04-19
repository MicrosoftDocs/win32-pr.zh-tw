---
description: WPD \_ 儲存體 \_ 類型 \_ 值列舉類型會描述不同的 Windows 可攜式裝置儲存類型。
ms.assetid: 52c34458-e64e-4355-9231-7457a6dff5c5
title: 'WPD_STORAGE_TYPE_VALUES 列舉 (PortableDevice .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WPD_STORAGE_TYPE_VALUES
api_type:
- HeaderDef
api_location:
- PortableDevice.h
ms.openlocfilehash: b741feb1cb9a834e16a35627fe98718ac8acf30f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106989639"
---
# <a name="wpd_storage_type_values-enumeration"></a>WPD \_ 儲存體 \_ 類型 \_ 值列舉

**WPD \_ 儲存體 \_ 類型 \_ 值** 列舉類型會描述不同的 Windows 可攜式裝置儲存類型。

## <a name="syntax"></a>Syntax


```C++
typedef enum tagWPD_STORAGE_TYPE_VALUES { 
  WPD_STORAGE_TYPE_UNDEFINED      = 0,
  WPD_STORAGE_TYPE_FIXED_ROM      = 1,
  WPD_STORAGE_TYPE_REMOVABLE_ROM  = 2,
  WPD_STORAGE_TYPE_FIXED_RAM      = 3,
  WPD_STORAGE_TYPE_REMOVABLE_RAM  = 4
} WPD_STORAGE_TYPE_VALUES;
```



## <a name="constants"></a>常數

<dl> <dt>

<span id="WPD_STORAGE_TYPE_UNDEFINED"></span><span id="wpd_storage_type_undefined"></span>**WPD \_ 儲存體 \_ 類型 \_ 未定義**
</dt> <dd>

儲存體是未定義的類型。

</dd> <dt>

<span id="WPD_STORAGE_TYPE_FIXED_ROM"></span><span id="wpd_storage_type_fixed_rom"></span>**WPD \_ 儲存體 \_ 類型 \_ 固定 \_ ROM**
</dt> <dd>

儲存體為非卸載式和唯讀。

</dd> <dt>

<span id="WPD_STORAGE_TYPE_REMOVABLE_ROM"></span><span id="wpd_storage_type_removable_rom"></span>**WPD \_ 存放裝置 \_ 類型的 \_ 可移動 \_ ROM**
</dt> <dd>

儲存體是可移動的，而且是唯讀的。

</dd> <dt>

<span id="WPD_STORAGE_TYPE_FIXED_RAM"></span><span id="wpd_storage_type_fixed_ram"></span>**WPD \_ 儲存體 \_ 類型 \_ 固定 \_ RAM**
</dt> <dd>

儲存體是不可卸載的，且可讀/寫功能。

</dd> <dt>

<span id="WPD_STORAGE_TYPE_REMOVABLE_RAM"></span><span id="wpd_storage_type_removable_ram"></span>**WPD \_ 儲存體 \_ 類型的 \_ 可移動 \_ RAM**
</dt> <dd>

儲存體是可移動的，且可讀/寫功能。

</dd> </dl>

## <a name="remarks"></a>備註

無。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------|---------------------------------------------------------------------------------------------|
| 標頭<br/> | <dl> <dt>PortableDevice。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**結構和列舉類型**](structures-and-enumeration-types.md)
</dt> </dl>

 

 




