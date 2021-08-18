---
title: GetAudioLanguageID 方法
description: GetAudioLanguageID 方法會針對指定的音訊語言索引，抓取 (LCID) 的地區設定識別碼。
ms.assetid: 8134a7ce-bdc7-46b2-b10e-2bf1215b0de1
keywords:
- getAudioLanguageID 方法 Windows Media Player
- getAudioLanguageID 方法 Windows Media Player、Controls 類別
- Controls 類別 Windows Media Player，getAudioLanguageID 方法
topic_type:
- apiref
api_name:
- Controls.getAudioLanguageID
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2352162d810ca75aeeee6db1c3d59c297b85414be46a365909c4ed56af179f8b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118119337"
---
# <a name="controlsgetaudiolanguageid-method"></a>GetAudioLanguageID 方法

**GetAudioLanguageID** 方法會針對指定的音訊語言索引，抓取 (LCID) 的地區設定識別碼。

## <a name="syntax"></a>語法


```JScript
retVal = Controls.getAudioLanguageID(
  index
)
```



## <a name="parameters"></a>參數

<dl> <dt>

*索引* \[在\]
</dt> <dd>

指定音訊語言索引的 **數位** (**long**) 。

</dd> </dl>

## <a name="return-value"></a>傳回值

這個方法會傳回 **數位** (**long**) 。

## <a name="remarks"></a>備註

LCID 可唯一識別特定語言方言，稱為地區設定。

針對 Windows 媒體型內容，與語言選取相關的屬性和方法只支援單一輸出。

**Windows Media Player 10** 行動裝置版：此屬性一律會傳回語言中立的 LCID (0) 。

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

[**GetAudioLanguageDescription**](controls-getaudiolanguagedescription.md)
</dt> <dt>

[**GetLanguageName**](controls-getlanguagename.md)
</dt> </dl>

 

 





