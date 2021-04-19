---
description: BERGetHeader 函式會解碼 choice 標頭。
ms.assetid: 2574a9b3-c28e-43d1-904f-d45888617584
title: 'BERGetHeader 函式 (Netmon. h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- BERGetHeader
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: 5e2213b15b6b4d2cbaa15b3b9aa9de028e20a62d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106975076"
---
# <a name="bergetheader-function"></a><span data-ttu-id="c2702-103">BERGetHeader 函式</span><span class="sxs-lookup"><span data-stu-id="c2702-103">BERGetHeader function</span></span>

<span data-ttu-id="c2702-104">**BERGetHeader** 函式會解碼 choice 標頭。</span><span class="sxs-lookup"><span data-stu-id="c2702-104">The **BERGetHeader** function decodes a choice header.</span></span>

## <a name="syntax"></a><span data-ttu-id="c2702-105">語法</span><span class="sxs-lookup"><span data-stu-id="c2702-105">Syntax</span></span>


```C++
BOOL BERGetHeader(
   LPBYTE  pCurrentPointer,
   LPBYTE  pTag,
   LPDWORD pHeaderLength,
   LPDWORD pDataLength,
   LPBYTE  *ppNext
);
```



## <a name="parameters"></a><span data-ttu-id="c2702-106">參數</span><span class="sxs-lookup"><span data-stu-id="c2702-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c2702-107">*pCurrentPointer*</span><span class="sxs-lookup"><span data-stu-id="c2702-107">*pCurrentPointer*</span></span> 
</dt> <dd>

<span data-ttu-id="c2702-108">選擇標頭的指標。</span><span class="sxs-lookup"><span data-stu-id="c2702-108">Pointer to the choice header.</span></span>

</dd> <dt>

<span data-ttu-id="c2702-109">*pTag*</span><span class="sxs-lookup"><span data-stu-id="c2702-109">*pTag*</span></span> 
</dt> <dd>

<span data-ttu-id="c2702-110">傳回之標記的指標。</span><span class="sxs-lookup"><span data-stu-id="c2702-110">Pointer to the returned tag.</span></span>

</dd> <dt>

<span data-ttu-id="c2702-111">*pHeaderLength*</span><span class="sxs-lookup"><span data-stu-id="c2702-111">*pHeaderLength*</span></span> 
</dt> <dd>

<span data-ttu-id="c2702-112">傳回之標頭長度的指標。</span><span class="sxs-lookup"><span data-stu-id="c2702-112">Pointer to the returned header length.</span></span>

</dd> <dt>

<span data-ttu-id="c2702-113">*pDataLength*</span><span class="sxs-lookup"><span data-stu-id="c2702-113">*pDataLength*</span></span> 
</dt> <dd>

<span data-ttu-id="c2702-114">所傳回資料長度的指標。</span><span class="sxs-lookup"><span data-stu-id="c2702-114">Pointer to the returned data length.</span></span>

</dd> <dt>

<span data-ttu-id="c2702-115">*ppNext*</span><span class="sxs-lookup"><span data-stu-id="c2702-115">*ppNext*</span></span> 
</dt> <dd>

<span data-ttu-id="c2702-116">標頭內容的指標。</span><span class="sxs-lookup"><span data-stu-id="c2702-116">Pointer to the header contents.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c2702-117">傳回值</span><span class="sxs-lookup"><span data-stu-id="c2702-117">Return value</span></span>

<span data-ttu-id="c2702-118">如果函式成功 (也就是，找到有效的 BER choice 標頭，) 傳回值為 **TRUE**。</span><span class="sxs-lookup"><span data-stu-id="c2702-118">If the function is successful (that is, a valid BER choice header is found) the return value is **TRUE**.</span></span>

<span data-ttu-id="c2702-119">如果函式不成功，則傳回值為 **FALSE**。</span><span class="sxs-lookup"><span data-stu-id="c2702-119">If the function is unsuccessful, the return value is **FALSE**.</span></span>

## <a name="requirements"></a><span data-ttu-id="c2702-120">規格需求</span><span class="sxs-lookup"><span data-stu-id="c2702-120">Requirements</span></span>



| <span data-ttu-id="c2702-121">需求</span><span class="sxs-lookup"><span data-stu-id="c2702-121">Requirement</span></span> | <span data-ttu-id="c2702-122">值</span><span class="sxs-lookup"><span data-stu-id="c2702-122">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="c2702-123">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="c2702-123">Minimum supported client</span></span><br/> | <span data-ttu-id="c2702-124">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="c2702-124">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                            |
| <span data-ttu-id="c2702-125">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="c2702-125">Minimum supported server</span></span><br/> | <span data-ttu-id="c2702-126">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="c2702-126">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="c2702-127">標頭</span><span class="sxs-lookup"><span data-stu-id="c2702-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="c2702-128"><dt>Netmon</dt></span><span class="sxs-lookup"><span data-stu-id="c2702-128"><dt>Netmon.h</dt></span></span> </dl>   |
| <span data-ttu-id="c2702-129">程式庫</span><span class="sxs-lookup"><span data-stu-id="c2702-129">Library</span></span><br/>                  | <dl> <span data-ttu-id="c2702-130"><dt>剖析器 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="c2702-130"><dt>Parser.lib</dt></span></span> </dl> |
| <span data-ttu-id="c2702-131">DLL</span><span class="sxs-lookup"><span data-stu-id="c2702-131">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c2702-132"><dt>Nmapi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c2702-132"><dt>Nmapi.dll</dt></span></span> </dl>  |



 

 




