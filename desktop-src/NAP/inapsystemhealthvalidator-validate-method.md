---
title: 'INapSystemHealthValidator Validate 方法 (NapSystemHealthValidator .h) '
description: 驗證從用戶端接收之 SoHRequest 的 NAP 系統。
ms.assetid: d67dc2c8-f18c-4e06-a51e-a538ca75c3f1
keywords:
- 驗證方法 NAP
- 驗證方法 NAP、INapSystemHealthValidator 介面
- INapSystemHealthValidator 介面 NAP，Validate 方法
topic_type:
- apiref
api_name:
- INapSystemHealthValidator.Validate
api_location:
- NapSystemHealthValidator.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4f7589a67b9a3b1454e3c65b17ad6f584ce0e655
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106995164"
---
# <a name="inapsystemhealthvalidatorvalidate-method"></a><span data-ttu-id="28333-106">INapSystemHealthValidator：： Validate 方法</span><span class="sxs-lookup"><span data-stu-id="28333-106">INapSystemHealthValidator::Validate method</span></span>

> [!Note]  
> <span data-ttu-id="28333-107">從 Windows 10 開始，無法使用網路存取保護平臺</span><span class="sxs-lookup"><span data-stu-id="28333-107">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="28333-108">**INapSystemHealthValidator：： Validate** 方法是由 SHV 開發人員定義，並由 NAP 系統呼叫來驗證從用戶端收到的 [**SoHRequest**](/windows/win32/api/naptypes/ns-naptypes-soh) 。</span><span class="sxs-lookup"><span data-stu-id="28333-108">The **INapSystemHealthValidator::Validate** method is defined by the SHV developer and called by the NAP system to validate the [**SoHRequest**](/windows/win32/api/naptypes/ns-naptypes-soh) received from a client.</span></span>

## <a name="syntax"></a><span data-ttu-id="28333-109">語法</span><span class="sxs-lookup"><span data-stu-id="28333-109">Syntax</span></span>


```C++
HRESULT Validate(
  [in] INapSystemHealthValidationRequest *request,
  [in] UINT32                            hintTimeOutInMsec,
  [in] INapServerCallback                *callback
);
```



## <a name="parameters"></a><span data-ttu-id="28333-110">參數</span><span class="sxs-lookup"><span data-stu-id="28333-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="28333-111">*要求* \[在\]</span><span class="sxs-lookup"><span data-stu-id="28333-111">*request* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="28333-112">識別驗證要求物件之 [**INapSystemHealthValidationRequest**](inapsystemhealthvalidationrequest.md) 物件的 COM 指標。</span><span class="sxs-lookup"><span data-stu-id="28333-112">A COM pointer to an [**INapSystemHealthValidationRequest**](inapsystemhealthvalidationrequest.md) object that identifies the validation request object.</span></span>

</dd> <dt>

<span data-ttu-id="28333-113">*hintTimeOutInMsec* \[在\]</span><span class="sxs-lookup"><span data-stu-id="28333-113">*hintTimeOutInMsec* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="28333-114">通訊逾時間隔的持續時間（以毫秒為單位）。</span><span class="sxs-lookup"><span data-stu-id="28333-114">The duration, in milliseconds, of the communication timeout period.</span></span> <span data-ttu-id="28333-115"> (SHV) 的系統健全狀況驗證程式應在這段時間內回應;否則會捨棄回應。</span><span class="sxs-lookup"><span data-stu-id="28333-115">The System Health Validator (SHV) should respond within this amount of time; otherwise the response is dropped.</span></span>

> [!Note]  
> <span data-ttu-id="28333-116">所有 Shv 的預設超時值為2000毫秒。</span><span class="sxs-lookup"><span data-stu-id="28333-116">The default timeout for all SHVs is 2000 milliseconds.</span></span> <span data-ttu-id="28333-117">使用預設值以外的值，將會變更所有已註冊之 Shv 的超時時間。</span><span class="sxs-lookup"><span data-stu-id="28333-117">Using a value other than the default will change the timeout for all registered SHVs.</span></span>

 

</dd> <dt>

