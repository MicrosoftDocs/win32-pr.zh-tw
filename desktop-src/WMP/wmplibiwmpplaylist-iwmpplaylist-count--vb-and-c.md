---
title: IWMPPlaylist count 屬性
description: Count 屬性會取得播放清單中的媒體專案數目。
ms.assetid: dbff3c86-2d42-4d47-a5cb-b8199efac728
keywords:
- count 屬性 Windows Media Player
- count 屬性 Windows Media Player，IWMPPlaylist 介面
- IWMPPlaylist 介面 Windows Media Player，count 屬性
topic_type:
- apiref
api_name:
- IWMPPlaylist.count
- IWMPPlaylist.get_count
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: aad690278b45563395c926adb4d0329bff8a01c7e8ace2f25ff3fefdb9c39cee
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118568693"
---
# <a name="iwmpplaylistcount-property"></a>IWMPPlaylist：： count 屬性

**Count** 屬性會取得播放清單中的媒體專案數目。

這個屬性是唯讀的。

## <a name="syntax"></a>語法


```CSharp
public System.Int32 count {get;}
```


```VB

Public ReadOnly Property count As System.Int32
```





## <a name="property-value"></a>屬性值

一 **種** system.string，也就是播放清單中的媒體專案數目。

## <a name="remarks"></a>備註

使用這個屬性之前，您必須擁有程式庫的讀取權限。 如需詳細資訊，請參閱連結 [庫存取](library-access.md)。

如需使用這個屬性的範例程式碼，請參閱 [attributeCount](wmplibiwmpplaylist-iwmpplaylist-attributecount--vb-and-c.md) 屬性。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| 版本<br/>   | Windows Media Player 9 系列或更新版本<br/>                                                                      |
| 命名空間<br/> | **WMPLib**<br/>                                                                                                  |
| 組件<br/>  | <dl> <dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**IWMPPlaylist 介面 (VB 和 c # )**](iwmpplaylist--vb-and-c.md)
</dt> </dl>

 

 





