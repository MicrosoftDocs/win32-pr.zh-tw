---
description: 抓取包含指定筆劃的筆墨分葉節點。
ms.assetid: d9ebc57d-63f5-4175-8bb6-a688b98823d4
title: 'IInkAnalyzer：： FindInkLeafNodesForStrokes 方法 (IACom .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IInkAnalyzer.FindInkLeafNodesForStrokes
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: a7424f62008e15feb538df7a6a27745dda17bf6ace4612218608f8e509e75e59
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118967277"
---
# <a name="iinkanalyzerfindinkleafnodesforstrokes-method"></a>IInkAnalyzer：： FindInkLeafNodesForStrokes 方法

抓取包含指定筆劃的筆墨分葉節點。

## <a name="syntax"></a>語法


```C++
HRESULT FindInkLeafNodesForStrokes(
  [in]  ULONG         ulStrokeIdsCount,
  [in]  LONG          *plStrokeIds,
  [out] IContextNodes **ppContextNodesFound
);
```



## <a name="parameters"></a>參數

<dl> <dt>

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

[**ICoNtextNode**](icontextnode.md)物件的集合，其中包含包含 *plStrokeIds* 陣列中識別碼之筆觸的所有筆墨分葉節點。

</dd> </dl>

## <a name="return-value"></a>傳回值

如需傳回值的描述，請參閱 [類別和介面-筆跡分析](classes-and-interfaces---ink-analysis.md)。

## <a name="remarks"></a>備註

> [!Caution]  
> 若要避免記憶體流失，請在 *ppCoNtextNodesFound* 上呼叫 [**IUnknown：： Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) （當您不再需要使用物件時）。

 

分葉節點不包含子節點。 筆墨節點包含筆觸資料。 筆墨分葉節點的範例包括 InkWord、InkDrawing、andInkBullet [**ICoNtextNode**](icontextnode.md) 物件。 如需詳細資訊，請參閱 [內容節點類型](context-node-types.md)。

如果沒有任何節點包含指定的筆觸，則會傳回空的 [**ICoNtextNodes**](icontextnodes.md) 集合。 同樣地，如果 *ulStrokeIdsCount* 為零，則會傳回空的 **ICoNtextNodes** 集合。

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

[**IInkAnalyzer：： FindInkLeafNodes 方法**](iinkanalyzer-findinkleafnodes.md)
</dt> <dt>

[**IInkAnalyzer：： FindLeafNodes 方法**](iinkanalyzer-findleafnodes.md)
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

 

