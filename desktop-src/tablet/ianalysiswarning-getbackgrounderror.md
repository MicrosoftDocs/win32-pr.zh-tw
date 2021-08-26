---
description: 如果發生錯誤，則捕獲背景筆墨分析作業的錯誤碼。
ms.assetid: 0255751e-9b2a-46f1-aa45-6509f9d1c658
title: 'IAnalysisWarning：： GetBackgroundError 方法 (IACom .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAnalysisWarning.GetBackgroundError
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: aa8c9c3c60f51ffd854ccdfebb6538337e7676a8c63e45899737333c41d99aad
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120057958"
---
# <a name="ianalysiswarninggetbackgrounderror-method"></a>IAnalysisWarning：： GetBackgroundError 方法

如果發生錯誤，則捕獲背景筆墨分析作業的錯誤碼。

## <a name="syntax"></a>語法


```C++
HRESULT GetBackgroundError();
```



## <a name="parameters"></a>參數

這個方法沒有任何參數。

## <a name="return-value"></a>傳回值

如需傳回值的描述，請參閱 [類別和介面-筆跡分析](classes-and-interfaces---ink-analysis.md)。

## <a name="remarks"></a>備註

如果背景分析作業中發生錯誤，則 [**IInkAnalyzer**](iinkanalyzer.md) 無法傳回錯誤碼，因為它發生在不同的執行緒中。 相反地， [**\_ IAnalysisEvents：： Results**](-ianalysisevents-results.md)事件處理常式會 [**接收 IAnalysisStatus**](ianalysisstatus.md) ，其中包含 [**AnalysisWarningCode**](/windows/desktop/tablet/analysiswarningcode)為 **AnalysisWarningCode \_ BackgroundException** 的 [**IAnalysisWarning**](ianalysiswarning.md) 。 此 **IAnalysisWarning** 包含背景分析操作的錯誤碼。 一般情況下，您的 **\_ IAnalysisEvents：： Results** 事件處理常式會傳回此錯誤碼，讓您可以在應用程式中的其他地方處理此錯誤碼。

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

[**IInkAnalyzer：： BackgroundAnalyze 方法**](iinkanalyzer-backgroundanalyze.md)
</dt> <dt>

[**\_IAnalysisEvents：： Results**](-ianalysisevents-results.md)
</dt> <dt>

[**AnalysisWarningCode**](/windows/desktop/tablet/analysiswarningcode)
</dt> <dt>

[筆跡分析參考](ink-analysis-reference.md)
</dt> </dl>

 

