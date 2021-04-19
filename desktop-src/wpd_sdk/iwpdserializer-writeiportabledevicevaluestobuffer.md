---
description: WriteIPortableDeviceValuesToBuffer 方法會將 IPortableDeviceValues 介面序列化為呼叫端配置的位元組陣列。
ms.assetid: 4d0108f1-563e-42df-897b-7cc0e9ff5b3a
title: 'IWpdSerializer：： WriteIPortableDeviceValuesToBuffer 方法 (PortableDeviceTypes .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWpdSerializer.WriteIPortableDeviceValuesToBuffer
api_type:
- COM
api_location:
- PortableDeviceGUIDs.lib
- PortableDeviceGUIDs.dll
ms.openlocfilehash: f2a8f8b374f967f7231881d9e0eca6434e9c57e2
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106986147"
---
# <a name="iwpdserializerwriteiportabledevicevaluestobuffer-method"></a>IWpdSerializer：： WriteIPortableDeviceValuesToBuffer 方法

**WriteIPortableDeviceValuesToBuffer** 方法會將 **IPortableDeviceValues** 介面序列化為呼叫端配置的位元組陣列。

## <a name="syntax"></a>語法


```C++
HRESULT WriteIPortableDeviceValuesToBuffer(
  [in]  DWORD                 dwOutputBufferLength,
  [in]  IPortableDeviceValues *pResults,
  [out] BYTE                  *pBuffer,
  [out] DWORD                 *pdwBytesWritten
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*dwOutputBufferLength* \[在\]
</dt> <dd>

指定 *pBuffer* 大小的 **DWORD** （以位元組為單位）。

</dd> <dt>

*pResults* \[在\]
</dt> <dd>

要序列化之 [**IPortableDeviceValues**](iportabledevicevalues.md) 介面的指標。

</dd> <dt>

*pBuffer* \[擴展\]
</dt> <dd>

呼叫端配置之緩衝區的指標。 若要瞭解所需的緩衝區大小，請呼叫 **GetSerializedSize**。

</dd> <dt>

*pdwBytesWritten* \[擴展\]
</dt> <dd>

**DWORD** 的指標，指出實際寫入至呼叫端配置之緩衝區的位元組數目。

</dd> </dl>

## <a name="return-value"></a>傳回值

方法會傳回 **HRESULT**。 可能的值包括 (但不限於) 下表中的這些值。



| 傳回碼                                                                                   | Description                                               |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------|
| <dl> <dt>**S \_ 確定**</dt> </dl>          | 此方法已成功。<br/>                          |
| <dl> <dt>**E \_ 指標**</dt> </dl>     | 必要的指標引數為 **Null**。<br/>      |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl> | 呼叫端提供的緩衝區不夠大。<br/> |



 

## <a name="remarks"></a>備註

這個方法會將 **IPortableDeviceValues** 介面複製到現有的緩衝區。 如果您想要配置新的緩衝區，請使用 [**GetBufferFromIPortableDeviceValues**](iwpdserializer-getbufferfromiportabledevicevalues.md)。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|----------------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>PortableDeviceTypes。h</dt> </dl>   |
| 程式庫<br/> | <dl> <dt>PortableDeviceGUIDs .lib</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**IWpdSerializer 介面**](iwpdserializer.md)
</dt> </dl>

 

 




