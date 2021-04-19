---
description: GetPreviousProtocolOffsetByName 函式會傳回指定通訊協定的上一個實例。
ms.assetid: 94f80776-564f-4089-9e3a-fdf38d9dfe8a
title: 'GetPreviousProtocolOffsetByName 函式 (Netmon. h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetPreviousProtocolOffsetByName
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: 2720d309224def5f368babf4f9ace85955907347
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106970371"
---
# <a name="getpreviousprotocoloffsetbyname-function"></a><span data-ttu-id="b8946-103">GetPreviousProtocolOffsetByName 函式</span><span class="sxs-lookup"><span data-stu-id="b8946-103">GetPreviousProtocolOffsetByName function</span></span>

<span data-ttu-id="b8946-104">**GetPreviousProtocolOffsetByName** 函式會傳回指定通訊協定的上一個實例。</span><span class="sxs-lookup"><span data-stu-id="b8946-104">The **GetPreviousProtocolOffsetByName** function returns the previous instance of a given protocol.</span></span>

## <a name="syntax"></a><span data-ttu-id="b8946-105">語法</span><span class="sxs-lookup"><span data-stu-id="b8946-105">Syntax</span></span>


```C++
DWORD WINAPI GetPreviousProtocolOffsetByName(
  _In_  HFRAME hFrame,
  _In_  DWORD  dwStartOffset,
  _In_  LPSTR  szProtocolName,
  _Out_ DWORD  *pdwPreviousOffset
);
```



## <a name="parameters"></a><span data-ttu-id="b8946-106">參數</span><span class="sxs-lookup"><span data-stu-id="b8946-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b8946-107">*hFrame* \[在\]</span><span class="sxs-lookup"><span data-stu-id="b8946-107">*hFrame* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b8946-108">框架的控制碼。</span><span class="sxs-lookup"><span data-stu-id="b8946-108">Handle to the frame.</span></span>

</dd> <dt>

<span data-ttu-id="b8946-109">*dwStartOffset* \[在\]</span><span class="sxs-lookup"><span data-stu-id="b8946-109">*dwStartOffset* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b8946-110">框架中的位移。</span><span class="sxs-lookup"><span data-stu-id="b8946-110">Offset in the frame.</span></span>

</dd> <dt>

<span data-ttu-id="b8946-111">*szProtocolName* \[在\]</span><span class="sxs-lookup"><span data-stu-id="b8946-111">*szProtocolName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b8946-112">您要搜尋的通訊協定名稱。</span><span class="sxs-lookup"><span data-stu-id="b8946-112">Name of the protocol you want to search for.</span></span>

</dd> <dt>

<span data-ttu-id="b8946-113">*pdwPreviousOffset* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="b8946-113">*pdwPreviousOffset* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="b8946-114">**DWORD** 的指標，其中包含前一個通訊協定的位移 (if 函數是否成功) 。</span><span class="sxs-lookup"><span data-stu-id="b8946-114">Pointer to a **DWORD** that contains the offset to the previous protocol (if the function succeeds).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b8946-115">傳回值</span><span class="sxs-lookup"><span data-stu-id="b8946-115">Return value</span></span>

<span data-ttu-id="b8946-116">如果函式成功，則傳回值為 NMERR \_ SUCCESS。</span><span class="sxs-lookup"><span data-stu-id="b8946-116">If the function is successful, the return value is NMERR\_SUCCESS.</span></span>

<span data-ttu-id="b8946-117">如果函式不成功，則傳回值為「找不到 NMERR \_ 通訊協定」 \_ \_ 。</span><span class="sxs-lookup"><span data-stu-id="b8946-117">If the function is unsuccessful, the return value is NMERR\_PROTOCOL\_NOT\_FOUND.</span></span>

## <a name="remarks"></a><span data-ttu-id="b8946-118">備註</span><span class="sxs-lookup"><span data-stu-id="b8946-118">Remarks</span></span>

<span data-ttu-id="b8946-119">[*專家*](e.md) 和 [*剖析*](p.md) 器可以呼叫 **GetPreviousProtocolOffsetByName**。</span><span class="sxs-lookup"><span data-stu-id="b8946-119">[*Experts*](e.md) and [*parsers*](p.md) can call the **GetPreviousProtocolOffsetByName**.</span></span>

## <a name="requirements"></a><span data-ttu-id="b8946-120">規格需求</span><span class="sxs-lookup"><span data-stu-id="b8946-120">Requirements</span></span>



| <span data-ttu-id="b8946-121">需求</span><span class="sxs-lookup"><span data-stu-id="b8946-121">Requirement</span></span> | <span data-ttu-id="b8946-122">值</span><span class="sxs-lookup"><span data-stu-id="b8946-122">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="b8946-123">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="b8946-123">Minimum supported client</span></span><br/> | <span data-ttu-id="b8946-124">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="b8946-124">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="b8946-125">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="b8946-125">Minimum supported server</span></span><br/> | <span data-ttu-id="b8946-126">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="b8946-126">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="b8946-127">標頭</span><span class="sxs-lookup"><span data-stu-id="b8946-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="b8946-128"><dt>Netmon</dt></span><span class="sxs-lookup"><span data-stu-id="b8946-128"><dt>Netmon.h</dt></span></span> </dl>  |
| <span data-ttu-id="b8946-129">程式庫</span><span class="sxs-lookup"><span data-stu-id="b8946-129">Library</span></span><br/>                  | <dl> <span data-ttu-id="b8946-130"><dt>Nmapi .lib</dt></span><span class="sxs-lookup"><span data-stu-id="b8946-130"><dt>Nmapi.lib</dt></span></span> </dl> |
| <span data-ttu-id="b8946-131">DLL</span><span class="sxs-lookup"><span data-stu-id="b8946-131">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b8946-132"><dt>Nmapi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b8946-132"><dt>Nmapi.dll</dt></span></span> </dl> |



 

 




