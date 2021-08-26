---
description: SetBufferValue 方法會將新的位元組 \* 值新增 (類型 VT \_ 向量 \| VT \_ UI1) 或覆寫現有的位元組值。
ms.assetid: 6c421240-2ff8-4862-bd90-1feee5d15a8d
title: 'IPortableDeviceValues：： SetBufferValue 方法 (PortableDeviceTypes .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPortableDeviceValues.SetBufferValue
api_type:
- COM
api_location:
- PortableDeviceGUIDs.lib
- PortableDeviceGUIDs.dll
ms.openlocfilehash: 25a087c6f2d1e254e225f82ef794915898fbc20c7203fe20315d51f78e9770f8
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120055098"
---
# <a name="iportabledevicevaluessetbuffervalue-method"></a>IPortableDeviceValues：： SetBufferValue 方法

**SetBufferValue** 方法會將新的 **位元組** \* 值新增 (類型 VT \_ 向量 \| VT \_ UI1) 或覆寫現有的位元組值。

## <a name="syntax"></a>語法


```C++
HRESULT SetBufferValue(
  [in] REFPROPERTYKEY key,
  [in] BYTE           *pValue,
  [in] DWORD          cbValue
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*金鑰* \[在\]
</dt> <dd>

指定要建立或覆寫之專案的 **REFPROPERTYKEY** 。

</dd> <dt>

*pValue* \[在\]
</dt> <dd>

**位元組 \*** ，其中包含要寫入至專案的資料。 提交的緩衝區資料會複製到介面，因此呼叫者可以在進行此呼叫之後釋放此緩衝區。

</dd> <dt>

*cbValue* \[在\]
</dt> <dd>

*PValue* 所指向的值大小（以位元組為單位）。

</dd> </dl>

## <a name="return-value"></a>傳回值

方法會傳回 **HRESULT**。 可能的值包括 (但不限於) 下表中的這些值。



| 傳回碼                                                                          | 描述                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <dt>**S \_ 確定**</dt> </dl> | 此方法已成功。<br/> |



 

## <a name="remarks"></a>備註

如果現有的值具有 *金鑰* 參數所指定的相同索引鍵，則會覆寫現有的值，而不會出現任何警告。 會適當地釋放現有的金鑰記憶體。

不支援設定 **Null** 或零大小的緩衝區。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|----------------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>PortableDeviceTypes。h</dt> </dl>   |
| 程式庫<br/> | <dl> <dt>PortableDeviceGUIDs .lib</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**IPortableDeviceValues 介面**](iportabledevicevalues.md)
</dt> <dt>

[**IPortableDeviceValues::GetBufferValue**](iportabledevicevalues-getbuffervalue.md)
</dt> </dl>

 

 




