---
title: 按鈕. downImage
description: DownImage 屬性會指定或抓取代表按鈕關閉狀態的影像。
ms.assetid: 18149668-5be6-4b64-8adf-8904585ff0be
keywords:
- DownImage Windows Media Player
topic_type:
- apiref
api_name:
- BUTTON.downImage
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bff24c568ae607b5b67d766f28eb7c221844f1434a959952628cc2ad5a5d6d5d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120123738"
---
# <a name="buttondownimage"></a>按鈕. downImage

**DownImage** 屬性會指定或抓取代表 **按鈕** 關閉狀態的影像。

``` syntax
        elementID.downImage
```

## <a name="possible-values"></a>可能的值

這個屬性是包含影像檔案名稱的讀取/寫入 **字串** 。

## <a name="remarks"></a>備註

支援的影像格式為 BMP、JPG、PNG 和 GIF。

預設影像是 **image** 屬性中指定的影像或其預設值。

如果下圖大於環境屬性中定義的區域，則會裁剪下圖。

如果無法抓取影像，則會顯示 (紅 x 影像) 的預設影像。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|------------------------------------------------------|
| 版本<br/> | Windows Media Player 7.0 版或更新版本<br/> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**BUTTON 元素**](button-element.md)
</dt> <dt>

[**按鈕。向下鍵**](button-down.md)
</dt> <dt>

[**按鈕。影像**](button-image.md)
</dt> </dl>

 

 





