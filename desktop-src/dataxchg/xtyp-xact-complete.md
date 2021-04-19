---
title: 'XTYP_XACT_COMPLETE 交易 (Ddeml .h) '
description: '\_ \_ 當非同步交易（由 DdeClientTransaction 函式的呼叫所起始）完成時，動態資料交換 (DDE) 用戶端回呼函式 DdeCallback 會接收 XTYP 的交易完成交易。'
ms.assetid: d34a6fab-0e3c-44fe-b25f-7011228fe261
keywords:
- XTYP_XACT_COMPLETE 交易資料交換
topic_type:
- apiref
api_name:
- XTYP_XACT_COMPLETE
api_location:
- Ddeml.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 03a81869270a771836c4dd5c1a6b300f148ea13d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106969762"
---
# <a name="xtyp_xact_complete-transaction"></a><span data-ttu-id="6be56-104">XTYP \_ \_ 交易完成交易</span><span class="sxs-lookup"><span data-stu-id="6be56-104">XTYP\_XACT\_COMPLETE transaction</span></span>

<span data-ttu-id="6be56-105">當非同步交易（由 [**DdeClientTransaction**](/windows/desktop/api/Ddeml/nf-ddeml-ddeclienttransaction)函式的呼叫所起始）完成時，動態資料交換 (DDE) 用戶端回呼函式 [*DdeCallback*](/windows/win32/api/ddeml/nc-ddeml-pfncallback)會接收 XTYP 的交易 **\_ \_ 完成** 交易。</span><span class="sxs-lookup"><span data-stu-id="6be56-105">A Dynamic Data Exchange (DDE) client callback function, [*DdeCallback*](/windows/win32/api/ddeml/nc-ddeml-pfncallback), receives the **XTYP\_XACT\_COMPLETE** transaction when an asynchronous transaction, initiated by a call to the [**DdeClientTransaction**](/windows/desktop/api/Ddeml/nf-ddeml-ddeclienttransaction) function, has completed.</span></span>


```C++
#define     XCLASS_NOTIFICATION      0x8000
#define     XTYP_XACT_COMPLETE      (0x0080 | XCLASS_NOTIFICATION  )
```



## <a name="parameters"></a><span data-ttu-id="6be56-106">參數</span><span class="sxs-lookup"><span data-stu-id="6be56-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6be56-107">*uType*</span><span class="sxs-lookup"><span data-stu-id="6be56-107">*uType*</span></span> 
</dt> <dd>

<span data-ttu-id="6be56-108">交易類型。</span><span class="sxs-lookup"><span data-stu-id="6be56-108">The transaction type.</span></span>

</dd> <dt>

<span data-ttu-id="6be56-109">*uFmt*</span><span class="sxs-lookup"><span data-stu-id="6be56-109">*uFmt*</span></span> 
</dt> <dd>

<span data-ttu-id="6be56-110">與已完成之交易相關聯的資料格式 (（如果適用) ），如果在交易期間未交換任何資料，則 **為 Null** 。</span><span class="sxs-lookup"><span data-stu-id="6be56-110">The format of the data associated with the completed transaction (if applicable) or **NULL** if no data was exchanged during the transaction.</span></span>

</dd> <dt>

<span data-ttu-id="6be56-111">*hconv*</span><span class="sxs-lookup"><span data-stu-id="6be56-111">*hconv*</span></span> 
</dt> <dd>

<span data-ttu-id="6be56-112">交談的控制碼。</span><span class="sxs-lookup"><span data-stu-id="6be56-112">A handle to the conversation.</span></span>

</dd> <dt>

<span data-ttu-id="6be56-113">*hsz1*</span><span class="sxs-lookup"><span data-stu-id="6be56-113">*hsz1*</span></span> 
</dt> <dd>

<span data-ttu-id="6be56-114">與已完成之交易相關之主題名稱的控制碼。</span><span class="sxs-lookup"><span data-stu-id="6be56-114">A handle to the topic name involved in the completed transaction.</span></span>

</dd> <dt>

<span data-ttu-id="6be56-115">*hsz2*</span><span class="sxs-lookup"><span data-stu-id="6be56-115">*hsz2*</span></span> 
</dt> <dd>

<span data-ttu-id="6be56-116">與已完成之交易相關之專案名稱的控制碼。</span><span class="sxs-lookup"><span data-stu-id="6be56-116">A handle to the item name involved in the completed transaction.</span></span>

</dd> <dt>

<span data-ttu-id="6be56-117">*hdata*</span><span class="sxs-lookup"><span data-stu-id="6be56-117">*hdata*</span></span> 
</dt> <dd>

<span data-ttu-id="6be56-118">已完成之交易中相關資料的控制碼（如果適用）。</span><span class="sxs-lookup"><span data-stu-id="6be56-118">A handle to the data involved in the completed transaction, if applicable.</span></span> <span data-ttu-id="6be56-119">如果交易成功但未包含任何資料，則此參數為 **TRUE**。</span><span class="sxs-lookup"><span data-stu-id="6be56-119">If the transaction was successful but involved no data, this parameter is **TRUE**.</span></span> <span data-ttu-id="6be56-120">如果交易失敗，此參數為 **Null** 。</span><span class="sxs-lookup"><span data-stu-id="6be56-120">This parameter is **NULL** if the transaction was unsuccessful.</span></span>

