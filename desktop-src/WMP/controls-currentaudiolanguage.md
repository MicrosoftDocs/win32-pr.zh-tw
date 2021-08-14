---
title: CurrentAudioLanguage
description: CurrentAudioLanguage 屬性會指定或抓取用來播放之音訊語言 (LCID) 的地區設定識別碼。
ms.assetid: 628845df-add3-4068-9c3d-b4a9b818808c
keywords:
- CurrentAudioLanguage Windows Media Player
topic_type:
- apiref
api_name:
- Controls.currentAudioLanguage
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 63c5eb53c9f408a9d50a7f738434e5dcd30fc804970b3e1ea95c985c90d62063
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117750610"
---
# <a name="controlscurrentaudiolanguage"></a>CurrentAudioLanguage

**CurrentAudioLanguage** 屬性會指定或抓取用來播放之音訊語言 (LCID) 的地區設定識別碼。

``` syntax
player.controls.currentAudioLanguage
      
```

## <a name="possible-values"></a>可能的值

這個屬性是 (**長**) 的讀取/寫入 **號碼**。

## <a name="remarks"></a>備註

LCID 可唯一識別特定語言方言，稱為地區設定。

針對 Windows 媒體型內容，與語言選取相關的屬性和方法只支援單一輸出。

使用 DVD 內容時，指定 LCID 將會導致第一個可用的音訊播放軌選取指定的語言識別項。

**Windows Media Player 10** 行動裝置版：這個屬性只會接受或傳回語言中立的 LCID (0) 。

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

[**CurrentAudioLanguageIndex**](controls-currentaudiolanguageindex.md)
</dt> <dt>

[**GetAudioLanguageDescription**](controls-getaudiolanguagedescription.md)
</dt> <dt>

[**GetAudioLanguageID**](controls-getaudiolanguageid.md)
</dt> <dt>

[**GetLanguageName**](controls-getlanguagename.md)
</dt> </dl>

 

 





