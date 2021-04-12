---
description: 將 ITransactionProxy 的執行與目前的內容產生關聯。
ms.assetid: 64009632-b536-41fb-95ac-b23e2cbf18da
title: ICoNtextTransactionInfo：： RegisterTransactionProxy 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IContextTransactionInfo.RegisterTransactionProxy
api_type:
- COM
api_location: ''
ms.openlocfilehash: 7b559453b0d4ed75f92f7a421be4c3a47e07fdf7
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104317932"
---
# <a name="icontexttransactioninforegistertransactionproxy-method"></a><span data-ttu-id="8ab9e-103">ICoNtextTransactionInfo：： RegisterTransactionProxy 方法</span><span class="sxs-lookup"><span data-stu-id="8ab9e-103">IContextTransactionInfo::RegisterTransactionProxy method</span></span>

<span data-ttu-id="8ab9e-104">將 [**ITransactionProxy**](/windows/desktop/api/ComSvcs/nn-comsvcs-itransactionproxy) 的執行與目前的內容產生關聯。</span><span class="sxs-lookup"><span data-stu-id="8ab9e-104">Associates an [**ITransactionProxy**](/windows/desktop/api/ComSvcs/nn-comsvcs-itransactionproxy) implementation with the current context.</span></span>

## <a name="syntax"></a><span data-ttu-id="8ab9e-105">語法</span><span class="sxs-lookup"><span data-stu-id="8ab9e-105">Syntax</span></span>


```C++
HRESULT RegisterTransactionProxy(
  [in]  ITransactionProxy *pProxy,
  [out] GUID              *pGuid
);
```



## <a name="parameters"></a><span data-ttu-id="8ab9e-106">參數</span><span class="sxs-lookup"><span data-stu-id="8ab9e-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8ab9e-107">*pProxy* \[在\]</span><span class="sxs-lookup"><span data-stu-id="8ab9e-107">*pProxy* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8ab9e-108">要與目前內容建立關聯的 [**ITransactionProxy**](/windows/desktop/api/ComSvcs/nn-comsvcs-itransactionproxy) 執行。</span><span class="sxs-lookup"><span data-stu-id="8ab9e-108">An [**ITransactionProxy**](/windows/desktop/api/ComSvcs/nn-comsvcs-itransactionproxy) implementation to associate with the current context.</span></span>

</dd> <dt>

<span data-ttu-id="8ab9e-109">*pGuid* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="8ab9e-109">*pGuid* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="8ab9e-110">識別交易 proxy 的 GUID。</span><span class="sxs-lookup"><span data-stu-id="8ab9e-110">A GUID that identifies the transaction proxy.</span></span> <span data-ttu-id="8ab9e-111">在交易 proxy 上呼叫 [**ITransactionProxy：： Commit**](/windows/desktop/api/ComSvcs/nf-comsvcs-itransactionproxy-commit) 時，com + 會使用此 GUID。</span><span class="sxs-lookup"><span data-stu-id="8ab9e-111">COM+ uses this GUID when calling [**ITransactionProxy::Commit**](/windows/desktop/api/ComSvcs/nf-comsvcs-itransactionproxy-commit) on the transaction proxy.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8ab9e-112">傳回值</span><span class="sxs-lookup"><span data-stu-id="8ab9e-112">Return value</span></span>

<span data-ttu-id="8ab9e-113">這個方法可以傳回標準傳回值 E \_ INVALIDARG、e \_ OUTOFMEMORY 和 e 非 \_ 預期的，以及下列值。</span><span class="sxs-lookup"><span data-stu-id="8ab9e-113">This method can return the standard return values E\_INVALIDARG, E\_OUTOFMEMORY, and E\_UNEXPECTED, as well as the following values.</span></span>



