---
description: FullScreenMode 屬性會設定或抓取值，指出顯示器是否處於全螢幕模式。
ms.assetid: e4682f50-080c-4f38-b2ca-ce4ca6b746d7
title: FullScreenMode 屬性
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 103938afa6710b858329147eafadec4e06fd7d2ba244b896dd1ac39c74cd12c1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119015616"
---
# <a name="fullscreenmode-property"></a>FullScreenMode 屬性

> [!Note]  
> 此元件可在 Microsoft Windows 2000、Windows XP 和 Windows Server 2003 作業系統中使用。 它在後續版本中可能會變更或無法使用。

 

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

 

 



