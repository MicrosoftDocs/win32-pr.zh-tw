---
title: WM/Language 屬性
description: WM/Language 屬性是專案的語言。
ms.assetid: aebfb518-61ca-4b75-875a-ce2127a74b67
keywords:
- WM/Language 屬性 Windows Media Player
topic_type:
- apiref
api_name:
- WM/Language
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 172cc8498bf5360e29822a484bcc2ddacd70b8b7
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "107000390"
---
# <a name="wmlanguage-attribute"></a>WM/Language 屬性

**WM/language** 屬性是專案的語言。

## <a name="applies-to"></a>套用至

-   [音訊專案](audio-item-attributes.md)
-   [常用的 Windows Media 檔案屬性](commonly-used-windows-media-file-attributes.md)
-   [單選項目](radio-item-attributes.md)
-   [影片專案](video-item-attributes.md)

## <a name="remarks"></a>備註

這個屬性會儲存在文件庫和數位媒體檔案中。

這個屬性可以有多個值。 若要取得多重值屬性的所有值，您必須使用 **getItemInfoByType** 方法，而不是 **getItemInfo** 方法。

**Language** 是這個屬性的別名。

這個屬性的 Windows Media Format SDK 常數是 g \_ wszWMLanguage。

若要判斷是否可以變更這個屬性的值，請使用 [isReadOnlyItem](media-isreadonlyitem.md) 方法。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|-----------------------------------------------------------------------------------------------------------------------|
| 版本<br/> | Windows Media Player 9 系列或更新版本 (單選項目只在 Windows Media Player 9 系列中支援) <br/> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**屬性參考**](attribute-reference.md)
</dt> <dt>

[**GetItemInfoByType**](media-getiteminfobytype.md)
</dt> </dl>

 

 





