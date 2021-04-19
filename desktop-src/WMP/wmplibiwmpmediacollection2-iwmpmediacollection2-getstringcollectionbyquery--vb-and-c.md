---
title: IWMPMediaCollection2 getStringCollectionByQuery 方法
description: GetStringCollectionByQuery 方法會傳回 IWMPStringCollection 介面，此介面可讓您存取符合查詢準則之指定屬性的所有字串值集。
ms.assetid: 2d3b29af-0b6c-4405-8334-9a47a30ff6de
keywords:
- getStringCollectionByQuery 方法 Windows Media Player
- getStringCollectionByQuery 方法 Windows Media Player，IWMPMediaCollection2 介面
- IWMPMediaCollection2 介面 Windows Media Player，getStringCollectionByQuery 方法
topic_type:
- apiref
api_name:
- IWMPMediaCollection2.getStringCollectionByQuery
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 322781bc9ddec3e6f8d74d7229f16ce38e519f05
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106994743"
---
# <a name="iwmpmediacollection2getstringcollectionbyquery-method"></a>IWMPMediaCollection2：： getStringCollectionByQuery 方法

`getStringCollectionByQuery`方法會傳回 **IWMPStringCollection** 介面，此介面可讓您存取符合查詢準則之指定屬性的所有字串值集。

## <a name="syntax"></a>語法


```CSharp
public IWMPStringCollection getStringCollectionByQuery(
  System.String bstrAttribute,
  IWMPQuery pQuery,
  System.String bstrMediaType,
  System.String bstrSortAttribute,
  System.Boolean fSortAscending
);
```


```VB

Public Function getStringCollectionByQuery( _
  ByVal bstrAttribute As System.String, _
  ByVal pQuery As IWMPQuery, _
  ByVal bstrMediaType As System.String, _
  ByVal bstrSortAttribute As System.String, _
  ByVal fSortAscending As System.Boolean _
) As IWMPStringCollection
Implements IWMPMediaCollection2.getStringCollectionByQuery
```





## <a name="parameters"></a>參數

<dl> <dt>

*bstrAttribute* \[在\]
</dt> <dd>

做為屬性名稱的 **system.string** 。

</dd> <dt>

*pQuery* \[在\]
</dt> <dd>

**WMPLib. IWMPQuery** 介面，這個介面會定義用來取出字串集合的條件。

</dd> <dt>

*bstrMediaType* \[在\]
</dt> <dd>

表示媒體類型的 **system.string** 。 必須包含下列其中一個值：「音訊」、「影片」、「相片」、「播放清單」或「其他」。

</dd> <dt>

*bstrSortAttribute* \[在\]
</dt> <dd>

用來排序的屬性名稱的 **system.string** 。 長度為零的字串 ( "" ) 表示不套用排序。

</dd> <dt>

*fSortAscending* \[在\]
</dt> <dd>

此為 **布林** 值，指出字串值集是否必須以遞增順序排序。

</dd> </dl>

## <a name="return-value"></a>傳回值

已抓取之字串值集的 **WMPLib IWMPStringCollection** 介面。

## <a name="remarks"></a>備註

使用 **IWMPQuery** 的複合查詢不區分大小寫。

當 *pQuery* 參數所指定的複合查詢包含在「 **媒體** 類型」屬性上建立的條件時，就會忽略該條件。 一律會使用 *bstrMediaType* 參數的值。 例如，如果複合查詢包含條件「媒體的等於音訊」，而 *bstrMediaType* 參數的值為「影片」，則產生的播放清單只會包含影片專案。

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
</dt> <dt>

[**IWMPStringCollection 介面 (VB 和 c # )**](iwmpstringcollection--vb-and-c.md)
</dt> <dt>

[**媒體屬性**](mediatype-attribute.md)
</dt> </dl>

 

 





