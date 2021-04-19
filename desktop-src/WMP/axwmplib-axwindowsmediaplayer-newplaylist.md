---
title: AxWindowsMediaPlayer. [] 方法
description: '[] 方法會傳回新播放清單的 IWMPPlaylist 介面。'
ms.assetid: caee8ee5-6201-474d-a4cb-80e574f84f0b
keywords:
- '[] 方法 Windows Media Player'
- '[] 方法 Windows Media Player，AxWindowsMediaPlayer 類別'
- AxWindowsMediaPlayer 類別 Windows Media Player，[] 方法
topic_type:
- apiref
api_name:
- AxWindowsMediaPlayer.newPlaylist
api_location:
- AxInterop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a8dc82be7aae37b4c1334b79f84e9d607b4f73cb
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106984328"
---
# <a name="axwindowsmediaplayernewplaylist-method"></a>AxWindowsMediaPlayer. [] 方法

[] 方法會傳回新播放清單的 IWMPPlaylist 介面。

## <a name="syntax"></a>語法


```CSharp
public IWMPPlaylist newPlaylist(
  System.String bstrName,
  System.String bstrURL
);
```


```VB

Public Function newPlaylist( _
  ByVal bstrName As System.String, _
  ByVal bstrURL As System.String _
) As IWMPPlaylist
```





## <a name="parameters"></a>參數

<dl> <dt>

*bstrName* 
</dt> <dd>

**System.string** ，這是新播放清單的名稱。

</dd> <dt>

*bstrURL* 
</dt> <dd>

**System.string** ，此為用來初始化新播放清單之 Windows Media 中繼檔播放清單的 URL。

</dd> </dl>

## <a name="return-value"></a>傳回值

WMPLib IWMPPlaylist 介面，代表新建立的播放清單。

## <a name="remarks"></a>備註

如果 *bstrURL* 參數為 null 或長度為零的字串 ( "" ) ，這個方法會建立空的 **播放清單**。 如果 *bstrName* 參數是長度為零的字串 ( "" ) ，這個方法會套用目前的中繼檔名稱。

使用這個方法建立的新播放清單，不會新增至程式庫。 若要將新的播放清單新增至程式庫，請使用 IWMPPlaylistCollection。**importPlaylist** 或 IWMPPlaylistCollection。**[]**。 新增至程式庫時，會自動移除播放清單名稱中的任何前置或尾端空格。

由於程式庫允許多個具有相同名稱的播放清單，因此您可能會想要先檢查具有指定名稱的播放清單是否存在，然後再新增一個。

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

[**IWMPPlaylist 介面 (VB 和 c # )**](iwmpplaylist--vb-and-c.md)
</dt> <dt>

[**IWMPPlaylistCollection. importPlaylist (VB 和 c # )**](wmplibiwmpplaylistcollection-iwmpplaylistcollection-importplaylist--vb-and-c.md)
</dt> <dt>

[**IWMPPlaylistCollection. [] (VB 和 c # )**](wmplibiwmpplaylistcollection-iwmpplaylistcollection-newplaylist--vb-and-c.md)
</dt> </dl>

 

 





