---
description: 抓取 IInkAnalysisRecognizer 物件的已排序集合。
ms.assetid: 67399237-38e2-4905-a97c-10ca72c7799b
title: 'IInkAnalyzer：： GetInkAnalysisRecognizersByPriority 方法 (IACom .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IInkAnalyzer.GetInkAnalysisRecognizersByPriority
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: d596a8138f8ab16852ce99116eef66372ff2b074
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103848075"
---
# <a name="iinkanalyzergetinkanalysisrecognizersbypriority-method"></a>IInkAnalyzer：： GetInkAnalysisRecognizersByPriority 方法

抓取 [**IInkAnalysisRecognizer**](iinkanalysisrecognizer.md) 物件的已排序集合。

## <a name="syntax"></a>語法


```C++
HRESULT GetInkAnalysisRecognizersByPriority(
  [out] IInkAnalysisRecognizers **ppInkAnalysisRecognizers
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*ppInkAnalysisRecognizers* \[擴展\]
</dt> <dd>

[**IInkAnalysisRecognizer**](iinkanalysisrecognizer.md)物件的已排序集合。

</dd> </dl>

## <a name="return-value"></a>傳回值

如需傳回值的描述，請參閱 [類別和介面-筆跡分析](classes-and-interfaces---ink-analysis.md)。

## <a name="remarks"></a>備註

> [!Caution]  
> 若要避免記憶體流失，請在 *ppInkAnalysisRecognizers* 上呼叫 [**IUnknown：： Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) （當您不再需要使用物件時）。

 

此集合中的辨識器順序表示 [**IInkAnalyzer**](iinkanalyzer.md) 評估可用辨識器的順序。 **IInkAnalyzer** 會使用筆觸的語言作為套用 [**IInkAnalysisRecognizer**](iinkanalysisrecognizer.md)的主要準則。 作為次要準則， **IInkAnalyzer** 會比較分析提示資訊與 **IInkAnalysisRecognizer** 物件的支援功能 (請參閱 [**IInkAnalysisRecognizer：： GetCapabilities**](iinkanalysisrecognizer-getcapabilities.md)) 。 如需有關分析提示的詳細資訊，請參閱 [**IInkAnalyzer：： CreateAnalysisHint 方法**](iinkanalyzer-createanalysishint.md)。

如果有一個以上的 [**IInkAnalysisRecognizer**](iinkanalysisrecognizer.md) 支援語言識別項，則 [**IInkAnalyzer**](iinkanalyzer.md) 會使用「第一個」演算法來選取第一個 **IInkAnalysisRecognizer** 來分析該語言的筆觸。

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

[**IInkAnalysisRecognizers**](iinkanalysisrecognizers.md)
</dt> <dt>

[**IInkAnalyzer：： SetHighestPriorityInkAnalysisRecognizer 方法**](iinkanalyzer-sethighestpriorityinkanalysisrecognizer.md)
</dt> <dt>

[筆跡分析參考](ink-analysis-reference.md)
</dt> </dl>

 

