---
description: PlayPeriodInTitleAutoStop 方法會在指定的時間點開始播放指定的標題，直到指定的停止時間為止。
ms.assetid: 0c4df76d-3991-4a6c-a8e5-5fd713eeffc2
title: PlayPeriodInTitleAutoStop 方法
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d05899b66b7f1a11f8f5b177d311b9634a52595b
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "103846144"
---
# <a name="playperiodintitleautostop-method"></a>PlayPeriodInTitleAutoStop 方法

> [!Note]  
> 此元件可用於 Microsoft Windows 2000、Windows XP 及 Windows Server 2003 作業系統。 它在後續版本中可能會變更或無法使用。

 

方法會在指定的 `PlayPeriodInTitleAutoStop` 時間點開始播放指定的標題，直到指定的停止時間為止。

``` syntax
MSWebDVD.PlayPeriodInTitleAutoStop(iTitle, sStartTime, sEndTime)
```

## <a name="parameters"></a>參數

<dl> <dt>

<span id="iTitle"></span><span id="ititle"></span><span id="ITITLE"></span>*iTitle*
</dt> <dd>

將標題指定為整數。

</dd> <dt>

<span id="sStartTime"></span><span id="sstarttime"></span><span id="SSTARTTIME"></span>*sStartTime*
</dt> <dd>

將開始時間指定為 "hh： mm： ss： ff" 格式的字串 (指定小時、分鐘、秒、畫面格) 。

</dd> <dt>

<span id="sEndTime"></span><span id="sendtime"></span><span id="SENDTIME"></span>*sEndTime*
</dt> <dd>

以 "hh： mm： ss： ff" 格式將結束時間指定為字串。

</dd> </dl>

## <a name="return-value"></a>傳回值

沒有傳回值。

## <a name="see-also"></a>另請參閱

<dl> <dt>

[**PlayChaptersAutoStop**](playchaptersautostop-method.md)
</dt> </dl>

 

 



