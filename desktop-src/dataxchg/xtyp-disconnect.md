---
title: 'XTYP_DISCONNECT 交易 (Ddeml .h) '
description: '\_當交談中的應用程式夥伴使用 DdeDisconnect 函式來終止交談時，應用程式的動態資料交換 (DDE) 回呼函式 DdeCallback 會接收 XTYP 中斷連接交易。'
ms.assetid: 22a9ec63-8a74-4829-ad02-d07dd0e8fa9b
keywords:
- XTYP_DISCONNECT 交易資料交換
topic_type:
- apiref
api_name:
- XTYP_DISCONNECT
api_location:
- Ddeml.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 38e73bc0446989ac572a27f394e594924573711d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103685615"
---
# <a name="xtyp_disconnect-transaction"></a><span data-ttu-id="b08f4-104">XTYP \_ 中斷連接交易</span><span class="sxs-lookup"><span data-stu-id="b08f4-104">XTYP\_DISCONNECT transaction</span></span>

<span data-ttu-id="b08f4-105">當交談中的應用程式夥伴使用 [**DdeDisconnect**](/windows/desktop/api/Ddeml/nf-ddeml-ddedisconnect)函式來終止交談時，應用程式的動態資料交換 (DDE) 回呼函式 [*DdeCallback*](/windows/win32/api/ddeml/nc-ddeml-pfncallback)會接收 **XTYP \_ 中斷連接** 交易。</span><span class="sxs-lookup"><span data-stu-id="b08f4-105">An application's Dynamic Data Exchange (DDE) callback function, [*DdeCallback*](/windows/win32/api/ddeml/nc-ddeml-pfncallback), receives the **XTYP\_DISCONNECT** transaction when the application's partner in a conversation uses the [**DdeDisconnect**](/windows/desktop/api/Ddeml/nf-ddeml-ddedisconnect) function to terminate the conversation.</span></span>


```C++
#define     XCLASS_NOTIFICATION      0x8000
#define     XTYPF_NOBLOCK            0x0002
#define     XTYP_DISCONNECT         (0x00C0 | XCLASS_NOTIFICATION | XTYPF_NOBLOCK)
```



## <a name="parameters"></a><span data-ttu-id="b08f4-106">參數</span><span class="sxs-lookup"><span data-stu-id="b08f4-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b08f4-107">*uType*</span><span class="sxs-lookup"><span data-stu-id="b08f4-107">*uType*</span></span> 
</dt> <dd>

<span data-ttu-id="b08f4-108">交易類型。</span><span class="sxs-lookup"><span data-stu-id="b08f4-108">The transaction type.</span></span>

</dd> <dt>

<span data-ttu-id="b08f4-109">*uFmt*</span><span class="sxs-lookup"><span data-stu-id="b08f4-109">*uFmt*</span></span> 
</dt> <dd>

<span data-ttu-id="b08f4-110">未使用。</span><span class="sxs-lookup"><span data-stu-id="b08f4-110">Not used.</span></span>

</dd> <dt>

<span data-ttu-id="b08f4-111">*hconv*</span><span class="sxs-lookup"><span data-stu-id="b08f4-111">*hconv*</span></span> 
</dt> <dd>

<span data-ttu-id="b08f4-112">已終止交談的控制碼。</span><span class="sxs-lookup"><span data-stu-id="b08f4-112">A handle to that the conversation was terminated.</span></span>

</dd> <dt>

<span data-ttu-id="b08f4-113">*hsz1*</span><span class="sxs-lookup"><span data-stu-id="b08f4-113">*hsz1*</span></span> 
</dt> <dd>

<span data-ttu-id="b08f4-114">未使用。</span><span class="sxs-lookup"><span data-stu-id="b08f4-114">Not used.</span></span>

</dd> <dt>

<span data-ttu-id="b08f4-115">*hsz2*</span><span class="sxs-lookup"><span data-stu-id="b08f4-115">*hsz2*</span></span> 
</dt> <dd>

<span data-ttu-id="b08f4-116">未使用。</span><span class="sxs-lookup"><span data-stu-id="b08f4-116">Not used.</span></span>

</dd> <dt>

<span data-ttu-id="b08f4-117">*hdata*</span><span class="sxs-lookup"><span data-stu-id="b08f4-117">*hdata*</span></span> 
</dt> <dd>

<span data-ttu-id="b08f4-118">未使用。</span><span class="sxs-lookup"><span data-stu-id="b08f4-118">Not used.</span></span>

</dd> <dt>

<span data-ttu-id="b08f4-119">*dwData1*</span><span class="sxs-lookup"><span data-stu-id="b08f4-119">*dwData1*</span></span> 
</dt> <dd>

<span data-ttu-id="b08f4-120">未使用。</span><span class="sxs-lookup"><span data-stu-id="b08f4-120">Not used.</span></span>

</dd> <dt>

<span data-ttu-id="b08f4-121">*dwData2*</span><span class="sxs-lookup"><span data-stu-id="b08f4-121">*dwData2*</span></span> 
</dt> <dd>

