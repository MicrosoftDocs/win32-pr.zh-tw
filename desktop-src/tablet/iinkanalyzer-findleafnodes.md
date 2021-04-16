---
description: 抓取所有分葉節點。
ms.assetid: 5534053c-c5b9-4576-857f-c8af39e821a7
title: 'IInkAnalyzer：： FindLeafNodes 方法 (IACom .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IInkAnalyzer.FindLeafNodes
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: f923afe94c25e45dbcbfe79d554282b69ebec3a2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104511660"
---
# <a name="iinkanalyzerfindleafnodes-method"></a>IInkAnalyzer：： FindLeafNodes 方法

抓取所有分葉節點。

## <a name="syntax"></a>語法


```C++
HRESULT FindLeafNodes(
  [out] IContextNodes **ppContextNodesFound
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*ppCoNtextNodesFound* \[擴展\]
</dt> <dd>

[**ICoNtextNodes**](icontextnodes.md)集合的指標，其中包含所有分葉節點。

</dd> </dl>

## <a name="return-value"></a>傳回值

如需傳回值的描述，請參閱 [類別和介面-筆跡分析](classes-and-interfaces---ink-analysis.md)。

## <a name="remarks"></a>備註

> [!Caution]  
> 若要避免記憶體流失，請在 *ppCoNtextNodesFound* 上呼叫 [**IUnknown：： Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) （當您不再需要使用物件時）。

 

分葉節點不包含子節點。 筆墨分葉節點的範例包括 InkWord、TextWord、Image、InkDrawing 和 InkBullet [**ICoNtextNode**](icontextnode.md) 物件。 如需詳細資訊，請參閱 [內容節點類型](context-node-types.md)。

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

[**IInkAnalyzer：： FindNode 方法**](iinkanalyzer-findnode.md)
</dt> <dt>

[**IInkAnalyzer：： FindNodesOfType 方法**](iinkanalyzer-findnodesoftype.md)
</dt> <dt>

[**IInkAnalyzer：： FindNodesOfTypeForStrokes 方法**](iinkanalyzer-findnodesoftypeforstrokes.md)
</dt> <dt>

[**IInkAnalyzer：： FindNodesOfTypeInSubTree 方法**](iinkanalyzer-findnodesoftypeinsubtree.md)
</dt> <dt>

[**IInkAnalyzer：： FindNodesWithCallBack 方法**](iinkanalyzer-findnodeswithcallback.md)
</dt> <dt>

[**IInkAnalyzer：： FindNodesWithCallBackInSubTree 方法**](iinkanalyzer-findnodeswithcallbackinsubtree.md)
</dt> <dt>

[筆跡分析參考](ink-analysis-reference.md)
</dt> </dl>

 

