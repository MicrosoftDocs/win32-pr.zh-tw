---
description: Play 方法會播放目前的 DVD 標題。
ms.assetid: fe9dc266-5b12-479d-85cb-50cc6bb9d580
title: 'Play 方法 (DirectShow) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f62323c9c86be476a35977dadf554bbfca3bca91
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "104509985"
---
# <a name="play-method-directshow"></a>Play 方法 (DirectShow) 

> [!Note]  
> 此元件可用於 Microsoft Windows 2000、Windows XP 及 Windows Server 2003 作業系統。 它在後續版本中可能會變更或無法使用。

 

`Play`方法會播放目前的 DVD 標題。

``` syntax
MSWebDVD.Play()
```

## <a name="return-value"></a>傳回值

沒有傳回值。

## <a name="remarks"></a>備註

如果播放暫停或停止，且 [**EnableResetOnStop**](enableresetonstop-property.md) 為 true，則呼叫 **Play** 將會在目前的位置繼續以正常速度播放。 如果播放已停止，且 **EnableResetOnStop** 為 false，則呼叫 **Play** 將會導致光碟在第一個標題的開頭開始播放。

## <a name="see-also"></a>另請參閱

<dl> <dt>

[**繼續**](resume-method.md)
</dt> </dl>

 

 



