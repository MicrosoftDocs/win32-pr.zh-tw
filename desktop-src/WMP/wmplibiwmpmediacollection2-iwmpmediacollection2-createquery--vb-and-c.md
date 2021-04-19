---
title: IWMPMediaCollection2 createQuery 方法
description: CreateQuery 方法會傳回代表新查詢的 IWMPQuery 介面。
ms.assetid: a12da325-e77e-4e44-93d1-5e9c5733ea44
keywords:
- createQuery 方法 Windows Media Player
- createQuery 方法 Windows Media Player，IWMPMediaCollection2 介面
- IWMPMediaCollection2 介面 Windows Media Player，createQuery 方法
topic_type:
- apiref
api_name:
- IWMPMediaCollection2.createQuery
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 318b27a20ba801e1fbed58ff79c5bed7841f8c29
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106995089"
---
# <a name="iwmpmediacollection2createquery-method"></a>IWMPMediaCollection2：： createQuery 方法

`createQuery`方法會傳回代表新查詢的 **IWMPQuery** 介面。

## <a name="syntax"></a>語法


```CSharp
public IWMPQuery createQuery();
```


```VB

Public Function createQuery() As IWMPQuery
Implements IWMPMediaCollection2.createQuery
```





## <a name="parameters"></a>參數

這個方法沒有任何參數。

## <a name="return-value"></a>傳回值

**WMPLib IWMPQuery** 介面，表示新的空白查詢。

## <a name="remarks"></a>備註

建立新的查詢是建立複合查詢的第一個步驟。

## <a name="examples"></a>範例

下列範例會使用 `createQuery` 來取得初始化為 null 的 **IWMPQuery** 介面。 因為此查詢並未加入任何條件，所以當它當做 **getStringCollectionByQuery** 方法中的引數使用時，方法會傳回包含指定媒體類型之所有媒體專案的字串集合。 接著會在清單方塊中顯示字串集合。


```CSharp
// Get an IWMPMediaCollection2 interface so that you can access the createQuery and
// getStringCollectionByQuery methods.
WMPLib.IWMPMediaCollection2 mc = (WMPLib.IWMPMediaCollection2)player.mediaCollection;

// Create an IWMPQuery interface with no conditions added to it.
WMPLib.IWMPQuery nullQuery = mc.createQuery();

// Get a string collection that contains the titles of all the audio items in the media
// collection.
WMPLib.IWMPStringCollection2 allTitles = (WMPLib.IWMPStringCollection2)mc.getStringCollectionByQuery("Title", nullQuery, "audio", "", false);

// Display the titles by adding them to a list box.
for (int i = 0; i < allTitles.count; i++)
{
    queryResults.Items.Add(allTitles.Item(i));
}
```


```VB

' Get an IWMPMediaCollection2 interface so that you can access
&#39; the createQuery and getStringCollectionByQuery methods.
Dim mc As WMPLib.IWMPMediaCollection2 = player.mediaCollection

&#39; Create an IWMPQuery interface with no conditions added to it.
Dim nullQuery As WMPLib.IWMPQuery = mc.createQuery()

&#39; Get a string collection that contains the titles of all the audio items in the media
&#39; collection
Dim allTitles As WMPLib.IWMPStringCollection2 = mc.getStringCollectionByQuery(&quot;Title&quot;, nullQuery, &quot;audio&quot;, &quot;&quot;, False)

&#39; Display the titles by adding them to a ListBox
For i As Integer = 0 To (allTitles.count - 1)

    queryResults.Items.Add(allTitles.Item(i))

Next i
```





## <a name="requirements"></a>規格需求



| 需求 | 值 |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| 版本<br/>   | Windows Media Player 11。<br/>                                                                                    |
| 命名空間<br/> | **WMPLib**<br/>                                                                                                  |
| 組件<br/>  | <dl> <dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**IWMPMediaCollection2 介面 (VB 和 c # )**](iwmpmediacollection2--vb-and-c.md)
</dt> <dt>

[**IWMPQuery 介面 (VB 和 c # )**](iwmpquery--vb-and-c.md)
</dt> </dl>

 

 





