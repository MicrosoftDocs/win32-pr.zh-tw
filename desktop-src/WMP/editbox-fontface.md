---
title: 編輯方塊. fontFace
description: FontFace 屬性會指定或抓取編輯方塊控制項中文字的字型。
ms.assetid: 5fb5e6d2-8535-402e-9ca1-d43e334e94e3
keywords:
- 編輯方塊. fontFace Windows Media Player
topic_type:
- apiref
api_name:
- EDITBOX.fontFace
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 49c5794da93821db840a48facbba45540da9249a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106984390"
---
# <a name="editboxfontface"></a>編輯方塊. fontFace

**FontFace** 屬性會指定或抓取編輯方塊控制項中文字的字型。

``` syntax
        elementID.fontFace
```

## <a name="possible-values"></a>可能的值

此屬性是讀取/寫入 **字串**。

## <a name="remarks"></a>備註

這個屬性可以是 Windows 中可用之任何有效字型的名稱。 Windows Media Player 將不支援安裝字型，因此請選擇您知道將會在預期系統上的字型。

如果使用者的系統無法使用指定的 **fontFace** ，編輯方塊控制項就會預設為 Windows 系統字型。 英文系統的預設值是「Tahoma」。 針對國際系統，預設會從資源檔載入。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|---------------------------------------------------------|
| 版本<br/> | 適用于 Windows XP 或更新版本的 Windows Media Player<br/> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**編輯方塊元素**](editbox-element.md)
</dt> <dt>

[**編輯方塊. fontSize**](editbox-fontsize.md)
</dt> <dt>

[**編輯方塊. fontStyle**](editbox-fontstyle.md)
</dt> </dl>

 

 





