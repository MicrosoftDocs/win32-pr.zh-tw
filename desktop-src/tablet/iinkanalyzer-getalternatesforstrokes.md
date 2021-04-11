---
description: 使用指定的筆觸識別碼抓取筆劃的分析替代項。
ms.assetid: e8bc198e-de0b-49b7-9120-4298985dfe64
title: 'IInkAnalyzer：： GetAlternatesForStrokes 方法 (IACom .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IInkAnalyzer.GetAlternatesForStrokes
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 115b2cc1be4ba35614ada6fddd9c9fbcdfa76357
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104113341"
---
# <a name="iinkanalyzergetalternatesforstrokes-method"></a>IInkAnalyzer：： GetAlternatesForStrokes 方法

使用指定的筆觸識別碼抓取筆劃的分析替代項。

## <a name="syntax"></a>語法


```C++
HRESULT GetAlternatesForStrokes(
  [in]  ULONG              ulStrokeIdsCount,
  [in]  LONG               *plStrokes,
  [in]  ULONG              ulMaximumAlternates,
  [out] AnalysisAlternates **ppAlternates
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*ulStrokeIdsCount* \[在\]
</dt> <dd>

*PlStrokes* 中的筆觸識別碼數目。

</dd> <dt>

*plStrokes* \[在\]
</dt> <dd>

筆觸識別碼的陣列。

</dd> <dt>

*ulMaximumAlternates* \[在\]
</dt> <dd>

傳回的最大分析替代專案數目。

</dd> <dt>

*ppAlternates* \[擴展\]
</dt> <dd>

包含分析替代專案的 [**IAnalysisAlternates**](ianalysisalternates.md) 物件。

</dd> </dl>

## <a name="return-value"></a>傳回值

如需傳回值的描述，請參閱 [類別和介面-筆跡分析](classes-and-interfaces---ink-analysis.md)。

## <a name="remarks"></a>備註

> [!Caution]  
> 若要避免記憶體流失，請在 ppAlternates 上呼叫 [**IUnknown：： Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) （ \* 當您不再需要使用物件時）。

 

Top [**IAnalysisAlternate**](ianalysisalternate.md) 會傳回為集合的第一個替代。

指定的筆觸不需要代表檔的相鄰區域。

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

[**IAnalysisAlternate**](ianalysisalternate.md)
</dt> <dt>

[**IAnalysisAlternates**](ianalysisalternates.md)
</dt> <dt>

[**IInkAnalyzer：： GetAlternates 方法**](iinkanalyzer-getalternates.md)
</dt> <dt>

[**IInkAnalyzer：： GetAlternatesForCoNtextNodes 方法**](iinkanalyzer-getalternatesforcontextnodes.md)
</dt> <dt>

[**IInkAnalyzer：： ModifyTopAlternate 方法**](iinkanalyzer-modifytopalternate.md)
</dt> <dt>

[**IInkAnalyzer：： ModifyTopAlternateWithConfirmation 方法**](iinkanalyzer-modifytopalternatewithconfirmation.md)
</dt> <dt>

[筆跡分析參考](ink-analysis-reference.md)
</dt> </dl>

 

