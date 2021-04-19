---
title: 播放清單。飽和度
description: 飽和度屬性會指定或抓取下拉式影像的飽和度值。
ms.assetid: 4c5dd3d9-828a-45c9-896a-9a702d354544
keywords:
- 播放清單。飽和度 Windows Media Player
topic_type:
- apiref
api_name:
- PLAYLIST.saturation
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 82eb53afeafb0754f0e754f68fd5ff785eaade8a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106982573"
---
# <a name="playlistsaturation"></a>播放清單。飽和度

**飽和度** 屬性會指定或抓取下拉式影像的飽和度值。

``` syntax
        elementID.saturation
```

## <a name="possible-values"></a>可能的值

這個屬性是一個讀/寫 **編號** (**float**) ，其值範圍從0.0 到2.0，預設值為1.0。

## <a name="remarks"></a>備註

這個屬性會變更 **dropDownBackgroundImage** 和 **dropDownImage** 屬性所指定之影像的飽和度值（如果已指定），而且它們參考的是8位的 BMP 影像。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|---------------------------------------------------|
| 版本<br/> | Windows Media Player 9 系列或更新版本<br/> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**播放清單元素**](playlist-element.md)
</dt> <dt>

[**播放清單。 dropDownBackgroundImage**](playlist-dropdownbackgroundimage.md)
</dt> <dt>

[**播放清單。 dropDownImage**](playlist-dropdownimage.md)
</dt> <dt>

[**播放清單。 hueShift**](playlist-hueshift.md)
</dt> </dl>

 

 





