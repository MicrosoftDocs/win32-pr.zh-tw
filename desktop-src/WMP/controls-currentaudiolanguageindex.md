---
title: CurrentAudioLanguageIndex
description: CurrentAudioLanguageIndex 屬性會指定或抓取對應于播放音訊語言的單一索引。
ms.assetid: 9a1ae887-4e64-4758-a8a2-bf2e10a7a5c7
keywords:
- CurrentAudioLanguageIndex Windows Media Player
topic_type:
- apiref
api_name:
- Controls.currentAudioLanguageIndex
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cf1eb87873170c486782368f431f4fa8e3597b20
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106976151"
---
# <a name="controlscurrentaudiolanguageindex"></a>CurrentAudioLanguageIndex

**CurrentAudioLanguageIndex** 屬性會指定或抓取對應于播放音訊語言的單一索引。

``` syntax
player.controls.currentAudioLanguageIndex
      
```

## <a name="possible-values"></a>可能的值

這個屬性是 (**長**) 的讀取/寫入 **號碼**。

## <a name="remarks"></a>備註

針對 Windows Media 內容，與語言選取相關的屬性和方法只支援單一輸出。

使用 **audioLanguageCount** 屬性來取得支援的音訊語言數目。

**Windows Media Player 10** 行動裝置版：這個屬性只接受或傳回0。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|------------------------------------------------------------------------------------|
| 版本<br/> | Windows Media Player  9  系列或更新的版本。<br/>                                 |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**Controls 物件**](controls-object.md)
</dt> <dt>

[**AudioLanguageCount**](controls-audiolanguagecount.md)
</dt> <dt>

[**CurrentAudioLanguage**](controls-currentaudiolanguage.md)
</dt> <dt>

[**GetAudioLanguageDescription**](controls-getaudiolanguagedescription.md)
</dt> <dt>

[**GetAudioLanguageID**](controls-getaudiolanguageid.md)
</dt> <dt>

[**GetLanguageName**](controls-getlanguagename.md)
</dt> </dl>

 

 





