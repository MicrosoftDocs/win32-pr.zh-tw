---
title: IWMPMediaCollection2 getPlaylistByQuery 方法
description: GetPlaylistByQuery 方法會傳回 IWMPPlaylist 介面，以提供符合查詢準則之媒體專案的存取權。
ms.assetid: ebbb631f-1faa-4c89-8c1d-cc2b128126b8
keywords:
- getPlaylistByQuery 方法 Windows Media Player
- getPlaylistByQuery 方法 Windows Media Player，IWMPMediaCollection2 介面
- IWMPMediaCollection2 介面 Windows Media Player，getPlaylistByQuery 方法
topic_type:
- apiref
api_name:
- IWMPMediaCollection2.getPlaylistByQuery
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: acd80467c78aac832c5ac2784281abcf07975a1956ee304c734b2b45b82901fc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119053576"
---
# <a name="iwmpmediacollection2getplaylistbyquery-method"></a>IWMPMediaCollection2：： getPlaylistByQuery 方法

`getPlaylistByQuery`方法會傳回 **IWMPPlaylist** 介面，以提供符合查詢準則之媒體專案的存取權。

## <a name="syntax"></a>語法


```CSharp
public IWMPPlaylist getPlaylistByQuery(
  IWMPQuery pQuery,
  System.String bstrMediaType,
  System.String bstrSortAttribute,
  System.Boolean fSortAscending
);
```


```VB

Public Function getPlaylistByQuery( _
  ByVal pQuery As IWMPQuery, _
  ByVal bstrMediaType As System.String, _
  ByVal bstrSortAttribute As System.String, _
  ByVal fSortAscending As System.Boolean _
) As IWMPPlaylist
Implements IWMPMediaCollection2.getPlaylistByQuery
```





## <a name="parameters"></a>參數

<dl> <dt>

*pQuery* \[在\]
</dt> <dd>

代表查詢的 **WMPLib. IWMPQuery** 介面。

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

此為 **布林** 值，指出播放清單是否必須以遞增順序排序。

</dd> </dl>

## <a name="return-value"></a>傳回值

已抓取播放清單的 **WMPLib IWMPPlaylist** 介面。

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

[**IWMPPlaylist 介面 (VB 和 c # )**](iwmpplaylist--vb-and-c.md)
</dt> <dt>

[**IWMPQuery 介面 (VB 和 c # )**](iwmpquery--vb-and-c.md)
</dt> <dt>

[**媒體屬性**](mediatype-attribute.md)
</dt> </dl>

 

 





