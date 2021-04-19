---
title: 'XTYP_ADVSTOP 交易 (Ddeml .h) '
description: 用戶端會使用 XTYP \_ ADVSTOP 交易，以伺服器結束「建議」迴圈。 當用戶端 \_ 在 DdeClientTransaction 函數中指定 XTYP ADVSTOP 時，動態資料交換 (DDE) server 回呼函式 DdeCallback 會接收此交易。
ms.assetid: 67dfa463-6a44-43a5-93be-a39c19c87c1c
keywords:
- XTYP_ADVSTOP 交易資料交換
topic_type:
- apiref
api_name:
- XTYP_ADVSTOP
api_location:
- Ddeml.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 61292683377cd6c7243c3e41c5dbd9332a671163
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106979681"
---
# <a name="xtyp_advstop-transaction"></a><span data-ttu-id="a881e-105">XTYP \_ ADVSTOP 交易</span><span class="sxs-lookup"><span data-stu-id="a881e-105">XTYP\_ADVSTOP transaction</span></span>

<span data-ttu-id="a881e-106">用戶端會使用 **XTYP \_ ADVSTOP** 交易，以伺服器結束「建議」迴圈。</span><span class="sxs-lookup"><span data-stu-id="a881e-106">A client uses the **XTYP\_ADVSTOP** transaction to end an advise loop with a server.</span></span> <span data-ttu-id="a881e-107">當用戶端在 [**DdeClientTransaction**](/windows/desktop/api/Ddeml/nf-ddeml-ddeclienttransaction)函數中指定 **XTYP \_ ADVSTOP** 時，動態資料交換 (DDE) server 回呼函式 [*DdeCallback*](/windows/win32/api/ddeml/nc-ddeml-pfncallback)會接收此交易。</span><span class="sxs-lookup"><span data-stu-id="a881e-107">A Dynamic Data Exchange (DDE) server callback function, [*DdeCallback*](/windows/win32/api/ddeml/nc-ddeml-pfncallback), receives this transaction when a client specifies **XTYP\_ADVSTOP** in the [**DdeClientTransaction**](/windows/desktop/api/Ddeml/nf-ddeml-ddeclienttransaction) function.</span></span>


```C++
#define     XCLASS_NOTIFICATION      0x8000
#define     XTYP_ADVSTOP            (0x0040 | XCLASS_NOTIFICATION)
```



## <a name="parameters"></a><span data-ttu-id="a881e-108">參數</span><span class="sxs-lookup"><span data-stu-id="a881e-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a881e-109">*uType*</span><span class="sxs-lookup"><span data-stu-id="a881e-109">*uType*</span></span> 
</dt> <dd>

<span data-ttu-id="a881e-110">交易類型。</span><span class="sxs-lookup"><span data-stu-id="a881e-110">The transaction type.</span></span>

</dd> <dt>

<span data-ttu-id="a881e-111">*uFmt*</span><span class="sxs-lookup"><span data-stu-id="a881e-111">*uFmt*</span></span> 
</dt> <dd>

<span data-ttu-id="a881e-112">與要結束的建議迴圈相關聯的資料格式。</span><span class="sxs-lookup"><span data-stu-id="a881e-112">The data format associated with the advise loop being ended.</span></span>

</dd> <dt>

<span data-ttu-id="a881e-113">*hconv*</span><span class="sxs-lookup"><span data-stu-id="a881e-113">*hconv*</span></span> 
</dt> <dd>

<span data-ttu-id="a881e-114">交談的控制碼。</span><span class="sxs-lookup"><span data-stu-id="a881e-114">A handle to the conversation.</span></span>

</dd> <dt>

<span data-ttu-id="a881e-115">*hsz1*</span><span class="sxs-lookup"><span data-stu-id="a881e-115">*hsz1*</span></span> 
</dt> <dd>

<span data-ttu-id="a881e-116">主題名稱的控制碼。</span><span class="sxs-lookup"><span data-stu-id="a881e-116">A handle to the topic name.</span></span>

</dd> <dt>

<span data-ttu-id="a881e-117">*hsz2*</span><span class="sxs-lookup"><span data-stu-id="a881e-117">*hsz2*</span></span> 
</dt> <dd>

<span data-ttu-id="a881e-118">專案名稱的控制碼。</span><span class="sxs-lookup"><span data-stu-id="a881e-118">A handle to the item name.</span></span>

