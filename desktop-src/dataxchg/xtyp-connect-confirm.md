---
title: 'XTYP_CONNECT_CONFIRM 交易 (Ddeml .h) '
description: 動態資料交換 (的 DDE) server 回呼函式 DdeCallback，會收到 XTYP \_ CONNECT \_ confirm 交易，以確認已與用戶端建立交談，以及為伺服器提供交談控制碼。
ms.assetid: 4db67539-9322-44d7-bf2b-749bd6cfcbb4
keywords:
- XTYP_CONNECT_CONFIRM 交易資料交換
topic_type:
- apiref
api_name:
- XTYP_CONNECT_CONFIRM
api_location:
- Ddeml.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e880dfffc7f7825c99ab9e4e3bf980baa978b786
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104384778"
---
# <a name="xtyp_connect_confirm-transaction"></a><span data-ttu-id="ab72b-104">XTYP \_ CONNECT \_ 確認交易</span><span class="sxs-lookup"><span data-stu-id="ab72b-104">XTYP\_CONNECT\_CONFIRM transaction</span></span>

<span data-ttu-id="ab72b-105">動態資料交換 (的 DDE) server 回呼函式 [*DdeCallback*](/windows/win32/api/ddeml/nc-ddeml-pfncallback)，會收到 **XTYP \_ CONNECT \_ confirm** 交易，以確認已與用戶端建立交談，以及為伺服器提供交談控制碼。</span><span class="sxs-lookup"><span data-stu-id="ab72b-105">A Dynamic Data Exchange (DDE) server callback function, [*DdeCallback*](/windows/win32/api/ddeml/nc-ddeml-pfncallback), receives the **XTYP\_CONNECT\_CONFIRM** transaction to confirm that a conversation has been established with a client and to provide the server with the conversation handle.</span></span> <span data-ttu-id="ab72b-106">由於先前的 [**XTYP \_ CONNECT**](xtyp-connect.md) 或 [**XTYP \_ WILDCONNECT**](xtyp-wildconnect.md) 交易的結果，系統會傳送此交易。</span><span class="sxs-lookup"><span data-stu-id="ab72b-106">The system sends this transaction as a result of a previous [**XTYP\_CONNECT**](xtyp-connect.md) or [**XTYP\_WILDCONNECT**](xtyp-wildconnect.md) transaction.</span></span>


```C++
#define     XTYPF_NOBLOCK            0x0002
#define     XCLASS_NOTIFICATION      0x8000
#define     XTYP_CONNECT_CONFIRM    (0x0070 | XCLASS_NOTIFICATION | XTYPF_NOBLOCK)
```



## <a name="parameters"></a><span data-ttu-id="ab72b-107">參數</span><span class="sxs-lookup"><span data-stu-id="ab72b-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ab72b-108">*uType*</span><span class="sxs-lookup"><span data-stu-id="ab72b-108">*uType*</span></span> 
</dt> <dd>

<span data-ttu-id="ab72b-109">交易類型。</span><span class="sxs-lookup"><span data-stu-id="ab72b-109">The transaction type.</span></span>

</dd> <dt>

<span data-ttu-id="ab72b-110">*uFmt*</span><span class="sxs-lookup"><span data-stu-id="ab72b-110">*uFmt*</span></span> 
</dt> <dd>

<span data-ttu-id="ab72b-111">未使用。</span><span class="sxs-lookup"><span data-stu-id="ab72b-111">Not used.</span></span>

</dd> <dt>

<span data-ttu-id="ab72b-112">*hconv*</span><span class="sxs-lookup"><span data-stu-id="ab72b-112">*hconv*</span></span> 
</dt> <dd>

<span data-ttu-id="ab72b-113">新對話的控制碼。</span><span class="sxs-lookup"><span data-stu-id="ab72b-113">A handle to the new conversation.</span></span>

</dd> <dt>

<span data-ttu-id="ab72b-114">*hsz1*</span><span class="sxs-lookup"><span data-stu-id="ab72b-114">*hsz1*</span></span> 
</dt> <dd>

<span data-ttu-id="ab72b-115">已建立交談之主題名稱的控制碼。</span><span class="sxs-lookup"><span data-stu-id="ab72b-115">A handle to the topic name on which the conversation has been established.</span></span>

</dd> <dt>

<span data-ttu-id="ab72b-116">*hsz2*</span><span class="sxs-lookup"><span data-stu-id="ab72b-116">*hsz2*</span></span> 
</dt> <dd>

<span data-ttu-id="ab72b-117">已建立交談之服務名稱的控制碼。</span><span class="sxs-lookup"><span data-stu-id="ab72b-117">A handle to the service name on which the conversation has been established.</span></span>

</dd> <dt>

<span data-ttu-id="ab72b-118">*hdata*</span><span class="sxs-lookup"><span data-stu-id="ab72b-118">*hdata*</span></span> 
</dt> <dd>

<span data-ttu-id="ab72b-119">未使用。</span><span class="sxs-lookup"><span data-stu-id="ab72b-119">Not used.</span></span>

