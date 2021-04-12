---
title: 'FreeRepairInfoExs 函式 (Ndattributils) '
description: 將內部配置的記憶體解除配置至 RepairInfoEx 結構的陣列。
ms.assetid: b4e3e758-88cd-4ce2-b1a4-5b47889aae9b
keywords:
- FreeRepairInfoExs 函式 NDF
topic_type:
- apiref
api_name:
- FreeRepairInfoExs
api_location:
- ndattributils.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 094c745486526caa870a500019de3aa819b6fe5a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104508675"
---
# <a name="freerepairinfoexs-function"></a><span data-ttu-id="54b7a-104">FreeRepairInfoExs 函式</span><span class="sxs-lookup"><span data-stu-id="54b7a-104">FreeRepairInfoExs function</span></span>

<span data-ttu-id="54b7a-105">**FreeRepairInfoExs** 函式會將內部配置的記憶體解除配置至 [**RepairInfoEx**](/windows/win32/api/ndattrib/ns-ndattrib-repairinfoex)結構的陣列。</span><span class="sxs-lookup"><span data-stu-id="54b7a-105">The **FreeRepairInfoExs** function deallocates the memory allocated internally to an array of [**RepairInfoEx**](/windows/win32/api/ndattrib/ns-ndattrib-repairinfoex) structures.</span></span> <span data-ttu-id="54b7a-106">此函數會呼叫 [**CoTaskMemFree**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree) 來解除配置記憶體。</span><span class="sxs-lookup"><span data-stu-id="54b7a-106">This function calls [**CoTaskMemFree**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree) to deallocate memory.</span></span>

## <a name="syntax"></a><span data-ttu-id="54b7a-107">語法</span><span class="sxs-lookup"><span data-stu-id="54b7a-107">Syntax</span></span>


```C++
VOID FreeRepairInfoExs(
  _In_ RepairInfoEx *pInfo,
       ULONG        RepairCount,
       BOOL         bFreePointer
);
```



## <a name="parameters"></a><span data-ttu-id="54b7a-108">參數</span><span class="sxs-lookup"><span data-stu-id="54b7a-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="54b7a-109">*pInfo* \[在\]</span><span class="sxs-lookup"><span data-stu-id="54b7a-109">*pInfo* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="54b7a-110">類型： \**[**RepairInfoEx**](/windows/win32/api/ndattrib/ns-ndattrib-repairinfoex) \** _</span><span class="sxs-lookup"><span data-stu-id="54b7a-110">Type: \**[**RepairInfoEx**](/windows/win32/api/ndattrib/ns-ndattrib-repairinfoex)\** _</span></span>

<span data-ttu-id="54b7a-111">結構的陣列。</span><span class="sxs-lookup"><span data-stu-id="54b7a-111">The array of structures.</span></span> <span data-ttu-id="54b7a-112">將釋放這些結構所指向的配置記憶體。</span><span class="sxs-lookup"><span data-stu-id="54b7a-112">The allocated memory pointed to by these structures will be freed.</span></span>

</dd> <dt>

<span data-ttu-id="54b7a-113">_RepairCount \*</span><span class="sxs-lookup"><span data-stu-id="54b7a-113">_RepairCount\*</span></span> 
</dt> <dd>

<span data-ttu-id="54b7a-114">類型： **ULONG**</span><span class="sxs-lookup"><span data-stu-id="54b7a-114">Type: **ULONG**</span></span>

<span data-ttu-id="54b7a-115">*PInfo* 所指向之陣列中的結構數目。</span><span class="sxs-lookup"><span data-stu-id="54b7a-115">The number of structures in the array pointed to by *pInfo*.</span></span>

</dd> <dt>

<span data-ttu-id="54b7a-116">*bFreePointer*</span><span class="sxs-lookup"><span data-stu-id="54b7a-116">*bFreePointer*</span></span> 
</dt> <dd>

<span data-ttu-id="54b7a-117">類型： **BOOL**</span><span class="sxs-lookup"><span data-stu-id="54b7a-117">Type: **BOOL**</span></span>

<span data-ttu-id="54b7a-118">如果也應該刪除結構的陣列，則為 True;否則為 false。</span><span class="sxs-lookup"><span data-stu-id="54b7a-118">True if the array of structures should also be deleted; otherwise, false.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="54b7a-119">傳回值</span><span class="sxs-lookup"><span data-stu-id="54b7a-119">Return value</span></span>

<span data-ttu-id="54b7a-120">此函式不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="54b7a-120">This function does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="54b7a-121">規格需求</span><span class="sxs-lookup"><span data-stu-id="54b7a-121">Requirements</span></span>



| <span data-ttu-id="54b7a-122">需求</span><span class="sxs-lookup"><span data-stu-id="54b7a-122">Requirement</span></span> | <span data-ttu-id="54b7a-123">值</span><span class="sxs-lookup"><span data-stu-id="54b7a-123">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| <span data-ttu-id="54b7a-124">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="54b7a-124">Minimum supported client</span></span><br/> | <span data-ttu-id="54b7a-125">\[僅 Windows 8 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="54b7a-125">Windows 8 \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="54b7a-126">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="54b7a-126">Minimum supported server</span></span><br/> | <span data-ttu-id="54b7a-127">僅限 Windows Server 2012 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="54b7a-127">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="54b7a-128">標頭</span><span class="sxs-lookup"><span data-stu-id="54b7a-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="54b7a-129"><dt>Ndattributils。h</dt></span><span class="sxs-lookup"><span data-stu-id="54b7a-129"><dt>Ndattributils.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="54b7a-130">另請參閱</span><span class="sxs-lookup"><span data-stu-id="54b7a-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="54b7a-131">**RepairInfoEx**</span><span class="sxs-lookup"><span data-stu-id="54b7a-131">**RepairInfoEx**</span></span>](/windows/win32/api/ndattrib/ns-ndattrib-repairinfoex)
</dt> <dt>

[<span data-ttu-id="54b7a-132">**CoTaskMemFree**</span><span class="sxs-lookup"><span data-stu-id="54b7a-132">**CoTaskMemFree**</span></span>](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree)
</dt> </dl>

 

