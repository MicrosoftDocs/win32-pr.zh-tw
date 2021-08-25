---
description: 將筆劃資料從此 ICoNtextNode 移動到指定的 ICoNtextNode。
ms.assetid: 583f2de9-d32e-4177-83d1-4abbd0f9f960
title: 'ICoNtextNode：： ReparentStrokeByIdToNode 方法 (IACom .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IContextNode.ReparentStrokeByIdToNode
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: a915425900bccb15145546658d51d50dcaee14880f8f219bd1908efaa17bd3c3
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120008408"
---
# <a name="icontextnodereparentstrokebyidtonode-method"></a>ICoNtextNode：： ReparentStrokeByIdToNode 方法

將筆劃資料從此 [**ICoNtextNode**](icontextnode.md) 移動到指定的 **ICoNtextNode**。

## <a name="syntax"></a>語法


```C++
HRESULT ReparentStrokeByIdToNode(
  [in] LONG         lStrokeId,
  [in] IContextNode *pContextNodeDestination
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*lStrokeId* \[在\]
</dt> <dd>

要移動之筆劃的識別碼。

</dd> <dt>

*pCoNtextNodeDestination* \[在\]
</dt> <dd>

要移動筆劃資料的 [**ICoNtextNode**](icontextnode.md) 物件。

</dd> </dl>

## <a name="return-value"></a>傳回值

如需傳回值的描述，請參閱 [類別和介面-筆跡分析](classes-and-interfaces---ink-analysis.md)。

## <a name="remarks"></a>備註

指定的 [**ICoNtextNode**](icontextnode.md) 物件必須是 [內容節點類型](context-node-types.md) 常數的下列其中一種類型： **InkWord**、 **InkDrawing**、 **InkBullet** 或 **UnclassifiedInk**。 嘗試將筆劃移至任何其他類型的 **ICoNtextNode** 物件時，會產生 **E \_ INVALIDARG** 的傳回值。

您可以從任何 [**ICoNtextNode**](icontextnode.md) 物件呼叫這個方法，包括非筆墨分葉 **ICoNtextNode** 物件。 指定的筆劃必須由這個 **ICoNtextNode** 物件的其中一個下階參考，否則會傳回 **E \_ INVALIDARG** 。

如果確認了此 [**ICoNtextNode**](icontextnode.md)或 *PCoNtextNodeDestination* 中的 **ICoNtextNode** ，則會傳回 **E \_ INVALIDARG** (請參閱 [**ICoNtextNode：： IsConfirmed**](icontextnode-isconfirmed.md)) 。

筆墨分析器不會從結果樹狀結構中刪除空的內容節點，以回應這個方法。

-   未參考任何筆觸資料的筆墨分葉節點是空的節點。
-   未參考任何子節點的容器節點是空的節點。

空白節點會在筆跡分析作業期間于樹狀結構中產生錯誤。 若要從筆墨分析器的樹狀結構中移除節點，請呼叫父節點的 [**ICoNtextNode：:D eletesubnode**](icontextnode-deletesubnode.md) 方法 (查看 [**ICoNtextNode：： GetParentNode**](icontextnode-getparentnode.md)) 。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows僅限 XP Tablet PC Edition \[ 桌面應用程式\]<br/>                                                 |
| 最低支援的伺服器<br/> | 都不支援<br/>                                                                                     |
| 標頭<br/>                   | <dl> <dt>IACom (也需要 IACom \_ c) </dt> </dl> |
| DLL<br/>                      | <dl> <dt>IACom.dll</dt> </dl>                          |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**ICoNtextNode**](icontextnode.md)
</dt> <dt>

[**ICoNtextNode::SetStrokes**](icontextnode-setstrokes.md)
</dt> <dt>

[筆跡分析參考](ink-analysis-reference.md)
</dt> </dl>

 

 




