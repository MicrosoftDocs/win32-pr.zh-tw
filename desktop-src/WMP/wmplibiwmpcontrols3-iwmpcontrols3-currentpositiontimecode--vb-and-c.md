---
title: IWMPControls3 currentPositionTimecode 屬性
description: CurrentPositionTimecode 屬性會使用時間碼格式，取得或設定目前媒體專案中的目前位置。 這個屬性目前支援 SMPTE 時間代碼。
ms.assetid: 035b812c-e976-4b4e-b4e5-820653257732
keywords:
- currentPositionTimecode 屬性 Windows Media Player
- currentPositionTimecode 屬性 Windows Media Player，IWMPControls3 介面
- IWMPControls3 介面 Windows Media Player，currentPositionTimecode 屬性
topic_type:
- apiref
api_name:
- IWMPControls3.currentPositionTimecode
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7660e6dc2690c310cf06f64e38190dc1cb3f24ab
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "107000970"
---
# <a name="iwmpcontrols3currentpositiontimecode-property"></a>IWMPControls3：： currentPositionTimecode 屬性

**CurrentPositionTimecode** 屬性會使用時間碼格式，取得或設定目前媒體專案中的目前位置。 這個屬性目前支援 SMPTE 時間代碼。

## <a name="syntax"></a>Syntax


```CSharp
public System.String currentPositionTimecode {get; set;}
```


```VB

Public Property currentPositionTimecode As System.String
```





## <a name="property-value"></a>屬性值

作為 SMPTE 時間代碼的 **system.string** 。

## <a name="remarks"></a>備註

SMPTE 時間程式碼提供一種標準方式來識別個別的影片畫面，這對同步播放很有用。 如果數位媒體檔案支援 SMPTE 時間代碼，Windows Media Player 可以取出目前時間代碼位置資訊，或搜尋特定時間代碼所識別的影片畫面。

SMPTE 時間代碼會依時數、分鐘數、秒數和框架數來識別特定的畫面格，以將其與特定的參考框架（指定為時間0）隔開。 通常，時間為零的框架是檔案的開頭，而特定的 SMPTE 時間代碼值代表自檔案開始以來經過的時間。

時間碼的格式 \[ *範圍* 為 \] *hh*：*mm*：*ss*。*ff* 的 \[ *範圍* \] 代表範圍，hh 代表小時， *mm* 代表分鐘， *ss* 代表秒，而 *ff* 代表畫面格。 設定 **currentPositionTimecode** 的值時，您必須包含全部八位數，並使用零做為預留位置。

\[*範圍* \]對應至 Windows Media Format **WMT 時間 \_ 碼 \_ 延伸模組 \_ 資料** 結構的 **wRange** 成員。 如需時間碼範圍的詳細資訊，請參閱 Windows Media Format SDK。

只有包含 SMPTE 時間程式碼資訊的檔案才支援設定和取得 **currentPositionTimecode** 。

## <a name="examples"></a>範例

下列程式碼範例會將 **currentPositionTimecode** 指定為1小時、零分鐘、30秒和5個框架。 **AxWMPLib. AxWindowsMediaPlayer** 物件是以名為 player 的變數來表示。


```CSharp
// Cast the interface returned by player.Ctlcontrols to an IWMPControls3 interface
// so that you can use the currentPositionTimecode property.
WMPLib.IWMPControls3 controls = (WMPLib.IWMPControls3)player.Ctlcontrols;

// Seek to a frame using SMPTE time code.
controls.currentPositionTimecode = "[00000]01:00:30.05";
```


```VB

' Cast the interface returned by player.Ctlcontrols to an IWMPControls3 interface
&#39; so that you can use the currentPositionTimecode property.
Dim controls As WMPLib.IWMPControls3 = player.Ctlcontrols

&#39; Seek to a frame using SMPTE time code.
Controls.currentPositionTimecode = &quot;[00000]01:00:30.05&quot;
```





## <a name="requirements"></a>規格需求



| 需求 | 值 |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| 版本<br/>   | Windows Media Player 9 系列或更新版本<br/>                                                                      |
| 命名空間<br/> | **WMPLib**<br/>                                                                                                  |
| 組件<br/>  | <dl> <dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**IWMPControls3 介面 (VB 和 c # )**](iwmpcontrols3--vb-and-c.md)
</dt> </dl>

 

 





