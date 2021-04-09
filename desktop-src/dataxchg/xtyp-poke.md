---
title: 'XTYP_POKE 交易 (Ddeml .h) '
description: 用戶端會使用 XTYP \_ 請求交易，將未經要求的資料傳送到伺服器。 當用戶端在 DdeClientTransaction 函式中指定 XTYP 時，動態資料交換 (DDE) server 回呼函式 DdeCallback 會接收此交易 \_ 。
ms.assetid: 63c6115e-24f8-4f35-8397-8be63110b21f
keywords:
- XTYP_POKE 交易資料交換
topic_type:
- apiref
api_name:
- XTYP_POKE
api_location:
- Ddeml.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e538f72b7a736ed9be5cf3e1d83e8729f42ef83d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103934287"
---
# <a name="xtyp_poke-transaction"></a><span data-ttu-id="cd29b-105">XTYP \_ 記錄</span><span class="sxs-lookup"><span data-stu-id="cd29b-105">XTYP\_POKE transaction</span></span>

<span data-ttu-id="cd29b-106">用戶端會使用 **XTYP \_** 請求交易，將未經要求的資料傳送到伺服器。</span><span class="sxs-lookup"><span data-stu-id="cd29b-106">A client uses the **XTYP\_POKE** transaction to send unsolicited data to the server.</span></span> <span data-ttu-id="cd29b-107">當用戶端在 [**DdeClientTransaction**](/windows/desktop/api/Ddeml/nf-ddeml-ddeclienttransaction)函式中指定 **XTYP \_** 時，動態資料交換 (DDE) server 回呼函式 [*DdeCallback*](/windows/win32/api/ddeml/nc-ddeml-pfncallback)會接收此交易。</span><span class="sxs-lookup"><span data-stu-id="cd29b-107">A Dynamic Data Exchange (DDE) server callback function, [*DdeCallback*](/windows/win32/api/ddeml/nc-ddeml-pfncallback), receives this transaction when a client specifies **XTYP\_POKE** in the [**DdeClientTransaction**](/windows/desktop/api/Ddeml/nf-ddeml-ddeclienttransaction) function.</span></span>


```C++
#define     XCLASS_FLAGS             0x4000
#define     XTYP_POKE               (0x0090 | XCLASS_FLAGS         )
```



## <a name="parameters"></a><span data-ttu-id="cd29b-108">參數</span><span class="sxs-lookup"><span data-stu-id="cd29b-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cd29b-109">*uType*</span><span class="sxs-lookup"><span data-stu-id="cd29b-109">*uType*</span></span> 
</dt> <dd>

<span data-ttu-id="cd29b-110">交易類型。</span><span class="sxs-lookup"><span data-stu-id="cd29b-110">The transaction type.</span></span>

</dd> <dt>

<span data-ttu-id="cd29b-111">*uFmt*</span><span class="sxs-lookup"><span data-stu-id="cd29b-111">*uFmt*</span></span> 
</dt> <dd>

<span data-ttu-id="cd29b-112">從伺服器傳送的資料格式。</span><span class="sxs-lookup"><span data-stu-id="cd29b-112">The format of the data sent from the server.</span></span>

</dd> <dt>

<span data-ttu-id="cd29b-113">*hconv*</span><span class="sxs-lookup"><span data-stu-id="cd29b-113">*hconv*</span></span> 
</dt> <dd>

<span data-ttu-id="cd29b-114">交談的控制碼。</span><span class="sxs-lookup"><span data-stu-id="cd29b-114">A handle to the conversation.</span></span>

</dd> <dt>

<span data-ttu-id="cd29b-115">*hsz1*</span><span class="sxs-lookup"><span data-stu-id="cd29b-115">*hsz1*</span></span> 
</dt> <dd>

<span data-ttu-id="cd29b-116">主題名稱的控制碼。</span><span class="sxs-lookup"><span data-stu-id="cd29b-116">A handle to the topic name.</span></span>

</dd> <dt>

<span data-ttu-id="cd29b-117">*hsz2*</span><span class="sxs-lookup"><span data-stu-id="cd29b-117">*hsz2*</span></span> 
</dt> <dd>

<span data-ttu-id="cd29b-118">專案名稱的控制碼。</span><span class="sxs-lookup"><span data-stu-id="cd29b-118">A handle to the item name.</span></span>

</dd> <dt>

<span data-ttu-id="cd29b-119">*hdata*</span><span class="sxs-lookup"><span data-stu-id="cd29b-119">*hdata*</span></span> 
</dt> <dd>

<span data-ttu-id="cd29b-120">用戶端傳送至伺服器之資料的控制碼。</span><span class="sxs-lookup"><span data-stu-id="cd29b-120">A handle to the data that the client is sending to the server.</span></span>

