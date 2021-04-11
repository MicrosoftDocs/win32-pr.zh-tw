---
description: 抓取位於指定之索引處的 ICoNtextLink。
ms.assetid: 46bb71b9-5ef3-4756-97f6-40e0aaa82826
title: 'ICoNtextLinks：： GetCoNtextLink 方法 (IACom .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IContextLinks.GetContextLink
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: ecc0ed9ba457a7a91cb2e1b615ac7419ce5a94c5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104113393"
---
# <a name="icontextlinksgetcontextlink-method"></a><span data-ttu-id="7be78-103">ICoNtextLinks：： GetCoNtextLink 方法</span><span class="sxs-lookup"><span data-stu-id="7be78-103">IContextLinks::GetContextLink method</span></span>

<span data-ttu-id="7be78-104">抓取位於指定之索引處的 [**ICoNtextLink**](icontextlink.md) 。</span><span class="sxs-lookup"><span data-stu-id="7be78-104">Retrieves the [**IContextLink**](icontextlink.md) at the specified index.</span></span>

## <a name="syntax"></a><span data-ttu-id="7be78-105">語法</span><span class="sxs-lookup"><span data-stu-id="7be78-105">Syntax</span></span>


```C++
HRESULT GetContextLink(
  [in]  ULONG        ulIndex,
  [out] IContextLink **ppContextLink
);
```



## <a name="parameters"></a><span data-ttu-id="7be78-106">參數</span><span class="sxs-lookup"><span data-stu-id="7be78-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7be78-107">*ulIndex* \[在\]</span><span class="sxs-lookup"><span data-stu-id="7be78-107">*ulIndex* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7be78-108">要取得之 [**ICoNtextLink**](icontextlink.md) 物件的以零為基底的索引。</span><span class="sxs-lookup"><span data-stu-id="7be78-108">The zero-based index of the [**IContextLink**](icontextlink.md) object to get.</span></span>

</dd> <dt>

<span data-ttu-id="7be78-109">*ppCoNtextLink* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="7be78-109">*ppContextLink* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="7be78-110">位於指定索引處之 [**ICoNtextLink**](icontextlink.md) 物件的指標。</span><span class="sxs-lookup"><span data-stu-id="7be78-110">A pointer to the [**IContextLink**](icontextlink.md) object at the specified index.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7be78-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="7be78-111">Return value</span></span>

<span data-ttu-id="7be78-112">如需傳回值的描述，請參閱 [類別和介面-筆跡分析](classes-and-interfaces---ink-analysis.md)。</span><span class="sxs-lookup"><span data-stu-id="7be78-112">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="7be78-113">備註</span><span class="sxs-lookup"><span data-stu-id="7be78-113">Remarks</span></span>

> [!Caution]  
> <span data-ttu-id="7be78-114">若要避免記憶體流失，請在 ppCoNtextLink 上呼叫 [**IUnknown：： Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) （ \* 當您不再需要使用內容連結時）。</span><span class="sxs-lookup"><span data-stu-id="7be78-114">To avoid a memory leak, call [**IUnknown::Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) on \**ppContextLink* when you no longer need to use the context link.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="7be78-115">規格需求</span><span class="sxs-lookup"><span data-stu-id="7be78-115">Requirements</span></span>



| <span data-ttu-id="7be78-116">需求</span><span class="sxs-lookup"><span data-stu-id="7be78-116">Requirement</span></span> | <span data-ttu-id="7be78-117">值</span><span class="sxs-lookup"><span data-stu-id="7be78-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7be78-118">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="7be78-118">Minimum supported client</span></span><br/> | <span data-ttu-id="7be78-119">僅限 Windows XP Tablet PC Edition \[ 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="7be78-119">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="7be78-120">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="7be78-120">Minimum supported server</span></span><br/> | <span data-ttu-id="7be78-121">都不支援</span><span class="sxs-lookup"><span data-stu-id="7be78-121">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="7be78-122">標頭</span><span class="sxs-lookup"><span data-stu-id="7be78-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="7be78-123"><dt>IACom (也需要 IACom \_ c) </dt></span><span class="sxs-lookup"><span data-stu-id="7be78-123"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="7be78-124">DLL</span><span class="sxs-lookup"><span data-stu-id="7be78-124">DLL</span></span><br/>                      | <dl> <span data-ttu-id="7be78-125"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7be78-125"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="7be78-126">另請參閱</span><span class="sxs-lookup"><span data-stu-id="7be78-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7be78-127">**ICoNtextLinks**</span><span class="sxs-lookup"><span data-stu-id="7be78-127">**IContextLinks**</span></span>](icontextlinks.md)
</dt> <dt>

[<span data-ttu-id="7be78-128">**ICoNtextNode**</span><span class="sxs-lookup"><span data-stu-id="7be78-128">**IContextNode**</span></span>](icontextnode.md)
</dt> <dt>

[<span data-ttu-id="7be78-129">筆跡分析參考</span><span class="sxs-lookup"><span data-stu-id="7be78-129">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

