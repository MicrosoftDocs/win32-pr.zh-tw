---
description: PlayBackwards 方法會從目前位置開始，以指定的速度向前播放。
ms.assetid: 7f8421e7-f835-4a10-a9c9-0e43de159e4f
title: PlayBackwards 方法
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b7236c225858d9508da0074ea64d104a50632b772302f42362dae373a987c352
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119748358"
---
# <a name="playbackwards-method"></a>PlayBackwards 方法

> [!Note]  
> 此元件可在 Microsoft Windows 2000、Windows XP 和 Windows Server 2003 作業系統中使用。 它在後續版本中可能會變更或無法使用。

 

`PlayBackwards`方法會從目前位置開始，以指定的速度向前播放。

``` syntax
MSWebDVD.PlayBackwards(nSpeed)
```

## <a name="parameters"></a>參數

<dl> <dt>

<span id="nSpeed"></span><span id="nspeed"></span><span id="NSPEED"></span>*nSpeed*
</dt> <dd>

指定要以數位的形式播放的速度。 這個數位是乘數，1.0 是正常的播放速度;2.0 是雙速度、0.5 為半快，依此類推。 當 **nSpeed** 不等於1.0 時，會將音訊靜音，並關閉子圖片。

</dd> </dl>

## <a name="return-value"></a>傳回值

沒有傳回值。

## <a name="see-also"></a>另請參閱

<dl> <dt>

[**PlayForwards**](playforwards-method.md)
</dt> </dl>

 

 