<span data-ttu-id="28333-118">*回呼* \[在\]</span><span class="sxs-lookup"><span data-stu-id="28333-118">*callback* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="28333-119">回呼物件 [**INapServerCallback**](inapservercallback.md)的指標。</span><span class="sxs-lookup"><span data-stu-id="28333-119">A pointer to the callback object [**INapServerCallback**](inapservercallback.md).</span></span> <span data-ttu-id="28333-120">當 Shv 從呼叫 **INapSystemHealthValidator：： Validate** 傳回 **E \_ 暫** 止時，就會使用此回呼指標。</span><span class="sxs-lookup"><span data-stu-id="28333-120">This callback pointer is used by the SHVs when they return **E\_PENDING** from the call to **INapSystemHealthValidator::Validate**.</span></span> <span data-ttu-id="28333-121">這可用於非同步驗證。</span><span class="sxs-lookup"><span data-stu-id="28333-121">This is used for asynchronous validation.</span></span> <span data-ttu-id="28333-122">Shv 預期會在 *hintTimeOutInMsec* 時間內回應，否則將會捨棄回應。</span><span class="sxs-lookup"><span data-stu-id="28333-122">The SHVs are expected to respond within the *hintTimeOutInMsec* time or else the response will be dropped.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="28333-123">傳回值</span><span class="sxs-lookup"><span data-stu-id="28333-123">Return value</span></span>

<span data-ttu-id="28333-124">如果傳回任何其他錯誤碼，則系統會假設發生 serverComponent 失敗，而且會完成適當的對應以通過/失敗。</span><span class="sxs-lookup"><span data-stu-id="28333-124">If any other error code is returned, then the system assumes serverComponent failure has occurred, and the appropriate mapping is done to pass/fail.</span></span>



| <span data-ttu-id="28333-125">傳回碼</span><span class="sxs-lookup"><span data-stu-id="28333-125">Return code</span></span>                                                                                                | <span data-ttu-id="28333-126">Description</span><span class="sxs-lookup"><span data-stu-id="28333-126">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
|------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="28333-127"><dt>**S \_ 確定**</dt></span><span class="sxs-lookup"><span data-stu-id="28333-127"><dt>**S\_OK**</dt></span></span> </dl>                       | <span data-ttu-id="28333-128">指出驗證程式已在 ' request ' 物件上設定 SoHResponse。</span><span class="sxs-lookup"><span data-stu-id="28333-128">Indicates that the validator has set an SoHResponse on the 'request' object.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                        |
| <dl> <span data-ttu-id="28333-129"><dt>**E \_ 暫止**</dt></span><span class="sxs-lookup"><span data-stu-id="28333-129"><dt>**E\_PENDING**</dt></span></span> </dl>                  | <span data-ttu-id="28333-130">指出將在個別的執行緒上呼叫 OnComplete () 。</span><span class="sxs-lookup"><span data-stu-id="28333-130">Indicates that OnComplete() will be called on a separate thread.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                    |
| <dl> <span data-ttu-id="28333-131"><dt>**RPC \_ S \_ 伺服器 \_ 無法使用**</dt></span><span class="sxs-lookup"><span data-stu-id="28333-131"><dt>**RPC\_S\_SERVER\_UNAVAILABLE**</dt></span></span> </dl> | <span data-ttu-id="28333-132">指出系統健全狀況驗證程式 (SHV) 進程終止，但 NapServer 實際上放開它的參考。</span><span class="sxs-lookup"><span data-stu-id="28333-132">Indicates that the System Health Validator (SHV) process terminated without the NapServer actually releasing a reference to it.</span></span> <span data-ttu-id="28333-133">NapServer 會嘗試重新建立新的 SHV 參考，並且會重新叫用驗證呼叫一次。</span><span class="sxs-lookup"><span data-stu-id="28333-133">The NapServer will try to re-create a new reference to the SHV and will reexecute the Validate call once.</span></span> <span data-ttu-id="28333-134">如果建立物件或重新執行的驗證失敗，則會從已載入的 Shv 清單中移除 SHV。</span><span class="sxs-lookup"><span data-stu-id="28333-134">If the creation of the object or the re-executed Validate fails, the SHV is removed from the list of loaded SHVs.</span></span> <span data-ttu-id="28333-135">現在可重載此 SHV 的唯一方法是再次取消註冊並重新註冊 SHV，或 NapServer 重新開機時</span><span class="sxs-lookup"><span data-stu-id="28333-135">The only way this SHV can now be reloaded is to unregister and reregister the SHV again, or when the NapServer restarts</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="28333-136">備註</span><span class="sxs-lookup"><span data-stu-id="28333-136">Remarks</span></span>

