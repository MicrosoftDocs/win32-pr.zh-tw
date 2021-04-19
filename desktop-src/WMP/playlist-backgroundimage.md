---
title: 播放清單。 backgroundImage
description: BackgroundImage 屬性會指定或抓取背景影像。
ms.assetid: d4efa774-d42e-4415-a487-1e858d984075
keywords:
- 播放清單. backgroundImage Windows Media Player
topic_type:
- apiref
api_name:
- PLAYLIST.backgroundImage
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7eca04f47f6e157d5ede529c47fb6ae65b4333cf
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106995944"
---
# <a name="playlistbackgroundimage"></a>播放清單。 backgroundImage

**BackgroundImage** 屬性會指定或抓取背景影像。

``` syntax
        elementID.backgroundImage
```

## <a name="possible-values"></a>可能的值

這個屬性是包含影像檔案名稱的讀取/寫入 **字串** 。 它沒有預設值。

## <a name="remarks"></a>備註

如果影像的高度和寬度小於 **播放清單** 元素的高度和寬度，則會將影像並排顯示。 支援的格式為 BMP、JPG、GIF 和 PNG。

針對背景影像指定 "漸層" 的值，會導致播放清單的背景顯示為色彩漸層。 這表示背景色彩會在 [backgroundColor](playlist-backgroundcolor.md) (于背景) 和 [播放清單. statusColor](playlist-statuscolor.md) 值的上方逐漸轉換。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------------------------|
| 版本<br/> | Windows Media Player 7.0 版或更新版本，漸層功能的 Windows Media Player 10<br/> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**播放清單元素**](playlist-element.md)
</dt> </dl>

 

 





