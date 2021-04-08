---
description: 傳回指定之筆劃的地區設定識別碼。
ms.assetid: a5fb9b7a-ed3e-4552-9412-39529203bd81
title: 'IInkAnalyzer：： GetStrokeLanguageId 方法 (IACom .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IInkAnalyzer.GetStrokeLanguageId
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: a231dde453467ad2973d729fa068cedcc35151c7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103690579"
---
# <a name="iinkanalyzergetstrokelanguageid-method"></a>IInkAnalyzer：： GetStrokeLanguageId 方法

傳回指定之筆劃的地區設定識別碼。

## <a name="syntax"></a>語法


```C++
HRESULT GetStrokeLanguageId(
  [in]  LONG lStrokeId,
  [out] LONG *lStrokeLCID
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*lStrokeId* \[在\]
</dt> <dd>

筆觸識別碼。

</dd> <dt>

*lStrokeLCID* \[擴展\]
</dt> <dd>

指定之筆劃的地區設定識別碼。

</dd> </dl>

## <a name="return-value"></a>傳回值

如需傳回值的描述，請參閱 [類別和介面-筆跡分析](classes-and-interfaces---ink-analysis.md)。

## <a name="remarks"></a>備註

當您藉由呼叫 [**IInkAnalyzer：： AddStroke 方法**](iinkanalyzer-addstroke.md)、 [**IInkAnalyzer：： AddStrokeForLanguage 方法**](iinkanalyzer-addstrokeforlanguage.md)、 [**IInkAnalyzer：： AddStrokes 方法**](iinkanalyzer-addstrokes.md)或 [**IInkAnalyzer：： AddStrokesForLanguage 方法**](iinkanalyzer-addstrokesforlanguage.md)來加入筆劃時，會設定筆觸的地區設定。 若要變更筆觸的地區設定，請使用 [**IInkAnalyzer：： SetStrokeLanguageId 方法**](iinkanalyzer-setstrokelanguageid.md) 或 [**IInkAnalyzer：： SetStrokesLanguageId 方法**](iinkanalyzer-setstrokeslanguageid.md)。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | 僅限 Windows XP Tablet PC Edition \[ 桌面應用程式\]<br/>                                                 |
| 最低支援的伺服器<br/> | 都不支援<br/>                                                                                     |
| 標頭<br/>                   | <dl> <dt>IACom (也需要 IACom \_ c) </dt> </dl> |
| DLL<br/>                      | <dl> <dt>IACom.dll</dt> </dl>                          |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**IInkAnalyzer**](iinkanalyzer.md)
</dt> <dt>

[**IInkAnalyzer：： SetStrokeLanguageId 方法**](iinkanalyzer-setstrokelanguageid.md)
</dt> <dt>

[**IInkAnalyzer：： SetStrokesLanguageId 方法**](iinkanalyzer-setstrokeslanguageid.md)
</dt> <dt>

[筆跡分析參考](ink-analysis-reference.md)
</dt> </dl>

 

 