<span data-ttu-id="28333-137">為了支援入侵偵測，系統會要求 Shv 驗證用戶端電腦，不論用戶端是否傳送了針對 SHV 的 [**SoHRequest**](/windows/win32/api/naptypes/ns-naptypes-soh) 。</span><span class="sxs-lookup"><span data-stu-id="28333-137">In order to support intrusion detection, SHVs will be asked to validate the client machine regardless of whether the client sent an [**SoHRequest**](/windows/win32/api/naptypes/ns-naptypes-soh) intended for the SHV.</span></span>

<span data-ttu-id="28333-138">SHV 必須執行下列動作：</span><span class="sxs-lookup"><span data-stu-id="28333-138">The SHV must do the following:</span></span>

-   <span data-ttu-id="28333-139">藉由呼叫要求，從 *要求* 中取出 [**SoHRequest**](/windows/win32/api/naptypes/ns-naptypes-soh) [**。GetSoHRequest ()**](inapsystemhealthvalidationrequest-getsohrequest-method.md)。</span><span class="sxs-lookup"><span data-stu-id="28333-139">Retrieve the [**SoHRequest**](/windows/win32/api/naptypes/ns-naptypes-soh) from *request* by calling [**request.GetSoHRequest()**](inapsystemhealthvalidationrequest-getsohrequest-method.md).</span></span>
-   <span data-ttu-id="28333-140">如果 [**SoHRequest**](/windows/win32/api/naptypes/ns-naptypes-soh) 封包為 null：</span><span class="sxs-lookup"><span data-stu-id="28333-140">If the [**SoHRequest**](/windows/win32/api/naptypes/ns-naptypes-soh) packet is null:</span></span>
    -   <span data-ttu-id="28333-141">如果 SHV 是入侵偵測系統，請使用適當的 [**NAP 錯誤碼**](nap-error-constants.md)填入 [**SoHRequest**](/windows/win32/api/naptypes/ns-naptypes-soh)封包，以因應用戶端電腦的惡意原因。</span><span class="sxs-lookup"><span data-stu-id="28333-141">If the SHV is an intrusion detection system, populate an [**SoHRequest**](/windows/win32/api/naptypes/ns-naptypes-soh) packet with the appropriate [**NAP error code**](nap-error-constants.md) as to why the client machine is malicious.</span></span>
    -   <span data-ttu-id="28333-142">所有其他 Shv 都應以 [**NAP \_ E \_ 缺少 \_ SOH**](nap-error-constants.md)的錯誤碼填入 [**SoHRequest**](/windows/win32/api/naptypes/ns-naptypes-soh)封包。</span><span class="sxs-lookup"><span data-stu-id="28333-142">All other SHVs should populate an [**SoHRequest**](/windows/win32/api/naptypes/ns-naptypes-soh) packet with an error code of [**NAP\_E\_MISSING\_SOH**](nap-error-constants.md).</span></span>
