---
title: 'XTYP_UNREGISTER 交易 (Ddeml .h) '
description: '\_當動態資料交換管理程式庫 (DDEML) 伺服器應用程式使用 DdeNameService 函式取消註冊服務名稱，或每次支援系統主題的非 DDEML 應用程式終止時，動態資料交換 (DDE) 回呼函式 DdeCallback 會接收 XTYP 取消註冊交易。'
ms.assetid: a57a5d53-7919-4698-8c84-6142dd29bb2a
keywords:
- XTYP_UNREGISTER 交易資料交換
topic_type:
- apiref
api_name:
- XTYP_UNREGISTER
api_location:
- Ddeml.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: eeba96b26c019aa0a3050a83f726745b749efa96
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103686250"
---
# <a name="xtyp_unregister-transaction"></a><span data-ttu-id="2f06d-104">XTYP \_ 取消註冊交易</span><span class="sxs-lookup"><span data-stu-id="2f06d-104">XTYP\_UNREGISTER transaction</span></span>

<span data-ttu-id="2f06d-105">當動態資料交換管理程式庫 (DDEML) 伺服器應用程式使用 [**DdeNameService**](/windows/desktop/api/Ddeml/nf-ddeml-ddenameservice)函式取消註冊服務名稱，或每次支援系統主題的非 DDEML 應用程式終止時，動態資料交換 (DDE) 回呼函式 [*DdeCallback*](/windows/win32/api/ddeml/nc-ddeml-pfncallback)會接收 **XTYP \_ 取消註冊** 交易。</span><span class="sxs-lookup"><span data-stu-id="2f06d-105">A Dynamic Data Exchange (DDE) callback function, [*DdeCallback*](/windows/win32/api/ddeml/nc-ddeml-pfncallback), receives the **XTYP\_UNREGISTER** transaction whenever a Dynamic Data Exchange Management Library (DDEML) server application uses the [**DdeNameService**](/windows/desktop/api/Ddeml/nf-ddeml-ddenameservice) function to unregister a service name, or whenever a non-DDEML application that supports the System topic is terminated.</span></span>


```C++
#define     XCLASS_NOTIFICATION      0x8000
#define     XTYPF_NOBLOCK            0x0002
#define     XTYP_UNREGISTER         (0x00D0 | XCLASS_NOTIFICATION | XTYPF_NOBLOCK)
```



## <a name="parameters"></a><span data-ttu-id="2f06d-106">參數</span><span class="sxs-lookup"><span data-stu-id="2f06d-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2f06d-107">*uType*</span><span class="sxs-lookup"><span data-stu-id="2f06d-107">*uType*</span></span> 
</dt> <dd>

<span data-ttu-id="2f06d-108">交易類型。</span><span class="sxs-lookup"><span data-stu-id="2f06d-108">The transaction type.</span></span>

</dd> <dt>

<span data-ttu-id="2f06d-109">*uFmt*</span><span class="sxs-lookup"><span data-stu-id="2f06d-109">*uFmt*</span></span> 
</dt> <dd>

<span data-ttu-id="2f06d-110">未使用。</span><span class="sxs-lookup"><span data-stu-id="2f06d-110">Not used.</span></span>

</dd> <dt>

<span data-ttu-id="2f06d-111">*hconv*</span><span class="sxs-lookup"><span data-stu-id="2f06d-111">*hconv*</span></span> 
</dt> <dd>

<span data-ttu-id="2f06d-112">未使用。</span><span class="sxs-lookup"><span data-stu-id="2f06d-112">Not used.</span></span>

</dd> <dt>

<span data-ttu-id="2f06d-113">*hsz1*</span><span class="sxs-lookup"><span data-stu-id="2f06d-113">*hsz1*</span></span> 
</dt> <dd>

<span data-ttu-id="2f06d-114">要取消註冊之基底服務名稱的控制碼。</span><span class="sxs-lookup"><span data-stu-id="2f06d-114">A handle to the base service name being unregistered.</span></span>

</dd> <dt>

<span data-ttu-id="2f06d-115">*hsz2*</span><span class="sxs-lookup"><span data-stu-id="2f06d-115">*hsz2*</span></span> 
</dt> <dd>

<span data-ttu-id="2f06d-116">要取消註冊之實例特定服務名稱的控制碼。</span><span class="sxs-lookup"><span data-stu-id="2f06d-116">A handle to the instance-specific service name being unregistered.</span></span>

</dd> <dt>

<span data-ttu-id="2f06d-117">*hdata*</span><span class="sxs-lookup"><span data-stu-id="2f06d-117">*hdata*</span></span> 
</dt> <dd>

<span data-ttu-id="2f06d-118">未使用。</span><span class="sxs-lookup"><span data-stu-id="2f06d-118">Not used.</span></span>

