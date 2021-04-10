---
title: 'INapSystemHealthAgentCallback NotifySystemIsolationStateChange 方法 (NapSystemHealthAgent .h) '
description: 由 NapAgent 呼叫，表示系統隔離狀態或試用結束時間已變更。
ms.assetid: 0837eea4-6d92-44dc-b8b8-eca6be5f63e6
keywords:
- NotifySystemIsolationStateChange 方法 NAP
- NotifySystemIsolationStateChange 方法 NAP，INapSystemHealthAgentCallback 介面
- INapSystemHealthAgentCallback 介面 NAP，NotifySystemIsolationStateChange 方法
topic_type:
- apiref
api_name:
- INapSystemHealthAgentCallback.NotifySystemIsolationStateChange
api_location:
- NapSystemHealthAgent.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3c519d1569fe2e43cc6012ffa30c5bfb4402cc56
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103686021"
---
# <a name="inapsystemhealthagentcallbacknotifysystemisolationstatechange-method"></a><span data-ttu-id="1fa05-106">INapSystemHealthAgentCallback：： NotifySystemIsolationStateChange 方法</span><span class="sxs-lookup"><span data-stu-id="1fa05-106">INapSystemHealthAgentCallback::NotifySystemIsolationStateChange method</span></span>

> [!Note]  
> <span data-ttu-id="1fa05-107">從 Windows 10 開始，無法使用網路存取保護平臺</span><span class="sxs-lookup"><span data-stu-id="1fa05-107">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="1fa05-108">NapAgent 會呼叫 **INapSystemHealthAgentCallback：： NotifySystemIsolationStateChange** 方法，表示系統隔離狀態或試用結束時間已變更。</span><span class="sxs-lookup"><span data-stu-id="1fa05-108">The **INapSystemHealthAgentCallback::NotifySystemIsolationStateChange** method is called by the NapAgent to indicate that the system isolation state or the probation end-time has changed.</span></span>

## <a name="syntax"></a><span data-ttu-id="1fa05-109">語法</span><span class="sxs-lookup"><span data-stu-id="1fa05-109">Syntax</span></span>


```C++
HRESULT NotifySystemIsolationStateChange();
```



## <a name="parameters"></a><span data-ttu-id="1fa05-110">參數</span><span class="sxs-lookup"><span data-stu-id="1fa05-110">Parameters</span></span>

<span data-ttu-id="1fa05-111">這個方法沒有任何參數。</span><span class="sxs-lookup"><span data-stu-id="1fa05-111">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="1fa05-112">傳回值</span><span class="sxs-lookup"><span data-stu-id="1fa05-112">Return value</span></span>

<span data-ttu-id="1fa05-113">這個方法可以傳回其中一個值。</span><span class="sxs-lookup"><span data-stu-id="1fa05-113">This method can return one of these values.</span></span>



| <span data-ttu-id="1fa05-114">傳回碼</span><span class="sxs-lookup"><span data-stu-id="1fa05-114">Return code</span></span>                                                                          | <span data-ttu-id="1fa05-115">Description</span><span class="sxs-lookup"><span data-stu-id="1fa05-115">Description</span></span>                   |
|--------------------------------------------------------------------------------------|-------------------------------|
| <dl> <span data-ttu-id="1fa05-116"><dt>**S \_ 確定**</dt></span><span class="sxs-lookup"><span data-stu-id="1fa05-116"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="1fa05-117">表示成功。</span><span class="sxs-lookup"><span data-stu-id="1fa05-117">Indicates success.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="1fa05-118">備註</span><span class="sxs-lookup"><span data-stu-id="1fa05-118">Remarks</span></span>

<span data-ttu-id="1fa05-119">此回呼方法是由 NAP 系統所宣告，而且是由 SHA 寫入器所執行。</span><span class="sxs-lookup"><span data-stu-id="1fa05-119">This callback method is declared by the NAP system and is to be implemented by the SHA writer.</span></span>

<span data-ttu-id="1fa05-120">健康情況代理程式可以使用 [**INapSystemHealthAgentBinding：： GetSystemIsolationInfo**](inapsystemhealthagentbinding-getsystemisolationinfo-method.md)來查詢系統 NAP 狀態。</span><span class="sxs-lookup"><span data-stu-id="1fa05-120">The health agent can query the system NAP state using the [**INapSystemHealthAgentBinding::GetSystemIsolationInfo**](inapsystemhealthagentbinding-getsystemisolationinfo-method.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="1fa05-121">規格需求</span><span class="sxs-lookup"><span data-stu-id="1fa05-121">Requirements</span></span>



| <span data-ttu-id="1fa05-122">需求</span><span class="sxs-lookup"><span data-stu-id="1fa05-122">Requirement</span></span> | <span data-ttu-id="1fa05-123">值</span><span class="sxs-lookup"><span data-stu-id="1fa05-123">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1fa05-124">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="1fa05-124">Minimum supported client</span></span><br/> | <span data-ttu-id="1fa05-125">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="1fa05-125">Windows Vista \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="1fa05-126">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="1fa05-126">Minimum supported server</span></span><br/> | <span data-ttu-id="1fa05-127">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="1fa05-127">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="1fa05-128">標頭</span><span class="sxs-lookup"><span data-stu-id="1fa05-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="1fa05-129"><dt>NapSystemHealthAgent。h</dt></span><span class="sxs-lookup"><span data-stu-id="1fa05-129"><dt>NapSystemHealthAgent.h</dt></span></span> </dl>   |
| <span data-ttu-id="1fa05-130">Idl</span><span class="sxs-lookup"><span data-stu-id="1fa05-130">IDL</span></span><br/>                      | <dl> <span data-ttu-id="1fa05-131"><dt>NapSystemHealthAgent .idl</dt></span><span class="sxs-lookup"><span data-stu-id="1fa05-131"><dt>NapSystemHealthAgent.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1fa05-132">另請參閱</span><span class="sxs-lookup"><span data-stu-id="1fa05-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1fa05-133">**INapSystemHealthAgentCallback**</span><span class="sxs-lookup"><span data-stu-id="1fa05-133">**INapSystemHealthAgentCallback**</span></span>](inapsystemhealthagentcallback.md)
</dt> </dl>

 

 





