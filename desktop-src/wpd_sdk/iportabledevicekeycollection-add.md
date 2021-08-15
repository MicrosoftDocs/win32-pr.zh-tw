---
description: Add 方法會將屬性索引鍵新增至集合。
ms.assetid: 640ef1c4-2843-48dd-a30a-9a2ef9de35b9
title: 'IPortableDeviceKeyCollection：： Add 方法 (PortableDeviceTypes .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPortableDeviceKeyCollection.Add
api_type:
- COM
api_location:
- PortableDeviceGUIDs.lib
- PortableDeviceGUIDs.dll
ms.openlocfilehash: 6aa28a7a8a6439f27a095033d35e8b066c1488af13d1ade921f16c4143843adf
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118194718"
---
# <a name="iportabledevicekeycollectionadd-method"></a>IPortableDeviceKeyCollection：： Add 方法

**Add** 方法會將屬性索引鍵新增至集合。

## <a name="syntax"></a>語法


```C++
HRESULT Add(
  [in] REFPROPERTYKEY Key
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*金鑰* \[在\]
</dt> <dd>

要加入至集合的 **REFPROPERTYKEY** 。 這個方法會將索引鍵複製到集合，因此您可以在呼叫這個方法之後釋放本機變數。

</dd> </dl>

## <a name="return-value"></a>傳回值

方法會傳回 **HRESULT**。 可能的值包括 (但不限於) 下表中的這些值。



| 傳回碼                                                                                   | Description                                                                       |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------|
| <dl> <dt>**S \_ 確定**</dt> </dl>          | 此方法已成功。<br/>                                                  |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl> | 沒有足夠的記憶體可用來將索引鍵新增至集合。<br/> |



 

## <a name="examples"></a>範例

如需如何使用此方法的範例，請參閱抓取 [單一物件的屬性](retrieving-properties-for-a-single-object.md)。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|----------------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>PortableDeviceTypes。h</dt> </dl>   |
| 程式庫<br/> | <dl> <dt>PortableDeviceGUIDs .lib</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**IPortableDeviceKeyCollection 介面**](iportabledevicekeycollection.md)
</dt> <dt>

[正在抓取內容物件屬性](retrieving-content-object-properties.md)
</dt> <dt>

[取得單一物件的屬性](retrieving-properties-for-a-single-object.md)
</dt> <dt>

[正在抓取裝置所支援的轉譯功能](retrieving-the-rendering-capabilities-supported-by-a-device.md)
</dt> </dl>

 

 




