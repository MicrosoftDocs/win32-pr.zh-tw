---
title: 'INapSystemHealthAgentCallback GetSoHRequest 方法 (NapSystemHealthAgent .h) '
description: NapAgent 會呼叫，以查詢系統健康情況代理程式的 SoH 要求。
ms.assetid: 4161a3e7-2f7a-40d1-b973-47f991bba5d0
keywords:
- GetSoHRequest 方法 NAP
- GetSoHRequest 方法 NAP，INapSystemHealthAgentCallback 介面
- INapSystemHealthAgentCallback 介面 NAP，GetSoHRequest 方法
topic_type:
- apiref
api_name:
- INapSystemHealthAgentCallback.GetSoHRequest
api_location:
- NapSystemHealthAgent.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d0fd95ce79587b5e7e259323286cfce138dd2df2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104384837"
---
# <a name="inapsystemhealthagentcallbackgetsohrequest-method"></a><span data-ttu-id="9ab37-106">INapSystemHealthAgentCallback：： GetSoHRequest 方法</span><span class="sxs-lookup"><span data-stu-id="9ab37-106">INapSystemHealthAgentCallback::GetSoHRequest method</span></span>

> [!Note]  
> <span data-ttu-id="9ab37-107">從 Windows 10 開始，無法使用網路存取保護平臺</span><span class="sxs-lookup"><span data-stu-id="9ab37-107">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="9ab37-108">NapAgent 會呼叫 **INapSystemHealthAgentCallback：： GetSoHRequest** 方法，以查詢系統健康情況代理程式的 SoH 要求。</span><span class="sxs-lookup"><span data-stu-id="9ab37-108">The **INapSystemHealthAgentCallback::GetSoHRequest** method is called by the NapAgent to query the system health agent's SoH request.</span></span>

## <a name="syntax"></a><span data-ttu-id="9ab37-109">語法</span><span class="sxs-lookup"><span data-stu-id="9ab37-109">Syntax</span></span>


```C++
HRESULT GetSoHRequest(
  [in] INapSystemHealthAgentRequest *request
);
```



## <a name="parameters"></a><span data-ttu-id="9ab37-110">參數</span><span class="sxs-lookup"><span data-stu-id="9ab37-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9ab37-111">*要求* \[在\]</span><span class="sxs-lookup"><span data-stu-id="9ab37-111">*request* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9ab37-112">識別要求物件之 [**INapSystemHealthAgentRequest**](inapsystemhealthagentrequest.md) 物件的 COM 指標。</span><span class="sxs-lookup"><span data-stu-id="9ab37-112">A COM pointer to an [**INapSystemHealthAgentRequest**](inapsystemhealthagentrequest.md) object that identifies the request object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9ab37-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="9ab37-113">Return value</span></span>



| <span data-ttu-id="9ab37-114">傳回碼</span><span class="sxs-lookup"><span data-stu-id="9ab37-114">Return code</span></span>                                                                                                                      | <span data-ttu-id="9ab37-115">Description</span><span class="sxs-lookup"><span data-stu-id="9ab37-115">Description</span></span>                                                                                                                                        |
|----------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="9ab37-116"><dt>**S \_ 確定**</dt></span><span class="sxs-lookup"><span data-stu-id="9ab37-116"><dt>**S\_OK**</dt></span></span> </dl>                                             | <span data-ttu-id="9ab37-117">表示成功。</span><span class="sxs-lookup"><span data-stu-id="9ab37-117">Indicates success.</span></span><br/>                                                                                                                      |
| <dl> <span data-ttu-id="9ab37-118"><dt>**\_ \_ 無法使用 WIN32 (RPC \_ S \_ 伺服器的 HRESULT \_)**</dt></span><span class="sxs-lookup"><span data-stu-id="9ab37-118"><dt>**HRESULT\_FROM\_WIN32(RPC\_S\_SERVER\_UNAVAILABLE)**</dt></span></span> </dl> | <span data-ttu-id="9ab37-119">如果您的執行傳回此程式碼，則 NapAgent 會接著從系結-SHA 清單中移除 SHA，並清除其快取專案。</span><span class="sxs-lookup"><span data-stu-id="9ab37-119">If this code is returned by your implementation, the NapAgent then removes the SHA from the bound-SHA list and flushes its cache entry.</span></span><br/> |



 

