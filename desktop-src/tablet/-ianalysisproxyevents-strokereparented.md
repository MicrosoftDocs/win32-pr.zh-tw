---
description: 當 IInkAnalyzer 將筆劃從一個 ICoNtextNode 物件移動到另一個時，就會發生。
ms.assetid: a90214af-c3ea-4e2a-94b4-bb5746a2b476
title: '_IAnalysisProxyEvents：： StrokeReparented 事件 (IACom .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- _IAnalysisProxyEvents.StrokeReparented
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 1e9262eb7b4ce2b323669eeb084abb597b5fe00488df90fc5fde0b2876b7e953
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118967867"
---
# <a name="_ianalysisproxyeventsstrokereparented-event"></a>\_IAnalysisProxyEvents：： StrokeReparented 事件

當 [**IInkAnalyzer**](iinkanalyzer.md) 將筆劃從一個 [**ICoNtextNode**](icontextnode.md) 物件移動到另一個時，就會發生。

## <a name="syntax"></a>語法


```C++
HRESULT StrokeReparented(
  [in] IInkAnalyzer *pInkAnalyzer,
  [in] LONG         lStrokeIdToMove,
  [in] IContextNode *pSourceContextNode,
  [in] IContextNode *pDestinationContextNode
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*pInkAnalyzer* \[在\]
</dt> <dd>

移動筆劃的 [**IInkAnalyzer**](iinkanalyzer.md) 物件。

</dd> <dt>

*lStrokeIdToMove* \[在\]
</dt> <dd>

要移動之筆劃的識別碼。

</dd> <dt>

*pSourceCoNtextNode* \[在\]
</dt> <dd>

要從中移動筆劃的 [**ICoNtextNode**](icontextnode.md) 物件。

</dd> <dt>

*pDestinationCoNtextNode* \[在\]
</dt> <dd>

要將筆劃移動至其中的 [**ICoNtextNode**](icontextnode.md) 物件。

</dd> </dl>

## <a name="return-value"></a>傳回值

如需傳回值的描述，請參閱 [類別和介面-筆跡分析](classes-and-interfaces---ink-analysis.md)。

## <a name="remarks"></a>備註

當您的應用程式維護自己的資料結構（與 [**IInkAnalyzer**](iinkanalyzer.md)同步處理）時，請使用此事件。 此事件發生于筆墨分析的協調階段，或為了回應將筆劃資料從一個 ICoNtextNode 移至另一個 [](icontextnode.md)的 **IInkAnalyzer** 方法。

如需有關同步處理應用程式資料與 [**IInkAnalyzer**](iinkanalyzer.md)的詳細資訊，請參閱 [使用筆墨分析的資料 Proxy](data-proxy-with-ink-analysis.md)。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows僅限 XP Tablet PC Edition \[ 桌面應用程式\]<br/>                                                 |
| 最低支援的伺服器<br/> | 都不支援<br/>                                                                                     |
| 標頭<br/>                   | <dl> <dt>IACom (也需要 IACom \_ c) </dt> </dl> |
| DLL<br/>                      | <dl> <dt>IACom.dll</dt> </dl>                          |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**\_IAnalysisProxyEvents**](-ianalysisproxyevents.md)
</dt> <dt>

[**IInkAnalyzer**](iinkanalyzer.md)
</dt> <dt>

[**ICoNtextNode**](icontextnode.md)
</dt> <dt>

[**IInkAnalyzer：：分析方法**](iinkanalyzer-analyze.md)
</dt> <dt>

[**IInkAnalyzer：： BackgroundAnalyze 方法**](iinkanalyzer-backgroundanalyze.md)
</dt> <dt>

[筆跡分析參考](ink-analysis-reference.md)
</dt> </dl>

 

 




