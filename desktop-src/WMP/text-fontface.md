---
title: FontFace
description: FontFace 屬性會指定或抓取文字控制項的字樣。
ms.assetid: 3b39e245-139a-4361-b678-0f9e962996b7
keywords:
- FontFace Windows Media Player
topic_type:
- apiref
api_name:
- TEXT.fontFace
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 183b25547e456cb90cac4d2137354679e13d8a96
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106994349"
---
# <a name="textfontface"></a>FontFace

**FontFace** 屬性會指定或抓取文字控制項的字樣。

``` syntax
        elementID.fontFace
```

## <a name="possible-values"></a>可能的值

此屬性是讀取/寫入 **字串**。

## <a name="remarks"></a>備註

這個屬性可以是 Windows 上任何可用的有效字型的名稱。 Windows Media Player 將不支援安裝字型，因此請選擇您知道將會在預期系統上的字型。

如果使用者的系統無法使用指定的 **fontFace** ，文字控制項會預設為 Windows 系統字型。

如需說明如何使用 **TEXT** 元素屬性的範例，請參閱 [value](text-value.md)屬性。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|------------------------------------------------------|
| 版本<br/> | Windows Media Player 7.0 版或更新版本<br/> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**TEXT 元素**](text-element.md)
</dt> <dt>

[**FontSize**](text-fontsize.md)
</dt> </dl>

 

 





