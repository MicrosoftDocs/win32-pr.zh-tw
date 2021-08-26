---
description: 取得與這個替代相關聯的 ICoNtextNode 物件。
ms.assetid: 6dfae9cc-d9d2-44de-b6cf-80bbcd296390
title: 'IAnalysisAlternate：： GetAlternateNodes 方法 (IACom .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAnalysisAlternate.GetAlternateNodes
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: fbaff3cea515c9636127ce2267b9f05e0c0a0006b96046a7f2474661b3b76f77
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119935518"
---
# <a name="ianalysisalternategetalternatenodes-method"></a>IAnalysisAlternate：： GetAlternateNodes 方法

取得與這個替代相關聯的 [**ICoNtextNode**](icontextnode.md) 物件。

## <a name="syntax"></a>語法


```C++
HRESULT GetAlternateNodes(
  [out] IContextNodes **ppAlternateNodes
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*ppAlternateNodes* \[擴展\]
</dt> <dd>

[**ICoNtextNodes**](icontextnodes.md)集合的指標，其中包含與這個替代相關聯的 [**ICoNtextNode**](icontextnode.md)物件。

</dd> </dl>

## <a name="return-value"></a>傳回值

如需傳回值的描述，請參閱 [類別和介面-筆跡分析](classes-and-interfaces---ink-analysis.md)。

## <a name="remarks"></a>備註

> [!Caution]  
> 若要避免記憶體流失， [](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) \* 當您不再需要使用內容節點集合時，請在 *ppAlternateNodes* 上呼叫 IUnknown：： Release。

 

這個方法會傳回與這個替代相關聯的分葉內容節點。 分葉節點的範例包括 InkWord、TextWord、Image、InkDrawing 和 InkBullet 內容節點。 如需詳細資訊，請參閱 [**ICoNtextNode：： GetType**](icontextnode-gettype.md) 和 [CoNtext 節點類型](context-node-types.md)。

因為它們對應至替代專案，所以這些 [**ICoNtextNode**](icontextnode.md) 物件不是 [**IInkAnalyzer**](iinkanalyzer.md) 物件根 **ICoNtextNode** 的下階 (請參閱 [**IInkAnalyzer：： GetRootNode 方法**](iinkanalyzer-getrootnode.md)) ，除非它們是最上層的替代專案，也就是 [**IAnalysisAlternates**](ianalysisalternates.md) 集合中的第一個元素。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows僅限 XP Tablet PC Edition \[ 桌面應用程式\]<br/>                                                 |
| 最低支援的伺服器<br/> | 都不支援<br/>                                                                                     |
| 標頭<br/>                   | <dl> <dt>IACom (也需要 IACom \_ c) </dt> </dl> |
| DLL<br/>                      | <dl> <dt>IACom.dll</dt> </dl>                          |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**IAnalysisAlternate**](ianalysisalternate.md)
</dt> <dt>

[**ICoNtextNode**](icontextnode.md)
</dt> <dt>

[**ICoNtextNodes**](icontextnodes.md)
</dt> <dt>

[筆跡分析參考](ink-analysis-reference.md)
</dt> <dt>

[系統。Windows。AnalysisCore. AnalysisAlternateBase. AlternateNodes](ianalysisalternate-getalternatenodes.md)
</dt> </dl>

 

