---
description: PlayState 屬性會捕獲 MSWebDVD 物件的目前狀態。
ms.assetid: ffe71c3f-f8c2-45cc-84bf-e937cfbbe7b9
title: PlayState 屬性
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4b66ae0ddfb1a8ceb296ec647a0149a42de68f635ffd198d6ba6609ff11e4888
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120102348"
---
# <a name="playstate-property"></a>PlayState 屬性

> [!Note]  
> 此元件可在 Microsoft Windows 2000、Windows XP 和 Windows Server 2003 作業系統中使用。 它在後續版本中可能會變更或無法使用。

 

`PlayState`屬性會捕獲 **MSWebDVD** 物件的目前狀態。

``` syntax
[ iState = ] MSWebDVD.PlayState
```

## <a name="return-value"></a>傳回值

傳回整數值，代表 DVD 導覽器的目前狀態。



| 傳回碼 | 描述   |
|-------------|---------------|
| -2          | 未定義     |
| -1          | 未初始化： |
| 0           | 已停止       |
| 1           | 已暫停        |
| 2           | 執行中       |



 

## <a name="remarks"></a>備註

這個屬性是唯讀的，沒有預設值。

**MSWebDVD** 物件控制 DirectShow dvd 導覽器篩選器，它會執行 dvd 流覽的實際工作。 這實際上是此屬性所參考 DVD 導覽器的狀態。 DVD 導覽器可以是數種狀態的其中一種，如上面所述。 `PlayState`屬性可以用來做為診斷工具，但通常不會有任何原因讓腳本應用程式監視 DVD 導覽器的狀態。

 

 



