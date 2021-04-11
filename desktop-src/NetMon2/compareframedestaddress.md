---
description: CompareFrameDestAddress 函式會比較位址與框架的目的位址。
ms.assetid: 739b3b9f-f989-459d-ac3e-6be7769adc06
title: 'CompareFrameDestAddress 函式 (Netmon. h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CompareFrameDestAddress
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: a9ce0ff776588c06b8fddc34240e9c2170ceca69
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103849130"
---
# <a name="compareframedestaddress-function"></a><span data-ttu-id="52ef8-103">CompareFrameDestAddress 函式</span><span class="sxs-lookup"><span data-stu-id="52ef8-103">CompareFrameDestAddress function</span></span>

<span data-ttu-id="52ef8-104">**CompareFrameDestAddress** 函式會比較位址與框架的目的位址。</span><span class="sxs-lookup"><span data-stu-id="52ef8-104">The **CompareFrameDestAddress** function compares an address to the destination address of a frame.</span></span>

## <a name="syntax"></a><span data-ttu-id="52ef8-105">語法</span><span class="sxs-lookup"><span data-stu-id="52ef8-105">Syntax</span></span>


```C++
BOOL WINAPI CompareFrameDestAddress(
  _In_ HFRAME    hFrame,
  _In_ LPADDRESS lpAddress
);
```



## <a name="parameters"></a><span data-ttu-id="52ef8-106">參數</span><span class="sxs-lookup"><span data-stu-id="52ef8-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="52ef8-107">*hFrame* \[在\]</span><span class="sxs-lookup"><span data-stu-id="52ef8-107">*hFrame* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="52ef8-108">框架的控制碼。</span><span class="sxs-lookup"><span data-stu-id="52ef8-108">Handle to a frame.</span></span>

</dd> <dt>

<span data-ttu-id="52ef8-109">*lpAddress* \[在\]</span><span class="sxs-lookup"><span data-stu-id="52ef8-109">*lpAddress* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="52ef8-110">位址的指標。</span><span class="sxs-lookup"><span data-stu-id="52ef8-110">Pointer to an address.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="52ef8-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="52ef8-111">Return value</span></span>

<span data-ttu-id="52ef8-112">如果位址相同，則傳回值為 **TRUE**。</span><span class="sxs-lookup"><span data-stu-id="52ef8-112">If the addresses are the same, the return value is **TRUE**.</span></span>

<span data-ttu-id="52ef8-113">如果位址不同，則傳回值為 **FALSE**。</span><span class="sxs-lookup"><span data-stu-id="52ef8-113">If the addresses are not the same, the return value is **FALSE**.</span></span>

## <a name="remarks"></a><span data-ttu-id="52ef8-114">備註</span><span class="sxs-lookup"><span data-stu-id="52ef8-114">Remarks</span></span>

<span data-ttu-id="52ef8-115">若要讓 **CompareFrameDestAddress** 函式成功傳回，目的地網址類別型必須符合 *lpAddress* 參數中指定的網址類別型。</span><span class="sxs-lookup"><span data-stu-id="52ef8-115">For the **CompareFrameDestAddress** function to return successfully, the destination address type must match the type of address specified in the *lpAddress* parameter.</span></span>

<span data-ttu-id="52ef8-116">網路監視器提供兩個其他函式： [CompareFrameSourceAddress](compareframesourceaddress.md) 和 [CompareAddresses](compareaddresses.md)，可供您用來比較位址。</span><span class="sxs-lookup"><span data-stu-id="52ef8-116">Network Monitor provides two other functions, [CompareFrameSourceAddress](compareframesourceaddress.md) and [CompareAddresses](compareaddresses.md), which you can use to compare addresses.</span></span> <span data-ttu-id="52ef8-117">**CompareFrameSourceAddress** 函式會比較指定的位址與框架的來源位址，而 **CompareAddress** 函數則會比較兩個指定的位址。</span><span class="sxs-lookup"><span data-stu-id="52ef8-117">The **CompareFrameSourceAddress** function compares a given address to the frame's source address, and the **CompareAddress** function compares two given addresses.</span></span>

<span data-ttu-id="52ef8-118">[*專家*](e.md) 和 [*剖析*](p.md) 器可以呼叫 **CompareFrameDestAddress** 函數。</span><span class="sxs-lookup"><span data-stu-id="52ef8-118">[*Experts*](e.md) and [*parsers*](p.md) can call the **CompareFrameDestAddress** function.</span></span>

## <a name="requirements"></a><span data-ttu-id="52ef8-119">規格需求</span><span class="sxs-lookup"><span data-stu-id="52ef8-119">Requirements</span></span>



| <span data-ttu-id="52ef8-120">需求</span><span class="sxs-lookup"><span data-stu-id="52ef8-120">Requirement</span></span> | <span data-ttu-id="52ef8-121">值</span><span class="sxs-lookup"><span data-stu-id="52ef8-121">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="52ef8-122">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="52ef8-122">Minimum supported client</span></span><br/> | <span data-ttu-id="52ef8-123">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="52ef8-123">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="52ef8-124">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="52ef8-124">Minimum supported server</span></span><br/> | <span data-ttu-id="52ef8-125">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="52ef8-125">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="52ef8-126">標頭</span><span class="sxs-lookup"><span data-stu-id="52ef8-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="52ef8-127"><dt>Netmon</dt></span><span class="sxs-lookup"><span data-stu-id="52ef8-127"><dt>Netmon.h</dt></span></span> </dl>  |
| <span data-ttu-id="52ef8-128">程式庫</span><span class="sxs-lookup"><span data-stu-id="52ef8-128">Library</span></span><br/>                  | <dl> <span data-ttu-id="52ef8-129"><dt>Nmapi .lib</dt></span><span class="sxs-lookup"><span data-stu-id="52ef8-129"><dt>Nmapi.lib</dt></span></span> </dl> |
| <span data-ttu-id="52ef8-130">DLL</span><span class="sxs-lookup"><span data-stu-id="52ef8-130">DLL</span></span><br/>                      | <dl> <span data-ttu-id="52ef8-131"><dt>Nmapi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="52ef8-131"><dt>Nmapi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="52ef8-132">另請參閱</span><span class="sxs-lookup"><span data-stu-id="52ef8-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="52ef8-133">CompareAddresses</span><span class="sxs-lookup"><span data-stu-id="52ef8-133">CompareAddresses</span></span>](compareaddresses.md)
</dt> <dt>

[<span data-ttu-id="52ef8-134">CompareFrameSourceAddress</span><span class="sxs-lookup"><span data-stu-id="52ef8-134">CompareFrameSourceAddress</span></span>](compareframesourceaddress.md)
</dt> </dl>

 

 




