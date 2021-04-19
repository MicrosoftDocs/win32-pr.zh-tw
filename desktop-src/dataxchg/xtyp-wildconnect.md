---
title: 'XTYP_WILDCONNECT 交易 (Ddeml .h) '
description: 讓用戶端能夠在每個伺服器的服務名稱和主題名稱組上，建立符合指定服務名稱和主題名稱的交談。
ms.assetid: 4651e14f-ca13-412e-853d-326a13db78e4
keywords:
- XTYP_WILDCONNECT 交易資料交換
topic_type:
- apiref
api_name:
- XTYP_WILDCONNECT
api_location:
- Ddeml.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cc63d6c367aebc440418beaabb0a06f05b0df967
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106966310"
---
# <a name="xtyp_wildconnect-transaction"></a><span data-ttu-id="b0f08-104">XTYP \_ WILDCONNECT 交易</span><span class="sxs-lookup"><span data-stu-id="b0f08-104">XTYP\_WILDCONNECT transaction</span></span>

<span data-ttu-id="b0f08-105">讓用戶端能夠在每個伺服器的服務名稱和主題名稱組上，建立符合指定服務名稱和主題名稱的交談。</span><span class="sxs-lookup"><span data-stu-id="b0f08-105">Enables a client to establish a conversation on each of the server's service name and topic name pairs that match the specified service name and topic name.</span></span> <span data-ttu-id="b0f08-106">當用戶端在 [**DdeConnect**](/windows/desktop/api/Ddeml/nf-ddeml-ddeconnect)或 [**DdeConnectList**](/windows/desktop/api/Ddeml/nf-ddeml-ddeconnectlist)函式的呼叫中指定 **null** 服務名稱、 **null** 主題名稱或兩者都指定時，動態資料交換 (DDE) server 回呼函式 [*DdeCallback*](/windows/win32/api/ddeml/nc-ddeml-pfncallback)會接收此交易。</span><span class="sxs-lookup"><span data-stu-id="b0f08-106">A Dynamic Data Exchange (DDE) server callback function, [*DdeCallback*](/windows/win32/api/ddeml/nc-ddeml-pfncallback), receives this transaction when a client specifies a **NULL** service name, a **NULL** topic name, or both in a call to the [**DdeConnect**](/windows/desktop/api/Ddeml/nf-ddeml-ddeconnect) or [**DdeConnectList**](/windows/desktop/api/Ddeml/nf-ddeml-ddeconnectlist) function.</span></span>


```C++
#define     XCLASS_DATA              0x2000
#define     XTYPF_NOBLOCK            0x0002
#define     XTYP_WILDCONNECT        (0x00E0 | XCLASS_DATA | XTYPF_NOBLOCK)
```



## <a name="parameters"></a><span data-ttu-id="b0f08-107">參數</span><span class="sxs-lookup"><span data-stu-id="b0f08-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b0f08-108">*uType*</span><span class="sxs-lookup"><span data-stu-id="b0f08-108">*uType*</span></span> 
</dt> <dd>

<span data-ttu-id="b0f08-109">交易類型。</span><span class="sxs-lookup"><span data-stu-id="b0f08-109">The transaction type.</span></span>

</dd> <dt>

<span data-ttu-id="b0f08-110">*uFmt*</span><span class="sxs-lookup"><span data-stu-id="b0f08-110">*uFmt*</span></span> 
</dt> <dd>

<span data-ttu-id="b0f08-111">未使用。</span><span class="sxs-lookup"><span data-stu-id="b0f08-111">Not used.</span></span>

</dd> <dt>

<span data-ttu-id="b0f08-112">*hconv*</span><span class="sxs-lookup"><span data-stu-id="b0f08-112">*hconv*</span></span> 
</dt> <dd>

<span data-ttu-id="b0f08-113">未使用。</span><span class="sxs-lookup"><span data-stu-id="b0f08-113">Not used.</span></span>

</dd> <dt>

<span data-ttu-id="b0f08-114">*hsz1*</span><span class="sxs-lookup"><span data-stu-id="b0f08-114">*hsz1*</span></span> 
</dt> <dd>

<span data-ttu-id="b0f08-115">主題名稱的控制碼。</span><span class="sxs-lookup"><span data-stu-id="b0f08-115">A handle to the topic name.</span></span> <span data-ttu-id="b0f08-116">如果這個參數是 **Null**，用戶端會要求伺服器支援的所有主題名稱上進行交談。</span><span class="sxs-lookup"><span data-stu-id="b0f08-116">If this parameter is **NULL**, the client is requesting a conversation on all topic names that the server supports.</span></span>

</dd> <dt>

