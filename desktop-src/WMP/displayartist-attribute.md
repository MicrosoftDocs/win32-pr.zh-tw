---
title: DisplayArtist 屬性
description: DisplayArtist 屬性是針對專案顯示之演出者的名稱。
ms.assetid: 8cf5a4e6-ce96-4fd4-b01a-6cd4264a5c09
keywords:
- DisplayArtist 屬性 Windows Media Player
topic_type:
- apiref
api_name:
- DisplayArtist
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c6c20e3d693aa7d5be5be0236d9eefebe7efcb70bc236db3f84389e5a3ceeccf
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118997318"
---
# <a name="displayartist-attribute"></a>DisplayArtist 屬性

**DisplayArtist** 屬性是針對專案顯示之演出者的名稱。

## <a name="applies-to"></a>套用至

-   [音訊專案](audio-item-attributes.md)

## <a name="remarks"></a>備註

一般來說，當設定屬性時， **DisplayArtist** 會具有與 **WM/AlbumArtist** 屬性相同的值。 否則，此值會是與專輯上第一個曲目相關聯之演出者的名稱。

若要判斷是否可以變更這個屬性的值，請使用 [isReadOnlyItem](media-isreadonlyitem.md) 方法。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|------------------------------------|
| 版本<br/> | Windows Media Player 11<br/> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**屬性參考**](attribute-reference.md)
</dt> <dt>

[**WM/AlbumArtist 屬性**](wm-albumartist-attribute.md)
</dt> </dl>

 

 





