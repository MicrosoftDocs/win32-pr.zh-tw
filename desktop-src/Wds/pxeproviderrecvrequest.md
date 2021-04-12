---
title: PxeProviderRecvRequest 回呼函式
description: 從用戶端收到要求時呼叫。
ms.assetid: 704972d5-177a-490e-881f-d2b3025babda
keywords:
- PxeProviderRecvRequest 回呼函式 Windows 部署服務
topic_type:
- apiref
api_name:
- PxeProviderRecvRequest
api_type:
- UserDefined
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: a173c6ba356d98dfd44beb64033f491b9c200d58
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104384665"
---
# <a name="pxeproviderrecvrequest-callback-function"></a><span data-ttu-id="3ccf6-104">PxeProviderRecvRequest 回呼函式</span><span class="sxs-lookup"><span data-stu-id="3ccf6-104">PxeProviderRecvRequest callback function</span></span>

<span data-ttu-id="3ccf6-105">從用戶端收到要求時呼叫。</span><span class="sxs-lookup"><span data-stu-id="3ccf6-105">Called when a request is received from a client.</span></span> <span data-ttu-id="3ccf6-106">此函式的註冊方式是呼叫 [**PxeRegisterCallback**](/windows/desktop/api/WdsPxe/nf-wdspxe-pxeregistercallback) 函式，並將 *CallbackType* 參數設定為 **PXE \_ 回呼 \_ 接收 \_ 要求**。</span><span class="sxs-lookup"><span data-stu-id="3ccf6-106">This function is registered by calling the [**PxeRegisterCallback**](/windows/desktop/api/WdsPxe/nf-wdspxe-pxeregistercallback) function with the *CallbackType* parameter set to **PXE\_CALLBACK\_RECV\_REQUEST**.</span></span>

## <a name="syntax"></a><span data-ttu-id="3ccf6-107">語法</span><span class="sxs-lookup"><span data-stu-id="3ccf6-107">Syntax</span></span>


```C++
DWORD PXEAPI PxeProviderRecvRequest(
  _In_  HANDLE          hClientRequest,
  _In_  PVOID           pPacket,
  _In_  ULONG           uPacketLen,
  _In_  PXE_ADDRESS     *pLocalAddress,
  _In_  PXE_ADDRESS     *pRemoteAddress,
  _Out_ PXE_BOOT_ACTION pAction,
  _In_  PVOID           pContext
);
```



## <a name="parameters"></a><span data-ttu-id="3ccf6-108">參數</span><span class="sxs-lookup"><span data-stu-id="3ccf6-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3ccf6-109">*hClientRequest* \[在\]</span><span class="sxs-lookup"><span data-stu-id="3ccf6-109">*hClientRequest* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3ccf6-110">從用戶端收到的要求控制碼。</span><span class="sxs-lookup"><span data-stu-id="3ccf6-110">Handle to a request received from a client.</span></span>

</dd> <dt>

<span data-ttu-id="3ccf6-111">*pPacket* \[在\]</span><span class="sxs-lookup"><span data-stu-id="3ccf6-111">*pPacket* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3ccf6-112">記憶體緩衝區的指標，其中包含已接收的封包。</span><span class="sxs-lookup"><span data-stu-id="3ccf6-112">Pointer to the memory buffer that contains the received packet.</span></span>

</dd> <dt>

<span data-ttu-id="3ccf6-113">*uPacketLen* \[在\]</span><span class="sxs-lookup"><span data-stu-id="3ccf6-113">*uPacketLen* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3ccf6-114">*PPacket* 參數所指向之緩衝區的長度（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="3ccf6-114">Length, in bytes, of the buffer pointed to by the *pPacket* parameter.</span></span>

</dd> <dt>

