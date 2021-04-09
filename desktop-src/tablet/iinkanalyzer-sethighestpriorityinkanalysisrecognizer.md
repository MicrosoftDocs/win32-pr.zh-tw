---
description: 將指定的 IInkAnalysisRecognizer 移至 IInkAnalyzer 物件的筆跡辨識器清單中的第一個位置。
ms.assetid: 9126187f-02dd-4988-91b8-c4f3d3b6f773
title: 'IInkAnalyzer：： SetHighestPriorityInkAnalysisRecognizer 方法 (IACom .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IInkAnalyzer.SetHighestPriorityInkAnalysisRecognizer
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 534b94e4f2964aa81f04e0adac6f45f346c530c4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103848073"
---
# <a name="iinkanalyzersethighestpriorityinkanalysisrecognizer-method"></a>IInkAnalyzer：： SetHighestPriorityInkAnalysisRecognizer 方法

將指定的 [**IInkAnalysisRecognizer**](iinkanalysisrecognizer.md) 移至 [**IInkAnalyzer**](iinkanalyzer.md) 物件的筆跡辨識器清單中的第一個位置。

## <a name="syntax"></a>語法


```C++
HRESULT SetHighestPriorityInkAnalysisRecognizer(
  [in] IInkAnalysisRecognizer *pInkAnalysisRecognizer
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*pInkAnalysisRecognizer* \[在\]
</dt> <dd>

要放在第一個位置的 [**IInkAnalysisRecognizer**](iinkanalysisrecognizer.md) 。

</dd> </dl>

## <a name="return-value"></a>傳回值

如需傳回值的描述，請參閱 [類別和介面-筆跡分析](classes-and-interfaces---ink-analysis.md)。

## <a name="remarks"></a>備註

若要依優先權順序取得筆跡辨識器的清單，請呼叫 [**IInkAnalyzer：： GetInkAnalysisRecognizersByPriority 方法**](iinkanalyzer-getinkanalysisrecognizersbypriority.md)。

這個方法不會影響 [**IInkAnalyzer**](iinkanalyzer.md)物件的筆墨辨識器清單中其餘 [**IInkAnalysisRecognizer**](iinkanalysisrecognizer.md)物件的順序。

[**IInkAnalyzer：： GetInkAnalysisRecognizersByPriority 方法**](iinkanalyzer-getinkanalysisrecognizersbypriority.md)所傳回的筆跡辨識器順序，表示 [**IInkAnalyzer**](iinkanalyzer.md)評估可用 [**IInkAnalysisRecognizer**](iinkanalysisrecognizer.md)物件的順序。

筆跡辨識器的使用會根據其在清單中的順序進行評估。

在筆跡分析期間， [**IInkAnalyzer**](iinkanalyzer.md) 會逐一查看其清單中的筆跡辨識器，直到找到支援筆觸語言和其他屬性的辨識器。 此辨識器會用於這些筆觸的筆跡辨識。

如果 [**IInkAnalyzer**](iinkanalyzer.md) 在分析期間找不到支援一組筆觸的 [**IInkAnalysisRecognizer**](iinkanalysisrecognizer.md) ，則 **IInkAnalyzer** 會產生 [**IAnalysisWarning**](ianalysiswarning.md) ，並顯示警告碼 **AnalysisWarningCode \_ InkAnalysisRecognizerNotInstalled** (請參閱 [**IAnalysisWarning：： GetWarningCode**](ianalysiswarning-getwarningcode.md)) 。

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

[**IInkAnalyzer：： GetInkAnalysisRecognizersByPriority 方法**](iinkanalyzer-getinkanalysisrecognizersbypriority.md)
</dt> <dt>

[**IInkAnalysisRecognizers**](iinkanalysisrecognizers.md)
</dt> <dt>

[**IAnalysisWarning**](ianalysiswarning.md)
</dt> <dt>

[筆跡分析參考](ink-analysis-reference.md)
</dt> </dl>

 

 




