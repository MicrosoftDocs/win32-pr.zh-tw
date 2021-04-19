---
title: 滑杆. disabledImage
description: DisabledImage 屬性會指定或抓取滑杆控制項停用時使用的滑杆影像。
ms.assetid: b6c4237d-8eb0-44ce-a23f-9bdc5c21aca8
keywords:
- DisabledImage Windows Media Player
topic_type:
- apiref
api_name:
- SLIDER.disabledImage
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cf1b90dcbd551ca0f8bb332f858eac0b69c46733
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106987048"
---
# <a name="sliderdisabledimage"></a>滑杆. disabledImage

**DisabledImage** 屬性會指定或抓取滑杆控制項停用時使用的滑杆影像。

``` syntax
        elementID.disabledImage
```

## <a name="possible-values"></a>可能的值

這個屬性是包含影像檔案名稱的讀取/寫入 **字串** 。

## <a name="remarks"></a>備註

**DisabledImage** 是選擇性的。 如果未提供，則會將 **backgroundImage** 用於所有停用的狀態。 當滑杆控制項停用時，就不會顯示任何前景影像。

支援的格式為 BMP、JPG、PNG 和 GIF (不包括動畫 Gif) 。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|------------------------------------------------------|
| 版本<br/> | Windows Media Player 7.0 版或更新版本<br/> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**滑杆元素**](slider-element.md)
</dt> <dt>

[**滑杆. backgroundImage**](slider-backgroundimage.md)
</dt> </dl>

 

 





