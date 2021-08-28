---
description: 在衍生類別中覆寫時，評估指定的 ICoNtextNode 物件是否符合準則。
ms.assetid: ade8e59c-6aeb-4a87-a95d-229f8f0b2223
title: 'IMatchesCriteriaCallBack：： EvaluateCoNtextNode 方法 (IACom .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IMatchesCriteriaCallBack.EvaluateContextNode
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: d5855928e0827632240c8230bdcc57dff836c5287eec61f2911cc62367a8915f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118719048"
---
# <a name="imatchescriteriacallbackevaluatecontextnode-method"></a>IMatchesCriteriaCallBack：： EvaluateCoNtextNode 方法

在衍生類別中覆寫時，評估指定的 [**ICoNtextNode**](icontextnode.md) 物件是否符合準則。

## <a name="syntax"></a>語法


```C++
HRESULT EvaluateContextNode(
  [in]  IContextNode *pContextNodeToEvaluate,
  [out] VARIANT_BOOL *pbResult
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*pCoNtextNodeToEvaluate* \[在\]
</dt> <dd>

要評估的 [**ICoNtextNode**](icontextnode.md) 物件。

</dd> <dt>

*pbResult* \[擴展\]
</dt> <dd>

**變異 \_** 如果 *pCoNtextNodeToEvaluate* 符合條件，則為 TRUE;否則， **VARIANT \_ FALSE**。

</dd> </dl>

## <a name="return-value"></a>傳回值

如需傳回值的描述，請參閱 [類別和介面-筆跡分析](classes-and-interfaces---ink-analysis.md)。

## <a name="remarks"></a>備註

若要使用 [**IInkAnalyzer：： FindNodesWithCallBack 方法**](iinkanalyzer-findnodeswithcallback.md) 或 [**IInkAnalyzer：： FindNodesWithCallBackInSubTree 方法**](iinkanalyzer-findnodeswithcallbackinsubtree.md)，請建立可執行 [**IMatchesCriteriaCallBack**](imatchescriteriacallback.md)的類別。 如果 [**ICoNtextNode**](icontextnode.md)物件符合您的準則，請執行 **IMatchesCriteriaCallBack：： EvaluateCoNtextNode** 傳回 **Variant \_ TRUE** ，否則傳回 **variant \_ FALSE** 。 針對某些準則，您可能需要提供方法來初始化或維護 **IMatchesCriteriaCallBack** 物件的狀態。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows僅限 XP Tablet PC Edition \[ 桌面應用程式\]<br/>                                                 |
| 最低支援的伺服器<br/> | 都不支援<br/>                                                                                     |
| 標頭<br/>                   | <dl> <dt>IACom (也需要 IACom \_ c) </dt> </dl> |
| DLL<br/>                      | <dl> <dt>IACom.dll</dt> </dl>                          |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**IMatchesCriteriaCallBack**](imatchescriteriacallback.md)
</dt> <dt>

[**IInkAnalyzer：： FindNodesWithCallBack 方法**](iinkanalyzer-findnodeswithcallback.md)
</dt> <dt>

[**IInkAnalyzer：： FindNodesWithCallBackInSubTree 方法**](iinkanalyzer-findnodeswithcallbackinsubtree.md)
</dt> <dt>

[筆跡分析參考](ink-analysis-reference.md)
</dt> </dl>

 

 




