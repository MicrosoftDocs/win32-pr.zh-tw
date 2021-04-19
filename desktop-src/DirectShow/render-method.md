---
description: Render 方法會初始化 DVD 篩選圖形。
ms.assetid: 910f1e3f-b3bb-498b-93da-3a974a3117e8
title: Render 方法
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 677abab1c669642c1e51e0041c98949d923147c7
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "106991593"
---
# <a name="render-method"></a>Render 方法

> [!Note]  
> 此元件可用於 Microsoft Windows 2000、Windows XP 及 Windows Server 2003 作業系統。 它在後續版本中可能會變更或無法使用。

 

`Render`方法會初始化 DVD 篩選圖形。

``` syntax
MSWebDVD.Render(iRender = 0)
```

## <a name="parameters"></a>參數

<dl> <dt>

<span id="iRender"></span><span id="irender"></span><span id="IRENDER"></span>*iRender*
</dt> <dd>

指定整數值，指出是否將終結和重建篩選圖形。



| 值 | 描述                                                                                         |
|-------|-----------------------------------------------------------------------------------------------------|
| 0     | 如果篩選圖形已經存在，將不會終結並重建。 這是預設值。 |
| 1     | 篩選圖形將會損毀並重建（如果已經存在的話）。                                |



 

</dd> </dl>

## <a name="return-value"></a>傳回值

沒有傳回值。

## <a name="remarks"></a>備註

`Render`方法可讓 **MSWebDVD** 物件在啟動時完全初始化基礎 DirectShow 篩選圖形。 這可避免使用者發出第一個命令來播放光碟或顯示功能表時，所發生的輕微延遲。 在 `Render` 呼叫任何其他方法之前，不需要呼叫任何情況。 例如，如果應用程式在初始化篩選圖形之前呼叫 [**PlayTitle**](playtitle-method.md) ， **MSWebDVD** 物件 `Render` 就會自動呼叫，然後再嘗試播放光碟。

 

 



