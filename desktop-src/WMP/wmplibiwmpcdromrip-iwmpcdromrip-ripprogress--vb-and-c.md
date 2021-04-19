---
title: IWMPCdromRip ripProgress 屬性
description: RipProgress 屬性會取得 CD 翻錄進度（完成的百分比）。
ms.assetid: 00d4f074-a16d-4c5f-930f-4411b90303f1
keywords:
- ripProgress 屬性 Windows Media Player
- ripProgress 屬性 Windows Media Player，IWMPCdromRip 介面
- IWMPCdromRip 介面 Windows Media Player，ripProgress 屬性
topic_type:
- apiref
api_name:
- IWMPCdromRip.ripProgress
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 113b9fc716698156aa4f7731a7b19888e0edf438
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106987170"
---
# <a name="iwmpcdromripripprogress-property"></a>IWMPCdromRip：： ripProgress 屬性

**RipProgress** 屬性會取得 CD 翻錄進度（完成的百分比）。

## <a name="syntax"></a>Syntax


```CSharp
public System.Int32 ripProgress {get; set;}
```


```VB

Public ReadOnly Property ripProgress As System.Int32
```





## <a name="property-value"></a>屬性值

作為進度值的 **system.object** 。 進度值的範圍是從0到100。

## <a name="remarks"></a>備註

進度值代表整個翻錄進程的完成百分比。 若要判斷特定追蹤的進度，請使用 [IWMPMedia getItemInfo](wmplibiwmpplaylist-iwmpplaylist-getiteminfo--vb-and-c.md) 搭配 **RipProgress** 作為屬性名稱。 若要取得目前正在翻錄之追蹤的索引，請使用 "CurrentRipTrackIndex" 做為屬性名稱來呼叫 IWMPPlaylist. getItemInfo。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| 版本<br/>   | Windows Media Player 11。<br/>                                                                                    |
| 命名空間<br/> | **WMPLib**<br/>                                                                                                  |
| 組件<br/>  | <dl> <dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**IWMPCdromRip 介面 (VB 和 c # )**](iwmpcdromrip--vb-and-c.md)
</dt> <dt>

[**將 CD 翻錄**](ripping-a-cd.md)
</dt> </dl>

 

 





