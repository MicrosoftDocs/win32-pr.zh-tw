---
description: 抓取 ICoNtextNode 物件，此物件為這個 ICoNtextLink 的目的地。
ms.assetid: 7e185e69-821b-409b-bc58-d89a4aefeb23
title: 'ICoNtextLink：： GetDestinationNode 方法 (IACom .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IContextLink.GetDestinationNode
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 86d34bfcca39f7df9d9010e8dae32747ca8f1d27
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104318467"
---
# <a name="icontextlinkgetdestinationnode-method"></a><span data-ttu-id="21acd-103">ICoNtextLink：： GetDestinationNode 方法</span><span class="sxs-lookup"><span data-stu-id="21acd-103">IContextLink::GetDestinationNode method</span></span>

<span data-ttu-id="21acd-104">抓取 [**ICoNtextNode**](icontextnode.md) 物件，此物件為這個 [**ICoNtextLink**](icontextlink.md)的目的地。</span><span class="sxs-lookup"><span data-stu-id="21acd-104">Retrieves the [**IContextNode**](icontextnode.md) object that is the destination for this [**IContextLink**](icontextlink.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="21acd-105">語法</span><span class="sxs-lookup"><span data-stu-id="21acd-105">Syntax</span></span>


```C++
HRESULT GetDestinationNode(
  [out] IContextNode **ppDstContextNodeId
);
```



## <a name="parameters"></a><span data-ttu-id="21acd-106">參數</span><span class="sxs-lookup"><span data-stu-id="21acd-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="21acd-107">*ppDstCoNtextNodeId* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="21acd-107">*ppDstContextNodeId* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="21acd-108">[**ICoNtextNode**](icontextnode.md)物件的指標，該物件是這個 [**ICoNtextLink**](icontextlink.md)的目的地。</span><span class="sxs-lookup"><span data-stu-id="21acd-108">A pointer to the [**IContextNode**](icontextnode.md) object that is the destination for this [**IContextLink**](icontextlink.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="21acd-109">傳回值</span><span class="sxs-lookup"><span data-stu-id="21acd-109">Return value</span></span>

<span data-ttu-id="21acd-110">如需傳回值的描述，請參閱 [類別和介面-筆跡分析](classes-and-interfaces---ink-analysis.md)。</span><span class="sxs-lookup"><span data-stu-id="21acd-110">For a description of return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="21acd-111">備註</span><span class="sxs-lookup"><span data-stu-id="21acd-111">Remarks</span></span>

> [!Caution]  
> <span data-ttu-id="21acd-112">若要避免記憶體流失， [](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) \* 當您不再需要使用目的地節點時，請在 *ppDstCoNtextNodeId* 上呼叫 IUnknown：： Release。</span><span class="sxs-lookup"><span data-stu-id="21acd-112">To avoid a memory leak, call [**IUnknown::Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) on \**ppDstContextNodeId* when you no longer need to use the destination node.</span></span>

 

<span data-ttu-id="21acd-113">如果 [**ICoNtextLink**](icontextlink.md) 物件是在包含撰寫的節點和包含繪圖的節點之間進行連結，則目的地節點通常是包含寫入的節點。</span><span class="sxs-lookup"><span data-stu-id="21acd-113">If the [**IContextLink**](icontextlink.md) object links between a node that contains writing and a node that contains drawing, the destination node is generally the node that contains writing.</span></span>

<span data-ttu-id="21acd-114">如果 ICoNtextLink 物件的連結 (類型是 [](icontextlink.md) ，請參閱 [**ICoNtextLink：： GetCoNtextLinkDirection**](icontextlink-getcontextlinkdirection.md)) ，目的節點是包含的 [**ICoNtextNode**](icontextnode.md)物件。</span><span class="sxs-lookup"><span data-stu-id="21acd-114">If the [**IContextLink**](icontextlink.md) object has a link type of Encloses (see [**IContextLink::GetContextLinkDirection**](icontextlink-getcontextlinkdirection.md)), the destination node is the [**IContextNode**](icontextnode.md) object that is enclosed.</span></span>

## <a name="requirements"></a><span data-ttu-id="21acd-115">規格需求</span><span class="sxs-lookup"><span data-stu-id="21acd-115">Requirements</span></span>



| <span data-ttu-id="21acd-116">需求</span><span class="sxs-lookup"><span data-stu-id="21acd-116">Requirement</span></span> | <span data-ttu-id="21acd-117">值</span><span class="sxs-lookup"><span data-stu-id="21acd-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="21acd-118">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="21acd-118">Minimum supported client</span></span><br/> | <span data-ttu-id="21acd-119">僅限 Windows XP Tablet PC Edition \[ 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="21acd-119">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="21acd-120">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="21acd-120">Minimum supported server</span></span><br/> | <span data-ttu-id="21acd-121">都不支援</span><span class="sxs-lookup"><span data-stu-id="21acd-121">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="21acd-122">標頭</span><span class="sxs-lookup"><span data-stu-id="21acd-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="21acd-123"><dt>IACom (也需要 IACom \_ c) </dt></span><span class="sxs-lookup"><span data-stu-id="21acd-123"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="21acd-124">DLL</span><span class="sxs-lookup"><span data-stu-id="21acd-124">DLL</span></span><br/>                      | <dl> <span data-ttu-id="21acd-125"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="21acd-125"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="21acd-126">另請參閱</span><span class="sxs-lookup"><span data-stu-id="21acd-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="21acd-127">**ICoNtextLink**</span><span class="sxs-lookup"><span data-stu-id="21acd-127">**IContextLink**</span></span>](icontextlink.md)
</dt> <dt>

[<span data-ttu-id="21acd-128">**ICoNtextLink::GetSourceNode**</span><span class="sxs-lookup"><span data-stu-id="21acd-128">**IContextLink::GetSourceNode**</span></span>](icontextlink-getsourcenode.md)
</dt> <dt>

[<span data-ttu-id="21acd-129">**CoNtextLinkDirection**</span><span class="sxs-lookup"><span data-stu-id="21acd-129">**ContextLinkDirection**</span></span>](contextlinkdirection.md)
</dt> <dt>

[<span data-ttu-id="21acd-130">筆跡分析參考</span><span class="sxs-lookup"><span data-stu-id="21acd-130">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