| <span data-ttu-id="8ab9e-114">傳回碼</span><span class="sxs-lookup"><span data-stu-id="8ab9e-114">Return code</span></span>                                                                                                     | <span data-ttu-id="8ab9e-115">Description</span><span class="sxs-lookup"><span data-stu-id="8ab9e-115">Description</span></span>                                                                                                             |
|-----------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="8ab9e-116"><dt>**S \_ 確定**</dt></span><span class="sxs-lookup"><span data-stu-id="8ab9e-116"><dt>**S\_OK**</dt></span></span> </dl>                            | <span data-ttu-id="8ab9e-117">已成功完成命令。</span><span class="sxs-lookup"><span data-stu-id="8ab9e-117">The method completed successfully.</span></span><br/>                                                                           |
| <dl> <span data-ttu-id="8ab9e-118"><dt>**內容 \_ E \_ ALREADYINTRANSACTION**</dt></span><span class="sxs-lookup"><span data-stu-id="8ab9e-118"><dt>**CONTEXT\_E\_ALREADYINTRANSACTION**</dt></span></span> </dl> | <span data-ttu-id="8ab9e-119">目前的內容已有相關聯的 [**ITransactionProxy**](/windows/desktop/api/ComSvcs/nn-comsvcs-itransactionproxy) 執行。</span><span class="sxs-lookup"><span data-stu-id="8ab9e-119">The current context already has an associated [**ITransactionProxy**](/windows/desktop/api/ComSvcs/nn-comsvcs-itransactionproxy) implementation.</span></span><br/> |
| <dl> <span data-ttu-id="8ab9e-120"><dt>**E \_ >NOTIMPL**</dt></span><span class="sxs-lookup"><span data-stu-id="8ab9e-120"><dt>**E\_NOTIMPL**</dt></span></span> </dl>                       | <span data-ttu-id="8ab9e-121">目前的內容是裝載「攜帶您自己的交易」 (BYOT) 交易或非根交易。</span><span class="sxs-lookup"><span data-stu-id="8ab9e-121">The current context is hosting a Bring Your Own Transaction (BYOT) transaction or a non-root transaction.</span></span><br/>    |



 

## <a name="remarks"></a><span data-ttu-id="8ab9e-122">備註</span><span class="sxs-lookup"><span data-stu-id="8ab9e-122">Remarks</span></span>

<span data-ttu-id="8ab9e-123">只有在目前的內容是根交易內容時，才能呼叫 **RegisterTransactionProxy** 方法。</span><span class="sxs-lookup"><span data-stu-id="8ab9e-123">The **RegisterTransactionProxy** method can only be called if the current context is a root transaction context.</span></span> <span data-ttu-id="8ab9e-124">如果內容裝載 BYOT 交易或非根交易，則無法呼叫它。</span><span class="sxs-lookup"><span data-stu-id="8ab9e-124">It cannot be called if the context is hosting a BYOT transaction or a non-root transaction.</span></span>

## <a name="requirements"></a><span data-ttu-id="8ab9e-125">規格需求</span><span class="sxs-lookup"><span data-stu-id="8ab9e-125">Requirements</span></span>



| <span data-ttu-id="8ab9e-126">需求</span><span class="sxs-lookup"><span data-stu-id="8ab9e-126">Requirement</span></span> | <span data-ttu-id="8ab9e-127">值</span><span class="sxs-lookup"><span data-stu-id="8ab9e-127">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------|
| <span data-ttu-id="8ab9e-128">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="8ab9e-128">Minimum supported client</span></span><br/> | <span data-ttu-id="8ab9e-129">僅限 Windows XP （含 SP2） \[ 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="8ab9e-129">Windows XP with SP2 \[desktop apps only\]</span></span><br/>          |
| <span data-ttu-id="8ab9e-130">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="8ab9e-130">Minimum supported server</span></span><br/> | <span data-ttu-id="8ab9e-131">僅限 Windows Server 2003 與 SP1 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="8ab9e-131">Windows Server 2003 with SP1 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="8ab9e-132">另請參閱</span><span class="sxs-lookup"><span data-stu-id="8ab9e-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8ab9e-133">**ICoNtextTransactionInfo**</span><span class="sxs-lookup"><span data-stu-id="8ab9e-133">**IContextTransactionInfo**</span></span>](icontexttransactioninfo.md)
</dt> </dl>

 

 




