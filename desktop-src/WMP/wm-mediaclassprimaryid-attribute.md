---
title: WM/MediaClassPrimaryID 屬性
description: WM/MediaClassPrimaryID 屬性是 GUID，用來指定其中一種主要媒體類別音樂、非音樂音訊、影片或其他。
ms.assetid: eb78f4a9-7c18-4cad-bb34-fd1ff15bad4f
keywords:
- WM/MediaClassPrimaryID 屬性 Windows Media Player
topic_type:
- apiref
api_name:
- WM/MediaClassPrimaryID
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7aebc52488ebcabfca843a8fdfdfbb51307cd96be4fe923386c718bab8752c61
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119506458"
---
# <a name="wmmediaclassprimaryid-attribute"></a>WM/MediaClassPrimaryID 屬性

**WM/MediaClassPrimaryID** 屬性是指定其中一個主要媒體類別的 GUID：音樂、非音樂音訊、影片或其他。

## <a name="applies-to"></a>套用至

-   [音訊專案](audio-item-attributes.md)
-   [常用 Windows 媒體檔案屬性](commonly-used-windows-media-file-attributes.md)
-   [其他專案](other-item-attributes.md)
-   [相片專案](photo-item-attributes.md)
-   [播放清單](playlist-attributes-ref.md)
-   [單選項目](radio-item-attributes.md)
-   [影片專案](video-item-attributes.md)

## <a name="remarks"></a>備註

這個屬性會儲存在文件庫和數位媒體檔案中。

**MediaClassPrimaryID** 是此屬性的別名。

這個屬性的 Windows 媒體格式 SDK 常數是 g \_ wszWMMediaClassPrimaryID。

若要判斷是否可以變更這個屬性的值，請使用 [isReadOnlyItem](media-isreadonlyitem.md) 方法。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------------------------------------------|
| 版本<br/> | Windows Media Player 9 系列或更新版本 (只有 Windows Media Player 10 或更新版本才支援相片專案) <br/> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**屬性參考**](attribute-reference.md)
</dt> </dl>

 

 