</dd> <dt>

<span data-ttu-id="a881e-119">*hdata*</span><span class="sxs-lookup"><span data-stu-id="a881e-119">*hdata*</span></span> 
</dt> <dd>

<span data-ttu-id="a881e-120">未使用。</span><span class="sxs-lookup"><span data-stu-id="a881e-120">Not used.</span></span>

</dd> <dt>

<span data-ttu-id="a881e-121">*dwData1*</span><span class="sxs-lookup"><span data-stu-id="a881e-121">*dwData1*</span></span> 
</dt> <dd>

<span data-ttu-id="a881e-122">未使用。</span><span class="sxs-lookup"><span data-stu-id="a881e-122">Not used.</span></span>

</dd> <dt>

<span data-ttu-id="a881e-123">*dwData2*</span><span class="sxs-lookup"><span data-stu-id="a881e-123">*dwData2*</span></span> 
</dt> <dd>

<span data-ttu-id="a881e-124">未使用。</span><span class="sxs-lookup"><span data-stu-id="a881e-124">Not used.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="a881e-125">備註</span><span class="sxs-lookup"><span data-stu-id="a881e-125">Remarks</span></span>

<span data-ttu-id="a881e-126">如果伺服器應用程式在 [**DdeInitialize**](/windows/desktop/api/Ddeml/nf-ddeml-ddeinitializea)函式中指定了 **CBF \_ FAIL 「 \_ 建議**」旗標，則會篩選此交易。</span><span class="sxs-lookup"><span data-stu-id="a881e-126">This transaction is filtered if the server application specified the **CBF\_FAIL\_ADVISES** flag in the [**DdeInitialize**](/windows/desktop/api/Ddeml/nf-ddeml-ddeinitializea) function.</span></span>

## <a name="requirements"></a><span data-ttu-id="a881e-127">規格需求</span><span class="sxs-lookup"><span data-stu-id="a881e-127">Requirements</span></span>



| <span data-ttu-id="a881e-128">需求</span><span class="sxs-lookup"><span data-stu-id="a881e-128">Requirement</span></span> | <span data-ttu-id="a881e-129">值</span><span class="sxs-lookup"><span data-stu-id="a881e-129">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a881e-130">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="a881e-130">Minimum supported client</span></span><br/> | <span data-ttu-id="a881e-131">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="a881e-131">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="a881e-132">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="a881e-132">Minimum supported server</span></span><br/> | <span data-ttu-id="a881e-133">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="a881e-133">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                   |
| <span data-ttu-id="a881e-134">標頭</span><span class="sxs-lookup"><span data-stu-id="a881e-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="a881e-135"><dt>Ddeml (包含) 的 Windows。h </dt></span><span class="sxs-lookup"><span data-stu-id="a881e-135"><dt>Ddeml.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a881e-136">另請參閱</span><span class="sxs-lookup"><span data-stu-id="a881e-136">See also</span></span>

<dl> <dt>

<span data-ttu-id="a881e-137">**參考**</span><span class="sxs-lookup"><span data-stu-id="a881e-137">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="a881e-138">**DdeClientTransaction**</span><span class="sxs-lookup"><span data-stu-id="a881e-138">**DdeClientTransaction**</span></span>](/windows/desktop/api/Ddeml/nf-ddeml-ddeclienttransaction)
</dt> <dt>

[<span data-ttu-id="a881e-139">**DdeInitialize**</span><span class="sxs-lookup"><span data-stu-id="a881e-139">**DdeInitialize**</span></span>](/windows/desktop/api/Ddeml/nf-ddeml-ddeinitializea)
</dt> <dt>

[<span data-ttu-id="a881e-140">**DdePostAdvise**</span><span class="sxs-lookup"><span data-stu-id="a881e-140">**DdePostAdvise**</span></span>](/windows/desktop/api/Ddeml/nf-ddeml-ddepostadvise)
</dt> <dt>

<span data-ttu-id="a881e-141">**概念**</span><span class="sxs-lookup"><span data-stu-id="a881e-141">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="a881e-142">動態資料交換管理程式庫</span><span class="sxs-lookup"><span data-stu-id="a881e-142">Dynamic Data Exchange Management Library</span></span>](dynamic-data-exchange-management-library.md)
</dt> </dl>

 