</dd> <dt>

<span data-ttu-id="2f06d-119">*dwData1*</span><span class="sxs-lookup"><span data-stu-id="2f06d-119">*dwData1*</span></span> 
</dt> <dd>

<span data-ttu-id="2f06d-120">未使用。</span><span class="sxs-lookup"><span data-stu-id="2f06d-120">Not used.</span></span>

</dd> <dt>

<span data-ttu-id="2f06d-121">*dwData2*</span><span class="sxs-lookup"><span data-stu-id="2f06d-121">*dwData2*</span></span> 
</dt> <dd>

<span data-ttu-id="2f06d-122">未使用。</span><span class="sxs-lookup"><span data-stu-id="2f06d-122">Not used.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="2f06d-123">備註</span><span class="sxs-lookup"><span data-stu-id="2f06d-123">Remarks</span></span>

<span data-ttu-id="2f06d-124">如果應用程式在 [**DdeInitialize**](/windows/desktop/api/Ddeml/nf-ddeml-ddeinitializea)函數中指定了 **CBF \_ SKIP \_ 註冊** 旗標，則會篩選此交易。</span><span class="sxs-lookup"><span data-stu-id="2f06d-124">This transaction is filtered if the application specified the **CBF\_SKIP\_REGISTRATIONS** flag in the [**DdeInitialize**](/windows/desktop/api/Ddeml/nf-ddeml-ddeinitializea) function.</span></span>

<span data-ttu-id="2f06d-125">應用程式無法封鎖此交易類型;\_會忽略 CBR 區塊傳回碼。</span><span class="sxs-lookup"><span data-stu-id="2f06d-125">A application cannot block this transaction type; the CBR\_BLOCK return code is ignored.</span></span>

<span data-ttu-id="2f06d-126">應用程式應該使用 *hsz1* 參數，將服務名稱從使用者可用的伺服器清單中移除。</span><span class="sxs-lookup"><span data-stu-id="2f06d-126">An application should use the *hsz1* parameter to remove the service name from the list of servers available to the user.</span></span> <span data-ttu-id="2f06d-127">應用程式應該使用 *hsz2* 參數來識別已終止的應用程式實例。</span><span class="sxs-lookup"><span data-stu-id="2f06d-127">An application should use the *hsz2* parameter to identify which application instance has terminated.</span></span>

## <a name="requirements"></a><span data-ttu-id="2f06d-128">規格需求</span><span class="sxs-lookup"><span data-stu-id="2f06d-128">Requirements</span></span>



| <span data-ttu-id="2f06d-129">需求</span><span class="sxs-lookup"><span data-stu-id="2f06d-129">Requirement</span></span> | <span data-ttu-id="2f06d-130">值</span><span class="sxs-lookup"><span data-stu-id="2f06d-130">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2f06d-131">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="2f06d-131">Minimum supported client</span></span><br/> | <span data-ttu-id="2f06d-132">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="2f06d-132">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="2f06d-133">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="2f06d-133">Minimum supported server</span></span><br/> | <span data-ttu-id="2f06d-134">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="2f06d-134">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                   |
| <span data-ttu-id="2f06d-135">標頭</span><span class="sxs-lookup"><span data-stu-id="2f06d-135">Header</span></span><br/>                   | <dl> <span data-ttu-id="2f06d-136"><dt>Ddeml (包含) 的 Windows。h </dt></span><span class="sxs-lookup"><span data-stu-id="2f06d-136"><dt>Ddeml.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2f06d-137">另請參閱</span><span class="sxs-lookup"><span data-stu-id="2f06d-137">See also</span></span>

<dl> <dt>

<span data-ttu-id="2f06d-138">**參考**</span><span class="sxs-lookup"><span data-stu-id="2f06d-138">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="2f06d-139">**DdeInitialize**</span><span class="sxs-lookup"><span data-stu-id="2f06d-139">**DdeInitialize**</span></span>](/windows/desktop/api/Ddeml/nf-ddeml-ddeinitializea)
</dt> <dt>

[<span data-ttu-id="2f06d-140">**DdeNameService**</span><span class="sxs-lookup"><span data-stu-id="2f06d-140">**DdeNameService**</span></span>](/windows/desktop/api/Ddeml/nf-ddeml-ddenameservice)
</dt> <dt>

<span data-ttu-id="2f06d-141">**概念**</span><span class="sxs-lookup"><span data-stu-id="2f06d-141">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="2f06d-142">動態資料交換管理程式庫</span><span class="sxs-lookup"><span data-stu-id="2f06d-142">Dynamic Data Exchange Management Library</span></span>](dynamic-data-exchange-management-library.md)
</dt> </dl>

 

