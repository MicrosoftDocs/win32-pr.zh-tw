---
title: 'INapEnforcementClientCallback NotifySoHChange 方法 (NapEnforcementClient .h) '
description: NapAgent 用來通知強制用戶端有 SoH 變更。
ms.assetid: da8b9238-6371-4a6a-a9e7-ab791391ffc2
keywords:
- NotifySoHChange 方法 NAP
- NotifySoHChange 方法 NAP，INapEnforcementClientCallback 介面
- INapEnforcementClientCallback 介面 NAP，NotifySoHChange 方法
topic_type:
- apiref
api_name:
- INapEnforcementClientCallback.NotifySoHChange
api_location:
- NapEnforcementClient.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6b405bca5ae27a68eea780dfcb922d1f986f475c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104106433"
---
# <a name="inapenforcementclientcallbacknotifysohchange-method"></a><span data-ttu-id="c2ee4-106">INapEnforcementClientCallback：： NotifySoHChange 方法</span><span class="sxs-lookup"><span data-stu-id="c2ee4-106">INapEnforcementClientCallback::NotifySoHChange method</span></span>

> [!Note]  
> <span data-ttu-id="c2ee4-107">從 Windows 10 開始，無法使用網路存取保護平臺</span><span class="sxs-lookup"><span data-stu-id="c2ee4-107">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="c2ee4-108">**INapEnforcementClientCallback：： NotifySoHChange** 回呼方法是由 NapAgent 用來通知強制用戶端的 SoH 變更。</span><span class="sxs-lookup"><span data-stu-id="c2ee4-108">The **INapEnforcementClientCallback::NotifySoHChange** callback method is used by the NapAgent to inform the enforcement client of SoH changes.</span></span>

## <a name="syntax"></a><span data-ttu-id="c2ee4-109">語法</span><span class="sxs-lookup"><span data-stu-id="c2ee4-109">Syntax</span></span>


```C++
HRESULT NotifySoHChange();
```



## <a name="parameters"></a><span data-ttu-id="c2ee4-110">參數</span><span class="sxs-lookup"><span data-stu-id="c2ee4-110">Parameters</span></span>

<span data-ttu-id="c2ee4-111">這個方法沒有任何參數。</span><span class="sxs-lookup"><span data-stu-id="c2ee4-111">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="c2ee4-112">傳回值</span><span class="sxs-lookup"><span data-stu-id="c2ee4-112">Return value</span></span>

<span data-ttu-id="c2ee4-113">此回呼方法必須傳回下列其中一個錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="c2ee4-113">This callback method must return one the following error codes.</span></span>



| <span data-ttu-id="c2ee4-114">傳回碼</span><span class="sxs-lookup"><span data-stu-id="c2ee4-114">Return code</span></span>                                                                                                | <span data-ttu-id="c2ee4-115">Description</span><span class="sxs-lookup"><span data-stu-id="c2ee4-115">Description</span></span>                                                                                                                                                                                                           |
|------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="c2ee4-116"><dt>**S \_ 確定**</dt></span><span class="sxs-lookup"><span data-stu-id="c2ee4-116"><dt>**S\_OK**</dt></span></span> </dl>                       | <span data-ttu-id="c2ee4-117">如果作業成功，則傳回此值。</span><span class="sxs-lookup"><span data-stu-id="c2ee4-117">Return this value if the operation succeeded.</span></span><br/>                                                                                                                                                              |
| <dl> <span data-ttu-id="c2ee4-118"><dt>**RPC \_ S \_ 伺服器 \_ 無法使用**</dt></span><span class="sxs-lookup"><span data-stu-id="c2ee4-118"><dt>**RPC\_S\_SERVER\_UNAVAILABLE**</dt></span></span> </dl> | <span data-ttu-id="c2ee4-119">傳回這個值會導致從系結的-SHA 清單中移除 enforcer，以及要排清的對應 NapAgent 快取專案。</span><span class="sxs-lookup"><span data-stu-id="c2ee4-119">Returning this value causes the enforcer to be removed from the bound-SHA list, and the corresponding NapAgent cache entry to be flushed.</span></span> <span data-ttu-id="c2ee4-120">失敗的 SHA 接著可以使用 NapAgent 重新初始化。</span><span class="sxs-lookup"><span data-stu-id="c2ee4-120">The failing SHA can then re-initialize itself with the NapAgent.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="c2ee4-121">備註</span><span class="sxs-lookup"><span data-stu-id="c2ee4-121">Remarks</span></span>

