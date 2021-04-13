---
title: 'XTYP_REGISTER 交易 (Ddeml .h) '
description: '\_每當動態資料交換管理程式庫 (DDEML) 伺服器應用程式使用 DdeNameService 函式來註冊服務名稱，或每當支援系統主題的非 DDEML 應用程式啟動時，動態資料交換 (DDE) 回呼函式 DdeCallback 會收到 XTYP REGISTER 交易類型。'
ms.assetid: 465e9c10-1526-4e2a-8a46-5984043f5a93
keywords:
- XTYP_REGISTER 交易資料交換
topic_type:
- apiref
api_name:
- XTYP_REGISTER
api_location:
- Ddeml.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cd56bf4f5ac2b4eb0f714e5348174942f685c2ab
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104464949"
---
# <a name="xtyp_register-transaction"></a><span data-ttu-id="a6960-104">XTYP \_ 註冊交易</span><span class="sxs-lookup"><span data-stu-id="a6960-104">XTYP\_REGISTER transaction</span></span>

<span data-ttu-id="a6960-105">每當動態資料交換管理程式庫 (DDEML) 伺服器應用程式使用 [**DdeNameService**](/windows/desktop/api/Ddeml/nf-ddeml-ddenameservice)函式來註冊服務名稱，或每當支援系統主題的非 DDEML 應用程式啟動時，動態資料交換 (DDE) 回呼函式 [*DdeCallback*](/windows/win32/api/ddeml/nc-ddeml-pfncallback)會收到 **XTYP \_ REGISTER** 交易類型。</span><span class="sxs-lookup"><span data-stu-id="a6960-105">A Dynamic Data Exchange (DDE) callback function, [*DdeCallback*](/windows/win32/api/ddeml/nc-ddeml-pfncallback), receives the **XTYP\_REGISTER** transaction type whenever a Dynamic Data Exchange Management Library (DDEML) server application uses the [**DdeNameService**](/windows/desktop/api/Ddeml/nf-ddeml-ddenameservice) function to register a service name, or whenever a non-DDEML application that supports the System topic is started.</span></span>


```C++
#define     XCLASS_NOTIFICATION      0x8000
#define     XTYPF_NOBLOCK            0x0002
#define     XTYP_REGISTER           (0x00A0 | XCLASS_NOTIFICATION | XTYPF_NOBLOCK)
```



## <a name="parameters"></a><span data-ttu-id="a6960-106">參數</span><span class="sxs-lookup"><span data-stu-id="a6960-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a6960-107">*uType*</span><span class="sxs-lookup"><span data-stu-id="a6960-107">*uType*</span></span> 
</dt> <dd>

<span data-ttu-id="a6960-108">交易類型。</span><span class="sxs-lookup"><span data-stu-id="a6960-108">The transaction type.</span></span>

</dd> <dt>

<span data-ttu-id="a6960-109">*uFmt*</span><span class="sxs-lookup"><span data-stu-id="a6960-109">*uFmt*</span></span> 
</dt> <dd>

<span data-ttu-id="a6960-110">未使用。</span><span class="sxs-lookup"><span data-stu-id="a6960-110">Not used.</span></span>

</dd> <dt>

<span data-ttu-id="a6960-111">*hconv*</span><span class="sxs-lookup"><span data-stu-id="a6960-111">*hconv*</span></span> 
</dt> <dd>

<span data-ttu-id="a6960-112">未使用。</span><span class="sxs-lookup"><span data-stu-id="a6960-112">Not used.</span></span>

</dd> <dt>

<span data-ttu-id="a6960-113">*hsz1*</span><span class="sxs-lookup"><span data-stu-id="a6960-113">*hsz1*</span></span> 
</dt> <dd>

<span data-ttu-id="a6960-114">要註冊之基底服務名稱的控制碼。</span><span class="sxs-lookup"><span data-stu-id="a6960-114">A handle to the base service name being registered.</span></span>

</dd> <dt>

<span data-ttu-id="a6960-115">*hsz2*</span><span class="sxs-lookup"><span data-stu-id="a6960-115">*hsz2*</span></span> 
</dt> <dd>

<span data-ttu-id="a6960-116">要註冊之實例特定服務名稱的控制碼。</span><span class="sxs-lookup"><span data-stu-id="a6960-116">A handle to the instance-specific service name being registered.</span></span>

</dd> <dt>

<span data-ttu-id="a6960-117">*hdata*</span><span class="sxs-lookup"><span data-stu-id="a6960-117">*hdata*</span></span> 
</dt> <dd>

<span data-ttu-id="a6960-118">未使用。</span><span class="sxs-lookup"><span data-stu-id="a6960-118">Not used.</span></span>

