---
title: 'INapSystemHealthValidationRequest GetPrivateData 方法 (NapSystemHealthValidator .h) '
description: 允許 NapServer 捕獲狀態資訊。
ms.assetid: f85026ca-852b-4eb1-9a8c-7e03cd1765f2
keywords:
- GetPrivateData 方法 NAP
- GetPrivateData 方法 NAP，INapSystemHealthValidationRequest 介面
- INapSystemHealthValidationRequest 介面 NAP，GetPrivateData 方法
topic_type:
- apiref
api_name:
- INapSystemHealthValidationRequest.GetPrivateData
api_location:
- qshvhost.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d78cceba42cd503ef8a875ece8f4ed196eaeff8c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103686369"
---
# <a name="inapsystemhealthvalidationrequestgetprivatedata-method"></a><span data-ttu-id="6a804-106">INapSystemHealthValidationRequest：： GetPrivateData 方法</span><span class="sxs-lookup"><span data-stu-id="6a804-106">INapSystemHealthValidationRequest::GetPrivateData method</span></span>

> [!Note]  
> <span data-ttu-id="6a804-107">從 Windows 10 開始，無法使用網路存取保護平臺</span><span class="sxs-lookup"><span data-stu-id="6a804-107">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="6a804-108">**INapSystemHealthValidationRequest：： GetPrivateData** 方法可讓 NapServer 取得狀態資訊。</span><span class="sxs-lookup"><span data-stu-id="6a804-108">The **INapSystemHealthValidationRequest::GetPrivateData** method allows the NapServer to retrieve state information.</span></span>

## <a name="syntax"></a><span data-ttu-id="6a804-109">語法</span><span class="sxs-lookup"><span data-stu-id="6a804-109">Syntax</span></span>


```C++
HRESULT GetPrivateData(
  [out] PrivateData **privateData
);
```



## <a name="parameters"></a><span data-ttu-id="6a804-110">參數</span><span class="sxs-lookup"><span data-stu-id="6a804-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6a804-111">*privateData* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="6a804-111">*privateData* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="6a804-112">指標，指向 [**PrivateData**](/windows/win32/api/naptypes/ns-naptypes-privatedata) 包含狀態資訊之不透明資料 blob 的指標。</span><span class="sxs-lookup"><span data-stu-id="6a804-112">A pointer to a pointer to [**PrivateData**](/windows/win32/api/naptypes/ns-naptypes-privatedata) opaque data blob that contains state information.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6a804-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="6a804-113">Return value</span></span>

<span data-ttu-id="6a804-114">也可能傳回其他 COM 特定的錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="6a804-114">Other COM-specific error codes also may be returned.</span></span>



| <span data-ttu-id="6a804-115">傳回碼</span><span class="sxs-lookup"><span data-stu-id="6a804-115">Return code</span></span>                                                                                     | <span data-ttu-id="6a804-116">Description</span><span class="sxs-lookup"><span data-stu-id="6a804-116">Description</span></span>                                                        |
|-------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <span data-ttu-id="6a804-117"><dt>**S \_確定**</dt></span><span class="sxs-lookup"><span data-stu-id="6a804-117"><dt>**S\_OK** </dt></span></span> </dl>           | <span data-ttu-id="6a804-118">作業成功。</span><span class="sxs-lookup"><span data-stu-id="6a804-118">Operation succeeded.</span></span><br/>                                    |
| <dl> <span data-ttu-id="6a804-119"><dt>**E \_ACCESSDENIED**</dt></span><span class="sxs-lookup"><span data-stu-id="6a804-119"><dt>**E\_ACCESSDENIED** </dt></span></span> </dl> | <span data-ttu-id="6a804-120">許可權錯誤，拒絕存取。</span><span class="sxs-lookup"><span data-stu-id="6a804-120">Permissions error, access denied.</span></span><br/>                       |
| <dl> <span data-ttu-id="6a804-121"><dt>**E \_OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="6a804-121"><dt>**E\_OUTOFMEMORY** </dt></span></span> </dl>  | <span data-ttu-id="6a804-122">系統資源限制，無法執行操作。</span><span class="sxs-lookup"><span data-stu-id="6a804-122">System resource limit, could not perform the operation.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="6a804-123">備註</span><span class="sxs-lookup"><span data-stu-id="6a804-123">Remarks</span></span>

<span data-ttu-id="6a804-124">只有 NapServer 可以解讀資料 blob。</span><span class="sxs-lookup"><span data-stu-id="6a804-124">Only the NapServer can interpret the data blob.</span></span>

## <a name="requirements"></a><span data-ttu-id="6a804-125">規格需求</span><span class="sxs-lookup"><span data-stu-id="6a804-125">Requirements</span></span>



| <span data-ttu-id="6a804-126">需求</span><span class="sxs-lookup"><span data-stu-id="6a804-126">Requirement</span></span> | <span data-ttu-id="6a804-127">值</span><span class="sxs-lookup"><span data-stu-id="6a804-127">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6a804-128">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="6a804-128">Minimum supported client</span></span><br/> | <span data-ttu-id="6a804-129">都不支援</span><span class="sxs-lookup"><span data-stu-id="6a804-129">None supported</span></span><br/>                                                                               |
| <span data-ttu-id="6a804-130">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="6a804-130">Minimum supported server</span></span><br/> | <span data-ttu-id="6a804-131">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="6a804-131">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="6a804-132">標頭</span><span class="sxs-lookup"><span data-stu-id="6a804-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="6a804-133"><dt>NapSystemHealthValidator。h</dt></span><span class="sxs-lookup"><span data-stu-id="6a804-133"><dt>NapSystemHealthValidator.h</dt></span></span> </dl>   |
| <span data-ttu-id="6a804-134">Idl</span><span class="sxs-lookup"><span data-stu-id="6a804-134">IDL</span></span><br/>                      | <dl> <span data-ttu-id="6a804-135"><dt>NapSystemHealthValidator .idl</dt></span><span class="sxs-lookup"><span data-stu-id="6a804-135"><dt>NapSystemHealthValidator.idl</dt></span></span> </dl> |
| <span data-ttu-id="6a804-136">DLL</span><span class="sxs-lookup"><span data-stu-id="6a804-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6a804-137"><dt>Qshvhost.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6a804-137"><dt>Qshvhost.dll</dt></span></span> </dl>                 |



## <a name="see-also"></a><span data-ttu-id="6a804-138">另請參閱</span><span class="sxs-lookup"><span data-stu-id="6a804-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6a804-139">**INapSystemHealthValidationRequest**</span><span class="sxs-lookup"><span data-stu-id="6a804-139">**INapSystemHealthValidationRequest**</span></span>](inapsystemhealthvalidationrequest.md)
</dt> </dl>

 

 





