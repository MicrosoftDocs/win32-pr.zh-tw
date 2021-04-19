---
description: GetFloatValue 方法會抓取 (type VT \_ R4) 由索引鍵指定的浮點值。
ms.assetid: 8a134dfb-f671-4cde-ae35-c8a41be270cf
title: 'IPortableDeviceValues：： GetFloatValue 方法 (PortableDeviceTypes .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPortableDeviceValues.GetFloatValue
api_type:
- COM
api_location:
- PortableDeviceGUIDs.lib
- PortableDeviceGUIDs.dll
ms.openlocfilehash: 0c99dcbb2d8436df7e3d593aa53efd086dc965ea
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106984051"
---
# <a name="iportabledevicevaluesgetfloatvalue-method"></a>IPortableDeviceValues：： GetFloatValue 方法

**GetFloatValue** 方法會抓取 ( type VT \_ R4) 由索引鍵指定的浮點值。

## <a name="syntax"></a>語法


```C++
HRESULT GetFloatValue(
  [in]  REFPROPERTYKEY key,
  [out] FLOAT          *pValue
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

已抓取 **浮點** 值的指標。

</dd> </dl>

## <a name="return-value"></a>傳回值

方法會傳回 **HRESULT**。 可能的值包括 (但不限於) 下表中的這些值。



| 傳回碼                                                                                             | Description                                                          |
|---------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------|
| <dl> <dt>**S \_ 確定**</dt> </dl>                    | 此方法已成功。<br/>                                     |
| <dl> <dt>**將 \_ 電子 \_ TYPEMISMATCH**</dt> </dl>    | 索引 *鍵* 所指定的屬性不是 **FLOAT** 類型。<br/>  |
| <dl> <dt>**E \_ \_ \_ 不支援的識別碼**</dt> </dl> | 索引 *鍵* 所指定的屬性不在集合中。<br/> |



 

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|----------------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>PortableDeviceTypes。h</dt> </dl>   |
| 程式庫<br/> | <dl> <dt>PortableDeviceGUIDs .lib</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**IPortableDeviceValues 介面**](iportabledevicevalues.md)
</dt> <dt>

[**IPortableDeviceValues::SetFloatValue**](iportabledevicevalues-setfloatvalue.md)
</dt> </dl>

 

 




