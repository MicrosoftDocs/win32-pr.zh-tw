---
title: IWMPStringCollection2 getItemInfo 方法
description: GetItemInfo 方法會傳回與指定的字串集合專案索引和名稱對應的字串。
ms.assetid: 4a107e85-9eb7-42be-b1f9-8e9e92e6e509
keywords:
- getItemInfo 方法 Windows Media Player
- getItemInfo 方法 Windows Media Player，IWMPStringCollection2 介面
- IWMPStringCollection2 介面 Windows Media Player，getItemInfo 方法
topic_type:
- apiref
api_name:
- IWMPStringCollection2.getItemInfo
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6f3f5371d55384544e4135e702b686cc7ce36707d204529ca7a4e68a3734d8ec
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119899838"
---
# <a name="iwmpstringcollection2getiteminfo-method"></a>IWMPStringCollection2：： getItemInfo 方法

**GetItemInfo** 方法會傳回與指定的字串集合專案索引和名稱對應的字串。

## <a name="syntax"></a>語法


```CSharp
public System.String getItemInfo(
  System.Int32 lCollectionIndex,
  System.String bstrItemName
);
```


```VB

Public Function getItemInfo( _
  ByVal lCollectionIndex As System.Int32, _
  ByVal bstrItemName As System.String _
) As System.String
Implements IWMPStringCollection2.getItemInfo
```





## <a name="parameters"></a>參數

<dl> <dt>

*lCollectionIndex* \[在\]
</dt> <dd>

指定要從中取得屬性之字串收集項的以零為基底之索引的 **system.object。**

</dd> <dt>

*bstrItemName* \[在\]
</dt> <dd>

做為屬性名稱的 **system.string** 。

</dd> </dl>

## <a name="return-value"></a>傳回值

System.string **，這個字串是** 字串收集項目的名稱。 對於其基礎值為 system.string 的 **屬性，它會傳回** 字串 "true" 或 "false"。

## <a name="remarks"></a>備註

若要使用具有複雜值的多個值和屬性來取得屬性，請使用 **getItemInfoByType** 方法。

若要使用此方法，需要有程式庫的讀取權限。 如需詳細資訊，請參閱連結 [庫存取](library-access.md)。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| 版本<br/>   | Windows Media Player 11。<br/>                                                                                    |
| 命名空間<br/> | **WMPLib**<br/>                                                                                                  |
| 組件<br/>  | <dl> <dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**IWMPStringCollection2 介面**](iwmpstringcollection2--vb-and-c.md)
</dt> <dt>

[**IWMPStringCollection2. getItemInfoByType (VB 和 c # )**](wmplibiwmpstringcollection2-iwmpstringcollection2-getiteminfobytype--vb-and-c.md)
</dt> </dl>

 

 





