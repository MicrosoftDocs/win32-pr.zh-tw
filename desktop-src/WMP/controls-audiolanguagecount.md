---
title: AudioLanguageCount
description: AudioLanguageCount 屬性會捕獲支援的音訊語言計數。
ms.assetid: a6dda8bf-db8c-4e97-9277-5a23dfa93156
keywords:
- AudioLanguageCount Windows Media Player
topic_type:
- apiref
api_name:
- Controls.audioLanguageCount
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 09193eb19580d9456f25ea336fe68b8d21e06bae
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106983110"
---
# <a name="controlsaudiolanguagecount"></a>AudioLanguageCount

**AudioLanguageCount** 屬性會捕獲支援的音訊語言計數。

``` syntax
player.controls.audioLanguageCount
      
```

## <a name="possible-values"></a>可能的值

這個屬性是唯讀的 **數位** (**long**) 。

## <a name="remarks"></a>備註

針對 Windows Media 內容，與語言選取相關的屬性和方法只支援單一輸出。

**Windows Media Player 10** 行動裝置版：此屬性一律會傳回1。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|------------------------------------------------------------------------------------|
| 版本<br/> | Windows Media Player  9  系列或更新的版本。<br/>                                 |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**Controls 物件**](controls-object.md)
</dt> <dt>

[**CurrentAudioLanguage**](controls-currentaudiolanguage.md)
</dt> <dt>

[**CurrentAudioLanguageIndex**](controls-currentaudiolanguageindex.md)
</dt> <dt>

[**GetAudioLanguageDescription**](controls-getaudiolanguagedescription.md)
</dt> <dt>

[**GetAudioLanguageID**](controls-getaudiolanguageid.md)
</dt> <dt>

[**GetLanguageName**](controls-getlanguagename.md)
</dt> </dl>

 

 





