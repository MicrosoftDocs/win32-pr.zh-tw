---
description: GetIPortableDeviceValuesFromBuffer 方法會將位元組陣列還原序列化為 IPortableDeviceValues 介面。
ms.assetid: 93bea711-74d5-407a-a707-a3abe47bc2cd
title: 'IWpdSerializer：： GetIPortableDeviceValuesFromBuffer 方法 (PortableDeviceTypes .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWpdSerializer.GetIPortableDeviceValuesFromBuffer
api_type:
- COM
api_location:
- PortableDeviceGUIDs.lib
- PortableDeviceGUIDs.dll
ms.openlocfilehash: 639a9455349e1d016b71d9c9717940695e9c0a85
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106999990"
---
# <a name="iwpdserializergetiportabledevicevaluesfrombuffer-method"></a>IWpdSerializer：： GetIPortableDeviceValuesFromBuffer 方法

**GetIPortableDeviceValuesFromBuffer** 方法會將位元組陣列還原序列化為 **IPortableDeviceValues** 介面。

## <a name="syntax"></a>語法


```C++
HRESULT GetIPortableDeviceValuesFromBuffer(
  [in]  BYTE                  *pBuffer,
  [in]  DWORD                 dwInputBufferLength,
  [out] IPortableDeviceValues **ppParams
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*pBuffer* \[在\]
</dt> <dd>

要還原序列化的緩衝區指標。

</dd> <dt>

*dwInputBufferLength* \[在\]
</dt> <dd>

指定緩衝區大小的 **DWORD** （以位元組為單位）。

</dd> <dt>

*ppParams* \[擴展\]
</dt> <dd>

變數的位址，此變數會接收從緩衝區建立之 [**IPortableDeviceValues**](iportabledevicevalues.md) 介面的指標。 應用程式會負責在介面上呼叫 **Release** 。

</dd> </dl>

## <a name="return-value"></a>傳回值

方法會傳回 **HRESULT**。 可能的值包括 (但不限於) 下表中的這些值。



| 傳回碼                                                                                  | Description                                          |
|----------------------------------------------------------------------------------------------|------------------------------------------------------|
| <dl> <dt>**S \_ 確定**</dt> </dl>         | 此方法已成功。<br/>                     |
| <dl> <dt>**E \_ 指標**</dt> </dl>    | 必要的指標引數為 **Null**。<br/> |
| <dl> <dt>**E 未 \_ 預期**</dt> </dl> | 發生未指定的轉換錯誤。<br/> |



 

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|----------------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>PortableDeviceTypes。h</dt> </dl>   |
| 程式庫<br/> | <dl> <dt>PortableDeviceGUIDs .lib</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**IWpdSerializer 介面**](iwpdserializer.md)
</dt> </dl>

 

 




