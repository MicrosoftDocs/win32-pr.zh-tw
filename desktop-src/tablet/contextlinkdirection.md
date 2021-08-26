---
description: 指定 ICoNtextLink 物件的方向。
ms.assetid: 4ba7dca7-6801-45bf-bbf1-1dd3172fbfa2
title: 'CoNtextLinkDirection 列舉 (IACom) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ContextLinkDirection
api_type:
- HeaderDef
api_location:
- IACom.h
ms.openlocfilehash: 1cd187b2a6efed6de5e6ee866cbd2e75ad67defc67b4b6d2250eb9117c62d89e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119941178"
---
# <a name="contextlinkdirection-enumeration"></a>CoNtextLinkDirection 列舉

指定 [**ICoNtextLink**](icontextlink.md) 物件的方向。

## <a name="syntax"></a>Syntax


```C++
typedef enum ContextLinkDirection { 
  ContextLinkDirection_LinksWith  = 0,
  ContextLinkDirection_LinksFrom  = 1,
  ContextLinkDirection_LinksTo    = 2
} ContextLinkDirection;
```



## <a name="constants"></a>常數

<dl> <dt>

<span id="ContextLinkDirection_LinksWith"></span><span id="contextlinkdirection_linkswith"></span><span id="CONTEXTLINKDIRECTION_LINKSWITH"></span>**CoNtextLinkDirection \_ LinksWith**
</dt> <dd>

[**ICoNtextNode**](icontextnode.md)是指向遠離 [**ICoNtextLink**](icontextlink.md)的方向性繪圖。

</dd> <dt>

<span id="ContextLinkDirection_LinksFrom"></span><span id="contextlinkdirection_linksfrom"></span><span id="CONTEXTLINKDIRECTION_LINKSFROM"></span>**CoNtextLinkDirection \_ LinksFrom**
</dt> <dd>

[**ICoNtextNode**](icontextnode.md)是指向 [**ICoNtextLink**](icontextlink.md)的方向性繪圖。

</dd> <dt>

<span id="ContextLinkDirection_LinksTo"></span><span id="contextlinkdirection_linksto"></span><span id="CONTEXTLINKDIRECTION_LINKSTO"></span>**CoNtextLinkDirection \_ LinksTo**
</dt> <dd>

連結中沒有任何方向的繪圖。 例如，筆墨繪圖可將筆墨文字加上底線。 沒有從底線推斷的方向。

</dd> </dl>

## <a name="examples"></a>範例

下列範例會採用 [**ICoNtextNode**](icontextnode.md) 物件， `m_pSelectedNode` 並將其連結的所有 **ICoNtextNode** 物件儲存在上階樹狀結構中，並將物件加入至 `CArray` 物件中 `linkedToNodes` 。 `CheckHResult` 是採用和字串的函式 `HRESULT` ，如果 `HRESULT` 不 **成功**，則會擲回以字串建立的例外狀況。


```C++
// Find all first ancestor that contains links of type Enclose
CArray<IContextNode*,IContextNode*> linkedToNodes = CArray<IContextNode*,IContextNode*>();
IContextNode* pAncestor;
CheckHResult(m_pSelectedNode->GetParentNode(&pAncestor),
    "IContextNode::GetParentNode failed");
while (pAncestor != NULL)
{
    // Get the links
    IContextLinks* pLinks;
    CheckHResult(pAncestor->GetContextLinks(&pLinks),
        "IContextNode::GetContextLinks failed");
    ULONG nLinks;
    CheckHResult(pLinks->GetCount(&nLinks), "IContextLinks::GetCount failed");
    for (ULONG i = 0; i < nLinks; i++)
    {
        IContextLink* pLink;
        CheckHResult(pLinks->GetContextLink(i, &pLink),
            "IContextLinks::GetContextLink failed");
        // Check link direction
        ContextLinkDirection linkDirection;
        CheckHResult(pLink->GetContextLinkDirection(&linkDirection),
            "IContextLink:GetContextLinkDirection failed");
        if (linkDirection == ContextLinkDirection_LinksTo)
        {
            // Get source node and add the array
            IContextNode* pSourceNode;
            CheckHResult(pLink->GetSourceNode(&pSourceNode),
                "IContextLink::GetSourceNode failed");
            linkedToNodes.Add(pSourceNode);
        }
    }
            
    // Go up another level
    IContextNode* pNewAncestor;
    CheckHResult(pAncestor->GetParentNode(&pNewAncestor),
        "IContextNode::GetParentNode failed");
    pAncestor = pNewAncestor;
}
```



## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows僅限 XP Tablet PC Edition \[ 桌面應用程式\]<br/>                                                 |
| 最低支援的伺服器<br/> | 都不支援<br/>                                                                                     |
| 標頭<br/>                   | <dl> <dt>IACom (也需要 IACom \_ c) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**ICoNtextLink**](icontextlink.md)
</dt> <dt>

[**ICoNtextNode::AddCoNtextLink**](icontextnode-addcontextlink.md)
</dt> </dl>

 

 




