---
title: WM/Writer 屬性
description: WM/Writer 屬性是寫入內容文字之寫入器的名稱。
ms.assetid: e2035cf7-29f4-4642-9388-4cd7cb08149e
keywords:
- WM/寫入器屬性 Windows Media Player
topic_type:
- apiref
api_name:
- WM/Writer
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a239fd83c936a0712459307fbf08b01c4bfcc4f6fd4c6d32cddc12d8092f2b2c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118332053"
---
# <a name="wmwriter-attribute"></a>WM/Writer 屬性

**WM/Writer** 屬性是寫入內容文字之寫入器的名稱。

## <a name="applies-to"></a>套用至

-   [音訊專案](audio-item-attributes.md)
-   [常用 Windows 媒體檔案屬性](commonly-used-windows-media-file-attributes.md)
-   [影片專案](video-item-attributes.md)

## <a name="remarks"></a>備註

這個屬性會儲存在文件庫和數位媒體檔案中。

這個屬性可以有多個值。 若要取得多重值屬性的所有值，您必須使用 **getItemInfoByType** 方法，而不是 **getItemInfo** 方法。

**寫入器** 是這個屬性的別名。

這個屬性的 Windows 媒體格式 SDK 常數是 g \_ wszWMWriter。

若要判斷是否可以變更這個屬性的值，請使用 [isReadOnlyItem](media-isreadonlyitem.md) 方法。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|---------------------------------------------------|
| 版本<br/> | Windows Media Player 9 系列或更新版本<br/> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**屬性參考**](attribute-reference.md)
</dt> <dt>

[**GetItemInfoByType**](media-getiteminfobytype.md)
</dt> </dl>

 

 





