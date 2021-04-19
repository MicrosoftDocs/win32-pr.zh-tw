---
description: 表示兩個 ICoNtextNode 物件之間的關聯性。
ms.assetid: ee81d9d7-eba9-4b11-84d0-5a6ca0df7d92
title: 'ICoNtextLink 介面 (IACom .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IContextLink
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: df1e0d8717ba29532486277aced19f17adb1d79c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106972645"
---
# <a name="icontextlink-interface"></a><span data-ttu-id="36d9c-103">ICoNtextLink 介面</span><span class="sxs-lookup"><span data-stu-id="36d9c-103">IContextLink interface</span></span>

<span data-ttu-id="36d9c-104">表示兩個 [**ICoNtextNode**](icontextnode.md) 物件之間的關聯性。</span><span class="sxs-lookup"><span data-stu-id="36d9c-104">Represents a relationship between two [**IContextNode**](icontextnode.md) objects.</span></span>

## <a name="members"></a><span data-ttu-id="36d9c-105">成員</span><span class="sxs-lookup"><span data-stu-id="36d9c-105">Members</span></span>

<span data-ttu-id="36d9c-106">**ICoNtextLink** 介面繼承自 [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown)介面。</span><span class="sxs-lookup"><span data-stu-id="36d9c-106">The **IContextLink** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="36d9c-107">**ICoNtextLink** 也有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="36d9c-107">**IContextLink** also has these types of members:</span></span>

-   [<span data-ttu-id="36d9c-108">方法</span><span class="sxs-lookup"><span data-stu-id="36d9c-108">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="36d9c-109">方法</span><span class="sxs-lookup"><span data-stu-id="36d9c-109">Methods</span></span>

<span data-ttu-id="36d9c-110">**ICoNtextLink** 介面具有這些方法。</span><span class="sxs-lookup"><span data-stu-id="36d9c-110">The **IContextLink** interface has these methods.</span></span>



| <span data-ttu-id="36d9c-111">方法</span><span class="sxs-lookup"><span data-stu-id="36d9c-111">Method</span></span>                                                                  | <span data-ttu-id="36d9c-112">描述</span><span class="sxs-lookup"><span data-stu-id="36d9c-112">Description</span></span>                                                                                                             |
|:------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="36d9c-113">**GetCoNtextLinkDirection**</span><span class="sxs-lookup"><span data-stu-id="36d9c-113">**GetContextLinkDirection**</span></span>](icontextlink-getcontextlinkdirection.md) | <span data-ttu-id="36d9c-114">抓取這個 **ICoNtextLink** 所代表的關聯性類型。</span><span class="sxs-lookup"><span data-stu-id="36d9c-114">Retrieves the type of relationship this **IContextLink** represents.</span></span><br/>                                         |
| [<span data-ttu-id="36d9c-115">**GetDestinationNode**</span><span class="sxs-lookup"><span data-stu-id="36d9c-115">**GetDestinationNode**</span></span>](icontextlink-getdestinationnode.md)           | <span data-ttu-id="36d9c-116">抓取 [**ICoNtextNode**](icontextnode.md) 物件，此物件為這個 **ICoNtextLink** 的目的地。</span><span class="sxs-lookup"><span data-stu-id="36d9c-116">Retrieves the [**IContextNode**](icontextnode.md) object that is the destination for this **IContextLink**.</span></span><br/> |
| [<span data-ttu-id="36d9c-117">**GetSourceNode**</span><span class="sxs-lookup"><span data-stu-id="36d9c-117">**GetSourceNode**</span></span>](icontextlink-getsourcenode.md)                     | <span data-ttu-id="36d9c-118">抓取 [**ICoNtextNode**](icontextnode.md) 物件，此物件為這個 **ICoNtextLink** 的來源。</span><span class="sxs-lookup"><span data-stu-id="36d9c-118">Retrieves the [**IContextNode**](icontextnode.md) object that is the source for this **IContextLink**.</span></span><br/>      |



 

## <a name="remarks"></a><span data-ttu-id="36d9c-119">備註</span><span class="sxs-lookup"><span data-stu-id="36d9c-119">Remarks</span></span>

<span data-ttu-id="36d9c-120">以下是 **ICoNtextLink** 物件所代表的關聯性範例：</span><span class="sxs-lookup"><span data-stu-id="36d9c-120">The following is an example of a relationship represented by an **IContextLink** object:</span></span>

-   <span data-ttu-id="36d9c-121">在筆跡分析中使用 AnalysisHint 節點時，筆跡分析作業會在 [分析提示] 節點和包含在提示區域內寫入的節點之間，建立類型為 AnalysisHint 的 **ICoNtextLink** 物件。</span><span class="sxs-lookup"><span data-stu-id="36d9c-121">When an AnalysisHint node is used in ink analysis, the ink analysis operation creates an **IContextLink** object of type AnalysisHint between the analysis hint node and the node that contains writing within the area of the hint.</span></span> <span data-ttu-id="36d9c-122">來源節點是分析提示節點，而目的地節點則是包含寫入的節點。</span><span class="sxs-lookup"><span data-stu-id="36d9c-122">The source node is the analysis hint node and the destination node is the node that contains writing.</span></span>

## <a name="requirements"></a><span data-ttu-id="36d9c-123">規格需求</span><span class="sxs-lookup"><span data-stu-id="36d9c-123">Requirements</span></span>



| <span data-ttu-id="36d9c-124">需求</span><span class="sxs-lookup"><span data-stu-id="36d9c-124">Requirement</span></span> | <span data-ttu-id="36d9c-125">值</span><span class="sxs-lookup"><span data-stu-id="36d9c-125">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="36d9c-126">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="36d9c-126">Minimum supported client</span></span><br/> | <span data-ttu-id="36d9c-127">僅限 Windows XP Tablet PC Edition \[ 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="36d9c-127">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="36d9c-128">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="36d9c-128">Minimum supported server</span></span><br/> | <span data-ttu-id="36d9c-129">都不支援</span><span class="sxs-lookup"><span data-stu-id="36d9c-129">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="36d9c-130">標頭</span><span class="sxs-lookup"><span data-stu-id="36d9c-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="36d9c-131"><dt>IACom (也需要 IACom \_ c) </dt></span><span class="sxs-lookup"><span data-stu-id="36d9c-131"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="36d9c-132">DLL</span><span class="sxs-lookup"><span data-stu-id="36d9c-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="36d9c-133"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="36d9c-133"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="36d9c-134">另請參閱</span><span class="sxs-lookup"><span data-stu-id="36d9c-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="36d9c-135">**ICoNtextNode::GetCoNtextLinks**</span><span class="sxs-lookup"><span data-stu-id="36d9c-135">**IContextNode::GetContextLinks**</span></span>](icontextnode-getcontextlinks.md)
</dt> <dt>

[<span data-ttu-id="36d9c-136">**ICoNtextLinks**</span><span class="sxs-lookup"><span data-stu-id="36d9c-136">**IContextLinks**</span></span>](icontextlinks.md)
</dt> <dt>

[<span data-ttu-id="36d9c-137">**CoNtextLinkDirection**</span><span class="sxs-lookup"><span data-stu-id="36d9c-137">**ContextLinkDirection**</span></span>](contextlinkdirection.md)
</dt> <dt>

[<span data-ttu-id="36d9c-138">內容節點類型</span><span class="sxs-lookup"><span data-stu-id="36d9c-138">Context Node Types</span></span>](context-node-types.md)
</dt> </dl>

 

