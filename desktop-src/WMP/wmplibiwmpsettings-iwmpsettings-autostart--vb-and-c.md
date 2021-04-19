---
title: IWMPSettings autoStart 屬性
description: AutoStart 屬性會取得或設定值，指出目前的媒體專案是否會自動開始播放。
ms.assetid: 01a1cb78-9951-478a-8ea3-1ae06164beab
keywords:
- autoStart 屬性 Windows Media Player
- autoStart 屬性 Windows Media Player，IWMPSettings 介面
- IWMPSettings 介面 Windows Media Player、autoStart 屬性
topic_type:
- apiref
api_name:
- IWMPSettings.autoStart
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: aaf6c1fb43107df11462737286e26fa7801360d0
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106997774"
---
# <a name="iwmpsettingsautostart-property"></a>IWMPSettings：： autoStart 屬性

**AutoStart** 屬性會取得或設定值，指出目前的媒體專案是否會自動開始播放。

## <a name="syntax"></a>Syntax


```CSharp
public System.Boolean autoStart {get; set;}
```


```VB

Public Property autoStart As System.Boolean
```





## <a name="property-value"></a>屬性值

System.string **值，** 指出目前的媒體專案是否會自動開始播放。 預設值為 **True**。

## <a name="remarks"></a>備註

如果 **自動啟動** 設定為 **true** **，則在** 設定 **AxWindowsMediaPlayer****時，會** 開始播放媒體專案。 否則，在呼叫 **IWMPControls** 方法之前，媒體專案將不會開始播放。

除非您在指定媒體專案之前立即將 **自動啟動** 設定為 **true** ，否則您不應該依賴這項設定來替代使用 **IWMPControls** 方法。

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

[**AxWindowsMediaPlayer. currentPlaylist (VB 和 c # )**](axwmplib-axwindowsmediaplayer-currentplaylist--vb-and-c.md)
</dt> <dt>

[**AxWindowsMediaPlayer (VB 和 c # )**](axwmplib-axwindowsmediaplayer-url--vb-and-c.md)
</dt> <dt>

[**IWMPControls (VB 和 c # )**](wmplibiwmpcontrols-iwmpcontrols-play--vb-and-c.md)
</dt> <dt>

[**IWMPSettings 介面 (VB 和 c # )**](iwmpsettings--vb-and-c.md)
</dt> </dl>

 

 





