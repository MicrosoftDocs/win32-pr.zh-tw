---
description: CurrentDomain 屬性會捕獲 MSWebDVD 物件所在的 DVD 網域。
ms.assetid: 9d545438-9a3d-4c57-a3df-5e75af2e4d1b
title: CurrentDomain 屬性
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ead6d61cd622fceac2a4d133a0297892992e763a
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "104467727"
---
# <a name="currentdomain-property"></a>CurrentDomain 屬性

> [!Note]  
> 此元件可用於 Microsoft Windows 2000、Windows XP 及 Windows Server 2003 作業系統。 它在後續版本中可能會變更或無法使用。

 

`CurrentDomain`屬性會抓取 MSWebDVD 物件所在的 DVD 網域。

``` syntax
[ iDomain = ] MSWebDVD.CurrentDomain
```

## <a name="return-value"></a>傳回值

傳回代表目前網域的整數值。

## <a name="remarks"></a>備註

屬性的可能值為：



| 值 | 描述          |
|-------|----------------------|
| 1     | 初次播放           |
| 2     | 影片管理員功能表   |
| 3     | 影片標題設定功能表 |
| 4     | 標題                |
| 5     | 停止                 |



 

呼叫這個方法，以確保 DVD 導覽器位於您要呼叫之方法的有效網域中。 例如，在呼叫 [**PlayTitle**](playtitle-method.md)之前，請檢查 `CurrentDomain` 屬性，以確定 DVD 導覽器不在「停止」或「第一個播放」網域中。

 

 



