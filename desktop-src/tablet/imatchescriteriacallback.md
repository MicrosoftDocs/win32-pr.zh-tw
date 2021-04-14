---
description: 公開方法，以評估 ICoNtextNode 物件是否符合或失敗指定的條件。
ms.assetid: 8b094882-e739-4088-87de-6ef4719b0b5b
title: 'IMatchesCriteriaCallBack 介面 (IACom .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IMatchesCriteriaCallBack
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 960bd221bdd1f621f6ec4deb5ea167f5bf9ee4d4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104511035"
---
# <a name="imatchescriteriacallback-interface"></a>IMatchesCriteriaCallBack 介面

公開方法，以評估 [**ICoNtextNode**](icontextnode.md) 物件是否符合或失敗指定的條件。

## <a name="members"></a>成員

**IMatchesCriteriaCallBack** 介面繼承自 [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown)介面。 **IMatchesCriteriaCallBack** 也有下列類型的成員：

-   [方法](#methods)

### <a name="methods"></a>方法

**IMatchesCriteriaCallBack** 介面具有這些方法。



| 方法                                                                      | 描述                                                                                                                                  |
|:----------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------|
| [**EvaluateCoNtextNode**](imatchescriteriacallback-evaluatecontextnode.md) | 在衍生類別中覆寫時，評估指定的 [**ICoNtextNode**](icontextnode.md) 物件是否符合準則。<br/> |



 

## <a name="remarks"></a>備註

若要使用 [**IInkAnalyzer：： FindNodesWithCallBack 方法**](iinkanalyzer-findnodeswithcallback.md) 或 [**IInkAnalyzer：： FindNodesWithCallBackInSubTree 方法**](iinkanalyzer-findnodeswithcallbackinsubtree.md)，請建立可執行 **IMatchesCriteriaCallBack** 的類別。 如果 [**ICoNtextNode**](icontextnode.md)物件符合您的準則，請執行 [**IMatchesCriteriaCallBack：： EvaluateCoNtextNode**](imatchescriteriacallback-evaluatecontextnode.md)傳回 **Variant \_ TRUE** ，否則傳回 **variant \_ FALSE** 。 針對某些準則，您可能需要提供方法來初始化或維護 **IMatchesCriteriaCallBack** 物件的狀態。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | 僅限 Windows XP Tablet PC Edition \[ 桌面應用程式\]<br/>                                                 |
| 最低支援的伺服器<br/> | 都不支援<br/>                                                                                     |
| 標頭<br/>                   | <dl> <dt>IACom (也需要 IACom \_ c) </dt> </dl> |
| DLL<br/>                      | <dl> <dt>IACom.dll</dt> </dl>                          |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**IInkAnalyzer：： FindNodesWithCallBack 方法**](iinkanalyzer-findnodeswithcallback.md)
</dt> <dt>

[**IInkAnalyzer：： FindNodesWithCallBackInSubTree 方法**](iinkanalyzer-findnodeswithcallbackinsubtree.md)
</dt> <dt>

[筆跡分析參考](ink-analysis-reference.md)
</dt> </dl>

 

