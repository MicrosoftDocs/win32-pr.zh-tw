---
title: 按鈕. hoverDownImage
description: HoverDownImage 屬性會指定或抓取按鈕處於關閉狀態時所顯示的影像，並使用滑鼠指標將滑鼠停留在其上方。
ms.assetid: 06645307-50f1-400d-aa73-c48d0fba3ee1
keywords:
- HoverDownImage Windows Media Player
topic_type:
- apiref
api_name:
- BUTTON.hoverDownImage
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bcdb23f9806e36cebd2f5da6a46a8307c268861d73f68361e07f56e9ce09dcc5
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119902398"
---
# <a name="buttonhoverdownimage"></a>按鈕. hoverDownImage

**HoverDownImage** 屬性會指定或抓取 **按鈕** 處於關閉狀態時所顯示的影像，並使用滑鼠指標將滑鼠停留在其上方。

``` syntax
        elementID.hoverDownImage
```

## <a name="possible-values"></a>可能的值

這個屬性是包含影像檔案名稱的讀取/寫入 **字串** 。

## <a name="remarks"></a>備註

支援的影像格式為 BMP、JPG、PNG 和 GIF。

預設影像是 **downImage** 屬性中指定的影像，或其預設值。

如果暫止的影像大於環境屬性中定義的區域，則會裁剪暫止的影像。

如果無法抓取影像，則會顯示 (紅 x 影像) 的預設影像。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|------------------------------------------------------|
| 版本<br/> | Windows Media Player 7.0 版或更新版本<br/> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**BUTTON 元素**](button-element.md)
</dt> <dt>

[**按鈕. downImage**](button-downimage.md)
</dt> </dl>

 

 





