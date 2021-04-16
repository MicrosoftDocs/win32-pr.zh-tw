---
description: 抓取值，這個值會指出是否已在此 ICoNtextNode 上設定傳遞給這個方法的 ConfirmationType。
ms.assetid: 4a96bc46-b627-4784-ad1d-1079f49592e5
title: 'ICoNtextNode：： IsConfirmed 方法 (IACom .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IContextNode.IsConfirmed
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 300e0126b4a1ff55d372ff31deebde0eab686645
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104511673"
---
# <a name="icontextnodeisconfirmed-method"></a><span data-ttu-id="12949-103">ICoNtextNode：： IsConfirmed 方法</span><span class="sxs-lookup"><span data-stu-id="12949-103">IContextNode::IsConfirmed method</span></span>

<span data-ttu-id="12949-104">抓取值，這個值會指出是否已在此 ICoNtextNode 上設定傳遞給這個方法的 ConfirmationType。</span><span class="sxs-lookup"><span data-stu-id="12949-104">Retrieves a value that indicates whether the ConfirmationType passed in to this method has been set on this IContextNode.</span></span>

## <a name="syntax"></a><span data-ttu-id="12949-105">語法</span><span class="sxs-lookup"><span data-stu-id="12949-105">Syntax</span></span>


```C++
HRESULT IsConfirmed(
  [in]  ConfirmationType confirmedType,
  [out] VARIANT_BOOL     *pfTypeConfirmed
);
```



## <a name="parameters"></a><span data-ttu-id="12949-106">參數</span><span class="sxs-lookup"><span data-stu-id="12949-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="12949-107">*confirmedType* \[在\]</span><span class="sxs-lookup"><span data-stu-id="12949-107">*confirmedType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="12949-108">要測試的確認類型。</span><span class="sxs-lookup"><span data-stu-id="12949-108">The confirmation type being tested for.</span></span>

</dd> <dt>

<span data-ttu-id="12949-109">*pfTypeConfirmed* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="12949-109">*pfTypeConfirmed* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="12949-110">**變異 \_** 如果已在這個 [**ICoNtextNode**](icontextnode.md)物件上設定 confirmedType 傳遞的型別，則為 TRUE;否則， **VARIANT \_ FALSE**。</span><span class="sxs-lookup"><span data-stu-id="12949-110">**VARIANT\_TRUE** if the type passed in confirmedType has been set on this [**IContextNode**](icontextnode.md) object; otherwise, **VARIANT\_FALSE**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="12949-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="12949-111">Return value</span></span>

<span data-ttu-id="12949-112">如需傳回值的描述，請參閱 [類別和介面-筆跡分析](classes-and-interfaces---ink-analysis.md)。</span><span class="sxs-lookup"><span data-stu-id="12949-112">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="12949-113">備註</span><span class="sxs-lookup"><span data-stu-id="12949-113">Remarks</span></span>

<span data-ttu-id="12949-114">這個值是由 [**ICoNtextNode：： Confirm**](icontextnode-confirm.md) 方法設定。</span><span class="sxs-lookup"><span data-stu-id="12949-114">This value is set by the [**IContextNode::Confirm**](icontextnode-confirm.md) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="12949-115">規格需求</span><span class="sxs-lookup"><span data-stu-id="12949-115">Requirements</span></span>



| <span data-ttu-id="12949-116">需求</span><span class="sxs-lookup"><span data-stu-id="12949-116">Requirement</span></span> | <span data-ttu-id="12949-117">值</span><span class="sxs-lookup"><span data-stu-id="12949-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="12949-118">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="12949-118">Minimum supported client</span></span><br/> | <span data-ttu-id="12949-119">僅限 Windows XP Tablet PC Edition \[ 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="12949-119">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="12949-120">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="12949-120">Minimum supported server</span></span><br/> | <span data-ttu-id="12949-121">都不支援</span><span class="sxs-lookup"><span data-stu-id="12949-121">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="12949-122">標頭</span><span class="sxs-lookup"><span data-stu-id="12949-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="12949-123"><dt>IACom (也需要 IACom \_ c) </dt></span><span class="sxs-lookup"><span data-stu-id="12949-123"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="12949-124">DLL</span><span class="sxs-lookup"><span data-stu-id="12949-124">DLL</span></span><br/>                      | <dl> <span data-ttu-id="12949-125"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="12949-125"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="12949-126">另請參閱</span><span class="sxs-lookup"><span data-stu-id="12949-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="12949-127">**ICoNtextNode**</span><span class="sxs-lookup"><span data-stu-id="12949-127">**IContextNode**</span></span>](icontextnode.md)
</dt> <dt>

[<span data-ttu-id="12949-128">**ICoNtextNode：： Confirm**</span><span class="sxs-lookup"><span data-stu-id="12949-128">**IContextNode::Confirm**</span></span>](icontextnode-confirm.md)
</dt> <dt>

[<span data-ttu-id="12949-129">筆跡分析參考</span><span class="sxs-lookup"><span data-stu-id="12949-129">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

 




