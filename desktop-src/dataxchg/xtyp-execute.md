---
title: 'XTYP_EXECUTE 交易 (Ddeml .h) '
description: 用戶端會使用 XTYP \_ EXECUTE transaction 將命令字串傳送至伺服器。 當用戶端 \_ 在 DdeClientTransaction 函數中指定 XTYP EXECUTE 時，動態資料交換 (DDE) server 回呼函式 DdeCallback 會接收此交易。
ms.assetid: 6001eb7d-59c0-49ec-97ce-26132891188c
keywords:
- XTYP_EXECUTE 交易資料交換
topic_type:
- apiref
api_name:
- XTYP_EXECUTE
api_location:
- Ddeml.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9ff08bfa60d07f3b8333f1de808359f77984cbba
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104025351"
---
# <a name="xtyp_execute-transaction"></a><span data-ttu-id="e0b16-105">XTYP \_ 執行交易</span><span class="sxs-lookup"><span data-stu-id="e0b16-105">XTYP\_EXECUTE transaction</span></span>

<span data-ttu-id="e0b16-106">用戶端會使用 **XTYP \_ EXECUTE** transaction 將命令字串傳送至伺服器。</span><span class="sxs-lookup"><span data-stu-id="e0b16-106">A client uses the **XTYP\_EXECUTE** transaction to send a command string to the server.</span></span> <span data-ttu-id="e0b16-107">當用戶端在 [**DdeClientTransaction**](/windows/desktop/api/Ddeml/nf-ddeml-ddeclienttransaction)函數中指定 **XTYP \_ EXECUTE** 時，動態資料交換 (DDE) server 回呼函式 [*DdeCallback*](/windows/win32/api/ddeml/nc-ddeml-pfncallback)會接收此交易。</span><span class="sxs-lookup"><span data-stu-id="e0b16-107">A Dynamic Data Exchange (DDE) server callback function, [*DdeCallback*](/windows/win32/api/ddeml/nc-ddeml-pfncallback), receives this transaction when a client specifies **XTYP\_EXECUTE** in the [**DdeClientTransaction**](/windows/desktop/api/Ddeml/nf-ddeml-ddeclienttransaction) function.</span></span>


```C++
#define     XCLASS_FLAGS             0x4000
#define     XTYP_EXECUTE            (0x0050 | XCLASS_FLAGS         )
```



## <a name="parameters"></a><span data-ttu-id="e0b16-108">參數</span><span class="sxs-lookup"><span data-stu-id="e0b16-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e0b16-109">*uType*</span><span class="sxs-lookup"><span data-stu-id="e0b16-109">*uType*</span></span> 
</dt> <dd>

<span data-ttu-id="e0b16-110">交易類型。</span><span class="sxs-lookup"><span data-stu-id="e0b16-110">The transaction type.</span></span>

</dd> <dt>

<span data-ttu-id="e0b16-111">*uFmt*</span><span class="sxs-lookup"><span data-stu-id="e0b16-111">*uFmt*</span></span> 
</dt> <dd>

<span data-ttu-id="e0b16-112">未使用。</span><span class="sxs-lookup"><span data-stu-id="e0b16-112">Not used.</span></span>

</dd> <dt>

<span data-ttu-id="e0b16-113">*hconv*</span><span class="sxs-lookup"><span data-stu-id="e0b16-113">*hconv*</span></span> 
</dt> <dd>

<span data-ttu-id="e0b16-114">交談的控制碼。</span><span class="sxs-lookup"><span data-stu-id="e0b16-114">A handle to the conversation.</span></span>

</dd> <dt>

<span data-ttu-id="e0b16-115">*hsz1*</span><span class="sxs-lookup"><span data-stu-id="e0b16-115">*hsz1*</span></span> 
</dt> <dd>

<span data-ttu-id="e0b16-116">主題名稱的控制碼。</span><span class="sxs-lookup"><span data-stu-id="e0b16-116">A handle to the topic name.</span></span>