<span data-ttu-id="9ab37-120">當您的實 SoHRequest 傳回的任何傳回值 (不是 **\_ \_ WIN32 (RPC \_ S \_ 伺服器 \_)**) 時，NAP 系統會使用下列屬性類型和值，來將 [](/windows/win32/api/naptypes/ns-naptypes-soh)結構和傳回對應的 SHV：</span><span class="sxs-lookup"><span data-stu-id="9ab37-120">When any return value (except **HRESULT\_FROM\_WIN32(RPC\_S\_SERVER\_UNAVAILABLE)**) is returned by your implementation, the NAP system constructs and returns a [**SoHRequest**](/windows/win32/api/naptypes/ns-naptypes-soh) to the corresponding SHV with the following attribute types and values:</span></span>

-   <span data-ttu-id="9ab37-121">[**sohAttributeTypeSystemHealthId**](sohattributetype-enum.md)= <id></span><span class="sxs-lookup"><span data-stu-id="9ab37-121">[**sohAttributeTypeSystemHealthId**](sohattributetype-enum.md)= <id></span></span>
-   <span data-ttu-id="9ab37-122">[**sohAttributeTypeFailureCategory**](sohattributetype-enum.md) = [ **failureCategoryClientComponent**](/windows/win32/api/naptypes/ne-naptypes-failurecategory)</span><span class="sxs-lookup"><span data-stu-id="9ab37-122">[**sohAttributeTypeFailureCategory**](sohattributetype-enum.md)= [**failureCategoryClientComponent**](/windows/win32/api/naptypes/ne-naptypes-failurecategory)</span></span>
-   <span data-ttu-id="9ab37-123">[**sohAttributeTypeErrorCodes**](sohattributetype-enum.md) = <錯誤-程式碼></span><span class="sxs-lookup"><span data-stu-id="9ab37-123">[**sohAttributeTypeErrorCodes**](sohattributetype-enum.md) = <error-code></span></span>

## <a name="remarks"></a><span data-ttu-id="9ab37-124">備註</span><span class="sxs-lookup"><span data-stu-id="9ab37-124">Remarks</span></span>

<span data-ttu-id="9ab37-125">此回呼方法是由 NAP 系統所宣告，而且是由 SHA 寫入器所執行。</span><span class="sxs-lookup"><span data-stu-id="9ab37-125">This callback method is declared by the NAP system and is to be implemented by the SHA writer.</span></span>

<span data-ttu-id="9ab37-126">這個方法必須處理要求並立即傳回。</span><span class="sxs-lookup"><span data-stu-id="9ab37-126">This method must process the request and return immediately.</span></span> <span data-ttu-id="9ab37-127">延遲傳回這個方法會對系統效能和回應性造成負面影響，而且可能會導致作業系統的其他部分超時。</span><span class="sxs-lookup"><span data-stu-id="9ab37-127">Delaying the return of this method negatively impacts system performance and responsiveness, and may cause other parts of the operating system to time out.</span></span>

<span data-ttu-id="9ab37-128">健全狀況狀態監視不應在此呼叫過程中完成，特別是在需要大量計算且需要很長的時間時。</span><span class="sxs-lookup"><span data-stu-id="9ab37-128">Health state monitoring should not be done as part of this call, especially if it is computation intensive and takes a long time.</span></span> <span data-ttu-id="9ab37-129">健全狀況狀態監視和 SoH 計算應該在個別的執行緒或服務中執行。</span><span class="sxs-lookup"><span data-stu-id="9ab37-129">Health state monitoring and SoH computation should be performed in a separate thread or service.</span></span> <span data-ttu-id="9ab37-130">這個方法的唯一功能應該是設定 SHA 的 SoH 並傳回。</span><span class="sxs-lookup"><span data-stu-id="9ab37-130">The sole function of this method should be to set the SHA's SoH and return.</span></span>

