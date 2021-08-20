---
title: WM/ProviderRating 屬性
description: WM/ProviderRating 屬性是屬性值提供者所指派之專案的評等。
ms.assetid: a1a76560-a8d9-486a-badc-56d7bf488c10
keywords:
- WM/ProviderRating 屬性 Windows Media Player
topic_type:
- apiref
api_name:
- WM/ProviderRating
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ddcff262f21b4f31daff6f704dba1cb096f54bb295a21a3ae9a7c90f574af34f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118116602"
---
# <a name="wmproviderrating-attribute"></a>WM/ProviderRating 屬性

**WM/ProviderRating** 屬性是屬性值提供者所指派之專案的評等。

## <a name="applies-to"></a>套用至

-   [音訊專案](audio-item-attributes.md)
-   [CD 播放清單](cd-playlist-attributes.md)
-   [CD 曲目](cd-track-attributes.md)
-   [常用 Windows 媒體檔案屬性](commonly-used-windows-media-file-attributes.md)
-   [DVD](dvd-attributes.md)
-   [影片專案](video-item-attributes.md)

## <a name="remarks"></a>備註

這個屬性會儲存在程式庫 (或快取) 和數位媒體檔案中。

**評** 等是此屬性的別名。

這個屬性的 Windows 媒體格式 SDK 常數是 g \_ wszWMProviderRating。

若要判斷是否可以變更這個屬性的值，請使用 [isReadOnlyItem](media-isreadonlyitem.md) 方法。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|---------------------------------------------------|
| 版本<br/> | Windows Media Player 9 系列或更新版本<br/> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**屬性參考**](attribute-reference.md)
</dt> </dl>

 

 