<span data-ttu-id="3ccf6-115">*pLocalAddress* \[在\]</span><span class="sxs-lookup"><span data-stu-id="3ccf6-115">*pLocalAddress* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3ccf6-116">[**PXE \_ 位址**](/windows/win32/api/wdspxe/ns-wdspxe-pxe_address)結構的指標，其中包含接收封包的本機位址。</span><span class="sxs-lookup"><span data-stu-id="3ccf6-116">Pointer to a [**PXE\_ADDRESS**](/windows/win32/api/wdspxe/ns-wdspxe-pxe_address) structure that contains the local address on which the packet was received.</span></span>

</dd> <dt>

<span data-ttu-id="3ccf6-117">*pRemoteAddress* \[在\]</span><span class="sxs-lookup"><span data-stu-id="3ccf6-117">*pRemoteAddress* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3ccf6-118">包含封包來源位址之 [**PXE \_ 位址**](/windows/win32/api/wdspxe/ns-wdspxe-pxe_address) 結構的指標。</span><span class="sxs-lookup"><span data-stu-id="3ccf6-118">Pointer to a [**PXE\_ADDRESS**](/windows/win32/api/wdspxe/ns-wdspxe-pxe_address) structure that contains the source address of the packet.</span></span>

</dd> <dt>

<span data-ttu-id="3ccf6-119">*pAction* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="3ccf6-119">*pAction* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="3ccf6-120">指定系統應該採取的動作。</span><span class="sxs-lookup"><span data-stu-id="3ccf6-120">Specifies the action that the system should take.</span></span>



| <span data-ttu-id="3ccf6-121">值</span><span class="sxs-lookup"><span data-stu-id="3ccf6-121">Value</span></span>                                                                                                                                                                                                                       | <span data-ttu-id="3ccf6-122">意義</span><span class="sxs-lookup"><span data-stu-id="3ccf6-122">Meaning</span></span>                                                                                                                                                                                                                                                                                                                       |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="PXE_BA_NBP"></span><span id="pxe_ba_nbp"></span><dl> <span data-ttu-id="3ccf6-123"><dt>**PXE \_BA \_ NBP**</dt> <dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="3ccf6-123"><dt>**PXE\_BA\_NBP**</dt> <dt>1</dt></span></span> </dl>                | <span data-ttu-id="3ccf6-124">此提供者會使用包含網路開機程式路徑的標準 DHCP 回應封包，回復至用戶端。</span><span class="sxs-lookup"><span data-stu-id="3ccf6-124">The provider replied to a client with a standard DHCP response packet that contains a path to the Network Boot Program.</span></span> <span data-ttu-id="3ccf6-125">傳回此動作表示提供者已成功呼叫 [**PxeSendReply**](/windows/desktop/api/WdsPxe/nf-wdspxe-pxesendreply) 函數一次，以順利完成用戶端要求。</span><span class="sxs-lookup"><span data-stu-id="3ccf6-125">Returning this action means that the provider successfully completed the client request by calling the [**PxeSendReply**](/windows/desktop/api/WdsPxe/nf-wdspxe-pxesendreply) function at least once.</span></span><br/>                        |
| <span id="PXE_BA_CUSTOM"></span><span id="pxe_ba_custom"></span><dl> <span data-ttu-id="3ccf6-126"><dt>**PXE \_BA \_ 自訂**</dt> <dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="3ccf6-126"><dt>**PXE\_BA\_CUSTOM**</dt> <dt>2</dt></span></span> </dl>       | <span data-ttu-id="3ccf6-127">提供者使用不符合 DHCP 規格的自訂回應來回複用戶端。</span><span class="sxs-lookup"><span data-stu-id="3ccf6-127">The provider replied to a client by using a custom response that does not conform to DHCP specifications.</span></span> <span data-ttu-id="3ccf6-128">傳回此動作表示提供者已成功呼叫 [**PxeSendReply**](/windows/desktop/api/WdsPxe/nf-wdspxe-pxesendreply) 函數一次，以順利完成用戶端要求。</span><span class="sxs-lookup"><span data-stu-id="3ccf6-128">Returning this action means that the provider successfully completed the client request by calling the [**PxeSendReply**](/windows/desktop/api/WdsPxe/nf-wdspxe-pxesendreply) function at least once.</span></span><br/>                                      |
| <span id="PXE_BA_IGNORE"></span><span id="pxe_ba_ignore"></span><dl> <span data-ttu-id="3ccf6-129"><dt>**PXE \_BA \_ 忽略**</dt> <dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="3ccf6-129"><dt>**PXE\_BA\_IGNORE**</dt> <dt>3</dt></span></span> </dl>       | <span data-ttu-id="3ccf6-130">提供者不會想要服務用戶端要求，且不應將要求傳遞給下一個提供者。</span><span class="sxs-lookup"><span data-stu-id="3ccf6-130">The provider does not want to service the client request and the request should not be passed to the next provider.</span></span> <span data-ttu-id="3ccf6-131">所有與用戶端要求相關聯的資源都會釋出，並忽略用戶端要求。</span><span class="sxs-lookup"><span data-stu-id="3ccf6-131">All resources associated with the client request are released and the client request is ignored.</span></span> <span data-ttu-id="3ccf6-132">如果提供者辨識用戶端，但要求的格式不正確，則也可以使用此值。</span><span class="sxs-lookup"><span data-stu-id="3ccf6-132">Providers can also use this value if they recognize the client but the request was malformed.</span></span><br/> |
| <span id="PXE_BA_REJECTED"></span><span id="pxe_ba_rejected"></span><dl> <span data-ttu-id="3ccf6-133"><dt>**PXE \_BA 已 \_ 拒絕**</dt> <dt>4</dt></span><span class="sxs-lookup"><span data-stu-id="3ccf6-133"><dt>**PXE\_BA\_REJECTED**</dt> <dt>4</dt></span></span> </dl> | <span data-ttu-id="3ccf6-134">提供者不想要服務用戶端要求。</span><span class="sxs-lookup"><span data-stu-id="3ccf6-134">The provider does not want to service the client request.</span></span> <span data-ttu-id="3ccf6-135">系統會將要求傳遞給已註冊之提供者清單中的下一個提供者。</span><span class="sxs-lookup"><span data-stu-id="3ccf6-135">The system passes the request to the next provider in the list of registered providers.</span></span> <span data-ttu-id="3ccf6-136">如果這是清單中的最後一個提供者，則會釋放與用戶端要求相關聯的所有資源，並忽略用戶端要求。</span><span class="sxs-lookup"><span data-stu-id="3ccf6-136">If this was the last provider in the list, then all resources associated with the client request are released and client request is ignored.</span></span><br/>                     |



 

