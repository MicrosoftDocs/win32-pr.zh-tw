---
title: CUSTOMSLIDER 影像
description: Image 屬性會指定或抓取檔案的名稱，其中包含對應至自訂滑杆之各種狀態的影像。
ms.assetid: 7db4f924-76af-4451-831c-1ed8ab1315ee
keywords:
- CUSTOMSLIDER Windows Media Player 映射
topic_type:
- apiref
api_name:
- CUSTOMSLIDER.image
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f3b169bbdcac0e251a161c8e09f352caf460280b23e0198167a641721caa6c64
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117936244"
---
# <a name="customsliderimage"></a>CUSTOMSLIDER 影像

**Image** 屬性會指定或抓取檔案的名稱，其中包含對應至自訂滑杆之各種狀態的影像。

``` syntax
        elementID.image
```

## <a name="possible-values"></a>可能的值

這個屬性是包含影像檔案名稱的讀取/寫入 **字串** 。

## <a name="remarks"></a>備註

需要 **image** 屬性。 它會指定包含一或多個子影像（以水準或垂直方式排列）的影像檔案，表示自訂滑杆的各種狀態。 每個子影像都必須有與 **positionImage** 相同的維度，否則自訂滑杆將無法正常運作。 因此，整體影像的高度或寬度必須是 **positionImage** 高度或寬度的偶數倍數。

支援的影像檔案類型為 BMP、JPG、PNG 和 GIF (不包括動畫 Gif) 。

## <a name="examples"></a>範例

以下是自訂滑杆影像的範例。 對應的 **positionImage** 會顯示在 [ **positionImage** ] 屬性的 [範例] 區段中。

![範例 customslider 影像](images/dial.png)

**PositionImage** 屬性也包含程式碼範例，說明如何使用 **CUSTOMSLIDER** 元素的屬性。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|------------------------------------------------------|
| 版本<br/> | Windows Media Player 7.0 版或更新版本<br/> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**CUSTOMSLIDER 元素**](customslider-element.md)
</dt> <dt>

[**CUSTOMSLIDER.positionImage**](customslider-positionimage.md)
</dt> </dl>

 

 





