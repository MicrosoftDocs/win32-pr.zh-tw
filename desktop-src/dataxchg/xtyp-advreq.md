---
title: 'XTYP_ADVREQ 交易 (Ddeml .h) '
description: XTYP \_ ADVREQ transaction 會通知伺服器，指定的主題名稱和專案名稱組上的建議交易未完成，而且對應至主題名稱和專案名稱組的資料已經變更。
ms.assetid: 9bd43e61-cbd6-4d53-bab3-90e85819b16b
keywords:
- XTYP_ADVREQ 交易資料交換
topic_type:
- apiref
api_name:
- XTYP_ADVREQ
api_location:
- Ddeml.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2884e838268342ab10c556c6ae3cfc8349ed5d2c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104384782"
---
# <a name="xtyp_advreq-transaction"></a><span data-ttu-id="36ad1-104">XTYP \_ ADVREQ 交易</span><span class="sxs-lookup"><span data-stu-id="36ad1-104">XTYP\_ADVREQ transaction</span></span>

<span data-ttu-id="36ad1-105">**XTYP \_ ADVREQ** transaction 會通知伺服器，指定的主題名稱和專案名稱組上的建議交易未完成，而且對應至主題名稱和專案名稱組的資料已經變更。</span><span class="sxs-lookup"><span data-stu-id="36ad1-105">The **XTYP\_ADVREQ** transaction informs the server that an advise transaction is outstanding on the specified topic name and item name pair and that data corresponding to the topic name and item name pair has changed.</span></span> <span data-ttu-id="36ad1-106">當伺服器呼叫 [**DdePostAdvise**](/windows/desktop/api/Ddeml/nf-ddeml-ddepostadvise)函式之後，系統會將此交易傳送給動態資料交換 (DDE) 回呼函數 [*DdeCallback*](/windows/win32/api/ddeml/nc-ddeml-pfncallback)。</span><span class="sxs-lookup"><span data-stu-id="36ad1-106">The system sends this transaction to the Dynamic Data Exchange (DDE) callback function, [*DdeCallback*](/windows/win32/api/ddeml/nc-ddeml-pfncallback), after the server calls the [**DdePostAdvise**](/windows/desktop/api/Ddeml/nf-ddeml-ddepostadvise) function.</span></span>


```C++
#define     XCLASS_DATA              0x2000
#define     XTYPF_NOBLOCK            0x0002
#define     XTYP_ADVREQ             (0x0020 | XCLASS_DATA | XTYPF_NOBLOCK )
```



## <a name="parameters"></a><span data-ttu-id="36ad1-107">參數</span><span class="sxs-lookup"><span data-stu-id="36ad1-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="36ad1-108">*uType*</span><span class="sxs-lookup"><span data-stu-id="36ad1-108">*uType*</span></span> 
</dt> <dd>

<span data-ttu-id="36ad1-109">交易類型。</span><span class="sxs-lookup"><span data-stu-id="36ad1-109">The transaction type.</span></span>

</dd> <dt>

<span data-ttu-id="36ad1-110">*uFmt*</span><span class="sxs-lookup"><span data-stu-id="36ad1-110">*uFmt*</span></span> 
</dt> <dd>

<span data-ttu-id="36ad1-111">應將資料提交至用戶端的格式。</span><span class="sxs-lookup"><span data-stu-id="36ad1-111">The format in which the data should be submitted to the client.</span></span>

</dd> <dt>

<span data-ttu-id="36ad1-112">*hconv*</span><span class="sxs-lookup"><span data-stu-id="36ad1-112">*hconv*</span></span> 
</dt> <dd>

<span data-ttu-id="36ad1-113">交談的控制碼。</span><span class="sxs-lookup"><span data-stu-id="36ad1-113">A handle to the conversation.</span></span>

</dd> <dt>

<span data-ttu-id="36ad1-114">*hsz1*</span><span class="sxs-lookup"><span data-stu-id="36ad1-114">*hsz1*</span></span> 
</dt> <dd>

