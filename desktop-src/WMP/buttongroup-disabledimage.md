---
title: BUTTONGROUP. disabledImage
description: DisabledImage 屬性會指定或抓取影像的名稱，此影像代表 BUTTONGROUP 中按鈕的停用狀態。
ms.assetid: 34d4e6a9-de73-4dfa-9c23-4f17b55298f6
keywords:
- BUTTONGROUP. disabledImage Windows Media Player
topic_type:
- apiref
api_name:
- BUTTONGROUP.disabledImage
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9659c4d726313c0fb202a840e12891f00ad3fcf0
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106975964"
---
# <a name="buttongroupdisabledimage"></a>BUTTONGROUP. disabledImage

**DisabledImage** 屬性會指定或抓取影像的名稱，此影像代表 **BUTTONGROUP** 中按鈕的停用狀態。

``` syntax
        elementID.disabledImage
```

## <a name="possible-values"></a>可能的值

此屬性是讀取/寫入 **字串**。

## <a name="remarks"></a>備註

支援的影像格式為 BMP、JPG、PNG 和 GIF。 如果影像是8位的 BMP 檔案，則可以使用 **hueShift** 和 **飽和度** 屬性動態變更其色調和飽和度值。

當 **BUTTONELEMENT** 專案的 **disabled** 屬性設定為 true 時，會顯示 **BUTTONGROUP** 之 **disabledImage** 的對應區域。 如果停用的映射大於定義的區域，則會裁剪停用的映射。

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

 

 





