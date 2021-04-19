---
description: 抓取 ICoNtextNode 物件的位置和大小。
ms.assetid: 40787a9b-1017-4209-aec8-09b7332bfa8a
title: 'ICoNtextNode：： GetLocation 方法 (IACom .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IContextNode.GetLocation
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 13366442399961eaba7a411b1b3c87171f0879b8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106970824"
---
# <a name="icontextnodegetlocation-method"></a>ICoNtextNode：： GetLocation 方法

抓取 [**ICoNtextNode**](icontextnode.md) 物件的位置和大小。

## <a name="syntax"></a>語法


```C++
HRESULT GetLocation(
  [out] IAnalysisRegion **ppIAnalysisRegion
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*ppIAnalysisRegion* \[擴展\]
</dt> <dd>

[**ICoNtextNode**](icontextnode.md)物件之位置和大小的指標。

</dd> </dl>

## <a name="return-value"></a>傳回值

如需傳回值的描述，請參閱 [類別和介面-筆跡分析](classes-and-interfaces---ink-analysis.md)。

## <a name="remarks"></a>備註

> [!Caution]  
> 若要避免記憶體流失，請在 ppIAnalysisRegion 上呼叫 [**IUnknown：： Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) （ \* 當您不再需要流量分析區域時）。

 

容器節點的位置是藉由尋找所有分葉位置的聯集來決定。 筆跡分葉節點的位置是藉由尋找相關聯筆劃之周框方塊的聯集來決定。 當建立節點時，會設定非筆墨分葉節點的位置，並且可使用 [**ICoNtextNode：： SetLocation**](icontextnode-setlocation.md)進行更新。

## <a name="examples"></a>範例

下列範例顯示 helper 方法，此方法會抓取指定節點的相關資訊，也就是其 *pCoNtextNode* 參數。 此 helper 方法會傳回下列方法的資訊。

-   [**ICoNtextNode：： GetId**](icontextnode-getid.md)
-   [**ICoNtextNode：： GetType**](icontextnode-gettype.md)
-   **ICoNtextNode::GetLocation**
-   [**ICoNtextNode::GetParentNode**](icontextnode-getparentnode.md)


```C++
// Helper method for collecting information about a context node.
HRESULT CMyClass::GetNodeInformation(
    IContextNode *pContextNode,
    GUID *pNodeIdentifier,
    GUID *pContextNodeType,
    IAnalysisRegion **ppAnalysisRegion,
    IContextNode **ppParentNode,
    IContextNodes **ppSubNodes)
{
    // Get the identifier of the context node.
    HRESULT hr = pContextNode->GetId(pNodeIdentifier);

    if (FAILED(hr))
    {
        return hr;
    }

    // Get the type identifier for the context node.
    hr = pContextNode->GetType(pContextNodeType);

    if (FAILED(hr))
    {
        return hr;
    }

    // Get the location of the context node.
    hr = pContextNode->GetLocation(ppAnalysisRegion);

    if (FAILED(hr))
    {
        return hr;
    }

    // Get the parent node of the context node.
    hr = pContextNode->GetParentNode(ppParentNode);

    if (FAILED(hr))
    {
        if ((*ppAnalysisRegion) != NULL)
        {
            (*ppAnalysisRegion)->Release();
            (*ppAnalysisRegion) = NULL;
        }
        return hr;
    }

    // Get the subnodes of the context node.
    hr = pContextNode->GetSubNodes(ppSubNodes);

    if (FAILED(hr))
    {
        if (*ppAnalysisRegion)
        {
            (*ppAnalysisRegion)->Release();
            (*ppAnalysisRegion) = NULL;
        }
        if (*ppParentNode)
        {
            (*ppParentNode)->Release();
            (*ppParentNode) = NULL;
        }
        return hr;
    }

    return hr;
}
```



## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | 僅限 Windows XP Tablet PC Edition \[ 桌面應用程式\]<br/>                                                 |
| 最低支援的伺服器<br/> | 都不支援<br/>                                                                                     |
| 標頭<br/>                   | <dl> <dt>IACom (也需要 IACom \_ c) </dt> </dl> |
| DLL<br/>                      | <dl> <dt>IACom.dll</dt> </dl>                          |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**ICoNtextNode**](icontextnode.md)
</dt> <dt>

[**IAnalysisRegion**](ianalysisregion.md)
</dt> <dt>

[**ICoNtextNode::SetLocation**](icontextnode-setlocation.md)
</dt> <dt>

[筆跡分析參考](ink-analysis-reference.md)
</dt> </dl>

 

