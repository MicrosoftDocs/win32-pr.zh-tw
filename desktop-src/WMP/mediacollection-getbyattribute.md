---
title: MediaCollection. getByAttribute 方法
description: GetByAttribute 方法會抓取媒體專案的播放清單，其中包含指定之屬性的指定值。
ms.assetid: a89f9c52-c655-4420-858e-c0eed661856f
keywords:
- getByAttribute 方法 Windows Media Player
- getByAttribute 方法 Windows Media Player，MediaCollection 類別
- MediaCollection 類別 Windows Media Player，getByAttribute 方法
topic_type:
- apiref
api_name:
- MediaCollection.getByAttribute
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f942f0718202d6c3e509b177c34c4c4be20c058b1e74991fa0ae89955d7711d8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118996307"
---
# <a name="mediacollectiongetbyattribute-method"></a>MediaCollection. getByAttribute 方法

**GetByAttribute** 方法會抓取媒體專案的播放清單，其中包含指定之屬性的指定值。

## <a name="syntax"></a>語法


```JScript
retVal = MediaCollection.getByAttribute(
  attribute,
  value
)
```



## <a name="parameters"></a>參數

<dl> <dt>

*屬性* \[在\]
</dt> <dd>

**字串** ，表示要搜尋的屬性名稱。 如需 Windows Media Player 所支援之屬性的詳細資訊，請參閱 Windows Media Player[屬性參考](attribute-reference.md)。

</dd> <dt>

*值* \[在\]
</dt> <dd>

**字串** ，表示屬性應該具有的值。

</dd> </dl>

## <a name="return-value"></a>傳回值

這個方法會傳回 **播放清單** 物件。

## <a name="remarks"></a>備註

這個方法可以用來建立符合資料庫中屬性值之媒體專案的一般查詢。 在使用者定義的屬性中，這非常有用。 如果屬性不存在，則會產生錯誤。

您可以使用這個方法來取得特定類型的所有媒體專案。 使用屬性名稱 "媒體" 和下列其中一個值：



| 值    | 描述                                                |
|----------|------------------------------------------------------------|
| 音訊    | 音樂和其他僅限音訊的專案。                          |
| 播放清單 | 以 **媒體** 物件表示的播放清單。                |
| radio    | 無線電站專案。 Windows Media Player 10 未使用。  |
| 影片    | 影片專案。                                               |
| 相片    | 相片專案。 需要 Windows Media Player 10。             |
| 其他    | 其他專案，例如 ASF 檔案或串流媒體的 Url。 |



 

若要使用此方法，需要有程式庫的讀取權限。 如需詳細資訊，請參閱連結 [庫存取](library-access.md)。

## <a name="examples"></a>範例

下列 JScript 範例會使用 *MediaCollection*。**getByAttribute** ，以名為 Triode 48 的演出者播放媒體櫃中的所有內容。 使用 ID = "Player" 建立 **player** 物件。


```JScript
// Get a playlist object filled with media items by a 
// particular artist.
var pl = Player.mediaCollection.getByAttribute("Artist", "Triode 48");

// Make the new playlist the current one.
Player.currentPlaylist = pl;

// Start Windows Media Player.
Player.controls.play();

```



## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|------------------------------------------------------------------------------------|
| 版本<br/> | Windows Media Player 7.0 版或更新版本。<br/>                              |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**MediaCollection 物件**](mediacollection-object.md)
</dt> <dt>

[**播放清單物件**](playlist-object.md)
</dt> <dt>

[**設定. mediaAccessRights**](settings-mediaaccessrights.md)
</dt> <dt>

[**設定. requestMediaAccessRights**](settings-requestmediaaccessrights.md)
</dt> </dl>

 

 





