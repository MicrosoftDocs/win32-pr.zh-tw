---
title: AxWindowsMediaPlayer. playlistCollection 屬性
description: PlaylistCollection 屬性會取得 IWMPPlaylistCollection 介面。
ms.assetid: f3c65f70-b58f-41c1-afe0-3a9d9c95561c
keywords:
- playlistCollection 屬性 Windows Media Player
- playlistCollection 屬性 Windows Media Player，AxWindowsMediaPlayer 類別
- AxWindowsMediaPlayer 類別 Windows Media Player，playlistCollection 屬性
topic_type:
- apiref
api_name:
- AxWindowsMediaPlayer.playlistCollection
api_location:
- AxInterop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6d646bec99c61032c0347d9d21df443c890837424255ebd687c15cc9f780a1d4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118581898"
---
# <a name="axwindowsmediaplayerplaylistcollection-property"></a>AxWindowsMediaPlayer. playlistCollection 屬性

PlaylistCollection 屬性會取得 **IWMPPlaylistCollection** 介面。

這個屬性是唯讀的。

## <a name="syntax"></a>語法


```CSharp
public IWMPPlaylistCollection playlistCollection {get;}
```


```VB

Public ReadOnly Property playlistCollection As IWMPPlaylistCollection
```





## <a name="property-value"></a>屬性值

WMPLib。**IWMPPlaylistCollection** 介面。

## <a name="remarks"></a>備註

若要取得這個屬性的值，需要有程式庫的讀取權限。 如需詳細資訊，請參閱連結 [庫存取](library-access.md)。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|----------------------|----------------------------------------------------------------------------------------------------------------------------|
| 版本<br/>   | Windows Media Player 9 系列或更新版本<br/>                                                                          |
| 命名空間<br/> | **AxWMPLib**<br/>                                                                                                    |
| 組件<br/>  | <dl> <dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**AxWindowsMediaPlayer 物件 (VB 和 c # )**](axwindowsmediaplayer-object--vb-and-c.md)
</dt> <dt>

[**IWMPPlaylistCollection 介面 (VB 和 c # )**](iwmpplaylistcollection--vb-and-c.md)
</dt> <dt>

[**IWMPSettings2. mediaAccessRights (VB 和 c # )**](wmplibiwmpsettings2-iwmpsettings2-mediaaccessrights--vb-and-c.md)
</dt> <dt>

[**IWMPSettings2. requestMediaAccessRights (VB 和 c # )**](wmplibiwmpsettings2-iwmpsettings2-requestmediaaccessrights--vb-and-c.md)
</dt> </dl>

 

 





