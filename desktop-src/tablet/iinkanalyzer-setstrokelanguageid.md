---
description: 變更指定之筆劃的地區設定識別碼。
ms.assetid: 3714462d-0391-481f-968a-3c121b7dd538
title: 'IInkAnalyzer：： SetStrokeLanguageId 方法 (IACom .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IInkAnalyzer.SetStrokeLanguageId
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: e103683d85ff971a8f0daff2574e97672dd5a84b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104511644"
---
# <a name="iinkanalyzersetstrokelanguageid-method"></a>IInkAnalyzer：： SetStrokeLanguageId 方法

變更指定之筆劃的地區設定識別碼。

## <a name="syntax"></a>語法


```C++
HRESULT SetStrokeLanguageId(
  [in] LONG lStrokeId,
  [in] LONG lStrokeLCID
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*lStrokeId* \[在\]
</dt> <dd>

要指派地區設定識別碼之筆劃的識別碼。

</dd> <dt>

*lStrokeLCID* \[在\]
</dt> <dd>

要指派給筆劃的地區設定識別碼。

</dd> </dl>

## <a name="return-value"></a>傳回值

如需傳回值的描述，請參閱 [類別和介面-筆跡分析](classes-and-interfaces---ink-analysis.md)。

## <a name="remarks"></a>備註

當您藉由呼叫 [**IInkAnalyzer：： AddStroke 方法**](iinkanalyzer-addstroke.md)、 [**IInkAnalyzer：： AddStrokeForLanguage 方法**](iinkanalyzer-addstrokeforlanguage.md)、 [**IInkAnalyzer：： AddStrokes 方法**](iinkanalyzer-addstrokes.md)或 [**IInkAnalyzer：： AddStrokesForLanguage 方法**](iinkanalyzer-addstrokesforlanguage.md)來加入筆劃時，會設定筆觸的地區設定。 若要取得目前指派給筆劃的地區設定，請呼叫 [**IInkAnalyzer：： GetStrokeLanguageId 方法**](iinkanalyzer-getstrokelanguageid.md)。

指定的筆觸會移至未分類的筆墨節點 (請參閱 [**ICoNtextNode：： GetType**](icontextnode-gettype.md)) ，其中包含相同語言的筆觸。 如果沒有這類 [**ICoNtextNode**](icontextnode.md) ，此方法會建立新的非分類筆墨節點，並將筆劃移至該節點。 未分類的筆墨節點是具有 UnclassifiedInk 類型的 **ICoNtextNode** 。

如果這個方法從非未分類筆墨節點的 [**ICoNtextNode**](icontextnode.md) 移動筆劃，此方法也會將筆劃的周框方塊新增至 ink 分析器的中途區域 (請參閱 [**IInkAnalyzer：： GetDirtyRegion 方法**](iinkanalyzer-getdirtyregion.md)) 。

如果 *lStrokeLCID* 參數符合筆劃目前的語言識別項，則這個方法不會移動筆劃。

如果指定的筆劃沒有與 [**IInkAnalyzer**](iinkanalyzer.md)相關聯，這個方法會傳回而不更新 **IInkAnalyzer**。

如需語言識別項的詳細資訊，請參閱 [語言識別項常數和字串](/windows/desktop/Intl/language-identifier-constants-and-strings)。

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

[**IInkAnalyzer：： AddStroke 方法**](iinkanalyzer-addstroke.md)
</dt> <dt>

[**IInkAnalyzer：： AddStrokeForLanguage 方法**](iinkanalyzer-addstrokeforlanguage.md)
</dt> <dt>

[**IInkAnalyzer：： AddStrokes 方法**](iinkanalyzer-addstrokes.md)
</dt> <dt>

[**IInkAnalyzer：： AddStrokesForLanguage 方法**](iinkanalyzer-addstrokesforlanguage.md)
</dt> <dt>

[**IInkAnalyzer：： GetStrokeLanguageId 方法**](iinkanalyzer-getstrokelanguageid.md)
</dt> <dt>

[**IInkAnalyzer：： SetStrokesLanguageId 方法**](iinkanalyzer-setstrokeslanguageid.md)
</dt> <dt>

[筆跡分析參考](ink-analysis-reference.md)
</dt> </dl>

 

