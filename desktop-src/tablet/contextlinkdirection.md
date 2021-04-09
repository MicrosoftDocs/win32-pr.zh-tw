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
ms.openlocfilehash: 82e10c7e908b4cc4035d8bfdde55d863f7b6ecf2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103849712"
---
# <a name="contextlinkdirection-enumeration"></a><span data-ttu-id="7cea0-103">CoNtextLinkDirection 列舉</span><span class="sxs-lookup"><span data-stu-id="7cea0-103">ContextLinkDirection enumeration</span></span>

<span data-ttu-id="7cea0-104">指定 [**ICoNtextLink**](icontextlink.md) 物件的方向。</span><span class="sxs-lookup"><span data-stu-id="7cea0-104">Specifies the direction of an [**IContextLink**](icontextlink.md) object.</span></span>

## <a name="syntax"></a><span data-ttu-id="7cea0-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="7cea0-105">Syntax</span></span>


```C++
typedef enum ContextLinkDirection { 
  ContextLinkDirection_LinksWith  = 0,
  ContextLinkDirection_LinksFrom  = 1,
  ContextLinkDirection_LinksTo    = 2
} ContextLinkDirection;
```



## <a name="constants"></a><span data-ttu-id="7cea0-106">常數</span><span class="sxs-lookup"><span data-stu-id="7cea0-106">Constants</span></span>

<dl> <dt>

<span data-ttu-id="7cea0-107"><span id="ContextLinkDirection_LinksWith"></span><span id="contextlinkdirection_linkswith"></span><span id="CONTEXTLINKDIRECTION_LINKSWITH"></span>**CoNtextLinkDirection \_ LinksWith**</span><span class="sxs-lookup"><span data-stu-id="7cea0-107"><span id="ContextLinkDirection_LinksWith"></span><span id="contextlinkdirection_linkswith"></span><span id="CONTEXTLINKDIRECTION_LINKSWITH"></span>**ContextLinkDirection\_LinksWith**</span></span>
</dt> <dd>

<span data-ttu-id="7cea0-108">[**ICoNtextNode**](icontextnode.md)是指向遠離 [**ICoNtextLink**](icontextlink.md)的方向性繪圖。</span><span class="sxs-lookup"><span data-stu-id="7cea0-108">The [**IContextNode**](icontextnode.md) is a directional drawing that points away from the [**IContextLink**](icontextlink.md).</span></span>

</dd> <dt>

<span data-ttu-id="7cea0-109"><span id="ContextLinkDirection_LinksFrom"></span><span id="contextlinkdirection_linksfrom"></span><span id="CONTEXTLINKDIRECTION_LINKSFROM"></span>**CoNtextLinkDirection \_ LinksFrom**</span><span class="sxs-lookup"><span data-stu-id="7cea0-109"><span id="ContextLinkDirection_LinksFrom"></span><span id="contextlinkdirection_linksfrom"></span><span id="CONTEXTLINKDIRECTION_LINKSFROM"></span>**ContextLinkDirection\_LinksFrom**</span></span>
</dt> <dd>

<span data-ttu-id="7cea0-110">[**ICoNtextNode**](icontextnode.md)是指向 [**ICoNtextLink**](icontextlink.md)的方向性繪圖。</span><span class="sxs-lookup"><span data-stu-id="7cea0-110">The [**IContextNode**](icontextnode.md) is a directional drawing that points to the [**IContextLink**](icontextlink.md).</span></span>

</dd> <dt>

<span data-ttu-id="7cea0-111"><span id="ContextLinkDirection_LinksTo"></span><span id="contextlinkdirection_linksto"></span><span id="CONTEXTLINKDIRECTION_LINKSTO"></span>**CoNtextLinkDirection \_ LinksTo**</span><span class="sxs-lookup"><span data-stu-id="7cea0-111"><span id="ContextLinkDirection_LinksTo"></span><span id="contextlinkdirection_linksto"></span><span id="CONTEXTLINKDIRECTION_LINKSTO"></span>**ContextLinkDirection\_LinksTo**</span></span>
</dt> <dd>

<span data-ttu-id="7cea0-112">連結中沒有任何方向的繪圖。</span><span class="sxs-lookup"><span data-stu-id="7cea0-112">There are no directional drawings in the link.</span></span> <span data-ttu-id="7cea0-113">例如，筆墨繪圖可將筆墨文字加上底線。</span><span class="sxs-lookup"><span data-stu-id="7cea0-113">For example, an ink drawing can underline an ink word.</span></span> <span data-ttu-id="7cea0-114">沒有從底線推斷的方向。</span><span class="sxs-lookup"><span data-stu-id="7cea0-114">There is no direction inferred from the underline.</span></span>

</dd> </dl>

## <a name="examples"></a><span data-ttu-id="7cea0-115">範例</span><span class="sxs-lookup"><span data-stu-id="7cea0-115">Examples</span></span>

<span data-ttu-id="7cea0-116">下列範例會採用 [**ICoNtextNode**](icontextnode.md) 物件， `m_pSelectedNode` 並將其連結的所有 **ICoNtextNode** 物件儲存在上階樹狀結構中，並將物件加入至 `CArray` 物件中 `linkedToNodes` 。</span><span class="sxs-lookup"><span data-stu-id="7cea0-116">The following example takes an [**IContextNode**](icontextnode.md) object, `m_pSelectedNode`, and saves all the **IContextNode** objects that it links to by walking up the ancestor tree and adding the objects into a `CArray` object, `linkedToNodes`.</span></span> <span data-ttu-id="7cea0-117">`CheckHResult` 是採用和字串的函式 `HRESULT` ，如果 `HRESULT` 不 **成功**，則會擲回以字串建立的例外狀況。</span><span class="sxs-lookup"><span data-stu-id="7cea0-117">`CheckHResult` is a function that takes an `HRESULT` and a string, and throws an exception created with the string if the `HRESULT` is not **SUCCESS**.</span></span>


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



## <a name="requirements"></a><span data-ttu-id="7cea0-118">規格需求</span><span class="sxs-lookup"><span data-stu-id="7cea0-118">Requirements</span></span>



| <span data-ttu-id="7cea0-119">需求</span><span class="sxs-lookup"><span data-stu-id="7cea0-119">Requirement</span></span> | <span data-ttu-id="7cea0-120">值</span><span class="sxs-lookup"><span data-stu-id="7cea0-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7cea0-121">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="7cea0-121">Minimum supported client</span></span><br/> | <span data-ttu-id="7cea0-122">僅限 Windows XP Tablet PC Edition \[ 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="7cea0-122">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="7cea0-123">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="7cea0-123">Minimum supported server</span></span><br/> | <span data-ttu-id="7cea0-124">都不支援</span><span class="sxs-lookup"><span data-stu-id="7cea0-124">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="7cea0-125">標頭</span><span class="sxs-lookup"><span data-stu-id="7cea0-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="7cea0-126"><dt>IACom (也需要 IACom \_ c) </dt></span><span class="sxs-lookup"><span data-stu-id="7cea0-126"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7cea0-127">另請參閱</span><span class="sxs-lookup"><span data-stu-id="7cea0-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7cea0-128">**ICoNtextLink**</span><span class="sxs-lookup"><span data-stu-id="7cea0-128">**IContextLink**</span></span>](icontextlink.md)
</dt> <dt>

[<span data-ttu-id="7cea0-129">**ICoNtextNode::AddCoNtextLink**</span><span class="sxs-lookup"><span data-stu-id="7cea0-129">**IContextNode::AddContextLink**</span></span>](icontextnode-addcontextlink.md)
</dt> </dl>

 

 




