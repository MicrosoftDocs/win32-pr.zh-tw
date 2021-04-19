---
title: IWMPCdromBurn burnPlaylist 屬性
description: BurnPlaylist 屬性會取得要燒錄到 CD 的目前播放清單。
ms.assetid: 973032de-7249-4ccd-9909-ccc888f4490f
keywords:
- burnPlaylist 屬性 Windows Media Player
- burnPlaylist 屬性 Windows Media Player，IWMPCdromBurn 介面
- IWMPCdromBurn 介面 Windows Media Player，burnPlaylist 屬性
topic_type:
- apiref
api_name:
- IWMPCdromBurn.burnPlaylist
- IWMPCdromBurn.get_burnPlaylist
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cae095696b9c106926fb7f363430574b2eb87cea
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106983095"
---
# <a name="iwmpcdromburnburnplaylist-property"></a>IWMPCdromBurn：： burnPlaylist 屬性

**BurnPlaylist** 屬性會取得要燒錄到 CD 的目前播放清單。

這個屬性是唯讀的。

## <a name="syntax"></a>語法


```CSharp
public IWMPPlaylist burnPlaylist {get;}
```


```VB

Public ReadOnly Property burnPlaylist As IWMPPlaylist
```





## <a name="property-value"></a>屬性值

要燒錄之播放清單的 **WMPLib IWMPPlaylist** 介面。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| 版本<br/>   | Windows Media Player 11<br/>                                                                                     |
| 命名空間<br/> | **WMPLib**<br/>                                                                                                  |
| 組件<br/>  | <dl> <dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**IWMPCdromBurn 介面 (VB 和 c # )**](iwmpcdromburn--vb-and-c.md)
</dt> <dt>

[**IWMPPlaylist 介面 (VB 和 c # )**](iwmpplaylist--vb-and-c.md)
</dt> </dl>

 

 





