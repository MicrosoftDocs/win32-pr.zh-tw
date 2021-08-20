---
description: GetUnsignedIntegerValue 方法會抓取 (type VT \_ UI4) 由索引鍵指定的 ULONG 值。
ms.assetid: 167163fa-6583-4e6b-b801-3a441a95644b
title: 'IPortableDeviceValues：： GetUnsignedIntegerValue 方法 (PortableDeviceTypes .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPortableDeviceValues.GetUnsignedIntegerValue
api_type:
- COM
api_location:
- PortableDeviceGUIDs.lib
- PortableDeviceGUIDs.dll
ms.openlocfilehash: eeb418d3d0aa42675f3d5766f2a8d08e1ad2377bbaa4a2a07f4ba96524d3dec9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119026836"
---
# <a name="iportabledevicevaluesgetunsignedintegervalue-method"></a>IPortableDeviceValues：： GetUnsignedIntegerValue 方法

**GetUnsignedIntegerValue** 方法會抓取 ( type VT \_ UI4) 由索引鍵指定的 ULONG 值。

## <a name="syntax"></a>語法


```C++
HRESULT GetUnsignedIntegerValue(
  [in]  REFPROPERTYKEY key,
  [out] ULONG          *pValue
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

所抓取之 **ULONG** 值的指標。

</dd> </dl>

## <a name="return-value"></a>傳回值

方法會傳回 **HRESULT**。 可能的值包括 (但不限於) 下表中的這些值。



| 傳回碼                                                                                                            | 描述                                                          |
|------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------|
| <dl> <dt>**S \_ 確定**</dt> </dl>                                   | 此方法已成功。<br/>                                     |
| <dl> <dt>**將 \_ 電子 \_ TYPEMISMATCH**</dt> </dl>                   | 索引 *鍵* 所指定的屬性不是 **ULONG** 類型。<br/>  |
| <dl> <dt>**\_ \_ \_ 找不到 WIN32 (錯誤 \_) 的 HRESULT**</dt> </dl> | 索引 *鍵* 所指定的屬性不在集合中。<br/> |



 

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

[**IPortableDeviceValues::SetUnsignedIntegerValue**](iportabledevicevalues-setunsignedintegervalue.md)
</dt> <dt>

[正在抓取支援的服務事件](retrieving-supported-events.md)
</dt> <dt>

[正在抓取支援的服務方法](retrieving-supported-methods.md)
</dt> <dt>

[正在抓取裝置所支援的轉譯功能](retrieving-the-rendering-capabilities-supported-by-a-device.md)
</dt> </dl>

 

 




