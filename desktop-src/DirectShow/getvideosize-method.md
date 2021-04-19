---
description: GetVideoSize 方法會抓取原生的影片維度。
ms.assetid: 50db2c15-4064-4d18-94f0-f6cf05f1d236
title: GetVideoSize 方法
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 89b96d01c3f22eaae78a442f3496f3c7c7416eac
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "106972954"
---
# <a name="getvideosize-method"></a>GetVideoSize 方法

> [!Note]  
> 此元件可用於 Microsoft Windows 2000、Windows XP 及 Windows Server 2003 作業系統。 它在後續版本中可能會變更或無法使用。

 

方法會抓取 `GetVideoSize` 原生的影片維度。

``` syntax
[ oSizeRect = ] MSWebDVD.GetVideoSize()
```

## <a name="return-value"></a>傳回值

傳回 [DVDRect](dvdrect-object.md) 物件，其中包含四個讀取/寫入屬性： (左上角) x; (左上角) y、寬度和高度。 **X** 和 **y** 屬性會設定為零，而其他兩個屬性會反映 cd 上所撰寫的影片矩形的寬度和高度。

 

 



