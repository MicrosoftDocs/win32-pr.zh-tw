---
description: 抓取包含指定筆劃之指定型別的所有 ICoNtextNode 物件。
ms.assetid: c674a03b-841c-4a9c-8268-302bc4038934
title: 'IInkAnalyzer：： FindNodesOfTypeForStrokes 方法 (IACom .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IInkAnalyzer.FindNodesOfTypeForStrokes
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 2dd98c72007a69521506e2be21ad10edeb46df27
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106970823"
---
# <a name="iinkanalyzerfindnodesoftypeforstrokes-method"></a>IInkAnalyzer：： FindNodesOfTypeForStrokes 方法

抓取包含指定筆劃之指定型別的所有 [**ICoNtextNode**](icontextnode.md) 物件。

## <a name="syntax"></a>語法


```C++
HRESULT FindNodesOfTypeForStrokes(
  [in]  const GUID          *pNodeType,
  [in]        ULONG         ulStrokeIdsCount,
  [in]        LONG          *plStrokeIds,
  [out]       IContextNodes **ppContextNodesFound
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*pNodeType* \[在\]
</dt> <dd>

 (GUID) 的全域唯一識別碼，可指定節點類型。

</dd> <dt>

*ulStrokeIdsCount* \[在\]
</dt> <dd>

傳入的筆觸識別碼數目。

</dd> <dt>

*plStrokeIds* \[在\]
</dt> <dd>

筆觸識別碼的陣列。

</dd> <dt>

*ppCoNtextNodesFound* \[擴展\]
</dt> <dd>

[**ICoNtextNode**](icontextnode.md)物件的集合，其中包含 *pNodeType* 類型的所有節點，這些節點包含 *plStrokeIds* 陣列中具有識別碼的筆劃。

</dd> </dl>

## <a name="return-value"></a>傳回值

如需傳回值的描述，請參閱 [類別和介面-筆跡分析](classes-and-interfaces---ink-analysis.md)。

## <a name="remarks"></a>備註

> [!Caution]  
> 若要避免記憶體流失，請在 ppCoNtextNodesFound 上呼叫 [**IUnknown：： Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) （ \* 當您不再需要使用物件時）。

 

*PNodeType* 屬性必須包含來自 [內容節點類型](context-node-types.md)常數的 GUID。

如果指定的節點類型不是分葉節點，但其中一個節點的下階參考筆劃集合中的筆劃，則該節點會加入至所傳回的集合。

如果 [**IInkAnalyzer**](iinkanalyzer.md) 未包含這類 [**ICoNtextNode**](icontextnode.md)，則會傳回空的 [**ICoNtextNodes**](icontextnodes.md) 集合。

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

[**IInkAnalyzer：： FindInkLeafNodes 方法**](iinkanalyzer-findinkleafnodes.md)
</dt> <dt>

[**IInkAnalyzer：： FindInkLeafNodesForStrokes 方法**](iinkanalyzer-findinkleafnodesforstrokes.md)
</dt> <dt>

[**IInkAnalyzer：： FindLeafNodes 方法**](iinkanalyzer-findleafnodes.md)
</dt> <dt>

[**IInkAnalyzer：： FindNode 方法**](iinkanalyzer-findnode.md)
</dt> <dt>

[**IInkAnalyzer：： FindNodesOfType 方法**](iinkanalyzer-findnodesoftype.md)
</dt> <dt>

[**IInkAnalyzer：： FindNodesOfTypeInSubTree 方法**](iinkanalyzer-findnodesoftypeinsubtree.md)
</dt> <dt>

[**IInkAnalyzer：： FindNodesWithCallBack 方法**](iinkanalyzer-findnodeswithcallback.md)
</dt> <dt>

[**IInkAnalyzer：： FindNodesWithCallBackInSubTree 方法**](iinkanalyzer-findnodeswithcallbackinsubtree.md)
</dt> <dt>

[筆跡分析參考](ink-analysis-reference.md)
</dt> </dl>

 

