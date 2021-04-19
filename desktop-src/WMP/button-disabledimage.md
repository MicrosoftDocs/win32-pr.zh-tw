---
title: 按鈕. disabledImage
description: DisabledImage 屬性會指定或抓取在停用按鈕時所顯示的影像。
ms.assetid: b5654323-589a-45da-9534-6fa67c3a4c4b
keywords:
- DisabledImage Windows Media Player
topic_type:
- apiref
api_name:
- BUTTON.disabledImage
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8eac407f6e7fbdd155f4bcabe98cecc0546f7d97
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106985960"
---
# <a name="buttondisabledimage"></a>按鈕. disabledImage

**DisabledImage** 屬性會指定或抓取在停用 **按鈕** 時所顯示的影像。

``` syntax
        elementID.disabledImage
```

## <a name="possible-values"></a>可能的值

這個屬性是包含影像檔案名稱的讀取/寫入 **字串** 。

## <a name="remarks"></a>備註

支援的影像格式為 BMP、JPG、PNG 和 GIF。

只要控制項的 [ **已停用** ] 屬性設定為 [true]，就會顯示此影像。 如果停用的映射大於定義的區域，則會裁剪停用的映射。

如果無法抓取影像，則會顯示 (紅 x 影像) 的預設影像。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|------------------------------------------------------|
| 版本<br/> | Windows Media Player 7.0 版或更新版本<br/> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**BUTTON 元素**](button-element.md)
</dt> </dl>

 

 