<span data-ttu-id="b0f08-117">*hsz2*</span><span class="sxs-lookup"><span data-stu-id="b0f08-117">*hsz2*</span></span> 
</dt> <dd>

<span data-ttu-id="b0f08-118">服務名稱的控制碼。</span><span class="sxs-lookup"><span data-stu-id="b0f08-118">A handle to the service name.</span></span> <span data-ttu-id="b0f08-119">如果這個參數是 **Null**，用戶端會要求伺服器支援的所有服務名稱上進行交談。</span><span class="sxs-lookup"><span data-stu-id="b0f08-119">If this parameter is **NULL**, the client is requesting a conversation on all service names that the server supports.</span></span>

</dd> <dt>

<span data-ttu-id="b0f08-120">*hdata*</span><span class="sxs-lookup"><span data-stu-id="b0f08-120">*hdata*</span></span> 
</dt> <dd>

<span data-ttu-id="b0f08-121">未使用。</span><span class="sxs-lookup"><span data-stu-id="b0f08-121">Not used.</span></span>

</dd> <dt>

<span data-ttu-id="b0f08-122">*dwData1*</span><span class="sxs-lookup"><span data-stu-id="b0f08-122">*dwData1*</span></span> 
</dt> <dd>

<span data-ttu-id="b0f08-123">[**CONVCONTEXT**](/windows/win32/api/ddeml/ns-ddeml-convcontext)結構的指標，其中包含交談的內容資訊。</span><span class="sxs-lookup"><span data-stu-id="b0f08-123">A pointer to a [**CONVCONTEXT**](/windows/win32/api/ddeml/ns-ddeml-convcontext) structure that contains context information for the conversation.</span></span> <span data-ttu-id="b0f08-124">如果用戶端不是 DDEML 應用程式，此參數會設定為0。</span><span class="sxs-lookup"><span data-stu-id="b0f08-124">If the client is not a DDEML application, this parameter is set to 0.</span></span>

</dd> <dt>

<span data-ttu-id="b0f08-125">*dwData2*</span><span class="sxs-lookup"><span data-stu-id="b0f08-125">*dwData2*</span></span> 
</dt> <dd>

<span data-ttu-id="b0f08-126">指定用戶端是否與伺服器相同的應用程式實例。</span><span class="sxs-lookup"><span data-stu-id="b0f08-126">Specifies whether the client is the same application instance as the server.</span></span> <span data-ttu-id="b0f08-127">如果參數是1，則用戶端會是相同的實例。</span><span class="sxs-lookup"><span data-stu-id="b0f08-127">If the parameter is 1, the client is same instance.</span></span> <span data-ttu-id="b0f08-128">如果參數為0，則用戶端為不同的實例。</span><span class="sxs-lookup"><span data-stu-id="b0f08-128">If the parameter is 0, the client is a different instance.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b0f08-129">傳回值</span><span class="sxs-lookup"><span data-stu-id="b0f08-129">Return value</span></span>

<span data-ttu-id="b0f08-130">伺服器應傳回識別 [**HSZPAIR**](/windows/win32/api/ddeml/ns-ddeml-hszpair) 結構陣列的資料控制碼。</span><span class="sxs-lookup"><span data-stu-id="b0f08-130">The server should return a data handle that identifies an array of [**HSZPAIR**](/windows/win32/api/ddeml/ns-ddeml-hszpair) structures.</span></span> <span data-ttu-id="b0f08-131">陣列應針對符合用戶端所要求的服務名稱和主題名稱組的每個服務名稱和主題名稱組，各包含一個結構。</span><span class="sxs-lookup"><span data-stu-id="b0f08-131">The array should contain one structure for each service-name and topic-name pair that matches the service-name and topic-name pair requested by the client.</span></span> <span data-ttu-id="b0f08-132">陣列必須以 **Null** 字串控制碼終止。</span><span class="sxs-lookup"><span data-stu-id="b0f08-132">The array must be terminated by a **NULL** string handle.</span></span> <span data-ttu-id="b0f08-133">系統會將 [**XTYP \_ CONNECT \_ 確認**](xtyp-connect-confirm.md) 交易傳送到伺服器，以確認每個交談並將交談控制碼傳遞至伺服器。</span><span class="sxs-lookup"><span data-stu-id="b0f08-133">The system sends the [**XTYP\_CONNECT\_CONFIRM**](xtyp-connect-confirm.md) transaction to the server to confirm each conversation and to pass the conversation handles to the server.</span></span> <span data-ttu-id="b0f08-134">如果伺服器在 [**DdeInitialize**](/windows/desktop/api/Ddeml/nf-ddeml-ddeinitializea)函數中指定了 **CBF \_ SKIP \_ CONNECT \_ 確認** 旗標，伺服器將不會收到這些確認。</span><span class="sxs-lookup"><span data-stu-id="b0f08-134">The server will not receive these confirmations if it specified the **CBF\_SKIP\_CONNECT\_CONFIRMS** flag in the [**DdeInitialize**](/windows/desktop/api/Ddeml/nf-ddeml-ddeinitializea) function.</span></span>