<span data-ttu-id="c2ee4-122">完成系統修正是系統健康狀態變更事件。</span><span class="sxs-lookup"><span data-stu-id="c2ee4-122">The completion of system fix-up is a system health change event.</span></span> <span data-ttu-id="c2ee4-123">這表示當 [**INapSystemHealthAgentCallback：： GetFixupInfo**](inapsystemhealthagentcallback-getfixupinfo-method.md)通知指出用戶端已修正時，您必須呼叫 **NotifySoHChange** 。</span><span class="sxs-lookup"><span data-stu-id="c2ee4-123">That means you must call **NotifySoHChange** when a [**INapSystemHealthAgentCallback::GetFixupInfo**](inapsystemhealthagentcallback-getfixupinfo-method.md) notification indicates that the client is fixed.</span></span> <span data-ttu-id="c2ee4-124">修正用戶端時， **GetFixupInfo** 所傳回之 [**FixupInfo**](/windows/win32/api/naptypes/ns-naptypes-fixupinfo)結構的 **狀態** 成員具有 **fixupStateSuccess** 的值。</span><span class="sxs-lookup"><span data-stu-id="c2ee4-124">When a client is fixed, the **state** member of the [**FixupInfo**](/windows/win32/api/naptypes/ns-naptypes-fixupinfo) structure returned by **GetFixupInfo** has a value of **fixupStateSuccess**.</span></span>

<span data-ttu-id="c2ee4-125">透過此回呼呼叫 NapAgent 之後，強制代理程式必須呼叫 [**INapEnforcementClientBinding：： GetSoHRequest**](inapenforcementclientbinding-getsohrequest-method.md) 以取得新的要求。</span><span class="sxs-lookup"><span data-stu-id="c2ee4-125">After being called by the NapAgent via this callback, the enforcement agent must then call [**INapEnforcementClientBinding::GetSoHRequest**](inapenforcementclientbinding-getsohrequest-method.md) to retrieve the new request.</span></span> <span data-ttu-id="c2ee4-126">此呼叫可以在與 **INapEnforcementClientCallback：： NotifySoHChange** 相同的執行緒上進行。</span><span class="sxs-lookup"><span data-stu-id="c2ee4-126">This call can be made on the same thread as **INapEnforcementClientCallback::NotifySoHChange**.</span></span>

## <a name="requirements"></a><span data-ttu-id="c2ee4-127">規格需求</span><span class="sxs-lookup"><span data-stu-id="c2ee4-127">Requirements</span></span>



| <span data-ttu-id="c2ee4-128">需求</span><span class="sxs-lookup"><span data-stu-id="c2ee4-128">Requirement</span></span> | <span data-ttu-id="c2ee4-129">值</span><span class="sxs-lookup"><span data-stu-id="c2ee4-129">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c2ee4-130">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="c2ee4-130">Minimum supported client</span></span><br/> | <span data-ttu-id="c2ee4-131">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="c2ee4-131">Windows Vista \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="c2ee4-132">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="c2ee4-132">Minimum supported server</span></span><br/> | <span data-ttu-id="c2ee4-133">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="c2ee4-133">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="c2ee4-134">標頭</span><span class="sxs-lookup"><span data-stu-id="c2ee4-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="c2ee4-135"><dt>NapEnforcementClient。h</dt></span><span class="sxs-lookup"><span data-stu-id="c2ee4-135"><dt>NapEnforcementClient.h</dt></span></span> </dl>   |
| <span data-ttu-id="c2ee4-136">Idl</span><span class="sxs-lookup"><span data-stu-id="c2ee4-136">IDL</span></span><br/>                      | <dl> <span data-ttu-id="c2ee4-137"><dt>NapEnforcementClient .idl</dt></span><span class="sxs-lookup"><span data-stu-id="c2ee4-137"><dt>NapEnforcementClient.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c2ee4-138">另請參閱</span><span class="sxs-lookup"><span data-stu-id="c2ee4-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c2ee4-139">**INapEnforcementClientCallback**</span><span class="sxs-lookup"><span data-stu-id="c2ee4-139">**INapEnforcementClientCallback**</span></span>](inapenforcementclientcallback.md)
</dt> </dl>

 

 





