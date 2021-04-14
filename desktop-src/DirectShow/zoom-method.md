---
description: Zoom 方法會放大或縮小影片，並以一組指定的螢幕座標為中心。
ms.assetid: 050f1264-8fbe-4322-970c-184275d5b219
title: Zoom 方法
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2625e6c4facf006a0d904e49068853720e20c29e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104469405"
---
# <a name="zoom-method"></a>Zoom 方法

> [!Note]  
> 此元件可用於 Microsoft Windows 2000、Windows XP 及 Windows Server 2003 作業系統。 它在後續版本中可能會變更或無法使用。

 

`Zoom`方法會放大或縮小影片，並以一組指定的螢幕座標為中心。

``` syntax
MSWebDVD.Zoom(iXPos, iYPos, iZoomRatio)
```

## <a name="parameters"></a>參數

<dl> <dt>

<span id="iXPos"></span><span id="ixpos"></span><span id="IXPOS"></span>*iXPos*
</dt> <dd>

將矩形縮放區域中央的 x 座標指定為整數。

</dd> <dt>

<span id="iYPos"></span><span id="iypos"></span><span id="IYPOS"></span>*iYPos*
</dt> <dd>

指定矩形中央的 y 座標，以縮放為整數。

</dd> <dt>

<span id="iZoomRatio"></span><span id="izoomratio"></span><span id="IZOOMRATIO"></span>*iZoomRatio*
</dt> <dd>

指定以整數形式套用至目前縮放值的放大因數。 總最大值取決於硬體重迭可支援的內容;這通常是原始大小32到64倍的因素。

</dd> </dl>

## <a name="return-value"></a>傳回值

沒有傳回值。

## <a name="remarks"></a>備註

新的縮放比例會一直有效，直到它還原為原始大小或再次變更為止。 換言之，兩個呼叫這個方法來指定兩個的 *iZoomRatio* ，會導致比原始影片大四倍的縮放比例。 如果使用者嘗試放大超過硬體可支援的範圍，此方法將會成功，但不會執行任何動作。

[**SetClipVideoRect**](setclipvideorect-method.md)方法是另一種放大的方式;這兩種方法之間的唯一差異在於指定縮放矩形的方式。

 

 



