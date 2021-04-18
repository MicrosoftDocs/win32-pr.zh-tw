---
title: 'XTYP_ADVDATA 交易 (Ddeml .h) '
description: 通知用戶端資料項目目的值已變更。 動態資料交換 (DDE) 用戶端回呼函式 DdeCallback，會在建立與伺服器的建議迴圈之後，接收此交易。
ms.assetid: c6e61785-b98c-4ffa-9d23-339e1c66cb4d
keywords:
- XTYP_ADVDATA 交易資料交換
topic_type:
- apiref
api_name:
- XTYP_ADVDATA
api_location:
- Ddeml.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8359e34388d185200b5f30c4554e138cc1f6b94a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106965281"
---
# <a name="xtyp_advdata-transaction"></a><span data-ttu-id="b2e75-105">XTYP \_ ADVDATA 交易</span><span class="sxs-lookup"><span data-stu-id="b2e75-105">XTYP\_ADVDATA transaction</span></span>

<span data-ttu-id="b2e75-106">通知用戶端資料項目目的值已變更。</span><span class="sxs-lookup"><span data-stu-id="b2e75-106">Informs the client that the value of the data item has changed.</span></span> <span data-ttu-id="b2e75-107">動態資料交換 (DDE) 用戶端回呼函式 [*DdeCallback*](/windows/win32/api/ddeml/nc-ddeml-pfncallback)，會在建立與伺服器的建議迴圈之後，接收此交易。</span><span class="sxs-lookup"><span data-stu-id="b2e75-107">The Dynamic Data Exchange (DDE) client callback function, [*DdeCallback*](/windows/win32/api/ddeml/nc-ddeml-pfncallback), receives this transaction after establishing an advise loop with a server.</span></span>


```C++
#define     XCLASS_FLAGS             0x4000
#define     XTYP_ADVDATA            (0x0010 | XCLASS_FLAGS         )
```



## <a name="parameters"></a><span data-ttu-id="b2e75-108">參數</span><span class="sxs-lookup"><span data-stu-id="b2e75-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b2e75-109">*uType*</span><span class="sxs-lookup"><span data-stu-id="b2e75-109">*uType*</span></span> 
</dt> <dd>

<span data-ttu-id="b2e75-110">交易類型。</span><span class="sxs-lookup"><span data-stu-id="b2e75-110">The transaction type.</span></span>

</dd> <dt>

<span data-ttu-id="b2e75-111">*uFmt*</span><span class="sxs-lookup"><span data-stu-id="b2e75-111">*uFmt*</span></span> 
</dt> <dd>

<span data-ttu-id="b2e75-112">從伺服器傳送之資料的格式 atom。</span><span class="sxs-lookup"><span data-stu-id="b2e75-112">The format atom of the data sent from the server.</span></span>

</dd> <dt>

<span data-ttu-id="b2e75-113">*hconv*</span><span class="sxs-lookup"><span data-stu-id="b2e75-113">*hconv*</span></span> 
</dt> <dd>

<span data-ttu-id="b2e75-114">交談的控制碼。</span><span class="sxs-lookup"><span data-stu-id="b2e75-114">A handle to the conversation.</span></span>

</dd> <dt>

<span data-ttu-id="b2e75-115">*hsz1*</span><span class="sxs-lookup"><span data-stu-id="b2e75-115">*hsz1*</span></span> 
</dt> <dd>

<span data-ttu-id="b2e75-116">主題名稱的控制碼。</span><span class="sxs-lookup"><span data-stu-id="b2e75-116">A handle to the topic name.</span></span>

</dd> <dt>

<span data-ttu-id="b2e75-117">*hsz2*</span><span class="sxs-lookup"><span data-stu-id="b2e75-117">*hsz2*</span></span> 
</dt> <dd>

<span data-ttu-id="b2e75-118">專案名稱的控制碼。</span><span class="sxs-lookup"><span data-stu-id="b2e75-118">A handle to the item name.</span></span>

</dd> <dt>

<span data-ttu-id="b2e75-119">*hdata*</span><span class="sxs-lookup"><span data-stu-id="b2e75-119">*hdata*</span></span> 
</dt> <dd>

<span data-ttu-id="b2e75-120">與主題名稱和專案名稱配對相關聯之資料的控制碼。</span><span class="sxs-lookup"><span data-stu-id="b2e75-120">A handle to the data associated with the topic name and item name pair.</span></span> <span data-ttu-id="b2e75-121">如果用戶端在要求「建議」迴圈時指定了 **XTYPF \_ NODATA** 旗標，則此參數為 **Null** 。</span><span class="sxs-lookup"><span data-stu-id="b2e75-121">This parameter is **NULL** if the client specified the **XTYPF\_NODATA** flag when it requested the advise loop.</span></span>

</dd> <dt>

<span data-ttu-id="b2e75-122">*dwData1*</span><span class="sxs-lookup"><span data-stu-id="b2e75-122">*dwData1*</span></span> 
</dt> <dd>

