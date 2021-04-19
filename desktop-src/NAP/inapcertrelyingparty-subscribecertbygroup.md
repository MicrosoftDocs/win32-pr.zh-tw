---
title: 'INapCertRelyingParty SubscribeCertByGroup 方法 (NapCertRelyingParty .h) '
description: 訂閱健康情況憑證伺服器 (HCS) 。
ms.assetid: 6fce113d-e183-45d7-8fb5-e04b6f4afcca
keywords:
- SubscribeCertByGroup 方法 NAP
- SubscribeCertByGroup 方法 NAP，INapCertRelyingParty 介面
- INapCertRelyingParty 介面 NAP，SubscribeCertByGroup 方法
topic_type:
- apiref
api_name:
- INapCertRelyingParty.SubscribeCertByGroup
api_location:
- NapCertRelyingParty.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 053c3c2dbf00e706003988bd5769cb2aa9201c41
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106999607"
---
# <a name="inapcertrelyingpartysubscribecertbygroup-method"></a><span data-ttu-id="9a847-106">INapCertRelyingParty：： SubscribeCertByGroup 方法</span><span class="sxs-lookup"><span data-stu-id="9a847-106">INapCertRelyingParty::SubscribeCertByGroup method</span></span>

> [!Note]  
> <span data-ttu-id="9a847-107">從 Windows 10 開始，無法使用網路存取保護平臺</span><span class="sxs-lookup"><span data-stu-id="9a847-107">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="9a847-108">**SubscribeCertByGroup** 方法會訂閱健康情況憑證伺服器 (HCS) 。</span><span class="sxs-lookup"><span data-stu-id="9a847-108">The **SubscribeCertByGroup** method subscribes to a health certificate server (HCS).</span></span> <span data-ttu-id="9a847-109">HCS 必須已在訂閱之前註冊。</span><span class="sxs-lookup"><span data-stu-id="9a847-109">The HCS must already be registered before subscribing.</span></span>

## <a name="syntax"></a><span data-ttu-id="9a847-110">語法</span><span class="sxs-lookup"><span data-stu-id="9a847-110">Syntax</span></span>


```C++
HRESULT SubscribeCertByGroup(
  [in]        EnforcementEntityId  id,
  [in]  const BSTR                subscriberName,
  [in]  const  VARIANT            *reserved,
  [out]       BOOL                *certExists
);
```



## <a name="parameters"></a><span data-ttu-id="9a847-111">參數</span><span class="sxs-lookup"><span data-stu-id="9a847-111">Parameters</span></span>

<dl> <dt>

 <span data-ttu-id="9a847-112"> \[ 中的識別碼\]</span><span class="sxs-lookup"><span data-stu-id="9a847-112">*id* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9a847-113">[**EnforcementEntityId**](nap-datatypes.md) ，其中包含所訂閱之強制用戶端的識別碼。</span><span class="sxs-lookup"><span data-stu-id="9a847-113">An [**EnforcementEntityId**](nap-datatypes.md) that contains the ID of the enforcement client that is subscribing.</span></span>

</dd> <dt>

<span data-ttu-id="9a847-114">*microsoft.sqlserver.replication.subscription.subscribername* \[在\]</span><span class="sxs-lookup"><span data-stu-id="9a847-114">*subscriberName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9a847-115">訂閱者的名稱。</span><span class="sxs-lookup"><span data-stu-id="9a847-115">The name of the subscriber.</span></span>

> [!Note]  
> <span data-ttu-id="9a847-116">這目前僅供記錄之用。</span><span class="sxs-lookup"><span data-stu-id="9a847-116">This is currently only used for logging purposes.</span></span>

 

</dd> <dt>

