---
title: 'INapSystemHealthValidationRequest SetPrivateData 方法 (NapSystemHealthValidator .h) '
description: 允許 NapServer 儲存狀態資訊。
ms.assetid: 128f9beb-e5da-4b20-bf5e-fcf064209da3
keywords:
- SetPrivateData 方法 NAP
- SetPrivateData 方法 NAP，INapSystemHealthValidationRequest 介面
- INapSystemHealthValidationRequest 介面 NAP，SetPrivateData 方法
topic_type:
- apiref
api_name:
- INapSystemHealthValidationRequest.SetPrivateData
api_location:
- qshvhost.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: da50ca236c08388632e17916decee162b3b71743
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103686088"
---
# <a name="inapsystemhealthvalidationrequestsetprivatedata-method"></a><span data-ttu-id="99292-106">INapSystemHealthValidationRequest：： SetPrivateData 方法</span><span class="sxs-lookup"><span data-stu-id="99292-106">INapSystemHealthValidationRequest::SetPrivateData method</span></span>

> [!Note]  
> <span data-ttu-id="99292-107">從 Windows 10 開始，無法使用網路存取保護平臺</span><span class="sxs-lookup"><span data-stu-id="99292-107">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="99292-108">**INapSystemHealthValidationRequest：： SetPrivateData** 方法允許 NapServer 儲存狀態資訊。</span><span class="sxs-lookup"><span data-stu-id="99292-108">The **INapSystemHealthValidationRequest::SetPrivateData** method allows the NapServer to store state information.</span></span>

## <a name="syntax"></a><span data-ttu-id="99292-109">語法</span><span class="sxs-lookup"><span data-stu-id="99292-109">Syntax</span></span>


```C++
HRESULT SetPrivateData(
  [in] const PrivateData *privateData
);
```



## <a name="parameters"></a><span data-ttu-id="99292-110">參數</span><span class="sxs-lookup"><span data-stu-id="99292-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="99292-111">*privateData* \[在\]</span><span class="sxs-lookup"><span data-stu-id="99292-111">*privateData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="99292-112">[**PrivateData**](/windows/win32/api/naptypes/ns-naptypes-privatedata)資料 blob 的指標，其中包含不透明的狀態資訊。</span><span class="sxs-lookup"><span data-stu-id="99292-112">A pointer to a [**PrivateData**](/windows/win32/api/naptypes/ns-naptypes-privatedata) data blob that contains the opaque state information.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="99292-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="99292-113">Return value</span></span>

<span data-ttu-id="99292-114">也可能傳回其他 COM 特定的錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="99292-114">Other COM-specific error codes also may be returned.</span></span>



| <span data-ttu-id="99292-115">傳回碼</span><span class="sxs-lookup"><span data-stu-id="99292-115">Return code</span></span>                                                                                     | <span data-ttu-id="99292-116">Description</span><span class="sxs-lookup"><span data-stu-id="99292-116">Description</span></span>                                                        |
|-------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <span data-ttu-id="99292-117"><dt>**S \_確定**</dt></span><span class="sxs-lookup"><span data-stu-id="99292-117"><dt>**S\_OK** </dt></span></span> </dl>           | <span data-ttu-id="99292-118">作業成功。</span><span class="sxs-lookup"><span data-stu-id="99292-118">Operation succeeded.</span></span><br/>                                    |
| <dl> <span data-ttu-id="99292-119"><dt>**E \_ACCESSDENIED**</dt></span><span class="sxs-lookup"><span data-stu-id="99292-119"><dt>**E\_ACCESSDENIED** </dt></span></span> </dl> | <span data-ttu-id="99292-120">許可權錯誤，拒絕存取。</span><span class="sxs-lookup"><span data-stu-id="99292-120">Permissions error, access denied.</span></span><br/>                       |
| <dl> <span data-ttu-id="99292-121"><dt>**E \_OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="99292-121"><dt>**E\_OUTOFMEMORY** </dt></span></span> </dl>  | <span data-ttu-id="99292-122">系統資源限制，無法執行操作。</span><span class="sxs-lookup"><span data-stu-id="99292-122">System resource limit, could not perform the operation.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="99292-123">備註</span><span class="sxs-lookup"><span data-stu-id="99292-123">Remarks</span></span>

<span data-ttu-id="99292-124">只有 NapServer 可以解讀資料 blob。</span><span class="sxs-lookup"><span data-stu-id="99292-124">Only the NapServer can interpret the data blob.</span></span>

## <a name="requirements"></a><span data-ttu-id="99292-125">規格需求</span><span class="sxs-lookup"><span data-stu-id="99292-125">Requirements</span></span>



| <span data-ttu-id="99292-126">需求</span><span class="sxs-lookup"><span data-stu-id="99292-126">Requirement</span></span> | <span data-ttu-id="99292-127">值</span><span class="sxs-lookup"><span data-stu-id="99292-127">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="99292-128">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="99292-128">Minimum supported client</span></span><br/> | <span data-ttu-id="99292-129">都不支援</span><span class="sxs-lookup"><span data-stu-id="99292-129">None supported</span></span><br/>                                                                               |
| <span data-ttu-id="99292-130">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="99292-130">Minimum supported server</span></span><br/> | <span data-ttu-id="99292-131">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="99292-131">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="99292-132">標頭</span><span class="sxs-lookup"><span data-stu-id="99292-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="99292-133"><dt>NapSystemHealthValidator。h</dt></span><span class="sxs-lookup"><span data-stu-id="99292-133"><dt>NapSystemHealthValidator.h</dt></span></span> </dl>   |
| <span data-ttu-id="99292-134">Idl</span><span class="sxs-lookup"><span data-stu-id="99292-134">IDL</span></span><br/>                      | <dl> <span data-ttu-id="99292-135"><dt>NapSystemHealthValidator .idl</dt></span><span class="sxs-lookup"><span data-stu-id="99292-135"><dt>NapSystemHealthValidator.idl</dt></span></span> </dl> |
| <span data-ttu-id="99292-136">DLL</span><span class="sxs-lookup"><span data-stu-id="99292-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="99292-137"><dt>Qshvhost.dll</dt></span><span class="sxs-lookup"><span data-stu-id="99292-137"><dt>Qshvhost.dll</dt></span></span> </dl>                 |



## <a name="see-also"></a><span data-ttu-id="99292-138">另請參閱</span><span class="sxs-lookup"><span data-stu-id="99292-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="99292-139">**INapSystemHealthValidationRequest**</span><span class="sxs-lookup"><span data-stu-id="99292-139">**INapSystemHealthValidationRequest**</span></span>](inapsystemhealthvalidationrequest.md)
</dt> </dl>

 

 





