---
title: IWMPDVD titleMenu 方法
description: TitleMenu 方法會停止播放並顯示標題功能表。
ms.assetid: 28714644-12c4-46eb-95fc-70091624f6dd
keywords:
- titleMenu 方法 Windows Media Player
- titleMenu 方法 Windows Media Player，IWMPDVD 介面
- IWMPDVD 介面 Windows Media Player，titleMenu 方法
topic_type:
- apiref
api_name:
- IWMPDVD.titleMenu
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ff485cd09915ec9acb076d2c06a8aa28c3549bf6527495e5e32d4a01d483285a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120000458"
---
# <a name="iwmpdvdtitlemenu-method"></a>IWMPDVD：： titleMenu 方法

**TitleMenu** 方法會停止播放並顯示標題功能表。

## <a name="syntax"></a>語法


```CSharp
public void titleMenu();
```


```VB

Public Sub titleMenu()
Implements IWMPDVD.titleMenu
```





## <a name="parameters"></a>參數

這個方法沒有任何參數。

## <a name="return-value"></a>傳回值

這個方法不會傳回值。

## <a name="remarks"></a>備註

每個 DVD 的撰寫方式不同。 DVD 必須包含功能表，這個方法才能運作。 撰寫一些 Dvd，讓 **IWMPDVD. topMenu** 和 **titleMenu** 方法開啟相同的功能表。 **TitleMenu** 方法通常會叫用標題功能表，但如果沒有可用的標題功能表，它可能會叫用頂端功能表。

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

[**IWMPDVD. topMenu (VB 和 c # )**](wmplibiwmpdvd-iwmpdvd-topmenu--vb-and-c.md)
</dt> </dl>

 

 