</dd> <dt>

<span data-ttu-id="3ccf6-137">*pCoNtext* \[在\]</span><span class="sxs-lookup"><span data-stu-id="3ccf6-137">*pContext* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3ccf6-138">傳遞至 [**PxeRegisterCallback**](/windows/desktop/api/WdsPxe/nf-wdspxe-pxeregistercallback) 函數的內容值。</span><span class="sxs-lookup"><span data-stu-id="3ccf6-138">Context value passed to the [**PxeRegisterCallback**](/windows/desktop/api/WdsPxe/nf-wdspxe-pxeregistercallback) function.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3ccf6-139">傳回值</span><span class="sxs-lookup"><span data-stu-id="3ccf6-139">Return value</span></span>

<span data-ttu-id="3ccf6-140">如果提供者已成功處理用戶端要求，回呼應該會傳回 **錯誤 \_ 成功**，而 *pAction* 參數所指向的 **PXE \_ 開機 \_ 動作** 則包含此要求的適當開機動作。</span><span class="sxs-lookup"><span data-stu-id="3ccf6-140">If the provider successfully processed the client request, the callback should return **ERROR\_SUCCESS** and the **PXE\_BOOT\_ACTION** pointed to by the *pAction* parameter contains the appropriate boot action for this request.</span></span> <span data-ttu-id="3ccf6-141">如果提供者將以非同步方式處理用戶端要求，則回呼應該會傳回 **錯誤 \_ IO \_ 暫** 止，並在處理用戶端要求時呼叫 [**PxeAsyncRecvDone**](/windows/desktop/api/WdsPxe/nf-wdspxe-pxeasyncrecvdone) 函數。</span><span class="sxs-lookup"><span data-stu-id="3ccf6-141">If the provider will process the client request asynchronously, the callback should return **ERROR\_IO\_PENDING** and call the [**PxeAsyncRecvDone**](/windows/desktop/api/WdsPxe/nf-wdspxe-pxeasyncrecvdone) function when the client request has been processed.</span></span> <span data-ttu-id="3ccf6-142">如果發生失敗，則應該傳回適當的錯誤碼，而系統將繼續進行，就像是指定了 **PXE \_ BA \_ 拒絕** 的開機動作一樣。</span><span class="sxs-lookup"><span data-stu-id="3ccf6-142">In case of failure, an appropriate error code should be returned and the system will proceed as if the **PXE\_BA\_REJECTED** boot action was specified.</span></span>

