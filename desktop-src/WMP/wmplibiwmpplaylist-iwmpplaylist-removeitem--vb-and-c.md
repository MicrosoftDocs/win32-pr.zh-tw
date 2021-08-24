---
title: IWMPPlaylist removeItem 方法
description: RemoveItem 方法會從播放清單中移除指定的媒體專案。
ms.assetid: 8b5a4c34-863d-4963-97c8-cc5aa2223ab5
keywords:
- removeItem 方法 Windows Media Player
- removeItem 方法 Windows Media Player，IWMPPlaylist 介面
- IWMPPlaylist 介面 Windows Media Player，removeItem 方法
topic_type:
- apiref
api_name:
- IWMPPlaylist.removeItem
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 01ea9250cc7e368699a916b4c87f419fc5b0b66001a4d7ca12afd5587a0adda7
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119246423"
---
# <a name="iwmpplaylistremoveitem-method"></a>IWMPPlaylist：： removeItem 方法

**RemoveItem** 方法會從播放清單中移除指定的媒體專案。

## <a name="syntax"></a>語法


```CSharp
public void removeItem(
  IWMPMedia pIWMPMedia
);
```


```VB

Public Sub removeItem( _
  ByVal pIWMPMedia As IWMPMedia _
)
Implements IWMPPlaylist.removeItem
```





## <a name="parameters"></a>參數

<dl> <dt>

*pIWMPMedia* \[在\]
</dt> <dd>

代表要從播放清單中移除之媒體專案的 **WMPLib IWMPMedia** 介面。

</dd> </dl>

## <a name="return-value"></a>傳回值

這個方法不會傳回值。

## <a name="remarks"></a>備註

如果移除的專案是目前播放的播放軌，播放會停止，且播放清單中的下一個專案會變成目前的播放軌。

如果沒有下一個專案，則會使用前一個專案。 如果沒有其他專案，則 **AxWindowsMediaPlayer. currentMedia** 屬性會傳回 **Null**。

在呼叫這個方法之前，您必須擁有程式庫的完整存取權。 如需詳細資訊，請參閱連結 [庫存取](library-access.md)。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| 版本<br/>   | Windows Media Player 9 系列或更新版本<br/>                                                                      |
| 命名空間<br/> | **WMPLib**<br/>                                                                                                  |
| 組件<br/>  | <dl> <dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**AxWindowsMediaPlayer. currentMedia (VB 和 c # )**](axwmplib-axwindowsmediaplayer-currentmedia--vb-and-c.md)
</dt> <dt>

[**IWMPMedia 介面 (VB 和 c # )**](iwmpmedia--vb-and-c.md)
</dt> <dt>

[**IWMPPlaylist 介面 (VB 和 c # )**](iwmpplaylist--vb-and-c.md)
</dt> <dt>

[**IWMPPlaylist. insertItem (VB 和 c # )**](wmplibiwmpplaylist-iwmpplaylist-insertitem--vb-and-c.md)
</dt> <dt>

[**IWMPPlaylist (VB 和 c # ) 的專案**](iwmpplaylist-item--vb-and-c.md)
</dt> <dt>

[**IWMPSettings2. mediaAccessRights (VB 和 c # )**](wmplibiwmpsettings2-iwmpsettings2-mediaaccessrights--vb-and-c.md)
</dt> <dt>

[**IWMPSettings2. requestMediaAccessRights (VB 和 c # )**](wmplibiwmpsettings2-iwmpsettings2-requestmediaaccessrights--vb-and-c.md)
</dt> </dl>

 

 





