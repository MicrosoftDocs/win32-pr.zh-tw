---
description: FullScreenMode 屬性會設定或抓取值，指出顯示器是否處於全螢幕模式。
ms.assetid: e4682f50-080c-4f38-b2ca-ce4ca6b746d7
title: FullScreenMode 屬性
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a96b3c0ca8261eb934e95eb7235b51e76e8c7579
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "104108537"
---
# <a name="fullscreenmode-property"></a>FullScreenMode 屬性

> [!Note]  
> 此元件可用於 Microsoft Windows 2000、Windows XP 及 Windows Server 2003 作業系統。 它在後續版本中可能會變更或無法使用。

 

`FullScreenMode`屬性會設定或抓取值，指出顯示器是否處於全螢幕模式。

``` syntax
[ bFullScreen = ] MSWebDVD.FullScreenMode
```

## <a name="return-value"></a>傳回值

傳回布林值，指出是否要啟用或停用全螢幕播放。

## <a name="remarks"></a>備註

這個屬性是讀取/寫入，預設值是 false。



| 值 | 描述                                            |
|-------|--------------------------------------------------------|
| true  | 啟用全螢幕播放。 這是預設值。 |
| false | 停用全螢幕播放。                          |



 

只有當 MSWebDVD 控制項以視窗模式執行時，才可使用全螢幕模式。

 

 



