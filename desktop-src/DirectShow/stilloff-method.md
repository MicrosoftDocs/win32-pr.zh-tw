---
description: StillOff 方法會繼續播放，正在取消仍處於模式。
ms.assetid: 62091aad-8a78-4543-a844-a4227aed81df
title: StillOff 方法
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d8986b62585768b83fc5737012a924e6cf33daf5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106985669"
---
# <a name="stilloff-method"></a>StillOff 方法

> [!Note]  
> 此元件可用於 Microsoft Windows 2000、Windows XP 及 Windows Server 2003 作業系統。 它在後續版本中可能會變更或無法使用。

 

`StillOff`方法會繼續播放，正在取消仍處於模式。

``` syntax
MSWebDVD.StillOff()
```

## <a name="return-value"></a>傳回值

沒有傳回值。

## <a name="remarks"></a>備註

當 [DVD 瀏覽器](dvd-navigator-filter.md) 遇到在光碟上撰寫的靜止畫面時，仍會進入模式。它會傳送 EC \_ DVD \_ 仍 \_ 在事件上，以通知您的應用程式。 由於使用者作業的不同，所以仍然模式與 DVD 導覽器處於暫停狀態的不同。 呼叫 `StillOff` 會從仍模式繼續播放，但不會在 DVD 導覽器處於暫停狀態時重新開機。

 

 



