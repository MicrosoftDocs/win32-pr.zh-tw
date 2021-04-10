---
title: 'XTYP_REQUEST 交易 (Ddeml .h) '
description: 用戶端會使用 XTYP \_ 要求交易來向伺服器要求資料。 當用戶端 \_ 在 DdeClientTransaction 函數中指定 XTYP 要求時，動態資料交換 (DDE) server 回呼函式 DdeCallback 會接收此交易。
ms.assetid: e776b995-6a64-4398-9e29-c151f3ef4c1d
keywords:
- XTYP_REQUEST 交易資料交換
topic_type:
- apiref
api_name:
- XTYP_REQUEST
api_location:
- Ddeml.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 32e902c1525a8837f6ace6ef9bceb0607a608cda
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103685614"
---
# <a name="xtyp_request-transaction"></a><span data-ttu-id="9aa9b-105">XTYP \_ 要求交易</span><span class="sxs-lookup"><span data-stu-id="9aa9b-105">XTYP\_REQUEST transaction</span></span>

<span data-ttu-id="9aa9b-106">用戶端會使用 **XTYP \_ 要求** 交易來向伺服器要求資料。</span><span class="sxs-lookup"><span data-stu-id="9aa9b-106">A client uses the **XTYP\_REQUEST** transaction to request data from a server.</span></span> <span data-ttu-id="9aa9b-107">當用戶端在 [**DdeClientTransaction**](/windows/desktop/api/Ddeml/nf-ddeml-ddeclienttransaction)函數中指定 **XTYP \_ 要求** 時，動態資料交換 (DDE) server 回呼函式 [*DdeCallback*](/windows/win32/api/ddeml/nc-ddeml-pfncallback)會接收此交易。</span><span class="sxs-lookup"><span data-stu-id="9aa9b-107">A Dynamic Data Exchange (DDE) server callback function, [*DdeCallback*](/windows/win32/api/ddeml/nc-ddeml-pfncallback), receives this transaction when a client specifies **XTYP\_REQUEST** in the [**DdeClientTransaction**](/windows/desktop/api/Ddeml/nf-ddeml-ddeclienttransaction) function.</span></span>


```C++
#define     XCLASS_DATA              0x2000
#define     XTYP_REQUEST            (0x00B0 | XCLASS_DATA          )
```



## <a name="parameters"></a><span data-ttu-id="9aa9b-108">參數</span><span class="sxs-lookup"><span data-stu-id="9aa9b-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9aa9b-109">*uType*</span><span class="sxs-lookup"><span data-stu-id="9aa9b-109">*uType*</span></span> 
</dt> <dd>

<span data-ttu-id="9aa9b-110">交易類型。</span><span class="sxs-lookup"><span data-stu-id="9aa9b-110">The transaction type.</span></span>

</dd> <dt>

<span data-ttu-id="9aa9b-111">*uFmt*</span><span class="sxs-lookup"><span data-stu-id="9aa9b-111">*uFmt*</span></span> 
</dt> <dd>

<span data-ttu-id="9aa9b-112">伺服器應該將資料提交至用戶端的格式。</span><span class="sxs-lookup"><span data-stu-id="9aa9b-112">The format in which the server should submit data to the client.</span></span>

</dd> <dt>

<span data-ttu-id="9aa9b-113">*hconv*</span><span class="sxs-lookup"><span data-stu-id="9aa9b-113">*hconv*</span></span> 
</dt> <dd>

<span data-ttu-id="9aa9b-114">交談的控制碼。</span><span class="sxs-lookup"><span data-stu-id="9aa9b-114">A handle to the conversation.</span></span>

</dd> <dt>

<span data-ttu-id="9aa9b-115">*hsz1*</span><span class="sxs-lookup"><span data-stu-id="9aa9b-115">*hsz1*</span></span> 
</dt> <dd>

