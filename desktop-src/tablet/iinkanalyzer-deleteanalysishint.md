---
description: 從 IInkAnalyzer 中移除分析提示。
ms.assetid: ba5498d4-d31c-4b3f-9004-0448e18d4835
title: 'IInkAnalyzer：:D eleteAnalysisHint 方法 (IACom .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IInkAnalyzer.DeleteAnalysisHint
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: f84f718701abd5bc76b55427aab9df072f758c3a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104113352"
---
# <a name="iinkanalyzerdeleteanalysishint-method"></a>IInkAnalyzer：:D eleteAnalysisHint 方法

從 [**IInkAnalyzer**](iinkanalyzer.md)中移除分析提示。

## <a name="syntax"></a>語法


```C++
HRESULT DeleteAnalysisHint(
  [in] IContextNode *pHintToDelete
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*pHintToDelete* \[在\]
</dt> <dd>

來自 [**IInkAnalyzer**](iinkanalyzer.md)的分析提示。

</dd> </dl>

## <a name="return-value"></a>傳回值

如需傳回值的描述，請參閱 [類別和介面-筆跡分析](classes-and-interfaces---ink-analysis.md)。

## <a name="remarks"></a>備註

移除分析提示並不會標示提示的區域以進行 reanalysis。 若要標記 reanalysis 提示內的區域，請使用 [**IInkAnalyzer：： SetDirtyRegion 方法**](iinkanalyzer-setdirtyregion.md) ，將中途區域設定為目前中途區域和分析提示區域的聯集。

提示已從分析器移除;不過， [**ICoNtextNode**](icontextnode.md) 本身不會被刪除。

當 *pHintToDelete* 是不是 AnalysisHint 類型的 [**ICoNtextNode**](icontextnode.md) 時，這個方法會傳回錯誤碼 (請參閱 [**ICoNtextNode：： GetType**](icontextnode-gettype.md)) 。

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

[**IInkAnalyzer：： CreateAnalysisHint 方法**](iinkanalyzer-createanalysishint.md)
</dt> <dt>

[**IInkAnalyzer：： GetAnalysisHints 方法**](iinkanalyzer-getanalysishints.md)
</dt> <dt>

[**IInkAnalyzer：： GetAnalysisHintsByName 方法**](iinkanalyzer-getanalysishintsbyname.md)
</dt> <dt>

[筆跡分析參考](ink-analysis-reference.md)
</dt> </dl>

 

 




