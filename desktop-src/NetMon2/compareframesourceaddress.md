---
description: CompareFrameSourceAddress 函式會比較位址與框架的來源位址。
ms.assetid: 7221c0cc-d6c1-4ec9-bf11-3ba1fefb35da
title: 'CompareFrameSourceAddress 函式 (Netmon. h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CompareFrameSourceAddress
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: 4a100273c37e25a7b1deba86ed2704886dbfccc7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104194083"
---
# <a name="compareframesourceaddress-function"></a><span data-ttu-id="c2d85-103">CompareFrameSourceAddress 函式</span><span class="sxs-lookup"><span data-stu-id="c2d85-103">CompareFrameSourceAddress function</span></span>

<span data-ttu-id="c2d85-104">**CompareFrameSourceAddress** 函式會比較位址與框架的來源位址。</span><span class="sxs-lookup"><span data-stu-id="c2d85-104">The **CompareFrameSourceAddress** function compares an address to the source address of a frame.</span></span>

## <a name="syntax"></a><span data-ttu-id="c2d85-105">語法</span><span class="sxs-lookup"><span data-stu-id="c2d85-105">Syntax</span></span>


```C++
BOOL WINAPI CompareFrameSourceAddress(
  _In_ HFRAME    hFrame,
  _In_ LPADDRESS lpAddress
);
```



## <a name="parameters"></a><span data-ttu-id="c2d85-106">參數</span><span class="sxs-lookup"><span data-stu-id="c2d85-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c2d85-107">*hFrame* \[在\]</span><span class="sxs-lookup"><span data-stu-id="c2d85-107">*hFrame* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c2d85-108">框架的控制碼。</span><span class="sxs-lookup"><span data-stu-id="c2d85-108">Handle to a frame.</span></span>

</dd> <dt>

<span data-ttu-id="c2d85-109">*lpAddress* \[在\]</span><span class="sxs-lookup"><span data-stu-id="c2d85-109">*lpAddress* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c2d85-110">位址的指標。</span><span class="sxs-lookup"><span data-stu-id="c2d85-110">Pointer to an address.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c2d85-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="c2d85-111">Return value</span></span>

<span data-ttu-id="c2d85-112">如果位址相同，則傳回值為 **TRUE**。</span><span class="sxs-lookup"><span data-stu-id="c2d85-112">If the addresses are the same, the return value is **TRUE**.</span></span>

<span data-ttu-id="c2d85-113">如果位址不同，則傳回值為 **FALSE**。</span><span class="sxs-lookup"><span data-stu-id="c2d85-113">If the addresses are not the same, the return value is **FALSE**.</span></span>

## <a name="remarks"></a><span data-ttu-id="c2d85-114">備註</span><span class="sxs-lookup"><span data-stu-id="c2d85-114">Remarks</span></span>

<span data-ttu-id="c2d85-115">若要讓 **CompareFrameSourceAddress** 函式成功，來源網址類別型必須符合 *lpAddress* 參數中指定的網址類別型。</span><span class="sxs-lookup"><span data-stu-id="c2d85-115">For the **CompareFrameSourceAddress** function to succeed, the source address type must match the type of address specified in the *lpAddress* parameter.</span></span>

<span data-ttu-id="c2d85-116">網路監視器提供兩個其他函數來比較位址： [CompareFrameDestAddress](compareframedestaddress.md) 和 [CompareAddresses](compareaddresses.md)。</span><span class="sxs-lookup"><span data-stu-id="c2d85-116">Network Monitor provides two other functions for comparing addresses: [CompareFrameDestAddress](compareframedestaddress.md) and [CompareAddresses](compareaddresses.md).</span></span> <span data-ttu-id="c2d85-117">**CompareFrameDestAddress** 函式會比較指定的位址與框架的目的地位址，而 **CompareAddress** 函式會比較兩個指定的位址。</span><span class="sxs-lookup"><span data-stu-id="c2d85-117">The **CompareFrameDestAddress** function compares a given address to the frame's destination address, and the **CompareAddress** function compares two given addresses.</span></span>

<span data-ttu-id="c2d85-118">[*專家*](e.md) 和 [*剖析*](p.md) 器可以呼叫 **CompareFrameSourceAddress** 函數。</span><span class="sxs-lookup"><span data-stu-id="c2d85-118">[*Experts*](e.md) and [*parsers*](p.md) can call the **CompareFrameSourceAddress** function.</span></span>

## <a name="requirements"></a><span data-ttu-id="c2d85-119">規格需求</span><span class="sxs-lookup"><span data-stu-id="c2d85-119">Requirements</span></span>



| <span data-ttu-id="c2d85-120">需求</span><span class="sxs-lookup"><span data-stu-id="c2d85-120">Requirement</span></span> | <span data-ttu-id="c2d85-121">值</span><span class="sxs-lookup"><span data-stu-id="c2d85-121">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="c2d85-122">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="c2d85-122">Minimum supported client</span></span><br/> | <span data-ttu-id="c2d85-123">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="c2d85-123">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="c2d85-124">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="c2d85-124">Minimum supported server</span></span><br/> | <span data-ttu-id="c2d85-125">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="c2d85-125">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="c2d85-126">標頭</span><span class="sxs-lookup"><span data-stu-id="c2d85-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="c2d85-127"><dt>Netmon</dt></span><span class="sxs-lookup"><span data-stu-id="c2d85-127"><dt>Netmon.h</dt></span></span> </dl>  |
| <span data-ttu-id="c2d85-128">程式庫</span><span class="sxs-lookup"><span data-stu-id="c2d85-128">Library</span></span><br/>                  | <dl> <span data-ttu-id="c2d85-129"><dt>Nmapi .lib</dt></span><span class="sxs-lookup"><span data-stu-id="c2d85-129"><dt>Nmapi.lib</dt></span></span> </dl> |
| <span data-ttu-id="c2d85-130">DLL</span><span class="sxs-lookup"><span data-stu-id="c2d85-130">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c2d85-131"><dt>Nmapi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c2d85-131"><dt>Nmapi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c2d85-132">另請參閱</span><span class="sxs-lookup"><span data-stu-id="c2d85-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c2d85-133">CompareAddresses</span><span class="sxs-lookup"><span data-stu-id="c2d85-133">CompareAddresses</span></span>](compareaddresses.md)
</dt> <dt>

[<span data-ttu-id="c2d85-134">CompareFrameDestAddress</span><span class="sxs-lookup"><span data-stu-id="c2d85-134">CompareFrameDestAddress</span></span>](compareframedestaddress.md)
</dt> </dl>

 

 




