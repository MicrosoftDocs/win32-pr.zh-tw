---
description: LINEGATHERTERM \_ 位旗標常數描述終止緩衝處理數位收集時所依據的條件。
ms.assetid: 409e1984-e5a4-4636-ab53-5973fe7b78ea
title: 'LINEGATHERTERM_ 的常數 (Tapi) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 968492a584024c7750b417a9fd03b68ac1df42ab
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106987977"
---
# <a name="linegatherterm_-constants"></a><span data-ttu-id="260d2-103">LINEGATHERTERM \_ 常數</span><span class="sxs-lookup"><span data-stu-id="260d2-103">LINEGATHERTERM\_ Constants</span></span>

<span data-ttu-id="260d2-104">**LINEGATHERTERM \_** 位旗標常數描述終止緩衝處理數位收集時所依據的條件。</span><span class="sxs-lookup"><span data-stu-id="260d2-104">The **LINEGATHERTERM\_** bit-flag constants describe the conditions under which buffered digit gathering is terminated.</span></span>

<dl> <dt>

<span data-ttu-id="260d2-105"><span id="LINEGATHERTERM_BUFFERFULL"></span><span id="linegatherterm_bufferfull"></span>**LINEGATHERTERM \_ BUFFERFULL**</span><span class="sxs-lookup"><span data-stu-id="260d2-105"><span id="LINEGATHERTERM_BUFFERFULL"></span><span id="linegatherterm_bufferfull"></span>**LINEGATHERTERM\_BUFFERFULL**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="260d2-106">已收集要求的數位數目。</span><span class="sxs-lookup"><span data-stu-id="260d2-106">The requested number of digits has been gathered.</span></span> <span data-ttu-id="260d2-107">緩衝區已滿。</span><span class="sxs-lookup"><span data-stu-id="260d2-107">The buffer is full.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="260d2-108"><span id="LINEGATHERTERM_CANCEL"></span><span id="linegatherterm_cancel"></span>**LINEGATHERTERM \_ 取消**</span><span class="sxs-lookup"><span data-stu-id="260d2-108"><span id="LINEGATHERTERM_CANCEL"></span><span id="linegatherterm_cancel"></span>**LINEGATHERTERM\_CANCEL**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="260d2-109">此應用程式已由另一個應用程式取消要求，或因為呼叫終止。</span><span class="sxs-lookup"><span data-stu-id="260d2-109">The request was canceled by this application, by another application, or because the call terminated.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="260d2-110"><span id="LINEGATHERTERM_FIRSTTIMEOUT"></span><span id="linegatherterm_firsttimeout"></span>**LINEGATHERTERM \_ FIRSTTIMEOUT**</span><span class="sxs-lookup"><span data-stu-id="260d2-110"><span id="LINEGATHERTERM_FIRSTTIMEOUT"></span><span id="linegatherterm_firsttimeout"></span>**LINEGATHERTERM\_FIRSTTIMEOUT**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="260d2-111">第一個位數 timeout 已過期。</span><span class="sxs-lookup"><span data-stu-id="260d2-111">The first digit timeout expired.</span></span> <span data-ttu-id="260d2-112">緩衝區不包含任何數位。</span><span class="sxs-lookup"><span data-stu-id="260d2-112">The buffer contains no digits.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="260d2-113"><span id="LINEGATHERTERM_INTERTIMEOUT"></span><span id="linegatherterm_intertimeout"></span>**LINEGATHERTERM \_ INTERTIMEOUT**</span><span class="sxs-lookup"><span data-stu-id="260d2-113"><span id="LINEGATHERTERM_INTERTIMEOUT"></span><span id="linegatherterm_intertimeout"></span>**LINEGATHERTERM\_INTERTIMEOUT**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="260d2-114">的位數 timeout 已過期。</span><span class="sxs-lookup"><span data-stu-id="260d2-114">The inter-digit timeout expired.</span></span> <span data-ttu-id="260d2-115">緩衝區包含至少一個數位。</span><span class="sxs-lookup"><span data-stu-id="260d2-115">The buffer contains at least one digit.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="260d2-116"><span id="LINEGATHERTERM_TERMDIGIT"></span><span id="linegatherterm_termdigit"></span>**LINEGATHERTERM \_ TERMDIGIT**</span><span class="sxs-lookup"><span data-stu-id="260d2-116"><span id="LINEGATHERTERM_TERMDIGIT"></span><span id="linegatherterm_termdigit"></span>**LINEGATHERTERM\_TERMDIGIT**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="260d2-117">其中一個終止數位符合接收的數位。</span><span class="sxs-lookup"><span data-stu-id="260d2-117">One of the termination digits matched a received digit.</span></span> <span data-ttu-id="260d2-118">相符的終止數位是緩衝區中的最後一個數位。</span><span class="sxs-lookup"><span data-stu-id="260d2-118">The matched termination digit is the last digit in the buffer.</span></span>


</dt> </dl> </dd> </dl>

## <a name="remarks"></a><span data-ttu-id="260d2-119">備註</span><span class="sxs-lookup"><span data-stu-id="260d2-119">Remarks</span></span>

<span data-ttu-id="260d2-120">無延伸。</span><span class="sxs-lookup"><span data-stu-id="260d2-120">No extensibility.</span></span> <span data-ttu-id="260d2-121">所有32位都是保留的。</span><span class="sxs-lookup"><span data-stu-id="260d2-121">All 32 bits are reserved.</span></span>

## <a name="requirements"></a><span data-ttu-id="260d2-122">規格需求</span><span class="sxs-lookup"><span data-stu-id="260d2-122">Requirements</span></span>



| <span data-ttu-id="260d2-123">需求</span><span class="sxs-lookup"><span data-stu-id="260d2-123">Requirement</span></span> | <span data-ttu-id="260d2-124">值</span><span class="sxs-lookup"><span data-stu-id="260d2-124">Value</span></span> |
|-------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="260d2-125">TAPI 版本</span><span class="sxs-lookup"><span data-stu-id="260d2-125">TAPI version</span></span><br/> | <span data-ttu-id="260d2-126">需要 TAPI 2.0 或更新版本</span><span class="sxs-lookup"><span data-stu-id="260d2-126">Requires TAPI 2.0 or later</span></span><br/>                                             |
| <span data-ttu-id="260d2-127">標頭</span><span class="sxs-lookup"><span data-stu-id="260d2-127">Header</span></span><br/>       | <dl> <span data-ttu-id="260d2-128"><dt>Tapi</dt></span><span class="sxs-lookup"><span data-stu-id="260d2-128"><dt>Tapi.h</dt></span></span> </dl> |



 

 




