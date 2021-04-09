---
title: 'INapCertRelyingParty UnSubscribeCertByGroup 方法 (NapCertRelyingParty .h) '
description: 從健康情況憑證伺服器取消訂閱 (HCS) 。
ms.assetid: 2b26b110-8aba-487e-bd49-c6afc6af11f8
keywords:
- UnSubscribeCertByGroup 方法 NAP
- UnSubscribeCertByGroup 方法 NAP，INapCertRelyingParty 介面
- INapCertRelyingParty 介面 NAP，UnSubscribeCertByGroup 方法
topic_type:
- apiref
api_name:
- INapCertRelyingParty.UnSubscribeCertByGroup
api_location:
- NapCertRelyingParty.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b01bbad5ef48b5f709f93f018c56b5798907d08c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103934518"
---
# <a name="inapcertrelyingpartyunsubscribecertbygroup-method"></a><span data-ttu-id="fffee-106">INapCertRelyingParty：： UnSubscribeCertByGroup 方法</span><span class="sxs-lookup"><span data-stu-id="fffee-106">INapCertRelyingParty::UnSubscribeCertByGroup method</span></span>

> [!Note]  
> <span data-ttu-id="fffee-107">從 Windows 10 開始，無法使用網路存取保護平臺</span><span class="sxs-lookup"><span data-stu-id="fffee-107">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="fffee-108">**UnSubscribeCertByGroup** 方法會從健康情況憑證伺服器取消訂閱 (HCS) 。</span><span class="sxs-lookup"><span data-stu-id="fffee-108">The **UnSubscribeCertByGroup** method unsubscribes from a health certificate server (HCS).</span></span>

## <a name="syntax"></a><span data-ttu-id="fffee-109">語法</span><span class="sxs-lookup"><span data-stu-id="fffee-109">Syntax</span></span>


```C++
HRESULT UnSubscribeCertByGroup(
  [in]        EnforcementEntityId   id,
  [in] const  VARIANT             * reserved
);
```



## <a name="parameters"></a><span data-ttu-id="fffee-110">參數</span><span class="sxs-lookup"><span data-stu-id="fffee-110">Parameters</span></span>

<dl> <dt>

 <span data-ttu-id="fffee-111"> \[ 中的識別碼\]</span><span class="sxs-lookup"><span data-stu-id="fffee-111">*id* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fffee-112">[**EnforcementEntityId**](nap-datatypes.md) ，其中包含正在取消訂閱之強制用戶端的識別碼。</span><span class="sxs-lookup"><span data-stu-id="fffee-112">An [**EnforcementEntityId**](nap-datatypes.md) that contains the ID of the enforcement client that is unsubscribing.</span></span>

</dd> <dt>

 <span data-ttu-id="fffee-113">*保留* \[在\]</span><span class="sxs-lookup"><span data-stu-id="fffee-113">*reserved* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fffee-114">必須是 **Null**。</span><span class="sxs-lookup"><span data-stu-id="fffee-114">Must be **NULL**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fffee-115">傳回值</span><span class="sxs-lookup"><span data-stu-id="fffee-115">Return value</span></span>

<span data-ttu-id="fffee-116">根據此操作的結果，傳回下列其中一個錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="fffee-116">Returns one of the following error codes based on the result of this operation.</span></span>



| <span data-ttu-id="fffee-117">傳回碼</span><span class="sxs-lookup"><span data-stu-id="fffee-117">Return code</span></span>                                                                                     | <span data-ttu-id="fffee-118">Description</span><span class="sxs-lookup"><span data-stu-id="fffee-118">Description</span></span>                                                        |
|-------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <span data-ttu-id="fffee-119"><dt>**S \_確定**</dt></span><span class="sxs-lookup"><span data-stu-id="fffee-119"><dt>**S\_OK** </dt></span></span> </dl>           | <span data-ttu-id="fffee-120">作業成功。</span><span class="sxs-lookup"><span data-stu-id="fffee-120">The operation is successful.</span></span><br/>                            |
| <dl> <span data-ttu-id="fffee-121"><dt>**E \_ACCESSDENIED**</dt></span><span class="sxs-lookup"><span data-stu-id="fffee-121"><dt>**E\_ACCESSDENIED** </dt></span></span> </dl> | <span data-ttu-id="fffee-122">許可權錯誤，拒絕存取。</span><span class="sxs-lookup"><span data-stu-id="fffee-122">Permissions error, access denied.</span></span><br/>                       |
| <dl> <span data-ttu-id="fffee-123"><dt>**E \_OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="fffee-123"><dt>**E\_OUTOFMEMORY** </dt></span></span> </dl>  | <span data-ttu-id="fffee-124">系統資源限制，無法執行操作。</span><span class="sxs-lookup"><span data-stu-id="fffee-124">System resource limit, could not perform the operation.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="fffee-125">備註</span><span class="sxs-lookup"><span data-stu-id="fffee-125">Remarks</span></span>

<span data-ttu-id="fffee-126">如果沒有其他 HCS 的訂閱者，NapAgent 將會從本機電腦存放區中刪除對應的健康情況憑證。</span><span class="sxs-lookup"><span data-stu-id="fffee-126">If there are no other subscribers to the HCS, the NapAgent will delete the corresponding health certificates from the local machine store.</span></span>

<span data-ttu-id="fffee-127">呼叫這個方法之前，請先呼叫 [**SubscribeCertByGroup**](inapcertrelyingparty-subscribecertbygroup.md)。</span><span class="sxs-lookup"><span data-stu-id="fffee-127">Before calling this method, call [**SubscribeCertByGroup**](inapcertrelyingparty-subscribecertbygroup.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="fffee-128">規格需求</span><span class="sxs-lookup"><span data-stu-id="fffee-128">Requirements</span></span>



| <span data-ttu-id="fffee-129">需求</span><span class="sxs-lookup"><span data-stu-id="fffee-129">Requirement</span></span> | <span data-ttu-id="fffee-130">值</span><span class="sxs-lookup"><span data-stu-id="fffee-130">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="fffee-131">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="fffee-131">Minimum supported client</span></span><br/> | <span data-ttu-id="fffee-132">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="fffee-132">Windows Vista \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="fffee-133">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="fffee-133">Minimum supported server</span></span><br/> | <span data-ttu-id="fffee-134">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="fffee-134">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="fffee-135">標頭</span><span class="sxs-lookup"><span data-stu-id="fffee-135">Header</span></span><br/>                   | <dl> <span data-ttu-id="fffee-136"><dt>NapCertRelyingParty。h</dt></span><span class="sxs-lookup"><span data-stu-id="fffee-136"><dt>NapCertRelyingParty.h</dt></span></span> </dl>   |
| <span data-ttu-id="fffee-137">Idl</span><span class="sxs-lookup"><span data-stu-id="fffee-137">IDL</span></span><br/>                      | <dl> <span data-ttu-id="fffee-138"><dt>NapCertRelyingParty .idl</dt></span><span class="sxs-lookup"><span data-stu-id="fffee-138"><dt>NapCertRelyingParty.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fffee-139">另請參閱</span><span class="sxs-lookup"><span data-stu-id="fffee-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fffee-140">**INapCertRelyingParty**</span><span class="sxs-lookup"><span data-stu-id="fffee-140">**INapCertRelyingParty**</span></span>](inapcertrelyingparty.md)
</dt> </dl>

 

 





