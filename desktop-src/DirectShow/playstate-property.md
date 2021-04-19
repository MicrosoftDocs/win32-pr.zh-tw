---
description: PlayState 屬性會捕獲 MSWebDVD 物件的目前狀態。
ms.assetid: ffe71c3f-f8c2-45cc-84bf-e937cfbbe7b9
title: PlayState 屬性
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9d8c699ce3f232f9afc14472f0308fa65adc6abb
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "106990918"
---
# <a name="playstate-property"></a>PlayState 屬性

> [!Note]  
> 此元件可用於 Microsoft Windows 2000、Windows XP 及 Windows Server 2003 作業系統。 它在後續版本中可能會變更或無法使用。

 

`PlayState`屬性會捕獲 **MSWebDVD** 物件的目前狀態。

``` syntax
[ iState = ] MSWebDVD.PlayState
```

## <a name="return-value"></a>傳回值

傳回整數值，代表 DVD 導覽器的目前狀態。



| 傳回碼 | Description   |
|-------------|---------------|
| -2          | 未定義     |
| -1          | 未初始化： |
| 0           | 已停止       |
| 1           | 已暫停        |
| 2           | 執行中       |



 

## <a name="remarks"></a>備註

這個屬性是唯讀的，沒有預設值。

**MSWebDVD** 物件可控制 [DirectShow dvd 瀏覽器] 篩選器，其會執行 DVD 流覽的實際工作。 這實際上是此屬性所參考 DVD 導覽器的狀態。 DVD 導覽器可以是數種狀態的其中一種，如上面所述。 `PlayState`屬性可以用來做為診斷工具，但通常不會有任何原因讓腳本應用程式監視 DVD 導覽器的狀態。

 

 



