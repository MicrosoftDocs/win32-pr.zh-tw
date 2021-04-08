---
title: 'XTYP_ADVSTART 交易 (Ddeml .h) '
description: 用戶端會使用 XTYP \_ ADVSTART 交易來建立與伺服器之間的建議迴圈。
ms.assetid: 8911e722-5656-4ca6-8b0a-6bdf8281611a
keywords:
- XTYP_ADVSTART 交易資料交換
topic_type:
- apiref
api_name:
- XTYP_ADVSTART
api_location:
- Ddeml.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 852351ad902a0552ee012d6c1e5c4d61501e6e58
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103685997"
---
# <a name="xtyp_advstart-transaction"></a><span data-ttu-id="aa1ad-104">XTYP \_ ADVSTART 交易</span><span class="sxs-lookup"><span data-stu-id="aa1ad-104">XTYP\_ADVSTART transaction</span></span>

<span data-ttu-id="aa1ad-105">用戶端會使用 **XTYP \_ ADVSTART** 交易來建立與伺服器之間的建議迴圈。</span><span class="sxs-lookup"><span data-stu-id="aa1ad-105">A client uses the **XTYP\_ADVSTART** transaction to establish an advise loop with a server.</span></span> <span data-ttu-id="aa1ad-106">當用戶端將 **XTYP \_ ADVSTART** 指定為 [**DdeClientTransaction**](/windows/desktop/api/Ddeml/nf-ddeml-ddeclienttransaction)函數的 *WTYPE* 參數時，動態資料交換 (DDE) server 回呼函式 [*DdeCallback*](/windows/win32/api/ddeml/nc-ddeml-pfncallback)會接收此交易。</span><span class="sxs-lookup"><span data-stu-id="aa1ad-106">A Dynamic Data Exchange (DDE) server callback function, [*DdeCallback*](/windows/win32/api/ddeml/nc-ddeml-pfncallback), receives this transaction when a client specifies **XTYP\_ADVSTART** as the *wType* parameter of the [**DdeClientTransaction**](/windows/desktop/api/Ddeml/nf-ddeml-ddeclienttransaction) function.</span></span>


```C++
#define     XCLASS_BOOL              0x1000
#define     XTYP_ADVSTART           (0x0030 | XCLASS_BOOL          )
```



## <a name="parameters"></a><span data-ttu-id="aa1ad-107">參數</span><span class="sxs-lookup"><span data-stu-id="aa1ad-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="aa1ad-108">*uType*</span><span class="sxs-lookup"><span data-stu-id="aa1ad-108">*uType*</span></span> 
</dt> <dd>

<span data-ttu-id="aa1ad-109">交易類型。</span><span class="sxs-lookup"><span data-stu-id="aa1ad-109">The transaction type.</span></span>

</dd> <dt>

<span data-ttu-id="aa1ad-110">*uFmt*</span><span class="sxs-lookup"><span data-stu-id="aa1ad-110">*uFmt*</span></span> 
</dt> <dd>

<span data-ttu-id="aa1ad-111">用戶端要求的資料格式。</span><span class="sxs-lookup"><span data-stu-id="aa1ad-111">The data format requested by the client.</span></span>

</dd> <dt>

<span data-ttu-id="aa1ad-112">*hconv*</span><span class="sxs-lookup"><span data-stu-id="aa1ad-112">*hconv*</span></span> 
</dt> <dd>

<span data-ttu-id="aa1ad-113">交談的控制碼。</span><span class="sxs-lookup"><span data-stu-id="aa1ad-113">A handle to the conversation.</span></span>

</dd> <dt>

<span data-ttu-id="aa1ad-114">*hsz1*</span><span class="sxs-lookup"><span data-stu-id="aa1ad-114">*hsz1*</span></span> 
</dt> <dd>

<span data-ttu-id="aa1ad-115">主題名稱的控制碼。</span><span class="sxs-lookup"><span data-stu-id="aa1ad-115">A handle to the topic name.</span></span>

</dd> <dt>

<span data-ttu-id="aa1ad-116">*hsz2*</span><span class="sxs-lookup"><span data-stu-id="aa1ad-116">*hsz2*</span></span> 
</dt> <dd>

<span data-ttu-id="aa1ad-117">專案名稱的控制碼。</span><span class="sxs-lookup"><span data-stu-id="aa1ad-117">A handle to the item name.</span></span>

</dd> <dt>

<span data-ttu-id="aa1ad-118">*hdata*</span><span class="sxs-lookup"><span data-stu-id="aa1ad-118">*hdata*</span></span> 
</dt> <dd>

<span data-ttu-id="aa1ad-119">未使用。</span><span class="sxs-lookup"><span data-stu-id="aa1ad-119">Not used.</span></span>

</dd> <dt>

<span data-ttu-id="aa1ad-120">*dwData1*</span><span class="sxs-lookup"><span data-stu-id="aa1ad-120">*dwData1*</span></span> 
</dt> <dd>

<span data-ttu-id="aa1ad-121">未使用。</span><span class="sxs-lookup"><span data-stu-id="aa1ad-121">Not used.</span></span>

</dd> <dt>

<span data-ttu-id="aa1ad-122">*dwData2*</span><span class="sxs-lookup"><span data-stu-id="aa1ad-122">*dwData2*</span></span> 
</dt> <dd>

<span data-ttu-id="aa1ad-123">未使用。</span><span class="sxs-lookup"><span data-stu-id="aa1ad-123">Not used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="aa1ad-124">傳回值</span><span class="sxs-lookup"><span data-stu-id="aa1ad-124">Return value</span></span>