-   <span data-ttu-id="28333-143">如果 *napSystemGenerated* 為 **TRUE** ，則是來自 [**要求的呼叫。GetSoHRequest ()**](inapsystemhealthvalidationrequest-getsohrequest-method.md)，SHV 應預期具有下列 3 TLVs 的 [**SoH**](/windows/win32/api/naptypes/ns-naptypes-soh) 封包： [**sohAttributeTypeSystemHealthId**](sohattributetype-enum.md)、 **sohAttributeTypeFailureCategory**、 **sohAttributeTypeErrorCodes**。</span><span class="sxs-lookup"><span data-stu-id="28333-143">If *napSystemGenerated* is **TRUE** from the call to [**request.GetSoHRequest()**](inapsystemhealthvalidationrequest-getsohrequest-method.md), the SHV should expect an [**SoH**](/windows/win32/api/naptypes/ns-naptypes-soh) packet with the following 3 TLVs: [**sohAttributeTypeSystemHealthId**](sohattributetype-enum.md), **sohAttributeTypeFailureCategory**, **sohAttributeTypeErrorCodes**.</span></span> <span data-ttu-id="28333-144">此 **SoHRequest** 是由 NapAgent 代表系統健康狀態代理程式產生， (sha) ，因為從 SHA 取出要求封包時發生錯誤。</span><span class="sxs-lookup"><span data-stu-id="28333-144">This **SoHRequest** is generated by the NapAgent on behalf of the System Health Agent (SHA) since there was an error in retrieving a request packet from the SHA.</span></span>
-   <span data-ttu-id="28333-145">驗證 [**SoHRequest**](/windows/win32/api/naptypes/ns-naptypes-soh) 封包。</span><span class="sxs-lookup"><span data-stu-id="28333-145">Validate the [**SoHRequest**](/windows/win32/api/naptypes/ns-naptypes-soh) packet.</span></span>
    -   <span data-ttu-id="28333-146">如果 [**SoHRequest**](/windows/win32/api/naptypes/ns-naptypes-soh)的格式不正確，則請使用錯誤碼 [**NAP \_ E 不正確封 \_ \_ 包**](nap-error-constants.md)來建立 **SoHResponse** 封包。</span><span class="sxs-lookup"><span data-stu-id="28333-146">If the [**SoHRequest**](/windows/win32/api/naptypes/ns-naptypes-soh) is malformed, then construct a **SoHResponse** packet with error code [**NAP\_E\_INVALID\_PACKET**](nap-error-constants.md).</span></span>
    -   <span data-ttu-id="28333-147">如果 SHV 只使用快取的資訊來驗證 [**SoHRequest**](/windows/win32/api/naptypes/ns-naptypes-soh) 封包 (也就是不會執行任何 i/o) ，它可以建立 **SoHResponse**，在 *要求* 中的物件上設定，並傳回「 **\_ 確定**」。</span><span class="sxs-lookup"><span data-stu-id="28333-147">If the SHV is only using cached information to validate the [**SoHRequest**](/windows/win32/api/naptypes/ns-naptypes-soh) packet (i.e. no I/O is performed), then it can construct the **SoHResponse**, set it on the object in *request* and return **S\_OK**.</span></span>
    -   <span data-ttu-id="28333-148">如果 SHV 正在執行 i/o 以便與後端伺服器通訊以驗證用戶端的健康狀態，則它必須將 i/o 排入佇列，並將此函式傳回 **E \_ PENDING**。</span><span class="sxs-lookup"><span data-stu-id="28333-148">If the SHV is performing I/O in order to talk to its back-end servers to validate the client's health, then it must queue up the I/O and return this function with **E\_PENDING**.</span></span> <span data-ttu-id="28333-149">在此情況下，SHV 必須呼叫 [**回呼。OnComplete**](inapservercallback-oncomplete-method.md) 在超時期間內的個別執行緒上進行 () *hintTimeOutInMsec*。</span><span class="sxs-lookup"><span data-stu-id="28333-149">In this case, the SHV must call [**callback.OnComplete()**](inapservercallback-oncomplete-method.md) on a separate thread within the timeout period, *hintTimeOutInMsec*.</span></span> <span data-ttu-id="28333-150">否則，將會捨棄 SHV 的回應。</span><span class="sxs-lookup"><span data-stu-id="28333-150">Otherwise, the SHV's response will be dropped.</span></span>
-   <span data-ttu-id="28333-151">請勿傳回上述任何其他錯誤。</span><span class="sxs-lookup"><span data-stu-id="28333-151">Do not return any other error other than those listed above.</span></span> <span data-ttu-id="28333-152">如果 SHV 傳回任何其他錯誤碼 (例如</span><span class="sxs-lookup"><span data-stu-id="28333-152">If any other error code is returned by the SHV (eg.</span></span> <span data-ttu-id="28333-153">某些系統錯誤) ，將會捨棄封包。</span><span class="sxs-lookup"><span data-stu-id="28333-153">some system error), the packet will be discarded.</span></span>

<span data-ttu-id="28333-154">SHV 必須在其 [**SoHRequest**](/windows/win32/api/naptypes/ns-naptypes-soh)中傳回 **sohAttributeTypeComplianceResultCodes** 或 **sohAttributeTypeFailureCategory** TLV。</span><span class="sxs-lookup"><span data-stu-id="28333-154">An SHV must return either an **sohAttributeTypeComplianceResultCodes** or **sohAttributeTypeFailureCategory** TLV in its [**SoHRequest**](/windows/win32/api/naptypes/ns-naptypes-soh).</span></span>

