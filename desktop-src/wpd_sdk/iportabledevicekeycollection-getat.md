---
description: GetAt 方法會依據索引，從集合中抓取 PROPERTYKEY。
ms.assetid: 9a3c5c28-39b4-4d53-a8d7-0f5a0d4d89ad
title: 'IPortableDeviceKeyCollection：： GetAt 方法 (PortableDeviceTypes .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPortableDeviceKeyCollection.GetAt
api_type:
- COM
api_location:
- PortableDeviceGUIDs.lib
- PortableDeviceGUIDs.dll
ms.openlocfilehash: b75285f6dcdb0961312fa1db8f5c912b771bd786
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106978780"
---
# <a name="iportabledevicekeycollectiongetat-method"></a>IPortableDeviceKeyCollection：： GetAt 方法

**GetAt** 方法會依據索引，從集合中抓取 **PROPERTYKEY** 。

## <a name="syntax"></a>語法


```C++
HRESULT GetAt(
  [in]  const DWORD       dwIndex,
  [out]       PROPERTYKEY *pKey
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*dwIndex* \[在\]
</dt> <dd>

**DWORD** ，其中包含要抓取之索引鍵的索引。

</dd> <dt>

*pKey* \[擴展\]
</dt> <dd>

**PROPERTYKEY** 物件的指標。

</dd> </dl>

## <a name="return-value"></a>傳回值

方法會傳回 **HRESULT**。 可能的值包括 (但不限於) 下表中的這些值。



| 傳回碼                                                                                  | Description                                          |
|----------------------------------------------------------------------------------------------|------------------------------------------------------|
| <dl> <dt>**S \_ 確定**</dt> </dl>         | 此方法已成功。<br/>                     |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl> | 傳入的索引超出範圍。<br/>     |
| <dl> <dt>**E \_ 指標**</dt> </dl>    | 必要的指標引數為 **Null**。<br/> |



 

## <a name="examples"></a>範例

如需如何使用此方法的範例，請參閱抓取 [支援的服務事件](retrieving-supported-events.md)。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|----------------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>PortableDeviceTypes。h</dt> </dl>   |
| 程式庫<br/> | <dl> <dt>PortableDeviceGUIDs .lib</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**IPortableDeviceKeyCollection 介面**](iportabledevicekeycollection.md)
</dt> <dt>

[正在抓取支援的服務事件](retrieving-supported-events.md)
</dt> <dt>

[正在抓取支援的服務方法](retrieving-supported-methods.md)
</dt> </dl>

 

 




