---
title: IWMPSettings volume 屬性
description: Volume 屬性會取得或設定目前的播放磁片區。
ms.assetid: cff4fe70-9ca2-4419-bfc3-d622e8c72756
keywords:
- 磁片區屬性 Windows Media Player
- volume 屬性 Windows Media Player，IWMPSettings 介面
- IWMPSettings 介面 Windows Media Player，磁片區屬性
topic_type:
- apiref
api_name:
- IWMPSettings.volume
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a2077547dd00b5c75b6ca77a966190db2bb3bb1bcde61d1f5c5b84c794af84e3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118568395"
---
# <a name="iwmpsettingsvolume-property"></a>IWMPSettings：： volume 屬性

**Volume** 屬性會取得或設定目前的播放磁片區。

## <a name="syntax"></a>Syntax


```CSharp
public System.Int32 volume {get; set;}
```


```VB

Public Property volume As System.Int32
```





## <a name="property-value"></a>屬性值

為磁片區層級的 **system.object** ，範圍從0到100。

## <a name="remarks"></a>備註

值為零，表示沒有任何磁片區 (靜音) 。 值為100時，會指定完整磁片區。 如果未指定此屬性的值，則預設為針對 Windows Media Player 所建立的最後一個磁片區設定。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| 版本<br/>   | Windows Media Player 9 系列或更新版本<br/>                                                                      |
| 命名空間<br/> | **WMPLib**<br/>                                                                                                  |
| 組件<br/>  | <dl> <dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**IWMPSettings 介面 (VB 和 c # )**](iwmpsettings--vb-and-c.md)
</dt> </dl>

 

 