</dd> <dt>

<span data-ttu-id="6be56-121">*dwData1*</span><span class="sxs-lookup"><span data-stu-id="6be56-121">*dwData1*</span></span> 
</dt> <dd>

<span data-ttu-id="6be56-122">已完成之交易的交易識別碼。</span><span class="sxs-lookup"><span data-stu-id="6be56-122">The transaction identifier of the completed transaction.</span></span>

</dd> <dt>

<span data-ttu-id="6be56-123">*dwData2*</span><span class="sxs-lookup"><span data-stu-id="6be56-123">*dwData2*</span></span> 
</dt> <dd>

<span data-ttu-id="6be56-124">低字組中任何適用的 **DDE \_** 狀態旗標。</span><span class="sxs-lookup"><span data-stu-id="6be56-124">Any applicable **DDE\_** status flags in the low word.</span></span> <span data-ttu-id="6be56-125">此參數可支援相依于 **DDE \_ APPSTATUS** 位的應用程式。</span><span class="sxs-lookup"><span data-stu-id="6be56-125">This parameter provides support for applications dependent on **DDE\_APPSTATUS** bits.</span></span> <span data-ttu-id="6be56-126">建議應用程式不再使用這些位，在未來的 DDEML 版本中可能不受支援。</span><span class="sxs-lookup"><span data-stu-id="6be56-126">It is recommended that applications no longer use these bits   they may not be supported in future versions of the DDEML.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="6be56-127">備註</span><span class="sxs-lookup"><span data-stu-id="6be56-127">Remarks</span></span>

<span data-ttu-id="6be56-128">應用程式不能釋放在此交易期間取得的資料控制碼。</span><span class="sxs-lookup"><span data-stu-id="6be56-128">An application must not free the data handle obtained during this transaction.</span></span> <span data-ttu-id="6be56-129">但是，如果應用程式必須在回呼函數傳回之後處理資料，則應用程式必須複製與資料控制碼相關聯的資料。</span><span class="sxs-lookup"><span data-stu-id="6be56-129">An application must, however, copy the data associated with the data handle if the application must process the data after the callback function returns.</span></span> <span data-ttu-id="6be56-130">應用程式可以使用 [**DdeGetData**](/windows/desktop/api/Ddeml/nf-ddeml-ddegetdata) 函數來複製資料。</span><span class="sxs-lookup"><span data-stu-id="6be56-130">An application can use the [**DdeGetData**](/windows/desktop/api/Ddeml/nf-ddeml-ddegetdata) function to copy the data.</span></span>

## <a name="requirements"></a><span data-ttu-id="6be56-131">規格需求</span><span class="sxs-lookup"><span data-stu-id="6be56-131">Requirements</span></span>



| <span data-ttu-id="6be56-132">需求</span><span class="sxs-lookup"><span data-stu-id="6be56-132">Requirement</span></span> | <span data-ttu-id="6be56-133">值</span><span class="sxs-lookup"><span data-stu-id="6be56-133">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6be56-134">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="6be56-134">Minimum supported client</span></span><br/> | <span data-ttu-id="6be56-135">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="6be56-135">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="6be56-136">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="6be56-136">Minimum supported server</span></span><br/> | <span data-ttu-id="6be56-137">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="6be56-137">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                   |
| <span data-ttu-id="6be56-138">標頭</span><span class="sxs-lookup"><span data-stu-id="6be56-138">Header</span></span><br/>                   | <dl> <span data-ttu-id="6be56-139"><dt>Ddeml (包含) 的 Windows。h </dt></span><span class="sxs-lookup"><span data-stu-id="6be56-139"><dt>Ddeml.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6be56-140">另請參閱</span><span class="sxs-lookup"><span data-stu-id="6be56-140">See also</span></span>

<dl> <dt>

<span data-ttu-id="6be56-141">**參考**</span><span class="sxs-lookup"><span data-stu-id="6be56-141">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="6be56-142">**DdeClientTransaction**</span><span class="sxs-lookup"><span data-stu-id="6be56-142">**DdeClientTransaction**</span></span>](/windows/desktop/api/Ddeml/nf-ddeml-ddeclienttransaction)
</dt> <dt>

[<span data-ttu-id="6be56-143">**DdeGetData**</span><span class="sxs-lookup"><span data-stu-id="6be56-143">**DdeGetData**</span></span>](/windows/desktop/api/Ddeml/nf-ddeml-ddegetdata)
</dt> <dt>

<span data-ttu-id="6be56-144">**概念**</span><span class="sxs-lookup"><span data-stu-id="6be56-144">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="6be56-145">動態資料交換管理程式庫</span><span class="sxs-lookup"><span data-stu-id="6be56-145">Dynamic Data Exchange Management Library</span></span>](dynamic-data-exchange-management-library.md)
</dt> </dl>

 

