---
title: 'INapSystemHealthAgentCallback ProcessSoHResponse 方法 (NapSystemHealthAgent .h) '
description: 當 NapAgent 收到以這個健康情況代理程式為目標的 SoHResponse 時，會呼叫。
ms.assetid: 860b1012-7df8-456f-8f21-eb0e1abd2b3b
keywords:
- ProcessSoHResponse 方法 NAP
- ProcessSoHResponse 方法 NAP，INapSystemHealthAgentCallback 介面
- INapSystemHealthAgentCallback 介面 NAP，ProcessSoHResponse 方法
topic_type:
- apiref
api_name:
- INapSystemHealthAgentCallback.ProcessSoHResponse
api_location:
- NapSystemHealthAgent.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 95c62c585c36680dde2c54c95c255a85f69fc5ce
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103934516"
---
# <a name="inapsystemhealthagentcallbackprocesssohresponse-method"></a><span data-ttu-id="a3e23-106">INapSystemHealthAgentCallback：:P rocessSoHResponse 方法</span><span class="sxs-lookup"><span data-stu-id="a3e23-106">INapSystemHealthAgentCallback::ProcessSoHResponse method</span></span>

> [!Note]  
> <span data-ttu-id="a3e23-107">從 Windows 10 開始，無法使用網路存取保護平臺</span><span class="sxs-lookup"><span data-stu-id="a3e23-107">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="a3e23-108">**INapSystemHealthAgentCallback：:P rocesssohresponse** 方法會在 NapAgent 收到以這個健康情況代理程式為目標的 [**SoHResponse**](/windows/win32/api/naptypes/ns-naptypes-soh)時呼叫。</span><span class="sxs-lookup"><span data-stu-id="a3e23-108">The **INapSystemHealthAgentCallback::ProcessSoHResponse** method is called when the NapAgent receives an [**SoHResponse**](/windows/win32/api/naptypes/ns-naptypes-soh) destined for this health agent.</span></span>

## <a name="syntax"></a><span data-ttu-id="a3e23-109">語法</span><span class="sxs-lookup"><span data-stu-id="a3e23-109">Syntax</span></span>


```C++
HRESULT ProcessSoHResponse(
  [in] INapSystemHealthAgentRequest *request
);
```



## <a name="parameters"></a><span data-ttu-id="a3e23-110">參數</span><span class="sxs-lookup"><span data-stu-id="a3e23-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a3e23-111">*要求* \[在\]</span><span class="sxs-lookup"><span data-stu-id="a3e23-111">*request* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a3e23-112">識別要求物件之 [**INapSystemHealthAgentRequest**](inapsystemhealthagentrequest.md) 物件的 COM 指標。</span><span class="sxs-lookup"><span data-stu-id="a3e23-112">A COM pointer to a [**INapSystemHealthAgentRequest**](inapsystemhealthagentrequest.md) object that identifies the request object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a3e23-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="a3e23-113">Return value</span></span>

<span data-ttu-id="a3e23-114">這個方法可以傳回其中一個值。</span><span class="sxs-lookup"><span data-stu-id="a3e23-114">This method can return one of these values.</span></span>



| <span data-ttu-id="a3e23-115">傳回碼</span><span class="sxs-lookup"><span data-stu-id="a3e23-115">Return code</span></span>                                                                                            | <span data-ttu-id="a3e23-116">Description</span><span class="sxs-lookup"><span data-stu-id="a3e23-116">Description</span></span>                                                                              |
|--------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="a3e23-117"><dt>**S \_ 確定**</dt></span><span class="sxs-lookup"><span data-stu-id="a3e23-117"><dt>**S\_OK**</dt></span></span> </dl>                   | <span data-ttu-id="a3e23-118">表示成功。</span><span class="sxs-lookup"><span data-stu-id="a3e23-118">Indicates success.</span></span><br/>                                                            |
| <dl> <span data-ttu-id="a3e23-119"><dt>**NAP \_ E \_ 不正確封 \_ 包**</dt></span><span class="sxs-lookup"><span data-stu-id="a3e23-119"><dt>**NAP\_E\_INVALID\_PACKET**</dt></span></span> </dl> | <span data-ttu-id="a3e23-120">如果回應的格式不正確，則會傳回此實作為。</span><span class="sxs-lookup"><span data-stu-id="a3e23-120">Returned by this implementation if the response is not in the correct format.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="a3e23-121">備註</span><span class="sxs-lookup"><span data-stu-id="a3e23-121">Remarks</span></span>

