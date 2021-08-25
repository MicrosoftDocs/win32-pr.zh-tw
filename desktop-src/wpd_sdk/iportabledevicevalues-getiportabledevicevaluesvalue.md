---
description: GetIPortableDeviceValuesValue 方法會抓取索引鍵所指定的 IPortableDeviceValues 值， (類型 \_ 為 VT 未知) 。
ms.assetid: bf62c6a9-560b-4667-94d0-2dea6657eed1
title: 'IPortableDeviceValues：： GetIPortableDeviceValuesValue 方法 (PortableDeviceTypes .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPortableDeviceValues.GetIPortableDeviceValuesValue
api_type:
- COM
api_location:
- PortableDeviceGUIDs.lib
- PortableDeviceGUIDs.dll
ms.openlocfilehash: aeec29bf3d9cf18bcf54c885d46d159c21c661a1e886903110952cd3a23c540e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120055158"
---
# <a name="iportabledevicevaluesgetiportabledevicevaluesvalue-method"></a>IPortableDeviceValues：： GetIPortableDeviceValuesValue 方法

**GetIPortableDeviceValuesValue** 方法會抓取索引鍵所指定的 **IPortableDeviceValues** 值， (類型 \_ 為 VT 未知) 。

## <a name="syntax"></a>語法


```C++
HRESULT GetIPortableDeviceValuesValue(
  [in]  REFPROPERTYKEY        key,
  [out] IPortableDeviceValues **ppValue
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

接收已抓取 [**IPortableDeviceValues**](iportabledevicevalues.md) 介面指標的變數位址。 呼叫端負責在抓取的介面上呼叫 **Release** 。

</dd> </dl>

## <a name="return-value"></a>傳回值

方法會傳回 **HRESULT**。 可能的值包括 (但不限於) 下表中的這些值。



| 傳回碼                                                                                                            | 描述                                                                               |
|------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ 確定**</dt> </dl>                                   | 此方法已成功。<br/>                                                          |
| <dl> <dt>**將 \_ 電子 \_ TYPEMISMATCH**</dt> </dl>                   | 索引 *鍵* 所指定的屬性不是 **IPortableDeviceValues** 介面。<br/> |
| <dl> <dt>**\_ \_ \_ 找不到 WIN32 (錯誤 \_) 的 HRESULT**</dt> </dl> | 索引 *鍵* 所指定的屬性不在集合中。<br/>                      |



 

## <a name="examples"></a>範例

如需如何使用此方法的範例，請參閱抓取 [支援的服務事件](retrieving-supported-events.md)。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|----------------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>PortableDeviceTypes。h</dt> </dl>   |
| 程式庫<br/> | <dl> <dt>PortableDeviceGUIDs .lib</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**IPortableDeviceValues 介面**](iportabledevicevalues.md)
</dt> <dt>

[**IPortableDeviceValues::SetIPortableDeviceValuesValue**](iportabledevicevalues-setiportabledevicevaluesvalue.md)
</dt> <dt>

[正在抓取支援的服務事件](retrieving-supported-events.md)
</dt> <dt>

[正在抓取裝置所支援的轉譯功能](retrieving-the-rendering-capabilities-supported-by-a-device.md)
</dt> </dl>

 

 




