---
title: IWMPMediaCollection getByAttribute 方法
description: GetByAttribute 方法會傳回 IWMPPlaylist 介面，這個介面會對應到具有指定值的指定屬性。
ms.assetid: ece70a2c-38bc-4652-8319-efcde5f9720a
keywords:
- getByAttribute 方法 Windows Media Player
- getByAttribute 方法 Windows Media Player，IWMPMediaCollection 介面
- IWMPMediaCollection 介面 Windows Media Player，getByAttribute 方法
topic_type:
- apiref
api_name:
- IWMPMediaCollection.getByAttribute
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dd7adba98fbfa450cd938b56ec6d91598b918d0d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106993679"
---
# <a name="iwmpmediacollectiongetbyattribute-method"></a>IWMPMediaCollection：： getByAttribute 方法

**GetByAttribute** 方法會傳回 **IWMPPlaylist** 介面，這個介面會對應到具有指定值的指定屬性。

## <a name="syntax"></a>語法


```CSharp
public IWMPPlaylist getByAttribute(
  System.String bstrAttribute,
  System.String bstrValue
);
```


```VB

Public Function getByAttribute( _
  ByVal bstrAttribute As System.String, _
  ByVal bstrValue As System.String _
) As IWMPPlaylist
Implements IWMPMediaCollection.getByAttribute
```





## <a name="parameters"></a>參數

<dl> <dt>

*bstrAttribute* \[在\]
</dt> <dd>

指定之屬性的 **system.string** 。

</dd> <dt>

*bstrValue* \[在\]
</dt> <dd>

指定之值的 **system.string** 。

</dd> </dl>

## <a name="return-value"></a>傳回值

抓取之媒體專案的 **WMPLib IWMPPlaylist** 介面。

## <a name="remarks"></a>備註

這個方法可以用來建立符合程式庫中屬性值之媒體專案的一般查詢。 在使用者定義的屬性中，這非常有用。 如果屬性不存在，則會產生錯誤。

您可以使用這個方法來取得特定類型的所有媒體專案。 使用屬性名稱 **媒體** 名稱和下列其中一個值。



| 值    | 描述                                               |
|----------|-----------------------------------------------------------|
| 音訊    | 音樂和其他僅限音訊的專案                          |
| 其他    | 其他專案，例如 .asf 檔案或資料流程的 URL。 |
| 相片    | 相片專案。 需要 Windows Media Player 10。            |
| 播放清單 | 以媒體專案表示的播放清單。                     |
| radio    | 無線電站專案。 Windows Media Player 10 未使用。 |
| 影片    | 影片專案。                                              |



 

在呼叫這個方法之前，您必須擁有程式庫的讀取權限。 如需詳細資訊，請參閱連結 [庫存取](library-access.md)。

如需 Windows Media Player 所支援之屬性的詳細資訊，請參閱 [屬性參考](attribute-reference.md)。

您有兩種方式可以取出 **IWMPMediaCollection** 介面，而 **getByAttribute** 方法的行為取決於您所使用的兩種方式。 如果您藉由呼叫 [AxWindowsMediaPlayer](axwmplib-axwindowsmediaplayer-mediacollection--vb-and-c.md)來取出介面，則 **getByAttribute** 方法會傳回媒體櫃中的所有媒體專案。 但是，如果您藉由呼叫 [IWMPLibrary](wmplibiwmplibrary-iwmplibrary-mediacollection--vb-and-c.md)來取出介面，則 **getByAttribute** 方法只會傳回程式庫中具有指定之屬性和值的音訊專案。

## <a name="examples"></a>範例

下列程式碼範例會使用 **getByAttribute** ，以名為 Triode 48 的演出者播放媒體櫃中的所有內容。 **AxWMPLib. AxWindowsMediaPlayer** 物件是以名為 player 的變數來表示。


```CSharp
// Get an interface to a playlist that contains media items by a particular artist.
WMPLib.IWMPPlaylist pl = player.mediaCollection.getByAttribute("Artist", "Triode 48");

// Make the new playlist the current one.
player.currentPlaylist = pl;

// Play the media items in the current playlist. 
player.Ctlcontrols.play();
```


```VB

' Get an interface to a playlist that contains media items by a particular artist.
Dim pl As WMPLib.IWMPPlaylist = player.mediaCollection.getByAttribute(&quot;Artist&quot;, &quot;Triode 48&quot;)

&#39; Make the new playlist the current one.
player.currentPlaylist = pl

&#39; Play the media items in the current playlist. 
player.Ctlcontrols.play()
```





## <a name="requirements"></a>規格需求



| 需求 | 值 |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| 版本<br/>   | Windows Media Player 9 系列或更新版本<br/>                                                                      |
| 命名空間<br/> | **WMPLib**<br/>                                                                                                  |
| 組件<br/>  | <dl> <dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**IWMPMediaCollection 介面 (VB 和 c # )**](iwmpmediacollection--vb-and-c.md)
</dt> <dt>

[**IWMPPlaylist 介面 (VB 和 c # )**](iwmpplaylist--vb-and-c.md)
</dt> <dt>

[**IWMPPlaylistCollection. getAll (VB 和 c # )**](wmplibiwmpplaylistcollection-iwmpplaylistcollection-getall--vb-and-c.md)
</dt> </dl>

 

 





