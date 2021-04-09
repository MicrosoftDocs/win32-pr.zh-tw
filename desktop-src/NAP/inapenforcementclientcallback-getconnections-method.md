---
title: 'INapEnforcementClientCallback GetConnections 方法 (NapEnforcementClient .h) '
description: 由 NapAgent 呼叫並由強制用戶端所執行，以傳回一組連接。
ms.assetid: 8f697217-5799-48e4-9f0b-715f516e48d9
keywords:
- GetConnections 方法 NAP
- GetConnections 方法 NAP，INapEnforcementClientCallback 介面
- INapEnforcementClientCallback 介面 NAP，GetConnections 方法
topic_type:
- apiref
api_name:
- INapEnforcementClientCallback.GetConnections
api_location:
- NapEnforcementClient.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9acdc68dbc69cabe710414f3fa2501585f3e384e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103844355"
---
# <a name="inapenforcementclientcallbackgetconnections-method"></a><span data-ttu-id="3cf05-106">INapEnforcementClientCallback：： GetConnections 方法</span><span class="sxs-lookup"><span data-stu-id="3cf05-106">INapEnforcementClientCallback::GetConnections method</span></span>

> [!Note]  
> <span data-ttu-id="3cf05-107">從 Windows 10 開始，無法使用網路存取保護平臺</span><span class="sxs-lookup"><span data-stu-id="3cf05-107">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="3cf05-108">**INapEnforcementClientCallback：： GetConnections** 回呼方法是由 NapAgent 呼叫，並且由強制用戶端所執行，以傳回一組連接。</span><span class="sxs-lookup"><span data-stu-id="3cf05-108">The **INapEnforcementClientCallback::GetConnections** callback method is called by the NapAgent and implemented by the enforcement client to return a set of connections.</span></span>

## <a name="syntax"></a><span data-ttu-id="3cf05-109">語法</span><span class="sxs-lookup"><span data-stu-id="3cf05-109">Syntax</span></span>


```C++
HRESULT GetConnections(
  [out] Connections **connections
);
```



## <a name="parameters"></a><span data-ttu-id="3cf05-110">參數</span><span class="sxs-lookup"><span data-stu-id="3cf05-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3cf05-111">*連接* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="3cf05-111">*connections* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="3cf05-112">目前維護之 [**連接**](connections-struct.md)集的指標。</span><span class="sxs-lookup"><span data-stu-id="3cf05-112">A pointer to the current set of maintained [**Connections**](connections-struct.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3cf05-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="3cf05-113">Return value</span></span>

<span data-ttu-id="3cf05-114">此回呼方法必須傳回下列其中一個錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="3cf05-114">This callback method must return one the following error codes.</span></span>



| <span data-ttu-id="3cf05-115">傳回碼</span><span class="sxs-lookup"><span data-stu-id="3cf05-115">Return code</span></span>                                                                                                | <span data-ttu-id="3cf05-116">Description</span><span class="sxs-lookup"><span data-stu-id="3cf05-116">Description</span></span>                                                                                                                                                                                                           |
|------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="3cf05-117"><dt>**S \_ 確定**</dt></span><span class="sxs-lookup"><span data-stu-id="3cf05-117"><dt>**S\_OK**</dt></span></span> </dl>                       | <span data-ttu-id="3cf05-118">如果作業成功，則傳回此值。</span><span class="sxs-lookup"><span data-stu-id="3cf05-118">Return this value if the operation succeeded.</span></span><br/>                                                                                                                                                              |
| <dl> <span data-ttu-id="3cf05-119"><dt>**RPC \_ S \_ 伺服器 \_ 無法使用**</dt></span><span class="sxs-lookup"><span data-stu-id="3cf05-119"><dt>**RPC\_S\_SERVER\_UNAVAILABLE**</dt></span></span> </dl> | <span data-ttu-id="3cf05-120">傳回這個值會導致從系結的-SHA 清單中移除 enforcer，以及要排清的對應 NapAgent 快取專案。</span><span class="sxs-lookup"><span data-stu-id="3cf05-120">Returning this value causes the enforcer to be removed from the bound-SHA list, and the corresponding NapAgent cache entry to be flushed.</span></span> <span data-ttu-id="3cf05-121">失敗的 SHA 接著可以使用 NapAgent 重新初始化。</span><span class="sxs-lookup"><span data-stu-id="3cf05-121">The failing SHA can then re-initialize itself with the NapAgent.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="3cf05-122">規格需求</span><span class="sxs-lookup"><span data-stu-id="3cf05-122">Requirements</span></span>



| <span data-ttu-id="3cf05-123">需求</span><span class="sxs-lookup"><span data-stu-id="3cf05-123">Requirement</span></span> | <span data-ttu-id="3cf05-124">值</span><span class="sxs-lookup"><span data-stu-id="3cf05-124">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3cf05-125">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="3cf05-125">Minimum supported client</span></span><br/> | <span data-ttu-id="3cf05-126">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="3cf05-126">Windows Vista \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="3cf05-127">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="3cf05-127">Minimum supported server</span></span><br/> | <span data-ttu-id="3cf05-128">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="3cf05-128">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="3cf05-129">標頭</span><span class="sxs-lookup"><span data-stu-id="3cf05-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="3cf05-130"><dt>NapEnforcementClient。h</dt></span><span class="sxs-lookup"><span data-stu-id="3cf05-130"><dt>NapEnforcementClient.h</dt></span></span> </dl>   |
| <span data-ttu-id="3cf05-131">Idl</span><span class="sxs-lookup"><span data-stu-id="3cf05-131">IDL</span></span><br/>                      | <dl> <span data-ttu-id="3cf05-132"><dt>NapEnforcementClient .idl</dt></span><span class="sxs-lookup"><span data-stu-id="3cf05-132"><dt>NapEnforcementClient.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3cf05-133">另請參閱</span><span class="sxs-lookup"><span data-stu-id="3cf05-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3cf05-134">**INapEnforcementClientCallback**</span><span class="sxs-lookup"><span data-stu-id="3cf05-134">**INapEnforcementClientCallback**</span></span>](inapenforcementclientcallback.md)
</dt> </dl>

 

 





