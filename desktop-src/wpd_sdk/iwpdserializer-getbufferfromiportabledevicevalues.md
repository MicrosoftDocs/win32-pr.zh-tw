---
description: GetBufferFromIPortableDeviceValues 方法會將提交的 IPortableDeviceValues 介面序列化為配置的位元組陣列。 傳回的位元組陣列是針對呼叫端配置的，而且應該由呼叫端使用 CoTaskMemFree 來釋放。
ms.assetid: fd856394-9cb3-41cb-875b-1d490ca859df
title: 'IWpdSerializer：： GetBufferFromIPortableDeviceValues 方法 (PortableDeviceTypes .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWpdSerializer.GetBufferFromIPortableDeviceValues
api_type:
- COM
api_location:
- PortableDeviceGUIDs.lib
- PortableDeviceGUIDs.dll
ms.openlocfilehash: 10a483331d15c09de8398d11e940453d8f239e2207fdefb82d86fd4bb1460daf
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117843011"
---
# <a name="iwpdserializergetbufferfromiportabledevicevalues-method"></a>IWpdSerializer：： GetBufferFromIPortableDeviceValues 方法

**GetBufferFromIPortableDeviceValues** 方法會將提交的 **IPortableDeviceValues** 介面序列化為配置的位元組陣列。 傳回的位元組陣列是針對呼叫端配置的，而且應該由呼叫端使用 **CoTaskMemFree** 來釋放。

## <a name="syntax"></a>語法


```C++
HRESULT GetBufferFromIPortableDeviceValues(
  [in]  IPortableDeviceValues *pSource,
  [out] BYTE                  **ppBuffer,
  [out] DWORD                 *pdwBufferSize
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*pSource* \[在\]
</dt> <dd>

要序列化之 [**IPortableDeviceValues**](iportabledevicevalues.md) 介面的指標。

</dd> <dt>

*ppBuffer* \[擴展\]
</dt> <dd>

**位元組 \* *_ 的指標，其中包含已序列化的資料。Windows可攜式裝置配置此記憶體;呼叫者必須藉由呼叫 _ CoTaskMemFree 來釋放它***。

</dd> <dt>

*pdwBufferSize* \[擴展\]
</dt> <dd>

**DWORD** 的指標，指定配置的緩衝區大小（以位元組為單位）。

</dd> </dl>

## <a name="return-value"></a>傳回值

方法會傳回 **HRESULT**。 可能的值包括 (但不限於) 下表中的這些值。



| 傳回碼                                                                                   | 描述                                                            |
|-----------------------------------------------------------------------------------------------|------------------------------------------------------------------------|
| <dl> <dt>**S \_ 確定**</dt> </dl>          | 此方法已成功。<br/>                                       |
| <dl> <dt>**E \_ 指標**</dt> </dl>     | 必要的指標引數為 **Null**。<br/>                   |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl> | 沒有足夠的記憶體可用來建立緩衝區。<br/> |



 

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|----------------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>PortableDeviceTypes。h</dt> </dl>   |
| 程式庫<br/> | <dl> <dt>PortableDeviceGUIDs .lib</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**IWpdSerializer 介面**](iwpdserializer.md)
</dt> </dl>

 

 




