---
title: 'XTYP_CONNECT 交易 (Ddeml .h) '
description: 用戶端會使用 XTYP \_ CONNECT 交易來建立交談。
ms.assetid: 74f43b10-f7ac-4370-9caa-7b9ddf3413ed
keywords:
- XTYP_CONNECT 交易資料交換
topic_type:
- apiref
api_name:
- XTYP_CONNECT
api_location:
- Ddeml.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e2268994f1be000373691d6c25dbb7220d3e109e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104104076"
---
# <a name="xtyp_connect-transaction"></a><span data-ttu-id="d692c-104">XTYP \_ CONNECT 交易</span><span class="sxs-lookup"><span data-stu-id="d692c-104">XTYP\_CONNECT transaction</span></span>

<span data-ttu-id="d692c-105">用戶端會使用 **XTYP \_ CONNECT** 交易來建立交談。</span><span class="sxs-lookup"><span data-stu-id="d692c-105">A client uses the **XTYP\_CONNECT** transaction to establish a conversation.</span></span> <span data-ttu-id="d692c-106">當用戶端指定伺服器支援 (的服務名稱，以及在 [**DdeConnect**](/windows/desktop/api/Ddeml/nf-ddeml-ddeconnect)函式的呼叫中) 非 **Null** 的主題名稱時，動態資料交換 (DDE) Server 回呼函式 [*DdeCallback*](/windows/win32/api/ddeml/nc-ddeml-pfncallback)會接收此交易。</span><span class="sxs-lookup"><span data-stu-id="d692c-106">A Dynamic Data Exchange (DDE) server callback function, [*DdeCallback*](/windows/win32/api/ddeml/nc-ddeml-pfncallback), receives this transaction when a client specifies a service name that the server supports (and a topic name that is not **NULL**) in a call to the [**DdeConnect**](/windows/desktop/api/Ddeml/nf-ddeml-ddeconnect) function.</span></span>


```C++
#define     XCLASS_BOOL              0x1000
#define     XTYPF_NOBLOCK            0x0002
#define     XTYP_CONNECT            (0x0060 | XCLASS_BOOL | XTYPF_NOBLOCK)
```



## <a name="parameters"></a><span data-ttu-id="d692c-107">參數</span><span class="sxs-lookup"><span data-stu-id="d692c-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d692c-108">*uType*</span><span class="sxs-lookup"><span data-stu-id="d692c-108">*uType*</span></span> 
</dt> <dd>

<span data-ttu-id="d692c-109">交易類型。</span><span class="sxs-lookup"><span data-stu-id="d692c-109">The transaction type.</span></span>

</dd> <dt>

<span data-ttu-id="d692c-110">*uFmt*</span><span class="sxs-lookup"><span data-stu-id="d692c-110">*uFmt*</span></span> 
</dt> <dd>

<span data-ttu-id="d692c-111">未使用。</span><span class="sxs-lookup"><span data-stu-id="d692c-111">Not used.</span></span>

</dd> <dt>

<span data-ttu-id="d692c-112">*hconv*</span><span class="sxs-lookup"><span data-stu-id="d692c-112">*hconv*</span></span> 
</dt> <dd>

<span data-ttu-id="d692c-113">未使用。</span><span class="sxs-lookup"><span data-stu-id="d692c-113">Not used.</span></span>

</dd> <dt>

<span data-ttu-id="d692c-114">*hsz1*</span><span class="sxs-lookup"><span data-stu-id="d692c-114">*hsz1*</span></span> 
</dt> <dd>

<span data-ttu-id="d692c-115">主題名稱的控制碼。</span><span class="sxs-lookup"><span data-stu-id="d692c-115">A handle to the topic name.</span></span>

</dd> <dt>

<span data-ttu-id="d692c-116">*hsz2*</span><span class="sxs-lookup"><span data-stu-id="d692c-116">*hsz2*</span></span> 
</dt> <dd>

<span data-ttu-id="d692c-117">服務名稱的控制碼。</span><span class="sxs-lookup"><span data-stu-id="d692c-117">A handle to the service name.</span></span>

</dd> <dt>

<span data-ttu-id="d692c-118">*hdata*</span><span class="sxs-lookup"><span data-stu-id="d692c-118">*hdata*</span></span> 
</dt> <dd>

<span data-ttu-id="d692c-119">未使用。</span><span class="sxs-lookup"><span data-stu-id="d692c-119">Not used.</span></span>

</dd> <dt>

<span data-ttu-id="d692c-120">*dwData1*</span><span class="sxs-lookup"><span data-stu-id="d692c-120">*dwData1*</span></span> 
</dt> <dd>

<span data-ttu-id="d692c-121">[**CONVCONTEXT**](/windows/win32/api/ddeml/ns-ddeml-convcontext)結構的指標，其中包含交談的內容資訊。</span><span class="sxs-lookup"><span data-stu-id="d692c-121">A pointer to a [**CONVCONTEXT**](/windows/win32/api/ddeml/ns-ddeml-convcontext) structure that contains context information for the conversation.</span></span> <span data-ttu-id="d692c-122">如果用戶端不是 DDEML 應用程式，此參數為0。</span><span class="sxs-lookup"><span data-stu-id="d692c-122">If the client is not a DDEML application, this parameter is 0.</span></span>

</dd> <dt>

<span data-ttu-id="d692c-123">*dwData2*</span><span class="sxs-lookup"><span data-stu-id="d692c-123">*dwData2*</span></span> 
</dt> <dd>

