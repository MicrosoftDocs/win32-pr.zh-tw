---
title: 按鈕. hoverImage
description: HoverImage 屬性會指定或抓取按鈕處於啟動狀態時所顯示的影像，並使用滑鼠指標將滑鼠停留在其上方。
ms.assetid: 6704e63d-1def-4e8e-808f-131c3cc1c0de
keywords:
- HoverImage Windows Media Player
topic_type:
- apiref
api_name:
- BUTTON.hoverImage
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8488fb599a958a96ef7b5aaa5afbf4c219110f0da5be7016a8190efe2004475d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120003718"
---
# <a name="buttonhoverimage"></a>按鈕. hoverImage

**HoverImage** 屬性會指定或抓取 **按鈕** 處於啟動狀態時所顯示的影像，並使用滑鼠指標將滑鼠停留在其上方。

``` syntax
        elementID.hoverImage
```

## <a name="possible-values"></a>可能的值

這個屬性是包含影像檔案名稱的讀取/寫入 **字串** 。

## <a name="remarks"></a>備註

支援的影像格式為 BMP、JPG、PNG 和 GIF。

預設影像是 **image** 屬性中指定的影像或其預設值。

如果暫留影像大於環境屬性中定義的區域，則會裁剪停留影像。

如果無法抓取影像，則會顯示 (紅 x 影像) 的預設影像。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|------------------------------------------------------|
| 版本<br/> | Windows Media Player 7.0 版或更新版本<br/> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**BUTTON 元素**](button-element.md)
</dt> <dt>

[**按鈕。影像**](button-image.md)
</dt> </dl>

 

 