-   <span data-ttu-id="28333-155">[**SOHATTRIBUTETYPECOMPLIANCERESULTCODES TLV**](sohattributetype-enum.md)：如果 SHV 可以驗證客戶 (端的健全狀況（例如狀況良好或狀況不良) ），則會傳回此 TLV。</span><span class="sxs-lookup"><span data-stu-id="28333-155">[**sohAttributeTypeComplianceResultCodes TLV**](sohattributetype-enum.md): If the SHV could validate the health of the client (i.e. healthy or unhealthy), this TLV is returned.</span></span>
-   <span data-ttu-id="28333-156">[**SOHATTRIBUTETYPEFAILURECATEGORY TLV**](sohattributetype-enum.md)：如果用戶端或伺服器上有任何元件或通訊失敗，則必須由此 tlv 表示。</span><span class="sxs-lookup"><span data-stu-id="28333-156">[**sohAttributeTypeFailureCategory TLV**](sohattributetype-enum.md): If there was any component or communication failure on the client or server, it must be indicated by this TLV.</span></span> <span data-ttu-id="28333-157">視 SHV 的設定而定，此 TLV 將進一步對應至狀況良好或狀況不良。</span><span class="sxs-lookup"><span data-stu-id="28333-157">This TLV will further be mapped to healthy or unhealthy depending upon the SHV's configuration.</span></span> <span data-ttu-id="28333-158">如需詳細資訊，請參閱 [**INapServerManagement**](inapservermanagement.md) 介面和 [**FailureCategoryMapping**](/windows/win32/api/naptypes/ns-naptypes-failurecategorymapping) 結構。</span><span class="sxs-lookup"><span data-stu-id="28333-158">For more details, see the [**INapServerManagement**](inapservermanagement.md) interface and the [**FailureCategoryMapping**](/windows/win32/api/naptypes/ns-naptypes-failurecategorymapping) structure.</span></span>

<span data-ttu-id="28333-159">Asyncronous 呼叫完成後，SHV 不得持有 *要求* 或 *回呼* 的參考。</span><span class="sxs-lookup"><span data-stu-id="28333-159">The SHV must not hold references to *request* or *callback* once the asyncronous call completes.</span></span>

## <a name="requirements"></a><span data-ttu-id="28333-160">規格需求</span><span class="sxs-lookup"><span data-stu-id="28333-160">Requirements</span></span>



| <span data-ttu-id="28333-161">需求</span><span class="sxs-lookup"><span data-stu-id="28333-161">Requirement</span></span> | <span data-ttu-id="28333-162">值</span><span class="sxs-lookup"><span data-stu-id="28333-162">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="28333-163">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="28333-163">Minimum supported client</span></span><br/> | <span data-ttu-id="28333-164">都不支援</span><span class="sxs-lookup"><span data-stu-id="28333-164">None supported</span></span><br/>                                                                               |
| <span data-ttu-id="28333-165">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="28333-165">Minimum supported server</span></span><br/> | <span data-ttu-id="28333-166">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="28333-166">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="28333-167">標頭</span><span class="sxs-lookup"><span data-stu-id="28333-167">Header</span></span><br/>                   | <dl> <span data-ttu-id="28333-168"><dt>NapSystemHealthValidator。h</dt></span><span class="sxs-lookup"><span data-stu-id="28333-168"><dt>NapSystemHealthValidator.h</dt></span></span> </dl>   |
| <span data-ttu-id="28333-169">Idl</span><span class="sxs-lookup"><span data-stu-id="28333-169">IDL</span></span><br/>                      | <dl> <span data-ttu-id="28333-170"><dt>NapSystemHealthValidator .idl</dt></span><span class="sxs-lookup"><span data-stu-id="28333-170"><dt>NapSystemHealthValidator.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="28333-171">另請參閱</span><span class="sxs-lookup"><span data-stu-id="28333-171">See also</span></span>

<dl> <dt>

[<span data-ttu-id="28333-172">**INapSystemHealthValidator**</span><span class="sxs-lookup"><span data-stu-id="28333-172">**INapSystemHealthValidator**</span></span>](inapsystemhealthvalidator.md)
</dt> </dl>

 

 