<span data-ttu-id="9ab37-131">如果 SHA 需要很長的時間才能產生 SoH，則應該將快取的 SoH 傳回給 NapAgent。</span><span class="sxs-lookup"><span data-stu-id="9ab37-131">If it will take a long time for the SHA to generate a SoH, then the cached SoH should be returned to the NapAgent.</span></span> <span data-ttu-id="9ab37-132">如果沒有快取的 SoH 要傳回，則 SHA 應該立即傳回具有下列屬性類型和值的 SoH：</span><span class="sxs-lookup"><span data-stu-id="9ab37-132">If there is no cached SoH to return, then the SHA should immediately return a SoH with the following attribute types and values:</span></span>

-   <span data-ttu-id="9ab37-133">[**sohAttributeTypeSystemHealthId**](sohattributetype-enum.md)= <id></span><span class="sxs-lookup"><span data-stu-id="9ab37-133">[**sohAttributeTypeSystemHealthId**](sohattributetype-enum.md)= <id></span></span>
-   <span data-ttu-id="9ab37-134">[**sohAttributeTypeFailureCategory**](sohattributetype-enum.md) = [ **failureCategoryClientCommunication**](/windows/win32/api/naptypes/ne-naptypes-failurecategory)</span><span class="sxs-lookup"><span data-stu-id="9ab37-134">[**sohAttributeTypeFailureCategory**](sohattributetype-enum.md)= [**failureCategoryClientCommunication**](/windows/win32/api/naptypes/ne-naptypes-failurecategory)</span></span>
-   <span data-ttu-id="9ab37-135">[**sohAttributeTypeErrorCodes**](sohattributetype-enum.md)  = [ **NAP \_ E \_ 沒有 \_ \_** 快取的 SOH](nap-error-constants.md)</span><span class="sxs-lookup"><span data-stu-id="9ab37-135">[**sohAttributeTypeErrorCodes**](sohattributetype-enum.md) = [**NAP\_E\_NO\_CACHED\_SOH**](nap-error-constants.md)</span></span>

<span data-ttu-id="9ab37-136">產生 SoH 時，SHA 必須呼叫 [**INapSystemHealthAgentBinding：： NotifySoHChange**](inapsystemhealthagentbinding-notifysohchange-method.md) ，以通知 NapAgent 系統健康狀態變更。</span><span class="sxs-lookup"><span data-stu-id="9ab37-136">When the SoH has been generated, the SHA must call [**INapSystemHealthAgentBinding::NotifySoHChange**](inapsystemhealthagentbinding-notifysohchange-method.md) to notify the NapAgent of the system health change.</span></span>

<span data-ttu-id="9ab37-137">NapAgent 會呼叫這個方法來查詢系統健康情況代理程式的 SoHRequest。</span><span class="sxs-lookup"><span data-stu-id="9ab37-137">The NapAgent calls this method to query the system health agent's SoHRequest.</span></span> <span data-ttu-id="9ab37-138">SHA 可以查詢傳遞的 [**INapSystemHealthAgentRequest**](inapsystemhealthagentrequest.md) 物件，以取得其所需的參數來計算 SoHRequest。</span><span class="sxs-lookup"><span data-stu-id="9ab37-138">The SHA can query the passed [**INapSystemHealthAgentRequest**](inapsystemhealthagentrequest.md) object for parameters that it needs to compute the SoHRequest.</span></span> <span data-ttu-id="9ab37-139">SHA 必須設定 request 物件的計算 SoHRequest。</span><span class="sxs-lookup"><span data-stu-id="9ab37-139">The SHA must set the computed SoHRequest on the request object.</span></span> <span data-ttu-id="9ab37-140">此呼叫完成之後，SHA 不能保留要求物件的參考。</span><span class="sxs-lookup"><span data-stu-id="9ab37-140">The SHA must not hold references to the request object once this call has completed.</span></span>

