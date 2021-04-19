---
title: WM/ContentDistributor 屬性
description: WM/ContentDistributor 屬性是專案的散發者名稱。
ms.assetid: 45f548a4-4059-464c-af93-1ba09e6b8d1e
keywords:
- WM/ContentDistributor 屬性 Windows Media Player
topic_type:
- apiref
api_name:
- WM/ContentDistributor
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 420e3e05a68f89d8e37b8ef95dd1247802442700
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106995270"
---
# <a name="wmcontentdistributor-attribute"></a>WM/ContentDistributor 屬性

**WM/ContentDistributor** 屬性是專案的散發者名稱。

## <a name="applies-to"></a>套用至

-   [音訊專案](audio-item-attributes.md)
-   [常用的 Windows Media 檔案屬性](commonly-used-windows-media-file-attributes.md)
-   [播放清單](playlist-attributes-ref.md)
-   [影片專案](video-item-attributes.md)

## <a name="remarks"></a>備註

這個屬性會儲存在文件庫和數位媒體檔案中。

**ContentDistributor** 是此屬性的別名。

這個屬性的 Windows Media Format SDK 常數是 g \_ wszWMContentDistributor。

若要判斷是否可以變更這個屬性的值，請使用 [isReadOnlyItem](media-isreadonlyitem.md) 方法。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|---------------------------------------------------|
| 版本<br/> | Windows Media Player 9 系列或更新版本<br/> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**屬性參考**](attribute-reference.md)
</dt> </dl>

 

 