<span data-ttu-id="aa1ad-125">伺服器回呼函數應該傳回 **TRUE** ，以允許指定之主題名稱和專案名稱組的建議迴圈，或使用 **FALSE** 來拒絕建議迴圈。</span><span class="sxs-lookup"><span data-stu-id="aa1ad-125">A server callback function should return **TRUE** to allow an advise loop on the specified topic name and item name pair, or **FALSE** to deny the advise loop.</span></span> <span data-ttu-id="aa1ad-126">如果回呼函式傳回 **TRUE**，則在相同主題名稱和專案名稱組上，伺服器對 [**DdePostAdvise**](/windows/desktop/api/Ddeml/nf-ddeml-ddepostadvise) 函式的任何後續呼叫都會導致系統傳送 [**XTYP \_ ADVREQ**](xtyp-advreq.md) 交易至伺服器。</span><span class="sxs-lookup"><span data-stu-id="aa1ad-126">If the callback function returns **TRUE**, any subsequent calls to the [**DdePostAdvise**](/windows/desktop/api/Ddeml/nf-ddeml-ddepostadvise) function by the server on the same topic name and item name pair causes the system to send [**XTYP\_ADVREQ**](xtyp-advreq.md) transactions to the server.</span></span>

## <a name="remarks"></a><span data-ttu-id="aa1ad-127">備註</span><span class="sxs-lookup"><span data-stu-id="aa1ad-127">Remarks</span></span>

<span data-ttu-id="aa1ad-128">如果用戶端針對已建立的「建議」迴圈，在主題名稱、專案名稱和資料格式上要求「建議」迴圈，則 (DDEML) 的動態資料交換管理程式庫不會建立重複的「建議」迴圈，但改為改變「建議迴圈」旗標 (**XTYPF \_ ACKREQ** 和 **XTYPF \_ NODATA**) 以符合最新的要求。</span><span class="sxs-lookup"><span data-stu-id="aa1ad-128">If a client requests an advise loop on a topic name, item name, and data format for an advise loop that is already established, the Dynamic Data Exchange Management Library (DDEML) does not create a duplicate advise loop but instead alters the advise loop flags (**XTYPF\_ACKREQ** and **XTYPF\_NODATA**) to match the latest request.</span></span>

<span data-ttu-id="aa1ad-129">如果伺服器應用程式在 [**DdeInitialize**](/windows/desktop/api/Ddeml/nf-ddeml-ddeinitializea)函式中指定了 **CBF \_ FAIL 「 \_ 建議**」旗標，則會篩選此交易。</span><span class="sxs-lookup"><span data-stu-id="aa1ad-129">This transaction is filtered if the server application specified the **CBF\_FAIL\_ADVISES** flag in the [**DdeInitialize**](/windows/desktop/api/Ddeml/nf-ddeml-ddeinitializea) function.</span></span>

## <a name="requirements"></a><span data-ttu-id="aa1ad-130">規格需求</span><span class="sxs-lookup"><span data-stu-id="aa1ad-130">Requirements</span></span>



| <span data-ttu-id="aa1ad-131">需求</span><span class="sxs-lookup"><span data-stu-id="aa1ad-131">Requirement</span></span> | <span data-ttu-id="aa1ad-132">值</span><span class="sxs-lookup"><span data-stu-id="aa1ad-132">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="aa1ad-133">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="aa1ad-133">Minimum supported client</span></span><br/> | <span data-ttu-id="aa1ad-134">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="aa1ad-134">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="aa1ad-135">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="aa1ad-135">Minimum supported server</span></span><br/> | <span data-ttu-id="aa1ad-136">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="aa1ad-136">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                   |
| <span data-ttu-id="aa1ad-137">標頭</span><span class="sxs-lookup"><span data-stu-id="aa1ad-137">Header</span></span><br/>                   | <dl> <span data-ttu-id="aa1ad-138"><dt>Ddeml (包含) 的 Windows。h </dt></span><span class="sxs-lookup"><span data-stu-id="aa1ad-138"><dt>Ddeml.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="aa1ad-139">另請參閱</span><span class="sxs-lookup"><span data-stu-id="aa1ad-139">See also</span></span>

<dl> <dt>

<span data-ttu-id="aa1ad-140">**參考**</span><span class="sxs-lookup"><span data-stu-id="aa1ad-140">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="aa1ad-141">**DdeClientTransaction**</span><span class="sxs-lookup"><span data-stu-id="aa1ad-141">**DdeClientTransaction**</span></span>](/windows/desktop/api/Ddeml/nf-ddeml-ddeclienttransaction)
</dt> <dt>

[<span data-ttu-id="aa1ad-142">**DdeInitialize**</span><span class="sxs-lookup"><span data-stu-id="aa1ad-142">**DdeInitialize**</span></span>](/windows/desktop/api/Ddeml/nf-ddeml-ddeinitializea)
</dt> <dt>

[<span data-ttu-id="aa1ad-143">**DdePostAdvise**</span><span class="sxs-lookup"><span data-stu-id="aa1ad-143">**DdePostAdvise**</span></span>](/windows/desktop/api/Ddeml/nf-ddeml-ddepostadvise)
</dt> <dt>

<span data-ttu-id="aa1ad-144">**概念**</span><span class="sxs-lookup"><span data-stu-id="aa1ad-144">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="aa1ad-145">動態資料交換管理程式庫</span><span class="sxs-lookup"><span data-stu-id="aa1ad-145">Dynamic Data Exchange Management Library</span></span>](dynamic-data-exchange-management-library.md)
</dt> </dl>

 

