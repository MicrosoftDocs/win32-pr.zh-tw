---
title: BUTTONGROUP. hoverDownImage
description: HoverDownImage 屬性會指定或抓取影像的名稱，代表 BUTTONGROUP 中按鈕的暫止狀態。 當按鈕處於關閉狀態，且使用者將滑鼠停留在該按鈕上方時，就會出現暫止狀態。
ms.assetid: dc048303-21d1-40ba-99bb-8d1c2f46628b
keywords:
- BUTTONGROUP. hoverDownImage Windows Media Player
topic_type:
- apiref
api_name:
- BUTTONGROUP.hoverDownImage
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c84d907a9b3fd1fc1a2eaf2dcf30337d016ae0732b147f435f49343d791b65c6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118119877"
---
# <a name="buttongrouphoverdownimage"></a>BUTTONGROUP. hoverDownImage

**HoverDownImage** 屬性會指定或抓取影像的名稱，代表 **BUTTONGROUP** 中按鈕的暫止狀態。 當按鈕處於關閉狀態，且使用者將滑鼠停留在該按鈕上方時，就會出現暫止狀態。

``` syntax
        elementID.hoverDownImage
```

## <a name="possible-values"></a>可能的值

此屬性是讀取/寫入 **字串**。

## <a name="remarks"></a>備註

支援的影像格式為 BMP、JPG、PNG 和 GIF。 如果影像是8位的 BMP 檔案，則可以使用 **hueShift** 和 **飽和度** 屬性動態變更其色調和飽和度值。

預設影像是 **downImage** 屬性中指定的影像，或其預設值。

如果暫留的影像大於所定義的區域，則會裁剪停留影像。

如果無法抓取影像，則會顯示 (紅 x 影像) 的預設影像。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|------------------------------------------------------|
| 版本<br/> | Windows Media Player 7.0 版或更新版本<br/> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**BUTTONGROUP 元素**](buttongroup-element.md)
</dt> <dt>

[**BUTTONGROUP. downImage**](buttongroup-downimage.md)
</dt> <dt>

[**BUTTONGROUP. hueShift**](buttongroup-hueshift.md)
</dt> <dt>

[**BUTTONGROUP 飽和度**](buttongroup-saturation.md)
</dt> </dl>

 

 





