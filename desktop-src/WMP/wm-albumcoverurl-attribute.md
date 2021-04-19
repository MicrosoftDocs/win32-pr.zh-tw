---
title: WM/AlbumCoverURL 屬性
description: WM/AlbumCoverURL 屬性是適用于專輯封面或縮圖影像 (URL) 的統一資源定位器。
ms.assetid: 0134867a-7c11-4d50-9ab5-b48c1ca6c473
keywords:
- WM/AlbumCoverURL 屬性 Windows Media Player
topic_type:
- apiref
api_name:
- WM/AlbumCoverURL Attribute
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6939c5451f3ae8f41214a817293e3c7f3cb3b66c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106978672"
---
# <a name="wmalbumcoverurl-attribute"></a>WM/AlbumCoverURL 屬性

**WM/AlbumCoverURL** 屬性是適用于專輯封面或縮圖影像 (URL) 的統一資源定位器。

## <a name="applies-to"></a>套用至

-   [**音訊專案**](audio-item-attributes.md)
-   [**相片專案**](photo-item-attributes.md)
-   [**影片專案**](video-item-attributes.md)

## <a name="remarks"></a>備註

若是音訊專案，這個屬性就是專輯封面的 URL。 如果是相片或影片專案，這個屬性就是縮圖影像的 URL。

目前使用者的本機文件庫中的媒體專案無法使用這個屬性。 它僅適用于屬於遠端媒體櫃的媒體專案;也就是，由家用網路上的另一位使用者所提供的程式庫。 若要判斷媒體櫃是否為遠端，請呼叫 [**IWMPLibrary：： get \_ 類型**](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmplibrary-get_type)。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|----------------------------------------------|
| 版本<br/> | Windows Media Player 12 或更新版本。<br/> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**屬性參考**](attribute-reference.md)
</dt> </dl>

 

 





