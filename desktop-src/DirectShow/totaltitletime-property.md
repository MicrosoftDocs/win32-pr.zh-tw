---
description: TotalTitleTime 屬性會抓取目前標題的總播放時間。
ms.assetid: b05bb76b-d4ba-42e6-92ea-8e48f4c8f409
title: TotalTitleTime 屬性
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6fd809391394dc661745717ce7d173ad548dfd4d01206c07293024dc8e44a478
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119650848"
---
# <a name="totaltitletime-property"></a>TotalTitleTime 屬性

> [!Note]  
> 此元件可在 Microsoft Windows 2000、Windows XP 和 Windows Server 2003 作業系統中使用。 它在後續版本中可能會變更或無法使用。

 

`TotalTitleTime`屬性會捕獲目前標題的總播放時間。

``` syntax
[ sTotalTime = ] MSWebDVD.TotalTitleTime
```

## <a name="return-value"></a>傳回值

以字串格式傳回目前標題的總播放時間，格式為 "hh： mm： ss： ff"。

## <a name="remarks"></a>備註

這個屬性是唯讀的，沒有預設值。 傳回的字串將會是11個字元，格式為 "hh： mm： ss： ff" (小時、分鐘、秒、畫面格) 。

## <a name="see-also"></a>另請參閱

<dl> <dt>

[**PlayAtTime**](playattime-method.md)
</dt> <dt>

[**PlayAtTimeInTitle**](playattimeintitle-method.md)
</dt> </dl>

 

 



