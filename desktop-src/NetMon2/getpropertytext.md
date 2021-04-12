---
description: GetPropertyText 函式會傳回屬性文字的指標。
ms.assetid: 1bcbdbb8-4ec5-4cea-a1c6-4a1f37476f50
title: 'GetPropertyText 函式 (Netmon. h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetPropertyText
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: 10dbabf32840d2ae5f965687a6261b8bec27a1a1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104318076"
---
# <a name="getpropertytext-function"></a><span data-ttu-id="16b73-103">GetPropertyText 函式</span><span class="sxs-lookup"><span data-stu-id="16b73-103">GetPropertyText function</span></span>

<span data-ttu-id="16b73-104">**GetPropertyText** 函式會傳回屬性文字的指標。</span><span class="sxs-lookup"><span data-stu-id="16b73-104">The **GetPropertyText** function returns a pointer to the property text.</span></span>

## <a name="syntax"></a><span data-ttu-id="16b73-105">語法</span><span class="sxs-lookup"><span data-stu-id="16b73-105">Syntax</span></span>


```C++
LPSTR WINAPI GetPropertyText(
  _In_ HFRAME         hFrame,
  _In_ LPPROPERTYINST lpPI,
  _In_ LPSTR          szBuffer,
  _In_ DWORD          BufferSize
);
```



## <a name="parameters"></a><span data-ttu-id="16b73-106">參數</span><span class="sxs-lookup"><span data-stu-id="16b73-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="16b73-107">*hFrame* \[在\]</span><span class="sxs-lookup"><span data-stu-id="16b73-107">*hFrame* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="16b73-108">框架的控制碼。</span><span class="sxs-lookup"><span data-stu-id="16b73-108">Handle to the frame.</span></span>

</dd> <dt>

<span data-ttu-id="16b73-109">*lpPI* \[在\]</span><span class="sxs-lookup"><span data-stu-id="16b73-109">*lpPI* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="16b73-110">屬性實例的指標。</span><span class="sxs-lookup"><span data-stu-id="16b73-110">Pointer to a property instance.</span></span>

</dd> <dt>

<span data-ttu-id="16b73-111">*szBuffer* \[在\]</span><span class="sxs-lookup"><span data-stu-id="16b73-111">*szBuffer* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="16b73-112">屬性文字字串的指標。</span><span class="sxs-lookup"><span data-stu-id="16b73-112">Pointer to the property text string.</span></span>

</dd> <dt>

<span data-ttu-id="16b73-113">*BufferSize* \[在\]</span><span class="sxs-lookup"><span data-stu-id="16b73-113">*BufferSize* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="16b73-114">文字字串緩衝區的大小。</span><span class="sxs-lookup"><span data-stu-id="16b73-114">Size of the text string buffer.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="16b73-115">傳回值</span><span class="sxs-lookup"><span data-stu-id="16b73-115">Return value</span></span>

<span data-ttu-id="16b73-116">如果函式成功，則傳回值為屬性文字的指標。</span><span class="sxs-lookup"><span data-stu-id="16b73-116">If the function is successful, the return value is a pointer to the property text.</span></span>

<span data-ttu-id="16b73-117">如果函式不成功，則傳回值為 **Null**。</span><span class="sxs-lookup"><span data-stu-id="16b73-117">If the function is unsuccessful, the return value is **NULL**.</span></span>

## <a name="remarks"></a><span data-ttu-id="16b73-118">備註</span><span class="sxs-lookup"><span data-stu-id="16b73-118">Remarks</span></span>

<span data-ttu-id="16b73-119">[*專家*](e.md) 和 [*剖析*](p.md) 器可以呼叫 **GetPropertyText** 函數。</span><span class="sxs-lookup"><span data-stu-id="16b73-119">[*Experts*](e.md) and [*parsers*](p.md) can call the **GetPropertyText** function.</span></span>

## <a name="requirements"></a><span data-ttu-id="16b73-120">規格需求</span><span class="sxs-lookup"><span data-stu-id="16b73-120">Requirements</span></span>



| <span data-ttu-id="16b73-121">需求</span><span class="sxs-lookup"><span data-stu-id="16b73-121">Requirement</span></span> | <span data-ttu-id="16b73-122">值</span><span class="sxs-lookup"><span data-stu-id="16b73-122">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="16b73-123">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="16b73-123">Minimum supported client</span></span><br/> | <span data-ttu-id="16b73-124">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="16b73-124">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="16b73-125">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="16b73-125">Minimum supported server</span></span><br/> | <span data-ttu-id="16b73-126">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="16b73-126">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="16b73-127">標頭</span><span class="sxs-lookup"><span data-stu-id="16b73-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="16b73-128"><dt>Netmon</dt></span><span class="sxs-lookup"><span data-stu-id="16b73-128"><dt>Netmon.h</dt></span></span> </dl>  |
| <span data-ttu-id="16b73-129">程式庫</span><span class="sxs-lookup"><span data-stu-id="16b73-129">Library</span></span><br/>                  | <dl> <span data-ttu-id="16b73-130"><dt>Nmapi .lib</dt></span><span class="sxs-lookup"><span data-stu-id="16b73-130"><dt>Nmapi.lib</dt></span></span> </dl> |
| <span data-ttu-id="16b73-131">DLL</span><span class="sxs-lookup"><span data-stu-id="16b73-131">DLL</span></span><br/>                      | <dl> <span data-ttu-id="16b73-132"><dt>Nmapi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="16b73-132"><dt>Nmapi.dll</dt></span></span> </dl> |



 

 