## <a name="remarks"></a><span data-ttu-id="3ccf6-143">備註</span><span class="sxs-lookup"><span data-stu-id="3ccf6-143">Remarks</span></span>

<span data-ttu-id="3ccf6-144">提供者看到的封包類型可以使用 [**PxeProviderSetAttribute**](/windows/desktop/api/WdsPxe/nf-wdspxe-pxeprovidersetattribute) 函式來變更。</span><span class="sxs-lookup"><span data-stu-id="3ccf6-144">The type of packets seen by a provider can be changed with the [**PxeProviderSetAttribute**](/windows/desktop/api/WdsPxe/nf-wdspxe-pxeprovidersetattribute) function.</span></span>

## <a name="requirements"></a><span data-ttu-id="3ccf6-145">規格需求</span><span class="sxs-lookup"><span data-stu-id="3ccf6-145">Requirements</span></span>



| <span data-ttu-id="3ccf6-146">需求</span><span class="sxs-lookup"><span data-stu-id="3ccf6-146">Requirement</span></span> | <span data-ttu-id="3ccf6-147">值</span><span class="sxs-lookup"><span data-stu-id="3ccf6-147">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="3ccf6-148">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="3ccf6-148">Minimum supported client</span></span><br/> | <span data-ttu-id="3ccf6-149">都不支援</span><span class="sxs-lookup"><span data-stu-id="3ccf6-149">None supported</span></span><br/>                                                          |
| <span data-ttu-id="3ccf6-150">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="3ccf6-150">Minimum supported server</span></span><br/> | <span data-ttu-id="3ccf6-151">僅限 windows Server 2008、Windows Server 2003 SP2 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="3ccf6-151">Windows Server 2008, Windows Server 2003 with SP2 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="3ccf6-152">另請參閱</span><span class="sxs-lookup"><span data-stu-id="3ccf6-152">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3ccf6-153">Windows 部署服務伺服器函數</span><span class="sxs-lookup"><span data-stu-id="3ccf6-153">Windows Deployment Services Server Functions</span></span>](windows-deployment-services-server-functions.md)
</dt> <dt>

[<span data-ttu-id="3ccf6-154">**PxeRegisterCallback**</span><span class="sxs-lookup"><span data-stu-id="3ccf6-154">**PxeRegisterCallback**</span></span>](/windows/desktop/api/WdsPxe/nf-wdspxe-pxeregistercallback)
</dt> <dt>

[<span data-ttu-id="3ccf6-155">**PxeSendReply**</span><span class="sxs-lookup"><span data-stu-id="3ccf6-155">**PxeSendReply**</span></span>](/windows/desktop/api/WdsPxe/nf-wdspxe-pxesendreply)
</dt> <dt>

[<span data-ttu-id="3ccf6-156">**PxeProviderSetAttribute**</span><span class="sxs-lookup"><span data-stu-id="3ccf6-156">**PxeProviderSetAttribute**</span></span>](/windows/desktop/api/WdsPxe/nf-wdspxe-pxeprovidersetattribute)
</dt> </dl>

 

 





