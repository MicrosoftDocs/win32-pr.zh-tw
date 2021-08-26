---
description: 當 MSWebDVD 物件處於全螢幕模式時，ShowCursor 方法會讓資料指標可見。
ms.assetid: 3a611cc8-7979-473d-bd0f-f4ca43701c63
title: ShowCursor 方法
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3013392a5dcea2b3c4c9af8ee94d54c540814b5f4221563429ee7c837dcdddd2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120050518"
---
# <a name="showcursor-method"></a>ShowCursor 方法

> [!Note]  
> 此元件可在 Microsoft Windows 2000、Windows XP 和 Windows Server 2003 作業系統中使用。 它在後續版本中可能會變更或無法使用。

 

`ShowCursor`當 **MSWebDVD** 物件處於全螢幕模式時，方法會讓資料指標可見。

``` syntax
MSWebDVD.ShowCursor(bShow)
```

## <a name="parameters"></a>參數

<dl> <dt>

<span id="bShow"></span><span id="bshow"></span><span id="BSHOW"></span>*bShow*
</dt> <dd>

指定是否將資料指標顯示為布林值。



| 值 | 描述            |
|-------|------------------------|
| true  | 顯示游標        |
| false | 不要顯示資料指標 |



 

</dd> </dl>

## <a name="return-value"></a>傳回值

沒有傳回值。

## <a name="remarks"></a>備註

當 DVD 顯示進入全螢幕模式時，游標會在3到5秒內消失。 如果您的應用程式的控制項按鈕是在全螢幕模式中顯示，請使用這個方法來再次顯示資料指標。

 

 



