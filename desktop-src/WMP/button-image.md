---
title: 按鈕。影像
description: Image 屬性會指定或抓取按鈕的預設影像。
ms.assetid: d0d97f14-2c4d-4769-b45c-c6cde7282bea
keywords:
- 按鈕。影像 Windows Media Player
topic_type:
- apiref
api_name:
- BUTTON.image
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 85874c79db8f3174b70af68c3ff1e58511c3f00cc7d648389dbca971c7efd96e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118342906"
---
# <a name="buttonimage"></a>按鈕。影像

**Image** 屬性會指定或抓取 **按鈕** 的預設影像。

``` syntax
        elementID.image
```

## <a name="possible-values"></a>可能的值

這個屬性是包含影像檔案名稱的讀取/寫入 **字串** 。

## <a name="remarks"></a>備註

支援的影像格式為 BMP、JPG、PNG 和 GIF (包括動畫 Gif) 。

如果 **按鈕** 影像大於 [ **寬度** ] 和 [ **高度** ] 屬性所定義的區域，則會裁剪影像。

如果未指定影像，但 **高度** 和 **寬度** 為，則會顯示直接在此控制項後方的影像。 這有助於在 **視圖** 本身繪製影像，減少所需的個別影像檔案數目。

如果無法抓取影像，則會顯示 (紅 x 影像) 的預設影像。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|------------------------------------------------------|
| 版本<br/> | Windows Media Player 7.0 版或更新版本<br/> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**BUTTON 元素**](button-element.md)
</dt> </dl>

 

 





