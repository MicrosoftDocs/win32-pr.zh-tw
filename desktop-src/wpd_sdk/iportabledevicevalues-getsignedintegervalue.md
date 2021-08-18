---
description: GetSignedIntegerValue 方法會抓取 (type VT \_ I4) 由索引鍵指定的 LONG 值。
ms.assetid: d2291a64-d0b3-4a30-a37c-2b6cd9880a11
title: 'IPortableDeviceValues：： GetSignedIntegerValue 方法 (PortableDeviceTypes .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPortableDeviceValues.GetSignedIntegerValue
api_type:
- COM
api_location:
- PortableDeviceGUIDs.lib
- PortableDeviceGUIDs.dll
ms.openlocfilehash: 5b2bab46a7509ce858af9db3c7c4785de5161b64e86c0f3c280fdad00ebe5f64
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117843001"
---
# <a name="iportabledevicevaluesgetsignedintegervalue-method"></a>IPortableDeviceValues：： GetSignedIntegerValue 方法

**GetSignedIntegerValue** 方法會抓取 ( type VT \_ I4) 由索引鍵指定的 LONG 值。

## <a name="syntax"></a>語法


```C++
HRESULT GetSignedIntegerValue(
  [in]  REFPROPERTYKEY key,
  [out] LONG           *pValue
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*金鑰* \[在\]
</dt> <dd>

指定要取出之專案的 **REFPROPERTYKEY** 索引鍵。

</dd> <dt>

*pValue* \[擴展\]
</dt> <dd>

已抓取之 **完整** 值的指標。

</dd> </dl>

## <a name="return-value"></a>傳回值

方法會傳回 **HRESULT**。 可能的值包括 (但不限於) 下表中的這些值。



| 傳回碼                                                                                                            | 描述                                                          |
|------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------|
| <dl> <dt>**S \_ 確定**</dt> </dl>                                   | 此方法已成功。<br/>                                     |
| <dl> <dt>**將 \_ 電子 \_ TYPEMISMATCH**</dt> </dl>                   | 索引 *鍵* 指定的屬性不是 **LONG** 類型。<br/>   |
| <dl> <dt>**\_ \_ \_ 找不到 WIN32 (錯誤 \_) 的 HRESULT**</dt> </dl> | 索引 *鍵* 所指定的屬性不在集合中。<br/> |



 

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|----------------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>PortableDeviceTypes。h</dt> </dl>   |
| 程式庫<br/> | <dl> <dt>PortableDeviceGUIDs .lib</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**IPortableDeviceValues 介面**](iportabledevicevalues.md)
</dt> <dt>

[**IPortableDeviceValues::SetSignedIntegerValue**](iportabledevicevalues-setsignedintegervalue.md)
</dt> </dl>

 

 




