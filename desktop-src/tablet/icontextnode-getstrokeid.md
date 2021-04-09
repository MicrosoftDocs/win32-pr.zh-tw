---
description: 抓取 ICoNtextNode 物件內索引值所參考之筆劃的筆觸識別碼。
ms.assetid: faac142e-cac1-45f9-9b40-76c50ac7006b
title: 'ICoNtextNode：： GetStrokeId 方法 (IACom .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IContextNode.GetStrokeId
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: b193b3719ac6b67284e3ff8c4297455888f6c9cd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103690599"
---
# <a name="icontextnodegetstrokeid-method"></a><span data-ttu-id="70242-103">ICoNtextNode：： GetStrokeId 方法</span><span class="sxs-lookup"><span data-stu-id="70242-103">IContextNode::GetStrokeId method</span></span>

<span data-ttu-id="70242-104">抓取 [**ICoNtextNode**](icontextnode.md) 物件內索引值所參考之筆劃的筆觸識別碼。</span><span class="sxs-lookup"><span data-stu-id="70242-104">Retrieves the stroke identifier for the stroke referenced by an index value within the [**IContextNode**](icontextnode.md) object.</span></span>

## <a name="syntax"></a><span data-ttu-id="70242-105">語法</span><span class="sxs-lookup"><span data-stu-id="70242-105">Syntax</span></span>


```C++
HRESULT GetStrokeId(
  [in]  ULONG ulIndex,
  [out] LONG  *plStrokeId
);
```



## <a name="parameters"></a><span data-ttu-id="70242-106">參數</span><span class="sxs-lookup"><span data-stu-id="70242-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="70242-107">*ulIndex* \[在\]</span><span class="sxs-lookup"><span data-stu-id="70242-107">*ulIndex* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="70242-108">要傳回之筆劃的索引。</span><span class="sxs-lookup"><span data-stu-id="70242-108">The index of the stroke to be returned.</span></span>

</dd> <dt>

<span data-ttu-id="70242-109">*plStrokeId* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="70242-109">*plStrokeId* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="70242-110">目前 [**ICoNtextNode**](icontextnode.md)物件內 *ulIndex* 參數所參考之筆劃的筆觸識別碼。</span><span class="sxs-lookup"><span data-stu-id="70242-110">The stroke identifier for the stroke referenced by the *ulIndex* parameter within the current [**IContextNode**](icontextnode.md) object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="70242-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="70242-111">Return value</span></span>

<span data-ttu-id="70242-112">如需傳回值的描述，請參閱 [類別和介面-筆跡分析](classes-and-interfaces---ink-analysis.md)。</span><span class="sxs-lookup"><span data-stu-id="70242-112">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="70242-113">規格需求</span><span class="sxs-lookup"><span data-stu-id="70242-113">Requirements</span></span>



| <span data-ttu-id="70242-114">需求</span><span class="sxs-lookup"><span data-stu-id="70242-114">Requirement</span></span> | <span data-ttu-id="70242-115">值</span><span class="sxs-lookup"><span data-stu-id="70242-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="70242-116">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="70242-116">Minimum supported client</span></span><br/> | <span data-ttu-id="70242-117">僅限 Windows XP Tablet PC Edition \[ 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="70242-117">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="70242-118">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="70242-118">Minimum supported server</span></span><br/> | <span data-ttu-id="70242-119">都不支援</span><span class="sxs-lookup"><span data-stu-id="70242-119">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="70242-120">標頭</span><span class="sxs-lookup"><span data-stu-id="70242-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="70242-121"><dt>IACom (也需要 IACom \_ c) </dt></span><span class="sxs-lookup"><span data-stu-id="70242-121"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="70242-122">DLL</span><span class="sxs-lookup"><span data-stu-id="70242-122">DLL</span></span><br/>                      | <dl> <span data-ttu-id="70242-123"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="70242-123"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="70242-124">另請參閱</span><span class="sxs-lookup"><span data-stu-id="70242-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="70242-125">**ICoNtextNode**</span><span class="sxs-lookup"><span data-stu-id="70242-125">**IContextNode**</span></span>](icontextnode.md)
</dt> <dt>

[<span data-ttu-id="70242-126">**ICoNtextNode::GetStrokeIds**</span><span class="sxs-lookup"><span data-stu-id="70242-126">**IContextNode::GetStrokeIds**</span></span>](icontextnode-getstrokeids.md)
</dt> <dt>

[<span data-ttu-id="70242-127">**ICoNtextNode::GetStrokeCount**</span><span class="sxs-lookup"><span data-stu-id="70242-127">**IContextNode::GetStrokeCount**</span></span>](icontextnode-getstrokecount.md)
</dt> <dt>

[<span data-ttu-id="70242-128">筆跡分析參考</span><span class="sxs-lookup"><span data-stu-id="70242-128">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

 




