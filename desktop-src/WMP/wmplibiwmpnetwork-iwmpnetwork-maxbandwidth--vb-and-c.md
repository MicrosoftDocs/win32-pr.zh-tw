---
title: IWMPNetwork maxBandwidth 屬性
description: MaxBandwidth 屬性會取得或設定允許的最大頻寬。
ms.assetid: ff7548d8-b80f-4cb4-bdd6-86d585fef329
keywords:
- maxBandwidth 屬性 Windows Media Player
- maxBandwidth 屬性 Windows Media Player，IWMPNetwork 介面
- IWMPNetwork 介面 Windows Media Player，maxBandwidth 屬性
topic_type:
- apiref
api_name:
- IWMPNetwork.maxBandwidth
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3620d609db0f1786da673923f54d726b3c99994a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106994152"
---
# <a name="iwmpnetworkmaxbandwidth-property"></a>IWMPNetwork：： maxBandwidth 屬性

**MaxBandwidth** 屬性會取得或設定允許的最大頻寬。

## <a name="syntax"></a>Syntax


```CSharp
public System.Int32 maxBandwidth {get; set;}
```


```VB

Public Property maxBandwidth As System.Int32
```





## <a name="property-value"></a>屬性值

最大頻寬的 **system.object** 。

## <a name="remarks"></a>備註

這個屬性沒有預設值。 當 Windows Media Player 現正播放時，可以指定此值，但在目前的媒體專案發行之前，您可以開啟另一個媒體專案，或呼叫 **AxWindowsMediaPlayer**，變更將不會生效。 Windows Media Player 嘗試達到可能的最高頻寬。 除非已設定此值，否則不會刻意減少頻寬。

這項設定有助於減少使用的頻寬量，特別是在多位元率 (MBR) 串流的情況下。 MBR 資料流程包含多個具有不同位速率的資料流程。 在某些情況下，您可能會想要使用比用戶端所需的位元速率低的資料流程。 在此情況下，使用 **IWMPNetwork. maxBandwidth** 屬性指定較低的位元速率，將會選取較低的位元速率串流。 例如，MBR 串流可能包含以每秒 20 kb 編碼的資料流程 (Kbps) 、37 Kbps 和 200 Kbps。 使用 **IWMPNetwork** 來指定 50000 (50 Kbps 的位元速率) 將會選取 37 kbps 資料流程，而不是 200 kbps 串流。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| 版本<br/>   | Windows Media Player 9 系列或更新版本<br/>                                                                      |
| 命名空間<br/> | **WMPLib**<br/>                                                                                                  |
| 組件<br/>  | <dl> <dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**AxWindowsMediaPlayer. close (VB 和 c # )**](axwmplib-axwindowsmediaplayer-close.md)
</dt> <dt>

[**IWMPNetwork 介面 (VB 和 c # )**](iwmpnetwork--vb-and-c.md)
</dt> </dl>

 

 





