---
title: MediaCollection. getPlaylistByQuery 方法
description: GetPlaylistByQuery 方法會抓取包含符合查詢準則之媒體物件的播放清單物件。
ms.assetid: 3487d442-a5bb-4519-ac45-d0138516305e
keywords:
- getPlaylistByQuery 方法 Windows Media Player
- getPlaylistByQuery 方法 Windows Media Player，MediaCollection 類別
- MediaCollection 類別 Windows Media Player，getPlaylistByQuery 方法
topic_type:
- apiref
api_name:
- MediaCollection.getPlaylistByQuery
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 50b57d4303ba8784f912db9570faacb26d01677d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "107001559"
---
# <a name="mediacollectiongetplaylistbyquery-method"></a>MediaCollection. getPlaylistByQuery 方法

**GetPlaylistByQuery** 方法會抓取包含符合查詢準則之 **媒體** 物件的 **播放清單** 物件。

## <a name="syntax"></a>語法


```JScript
retVal = MediaCollection.getPlaylistByQuery(
  query,
  mediaType,
  sortAttribute,
  sortAscending
)
```



## <a name="parameters"></a>參數

<dl> <dt>

*查詢* \[在\]
</dt> <dd>

**查詢** 物件，定義用來建立播放清單的條件。

</dd> <dt>

*媒體媒體* \[在\]
</dt> <dd>

包含媒體類型的 **字串**。 必須包含下列其中一個值：「音訊」、「影片」、「相片」、「播放清單」或「其他」。

</dd> <dt>

*sortAttribute* \[在\]
</dt> <dd>

包含用於排序之屬性名稱的 **字串**。 空字串 ( "" ) 表示不套用排序。

</dd> <dt>

*sortAscending* \[在\]
</dt> <dd>

**布林** 值，表示播放清單必須以遞增順序排序。

</dd> </dl>

## <a name="return-value"></a>傳回值

這個方法會傳回 **播放清單** 物件。

## <a name="remarks"></a>備註

使用 **查詢** 的複合查詢不區分大小寫。

當 *查詢* 參數所指定的複合查詢包含以「 **媒體** 類型」（attribute）為基礎的條件時，就會忽略該條件。 [ *媒體* ] 參數的值一律會使用。 例如，如果複合查詢包含「媒體的等於音訊」條件，而「 *媒體媒體* 」參數的值為「影片」，則產生的播放清單只會包含影片專案。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|------------------------------------------------------------------------------------|
| 版本<br/> | Windows Media Player 11。<br/>                                                |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**MediaCollection 物件**](mediacollection-object.md)
</dt> <dt>

[**媒體屬性**](mediatype-attribute.md)
</dt> <dt>

[**Query 物件**](query-object.md)
</dt> </dl>

 

 





