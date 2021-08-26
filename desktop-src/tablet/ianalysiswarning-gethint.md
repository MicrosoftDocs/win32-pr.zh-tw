---
description: 抓取造成此警告的分析提示。
ms.assetid: 715aa4b2-6c45-414b-96f2-44c73a073213
title: 'IAnalysisWarning：： GetHint 方法 (IACom .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAnalysisWarning.GetHint
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 51eb76839b157c2ac9611ef9be978ea967c8e9b3506513a23b0ca70906dd32b4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119940508"
---
# <a name="ianalysiswarninggethint-method"></a>IAnalysisWarning：： GetHint 方法

抓取造成此警告的分析提示。

## <a name="syntax"></a>語法


```C++
HRESULT GetHint(
  [out] IContextNode **pAnalysisHint
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*pAnalysisHint* \[擴展\]
</dt> <dd>

造成此警告的分析提示內容節點，如果分析提示未造成此警告，則 **為 Null** 。

</dd> </dl>

## <a name="return-value"></a>傳回值

如需傳回值的描述，請參閱 [類別和介面-筆跡分析](classes-and-interfaces---ink-analysis.md)。

## <a name="remarks"></a>備註

> [!Caution]  
> 若要避免記憶體流失， [](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) \* 當您不再需要流量分析提示內容節點時，請在 *pAnalysisHint* 上呼叫 IUnknown：： Release。

 

產生 [**IAnalysisWarning**](ianalysiswarning.md) 的分析提示範例是包含拼寫不正確之模擬的分析提示。 在此情況下，「筆跡分析」會傳回 [**IAnalysisStatus**](ianalysisstatus.md) ，其中包含的 **IAnalysisWarning** 會以拼錯的模擬項參考分析提示內容節點。 此外，在此情況下，分析警告的 [**IAnalysisWarning：： GetWarningCode**](ianalysiswarning-getwarningcode.md)方法會傳回 **AnalysisWarningCode \_ FactoidNotSupported** 的 [**AnalysisWarningCode**](/windows/desktop/tablet/analysiswarningcode)值。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows僅限 XP Tablet PC Edition \[ 桌面應用程式\]<br/>                                                 |
| 最低支援的伺服器<br/> | 都不支援<br/>                                                                                     |
| 標頭<br/>                   | <dl> <dt>IACom (也需要 IACom \_ c) </dt> </dl> |
| DLL<br/>                      | <dl> <dt>IACom.dll</dt> </dl>                          |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**IAnalysisWarning**](ianalysiswarning.md)
</dt> <dt>

[**IAnalysisStatus**](ianalysisstatus.md)
</dt> <dt>

[**IInkAnalyzer：：分析方法**](iinkanalyzer-analyze.md)
</dt> <dt>

[**IInkAnalyzer：： BackgroundAnalyze 方法**](iinkanalyzer-backgroundanalyze.md)
</dt> <dt>

[**AnalysisWarningCode**](/windows/desktop/tablet/analysiswarningcode)
</dt> <dt>

[筆跡分析參考](ink-analysis-reference.md)
</dt> </dl>

 