<span data-ttu-id="9aa9b-116">主題名稱的控制碼。</span><span class="sxs-lookup"><span data-stu-id="9aa9b-116">A handle to the topic name.</span></span>

</dd> <dt>

<span data-ttu-id="9aa9b-117">*hsz2*</span><span class="sxs-lookup"><span data-stu-id="9aa9b-117">*hsz2*</span></span> 
</dt> <dd>

<span data-ttu-id="9aa9b-118">專案名稱的控制碼。</span><span class="sxs-lookup"><span data-stu-id="9aa9b-118">A handle to the item name.</span></span>

</dd> <dt>

<span data-ttu-id="9aa9b-119">*hdata*</span><span class="sxs-lookup"><span data-stu-id="9aa9b-119">*hdata*</span></span> 
</dt> <dd>

<span data-ttu-id="9aa9b-120">未使用。</span><span class="sxs-lookup"><span data-stu-id="9aa9b-120">Not used.</span></span>

</dd> <dt>

<span data-ttu-id="9aa9b-121">*dwData1*</span><span class="sxs-lookup"><span data-stu-id="9aa9b-121">*dwData1*</span></span> 
</dt> <dd>

<span data-ttu-id="9aa9b-122">未使用。</span><span class="sxs-lookup"><span data-stu-id="9aa9b-122">Not used.</span></span>

</dd> <dt>

<span data-ttu-id="9aa9b-123">*dwData2*</span><span class="sxs-lookup"><span data-stu-id="9aa9b-123">*dwData2*</span></span> 
</dt> <dd>

<span data-ttu-id="9aa9b-124">未使用。</span><span class="sxs-lookup"><span data-stu-id="9aa9b-124">Not used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9aa9b-125">傳回值</span><span class="sxs-lookup"><span data-stu-id="9aa9b-125">Return value</span></span>

<span data-ttu-id="9aa9b-126">伺服器應該呼叫 [**DdeCreateDataHandle**](/windows/desktop/api/Ddeml/nf-ddeml-ddecreatedatahandle) 函式來建立可識別資料的資料控制碼，然後傳回控制碼。</span><span class="sxs-lookup"><span data-stu-id="9aa9b-126">The server should call the [**DdeCreateDataHandle**](/windows/desktop/api/Ddeml/nf-ddeml-ddecreatedatahandle) function to create a data handle that identifies the data and then return the handle.</span></span> <span data-ttu-id="9aa9b-127">如果伺服器無法完成交易，則應該傳回 **Null** 。</span><span class="sxs-lookup"><span data-stu-id="9aa9b-127">The server should return **NULL** if it is unable to complete the transaction.</span></span> <span data-ttu-id="9aa9b-128">如果伺服器傳回 **Null**，用戶端會收到 DDE \_ FNOTPROCESSED 旗標。</span><span class="sxs-lookup"><span data-stu-id="9aa9b-128">If the server returns **NULL**, the client will receive a DDE\_FNOTPROCESSED flag.</span></span>

## <a name="remarks"></a><span data-ttu-id="9aa9b-129">備註</span><span class="sxs-lookup"><span data-stu-id="9aa9b-129">Remarks</span></span>

<span data-ttu-id="9aa9b-130">如果伺服器應用程式在 [**DdeInitialize**](/windows/desktop/api/Ddeml/nf-ddeml-ddeinitializea)函數中指定了 **CBF \_ FAIL \_ REQUESTS 要求** 旗標，則會篩選此交易。</span><span class="sxs-lookup"><span data-stu-id="9aa9b-130">This transaction is filtered if the server application specified the **CBF\_FAIL\_REQUESTS** flag in the [**DdeInitialize**](/windows/desktop/api/Ddeml/nf-ddeml-ddeinitializea) function.</span></span>

