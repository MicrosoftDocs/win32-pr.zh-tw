---
title: AmbientAttributes.nineGridMargins
description: NineGridMargins 屬性會指定面板元素之非統一縮放的邊界寬度。
ms.assetid: b8a7efd0-6c12-4436-9d53-0dcfa1600aa5
keywords:
- AmbientAttributes. nineGridMargins Windows Media Player
topic_type:
- apiref
api_name:
- AmbientAttributes.nineGridMargins
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3cf77c1fcfdb64fb9e4b0dde8753572255c17eda
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106999327"
---
# <a name="ambientattributesninegridmargins"></a>AmbientAttributes.nineGridMargins

**NineGridMargins** 屬性會指定面板元素之非統一縮放的邊界寬度。

``` syntax
        elementID.nineGridMargins
```

## <a name="possible-values"></a>可能的值

這個屬性是包含邊界寬度的讀取/寫入 **字串** ，格式為 "*widthLeft*，*widthTop*，*widthRight*，*widthBottom*"。 每個寬度值都是一個數位，代表九個方格的邊界寬度（以圖元為單位）。

## <a name="remarks"></a>備註

*九個方格* 是一種技術，用來將使用者介面元素分割成以 3 x 3 矩陣排列的九個矩形區域。 當專案調整大小時，九個方格區域可以依不同的因數進行調整。

您指定的四個寬度值都代表三個相鄰區域中資料列或資料行的寬度。 每個資料列或資料行會形成九個方格的左邊、右上角或底部。

[AmbientAttributes](ambientattributes-resizeimages.md) 必須設定為 true，此屬性才能運作。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|------------------------------------|
| 版本<br/> | Windows Media Player 11<br/> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**環境屬性**](ambient-attributes.md)
</dt> </dl>

 

 





