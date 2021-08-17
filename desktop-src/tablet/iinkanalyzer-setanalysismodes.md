---
description: 修改旗標，以控制 IInkAnalyzer 執行筆墨分析的方式。
ms.assetid: cb82edd0-1f15-4313-a286-1fcd715ac6df
title: 'IInkAnalyzer：： SetAnalysisModes 方法 (IACom .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IInkAnalyzer.SetAnalysisModes
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: c7edd167cd40b80a01fd2f23243c931fe6a15795da08d7735b6e2433c462ee01
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119091494"
---
# <a name="iinkanalyzersetanalysismodes-method"></a>IInkAnalyzer：： SetAnalysisModes 方法

修改旗標，以控制 [**IInkAnalyzer**](iinkanalyzer.md) 執行筆墨分析的方式。

## <a name="syntax"></a>語法


```C++
HRESULT SetAnalysisModes(
  [in] AnalysisModes analysisMode
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*analysisMode* \[在\]
</dt> <dd>

[**AnalysisModes**](analysismodes.md)列舉值的位元組合。

</dd> </dl>

## <a name="return-value"></a>傳回值

如需傳回值的描述，請參閱 [類別和介面-筆跡分析](classes-and-interfaces---ink-analysis.md)。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows僅限 XP Tablet PC Edition \[ 桌面應用程式\]<br/>                                                 |
| 最低支援的伺服器<br/> | 都不支援<br/>                                                                                     |
| 標頭<br/>                   | <dl> <dt>IACom (也需要 IACom \_ c) </dt> </dl> |
| DLL<br/>                      | <dl> <dt>IACom.dll</dt> </dl>                          |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**IInkAnalyzer**](iinkanalyzer.md)
</dt> <dt>

[**AnalysisModes**](analysismodes.md)
</dt> <dt>

[**IInkAnalyzer：：分析方法**](iinkanalyzer-analyze.md)
</dt> <dt>

[**IInkAnalyzer：： BackgroundAnalyze 方法**](iinkanalyzer-backgroundanalyze.md)
</dt> <dt>

[**IInkAnalyzer：： GetAnalysisModes 方法**](iinkanalyzer-getanalysismodes.md)
</dt> <dt>

[筆跡分析參考](ink-analysis-reference.md)
</dt> </dl>

 

 