<span data-ttu-id="36ad1-115">主題名稱的控制碼。</span><span class="sxs-lookup"><span data-stu-id="36ad1-115">A handle to the topic name.</span></span>

</dd> <dt>

<span data-ttu-id="36ad1-116">*hsz2*</span><span class="sxs-lookup"><span data-stu-id="36ad1-116">*hsz2*</span></span> 
</dt> <dd>

<span data-ttu-id="36ad1-117">已變更之專案名稱的控制碼。</span><span class="sxs-lookup"><span data-stu-id="36ad1-117">A handle to the item name that has changed.</span></span>

</dd> <dt>

<span data-ttu-id="36ad1-118">*hdata*</span><span class="sxs-lookup"><span data-stu-id="36ad1-118">*hdata*</span></span> 
</dt> <dd>

<span data-ttu-id="36ad1-119">未使用。</span><span class="sxs-lookup"><span data-stu-id="36ad1-119">Not used.</span></span>

</dd> <dt>

<span data-ttu-id="36ad1-120">*dwData1*</span><span class="sxs-lookup"><span data-stu-id="36ad1-120">*dwData1*</span></span> 
</dt> <dd>

<span data-ttu-id="36ad1-121">在低序位單字中， **XTYP \_ ADVREQ** 交易的計數，這些交易仍會在目前呼叫 [**DdePostAdvise**](/windows/desktop/api/Ddeml/nf-ddeml-ddepostadvise) 函式的內容中設定的相同主題、專案和格式名稱上進行處理。</span><span class="sxs-lookup"><span data-stu-id="36ad1-121">The count, in the low-order word, of **XTYP\_ADVREQ** transactions that remain to be processed on the same topic, item, and format name set within the context of the current call to the [**DdePostAdvise**](/windows/desktop/api/Ddeml/nf-ddeml-ddepostadvise) function.</span></span> <span data-ttu-id="36ad1-122">如果目前的 **XTYP \_ ADVREQ** 交易是最後一個交易，則此計數為零。</span><span class="sxs-lookup"><span data-stu-id="36ad1-122">The count is zero if the current **XTYP\_ADVREQ** transaction is the last one.</span></span> <span data-ttu-id="36ad1-123">伺服器可以使用此計數來判斷是否要建立建議資料的 **HDATA \_ APPOWNED** 資料控制碼。</span><span class="sxs-lookup"><span data-stu-id="36ad1-123">A server can use this count to determine whether to create an **HDATA\_APPOWNED** data handle to the advise data.</span></span>

<span data-ttu-id="36ad1-124">如果 DDEML 發出 **XTYP \_ ADVREQ** 交易，則低序位單字會設定為 **CADV \_ LATEACK** ，因為 \_ 來自伺服器所 outrun 的用戶端會收到延遲抵達的 DDE ACK 訊息。</span><span class="sxs-lookup"><span data-stu-id="36ad1-124">The low-order word is set to **CADV\_LATEACK** if the DDEML issued the **XTYP\_ADVREQ** transaction because of a late-arriving DDE\_ACK message from a client being outrun by the server.</span></span>

<span data-ttu-id="36ad1-125">未使用高序位字組。</span><span class="sxs-lookup"><span data-stu-id="36ad1-125">The high-order word is not used.</span></span>

</dd> <dt>

<span data-ttu-id="36ad1-126">*dwData2*</span><span class="sxs-lookup"><span data-stu-id="36ad1-126">*dwData2*</span></span> 
</dt> <dd>

<span data-ttu-id="36ad1-127">未使用。</span><span class="sxs-lookup"><span data-stu-id="36ad1-127">Not used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="36ad1-128">傳回值</span><span class="sxs-lookup"><span data-stu-id="36ad1-128">Return value</span></span>

