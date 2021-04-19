---
description: GetIUnknownValue 方法會抓取 IUnknown 介面值， (輸入 \_ 由索引鍵指定的 VT 未知) 。
ms.assetid: 2197fa1f-639d-4ac1-9d5b-c6534f3ecf1c
title: 'IPortableDeviceValues：： GetIUnknownValue 方法 (PortableDeviceTypes .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPortableDeviceValues.GetIUnknownValue
api_type:
- COM
api_location:
- PortableDeviceGUIDs.lib
- PortableDeviceGUIDs.dll
ms.openlocfilehash: bc7ecfdc699cfe5f572c303d2c8a9e71bafc026b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106995975"
---
# <a name="iportabledevicevaluesgetiunknownvalue-method"></a>IPortableDeviceValues：： GetIUnknownValue 方法

**GetIUnknownValue** 方法會抓取 **IUnknown** 介面值， (輸入由索引鍵指定的 VT \_ 未知) 。

## <a name="syntax"></a>語法


```C++
HRESULT GetIUnknownValue(
  [in]  REFPROPERTYKEY key,
  [out] IUnknown       **ppValue
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*金鑰* \[在\]
</dt> <dd>

指定要取出之專案的 **REFPROPERTYKEY** 索引鍵。

</dd> <dt>

*ppValue* \[擴展\]
</dt> <dd>

接收所抓取 **IUnknown** 介面指標的變數位址。 呼叫端負責在抓取的介面上呼叫 **Release** 。

</dd> </dl>

## <a name="return-value"></a>傳回值

方法會傳回 **HRESULT**。 可能的值包括 (但不限於) 下表中的這些值。



| 傳回碼                                                                                                            | Description                                                                  |
|------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------|
| <dl> <dt>**S \_ 確定**</dt> </dl>                                   | 此方法已成功。<br/>                                             |
| <dl> <dt>**將 \_ 電子 \_ TYPEMISMATCH**</dt> </dl>                   | 索引 *鍵* 所指定的屬性不是 **IUnknown** 介面。<br/> |
| <dl> <dt>**\_ \_ \_ 找不到 WIN32 (錯誤 \_) 的 HRESULT**</dt> </dl> | 索引 *鍵* 所指定的屬性不在集合中。<br/>         |



 

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|----------------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>PortableDeviceTypes。h</dt> </dl>   |
| 程式庫<br/> | <dl> <dt>PortableDeviceGUIDs .lib</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**IPortableDeviceValues 介面**](iportabledevicevalues.md)
</dt> <dt>

[**IPortableDeviceValues::SetIUnknownValue**](iportabledevicevalues-setiunknownvalue.md)
</dt> </dl>

 

 




