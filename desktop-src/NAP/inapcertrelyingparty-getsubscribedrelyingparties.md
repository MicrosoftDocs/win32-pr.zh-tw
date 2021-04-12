---
title: 'INapCertRelyingParty GetSubscribedRelyingParties 方法 (NapCertRelyingParty .h) '
description: 取得已訂閱的信賴憑證者清單。
ms.assetid: 7eef28fd-71cd-4765-89a5-2c9ce29fdc00
keywords:
- GetSubscribedRelyingParties 方法 NAP
- GetSubscribedRelyingParties 方法 NAP，INapCertRelyingParty 介面
- INapCertRelyingParty 介面 NAP，GetSubscribedRelyingParties 方法
topic_type:
- apiref
api_name:
- INapCertRelyingParty.GetSubscribedRelyingParties
api_location:
- NapCertRelyingParty.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a84871838324c431278d15bb9e78471f48aa1f34
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104464489"
---
# <a name="inapcertrelyingpartygetsubscribedrelyingparties-method"></a><span data-ttu-id="48f4d-106">INapCertRelyingParty：： GetSubscribedRelyingParties 方法</span><span class="sxs-lookup"><span data-stu-id="48f4d-106">INapCertRelyingParty::GetSubscribedRelyingParties method</span></span>

> [!Note]  
> <span data-ttu-id="48f4d-107">從 Windows 10 開始，無法使用網路存取保護平臺</span><span class="sxs-lookup"><span data-stu-id="48f4d-107">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="48f4d-108">**GetSubscribedRelyingParties** 方法會取得已訂閱的信賴憑證者清單。</span><span class="sxs-lookup"><span data-stu-id="48f4d-108">The **GetSubscribedRelyingParties** method gets a list of relying parties that have subscribed.</span></span>

## <a name="syntax"></a><span data-ttu-id="48f4d-109">語法</span><span class="sxs-lookup"><span data-stu-id="48f4d-109">Syntax</span></span>


```C++
HRESULT GetSubscribedRelyingParties(
  [out] EnforcementEntityCount *count,
  [out]  EnforcementEntityId   **relyingParties
);
```



## <a name="parameters"></a><span data-ttu-id="48f4d-110">參數</span><span class="sxs-lookup"><span data-stu-id="48f4d-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="48f4d-111">*計數* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="48f4d-111">*count* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="48f4d-112">[**EnforcementEntityCount**](nap-datatypes.md)的指標，其中包含已訂閱的信賴憑證者數目。</span><span class="sxs-lookup"><span data-stu-id="48f4d-112">A pointer to a [**EnforcementEntityCount**](nap-datatypes.md) that contains the number of subscribed relying parties.</span></span>

</dd> <dt>

<span data-ttu-id="48f4d-113">*relyingParties* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="48f4d-113">*relyingParties* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="48f4d-114">指向 [**EnforcementEntityId**](nap-datatypes.md) 的指標，其中包含已訂閱之信賴憑證者的清單。</span><span class="sxs-lookup"><span data-stu-id="48f4d-114">A pointer to a pointer to an [**EnforcementEntityId**](nap-datatypes.md) that contains the list of subscribed relying parties.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="48f4d-115">傳回值</span><span class="sxs-lookup"><span data-stu-id="48f4d-115">Return value</span></span>

<span data-ttu-id="48f4d-116">根據此操作的結果，傳回下列其中一個錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="48f4d-116">Returns one of the following error codes based on the result of this operation.</span></span>



| <span data-ttu-id="48f4d-117">傳回碼</span><span class="sxs-lookup"><span data-stu-id="48f4d-117">Return code</span></span>                                                                                     | <span data-ttu-id="48f4d-118">Description</span><span class="sxs-lookup"><span data-stu-id="48f4d-118">Description</span></span>                                                        |
|-------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <span data-ttu-id="48f4d-119"><dt>**S \_確定**</dt></span><span class="sxs-lookup"><span data-stu-id="48f4d-119"><dt>**S\_OK** </dt></span></span> </dl>           | <span data-ttu-id="48f4d-120">作業成功。</span><span class="sxs-lookup"><span data-stu-id="48f4d-120">The operation is successful.</span></span><br/>                            |
| <dl> <span data-ttu-id="48f4d-121"><dt>**E \_ACCESSDENIED**</dt></span><span class="sxs-lookup"><span data-stu-id="48f4d-121"><dt>**E\_ACCESSDENIED** </dt></span></span> </dl> | <span data-ttu-id="48f4d-122">許可權錯誤，拒絕存取。</span><span class="sxs-lookup"><span data-stu-id="48f4d-122">Permissions error, access denied.</span></span><br/>                       |
| <dl> <span data-ttu-id="48f4d-123"><dt>**E \_OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="48f4d-123"><dt>**E\_OUTOFMEMORY** </dt></span></span> </dl>  | <span data-ttu-id="48f4d-124">系統資源限制，無法執行操作。</span><span class="sxs-lookup"><span data-stu-id="48f4d-124">System resource limit, could not perform the operation.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="48f4d-125">備註</span><span class="sxs-lookup"><span data-stu-id="48f4d-125">Remarks</span></span>

<span data-ttu-id="48f4d-126">呼叫端必須使用 **CoTaskMemFree** 釋放 *relyingParties* 參數。</span><span class="sxs-lookup"><span data-stu-id="48f4d-126">The caller must free the *relyingParties* parameter using **CoTaskMemFree**.</span></span>

## <a name="requirements"></a><span data-ttu-id="48f4d-127">規格需求</span><span class="sxs-lookup"><span data-stu-id="48f4d-127">Requirements</span></span>



| <span data-ttu-id="48f4d-128">需求</span><span class="sxs-lookup"><span data-stu-id="48f4d-128">Requirement</span></span> | <span data-ttu-id="48f4d-129">值</span><span class="sxs-lookup"><span data-stu-id="48f4d-129">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="48f4d-130">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="48f4d-130">Minimum supported client</span></span><br/> | <span data-ttu-id="48f4d-131">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="48f4d-131">Windows Vista \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="48f4d-132">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="48f4d-132">Minimum supported server</span></span><br/> | <span data-ttu-id="48f4d-133">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="48f4d-133">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="48f4d-134">標頭</span><span class="sxs-lookup"><span data-stu-id="48f4d-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="48f4d-135"><dt>NapCertRelyingParty。h</dt></span><span class="sxs-lookup"><span data-stu-id="48f4d-135"><dt>NapCertRelyingParty.h</dt></span></span> </dl>   |
| <span data-ttu-id="48f4d-136">Idl</span><span class="sxs-lookup"><span data-stu-id="48f4d-136">IDL</span></span><br/>                      | <dl> <span data-ttu-id="48f4d-137"><dt>NapCertRelyingParty .idl</dt></span><span class="sxs-lookup"><span data-stu-id="48f4d-137"><dt>NapCertRelyingParty.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="48f4d-138">另請參閱</span><span class="sxs-lookup"><span data-stu-id="48f4d-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="48f4d-139">**INapCertRelyingParty**</span><span class="sxs-lookup"><span data-stu-id="48f4d-139">**INapCertRelyingParty**</span></span>](inapcertrelyingparty.md)
</dt> </dl>

 

 