<span data-ttu-id="b0f08-135">伺服器應傳回 **Null** 以拒絕 **XTYP \_ WILDCONNECT** 交易。</span><span class="sxs-lookup"><span data-stu-id="b0f08-135">The server should return **NULL** to refuse the **XTYP\_WILDCONNECT** transaction.</span></span>

## <a name="remarks"></a><span data-ttu-id="b0f08-136">備註</span><span class="sxs-lookup"><span data-stu-id="b0f08-136">Remarks</span></span>

<span data-ttu-id="b0f08-137">如果伺服器應用程式在 [**DdeInitialize**](/windows/desktop/api/Ddeml/nf-ddeml-ddeinitializea)函數中指定了 **CBF \_ FAIL \_ CONNECTIONS 連接** 旗標，則會篩選此交易。</span><span class="sxs-lookup"><span data-stu-id="b0f08-137">This transaction is filtered if the server application specified the **CBF\_FAIL\_CONNECTIONS** flag in the [**DdeInitialize**](/windows/desktop/api/Ddeml/nf-ddeml-ddeinitializea) function.</span></span>

<span data-ttu-id="b0f08-138">伺服器無法封鎖此交易類型;\_會忽略 CBR 區塊傳回碼。</span><span class="sxs-lookup"><span data-stu-id="b0f08-138">A server cannot block this transaction type; the CBR\_BLOCK return code is ignored.</span></span>

## <a name="requirements"></a><span data-ttu-id="b0f08-139">規格需求</span><span class="sxs-lookup"><span data-stu-id="b0f08-139">Requirements</span></span>



| <span data-ttu-id="b0f08-140">需求</span><span class="sxs-lookup"><span data-stu-id="b0f08-140">Requirement</span></span> | <span data-ttu-id="b0f08-141">值</span><span class="sxs-lookup"><span data-stu-id="b0f08-141">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b0f08-142">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="b0f08-142">Minimum supported client</span></span><br/> | <span data-ttu-id="b0f08-143">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="b0f08-143">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="b0f08-144">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="b0f08-144">Minimum supported server</span></span><br/> | <span data-ttu-id="b0f08-145">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="b0f08-145">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                   |
| <span data-ttu-id="b0f08-146">標頭</span><span class="sxs-lookup"><span data-stu-id="b0f08-146">Header</span></span><br/>                   | <dl> <span data-ttu-id="b0f08-147"><dt>Ddeml (包含) 的 Windows。h </dt></span><span class="sxs-lookup"><span data-stu-id="b0f08-147"><dt>Ddeml.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b0f08-148">另請參閱</span><span class="sxs-lookup"><span data-stu-id="b0f08-148">See also</span></span>

<dl> <dt>

<span data-ttu-id="b0f08-149">**參考**</span><span class="sxs-lookup"><span data-stu-id="b0f08-149">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="b0f08-150">**CONVCONTEXT**</span><span class="sxs-lookup"><span data-stu-id="b0f08-150">**CONVCONTEXT**</span></span>](/windows/win32/api/ddeml/ns-ddeml-convcontext)
</dt> <dt>

[<span data-ttu-id="b0f08-151">**DdeConnect**</span><span class="sxs-lookup"><span data-stu-id="b0f08-151">**DdeConnect**</span></span>](/windows/desktop/api/Ddeml/nf-ddeml-ddeconnect)
</dt> <dt>

[<span data-ttu-id="b0f08-152">**DdeInitialize**</span><span class="sxs-lookup"><span data-stu-id="b0f08-152">**DdeInitialize**</span></span>](/windows/desktop/api/Ddeml/nf-ddeml-ddeinitializea)
</dt> <dt>

[<span data-ttu-id="b0f08-153">**HSZPAIR**</span><span class="sxs-lookup"><span data-stu-id="b0f08-153">**HSZPAIR**</span></span>](/windows/win32/api/ddeml/ns-ddeml-hszpair)
</dt> <dt>

<span data-ttu-id="b0f08-154">**概念**</span><span class="sxs-lookup"><span data-stu-id="b0f08-154">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="b0f08-155">動態資料交換管理程式庫</span><span class="sxs-lookup"><span data-stu-id="b0f08-155">Dynamic Data Exchange Management Library</span></span>](dynamic-data-exchange-management-library.md)
</dt> </dl>

 

