---
description: 捕獲 ICoNtextNode 物件的型別。
ms.assetid: 285384ce-5cdc-47f5-a1c4-6c6d7f18e215
title: 'ICoNtextNode：： GetType 方法 (IACom .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IContextNode.GetType
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 8602de657415891646ab85101aebb738458db670664caea8442328b502690042
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118044748"
---
# <a name="icontextnodegettype-method"></a>ICoNtextNode：： GetType 方法

捕獲 [**ICoNtextNode**](icontextnode.md) 物件的型別。

## <a name="syntax"></a>語法


```C++
HRESULT GetType(
  [out] GUID *pContextNodeType
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*pCoNtextNodeType* \[擴展\]
</dt> <dd>

[**ICoNtextNode**](icontextnode.md)物件的類型。

</dd> </dl>

## <a name="return-value"></a>傳回值

如需傳回值的描述，請參閱 [類別和介面-筆跡分析](classes-and-interfaces---ink-analysis.md)。

## <a name="remarks"></a>備註

節點的類型會在 [內容節點類型](context-node-types.md) 常數中描述。

## <a name="examples"></a>範例

下列範例顯示 helper 方法，此方法會抓取指定節點的相關資訊，也就是其 *pCoNtextNode* 參數。 此 helper 方法會傳回下列方法的資訊。

-   [**ICoNtextNode：： GetId**](icontextnode-getid.md)
-   **ICoNtextNode：： GetType**
-   [**ICoNtextNode::GetLocation**](icontextnode-getlocation.md)
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
| 最低支援的用戶端<br/> | Windows僅限 XP Tablet PC Edition \[ 桌面應用程式\]<br/>                                                 |
| 最低支援的伺服器<br/> | 都不支援<br/>                                                                                     |
| 標頭<br/>                   | <dl> <dt>IACom (也需要 IACom \_ c) </dt> </dl> |
| DLL<br/>                      | <dl> <dt>IACom.dll</dt> </dl>                          |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**ICoNtextNode**](icontextnode.md)
</dt> <dt>

[內容節點類型](context-node-types.md)
</dt> <dt>

[筆跡分析參考](ink-analysis-reference.md)
</dt> </dl>

 

 




