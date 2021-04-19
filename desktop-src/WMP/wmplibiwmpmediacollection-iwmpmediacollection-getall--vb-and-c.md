---
title: IWMPMediaCollection getAll 方法
description: GetAll 方法會傳回 IWMPPlaylist 介面，該介面對應至包含媒體櫃中所有媒體專案的播放清單。
ms.assetid: f2bbb4a4-7397-4c97-afd9-e8ee380af9da
keywords:
- getAll 方法 Windows Media Player
- getAll 方法 Windows Media Player，IWMPMediaCollection 介面
- IWMPMediaCollection 介面 Windows Media Player，getAll 方法
topic_type:
- apiref
api_name:
- IWMPMediaCollection.getAll
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: be08548ae29db12ded788f34563ef5e319c27d61
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106989250"
---
# <a name="iwmpmediacollectiongetall-method"></a>IWMPMediaCollection：： getAll 方法

**GetAll** 方法會傳回 **IWMPPlaylist** 介面，該介面對應至包含媒體櫃中所有媒體專案的播放清單。

## <a name="syntax"></a>語法


```CSharp
public IWMPPlaylist getAll();
```


```VB

Public Function getAll() As IWMPPlaylist
Implements IWMPMediaCollection.getAll
```





## <a name="parameters"></a>參數

這個方法沒有任何參數。

## <a name="return-value"></a>傳回值

播放清單的 **WMPLib IWMPPlaylist** 介面，其中包含所有要求的媒體專案。

## <a name="remarks"></a>備註

在呼叫這個方法之前，您必須擁有程式庫的讀取權限。 如需詳細資訊，請參閱連結 [庫存取](library-access.md)。

您有兩種方式可以取出 **IWMPMediaCollection** 介面，而 **getAll** 方法的行為取決於您所使用的兩種方式。 如果您藉由呼叫 [AxWindowsMediaPlayer](axwmplib-axwindowsmediaplayer-mediacollection--vb-and-c.md)來取出介面，則 **getAll** 方法會傳回媒體櫃中的所有媒體專案。 但是，如果您藉由呼叫 [IWMPLibrary](wmplibiwmplibrary-iwmplibrary-mediacollection--vb-and-c.md)來取出介面，則 **getAll** 方法只會傳回媒體櫃中的音訊專案。

## <a name="examples"></a>範例

下列範例會使用 **getAll** ，從媒體集合隨機播放媒體專案。 **AxWMPLib. AxWindowsMediaPlayer** 物件是以名為 player 的變數來表示。


```CSharp
// Create a random number generator. 
System.Random randGenerator = new System.Random();

// Store the count of all media items in the media collection.
int count = player.mediaCollection.getAll().count;

// Get a random integer using the count as the max value.
int rand = randGenerator.Next(count);

// Make the random media item the current media item.
player.currentMedia = player.mediaCollection.getAll().get_Item(rand);

// Play the media item.
player.Ctlcontrols.play();
```


```VB

' Create a random number generator. 
Dim randGenerator As System.Random = New System.Random()

&#39; Store the count of all media items in the media collection.
Dim count As Integer = player.mediaCollection.getAll().count

&#39; Get a random integer using the count as the max value.
Dim rand As Integer = randGenerator.Next(count)

&#39; Make the random media item the current media item.
player.currentMedia = player.mediaCollection.getAll().Item(rand)

&#39; Play the media item.
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
</dt> </dl>

 

 





