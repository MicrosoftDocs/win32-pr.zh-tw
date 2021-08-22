---
title: ContentDistributorDuration 屬性
description: ContentDistributorDuration 屬性是專案的播放持續時間（以秒為單位）。
ms.assetid: c64cb4ca-b0bc-4beb-b2ae-ddd0c5fcd35c
keywords:
- ContentDistributorDuration 屬性 Windows Media Player
topic_type:
- apiref
api_name:
- ContentDistributorDuration
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: eefee789358f2d913d976432a485cf7726e3f7d6afa14e845ad9d7699d8ed4a6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119135751"
---
# <a name="contentdistributorduration-attribute"></a>ContentDistributorDuration 屬性

**ContentDistributorDuration** 屬性是專案的播放持續時間（以秒為單位）。

## <a name="applies-to"></a>套用至

-   [音訊專案](audio-item-attributes.md)
-   [其他專案](other-item-attributes.md)

## <a name="remarks"></a>備註

如果 [一般 **持續時間** ] 屬性未設定 (Null) 或0，則會改為傳回這個屬性的值。

若要判斷是否可以變更這個屬性的值，請使用 [isReadOnlyItem](media-isreadonlyitem.md) 方法。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|------------------------------------|
| 版本<br/> | Windows Media Player 11<br/> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**屬性參考**](attribute-reference.md)
</dt> <dt>

[**Duration 屬性**](duration-attribute.md)
</dt> </dl>

 

 





