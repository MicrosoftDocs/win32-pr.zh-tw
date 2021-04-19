---
description: 包含物件的集合，這些物件會執行 ICoNtextNode 介面，且為筆跡分析作業的結果。
ms.assetid: 2c4e9d84-243a-40e4-b3f9-5c4cafc5aac4
title: 'ICoNtextNodes 介面 (IACom .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IContextNodes
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 306abcd32dcb0ee55978a6b95ee9f8a2c22cd19c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106972052"
---
# <a name="icontextnodes-interface"></a><span data-ttu-id="b32f8-103">ICoNtextNodes 介面</span><span class="sxs-lookup"><span data-stu-id="b32f8-103">IContextNodes interface</span></span>

<span data-ttu-id="b32f8-104">包含物件的集合，這些物件會執行 [**ICoNtextNode**](icontextnode.md) 介面，且為筆跡分析作業的結果。</span><span class="sxs-lookup"><span data-stu-id="b32f8-104">Contains a collection of objects that implement the [**IContextNode**](icontextnode.md) interface and that are the result of an ink analysis operation.</span></span>

## <a name="members"></a><span data-ttu-id="b32f8-105">成員</span><span class="sxs-lookup"><span data-stu-id="b32f8-105">Members</span></span>

<span data-ttu-id="b32f8-106">**ICoNtextNodes** 介面繼承自 [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown)介面。</span><span class="sxs-lookup"><span data-stu-id="b32f8-106">The **IContextNodes** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="b32f8-107">**ICoNtextNodes** 也有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="b32f8-107">**IContextNodes** also has these types of members:</span></span>

-   [<span data-ttu-id="b32f8-108">方法</span><span class="sxs-lookup"><span data-stu-id="b32f8-108">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="b32f8-109">方法</span><span class="sxs-lookup"><span data-stu-id="b32f8-109">Methods</span></span>

<span data-ttu-id="b32f8-110">**ICoNtextNodes** 介面具有這些方法。</span><span class="sxs-lookup"><span data-stu-id="b32f8-110">The **IContextNodes** interface has these methods.</span></span>



| <span data-ttu-id="b32f8-111">方法</span><span class="sxs-lookup"><span data-stu-id="b32f8-111">Method</span></span>                                                       | <span data-ttu-id="b32f8-112">描述</span><span class="sxs-lookup"><span data-stu-id="b32f8-112">Description</span></span>                                                                                                          |
|:-------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="b32f8-113">**AddCoNtextNode**</span><span class="sxs-lookup"><span data-stu-id="b32f8-113">**AddContextNode**</span></span>](icontextnodes-addcontextnode.md)       | <span data-ttu-id="b32f8-114">將 [**ICoNtextNode**](icontextnode.md) 物件加入至此集合。</span><span class="sxs-lookup"><span data-stu-id="b32f8-114">Adds an [**IContextNode**](icontextnode.md) object to this collection.</span></span> <br/>                                  |
| [<span data-ttu-id="b32f8-115">**GetCoNtextNode**</span><span class="sxs-lookup"><span data-stu-id="b32f8-115">**GetContextNode**</span></span>](icontextnodes-getcontextnode.md)       | <span data-ttu-id="b32f8-116">在此集合中的指定索引處，抓取 [**ICoNtextNode**](icontextnode.md) 物件。</span><span class="sxs-lookup"><span data-stu-id="b32f8-116">Retrieves the [**IContextNode**](icontextnode.md) object at the specified index within this collection.</span></span> <br/> |
| [<span data-ttu-id="b32f8-117">**GetCount**</span><span class="sxs-lookup"><span data-stu-id="b32f8-117">**GetCount**</span></span>](icontextnodes-getcount.md)                   | <span data-ttu-id="b32f8-118">抓取此集合中包含的 [**ICoNtextNode**](icontextnode.md) 物件數目。</span><span class="sxs-lookup"><span data-stu-id="b32f8-118">Retrieves the number of [**IContextNode**](icontextnode.md) objects contained in this collection.</span></span> <br/>       |
| [<span data-ttu-id="b32f8-119">**RemoveCoNtextNode**</span><span class="sxs-lookup"><span data-stu-id="b32f8-119">**RemoveContextNode**</span></span>](icontextnodes-removecontextnode.md) | <span data-ttu-id="b32f8-120">從此集合移除 [**ICoNtextNode**](icontextnode.md) 物件。</span><span class="sxs-lookup"><span data-stu-id="b32f8-120">Removes an [**IContextNode**](icontextnode.md) object from this collection.</span></span> <br/>                             |



 

## <a name="requirements"></a><span data-ttu-id="b32f8-121">規格需求</span><span class="sxs-lookup"><span data-stu-id="b32f8-121">Requirements</span></span>



| <span data-ttu-id="b32f8-122">需求</span><span class="sxs-lookup"><span data-stu-id="b32f8-122">Requirement</span></span> | <span data-ttu-id="b32f8-123">值</span><span class="sxs-lookup"><span data-stu-id="b32f8-123">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b32f8-124">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="b32f8-124">Minimum supported client</span></span><br/> | <span data-ttu-id="b32f8-125">僅限 Windows XP Tablet PC Edition \[ 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="b32f8-125">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="b32f8-126">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="b32f8-126">Minimum supported server</span></span><br/> | <span data-ttu-id="b32f8-127">都不支援</span><span class="sxs-lookup"><span data-stu-id="b32f8-127">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="b32f8-128">標頭</span><span class="sxs-lookup"><span data-stu-id="b32f8-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="b32f8-129"><dt>IACom (也需要 IACom \_ c) </dt></span><span class="sxs-lookup"><span data-stu-id="b32f8-129"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="b32f8-130">DLL</span><span class="sxs-lookup"><span data-stu-id="b32f8-130">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b32f8-131"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b32f8-131"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="b32f8-132">另請參閱</span><span class="sxs-lookup"><span data-stu-id="b32f8-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b32f8-133">**ICoNtextNode**</span><span class="sxs-lookup"><span data-stu-id="b32f8-133">**IContextNode**</span></span>](icontextnode.md)
</dt> <dt>

[<span data-ttu-id="b32f8-134">筆跡分析參考</span><span class="sxs-lookup"><span data-stu-id="b32f8-134">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

