---
description: 抓取值，這個值會指出 ICoNtextNode 物件是否已部分擴展或完整填入。
ms.assetid: 13ac3fb2-7baa-48d7-bf8e-f36b4031fbc4
title: 'ICoNtextNode：： GetPartiallyPopulated 方法 (IACom .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IContextNode.GetPartiallyPopulated
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 4b05cb8aae681a7302ae7da40a7412cf828fc159
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104113385"
---
# <a name="icontextnodegetpartiallypopulated-method"></a><span data-ttu-id="71f97-103">ICoNtextNode：： GetPartiallyPopulated 方法</span><span class="sxs-lookup"><span data-stu-id="71f97-103">IContextNode::GetPartiallyPopulated method</span></span>

<span data-ttu-id="71f97-104">抓取值，這個值會指出 [**ICoNtextNode**](icontextnode.md) 物件是否已部分擴展或完整填入。</span><span class="sxs-lookup"><span data-stu-id="71f97-104">Retrieves the value that indicates whether an [**IContextNode**](icontextnode.md) object is partially populated or fully populated.</span></span>

## <a name="syntax"></a><span data-ttu-id="71f97-105">語法</span><span class="sxs-lookup"><span data-stu-id="71f97-105">Syntax</span></span>


```C++
HRESULT GetPartiallyPopulated(
  [out] VARIANT_BOOL *pfPartiallyPopulated
);
```



## <a name="parameters"></a><span data-ttu-id="71f97-106">參數</span><span class="sxs-lookup"><span data-stu-id="71f97-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="71f97-107">*pfPartiallyPopulated* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="71f97-107">*pfPartiallyPopulated* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="71f97-108">**變異 \_** 如果這個 [**ICoNtextNode**](icontextnode.md)物件不包含完整資料，則為 TRUE;否則， **VARIANT \_ FALSE**。</span><span class="sxs-lookup"><span data-stu-id="71f97-108">**VARIANT\_TRUE** if this [**IContextNode**](icontextnode.md) object does not contain complete data; otherwise, **VARIANT\_FALSE**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="71f97-109">傳回值</span><span class="sxs-lookup"><span data-stu-id="71f97-109">Return value</span></span>

<span data-ttu-id="71f97-110">如需傳回值的描述，請參閱 [類別和介面-筆跡分析](classes-and-interfaces---ink-analysis.md)。</span><span class="sxs-lookup"><span data-stu-id="71f97-110">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="71f97-111">備註</span><span class="sxs-lookup"><span data-stu-id="71f97-111">Remarks</span></span>

<span data-ttu-id="71f97-112">當您的應用程式維護自己的資料結構（與 [**IInkAnalyzer**](iinkanalyzer.md)同步處理）時，請使用這個方法。</span><span class="sxs-lookup"><span data-stu-id="71f97-112">Use this method when your application maintains its own data structure, which is synchronized with that of the [**IInkAnalyzer**](iinkanalyzer.md).</span></span> <span data-ttu-id="71f97-113">如需詳細資訊，請參閱 [使用筆墨分析的資料 Proxy](data-proxy-with-ink-analysis.md)。</span><span class="sxs-lookup"><span data-stu-id="71f97-113">For more information, see [Data Proxy with Ink Analysis](data-proxy-with-ink-analysis.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="71f97-114">規格需求</span><span class="sxs-lookup"><span data-stu-id="71f97-114">Requirements</span></span>



| <span data-ttu-id="71f97-115">需求</span><span class="sxs-lookup"><span data-stu-id="71f97-115">Requirement</span></span> | <span data-ttu-id="71f97-116">值</span><span class="sxs-lookup"><span data-stu-id="71f97-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="71f97-117">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="71f97-117">Minimum supported client</span></span><br/> | <span data-ttu-id="71f97-118">僅限 Windows XP Tablet PC Edition \[ 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="71f97-118">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="71f97-119">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="71f97-119">Minimum supported server</span></span><br/> | <span data-ttu-id="71f97-120">都不支援</span><span class="sxs-lookup"><span data-stu-id="71f97-120">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="71f97-121">標頭</span><span class="sxs-lookup"><span data-stu-id="71f97-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="71f97-122"><dt>IACom (也需要 IACom \_ c) </dt></span><span class="sxs-lookup"><span data-stu-id="71f97-122"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="71f97-123">DLL</span><span class="sxs-lookup"><span data-stu-id="71f97-123">DLL</span></span><br/>                      | <dl> <span data-ttu-id="71f97-124"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="71f97-124"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="71f97-125">另請參閱</span><span class="sxs-lookup"><span data-stu-id="71f97-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="71f97-126">**ICoNtextNode**</span><span class="sxs-lookup"><span data-stu-id="71f97-126">**IContextNode**</span></span>](icontextnode.md)
</dt> <dt>

[<span data-ttu-id="71f97-127">**ICoNtextNode::SetPartiallyPopulated**</span><span class="sxs-lookup"><span data-stu-id="71f97-127">**IContextNode::SetPartiallyPopulated**</span></span>](icontextnode-setpartiallypopulated.md)
</dt> <dt>

[<span data-ttu-id="71f97-128">**ICoNtextNode::CreatePartiallyPopulatedSubNode**</span><span class="sxs-lookup"><span data-stu-id="71f97-128">**IContextNode::CreatePartiallyPopulatedSubNode**</span></span>](icontextnode-createpartiallypopulatedsubnode.md)
</dt> <dt>

[<span data-ttu-id="71f97-129">**\_IAnalysisProxyEvents：:P opulateCoNtextNode**</span><span class="sxs-lookup"><span data-stu-id="71f97-129">**\_IAnalysisProxyEvents::PopulateContextNode**</span></span>](-ianalysisproxyevents-populatecontextnode.md)
</dt> <dt>

[<span data-ttu-id="71f97-130">筆跡分析參考</span><span class="sxs-lookup"><span data-stu-id="71f97-130">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

 