<span data-ttu-id="36ad1-129">伺服器應該先呼叫 [**DdeCreateDataHandle**](/windows/desktop/api/Ddeml/nf-ddeml-ddecreatedatahandle) 函數來建立資料控制碼，以識別已變更的資料，然後傳回控制碼。</span><span class="sxs-lookup"><span data-stu-id="36ad1-129">The server should first call the [**DdeCreateDataHandle**](/windows/desktop/api/Ddeml/nf-ddeml-ddecreatedatahandle) function to create a data handle that identifies the changed data and then return the handle.</span></span> <span data-ttu-id="36ad1-130">如果伺服器無法完成交易，則應該傳回 **Null** 。</span><span class="sxs-lookup"><span data-stu-id="36ad1-130">The server should return **NULL** if it is unable to complete the transaction.</span></span>

## <a name="remarks"></a><span data-ttu-id="36ad1-131">備註</span><span class="sxs-lookup"><span data-stu-id="36ad1-131">Remarks</span></span>

<span data-ttu-id="36ad1-132">伺服器無法封鎖此交易類型;會忽略 **CBR \_ 區塊** 傳回碼。</span><span class="sxs-lookup"><span data-stu-id="36ad1-132">A server cannot block this transaction type; the **CBR\_BLOCK** return code is ignored.</span></span>

## <a name="requirements"></a><span data-ttu-id="36ad1-133">規格需求</span><span class="sxs-lookup"><span data-stu-id="36ad1-133">Requirements</span></span>



| <span data-ttu-id="36ad1-134">需求</span><span class="sxs-lookup"><span data-stu-id="36ad1-134">Requirement</span></span> | <span data-ttu-id="36ad1-135">值</span><span class="sxs-lookup"><span data-stu-id="36ad1-135">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="36ad1-136">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="36ad1-136">Minimum supported client</span></span><br/> | <span data-ttu-id="36ad1-137">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="36ad1-137">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="36ad1-138">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="36ad1-138">Minimum supported server</span></span><br/> | <span data-ttu-id="36ad1-139">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="36ad1-139">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                   |
| <span data-ttu-id="36ad1-140">標頭</span><span class="sxs-lookup"><span data-stu-id="36ad1-140">Header</span></span><br/>                   | <dl> <span data-ttu-id="36ad1-141"><dt>Ddeml (包含) 的 Windows。h </dt></span><span class="sxs-lookup"><span data-stu-id="36ad1-141"><dt>Ddeml.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="36ad1-142">另請參閱</span><span class="sxs-lookup"><span data-stu-id="36ad1-142">See also</span></span>

<dl> <dt>

<span data-ttu-id="36ad1-143">**參考**</span><span class="sxs-lookup"><span data-stu-id="36ad1-143">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="36ad1-144">**DdeCreateDataHandle**</span><span class="sxs-lookup"><span data-stu-id="36ad1-144">**DdeCreateDataHandle**</span></span>](/windows/desktop/api/Ddeml/nf-ddeml-ddecreatedatahandle)
</dt> <dt>

[<span data-ttu-id="36ad1-145">**DdeInitialize**</span><span class="sxs-lookup"><span data-stu-id="36ad1-145">**DdeInitialize**</span></span>](/windows/desktop/api/Ddeml/nf-ddeml-ddeinitializea)
</dt> <dt>

[<span data-ttu-id="36ad1-146">**DdePostAdvise**</span><span class="sxs-lookup"><span data-stu-id="36ad1-146">**DdePostAdvise**</span></span>](/windows/desktop/api/Ddeml/nf-ddeml-ddepostadvise)
</dt> <dt>

<span data-ttu-id="36ad1-147">**概念**</span><span class="sxs-lookup"><span data-stu-id="36ad1-147">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="36ad1-148">動態資料交換管理程式庫</span><span class="sxs-lookup"><span data-stu-id="36ad1-148">Dynamic Data Exchange Management Library</span></span>](dynamic-data-exchange-management-library.md)
</dt> </dl>

 

