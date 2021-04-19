---
description: 指定 ICoNtextNode 物件上可能發生的確認類型。
ms.assetid: 5c906548-dbf5-4448-b248-070bd43b054e
title: 'ConfirmationType 列舉 (IACom) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ConfirmationType
api_type:
- HeaderDef
api_location:
- IACom.h
ms.openlocfilehash: 2c43971c6ccf44513c11e46d4bc5db86d973d7f2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106972162"
---
# <a name="confirmationtype-enumeration"></a><span data-ttu-id="452ba-103">ConfirmationType 列舉</span><span class="sxs-lookup"><span data-stu-id="452ba-103">ConfirmationType enumeration</span></span>

<span data-ttu-id="452ba-104">指定 [**ICoNtextNode**](icontextnode.md) 物件上可能發生的確認類型。</span><span class="sxs-lookup"><span data-stu-id="452ba-104">Specifies the type of confirmation that can occur on an [**IContextNode**](icontextnode.md) object.</span></span>

## <a name="syntax"></a><span data-ttu-id="452ba-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="452ba-105">Syntax</span></span>


```C++
typedef enum ConfirmationType { 
  ConfirmationType_None                   = 0,
  ConfirmationType_NodeTypeAndProperties  = 1,
  ConfirmationType_TopBoundary            = 4
} ConfirmationType;
```



## <a name="constants"></a><span data-ttu-id="452ba-106">常數</span><span class="sxs-lookup"><span data-stu-id="452ba-106">Constants</span></span>

<dl> <dt>

<span data-ttu-id="452ba-107"><span id="ConfirmationType_None"></span><span id="confirmationtype_none"></span><span id="CONFIRMATIONTYPE_NONE"></span>**ConfirmationType \_ 無**</span><span class="sxs-lookup"><span data-stu-id="452ba-107"><span id="ConfirmationType_None"></span><span id="confirmationtype_none"></span><span id="CONFIRMATIONTYPE_NONE"></span>**ConfirmationType\_None**</span></span>
</dt> <dd>

<span data-ttu-id="452ba-108">未套用任何確認。</span><span class="sxs-lookup"><span data-stu-id="452ba-108">No confirmation is applied.</span></span> <span data-ttu-id="452ba-109">[**IInkAnalyzer**](iinkanalyzer.md)可以視需要隨時變更內容節點或任何其子系。</span><span class="sxs-lookup"><span data-stu-id="452ba-109">The [**IInkAnalyzer**](iinkanalyzer.md) is free to change a context node or any of its descendants as needed.</span></span>

</dd> <dt>

<span data-ttu-id="452ba-110"><span id="ConfirmationType_NodeTypeAndProperties"></span><span id="confirmationtype_nodetypeandproperties"></span><span id="CONFIRMATIONTYPE_NODETYPEANDPROPERTIES"></span>**ConfirmationType \_ NodeTypeAndProperties**</span><span class="sxs-lookup"><span data-stu-id="452ba-110"><span id="ConfirmationType_NodeTypeAndProperties"></span><span id="confirmationtype_nodetypeandproperties"></span><span id="CONFIRMATIONTYPE_NODETYPEANDPROPERTIES"></span>**ConfirmationType\_NodeTypeAndProperties**</span></span>
</dt> <dd>

<span data-ttu-id="452ba-111">[**IInkAnalyzer**](iinkanalyzer.md)無法變更指定之內容節點的類型或任何屬性。</span><span class="sxs-lookup"><span data-stu-id="452ba-111">The [**IInkAnalyzer**](iinkanalyzer.md) cannot change the type or any properties of the specified context node.</span></span>

</dd> <dt>

<span data-ttu-id="452ba-112"><span id="ConfirmationType_TopBoundary"></span><span id="confirmationtype_topboundary"></span><span id="CONFIRMATIONTYPE_TOPBOUNDARY"></span>**ConfirmationType \_ TopBoundary**</span><span class="sxs-lookup"><span data-stu-id="452ba-112"><span id="ConfirmationType_TopBoundary"></span><span id="confirmationtype_topboundary"></span><span id="CONFIRMATIONTYPE_TOPBOUNDARY"></span>**ConfirmationType\_TopBoundary**</span></span>
</dt> <dd>

<span data-ttu-id="452ba-113">[**IInkAnalyzer**](iinkanalyzer.md)將不會執行作業，包括新增筆墨或與其他 [**CoNtextNodes**](icontextnodes.md)合併，而導致 TopBoundary 移至目前的上方界限之外。</span><span class="sxs-lookup"><span data-stu-id="452ba-113">The [**IInkAnalyzer**](iinkanalyzer.md) will not perform operations, including adding ink or merging with other [**ContextNodes**](icontextnodes.md), that cause the TopBoundary to move beyond the current top boundary.</span></span> <span data-ttu-id="452ba-114">例如：</span><span class="sxs-lookup"><span data-stu-id="452ba-114">For example:</span></span>