<span data-ttu-id="a3e23-122">此回呼方法是由 NAP 系統所宣告，而且是由 SHA 寫入器所執行。</span><span class="sxs-lookup"><span data-stu-id="a3e23-122">This callback method is declared by the NAP system and is to be implemented by the SHA writer.</span></span>

<span data-ttu-id="a3e23-123">當 NapAgent 收到以這個健康情況代理程式為目標的 [**SoHResponse**](/windows/win32/api/naptypes/ns-naptypes-soh) 時，它會叫用這個方法。</span><span class="sxs-lookup"><span data-stu-id="a3e23-123">When the NapAgent receives an [**SoHResponse**](/windows/win32/api/naptypes/ns-naptypes-soh) destined for this health agent, it invokes this method.</span></span> <span data-ttu-id="a3e23-124">健康情況代理程式必須從要求物件查詢 SoHResponse。</span><span class="sxs-lookup"><span data-stu-id="a3e23-124">The health agent must query the SoHResponse from the request object.</span></span> <span data-ttu-id="a3e23-125">一旦完成此呼叫，它就不能保存要求物件的參考。</span><span class="sxs-lookup"><span data-stu-id="a3e23-125">It must not hold references to the request object once this call has completed.</span></span>

<span data-ttu-id="a3e23-126">**INapSystemHealthAgentCallback：:P rocesssohresponse** 方法不得封鎖。</span><span class="sxs-lookup"><span data-stu-id="a3e23-126">The **INapSystemHealthAgentCallback::ProcessSoHResponse** method must not block.</span></span> <span data-ttu-id="a3e23-127">如果需要進行任何修正程式，則任何 **ProcessSoHResponse** 的執行都必須啟動新的執行緒，以執行修正處理。</span><span class="sxs-lookup"><span data-stu-id="a3e23-127">If any fix-up processing is required, any implementation of **ProcessSoHResponse** must start a new thread to perform fix-up processing.</span></span> <span data-ttu-id="a3e23-128">NapAgent 必須呼叫 [**INapSystemHealthAgentCallBack：： GetFixupInfo**](inapsystemhealthagentcallback-getfixupinfo-method.md) ，以判斷 SHA 的修正狀態。</span><span class="sxs-lookup"><span data-stu-id="a3e23-128">The NapAgent must call [**INapSystemHealthAgentCallBack::GetFixupInfo**](inapsystemhealthagentcallback-getfixupinfo-method.md) to determine the fix-up status of the SHA.</span></span>

<span data-ttu-id="a3e23-129">如果回應的格式不正確，此方法必須傳回 **NAP \_ E \_ 無效 \_** 的封包。</span><span class="sxs-lookup"><span data-stu-id="a3e23-129">This method must return **NAP\_E\_INVALID\_PACKET** if the response is not in the correct format.</span></span>

## <a name="requirements"></a><span data-ttu-id="a3e23-130">規格需求</span><span class="sxs-lookup"><span data-stu-id="a3e23-130">Requirements</span></span>



| <span data-ttu-id="a3e23-131">需求</span><span class="sxs-lookup"><span data-stu-id="a3e23-131">Requirement</span></span> | <span data-ttu-id="a3e23-132">值</span><span class="sxs-lookup"><span data-stu-id="a3e23-132">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a3e23-133">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="a3e23-133">Minimum supported client</span></span><br/> | <span data-ttu-id="a3e23-134">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="a3e23-134">Windows Vista \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="a3e23-135">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="a3e23-135">Minimum supported server</span></span><br/> | <span data-ttu-id="a3e23-136">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="a3e23-136">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="a3e23-137">標頭</span><span class="sxs-lookup"><span data-stu-id="a3e23-137">Header</span></span><br/>                   | <dl> <span data-ttu-id="a3e23-138"><dt>NapSystemHealthAgent。h</dt></span><span class="sxs-lookup"><span data-stu-id="a3e23-138"><dt>NapSystemHealthAgent.h</dt></span></span> </dl>   |
| <span data-ttu-id="a3e23-139">Idl</span><span class="sxs-lookup"><span data-stu-id="a3e23-139">IDL</span></span><br/>                      | <dl> <span data-ttu-id="a3e23-140"><dt>NapSystemHealthAgent .idl</dt></span><span class="sxs-lookup"><span data-stu-id="a3e23-140"><dt>NapSystemHealthAgent.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a3e23-141">另請參閱</span><span class="sxs-lookup"><span data-stu-id="a3e23-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a3e23-142">**INapSystemHealthAgentCallback**</span><span class="sxs-lookup"><span data-stu-id="a3e23-142">**INapSystemHealthAgentCallback**</span></span>](inapsystemhealthagentcallback.md)
</dt> </dl>

 

 





