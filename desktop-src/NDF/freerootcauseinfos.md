---
title: 'FreeRootCauseInfos 函式 (Ndattributils) '
description: 將內部配置的記憶體解除配置至 RootCauseInfo 結構的陣列。
ms.assetid: b45fa432-0db4-470b-80ce-ae25c33f88d6
keywords:
- FreeRootCauseInfos 函式 NDF
topic_type:
- apiref
api_name:
- FreeRootCauseInfos
api_location:
- ndattributils.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 97d302a1c58f1a77aafa7611f437f3d445f29f9a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103685756"
---
# <a name="freerootcauseinfos-function"></a><span data-ttu-id="33a53-104">FreeRootCauseInfos 函式</span><span class="sxs-lookup"><span data-stu-id="33a53-104">FreeRootCauseInfos function</span></span>

<span data-ttu-id="33a53-105">**FreeRootCauseInfos** 函式會將內部配置的記憶體解除配置至 [**RootCauseInfo**](/windows/win32/api/ndattrib/ns-ndattrib-rootcauseinfo)結構的陣列。</span><span class="sxs-lookup"><span data-stu-id="33a53-105">The **FreeRootCauseInfos** function deallocates the memory allocated internally to an array of [**RootCauseInfo**](/windows/win32/api/ndattrib/ns-ndattrib-rootcauseinfo) structures.</span></span> <span data-ttu-id="33a53-106">此函數會呼叫 [**CoTaskMemFree**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree) 來解除配置記憶體。</span><span class="sxs-lookup"><span data-stu-id="33a53-106">This function calls [**CoTaskMemFree**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree) to deallocate memory.</span></span>

## <a name="syntax"></a><span data-ttu-id="33a53-107">語法</span><span class="sxs-lookup"><span data-stu-id="33a53-107">Syntax</span></span>


```C++
VOID FreeRootCauseInfos(
  _In_ RootCauseInfo *pInfo,
       ULONG         RootCauseCount,
       BOOL          bFreePointer
);
```



## <a name="parameters"></a><span data-ttu-id="33a53-108">參數</span><span class="sxs-lookup"><span data-stu-id="33a53-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="33a53-109">*pInfo* \[在\]</span><span class="sxs-lookup"><span data-stu-id="33a53-109">*pInfo* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="33a53-110">類型： \**[**RootCauseInfo**](/windows/win32/api/ndattrib/ns-ndattrib-rootcauseinfo) \** _</span><span class="sxs-lookup"><span data-stu-id="33a53-110">Type: \**[**RootCauseInfo**](/windows/win32/api/ndattrib/ns-ndattrib-rootcauseinfo)\** _</span></span>

<span data-ttu-id="33a53-111">結構的陣列。</span><span class="sxs-lookup"><span data-stu-id="33a53-111">The array of structures.</span></span> <span data-ttu-id="33a53-112">將釋放這些結構所指向的配置記憶體。</span><span class="sxs-lookup"><span data-stu-id="33a53-112">The allocated memory pointed to by these structures will be freed.</span></span>

</dd> <dt>

<span data-ttu-id="33a53-113">_RootCauseCount \*</span><span class="sxs-lookup"><span data-stu-id="33a53-113">_RootCauseCount\*</span></span> 
</dt> <dd>

<span data-ttu-id="33a53-114">類型： **ULONG**</span><span class="sxs-lookup"><span data-stu-id="33a53-114">Type: **ULONG**</span></span>

<span data-ttu-id="33a53-115">*PInfo* 所指向之陣列中的結構數目。</span><span class="sxs-lookup"><span data-stu-id="33a53-115">The number of structures in the array pointed to by *pInfo*.</span></span>

</dd> <dt>

<span data-ttu-id="33a53-116">*bFreePointer*</span><span class="sxs-lookup"><span data-stu-id="33a53-116">*bFreePointer*</span></span> 
</dt> <dd>

<span data-ttu-id="33a53-117">類型： **BOOL**</span><span class="sxs-lookup"><span data-stu-id="33a53-117">Type: **BOOL**</span></span>

<span data-ttu-id="33a53-118">如果也應該刪除結構的陣列，則為 True;否則為 false。</span><span class="sxs-lookup"><span data-stu-id="33a53-118">True if the array of structures should also be deleted; otherwise, false.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="33a53-119">傳回值</span><span class="sxs-lookup"><span data-stu-id="33a53-119">Return value</span></span>

<span data-ttu-id="33a53-120">此函式不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="33a53-120">This function does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="33a53-121">規格需求</span><span class="sxs-lookup"><span data-stu-id="33a53-121">Requirements</span></span>



| <span data-ttu-id="33a53-122">需求</span><span class="sxs-lookup"><span data-stu-id="33a53-122">Requirement</span></span> | <span data-ttu-id="33a53-123">值</span><span class="sxs-lookup"><span data-stu-id="33a53-123">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| <span data-ttu-id="33a53-124">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="33a53-124">Minimum supported client</span></span><br/> | <span data-ttu-id="33a53-125">\[僅 Windows 8 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="33a53-125">Windows 8 \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="33a53-126">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="33a53-126">Minimum supported server</span></span><br/> | <span data-ttu-id="33a53-127">僅限 Windows Server 2012 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="33a53-127">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="33a53-128">標頭</span><span class="sxs-lookup"><span data-stu-id="33a53-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="33a53-129"><dt>Ndattributils。h</dt></span><span class="sxs-lookup"><span data-stu-id="33a53-129"><dt>Ndattributils.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="33a53-130">另請參閱</span><span class="sxs-lookup"><span data-stu-id="33a53-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="33a53-131">**RootCauseInfo**</span><span class="sxs-lookup"><span data-stu-id="33a53-131">**RootCauseInfo**</span></span>](/windows/win32/api/ndattrib/ns-ndattrib-rootcauseinfo)
</dt> <dt>

[<span data-ttu-id="33a53-132">**CoTaskMemFree**</span><span class="sxs-lookup"><span data-stu-id="33a53-132">**CoTaskMemFree**</span></span>](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree)
</dt> </dl>

 

