---
title: AmbientAttributes.clippingImage
description: ClippingImage 屬性會指定或抓取要裁剪控制項的區域。
ms.assetid: e4b51d31-f9c7-4398-983d-95867a2cab45
keywords:
- AmbientAttributes. clippingImage Windows Media Player
topic_type:
- apiref
api_name:
- AmbientAttributes.clippingImage
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7e05e05ca9c7c3efdf842ffd4297da6f9fee035d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "107000918"
---
# <a name="ambientattributesclippingimage"></a>AmbientAttributes.clippingImage

**ClippingImage** 屬性會指定或抓取要裁剪控制項的區域。

``` syntax
        elementID.clippingImage
```

## <a name="possible-values"></a>可能的值

這個屬性是讀取/寫入 **字串** ，表示影像檔案名稱。 它沒有預設值。

## <a name="remarks"></a>備註

**ClippingImage** 屬性支援 PNG、JPG、BMP 和 GIF 檔案 (不包括動畫 gif) 。 由於 Jpg 是有損耗的，因此可能會發生非預期的色彩變更，因此不建議將影像裁剪。

當您只想要顯示控制項影像的一部分，而不是整個矩形區域時，這個屬性就很有用。 **ClippingColor** 屬性指出裁剪影像的區域，其對應至控制項的透明、不可按的部分。 因此，控制項可以是任何圖形。 為了獲得最佳結果，裁剪影像的大小應該與控制項影像相同。

**播放清單**、 **VIEW** 和子 **視圖** 元素不支援 **clippingImage** 屬性。 如果 *影片*，裁剪影像將無法搭配 **video** 元素使用。[**無視窗**] 會設定為 false，而效果元素 *則會* 設定為 [**效果**]。**視窗** 設定為 true。

因為裁剪影像的使用會影響效能，所以不應在效率為問題時使用。

## <a name="examples"></a>範例

如需說明如何使用此屬性的範例，請參閱 [BUTTONELEMENT mappingColor](buttonelement-mappingcolor.md) 屬性。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|------------------------------------------------------|
| 版本<br/> | Windows Media Player 7.0 版或更新版本<br/> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**環境屬性**](ambient-attributes.md)
</dt> <dt>

[**AmbientAttributes.clippingColor**](ambientattributes-clippingcolor.md)
</dt> </dl>

 

 