</dd> <dt>

<span data-ttu-id="a6960-119">*dwData1*</span><span class="sxs-lookup"><span data-stu-id="a6960-119">*dwData1*</span></span> 
</dt> <dd>

<span data-ttu-id="a6960-120">未使用。</span><span class="sxs-lookup"><span data-stu-id="a6960-120">Not used.</span></span>

</dd> <dt>

<span data-ttu-id="a6960-121">*dwData2*</span><span class="sxs-lookup"><span data-stu-id="a6960-121">*dwData2*</span></span> 
</dt> <dd>

<span data-ttu-id="a6960-122">未使用。</span><span class="sxs-lookup"><span data-stu-id="a6960-122">Not used.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="a6960-123">備註</span><span class="sxs-lookup"><span data-stu-id="a6960-123">Remarks</span></span>

<span data-ttu-id="a6960-124">如果應用程式在 [**DdeInitialize**](/windows/desktop/api/Ddeml/nf-ddeml-ddeinitializea)函數中指定了 **CBF \_ SKIP \_ 註冊** 旗標，則會篩選此交易。</span><span class="sxs-lookup"><span data-stu-id="a6960-124">This transaction is filtered if the application specified the **CBF\_SKIP\_REGISTRATIONS** flag in the [**DdeInitialize**](/windows/desktop/api/Ddeml/nf-ddeml-ddeinitializea) function.</span></span>

<span data-ttu-id="a6960-125">應用程式無法封鎖此交易類型;會忽略 **CBR \_ 區塊** 傳回碼。</span><span class="sxs-lookup"><span data-stu-id="a6960-125">A application cannot block this transaction type; the **CBR\_BLOCK** return code is ignored.</span></span>

<span data-ttu-id="a6960-126">應用程式應該使用 *hsz1* 參數，將服務名稱新增至使用者可用的伺服器清單。</span><span class="sxs-lookup"><span data-stu-id="a6960-126">An application should use the *hsz1* parameter to add the service name to the list of servers available to the user.</span></span> <span data-ttu-id="a6960-127">應用程式應該使用 *hsz2* 參數來識別已啟動的應用程式實例。</span><span class="sxs-lookup"><span data-stu-id="a6960-127">An application should use the *hsz2* parameter to identify which application instance has started.</span></span>

## <a name="requirements"></a><span data-ttu-id="a6960-128">規格需求</span><span class="sxs-lookup"><span data-stu-id="a6960-128">Requirements</span></span>



| <span data-ttu-id="a6960-129">需求</span><span class="sxs-lookup"><span data-stu-id="a6960-129">Requirement</span></span> | <span data-ttu-id="a6960-130">值</span><span class="sxs-lookup"><span data-stu-id="a6960-130">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a6960-131">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="a6960-131">Minimum supported client</span></span><br/> | <span data-ttu-id="a6960-132">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="a6960-132">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="a6960-133">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="a6960-133">Minimum supported server</span></span><br/> | <span data-ttu-id="a6960-134">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="a6960-134">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                   |
| <span data-ttu-id="a6960-135">標頭</span><span class="sxs-lookup"><span data-stu-id="a6960-135">Header</span></span><br/>                   | <dl> <span data-ttu-id="a6960-136"><dt>Ddeml (包含) 的 Windows。h </dt></span><span class="sxs-lookup"><span data-stu-id="a6960-136"><dt>Ddeml.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a6960-137">另請參閱</span><span class="sxs-lookup"><span data-stu-id="a6960-137">See also</span></span>

<dl> <dt>

<span data-ttu-id="a6960-138">**參考**</span><span class="sxs-lookup"><span data-stu-id="a6960-138">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="a6960-139">**DdeInitialize**</span><span class="sxs-lookup"><span data-stu-id="a6960-139">**DdeInitialize**</span></span>](/windows/desktop/api/Ddeml/nf-ddeml-ddeinitializea)
</dt> <dt>

[<span data-ttu-id="a6960-140">**DdeNameService**</span><span class="sxs-lookup"><span data-stu-id="a6960-140">**DdeNameService**</span></span>](/windows/desktop/api/Ddeml/nf-ddeml-ddenameservice)
</dt> <dt>

<span data-ttu-id="a6960-141">**概念**</span><span class="sxs-lookup"><span data-stu-id="a6960-141">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="a6960-142">動態資料交換管理程式庫</span><span class="sxs-lookup"><span data-stu-id="a6960-142">Dynamic Data Exchange Management Library</span></span>](dynamic-data-exchange-management-library.md)
</dt> </dl>

 