</dd> <dt>

<span data-ttu-id="e0b16-117">*hsz2*</span><span class="sxs-lookup"><span data-stu-id="e0b16-117">*hsz2*</span></span> 
</dt> <dd>

<span data-ttu-id="e0b16-118">未使用。</span><span class="sxs-lookup"><span data-stu-id="e0b16-118">Not used.</span></span>

</dd> <dt>

<span data-ttu-id="e0b16-119">*hdata*</span><span class="sxs-lookup"><span data-stu-id="e0b16-119">*hdata*</span></span> 
</dt> <dd>

<span data-ttu-id="e0b16-120">命令字串的控制碼。</span><span class="sxs-lookup"><span data-stu-id="e0b16-120">A handle to the command string.</span></span>

</dd> <dt>

<span data-ttu-id="e0b16-121">*dwData1*</span><span class="sxs-lookup"><span data-stu-id="e0b16-121">*dwData1*</span></span> 
</dt> <dd>

<span data-ttu-id="e0b16-122">未使用。</span><span class="sxs-lookup"><span data-stu-id="e0b16-122">Not used.</span></span>

</dd> <dt>

<span data-ttu-id="e0b16-123">*dwData2*</span><span class="sxs-lookup"><span data-stu-id="e0b16-123">*dwData2*</span></span> 
</dt> <dd>

<span data-ttu-id="e0b16-124">未使用。</span><span class="sxs-lookup"><span data-stu-id="e0b16-124">Not used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e0b16-125">傳回值</span><span class="sxs-lookup"><span data-stu-id="e0b16-125">Return value</span></span>

<span data-ttu-id="e0b16-126">如果伺服器回呼函式處理此交易，則會傳回 **dde \_ FACK** ，如果它太忙碌而無法處理此交易，則會傳回 dde **\_ FBUSY** ，如果拒絕此交易，則會傳回 dde **\_ FNOTPROCESSED** 。</span><span class="sxs-lookup"><span data-stu-id="e0b16-126">A server callback function should return **DDE\_FACK** if it processes this transaction, **DDE\_FBUSY** if it is too busy to process this transaction, or **DDE\_FNOTPROCESSED** if it rejects this transaction.</span></span>

## <a name="remarks"></a><span data-ttu-id="e0b16-127">備註</span><span class="sxs-lookup"><span data-stu-id="e0b16-127">Remarks</span></span>

<span data-ttu-id="e0b16-128">如果伺服器應用程式在 [**DdeInitialize**](/windows/desktop/api/Ddeml/nf-ddeml-ddeinitializea)函數中指定了 **CBF \_ FAIL \_ 執行** 旗標，則會篩選此交易。</span><span class="sxs-lookup"><span data-stu-id="e0b16-128">This transaction is filtered if the server application specified the **CBF\_FAIL\_EXECUTES** flag in the [**DdeInitialize**](/windows/desktop/api/Ddeml/nf-ddeml-ddeinitializea) function.</span></span>

<span data-ttu-id="e0b16-129">應用程式必須釋放在此交易期間取得的資料控制碼。</span><span class="sxs-lookup"><span data-stu-id="e0b16-129">An application must free the data handle obtained during this transaction.</span></span> <span data-ttu-id="e0b16-130">但是，如果應用程式必須在回呼函數傳回之後處理字串，則應用程式必須複製與資料控制碼相關聯的命令字串。</span><span class="sxs-lookup"><span data-stu-id="e0b16-130">An application must, however, copy the command string associated with the data handle if the application must process the string after the callback function returns.</span></span> <span data-ttu-id="e0b16-131">應用程式可以使用 [**DdeGetData**](/windows/desktop/api/Ddeml/nf-ddeml-ddegetdata) 函數來複製資料。</span><span class="sxs-lookup"><span data-stu-id="e0b16-131">An application can use the [**DdeGetData**](/windows/desktop/api/Ddeml/nf-ddeml-ddegetdata) function to copy the data.</span></span>

