---
title: IWMPStringCollection2 getAttributeCountByType 方法
description: GetAttributeCountByType 方法會傳回與指定的字串集合索引、屬性名稱和語言相關聯的屬性數目。
ms.assetid: 30312039-3676-4322-b6f6-fb86098bf578
keywords:
- getAttributeCountByType 方法 Windows Media Player
- getAttributeCountByType 方法 Windows Media Player，IWMPStringCollection2 介面
- IWMPStringCollection2 介面 Windows Media Player，getAttributeCountByType 方法
topic_type:
- apiref
api_name:
- IWMPStringCollection2.getAttributeCountByType
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e9bb60fdd843fb3f45b6e4e3aff444a8a915fa0f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106983168"
---
# <a name="iwmpstringcollection2getattributecountbytype-method"></a>IWMPStringCollection2：： getAttributeCountByType 方法

**GetAttributeCountByType** 方法會傳回與指定的字串集合索引、屬性名稱和語言相關聯的屬性數目。

## <a name="syntax"></a>語法


```CSharp
public System.Int32 getAttributeCountByType(
  System.Int32 lCollectionIndex,
  System.String bstrType,
  System.String bstrLanguage
);
```


```VB

Public Function getAttributeCountByType( _
  ByVal lCollectionIndex As System.Int32, _
  ByVal bstrType As System.String, _
  ByVal bstrLanguage As System.String _
) As System.Int32
Implements IWMPStringCollection2.getAttributeCountByType
```





## <a name="parameters"></a>參數

<dl> <dt>

*lCollectionIndex* \[在\]
</dt> <dd>

指定要從中取得屬性之字串收集項的以零為基底之索引的 **system.object。**

</dd> <dt>

*bstrType* \[在\]
</dt> <dd>

表示屬性名稱的 **system.string** 。

</dd> <dt>

*bstrLanguage* \[在\]
</dt> <dd>

表示語言名稱的 **system.string** 。 如果值設定為 null 或零長度的字串 ( "" ) ，則會使用目前的地區設定字串。 否則，此值必須是有效的 RFC 1766 語言字串，例如 "en-us"。

</dd> </dl>

## <a name="return-value"></a>傳回值

作為計數的 **system.object** 。

## <a name="remarks"></a>備註

這個方法是用來針對指定的 **StringCollection** 專案，探索對應至特定屬性名稱的屬性數目。 然後，您可以將索引編號傳遞給 **getItemInfoByType** 方法的第四個參數。

若要使用此方法，需要有程式庫的讀取權限。 如需詳細資訊，請參閱連結 [庫存取](library-access.md)。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| 版本<br/>   | Windows Media Player 11。<br/>                                                                                    |
| 命名空間<br/> | **WMPLib**<br/>                                                                                                  |
| 組件<br/>  | <dl> <dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**IWMPStringCollection2 介面 (VB 和 c # )**](iwmpstringcollection2--vb-and-c.md)
</dt> <dt>

[**IWMPStringCollection2. getItemInfoByType (VB 和 c # )**](wmplibiwmpstringcollection2-iwmpstringcollection2-getiteminfobytype--vb-and-c.md)
</dt> </dl>

 

 





