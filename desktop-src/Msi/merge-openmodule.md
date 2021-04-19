---
description: Merge 物件的 OpenModule 方法會以唯讀模式開啟 Windows Installer 合併模組。 必須先開啟模組，才能與安裝資料庫合併。
ms.assetid: fc976899-2c39-4314-b2fb-417e0dfc53b9
title: 'OpenModule 方法 (Mergemod .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Merge.OpenModule
- IMsmMerge.OpenModule
api_type:
- COM
api_location:
- Mergemod.dll
ms.openlocfilehash: 9d83a9331c91817f70c49ecf74c7171c5e627be6
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106991362"
---
# <a name="mergeopenmodule-method"></a>Merge. OpenModule 方法

[**Merge**](merge-object.md)物件的 **OpenModule** 方法會以唯讀模式開啟 Windows Installer 合併模組。 必須先開啟模組，才能與安裝資料庫合併。

## <a name="syntax"></a>語法


```JScript
Merge.OpenModule(
  FileName,
  Language
)
```



## <a name="parameters"></a>參數

<dl> <dt>

*FileName* 
</dt> <dd>

指向合併模組的完整檔案名。

</dd> <dt>

*Language* 
</dt> <dd>

 (LANGID) 的有效語言識別項。

</dd> </dl>

## <a name="return-value"></a>傳回值

這個方法不會傳回值。

## <a name="remarks"></a>備註

此函式會在唯讀模式中開啟合併模組，並且在呼叫 [**CloseModule**](merge-closemodule.md) 方法之前，不會將其他程式寫入至合併模組。

安裝程式會嘗試以 *語言* 指定的語言或更通用的語言來開啟模組。 例如，如果 *Language* 指定為1033，則可以使用預設語言來開啟具有1033、9或0之預設語言的模組。 *語言* 值9會開啟預設語言為9或0的模組。 如果模組的預設語言不符合指定的需求，則會嘗試將模組轉換成所要求的語言。 如果發生這種情況，則會將模組轉換成逐漸普及的語言，而不是語言中立的。 如果沒有任何轉換成功，則模組無法開啟。 在此情況下，會將錯誤加入至 msmErrorLanguageUnsupported 類型的錯誤清單。 如果將模組轉換成所需的語言時發生錯誤，則會將錯誤加入至 msmErrorLanguageFailed 類型的錯誤清單。 如需詳細資訊，請參閱 [**Error**](error-object.md)物件的 [**Type**](error-type.md)屬性。 開啟合併模組會清除尚未抓取的任何錯誤。

### <a name="c"></a>C++

請參閱 [**OpenModule**](/windows/win32/api/mergemod/nf-mergemod-imsmmerge-openmodule) 函式。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|-----------------------------------------------------------------------------------------|
| 版本<br/> | Mergemod.dll 1.0 或更新版本<br/>                                                    |
| 標頭<br/>  | <dl> <dt>Mergemod。h</dt> </dl>   |
| DLL<br/>     | <dl> <dt>Mergemod.dll</dt> </dl> |



 

 