<span data-ttu-id="b2e75-123">未使用。</span><span class="sxs-lookup"><span data-stu-id="b2e75-123">Not used.</span></span>

</dd> <dt>

<span data-ttu-id="b2e75-124">*dwData2*</span><span class="sxs-lookup"><span data-stu-id="b2e75-124">*dwData2*</span></span> 
</dt> <dd>

<span data-ttu-id="b2e75-125">未使用。</span><span class="sxs-lookup"><span data-stu-id="b2e75-125">Not used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b2e75-126">傳回值</span><span class="sxs-lookup"><span data-stu-id="b2e75-126">Return value</span></span>

<span data-ttu-id="b2e75-127">如果 DDE 回呼函數處理這項交易，則會傳回 **dde \_ FACK** ，如果它太忙碌而無法處理此交易，則會傳回 dde **\_ FBUSY** ; 如果拒絕此交易，則會傳回 dde **\_ FNOTPROCESSED** 。</span><span class="sxs-lookup"><span data-stu-id="b2e75-127">A DDE callback function should return **DDE\_FACK** if it processes this transaction, **DDE\_FBUSY** if it is too busy to process this transaction, or **DDE\_FNOTPROCESSED** if it rejects this transaction.</span></span>

## <a name="remarks"></a><span data-ttu-id="b2e75-128">備註</span><span class="sxs-lookup"><span data-stu-id="b2e75-128">Remarks</span></span>

<span data-ttu-id="b2e75-129">應用程式不能釋放在此交易期間取得的資料控制碼。</span><span class="sxs-lookup"><span data-stu-id="b2e75-129">An application must not free the data handle obtained during this transaction.</span></span> <span data-ttu-id="b2e75-130">但是，如果應用程式必須在回呼函數傳回之後處理資料，則應用程式必須複製與資料控制碼相關聯的資料。</span><span class="sxs-lookup"><span data-stu-id="b2e75-130">An application must, however, copy the data associated with the data handle if the application must process the data after the callback function returns.</span></span> <span data-ttu-id="b2e75-131">應用程式可以使用 [**DdeGetData**](/windows/desktop/api/Ddeml/nf-ddeml-ddegetdata) 函數來複製資料。</span><span class="sxs-lookup"><span data-stu-id="b2e75-131">An application can use the [**DdeGetData**](/windows/desktop/api/Ddeml/nf-ddeml-ddegetdata) function to copy the data.</span></span>

## <a name="requirements"></a><span data-ttu-id="b2e75-132">規格需求</span><span class="sxs-lookup"><span data-stu-id="b2e75-132">Requirements</span></span>



| <span data-ttu-id="b2e75-133">需求</span><span class="sxs-lookup"><span data-stu-id="b2e75-133">Requirement</span></span> | <span data-ttu-id="b2e75-134">值</span><span class="sxs-lookup"><span data-stu-id="b2e75-134">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b2e75-135">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="b2e75-135">Minimum supported client</span></span><br/> | <span data-ttu-id="b2e75-136">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="b2e75-136">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="b2e75-137">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="b2e75-137">Minimum supported server</span></span><br/> | <span data-ttu-id="b2e75-138">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="b2e75-138">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                   |
| <span data-ttu-id="b2e75-139">標頭</span><span class="sxs-lookup"><span data-stu-id="b2e75-139">Header</span></span><br/>                   | <dl> <span data-ttu-id="b2e75-140"><dt>Ddeml (包含) 的 Windows。h </dt></span><span class="sxs-lookup"><span data-stu-id="b2e75-140"><dt>Ddeml.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b2e75-141">另請參閱</span><span class="sxs-lookup"><span data-stu-id="b2e75-141">See also</span></span>

<dl> <dt>

<span data-ttu-id="b2e75-142">**參考**</span><span class="sxs-lookup"><span data-stu-id="b2e75-142">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="b2e75-143">**DdeClientTransaction**</span><span class="sxs-lookup"><span data-stu-id="b2e75-143">**DdeClientTransaction**</span></span>](/windows/desktop/api/Ddeml/nf-ddeml-ddeclienttransaction)
</dt> <dt>

[<span data-ttu-id="b2e75-144">**DdeGetData**</span><span class="sxs-lookup"><span data-stu-id="b2e75-144">**DdeGetData**</span></span>](/windows/desktop/api/Ddeml/nf-ddeml-ddegetdata)
</dt> <dt>

[<span data-ttu-id="b2e75-145">**DdePostAdvise**</span><span class="sxs-lookup"><span data-stu-id="b2e75-145">**DdePostAdvise**</span></span>](/windows/desktop/api/Ddeml/nf-ddeml-ddepostadvise)
</dt> <dt>

<span data-ttu-id="b2e75-146">**概念**</span><span class="sxs-lookup"><span data-stu-id="b2e75-146">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="b2e75-147">動態資料交換管理程式庫</span><span class="sxs-lookup"><span data-stu-id="b2e75-147">Dynamic Data Exchange Management Library</span></span>](dynamic-data-exchange-management-library.md)
</dt> </dl>

 

