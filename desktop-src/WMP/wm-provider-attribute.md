---
title: WM/提供者屬性
description: WM/提供者屬性是屬性值提供者的名稱。
ms.assetid: 358651d3-5bcd-4a03-a9aa-a33745d0323a
keywords:
- WM/提供者屬性 Windows Media Player
topic_type:
- apiref
api_name:
- WM/Provider
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1d7c2c1c796edf28a567f72708c60c7976f718bb
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106977484"
---
# <a name="wmprovider-attribute"></a>WM/提供者屬性

**WM/提供者** 屬性是屬性值提供者的名稱。

## <a name="applies-to"></a>套用至

-   [音訊專案](audio-item-attributes.md)
-   [CD 播放清單](cd-playlist-attributes.md)
-   [CD 曲目](cd-track-attributes.md)
-   [常用的 Windows Media 檔案屬性](commonly-used-windows-media-file-attributes.md)
-   [單選項目](radio-item-attributes.md)
-   [影片專案](video-item-attributes.md)

## <a name="remarks"></a>備註

這個屬性會儲存在程式庫 (或快取) 和數位媒體檔案中。

**MetadataSource** 是此屬性的別名。

這個屬性的 Windows Media Format SDK 常數是 g \_ wszWMProvider。

若要判斷是否可以變更這個屬性的值，請使用 [isReadOnlyItem](media-isreadonlyitem.md) 方法。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------------------------------------------|
| 版本<br/> | Windows Media Player 9 系列或更新版本 (只有 Windows Media Player 10 或更新版本才支援相片專案) <br/> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**屬性參考**](attribute-reference.md)
</dt> </dl>

 

 





