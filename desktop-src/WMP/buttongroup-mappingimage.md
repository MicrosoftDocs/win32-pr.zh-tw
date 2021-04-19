---
title: BUTTONGROUP. mappingImage
description: MappingImage 屬性會指定或抓取代表 BUTTONGROUP 之按鈕對應的影像名稱。
ms.assetid: bfea52d1-0e7f-4f77-a212-d34e356a4d85
keywords:
- BUTTONGROUP. mappingImage Windows Media Player
topic_type:
- apiref
api_name:
- BUTTONGROUP.mappingImage
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 26e4afc44a00d5ce9b15ee01d4a0dc1aff52c555
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106990702"
---
# <a name="buttongroupmappingimage"></a>BUTTONGROUP. mappingImage

**MappingImage** 屬性會指定或抓取代表 **BUTTONGROUP** 之按鈕對應的影像名稱。

``` syntax
        elementID.mappingImage
```

## <a name="possible-values"></a>可能的值

此屬性是讀取/寫入 **字串**。

## <a name="remarks"></a>備註

這是必須指定的必要屬性。

對應影像的大小應該與主要 **影像** 相同。 它是主影像可點擊區域的對應。 以不同的色彩填滿每個可點按的區域，以建立地圖。

定義每個 **BUTTONELEMENT** 時，請使用 **mappingColor** 屬性來指定其在地圖中的色彩。 例如，如果主要影像中有一個停止符號形狀的按鈕圖形，您可以使用標示為紅色的區域來建立地圖。 然後，必須將 **BUTTONELEMENT** 屬性指定為紅色，才能讓「停止簽署」映射可供按一下。

支援的影像格式為 BMP、JPG、PNG 和 GIF (不包括動畫 Gif) 。 由於 Jpg 是失真的，因此可能會發生非預期的色彩變更，因此不建議用於對應影像。

## <a name="examples"></a>範例

下圖是 **mappingImage** 和它所對應之可見影像的範例。 這些映射屬於 SDK 隨附之小型資料夾中的面板。

![範例對應影像](images/absam01m.png)![範例背景影像](images/absam01f.png)

請參閱 *BUTTONELEMENT*。說明如何使用此屬性之程式碼範例的 [mappingColor](buttonelement-mappingcolor.md) 屬性。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|------------------------------------------------------|
| 版本<br/> | Windows Media Player 7.0 版或更新版本<br/> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**BUTTONELEMENT.mappingColor**](buttonelement-mappingcolor.md)
</dt> <dt>

[**BUTTONGROUP 元素**](buttongroup-element.md)
</dt> <dt>

[**BUTTONGROUP 影像**](buttongroup-image.md)
</dt> <dt>

[**BUTTONGROUP. transparencyColor**](buttongroup-transparencycolor.md)
</dt> </dl>

 

 