<span data-ttu-id="d692c-124">指定用戶端是否與伺服器相同的應用程式實例。</span><span class="sxs-lookup"><span data-stu-id="d692c-124">Specifies whether the client is the same application instance as the server.</span></span> <span data-ttu-id="d692c-125">如果參數是1，則用戶端會是相同的實例。</span><span class="sxs-lookup"><span data-stu-id="d692c-125">If the parameter is 1, the client is the same instance.</span></span> <span data-ttu-id="d692c-126">如果參數為0，則用戶端為不同的實例。</span><span class="sxs-lookup"><span data-stu-id="d692c-126">If the parameter is 0, the client is a different instance.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d692c-127">傳回值</span><span class="sxs-lookup"><span data-stu-id="d692c-127">Return value</span></span>

<span data-ttu-id="d692c-128">伺服器回呼函數應該傳回 **TRUE** ，以允許用戶端在指定的服務名稱和主題名稱組上建立交談，否則函數應該會傳回 **FALSE** 以拒絕交談。</span><span class="sxs-lookup"><span data-stu-id="d692c-128">A server callback function should return **TRUE** to allow the client to establish a conversation on the specified service name and topic name pair, or the function should return **FALSE** to deny the conversation.</span></span> <span data-ttu-id="d692c-129">如果回呼函式傳回 **TRUE** 且已成功建立交談，則系統會將 [**XTYP \_ CONNECT \_ 確認**](xtyp-connect-confirm.md)交易發出至伺服器的回呼函式，藉此將交談控制碼傳遞給伺服器 (除非伺服器在 [**DdeInitialize**](/windows/desktop/api/Ddeml/nf-ddeml-ddeinitializea)函式) 中指定了 **CBF \_ SKIP \_ CONNECT \_ 確認** 旗標。</span><span class="sxs-lookup"><span data-stu-id="d692c-129">If the callback function returns **TRUE** and a conversation is successfully established, the system passes the conversation handle to the server by issuing an [**XTYP\_CONNECT\_CONFIRM**](xtyp-connect-confirm.md) transaction to the server's callback function (unless the server specified the **CBF\_SKIP\_CONNECT\_CONFIRMS** flag in the [**DdeInitialize**](/windows/desktop/api/Ddeml/nf-ddeml-ddeinitializea) function).</span></span>

## <a name="remarks"></a><span data-ttu-id="d692c-130">備註</span><span class="sxs-lookup"><span data-stu-id="d692c-130">Remarks</span></span>

<span data-ttu-id="d692c-131">如果伺服器應用程式在 [**DdeInitialize**](/windows/desktop/api/Ddeml/nf-ddeml-ddeinitializea)函數中指定了 **CBF \_ FAIL \_ CONNECTIONS 連接** 旗標，則會篩選此交易。</span><span class="sxs-lookup"><span data-stu-id="d692c-131">This transaction is filtered if the server application specified the **CBF\_FAIL\_CONNECTIONS** flag in the [**DdeInitialize**](/windows/desktop/api/Ddeml/nf-ddeml-ddeinitializea) function.</span></span>

<span data-ttu-id="d692c-132">伺服器無法封鎖此交易類型;會忽略 **CBR \_ 區塊** 傳回碼。</span><span class="sxs-lookup"><span data-stu-id="d692c-132">A server cannot block this transaction type; the **CBR\_BLOCK** return code is ignored.</span></span>

## <a name="requirements"></a><span data-ttu-id="d692c-133">規格需求</span><span class="sxs-lookup"><span data-stu-id="d692c-133">Requirements</span></span>



| <span data-ttu-id="d692c-134">需求</span><span class="sxs-lookup"><span data-stu-id="d692c-134">Requirement</span></span> | <span data-ttu-id="d692c-135">值</span><span class="sxs-lookup"><span data-stu-id="d692c-135">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d692c-136">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="d692c-136">Minimum supported client</span></span><br/> | <span data-ttu-id="d692c-137">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="d692c-137">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="d692c-138">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="d692c-138">Minimum supported server</span></span><br/> | <span data-ttu-id="d692c-139">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="d692c-139">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                   |
| <span data-ttu-id="d692c-140">標頭</span><span class="sxs-lookup"><span data-stu-id="d692c-140">Header</span></span><br/>                   | <dl> <span data-ttu-id="d692c-141"><dt>Ddeml (包含) 的 Windows。h </dt></span><span class="sxs-lookup"><span data-stu-id="d692c-141"><dt>Ddeml.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d692c-142">另請參閱</span><span class="sxs-lookup"><span data-stu-id="d692c-142">See also</span></span>

<dl> <dt>

<span data-ttu-id="d692c-143">**參考**</span><span class="sxs-lookup"><span data-stu-id="d692c-143">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="d692c-144">**CONVCONTEXT**</span><span class="sxs-lookup"><span data-stu-id="d692c-144">**CONVCONTEXT**</span></span>](/windows/win32/api/ddeml/ns-ddeml-convcontext)
</dt> <dt>

[<span data-ttu-id="d692c-145">**DdeConnect**</span><span class="sxs-lookup"><span data-stu-id="d692c-145">**DdeConnect**</span></span>](/windows/desktop/api/Ddeml/nf-ddeml-ddeconnect)
</dt> <dt>

[<span data-ttu-id="d692c-146">**DdeInitialize**</span><span class="sxs-lookup"><span data-stu-id="d692c-146">**DdeInitialize**</span></span>](/windows/desktop/api/Ddeml/nf-ddeml-ddeinitializea)
</dt> <dt>

<span data-ttu-id="d692c-147">**概念**</span><span class="sxs-lookup"><span data-stu-id="d692c-147">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="d692c-148">動態資料交換管理程式庫</span><span class="sxs-lookup"><span data-stu-id="d692c-148">Dynamic Data Exchange Management Library</span></span>](dynamic-data-exchange-management-library.md)
</dt> </dl>

 

