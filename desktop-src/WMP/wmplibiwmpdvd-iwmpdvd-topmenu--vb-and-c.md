---
title: IWMPDVD topMenu 方法
description: TopMenu 方法會停止播放，並顯示目前標題的上方 (或根) 功能表。
ms.assetid: d6eb6311-167d-4cc1-b445-4e3d3e111e43
keywords:
- topMenu 方法 Windows Media Player
- topMenu 方法 Windows Media Player，IWMPDVD 介面
- IWMPDVD 介面 Windows Media Player，topMenu 方法
topic_type:
- apiref
api_name:
- IWMPDVD.topMenu
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0d59bf126a026626cc7f1ba87ea9d0eb94bd1a91
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106996464"
---
# <a name="iwmpdvdtopmenu-method"></a>IWMPDVD：： topMenu 方法

**TopMenu** 方法會停止播放，並顯示目前標題的上方 (或根) 功能表。

## <a name="syntax"></a>語法


```CSharp
public void topMenu();
```


```VB

Public Sub topMenu()
Implements IWMPDVD.topMenu
```





## <a name="parameters"></a>參數

這個方法沒有任何參數。

## <a name="return-value"></a>傳回值

這個方法不會傳回值。

## <a name="remarks"></a>備註

每個 DVD 的撰寫方式不同。 DVD 必須包含功能表，這個方法才能運作。 某些 Dvd 的撰寫方式是讓 **topMenu** 和 **IWMPDVD titleMenu** 方法開啟相同的功能表。 **TopMenu** 方法通常會叫用頂端 (或根) 功能表，但如果沒有可用的根功能表，它可能會叫用標題功能表。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| 版本<br/>   | Windows Media Player 9 系列或更新版本<br/>                                                                      |
| 命名空間<br/> | **WMPLib**<br/>                                                                                                  |
| 組件<br/>  | <dl> <dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**IWMPDVD 介面 (VB 和 c # )**](iwmpdvd--vb-and-c.md)
</dt> <dt>

[**IWMPDVD. titleMenu (VB 和 c # )**](wmplibiwmpdvd-iwmpdvd-titlemenu--vb-and-c.md)
</dt> </dl>

 

 





