---
title: IWMPMediaCollection add 方法
description: Add 方法會將新的媒體專案或播放清單新增至程式庫。 |IWMPMediaCollection add 方法
ms.assetid: a3539646-797b-4481-a31e-86771f3633a9
keywords:
- 新增方法 Windows Media Player
- 新增方法 Windows Media Player，IWMPMediaCollection 介面
- IWMPMediaCollection 介面 Windows Media Player，add 方法
topic_type:
- apiref
api_name:
- IWMPMediaCollection.add
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 778850da4094d8ac745018b115248de9008d15339b7ffee75de177cf957d3fc2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119861156"
---
# <a name="iwmpmediacollectionadd-method"></a>IWMPMediaCollection：： add 方法

**Add** 方法會將新的媒體專案或播放清單新增至程式庫。

## <a name="syntax"></a>語法


```CSharp
public IWMPMedia add(
  System.String bstrURL
);
```


```VB

Public Function add( _
  ByVal bstrURL As System.String _
) As IWMPMedia
Implements IWMPMediaCollection.add
```





## <a name="parameters"></a>參數

<dl> <dt>

*bstrURL* \[在\]
</dt> <dd>

指定媒體專案或播放清單位置之 URL 的 **system.string** 。

</dd> </dl>

## <a name="return-value"></a>傳回值

所加入之專案或播放清單的 **WMPLib. IWMPMedia** 介面。

## <a name="remarks"></a>備註

這個方法會在指定路徑的情況下，將現有的媒體專案或播放清單載入至程式庫。 這個方法不會移動或變更檔案。 如果指定了不正確本機路徑，這個方法將會失敗，但在新增至程式庫之前，不會檢查媒體專案的有效性。

這個方法會接受靜態和自動播放清單檔案。 **IWMPPlaylistCollection. importPlaylist** 方法也可以用來將靜態播放清單新增至程式庫。

在呼叫這個方法之前，您必須擁有程式庫的完整存取權。 如需詳細資訊，請參閱連結 [庫存取](library-access.md)。

## <a name="examples"></a>範例

下列範例會將三個媒體物件新增至 Windows Media Player 媒體集合。 AxWMPLib. AxWindowsMediaPlayer 物件是以名為 player 的變數來表示。


```CSharp
// Adding a media object using a website.
player.mediaCollection.add("https://www.proseware.com/Media/Laure.wma");

// Adding a media object from a local network.
// Either use the @ symbol to denote a quoted string literal or add additional
// backlashes as an escape for every original backslash.
player.mediaCollection.add(@"\\yourservername\Public\Jeanne.wma");

// Adding a media object from a file on a local drive.
// Either use the @ symbol to denote a quoted string literal or add additional
// backlashes as an escape for every original backslash.
player.mediaCollection.add(@"C:\WMSDK\WMPSDK\samples\media\house.wma");
```


```VB

' Adding a media object using a website.
player.mediaCollection.add(&quot;http:&#39;www.proseware.com/Media/Laure.wma&quot;)

&#39; Adding a media object from a local network.
player.mediaCollection.add(&quot;\\yourservername\Public\Jeanne.wma&quot;)

&#39; Adding a media object from a file on a local drive.
player.mediaCollection.add(&quot;C:\WMSDK\WMPSDK\samples\media\house.wma&quot;)
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

[**IWMPMediaCollection 移除 (VB 和 c # )**](wmplibiwmpmediacollection-iwmpmediacollection-remove--vb-and-c.md)
</dt> <dt>

[**IWMPPlaylistCollection. importPlaylist (VB 和 c # )**](wmplibiwmpplaylistcollection-iwmpplaylistcollection-importplaylist--vb-and-c.md)
</dt> </dl>

 

 





