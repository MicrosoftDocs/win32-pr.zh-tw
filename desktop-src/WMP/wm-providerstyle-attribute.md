---
title: WM/ProviderStyle 屬性
description: WM/ProviderStyle 屬性是屬性值提供者所指派之專案的樣式。
ms.assetid: 43994d6b-0d71-4f2c-834a-47bbcd32b461
keywords:
- WM/ProviderStyle 屬性 Windows Media Player
topic_type:
- apiref
api_name:
- WM/ProviderStyle
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a18af02254e7ce476ffc9c1e427465966cd66c84
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106979445"
---
# <a name="wmproviderstyle-attribute"></a>WM/ProviderStyle 屬性

**WM/ProviderStyle** 屬性是屬性值提供者所指派之專案的樣式。

## <a name="applies-to"></a>套用至

-   [音訊專案](audio-item-attributes.md)
-   [CD 播放清單](cd-playlist-attributes.md)
-   [CD 曲目](cd-track-attributes.md)
-   [常用的 Windows Media 檔案屬性](commonly-used-windows-media-file-attributes.md)
-   [影片專案](video-item-attributes.md)

## <a name="remarks"></a>備註

這個屬性會儲存在程式庫 (或快取) 和數位媒體檔案中。

**Style** 是這個屬性的別名。

這個屬性的 Windows Media Format SDK 常數是 g \_ wszWMProviderStyle。

若要判斷是否可以變更這個屬性的值，請使用 [isReadOnlyItem](media-isreadonlyitem.md) 方法。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|---------------------------------------------------|
| 版本<br/> | Windows Media Player 9 系列或更新版本<br/> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**屬性參考**](attribute-reference.md)
</dt> </dl>

 

 





