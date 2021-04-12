---
description: CanStep 方法會判斷本機系統上的 MPEG-2 解碼器是否可以依照指定的方向執行框架逐步執行。
ms.assetid: 21721722-0bf4-4cc7-a0e4-96b353888948
title: CanStep 方法
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 506e7436e5ec79947aceeca69891e52074cf2ea7
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "104025645"
---
# <a name="canstep-method"></a>CanStep 方法

> [!Note]  
> 此元件可用於 Microsoft Windows 2000、Windows XP 及 Windows Server 2003 作業系統。 它在後續版本中可能會變更或無法使用。

 

`CanStep`方法會判斷本機系統上的 mpeg-2 解碼器是否可以依照指定的方向執行框架逐步執行。

``` syntax
[ bCanStep = ] MSWebDVD.CanStep(bDirection)
```

## <a name="parameters"></a>參數

<dl> <dt>

<span id="bDirection"></span><span id="bdirection"></span><span id="BDIRECTION"></span>*bDirection*
</dt> <dd>

用來作為旗標的布林值，用來指定解碼器的框架逐步執行功能方向、向前或向後。



| 值 | 描述                                          |
|-------|------------------------------------------------------|
| true  | 是否可以回溯執行解碼器？                           |
| false | 是否可以向前跳到解碼器？ 這是預設值。 |



 

</dd> </dl>

## <a name="return-value"></a>傳回值

如果解碼器可以逐步執行指定的方向，則會傳回布林值 true，否則傳回 false。

## <a name="remarks"></a>備註

並非所有硬體 MPEG-2 解碼器都支援 DirectShow®8.0 中新的框架逐步執行功能。 這個方法會查詢其框架逐步執行功能的解碼器。 如果此解碼器可以執行畫面格逐步執行，則應用程式可以使用 [**步驟**](step-method.md) 方法來逐步執行畫面格。 如果正在使用軟體解碼器，這個方法一律會傳回 **true** 。

 

 



