---
description: 更新此 ICoNtextNode 的區域。
ms.assetid: e7001411-17e4-4f33-af04-dd3220275895
title: 'ICoNtextNode：： SetLocation 方法 (IACom .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IContextNode.SetLocation
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 20daefeab7a9e36d5e968d5d14bfa5110d733487
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106971415"
---
# <a name="icontextnodesetlocation-method"></a><span data-ttu-id="1b866-103">ICoNtextNode：： SetLocation 方法</span><span class="sxs-lookup"><span data-stu-id="1b866-103">IContextNode::SetLocation method</span></span>

<span data-ttu-id="1b866-104">更新此 [**ICoNtextNode**](icontextnode.md)的區域。</span><span class="sxs-lookup"><span data-stu-id="1b866-104">Updates the area of this [**IContextNode**](icontextnode.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="1b866-105">語法</span><span class="sxs-lookup"><span data-stu-id="1b866-105">Syntax</span></span>


```C++
HRESULT SetLocation(
  [in] IAnalysisRegion *pIAnalysisRegion
);
```



## <a name="parameters"></a><span data-ttu-id="1b866-106">參數</span><span class="sxs-lookup"><span data-stu-id="1b866-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1b866-107">*pIAnalysisRegion* \[在\]</span><span class="sxs-lookup"><span data-stu-id="1b866-107">*pIAnalysisRegion* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1b866-108">[**IAnalysisRegion**](ianalysisregion.md) ，描述要設定 [**ICoNtextNode**](icontextnode.md)物件位置的區域。</span><span class="sxs-lookup"><span data-stu-id="1b866-108">The [**IAnalysisRegion**](ianalysisregion.md) describing the area to which to set the [**IContextNode**](icontextnode.md) object's location.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1b866-109">傳回值</span><span class="sxs-lookup"><span data-stu-id="1b866-109">Return value</span></span>

<span data-ttu-id="1b866-110">如需傳回值的描述，請參閱 [類別和介面-筆跡分析](classes-and-interfaces---ink-analysis.md)。</span><span class="sxs-lookup"><span data-stu-id="1b866-110">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="1b866-111">備註</span><span class="sxs-lookup"><span data-stu-id="1b866-111">Remarks</span></span>

<span data-ttu-id="1b866-112">使用這個方法來更新內容節點的位置 (參閱 [**ICoNtextNode：： GetLocation**](icontextnode-getlocation.md)) 。</span><span class="sxs-lookup"><span data-stu-id="1b866-112">Use this method to update the context node's location (see [**IContextNode::GetLocation**](icontextnode-getlocation.md)).</span></span>

## <a name="requirements"></a><span data-ttu-id="1b866-113">規格需求</span><span class="sxs-lookup"><span data-stu-id="1b866-113">Requirements</span></span>



| <span data-ttu-id="1b866-114">需求</span><span class="sxs-lookup"><span data-stu-id="1b866-114">Requirement</span></span> | <span data-ttu-id="1b866-115">值</span><span class="sxs-lookup"><span data-stu-id="1b866-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1b866-116">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="1b866-116">Minimum supported client</span></span><br/> | <span data-ttu-id="1b866-117">僅限 Windows XP Tablet PC Edition \[ 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="1b866-117">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="1b866-118">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="1b866-118">Minimum supported server</span></span><br/> | <span data-ttu-id="1b866-119">都不支援</span><span class="sxs-lookup"><span data-stu-id="1b866-119">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="1b866-120">標頭</span><span class="sxs-lookup"><span data-stu-id="1b866-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="1b866-121"><dt>IACom (也需要 IACom \_ c) </dt></span><span class="sxs-lookup"><span data-stu-id="1b866-121"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="1b866-122">DLL</span><span class="sxs-lookup"><span data-stu-id="1b866-122">DLL</span></span><br/>                      | <dl> <span data-ttu-id="1b866-123"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="1b866-123"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="1b866-124">另請參閱</span><span class="sxs-lookup"><span data-stu-id="1b866-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1b866-125">**ICoNtextNode**</span><span class="sxs-lookup"><span data-stu-id="1b866-125">**IContextNode**</span></span>](icontextnode.md)
</dt> <dt>

[<span data-ttu-id="1b866-126">**IAnalysisRegion**</span><span class="sxs-lookup"><span data-stu-id="1b866-126">**IAnalysisRegion**</span></span>](ianalysisregion.md)
</dt> <dt>

[<span data-ttu-id="1b866-127">**ICoNtextNode::GetLocation**</span><span class="sxs-lookup"><span data-stu-id="1b866-127">**IContextNode::GetLocation**</span></span>](icontextnode-getlocation.md)
</dt> <dt>

[<span data-ttu-id="1b866-128">**ICoNtextNode::GetPartiallyPopulated**</span><span class="sxs-lookup"><span data-stu-id="1b866-128">**IContextNode::GetPartiallyPopulated**</span></span>](icontextnode-getpartiallypopulated.md)
</dt> <dt>

[<span data-ttu-id="1b866-129">筆跡分析參考</span><span class="sxs-lookup"><span data-stu-id="1b866-129">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

 




