---
title: BUTTONGROUP 影像
description: Image 屬性會指定或抓取代表 BUTTONGROUP 按鈕的影像名稱。
ms.assetid: dad50a1e-d147-4e0f-b5d6-8cbfeef32438
keywords:
- BUTTONGROUP Windows Media Player 映射
topic_type:
- apiref
api_name:
- BUTTONGROUP.image
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1fa395edc149671ad05a38a5ff7c77053b6e3d82
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106999485"
---
# <a name="buttongroupimage"></a>BUTTONGROUP 影像

**Image** 屬性會指定或抓取代表 **BUTTONGROUP** 按鈕的影像名稱。

``` syntax
        elementID.image
```

## <a name="possible-values"></a>可能的值

此屬性是讀取/寫入 **字串**。

## <a name="remarks"></a>備註

支援的影像格式為 BMP、JPG、PNG 和 GIF。 如果影像是8位的 BMP 檔案，則可以使用 **hueShift** 和 **飽和度** 屬性動態變更其色調和飽和度值。

如果控制項的影像大於定義的區域，則會裁剪影像。

如果無法抓取影像，則會顯示 (紅 x 影像) 的預設影像。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|------------------------------------------------------|
| 版本<br/> | Windows Media Player 7.0 版或更新版本<br/> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**BUTTONGROUP 元素**](buttongroup-element.md)
</dt> <dt>

[**BUTTONGROUP. hueShift**](buttongroup-hueshift.md)
</dt> <dt>

[**BUTTONGROUP 飽和度**](buttongroup-saturation.md)
</dt> </dl>

 

 