<span data-ttu-id="b08f4-122">指定交談中的夥伴是否為相同的應用程式實例。</span><span class="sxs-lookup"><span data-stu-id="b08f4-122">Specifies whether the partners in the conversation are the same application instance.</span></span> <span data-ttu-id="b08f4-123">如果這個參數是1，則夥伴是相同的實例。</span><span class="sxs-lookup"><span data-stu-id="b08f4-123">If this parameter is 1, the partners are the same instance.</span></span> <span data-ttu-id="b08f4-124">如果此參數為0，則夥伴為不同的實例。</span><span class="sxs-lookup"><span data-stu-id="b08f4-124">If this parameter is 0, the partners are different instances.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="b08f4-125">備註</span><span class="sxs-lookup"><span data-stu-id="b08f4-125">Remarks</span></span>

<span data-ttu-id="b08f4-126">如果應用程式在 [**DdeInitialize**](/windows/desktop/api/Ddeml/nf-ddeml-ddeinitializea)函式中指定了 **CBF \_ 略過 \_ 中斷連接** 旗標，則會篩選此交易。</span><span class="sxs-lookup"><span data-stu-id="b08f4-126">This transaction is filtered if the application specified the **CBF\_SKIP\_DISCONNECTS** flag in the [**DdeInitialize**](/windows/desktop/api/Ddeml/nf-ddeml-ddeinitializea) function.</span></span>

<span data-ttu-id="b08f4-127">應用程式可以在處理此交易時呼叫 [**DdeQueryConvInfo**](/windows/desktop/api/Ddeml/nf-ddeml-ddequeryconvinfo) 函式，以取得已終止交談的狀態。</span><span class="sxs-lookup"><span data-stu-id="b08f4-127">The application can obtain the status of the terminated conversation by calling the [**DdeQueryConvInfo**](/windows/desktop/api/Ddeml/nf-ddeml-ddequeryconvinfo) function while processing this transaction.</span></span> <span data-ttu-id="b08f4-128">在回呼函數傳回之後，交談控制碼會變成無效。</span><span class="sxs-lookup"><span data-stu-id="b08f4-128">The conversation handle becomes invalid after the callback function returns.</span></span>

<span data-ttu-id="b08f4-129">應用程式無法封鎖此交易類型;會忽略 **CBR \_ 區塊** 傳回碼。</span><span class="sxs-lookup"><span data-stu-id="b08f4-129">An application cannot block this transaction type; the **CBR\_BLOCK** return code is ignored.</span></span>

## <a name="requirements"></a><span data-ttu-id="b08f4-130">規格需求</span><span class="sxs-lookup"><span data-stu-id="b08f4-130">Requirements</span></span>



| <span data-ttu-id="b08f4-131">需求</span><span class="sxs-lookup"><span data-stu-id="b08f4-131">Requirement</span></span> | <span data-ttu-id="b08f4-132">值</span><span class="sxs-lookup"><span data-stu-id="b08f4-132">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b08f4-133">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="b08f4-133">Minimum supported client</span></span><br/> | <span data-ttu-id="b08f4-134">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="b08f4-134">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="b08f4-135">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="b08f4-135">Minimum supported server</span></span><br/> | <span data-ttu-id="b08f4-136">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="b08f4-136">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                   |
| <span data-ttu-id="b08f4-137">標頭</span><span class="sxs-lookup"><span data-stu-id="b08f4-137">Header</span></span><br/>                   | <dl> <span data-ttu-id="b08f4-138"><dt>Ddeml (包含) 的 Windows。h </dt></span><span class="sxs-lookup"><span data-stu-id="b08f4-138"><dt>Ddeml.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b08f4-139">另請參閱</span><span class="sxs-lookup"><span data-stu-id="b08f4-139">See also</span></span>

<dl> <dt>

<span data-ttu-id="b08f4-140">**參考**</span><span class="sxs-lookup"><span data-stu-id="b08f4-140">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="b08f4-141">**DdeDisconnect**</span><span class="sxs-lookup"><span data-stu-id="b08f4-141">**DdeDisconnect**</span></span>](/windows/desktop/api/Ddeml/nf-ddeml-ddedisconnect)
</dt> <dt>

[<span data-ttu-id="b08f4-142">**DdeInitialize**</span><span class="sxs-lookup"><span data-stu-id="b08f4-142">**DdeInitialize**</span></span>](/windows/desktop/api/Ddeml/nf-ddeml-ddeinitializea)
</dt> <dt>

[<span data-ttu-id="b08f4-143">**DdeQueryConvInfo**</span><span class="sxs-lookup"><span data-stu-id="b08f4-143">**DdeQueryConvInfo**</span></span>](/windows/desktop/api/Ddeml/nf-ddeml-ddequeryconvinfo)
</dt> <dt>

<span data-ttu-id="b08f4-144">**概念**</span><span class="sxs-lookup"><span data-stu-id="b08f4-144">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="b08f4-145">動態資料交換管理程式庫</span><span class="sxs-lookup"><span data-stu-id="b08f4-145">Dynamic Data Exchange Management Library</span></span>](dynamic-data-exchange-management-library.md)
</dt> </dl>

 

