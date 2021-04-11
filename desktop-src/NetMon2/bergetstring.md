---
description: BERGetString 函式會將 BER 編碼的字串解碼。
ms.assetid: 1f72f061-c0ed-4634-9709-e08c2b9468bb
title: 'BERGetString 函式 (Netmon. h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- BERGetString
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: 6f8f864b8042ad49502ae53061e157575192e7bd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103849134"
---
# <a name="bergetstring-function"></a><span data-ttu-id="e5a01-103">BERGetString 函式</span><span class="sxs-lookup"><span data-stu-id="e5a01-103">BERGetString function</span></span>

<span data-ttu-id="e5a01-104">**BERGetString** 函式會將 BER 編碼的字串解碼。</span><span class="sxs-lookup"><span data-stu-id="e5a01-104">The **BERGetString** function decodes a BER-encoded string.</span></span>

## <a name="syntax"></a><span data-ttu-id="e5a01-105">語法</span><span class="sxs-lookup"><span data-stu-id="e5a01-105">Syntax</span></span>


```C++
BOOL BERGetString(
   LPBYTE  pCurrentPointer,
   LPBYTE  *ppValuePointer,
   LPDWORD pHeaderLength,
   LPDWORD pDataLength,
   LPBYTE  *ppNext
);
```



## <a name="parameters"></a><span data-ttu-id="e5a01-106">參數</span><span class="sxs-lookup"><span data-stu-id="e5a01-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e5a01-107">*pCurrentPointer*</span><span class="sxs-lookup"><span data-stu-id="e5a01-107">*pCurrentPointer*</span></span> 
</dt> <dd>

<span data-ttu-id="e5a01-108">已解碼之字串的指標。</span><span class="sxs-lookup"><span data-stu-id="e5a01-108">Pointer to the string that is decoded.</span></span>

</dd> <dt>

<span data-ttu-id="e5a01-109">*ppValuePointer*</span><span class="sxs-lookup"><span data-stu-id="e5a01-109">*ppValuePointer*</span></span> 
</dt> <dd>

<span data-ttu-id="e5a01-110">已解碼之字串指標的指標。</span><span class="sxs-lookup"><span data-stu-id="e5a01-110">Pointer to the pointer of the decoded string.</span></span>

</dd> <dt>

<span data-ttu-id="e5a01-111">*pHeaderLength*</span><span class="sxs-lookup"><span data-stu-id="e5a01-111">*pHeaderLength*</span></span> 
</dt> <dd>

<span data-ttu-id="e5a01-112">傳回之標頭長度的指標。</span><span class="sxs-lookup"><span data-stu-id="e5a01-112">Pointer to the returned header length.</span></span>

</dd> <dt>

<span data-ttu-id="e5a01-113">*pDataLength*</span><span class="sxs-lookup"><span data-stu-id="e5a01-113">*pDataLength*</span></span> 
</dt> <dd>

<span data-ttu-id="e5a01-114">字串長度的指標。</span><span class="sxs-lookup"><span data-stu-id="e5a01-114">Pointer to the string length.</span></span>

</dd> <dt>

<span data-ttu-id="e5a01-115">*ppNext*</span><span class="sxs-lookup"><span data-stu-id="e5a01-115">*ppNext*</span></span> 
</dt> <dd>

<span data-ttu-id="e5a01-116">下一個 BER 專案指標的指標。</span><span class="sxs-lookup"><span data-stu-id="e5a01-116">Pointer to the pointer of the next BER entry.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e5a01-117">傳回值</span><span class="sxs-lookup"><span data-stu-id="e5a01-117">Return value</span></span>

<span data-ttu-id="e5a01-118">如果函式成功 (也就是，如果有效的 BER 編碼字串) 解碼，則傳回值為 **TRUE**。</span><span class="sxs-lookup"><span data-stu-id="e5a01-118">If the function is successful (that is, if a valid BER-encoded string is decoded), the return value is **TRUE**.</span></span>

<span data-ttu-id="e5a01-119">如果函式不成功，則傳回值為 **FALSE**。</span><span class="sxs-lookup"><span data-stu-id="e5a01-119">If function is unsuccessful, the return value is **FALSE**.</span></span>

## <a name="requirements"></a><span data-ttu-id="e5a01-120">規格需求</span><span class="sxs-lookup"><span data-stu-id="e5a01-120">Requirements</span></span>



| <span data-ttu-id="e5a01-121">需求</span><span class="sxs-lookup"><span data-stu-id="e5a01-121">Requirement</span></span> | <span data-ttu-id="e5a01-122">值</span><span class="sxs-lookup"><span data-stu-id="e5a01-122">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="e5a01-123">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="e5a01-123">Minimum supported client</span></span><br/> | <span data-ttu-id="e5a01-124">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="e5a01-124">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                            |
| <span data-ttu-id="e5a01-125">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="e5a01-125">Minimum supported server</span></span><br/> | <span data-ttu-id="e5a01-126">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="e5a01-126">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="e5a01-127">標頭</span><span class="sxs-lookup"><span data-stu-id="e5a01-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="e5a01-128"><dt>Netmon</dt></span><span class="sxs-lookup"><span data-stu-id="e5a01-128"><dt>Netmon.h</dt></span></span> </dl>   |
| <span data-ttu-id="e5a01-129">程式庫</span><span class="sxs-lookup"><span data-stu-id="e5a01-129">Library</span></span><br/>                  | <dl> <span data-ttu-id="e5a01-130"><dt>剖析器 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="e5a01-130"><dt>Parser.lib</dt></span></span> </dl> |
| <span data-ttu-id="e5a01-131">DLL</span><span class="sxs-lookup"><span data-stu-id="e5a01-131">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e5a01-132"><dt>Nmapi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e5a01-132"><dt>Nmapi.dll</dt></span></span> </dl>  |



 

 




