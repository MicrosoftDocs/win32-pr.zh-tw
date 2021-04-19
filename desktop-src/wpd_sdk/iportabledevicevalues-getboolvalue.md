---
description: GetBoolValue 方法會抓取布林值， (由索引 \_ 鍵指定的 VT BOOL) 類型。
ms.assetid: cb5fed7a-50b5-4af1-806a-c6582409d265
title: 'IPortableDeviceValues：： GetBoolValue 方法 (PortableDeviceTypes .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPortableDeviceValues.GetBoolValue
api_type:
- COM
api_location:
- PortableDeviceGUIDs.lib
- PortableDeviceGUIDs.dll
ms.openlocfilehash: 8554fc30a1b66226f6e4f8de4e5d8ac0e8abfabf
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106994248"
---
# <a name="iportabledevicevaluesgetboolvalue-method"></a>IPortableDeviceValues：： GetBoolValue 方法

**GetBoolValue** 方法會抓取 **布林** 值， (由索引 \_ 鍵指定的 VT BOOL) 類型。

## <a name="syntax"></a>語法


```C++
HRESULT GetBoolValue(
  [in]  REFPROPERTYKEY key,
  [out] BOOL           *pValue
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

已抓取之 **BOOL** 值的指標。

</dd> </dl>

## <a name="return-value"></a>傳回值

方法會傳回 **HRESULT**。 可能的值包括 (但不限於) 下表中的這些值。



| 傳回碼                                                                                                            | Description                                                          |
|------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------|
| <dl> <dt>**S \_ 確定**</dt> </dl>                                   | 此方法已成功。<br/>                                     |
| <dl> <dt>**將 \_ 電子 \_ TYPEMISMATCH**</dt> </dl>                   | 索引 *鍵* 所指定的屬性不是 **BOOL** 類型。<br/>   |
| <dl> <dt>**\_ \_ \_ 找不到 WIN32 (錯誤 \_) 的 HRESULT**</dt> </dl> | 索引 *鍵* 所指定的屬性不在集合中。<br/> |



 

## <a name="examples"></a>範例

如需如何使用此方法的範例，請參閱 [設定單一物件的屬性](setting-properties-for-a-single-object.md)。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|----------------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>PortableDeviceTypes。h</dt> </dl>   |
| 程式庫<br/> | <dl> <dt>PortableDeviceGUIDs .lib</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**IPortableDeviceValues 介面**](iportabledevicevalues.md)
</dt> <dt>

[**IPortableDeviceValues：： SetBoolValue**](iportabledevicevalues-setboolvalue.md)
</dt> <dt>

[正在抓取支援的服務事件](retrieving-supported-events.md)
</dt> <dt>

[設定單一物件的屬性](setting-properties-for-a-single-object.md)
</dt> <dt>

[寫入內容物件屬性](writing-content-object-properties.md)
</dt> </dl>

 

 




