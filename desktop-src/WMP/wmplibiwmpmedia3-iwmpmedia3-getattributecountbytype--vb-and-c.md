---
title: IWMPMedia3 getAttributeCountByType 方法
description: GetAttributeCountByType 方法會傳回與指定之屬性類型相關聯的屬性數目。
ms.assetid: d692635f-f9f1-4d8e-a9c5-9d7fa84f41bd
keywords:
- getAttributeCountByType 方法 Windows Media Player
- getAttributeCountByType 方法 Windows Media Player，IWMPMedia3 介面
- IWMPMedia3 介面 Windows Media Player，getAttributeCountByType 方法
topic_type:
- apiref
api_name:
- IWMPMedia3.getAttributeCountByType
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 49505f9e9df8778cc2c17ba062da6700b9b8aec4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106982496"
---
# <a name="iwmpmedia3getattributecountbytype-method"></a>IWMPMedia3：： getAttributeCountByType 方法

**GetAttributeCountByType** 方法會傳回與指定之屬性類型相關聯的屬性數目。

## <a name="syntax"></a>語法


```CSharp
public System.Int32 getAttributeCountByType(
  System.String bstrType,
  System.String bstrLanguage
);
```


```VB

Public Function getAttributeCountByType( _
  ByVal bstrType As System.String, _
  ByVal bstrLanguage As System.String _
) As System.Int32
Implements IWMPMedia3.getAttributeCountByType
```





## <a name="parameters"></a>參數

<dl> <dt>

*bstrType* \[在\]
</dt> <dd>

屬於屬性型別的 **system.string** 。

</dd> <dt>

*bstrLanguage* \[在\]
</dt> <dd>

表示語言的 **system.string** 。 如果值設定為 null 或長度為零的字串 ( "" ) ，則會使用目前的地區設定字串。 否則，此值必須是有效的 RFC 1766 語言字串，例如 "en-us"。

</dd> </dl>

## <a name="return-value"></a>傳回值

此為與類型相關聯的屬性計數的 **system.object** 。

## <a name="remarks"></a>備註

這個方法是用來探索特定媒體專案的特定屬性名稱對應的屬性數目。 然後，您可以將索引編號傳遞給 **getItemInfoByType** 方法。 例如，當媒體專案已分類為多個內容時，這非常有用。

在呼叫這個方法之前，您必須擁有程式庫的讀取權限。 如需詳細資訊，請參閱連結 [庫存取](library-access.md)。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| 版本<br/>   | Windows Media Player 9 系列或更新版本<br/>                                                                      |
| 命名空間<br/> | **WMPLib**<br/>                                                                                                  |
| 組件<br/>  | <dl> <dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**IWMPMedia3 介面 (VB 和 c # )**](iwmpmedia3--vb-and-c.md)
</dt> <dt>

[**IWMPMedia3. getItemInfoByType (VB 和 c # )**](wmplibiwmpmedia3-iwmpmedia3-getiteminfobytype--vb-and-c.md)
</dt> </dl>

 

 





