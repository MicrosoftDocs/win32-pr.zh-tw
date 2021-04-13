---
title: 'FreeHelperAttributes 函式 (Ndattributils) '
description: 將內部配置的記憶體解除配置至 HELPER \_ 屬性結構的陣列。
ms.assetid: d973bdb9-c1d1-4cea-bcc6-98671349413f
keywords:
- FreeHelperAttributes 函式 NDF
topic_type:
- apiref
api_name:
- FreeHelperAttributes
api_location:
- ndattributils.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 400addd7d32914cb4e849e4e0bfae76ccc3ddf22
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104464821"
---
# <a name="freehelperattributes-function"></a><span data-ttu-id="3ec21-104">FreeHelperAttributes 函式</span><span class="sxs-lookup"><span data-stu-id="3ec21-104">FreeHelperAttributes function</span></span>

<span data-ttu-id="3ec21-105">**FreeHelperAttributes** 函式會將內部配置的記憶體解除配置至 [**HELPER \_ 屬性**](/windows/win32/api/ndattrib/ns-ndattrib-helper_attribute)結構的陣列。</span><span class="sxs-lookup"><span data-stu-id="3ec21-105">The **FreeHelperAttributes** function deallocates the memory allocated internally to an array of [**HELPER\_ATTRIBUTE**](/windows/win32/api/ndattrib/ns-ndattrib-helper_attribute) structures.</span></span> <span data-ttu-id="3ec21-106">此函數會呼叫 [**CoTaskMemFree**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree) 來解除配置記憶體。</span><span class="sxs-lookup"><span data-stu-id="3ec21-106">This function calls [**CoTaskMemFree**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree) to deallocate memory.</span></span>

## <a name="syntax"></a><span data-ttu-id="3ec21-107">語法</span><span class="sxs-lookup"><span data-stu-id="3ec21-107">Syntax</span></span>


```C++
VOID FreeHelperAttributes(
  _In_ HELPER_ATTRIBUTE *pInfo,
       ULONG            HelperAttributeCount,
       BOOL             bFreePointer
);
```



## <a name="parameters"></a><span data-ttu-id="3ec21-108">參數</span><span class="sxs-lookup"><span data-stu-id="3ec21-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3ec21-109">*pInfo* \[在\]</span><span class="sxs-lookup"><span data-stu-id="3ec21-109">*pInfo* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3ec21-110">類型： \* 協助程式 *[**\_ 屬性**](/windows/win32/api/ndattrib/ns-ndattrib-helper_attribute) \** _</span><span class="sxs-lookup"><span data-stu-id="3ec21-110">Type: \**[**HELPER\_ATTRIBUTE**](/windows/win32/api/ndattrib/ns-ndattrib-helper_attribute)\** _</span></span>

<span data-ttu-id="3ec21-111">結構的陣列。</span><span class="sxs-lookup"><span data-stu-id="3ec21-111">The array of structures.</span></span> <span data-ttu-id="3ec21-112">將釋放這些結構所指向的配置記憶體。</span><span class="sxs-lookup"><span data-stu-id="3ec21-112">The allocated memory pointed to by these structures will be freed.</span></span>

</dd> <dt>

<span data-ttu-id="3ec21-113">_HelperAttributeCount \*</span><span class="sxs-lookup"><span data-stu-id="3ec21-113">_HelperAttributeCount\*</span></span> 
</dt> <dd>

<span data-ttu-id="3ec21-114">類型： **ULONG**</span><span class="sxs-lookup"><span data-stu-id="3ec21-114">Type: **ULONG**</span></span>

<span data-ttu-id="3ec21-115">*PInfo* 所指向之陣列中的結構數目。</span><span class="sxs-lookup"><span data-stu-id="3ec21-115">The number of structures in the array pointed to by *pInfo*.</span></span>

</dd> <dt>

<span data-ttu-id="3ec21-116">*bFreePointer*</span><span class="sxs-lookup"><span data-stu-id="3ec21-116">*bFreePointer*</span></span> 
</dt> <dd>

<span data-ttu-id="3ec21-117">類型： **BOOL**</span><span class="sxs-lookup"><span data-stu-id="3ec21-117">Type: **BOOL**</span></span>

<span data-ttu-id="3ec21-118">如果也應該刪除結構的陣列，則為 True;否則為 false。</span><span class="sxs-lookup"><span data-stu-id="3ec21-118">True if the array of structures should also be deleted; otherwise, false.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3ec21-119">傳回值</span><span class="sxs-lookup"><span data-stu-id="3ec21-119">Return value</span></span>

<span data-ttu-id="3ec21-120">此函式不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="3ec21-120">This function does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="3ec21-121">規格需求</span><span class="sxs-lookup"><span data-stu-id="3ec21-121">Requirements</span></span>



| <span data-ttu-id="3ec21-122">需求</span><span class="sxs-lookup"><span data-stu-id="3ec21-122">Requirement</span></span> | <span data-ttu-id="3ec21-123">值</span><span class="sxs-lookup"><span data-stu-id="3ec21-123">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| <span data-ttu-id="3ec21-124">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="3ec21-124">Minimum supported client</span></span><br/> | <span data-ttu-id="3ec21-125">\[僅 Windows 8 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="3ec21-125">Windows 8 \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="3ec21-126">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="3ec21-126">Minimum supported server</span></span><br/> | <span data-ttu-id="3ec21-127">僅限 Windows Server 2012 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="3ec21-127">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="3ec21-128">標頭</span><span class="sxs-lookup"><span data-stu-id="3ec21-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="3ec21-129"><dt>Ndattributils。h</dt></span><span class="sxs-lookup"><span data-stu-id="3ec21-129"><dt>Ndattributils.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3ec21-130">另請參閱</span><span class="sxs-lookup"><span data-stu-id="3ec21-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3ec21-131">**HELPER \_ 屬性**</span><span class="sxs-lookup"><span data-stu-id="3ec21-131">**HELPER\_ATTRIBUTE**</span></span>](/windows/win32/api/ndattrib/ns-ndattrib-helper_attribute)
</dt> <dt>

[<span data-ttu-id="3ec21-132">**CoTaskMemFree**</span><span class="sxs-lookup"><span data-stu-id="3ec21-132">**CoTaskMemFree**</span></span>](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree)
</dt> </dl>

 