<span data-ttu-id="9a847-117">*保留* \[在\]</span><span class="sxs-lookup"><span data-stu-id="9a847-117">*reserved* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9a847-118">必須是 **Null**。</span><span class="sxs-lookup"><span data-stu-id="9a847-118">Must be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="9a847-119">*certExists* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="9a847-119">*certExists* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="9a847-120">指出此 HCS 的健康情況憑證是否已由 NapAgent 維護，並存在於電腦存放區中。</span><span class="sxs-lookup"><span data-stu-id="9a847-120">Indicates whether a health certificate from this HCS is already being maintained by the NapAgent and is present in the machine store.</span></span> <span data-ttu-id="9a847-121">若 **為 TRUE**，則表示健康狀態憑證已在維護中且存在。</span><span class="sxs-lookup"><span data-stu-id="9a847-121">If **TRUE**, a health certificate is already being maintained and is present.</span></span> <span data-ttu-id="9a847-122">如果 **為 FALSE**，則表示健康情況憑證目前未進行維護，而且不存在。</span><span class="sxs-lookup"><span data-stu-id="9a847-122">If **FALSE**, a health certificate is not currently being maintained and present.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9a847-123">傳回值</span><span class="sxs-lookup"><span data-stu-id="9a847-123">Return value</span></span>

<span data-ttu-id="9a847-124">根據此操作的結果，傳回下列其中一個錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="9a847-124">Returns one of the following error codes based on the result of this operation.</span></span>



| <span data-ttu-id="9a847-125">傳回碼</span><span class="sxs-lookup"><span data-stu-id="9a847-125">Return code</span></span>                                                                                     | <span data-ttu-id="9a847-126">Description</span><span class="sxs-lookup"><span data-stu-id="9a847-126">Description</span></span>                                                        |
|-------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <span data-ttu-id="9a847-127"><dt>**S \_確定**</dt></span><span class="sxs-lookup"><span data-stu-id="9a847-127"><dt>**S\_OK** </dt></span></span> </dl>           | <span data-ttu-id="9a847-128">作業成功。</span><span class="sxs-lookup"><span data-stu-id="9a847-128">The operation is successful.</span></span><br/>                            |
| <dl> <span data-ttu-id="9a847-129"><dt>**E \_ACCESSDENIED**</dt></span><span class="sxs-lookup"><span data-stu-id="9a847-129"><dt>**E\_ACCESSDENIED** </dt></span></span> </dl> | <span data-ttu-id="9a847-130">許可權錯誤，拒絕存取。</span><span class="sxs-lookup"><span data-stu-id="9a847-130">Permissions error, access denied.</span></span><br/>                       |
| <dl> <span data-ttu-id="9a847-131"><dt>**E \_OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="9a847-131"><dt>**E\_OUTOFMEMORY** </dt></span></span> </dl>  | <span data-ttu-id="9a847-132">系統資源限制，無法執行操作。</span><span class="sxs-lookup"><span data-stu-id="9a847-132">System resource limit, could not perform the operation.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="9a847-133">規格需求</span><span class="sxs-lookup"><span data-stu-id="9a847-133">Requirements</span></span>



| <span data-ttu-id="9a847-134">需求</span><span class="sxs-lookup"><span data-stu-id="9a847-134">Requirement</span></span> | <span data-ttu-id="9a847-135">值</span><span class="sxs-lookup"><span data-stu-id="9a847-135">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9a847-136">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="9a847-136">Minimum supported client</span></span><br/> | <span data-ttu-id="9a847-137">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="9a847-137">Windows Vista \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="9a847-138">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="9a847-138">Minimum supported server</span></span><br/> | <span data-ttu-id="9a847-139">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="9a847-139">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="9a847-140">標頭</span><span class="sxs-lookup"><span data-stu-id="9a847-140">Header</span></span><br/>                   | <dl> <span data-ttu-id="9a847-141"><dt>NapCertRelyingParty。h</dt></span><span class="sxs-lookup"><span data-stu-id="9a847-141"><dt>NapCertRelyingParty.h</dt></span></span> </dl>   |
| <span data-ttu-id="9a847-142">Idl</span><span class="sxs-lookup"><span data-stu-id="9a847-142">IDL</span></span><br/>                      | <dl> <span data-ttu-id="9a847-143"><dt>NapCertRelyingParty .idl</dt></span><span class="sxs-lookup"><span data-stu-id="9a847-143"><dt>NapCertRelyingParty.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9a847-144">另請參閱</span><span class="sxs-lookup"><span data-stu-id="9a847-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9a847-145">**INapCertRelyingParty**</span><span class="sxs-lookup"><span data-stu-id="9a847-145">**INapCertRelyingParty**</span></span>](inapcertrelyingparty.md)
</dt> </dl>

 

 





