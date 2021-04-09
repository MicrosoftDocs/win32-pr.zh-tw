---
description: ShowMenu 方法會在螢幕上顯示指定的功能表。
ms.assetid: 971c5bc3-a327-4840-8f3c-9a6573204ffb
title: ShowMenu 方法
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7c64b2a08c8881001cc47c972ad8cc865af8a174
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "103688071"
---
# <a name="showmenu-method"></a>ShowMenu 方法

> [!Note]  
> 此元件可用於 Microsoft Windows 2000、Windows XP 及 Windows Server 2003 作業系統。 它在後續版本中可能會變更或無法使用。

 

`ShowMenu`方法會在螢幕上顯示指定的功能表。

``` syntax
MSWebDVD.ShowMenu(iMenuID)
```

## <a name="parameters"></a>參數

<dl> <dt>

<span id="iMenuID"></span><span id="imenuid"></span><span id="IMENUID"></span>*iMenuID*
</dt> <dd>

將功能表識別碼指定為整數。



| 值 | 描述 |
|-------|-------------|
| 2     | 標題 (Top)  |
| 3     | Root        |
| 4     | 子圖片  |
| 5     | 音訊       |
| 6     | 角度       |
| 7     | 章節     |



 

</dd> </dl>

## <a name="return-value"></a>傳回值

沒有傳回值。

## <a name="remarks"></a>備註

DVD 功能表名稱可能有點令人困惑。 標題功能表是影片管理員功能表的另一個名稱，也就是整個光碟的主功能表;它通常會列出光碟上所有可用的影片標題集。根功能表是一個影片標題集的功能表，其中可包含一個標題或一組標題。 標題集中的所有標題都會共用相同的子圖片、音訊和角度功能表。

 

 