-   <span data-ttu-id="452ba-115">應用程式會分析一組筆墨，並識別出 ParagraphNode。</span><span class="sxs-lookup"><span data-stu-id="452ba-115">An application analyzes a set of Ink, and a ParagraphNode is identified.</span></span>
-   <span data-ttu-id="452ba-116">應用程式會確認此段落的 TopBoundary。</span><span class="sxs-lookup"><span data-stu-id="452ba-116">The application confirms the TopBoundary of this paragraph.</span></span>
-   <span data-ttu-id="452ba-117">應用程式的使用者會將新筆墨寫入目前的段落上方。</span><span class="sxs-lookup"><span data-stu-id="452ba-117">The user of the application writes new ink above the current paragraph.</span></span> <span data-ttu-id="452ba-118">再次呼叫 [分析] 時，新的筆墨將不會併入確認的段落節點。</span><span class="sxs-lookup"><span data-stu-id="452ba-118">When analyze is called again, the new ink will not be incorporated into the Confirmed paragraph node.</span></span>
-   <span data-ttu-id="452ba-119">因為只確認最上層界限，所以 CoNtextNode 可以繼續以其他方向成長。</span><span class="sxs-lookup"><span data-stu-id="452ba-119">Since only the top boundary is confirmed, the ContextNode can continue to grow in other directions.</span></span> <span data-ttu-id="452ba-120">刪除筆劃可能會導致頂端界限下移。</span><span class="sxs-lookup"><span data-stu-id="452ba-120">Deleting strokes can cause the top boundary to move down.</span></span> <span data-ttu-id="452ba-121">轉譯 CoNtextNode 可能會導致位置變更，但不允許將其他筆墨合併到新的位置。</span><span class="sxs-lookup"><span data-stu-id="452ba-121">Translating the ContextNode can cause the location to change, but will not allow additional ink to be merged in the new location.</span></span>

<span data-ttu-id="452ba-122">此 ConfirmationType 僅適用于段落節點。</span><span class="sxs-lookup"><span data-stu-id="452ba-122">This ConfirmationType is only applicable to paragraph nodes.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="452ba-123">備註</span><span class="sxs-lookup"><span data-stu-id="452ba-123">Remarks</span></span>

<span data-ttu-id="452ba-124">您只能將 **NodeTypeAndProperties** 值用於筆墨單字和筆墨繪圖節點 (請參閱 [**ICoNtextNode：： GetType**](icontextnode-gettype.md)) 。</span><span class="sxs-lookup"><span data-stu-id="452ba-124">You can use the **NodeTypeAndProperties** value only for ink word and ink drawing nodes (see [**IContextNode::GetType**](icontextnode-gettype.md)).</span></span> <span data-ttu-id="452ba-125">否則，會從 [**ICoNtextNode：： Confirm**](icontextnode-confirm.md)傳回 **E \_ INVALIDARG** 。</span><span class="sxs-lookup"><span data-stu-id="452ba-125">Otherwise, an **E\_INVALIDARG** is returned from [**IContextNode::Confirm**](icontextnode-confirm.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="452ba-126">規格需求</span><span class="sxs-lookup"><span data-stu-id="452ba-126">Requirements</span></span>



| <span data-ttu-id="452ba-127">需求</span><span class="sxs-lookup"><span data-stu-id="452ba-127">Requirement</span></span> | <span data-ttu-id="452ba-128">值</span><span class="sxs-lookup"><span data-stu-id="452ba-128">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="452ba-129">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="452ba-129">Minimum supported client</span></span><br/> | <span data-ttu-id="452ba-130">僅限 Windows XP Tablet PC Edition \[ 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="452ba-130">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="452ba-131">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="452ba-131">Minimum supported server</span></span><br/> | <span data-ttu-id="452ba-132">都不支援</span><span class="sxs-lookup"><span data-stu-id="452ba-132">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="452ba-133">標頭</span><span class="sxs-lookup"><span data-stu-id="452ba-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="452ba-134"><dt>IACom (也需要 IACom \_ c) </dt></span><span class="sxs-lookup"><span data-stu-id="452ba-134"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="452ba-135">另請參閱</span><span class="sxs-lookup"><span data-stu-id="452ba-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="452ba-136">**ICoNtextNode：： Confirm**</span><span class="sxs-lookup"><span data-stu-id="452ba-136">**IContextNode::Confirm**</span></span>](icontextnode-confirm.md)
</dt> <dt>

[<span data-ttu-id="452ba-137">**ICoNtextNode::IsConfirmed**</span><span class="sxs-lookup"><span data-stu-id="452ba-137">**IContextNode::IsConfirmed**</span></span>](icontextnode-isconfirmed.md)
</dt> </dl>

 

 