<span data-ttu-id="e0b16-132">因為大部分的用戶端應用程式預期伺服器應用程式會以同步方式執行 **XTYP \_ 執行** 交易，所以伺服器應該嘗試從 DDE 回呼函式內或藉由傳回 **CBR \_ 區塊** 傳回碼，來執行 **XTYP \_ 執行** 交易的所有處理。</span><span class="sxs-lookup"><span data-stu-id="e0b16-132">Because most client applications expect a server application to perform an **XTYP\_EXECUTE** transaction synchronously, a server should attempt to perform all processing of the **XTYP\_EXECUTE** transaction either from within the DDE callback function or by returning the **CBR\_BLOCK** return code.</span></span> <span data-ttu-id="e0b16-133">如果 *hdata* 參數是指示伺服器終止的命令，伺服器應該在處理 **XTYP \_ EXECUTE** transaction 之後執行此動作。</span><span class="sxs-lookup"><span data-stu-id="e0b16-133">If the *hdata* parameter is a command that instructs the server to terminate, the server should do so after processing the **XTYP\_EXECUTE** transaction.</span></span>

## <a name="requirements"></a><span data-ttu-id="e0b16-134">規格需求</span><span class="sxs-lookup"><span data-stu-id="e0b16-134">Requirements</span></span>



| <span data-ttu-id="e0b16-135">需求</span><span class="sxs-lookup"><span data-stu-id="e0b16-135">Requirement</span></span> | <span data-ttu-id="e0b16-136">值</span><span class="sxs-lookup"><span data-stu-id="e0b16-136">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e0b16-137">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="e0b16-137">Minimum supported client</span></span><br/> | <span data-ttu-id="e0b16-138">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="e0b16-138">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="e0b16-139">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="e0b16-139">Minimum supported server</span></span><br/> | <span data-ttu-id="e0b16-140">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="e0b16-140">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                   |
| <span data-ttu-id="e0b16-141">標頭</span><span class="sxs-lookup"><span data-stu-id="e0b16-141">Header</span></span><br/>                   | <dl> <span data-ttu-id="e0b16-142"><dt>Ddeml (包含) 的 Windows。h </dt></span><span class="sxs-lookup"><span data-stu-id="e0b16-142"><dt>Ddeml.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e0b16-143">另請參閱</span><span class="sxs-lookup"><span data-stu-id="e0b16-143">See also</span></span>

<dl> <dt>

<span data-ttu-id="e0b16-144">**參考**</span><span class="sxs-lookup"><span data-stu-id="e0b16-144">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="e0b16-145">**DdeClientTransaction**</span><span class="sxs-lookup"><span data-stu-id="e0b16-145">**DdeClientTransaction**</span></span>](/windows/desktop/api/Ddeml/nf-ddeml-ddeclienttransaction)
</dt> <dt>

[<span data-ttu-id="e0b16-146">**DdeGetData**</span><span class="sxs-lookup"><span data-stu-id="e0b16-146">**DdeGetData**</span></span>](/windows/desktop/api/Ddeml/nf-ddeml-ddegetdata)
</dt> <dt>

[<span data-ttu-id="e0b16-147">**DdeInitialize**</span><span class="sxs-lookup"><span data-stu-id="e0b16-147">**DdeInitialize**</span></span>](/windows/desktop/api/Ddeml/nf-ddeml-ddeinitializea)
</dt> <dt>

<span data-ttu-id="e0b16-148">**概念**</span><span class="sxs-lookup"><span data-stu-id="e0b16-148">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="e0b16-149">動態資料交換管理程式庫</span><span class="sxs-lookup"><span data-stu-id="e0b16-149">Dynamic Data Exchange Management Library</span></span>](dynamic-data-exchange-management-library.md)
</dt> </dl>

 