</dd> <dt>

<span data-ttu-id="ab72b-120">*dwData1*</span><span class="sxs-lookup"><span data-stu-id="ab72b-120">*dwData1*</span></span> 
</dt> <dd>

<span data-ttu-id="ab72b-121">未使用。</span><span class="sxs-lookup"><span data-stu-id="ab72b-121">Not used.</span></span>

</dd> <dt>

<span data-ttu-id="ab72b-122">*dwData2*</span><span class="sxs-lookup"><span data-stu-id="ab72b-122">*dwData2*</span></span> 
</dt> <dd>

<span data-ttu-id="ab72b-123">指定用戶端是否與伺服器相同的應用程式實例。</span><span class="sxs-lookup"><span data-stu-id="ab72b-123">Specifies whether the client is the same application instance as the server.</span></span> <span data-ttu-id="ab72b-124">如果參數是1，則用戶端會是相同的實例。</span><span class="sxs-lookup"><span data-stu-id="ab72b-124">If the parameter is 1, the client is the same instance.</span></span> <span data-ttu-id="ab72b-125">如果參數為0，則用戶端為不同的實例。</span><span class="sxs-lookup"><span data-stu-id="ab72b-125">If the parameter is 0, the client is a different instance.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="ab72b-126">備註</span><span class="sxs-lookup"><span data-stu-id="ab72b-126">Remarks</span></span>

<span data-ttu-id="ab72b-127">如果伺服器應用程式在 [**DdeInitialize**](/windows/desktop/api/Ddeml/nf-ddeml-ddeinitializea)函數中指定了 **CBF \_ SKIP \_ CONNECT \_ 確認** 旗標，則會篩選此交易。</span><span class="sxs-lookup"><span data-stu-id="ab72b-127">This transaction is filtered if the server application specified the **CBF\_SKIP\_CONNECT\_CONFIRMS** flag in the [**DdeInitialize**](/windows/desktop/api/Ddeml/nf-ddeml-ddeinitializea) function.</span></span>

<span data-ttu-id="ab72b-128">伺服器無法封鎖此交易類型;會忽略 **CBR \_ 區塊** 傳回碼。</span><span class="sxs-lookup"><span data-stu-id="ab72b-128">A server cannot block this transaction type; the **CBR\_BLOCK** return code is ignored.</span></span>

## <a name="requirements"></a><span data-ttu-id="ab72b-129">規格需求</span><span class="sxs-lookup"><span data-stu-id="ab72b-129">Requirements</span></span>



| <span data-ttu-id="ab72b-130">需求</span><span class="sxs-lookup"><span data-stu-id="ab72b-130">Requirement</span></span> | <span data-ttu-id="ab72b-131">值</span><span class="sxs-lookup"><span data-stu-id="ab72b-131">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ab72b-132">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="ab72b-132">Minimum supported client</span></span><br/> | <span data-ttu-id="ab72b-133">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="ab72b-133">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="ab72b-134">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="ab72b-134">Minimum supported server</span></span><br/> | <span data-ttu-id="ab72b-135">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="ab72b-135">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                   |
| <span data-ttu-id="ab72b-136">標頭</span><span class="sxs-lookup"><span data-stu-id="ab72b-136">Header</span></span><br/>                   | <dl> <span data-ttu-id="ab72b-137"><dt>Ddeml (包含) 的 Windows。h </dt></span><span class="sxs-lookup"><span data-stu-id="ab72b-137"><dt>Ddeml.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ab72b-138">另請參閱</span><span class="sxs-lookup"><span data-stu-id="ab72b-138">See also</span></span>

<dl> <dt>

<span data-ttu-id="ab72b-139">**參考**</span><span class="sxs-lookup"><span data-stu-id="ab72b-139">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="ab72b-140">**DdeConnect**</span><span class="sxs-lookup"><span data-stu-id="ab72b-140">**DdeConnect**</span></span>](/windows/desktop/api/Ddeml/nf-ddeml-ddeconnect)
</dt> <dt>

[<span data-ttu-id="ab72b-141">**DdeConnectList**</span><span class="sxs-lookup"><span data-stu-id="ab72b-141">**DdeConnectList**</span></span>](/windows/desktop/api/Ddeml/nf-ddeml-ddeconnectlist)
</dt> <dt>

[<span data-ttu-id="ab72b-142">**DdeInitialize**</span><span class="sxs-lookup"><span data-stu-id="ab72b-142">**DdeInitialize**</span></span>](/windows/desktop/api/Ddeml/nf-ddeml-ddeinitializea)
</dt> <dt>

<span data-ttu-id="ab72b-143">**概念**</span><span class="sxs-lookup"><span data-stu-id="ab72b-143">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="ab72b-144">動態資料交換管理程式庫</span><span class="sxs-lookup"><span data-stu-id="ab72b-144">Dynamic Data Exchange Management Library</span></span>](dynamic-data-exchange-management-library.md)
</dt> </dl>

 