<span data-ttu-id="9ab37-141">當呼叫這個方法時，如果 NapAgent 的快取中有 SoH，則會在要求物件上設定它。</span><span class="sxs-lookup"><span data-stu-id="9ab37-141">When this method is called, if there is a SoH in the NapAgent's cache, then it is set on the request object.</span></span> <span data-ttu-id="9ab37-142">SHA 可以使用 **GetSoHRequest** 來查詢它。</span><span class="sxs-lookup"><span data-stu-id="9ab37-142">The SHA can query for it using **GetSoHRequest**.</span></span> <span data-ttu-id="9ab37-143">如果 SHA 沒有設定新的 SoH，則會使用快取的 SoH。</span><span class="sxs-lookup"><span data-stu-id="9ab37-143">If the SHA does not set a new SoH, then the cached one is used.</span></span>

<span data-ttu-id="9ab37-144">針對已向系統註冊的未系結 Sha，NAP 系統會使用下列屬性類型和值，來建立 SoHRequest 並將其傳送至對應的 SHV：</span><span class="sxs-lookup"><span data-stu-id="9ab37-144">For unbound SHAs which are registered with the system, the NAP system constructs and sends a SoHRequest to the corresponding SHV with the following attribute types and values:</span></span>

-   <span data-ttu-id="9ab37-145">[**sohAttributeTypeSystemHealthId**](sohattributetype-enum.md)= <id></span><span class="sxs-lookup"><span data-stu-id="9ab37-145">[**sohAttributeTypeSystemHealthId**](sohattributetype-enum.md)= <id></span></span>
-   <span data-ttu-id="9ab37-146">[**sohAttributeTypeFailureCategory**](sohattributetype-enum.md) = [ **failureCategoryClientComponent**](/windows/win32/api/naptypes/ne-naptypes-failurecategory)</span><span class="sxs-lookup"><span data-stu-id="9ab37-146">[**sohAttributeTypeFailureCategory**](sohattributetype-enum.md)= [**failureCategoryClientComponent**](/windows/win32/api/naptypes/ne-naptypes-failurecategory)</span></span>
-   <span data-ttu-id="9ab37-147">[**sohAttributeTypeErrorCodes**](sohattributetype-enum.md)  = [ **NAP \_ E \_ 未 \_ 初始化**](nap-error-constants.md)</span><span class="sxs-lookup"><span data-stu-id="9ab37-147">[**sohAttributeTypeErrorCodes**](sohattributetype-enum.md) = [**NAP\_E\_NOT\_INITIALIZED**](nap-error-constants.md)</span></span>

## <a name="requirements"></a><span data-ttu-id="9ab37-148">規格需求</span><span class="sxs-lookup"><span data-stu-id="9ab37-148">Requirements</span></span>



| <span data-ttu-id="9ab37-149">需求</span><span class="sxs-lookup"><span data-stu-id="9ab37-149">Requirement</span></span> | <span data-ttu-id="9ab37-150">值</span><span class="sxs-lookup"><span data-stu-id="9ab37-150">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9ab37-151">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="9ab37-151">Minimum supported client</span></span><br/> | <span data-ttu-id="9ab37-152">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="9ab37-152">Windows Vista \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="9ab37-153">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="9ab37-153">Minimum supported server</span></span><br/> | <span data-ttu-id="9ab37-154">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="9ab37-154">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="9ab37-155">標頭</span><span class="sxs-lookup"><span data-stu-id="9ab37-155">Header</span></span><br/>                   | <dl> <span data-ttu-id="9ab37-156"><dt>NapSystemHealthAgent。h</dt></span><span class="sxs-lookup"><span data-stu-id="9ab37-156"><dt>NapSystemHealthAgent.h</dt></span></span> </dl>   |
| <span data-ttu-id="9ab37-157">Idl</span><span class="sxs-lookup"><span data-stu-id="9ab37-157">IDL</span></span><br/>                      | <dl> <span data-ttu-id="9ab37-158"><dt>NapSystemHealthAgent .idl</dt></span><span class="sxs-lookup"><span data-stu-id="9ab37-158"><dt>NapSystemHealthAgent.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9ab37-159">另請參閱</span><span class="sxs-lookup"><span data-stu-id="9ab37-159">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9ab37-160">**INapSystemHealthAgentCallback**</span><span class="sxs-lookup"><span data-stu-id="9ab37-160">**INapSystemHealthAgentCallback**</span></span>](inapsystemhealthagentcallback.md)
</dt> </dl>

 

 





