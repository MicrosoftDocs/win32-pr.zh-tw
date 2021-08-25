---
description: GetSerializedSize 方法會計算保存序列化 IPortableDeviceValues 介面所需的緩衝區大小。
ms.assetid: 12fa6ed1-ce3b-4c5d-920a-87ff693fe0ea
title: 'IWpdSerializer：： GetSerializedSize 方法 (PortableDeviceTypes .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWpdSerializer.GetSerializedSize
api_type:
- COM
api_location:
- PortableDeviceGUIDs.lib
- PortableDeviceGUIDs.dll
ms.openlocfilehash: ae6b8381928c64b7d16e9f5daa4dd9fd85acd9b61c13531365d871563ef6afe0
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119704518"
---
# <a name="iwpdserializergetserializedsize-method"></a>IWpdSerializer：： GetSerializedSize 方法

**GetSerializedSize** 方法會計算保存序列化 [**IPortableDeviceValues**](iportabledevicevalues.md)介面所需的緩衝區大小。

## <a name="syntax"></a>語法


```C++
HRESULT GetSerializedSize(
  [in]  IPortableDeviceValues *pSource,
  [out] DWORD                 *pdwSize
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*pSource* \[在\]
</dt> <dd>

要要求其大小之 [**IPortableDeviceValues**](iportabledevicevalues.md) 介面的指標。

</dd> <dt>

*pdwSize* \[擴展\]
</dt> <dd>

**DWORD** 的指標，指出序列化 *pSource* 所需的緩衝區大小（以位元組為單位）。

</dd> </dl>

## <a name="return-value"></a>傳回值

方法會傳回 **HRESULT**。 可能的值包括 (但不限於) 下表中的這些值。



| 傳回碼                                                                                   | 描述                                                            |
|-----------------------------------------------------------------------------------------------|------------------------------------------------------------------------|
| <dl> <dt>**S \_ 確定**</dt> </dl>          | 此方法已成功。<br/>                                       |
| <dl> <dt>**E \_ 指標**</dt> </dl>     | 必要的指標引數為 **Null**。<br/>                   |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl> | 沒有足夠的可用記憶體來建立緩衝區。<br/> |



 

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|----------------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>PortableDeviceTypes。h</dt> </dl>   |
| 程式庫<br/> | <dl> <dt>PortableDeviceGUIDs .lib</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**IWpdSerializer 介面**](iwpdserializer.md)
</dt> </dl>

 

 




