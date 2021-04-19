---
title: LISTBOX. fontFace
description: FontFace 屬性會指定或抓取清單方塊控制項的字型。
ms.assetid: 15e3180a-6e1e-4654-a0bb-164d66a86a26
keywords:
- LISTBOX. fontFace Windows Media Player
topic_type:
- apiref
api_name:
- LISTBOX.fontFace
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 82c03c367001b307dd8bd5059ec7e3f4a0b364e6
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106990203"
---
# <a name="listboxfontface"></a>LISTBOX. fontFace

**FontFace** 屬性會指定或抓取清單方塊控制項的字型。

``` syntax
        elementID.fontFace
```

## <a name="possible-values"></a>可能的值

此屬性是讀取/寫入 **字串**。

## <a name="remarks"></a>備註

這個屬性可以是 Windows 中可用之任何有效字型的名稱。 Windows Media Player 將不支援安裝字型，因此請選擇您知道將會在預期系統上的字型。

如果指定的 **fontFace** 無法在使用者的系統上使用，則清單方塊控制項預設為 Windows 系統字型。 英文系統的預設值是「Tahoma」。 針對國際系統，預設會從資源檔載入。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|---------------------------------------------------------|
| 版本<br/> | 適用于 Windows XP 或更新版本的 Windows Media Player<br/> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**LISTBOX 元素**](listbox-element.md)
</dt> <dt>

[**LISTBOX. fontSize**](listbox-fontsize.md)
</dt> <dt>

[**LISTBOX. fontStyle**](listbox-fontstyle.md)
</dt> </dl>

 

 