</dd> <dt>

<span data-ttu-id="cd29b-121">*dwData1*</span><span class="sxs-lookup"><span data-stu-id="cd29b-121">*dwData1*</span></span> 
</dt> <dd>

<span data-ttu-id="cd29b-122">未使用。</span><span class="sxs-lookup"><span data-stu-id="cd29b-122">Not used.</span></span>

</dd> <dt>

<span data-ttu-id="cd29b-123">*dwData2*</span><span class="sxs-lookup"><span data-stu-id="cd29b-123">*dwData2*</span></span> 
</dt> <dd>

<span data-ttu-id="cd29b-124">未使用。</span><span class="sxs-lookup"><span data-stu-id="cd29b-124">Not used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="cd29b-125">傳回值</span><span class="sxs-lookup"><span data-stu-id="cd29b-125">Return value</span></span>

<span data-ttu-id="cd29b-126">伺服器回呼函數應該會傳回 **dde \_ FACK** 旗標（如果它處理此交易）、 **dde \_ FBUSY** 旗標（如果它太忙碌而無法處理此交易）或 **dde \_ FNOTPROCESSED** 旗標（如果它拒絕此交易）。</span><span class="sxs-lookup"><span data-stu-id="cd29b-126">A server callback function should return the **DDE\_FACK** flag if it processes this transaction, the **DDE\_FBUSY** flag if it is too busy to process this transaction, or the **DDE\_FNOTPROCESSED** flag if it rejects this transaction.</span></span>

## <a name="remarks"></a><span data-ttu-id="cd29b-127">備註</span><span class="sxs-lookup"><span data-stu-id="cd29b-127">Remarks</span></span>

<span data-ttu-id="cd29b-128">如果伺服器應用程式在 [**DdeInitialize**](/windows/desktop/api/Ddeml/nf-ddeml-ddeinitializea)函數中指定了 **CBF \_ FAIL \_ 友善** 旗標，則會篩選此交易。</span><span class="sxs-lookup"><span data-stu-id="cd29b-128">This transaction is filtered if the server application specified the **CBF\_FAIL\_POKES** flag in the [**DdeInitialize**](/windows/desktop/api/Ddeml/nf-ddeml-ddeinitializea) function.</span></span>

## <a name="requirements"></a><span data-ttu-id="cd29b-129">規格需求</span><span class="sxs-lookup"><span data-stu-id="cd29b-129">Requirements</span></span>



| <span data-ttu-id="cd29b-130">需求</span><span class="sxs-lookup"><span data-stu-id="cd29b-130">Requirement</span></span> | <span data-ttu-id="cd29b-131">值</span><span class="sxs-lookup"><span data-stu-id="cd29b-131">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="cd29b-132">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="cd29b-132">Minimum supported client</span></span><br/> | <span data-ttu-id="cd29b-133">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="cd29b-133">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="cd29b-134">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="cd29b-134">Minimum supported server</span></span><br/> | <span data-ttu-id="cd29b-135">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="cd29b-135">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                   |
| <span data-ttu-id="cd29b-136">標頭</span><span class="sxs-lookup"><span data-stu-id="cd29b-136">Header</span></span><br/>                   | <dl> <span data-ttu-id="cd29b-137"><dt>Ddeml (包含) 的 Windows。h </dt></span><span class="sxs-lookup"><span data-stu-id="cd29b-137"><dt>Ddeml.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cd29b-138">另請參閱</span><span class="sxs-lookup"><span data-stu-id="cd29b-138">See also</span></span>

<dl> <dt>

<span data-ttu-id="cd29b-139">**參考**</span><span class="sxs-lookup"><span data-stu-id="cd29b-139">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="cd29b-140">**DdeClientTransaction**</span><span class="sxs-lookup"><span data-stu-id="cd29b-140">**DdeClientTransaction**</span></span>](/windows/desktop/api/Ddeml/nf-ddeml-ddeclienttransaction)
</dt> <dt>

[<span data-ttu-id="cd29b-141">**DdeInitialize**</span><span class="sxs-lookup"><span data-stu-id="cd29b-141">**DdeInitialize**</span></span>](/windows/desktop/api/Ddeml/nf-ddeml-ddeinitializea)
</dt> <dt>

<span data-ttu-id="cd29b-142">**概念**</span><span class="sxs-lookup"><span data-stu-id="cd29b-142">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="cd29b-143">動態資料交換管理程式庫</span><span class="sxs-lookup"><span data-stu-id="cd29b-143">Dynamic Data Exchange Management Library</span></span>](dynamic-data-exchange-management-library.md)
</dt> </dl>

 

