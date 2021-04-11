---
description: 抓取 ICoNtextNode 物件，此物件為這個 ICoNtextLink 的來源。
ms.assetid: 2f55ae9c-9f63-4d49-9bf0-9e169b819e79
title: 'ICoNtextLink：： GetSourceNode 方法 (IACom .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IContextLink.GetSourceNode
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: eddab21740bf30c67e247cec89723bc47cd9dca1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104191416"
---
# <a name="icontextlinkgetsourcenode-method"></a><span data-ttu-id="4ca85-103">ICoNtextLink：： GetSourceNode 方法</span><span class="sxs-lookup"><span data-stu-id="4ca85-103">IContextLink::GetSourceNode method</span></span>

<span data-ttu-id="4ca85-104">抓取 [**ICoNtextNode**](icontextnode.md) 物件，此物件為這個 [**ICoNtextLink**](icontextlink.md)的來源。</span><span class="sxs-lookup"><span data-stu-id="4ca85-104">Retrieves the [**IContextNode**](icontextnode.md) object that is the source for this [**IContextLink**](icontextlink.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="4ca85-105">語法</span><span class="sxs-lookup"><span data-stu-id="4ca85-105">Syntax</span></span>


```C++
HRESULT GetSourceNode(
  [out] IContextNode **ppSrcContextNodeId
);
```



## <a name="parameters"></a><span data-ttu-id="4ca85-106">參數</span><span class="sxs-lookup"><span data-stu-id="4ca85-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4ca85-107">*ppSrcCoNtextNodeId* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="4ca85-107">*ppSrcContextNodeId* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="4ca85-108">[**ICoNtextNode**](icontextnode.md)物件的指標，該物件為此 [**ICoNtextLink**](icontextlink.md)的來源。</span><span class="sxs-lookup"><span data-stu-id="4ca85-108">A pointer to the [**IContextNode**](icontextnode.md) object that is the source for this [**IContextLink**](icontextlink.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4ca85-109">傳回值</span><span class="sxs-lookup"><span data-stu-id="4ca85-109">Return value</span></span>

<span data-ttu-id="4ca85-110">如需傳回值的描述，請參閱 [類別和介面-筆跡分析](classes-and-interfaces---ink-analysis.md)。</span><span class="sxs-lookup"><span data-stu-id="4ca85-110">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="4ca85-111">備註</span><span class="sxs-lookup"><span data-stu-id="4ca85-111">Remarks</span></span>

> [!Caution]  
> <span data-ttu-id="4ca85-112">若要避免記憶體流失， [](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) \* 當您不再需要使用來源節點時，請在 *ppSrcCoNtextNodeId* 上呼叫 IUnknown：： Release。</span><span class="sxs-lookup"><span data-stu-id="4ca85-112">To avoid a memory leak, call [**IUnknown::Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) on \**ppSrcContextNodeId* when you no longer need to use the source node.</span></span>

 

<span data-ttu-id="4ca85-113">如果 [**ICoNtextLink**](icontextlink.md) 物件是在包含撰寫的節點和包含繪圖的節點之間進行連結，則來源節點通常是包含繪圖的節點。</span><span class="sxs-lookup"><span data-stu-id="4ca85-113">If the [**IContextLink**](icontextlink.md) object links between a node that contains writing and a node that contains drawing, the source node is generally the node that contains drawing.</span></span>

<span data-ttu-id="4ca85-114">如果 ICoNtextLink 物件的連結 (類型是 [](icontextlink.md) ，請參閱 [**ICoNtextLink：： GetCoNtextLinkDirection**](icontextlink-getcontextlinkdirection.md)) ，來源節點是包含目的地節點的節點。</span><span class="sxs-lookup"><span data-stu-id="4ca85-114">If the [**IContextLink**](icontextlink.md) object has a link type of Encloses (see [**IContextLink::GetContextLinkDirection**](icontextlink-getcontextlinkdirection.md)), the source node is the node that encloses the destination node.</span></span>

## <a name="requirements"></a><span data-ttu-id="4ca85-115">規格需求</span><span class="sxs-lookup"><span data-stu-id="4ca85-115">Requirements</span></span>



| <span data-ttu-id="4ca85-116">需求</span><span class="sxs-lookup"><span data-stu-id="4ca85-116">Requirement</span></span> | <span data-ttu-id="4ca85-117">值</span><span class="sxs-lookup"><span data-stu-id="4ca85-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4ca85-118">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="4ca85-118">Minimum supported client</span></span><br/> | <span data-ttu-id="4ca85-119">僅限 Windows XP Tablet PC Edition \[ 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="4ca85-119">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="4ca85-120">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="4ca85-120">Minimum supported server</span></span><br/> | <span data-ttu-id="4ca85-121">都不支援</span><span class="sxs-lookup"><span data-stu-id="4ca85-121">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="4ca85-122">標頭</span><span class="sxs-lookup"><span data-stu-id="4ca85-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="4ca85-123"><dt>IACom (也需要 IACom \_ c) </dt></span><span class="sxs-lookup"><span data-stu-id="4ca85-123"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="4ca85-124">DLL</span><span class="sxs-lookup"><span data-stu-id="4ca85-124">DLL</span></span><br/>                      | <dl> <span data-ttu-id="4ca85-125"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="4ca85-125"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="4ca85-126">另請參閱</span><span class="sxs-lookup"><span data-stu-id="4ca85-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4ca85-127">**ICoNtextLink**</span><span class="sxs-lookup"><span data-stu-id="4ca85-127">**IContextLink**</span></span>](icontextlink.md)
</dt> <dt>

[<span data-ttu-id="4ca85-128">**ICoNtextLink::GetDestinationNode**</span><span class="sxs-lookup"><span data-stu-id="4ca85-128">**IContextLink::GetDestinationNode**</span></span>](icontextlink-getdestinationnode.md)
</dt> <dt>

[<span data-ttu-id="4ca85-129">**CoNtextLinkDirection**</span><span class="sxs-lookup"><span data-stu-id="4ca85-129">**ContextLinkDirection**</span></span>](contextlinkdirection.md)
</dt> <dt>

[<span data-ttu-id="4ca85-130">筆跡分析參考</span><span class="sxs-lookup"><span data-stu-id="4ca85-130">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