<span data-ttu-id="9aa9b-131">如果回應此交易需要冗長的處理，伺服器可以傳回 CBR 區塊傳回 \_ 碼，以暫停目前交談上的未來交易，然後以非同步方式處理交易。</span><span class="sxs-lookup"><span data-stu-id="9aa9b-131">If responding to this transaction requires lengthy processing, the server can return the CBR\_BLOCK return code to suspend future transactions on the current conversation and then process the transaction asynchronously.</span></span> <span data-ttu-id="9aa9b-132">當伺服器完成且資料已準備好傳遞給用戶端時，伺服器可以呼叫 [**DdeEnableCallback**](/windows/desktop/api/Ddeml/nf-ddeml-ddeenablecallback) 函數來繼續交談。</span><span class="sxs-lookup"><span data-stu-id="9aa9b-132">When the server has finished and the data is ready to pass to the client, the server can call the [**DdeEnableCallback**](/windows/desktop/api/Ddeml/nf-ddeml-ddeenablecallback) function to resume the conversation.</span></span>

## <a name="requirements"></a><span data-ttu-id="9aa9b-133">規格需求</span><span class="sxs-lookup"><span data-stu-id="9aa9b-133">Requirements</span></span>



| <span data-ttu-id="9aa9b-134">需求</span><span class="sxs-lookup"><span data-stu-id="9aa9b-134">Requirement</span></span> | <span data-ttu-id="9aa9b-135">值</span><span class="sxs-lookup"><span data-stu-id="9aa9b-135">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9aa9b-136">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="9aa9b-136">Minimum supported client</span></span><br/> | <span data-ttu-id="9aa9b-137">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="9aa9b-137">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="9aa9b-138">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="9aa9b-138">Minimum supported server</span></span><br/> | <span data-ttu-id="9aa9b-139">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="9aa9b-139">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                   |
| <span data-ttu-id="9aa9b-140">標頭</span><span class="sxs-lookup"><span data-stu-id="9aa9b-140">Header</span></span><br/>                   | <dl> <span data-ttu-id="9aa9b-141"><dt>Ddeml (包含) 的 Windows。h </dt></span><span class="sxs-lookup"><span data-stu-id="9aa9b-141"><dt>Ddeml.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9aa9b-142">另請參閱</span><span class="sxs-lookup"><span data-stu-id="9aa9b-142">See also</span></span>

<dl> <dt>

<span data-ttu-id="9aa9b-143">**參考**</span><span class="sxs-lookup"><span data-stu-id="9aa9b-143">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="9aa9b-144">**DdeClientTransaction**</span><span class="sxs-lookup"><span data-stu-id="9aa9b-144">**DdeClientTransaction**</span></span>](/windows/desktop/api/Ddeml/nf-ddeml-ddeclienttransaction)
</dt> <dt>

[<span data-ttu-id="9aa9b-145">**DdeCreateDataHandle**</span><span class="sxs-lookup"><span data-stu-id="9aa9b-145">**DdeCreateDataHandle**</span></span>](/windows/desktop/api/Ddeml/nf-ddeml-ddecreatedatahandle)
</dt> <dt>

[<span data-ttu-id="9aa9b-146">**DdeEnableCallback**</span><span class="sxs-lookup"><span data-stu-id="9aa9b-146">**DdeEnableCallback**</span></span>](/windows/desktop/api/Ddeml/nf-ddeml-ddeenablecallback)
</dt> <dt>

[<span data-ttu-id="9aa9b-147">**DdeInitialize**</span><span class="sxs-lookup"><span data-stu-id="9aa9b-147">**DdeInitialize**</span></span>](/windows/desktop/api/Ddeml/nf-ddeml-ddeinitializea)
</dt> <dt>

<span data-ttu-id="9aa9b-148">**概念**</span><span class="sxs-lookup"><span data-stu-id="9aa9b-148">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="9aa9b-149">動態資料交換管理程式庫</span><span class="sxs-lookup"><span data-stu-id="9aa9b-149">Dynamic Data Exchange Management Library</span></span>](dynamic-data-exchange-management-library.md)
</dt> </dl>

 

