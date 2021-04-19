---
title: GetAudioLanguageDescription 方法
description: GetAudioLanguageDescription 方法會抓取對應于指定之以一為基礎之索引的音訊語言描述。
ms.assetid: 995a2568-f15f-4b92-9782-92ba5273f444
keywords:
- getAudioLanguageDescription 方法 Windows Media Player
- getAudioLanguageDescription 方法 Windows Media Player、Controls 類別
- Controls 類別 Windows Media Player，getAudioLanguageDescription 方法
topic_type:
- apiref
api_name:
- Controls.getAudioLanguageDescription
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1d28e82648a1047252402694f4948d2a2734f344
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106984002"
---
# <a name="controlsgetaudiolanguagedescription-method"></a>GetAudioLanguageDescription 方法

**GetAudioLanguageDescription** 方法會抓取對應于指定之以一為基礎之索引的音訊語言描述。

## <a name="syntax"></a>語法


```JScript
strRetVal = Controls.getAudioLanguageDescription(
  index
)
```



## <a name="parameters"></a>參數

<dl> <dt>

*索引* \[在\]
</dt> <dd>

指定以一為基礎之音訊語言索引的 (**long**) **數目**。

</dd> </dl>

## <a name="return-value"></a>傳回值

這個方法會傳回 **字串** 值。

## <a name="remarks"></a>備註

針對 Windows Media 內容，與語言選取相關的屬性和方法只支援單一輸出。

使用 **audioLanguageCount** 屬性來取得支援的音訊語言數目，然後使用以一為基礎的索引個別存取音訊語言。

**Windows Media Player 10** 行動裝置版：不支援這個方法。

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

[**CurrentAudioLanguageIndex**](controls-currentaudiolanguageindex.md)
</dt> <dt>

[**GetAudioLanguageID**](controls-getaudiolanguageid.md)
</dt> <dt>

[**GetLanguageName**](controls-getlanguagename.md)
</dt> </dl>

 

 





