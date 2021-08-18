---
description: FramesPerSecond 屬性會抓取目前 DVD 標題的影片畫面播放速率。
ms.assetid: c5d36308-1447-4636-9b3a-4a3f93d27789
title: FramesPerSecond 屬性
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 96a883f031680a57711fa092f29bc9ecbd76cb1a017c03f80337959050e62cd2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119015666"
---
# <a name="framespersecond-property"></a>FramesPerSecond 屬性

> [!Note]  
> 此元件可在 Microsoft Windows 2000、Windows XP 和 Windows Server 2003 作業系統中使用。 它在後續版本中可能會變更或無法使用。

 

屬性會抓取 `FramesPerSecond` 目前 DVD 標題的影片畫面播放速率。

``` syntax
[ iFramesPerSec = ] MSWebDVD.FramesPerSecond
```

## <a name="return-value"></a>傳回值

傳回代表影片畫面播放速率的整數值;每秒25或30個畫面格。

## <a name="remarks"></a>備註

這個屬性是唯讀的，沒有預設值。 NTSC 視訊訊號會在每秒30個畫面上顯示。 PAL 以每秒25個畫面顯示。 光碟會編碼為在 NTSC 或 PAL 上播放，但無法在兩者上播放。

 

 



