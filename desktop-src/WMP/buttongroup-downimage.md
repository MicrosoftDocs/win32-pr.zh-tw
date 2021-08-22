---
title: BUTTONGROUP. downImage
description: DownImage 屬性會指定或抓取代表 BUTTONGROUP 關閉狀態之影像的名稱。
ms.assetid: 022e77e7-d3c0-41b5-984a-84d016a5a25a
keywords:
- BUTTONGROUP. downImage Windows Media Player
topic_type:
- apiref
api_name:
- BUTTONGROUP.downImage
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 233c56951ec88444ab58de901732517a4ced4c249f8a9b75f3461eb38e86c975
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118997748"
---
# <a name="buttongroupdownimage"></a>BUTTONGROUP. downImage

**DownImage** 屬性會指定或抓取代表 **BUTTONGROUP** 關閉狀態之影像的名稱。

``` syntax
        elementID.downImage
```

## <a name="possible-values"></a>可能的值

此屬性是讀取/寫入 **字串**。

## <a name="remarks"></a>備註

支援的影像格式為 BMP、JPG、PNG 和 GIF。 如果影像是8位的 BMP 檔案，則可以使用 **hueShift** 和 **飽和度** 屬性動態變更其色調和飽和度值。

預設影像是在 **image** 屬性中指定的影像。

如果向下影像大於定義的區域，則會裁剪下圖。

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

[**BUTTONGROUP 影像**](buttongroup-image.md)
</dt> <dt>

[**BUTTONGROUP 飽和度**](buttongroup-saturation.md)
</dt> </dl>

 

 





