---
description: 取得值，指出 IInkAnalyzer 對 IAnalysisAlternate 精確度的信賴等級。
ms.assetid: ac1c68df-2e0c-4633-b7ee-519482a4d67a
title: 'IAnalysisAlternate：： GetRecognitionConfidence 方法 (IACom .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAnalysisAlternate.GetRecognitionConfidence
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: eacaf7e5a8feaddcd437e68cf7acfa4fc5a7fc80
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103690619"
---
# <a name="ianalysisalternategetrecognitionconfidence-method"></a>IAnalysisAlternate：： GetRecognitionConfidence 方法

取得值，指出 [**IInkAnalyzer**](iinkanalyzer.md) 對 [**IAnalysisAlternate**](ianalysisalternate.md)精確度的信賴等級。

## <a name="syntax"></a>語法


```C++
HRESULT GetRecognitionConfidence(
  [out] RecognitionConfidence *pConfidence
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*pConfidence* \[擴展\]
</dt> <dd>

[**InkRecognitionConfidence 列舉**](/windows/desktop/api/msinkaut/ne-msinkaut-inkrecognitionconfidence)的指標，指出 [**IInkAnalysisRecognizer**](iinkanalysisrecognizer.md)具有替代辨識之精確度的信賴等級。

</dd> </dl>

## <a name="return-value"></a>傳回值

如需傳回值的描述，請參閱 [類別和介面-筆跡分析](classes-and-interfaces---ink-analysis.md)。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | 僅限 Windows XP Tablet PC Edition \[ 桌面應用程式\]<br/>                                                 |
| 最低支援的伺服器<br/> | 都不支援<br/>                                                                                     |
| 標頭<br/>                   | <dl> <dt>IACom (也需要 IACom \_ c) </dt> </dl> |
| DLL<br/>                      | <dl> <dt>IACom.dll</dt> </dl>                          |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**IAnalysisAlternate**](ianalysisalternate.md)
</dt> <dt>

[**IInkAnalyzer**](iinkanalyzer.md)
</dt> <dt>

[**IInkAnalysisRecognizer**](iinkanalysisrecognizer.md)
</dt> <dt>

[**RecognitionConfidence**](recognitionconfidence.md)
</dt> <dt>

[筆跡分析參考](ink-analysis-reference.md)
</dt> </dl>

 

 




