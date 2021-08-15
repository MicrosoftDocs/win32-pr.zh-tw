---
description: GetGuidValue 方法會抓取索引鍵所指定的 GUID 值 (類型的 VT \_ CLSID) 。
ms.assetid: 1cfa75e8-2c3b-4893-954e-dae25a6b8220
title: 'IPortableDeviceValues：： GetGuidValue 方法 (PortableDeviceTypes .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPortableDeviceValues.GetGuidValue
api_type:
- COM
api_location:
- PortableDeviceGUIDs.lib
- PortableDeviceGUIDs.dll
ms.openlocfilehash: d6389b426aca52f20b082ed4730778432bdbe56c4a6a1e0a4495060f13dbb5d9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118963677"
---
# <a name="iportabledevicevaluesgetguidvalue-method"></a>IPortableDeviceValues：： GetGuidValue 方法

**GetGuidValue** 方法會抓取索引鍵所指定的 **GUID** 值 (類型的 VT \_ CLSID) 。

## <a name="syntax"></a>語法


```C++
HRESULT GetGuidValue(
  [in]  REFPROPERTYKEY key,
  [out] GUID           *pValue
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

已抓取 **GUID** 值的指標。

</dd> </dl>

## <a name="return-value"></a>傳回值

方法會傳回 **HRESULT**。 可能的值包括 (但不限於) 下表中的這些值。



| 傳回碼                                                                                                            | Description                                                          |
|------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------|
| <dl> <dt>**S \_ 確定**</dt> </dl>                                   | 此方法已成功。<br/>                                     |
| <dl> <dt>**將 \_ 電子 \_ TYPEMISMATCH**</dt> </dl>                   | 索引 *鍵* 所指定的屬性不是 **GUID** 類型。<br/>   |
| <dl> <dt>**\_ \_ \_ 找不到 WIN32 (錯誤 \_) 的 HRESULT**</dt> </dl> | 索引 *鍵* 所指定的屬性不在集合中。<br/> |



 

## <a name="examples"></a>範例

如需如何使用此方法的範例，請參閱抓取 [支援的服務方法](retrieving-supported-methods.md)。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|----------------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>PortableDeviceTypes。h</dt> </dl>   |
| 程式庫<br/> | <dl> <dt>PortableDeviceGUIDs .lib</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**IPortableDeviceValues 介面**](iportabledevicevalues.md)
</dt> <dt>

[**IPortableDeviceValues::SetGuidValue**](iportabledevicevalues-setguidvalue.md)
</dt> <dt>

[正在抓取支援的服務方法](retrieving-supported-methods.md)
</dt> <dt>

[正在抓取裝置所支援的轉譯功能](retrieving-the-rendering-capabilities-supported-by-a-device.md)
</dt> </dl>

 

 




