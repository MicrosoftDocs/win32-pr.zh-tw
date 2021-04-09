---
description: PlayForwards 方法會從目前位置開始，以指定的速度向前播放。
ms.assetid: 4f1a3e74-b343-413d-8df7-6c4bea39c62d
title: PlayForwards 方法
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 10d49d8d6d80613c4dd5b2b8a374002b37d9baa4
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "103688075"
---
# <a name="playforwards-method"></a>PlayForwards 方法

> [!Note]  
> 此元件可用於 Microsoft Windows 2000、Windows XP 及 Windows Server 2003 作業系統。 它在後續版本中可能會變更或無法使用。

 

`PlayForwards`方法會從目前位置開始，以指定的速度向前播放。

``` syntax
MSWebDVD.PlayForwards(nSpeed)
```

## <a name="parameters"></a>參數

<dl> <dt>

<span id="nSpeed"></span><span id="nspeed"></span><span id="NSPEED"></span>*nSpeed*
</dt> <dd>

指定以整數值播放的速度。 此值為乘數，1.0 是正常的播放速度;2.0 是雙速度、0.5 為半快，依此類推。 當 **nSpeed** 不等於1.0 時，會將音訊靜音，並關閉子圖片。

</dd> </dl>

## <a name="return-value"></a>傳回值

沒有傳回值。

## <a name="see-also"></a>另請參閱

<dl> <dt>

[**PlayBackwards**](playbackwards-method.md)
</dt> </dl>

 

 



