---
description: 刪除 \_ 物件 \_ 選項列舉型別描述刪除物件時，裝置所支援的選項。
ms.assetid: d0e46e77-d333-498f-b2f5-26be1461a116
title: 'DELETE_OBJECT_OPTIONS 列舉 (PortableDevice .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DELETE_OBJECT_OPTIONS
api_type:
- HeaderDef
api_location:
- PortableDevice.h
ms.openlocfilehash: 018c47a383a4fcd95d25bd13b00628678c6fa4a71e608f82544429020ea3f2c1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118194874"
---
# <a name="delete_object_options-enumeration"></a>刪除 \_ 物件 \_ 選項列舉

**刪除 \_ 物件 \_ 選項** 列舉型別描述刪除物件時，裝置所支援的選項。

## <a name="syntax"></a>Syntax


```C++
typedef enum DELETE_OBJECT_OPTIONS { 
  PORTABLE_DEVICE_DELETE_NO_RECURSION    = 0,
  PORTABLE_DEVICE_DELETE_WITH_RECURSION  = 1
} ;
```



## <a name="constants"></a>常數

<dl> <dt>

<span id="PORTABLE_DEVICE_DELETE_NO_RECURSION"></span><span id="portable_device_delete_no_recursion"></span>**便攜 \_ 設備 \_ 刪除 \_ 沒有 \_ 遞迴**
</dt> <dd>

只刪除物件，如果它有子系，則會失敗。

</dd> <dt>

<span id="PORTABLE_DEVICE_DELETE_WITH_RECURSION"></span><span id="portable_device_delete_with_recursion"></span>**\_ \_ \_ 使用遞迴的可攜式裝置刪除 \_**
</dt> <dd>

刪除物件及其所有子系。

</dd> </dl>

## <a name="remarks"></a>備註

應用程式可以藉由呼叫 [**IPortableDeviceCapabilities：： GetCommandOptions**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevicecapabilities-getcommandoptions) 來取得裝置支援的刪除選項，以執行 **WPD \_ 命令物件管理的 [ \_ \_ \_ 刪除 \_ 物件** ] 命令。 它應該會檢查此方法在 [**IPortableDeviceValuesCollection**](iportabledevicevaluescollection.md)物件中傳回的 **WPD \_ 選項 \_ 物件 \_ 管理 \_ 遞迴 \_ 刪除 \_ 支援** 的選項值。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------|---------------------------------------------------------------------------------------------|
| 標頭<br/> | <dl> <dt>PortableDevice。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**結構和列舉類型**](structures-and-enumeration-types.md)
</dt> </dl>

 

 




