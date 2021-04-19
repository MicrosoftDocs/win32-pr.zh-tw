---
title: GetLanguageName 方法
description: GetLanguageName 方法會使用指定的地區設定識別碼 (LCID) 來抓取音訊語言的名稱。
ms.assetid: 9e142c89-92bf-476f-bae7-b94f5b5ebe01
keywords:
- getLanguageName 方法 Windows Media Player
- getLanguageName 方法 Windows Media Player、Controls 類別
- Controls 類別 Windows Media Player，getLanguageName 方法
topic_type:
- apiref
api_name:
- Controls.getLanguageName
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 798a6b22f344953df716e4df4ed8a9a0daff2a7b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106983151"
---
# <a name="controlsgetlanguagename-method"></a>GetLanguageName 方法

**GetLanguageName** 方法會使用指定的地區設定識別碼 (LCID) 來抓取音訊語言的名稱。

## <a name="syntax"></a>語法


```JScript
strRetVal = Controls.getLanguageName(
  LCID
)
```



## <a name="parameters"></a>參數

<dl> <dt>

 \[ 中的 LCID\]
</dt> <dd>

指定 LCID (**long**) 的 **數目**。

</dd> </dl>

## <a name="return-value"></a>傳回值

這個方法會傳回 **字串**。

## <a name="remarks"></a>備註

LCID 可唯一識別特定語言方言，稱為地區設定。

針對 Windows Media 內容，與語言選取相關的屬性和方法只支援單一輸出。

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

[**GetAudioLanguageID**](controls-getaudiolanguageid.md)
</dt> </dl>

 

 





