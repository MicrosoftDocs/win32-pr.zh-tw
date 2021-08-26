---
description: 建立子 ICoNtextNode 物件，其中只包含型別、識別碼和位置的相關資訊。
ms.assetid: 181028fb-f67c-4c90-bb09-94b68a887bd1
title: 'ICoNtextNode：： CreatePartiallyPopulatedSubNode 方法 (IACom .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IContextNode.CreatePartiallyPopulatedSubNode
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 7233c6e0303f0634c71a67fde13f237feb2b2f6c6518dd8edc0b1624b4e2b6b8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119940288"
---
# <a name="icontextnodecreatepartiallypopulatedsubnode-method"></a>ICoNtextNode：： CreatePartiallyPopulatedSubNode 方法

建立子 [**ICoNtextNode**](icontextnode.md) 物件，其中只包含型別、識別碼和位置的相關資訊。

## <a name="syntax"></a>語法


```C++
HRESULT CreatePartiallyPopulatedSubNode(
  [in]  const GUID            *pNodeType,
  [in]  const GUID            *pNodeId,
  [in]        IAnalysisRegion *pNodeLocation,
  [out]       IContextNode    **pPartiallyPopulatedContextNodeCreated
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*pNodeType* \[在\]
</dt> <dd>

要建立之內容節點的型別。

</dd> <dt>

*pNodeId* \[在\]
</dt> <dd>

新節點的識別碼。

</dd> <dt>

*pNodeLocation* \[在\]
</dt> <dd>

新節點的位置。

</dd> <dt>

*pPartiallyPopulatedCoNtextNodeCreated* \[擴展\]
</dt> <dd>

新的部分填入 [**ICoNtextNode**](icontextnode.md)的指標。

</dd> </dl>

## <a name="return-value"></a>傳回值

如需傳回值的描述，請參閱 [類別和介面-筆跡分析](classes-and-interfaces---ink-analysis.md)。

## <a name="remarks"></a>備註

> [!Caution]  
> 若要避免記憶體流失， [](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) \* 當您不再需要使用內容節點時，請在 *pPartiallyPopulatedCoNtextNodeCreated* 上呼叫 IUnknown：： Release。

 

新的 [**ICoNtextNode**](icontextnode.md) 會加入至此內容節點的子節點集合 (請參閱 [**ICoNtextNode：： GetSubNodes**](icontextnode-getsubnodes.md)) 。 當有現有的子節點時，新建立的 **ICoNtextNode** 會加入做為最後一個子節點。

如需類型、識別碼和位置的詳細資訊，請參閱 [**ICoNtextNode：： GetType**](icontextnode-gettype.md)、 [**ICoNtextNode：： GetId**](icontextnode-getid.md)和 [**ICoNtextNode：： GetLocation**](icontextnode-getlocation.md)。

此方法是用來在內容節點樹狀結構中，用來建立 [**ICoNtextNode**](icontextnode.md) 物件的方法，然後才能使用它的所有相關資訊。 如需詳細資訊，請參閱 [使用筆墨分析的資料 Proxy](data-proxy-with-ink-analysis.md)。

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

[**IAnalysisRegion**](ianalysisregion.md)
</dt> <dt>

[**ICoNtextNode::GetPartiallyPopulated**](icontextnode-getpartiallypopulated.md)
</dt> <dt>

[內容節點類型](context-node-types.md)
</dt> <dt>

[筆跡分析參考](ink-analysis-reference.md)
</dt> </dl>

 

