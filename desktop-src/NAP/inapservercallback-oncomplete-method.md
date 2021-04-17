---
title: 'INapServerCallback OnComplete 方法 (NapSystemHealthValidator .h) '
description: 由 Shv 用來指示非同步要求完成。
ms.assetid: 959ee4ac-7c29-4013-a174-24abc6a580c7
keywords:
- OnComplete 方法 NAP
- OnComplete 方法 NAP，INapServerCallback 介面
- INapServerCallback 介面 NAP，OnComplete 方法
topic_type:
- apiref
api_name:
- INapServerCallback.OnComplete
api_location:
- qshvhost.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8ef846d3d9dc2d6618f0eca9f097d74222606eb4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104467060"
---
# <a name="inapservercallbackoncomplete-method"></a><span data-ttu-id="21369-106">INapServerCallback：： OnComplete 方法</span><span class="sxs-lookup"><span data-stu-id="21369-106">INapServerCallback::OnComplete method</span></span>

> [!Note]  
> <span data-ttu-id="21369-107">從 Windows 10 開始，無法使用網路存取保護平臺</span><span class="sxs-lookup"><span data-stu-id="21369-107">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="21369-108">Shv 會使用 **INapServerCallback：： OnComplete** 方法來通知非同步要求完成。</span><span class="sxs-lookup"><span data-stu-id="21369-108">The **INapServerCallback::OnComplete** method is used by SHVs to signal asynchronous request completion.</span></span>

## <a name="syntax"></a><span data-ttu-id="21369-109">語法</span><span class="sxs-lookup"><span data-stu-id="21369-109">Syntax</span></span>


```C++
HRESULT OnComplete(
  [in] INapSystemHealthValidationRequest *request,
  [in] HRESULT                           errorCode
);
```



## <a name="parameters"></a><span data-ttu-id="21369-110">參數</span><span class="sxs-lookup"><span data-stu-id="21369-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="21369-111">*要求* \[在\]</span><span class="sxs-lookup"><span data-stu-id="21369-111">*request* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="21369-112">代表驗證要求之 [**INapSystemHealthValidationRequest**](inapsystemhealthvalidationrequest.md) 物件的指標。</span><span class="sxs-lookup"><span data-stu-id="21369-112">A pointer to an [**INapSystemHealthValidationRequest**](inapsystemhealthvalidationrequest.md) object that represents a validation request.</span></span>

</dd> <dt>

<span data-ttu-id="21369-113">*errorCode* \[在\]</span><span class="sxs-lookup"><span data-stu-id="21369-113">*errorCode* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="21369-114">指出無法執行驗證之原因的 [**NAP 錯誤碼**](nap-error-constants.md) 。</span><span class="sxs-lookup"><span data-stu-id="21369-114">A [**NAP error code**](nap-error-constants.md) that indicates the reason why the validation could not be performed.</span></span>

> [!Note]  
> <span data-ttu-id="21369-115">一般而言， [**INapSystemHealthValidationRequest：： SetSoHResponse**](inapsystemhealthvalidationrequest-setsohresponse-method.md) 方法的傳回值會傳遞給這個參數。</span><span class="sxs-lookup"><span data-stu-id="21369-115">Typically, the return value of the [**INapSystemHealthValidationRequest::SetSoHResponse**](inapsystemhealthvalidationrequest-setsohresponse-method.md) method is passed to this parameter.</span></span> <span data-ttu-id="21369-116">但是，如果因為重新處理失敗而無法呼叫 **SetSoHResponse** ，就會傳遞 failed 命令所傳回的值。</span><span class="sxs-lookup"><span data-stu-id="21369-116">However, if **SetSoHResponse** could not be called due to a reprocessing failure, the value returned by the failed command is passed.</span></span>

 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="21369-117">傳回值</span><span class="sxs-lookup"><span data-stu-id="21369-117">Return value</span></span>

<span data-ttu-id="21369-118">也可能傳回其他 COM 特定的錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="21369-118">Other COM-specific error codes also may be returned.</span></span>



| <span data-ttu-id="21369-119">傳回碼</span><span class="sxs-lookup"><span data-stu-id="21369-119">Return code</span></span>                                                                                     | <span data-ttu-id="21369-120">Description</span><span class="sxs-lookup"><span data-stu-id="21369-120">Description</span></span>                                                        |
|-------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <span data-ttu-id="21369-121"><dt>**S \_確定**</dt></span><span class="sxs-lookup"><span data-stu-id="21369-121"><dt>**S\_OK** </dt></span></span> </dl>           | <span data-ttu-id="21369-122">作業成功。</span><span class="sxs-lookup"><span data-stu-id="21369-122">Operation succeeded.</span></span><br/>                                    |
| <dl> <span data-ttu-id="21369-123"><dt>**E \_ACCESSDENIED**</dt></span><span class="sxs-lookup"><span data-stu-id="21369-123"><dt>**E\_ACCESSDENIED** </dt></span></span> </dl> | <span data-ttu-id="21369-124">許可權錯誤，拒絕存取。</span><span class="sxs-lookup"><span data-stu-id="21369-124">Permissions error, access denied.</span></span><br/>                       |
| <dl> <span data-ttu-id="21369-125"><dt>**E \_OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="21369-125"><dt>**E\_OUTOFMEMORY** </dt></span></span> </dl>  | <span data-ttu-id="21369-126">系統資源限制，無法執行操作。</span><span class="sxs-lookup"><span data-stu-id="21369-126">System resource limit, could not perform the operation.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="21369-127">備註</span><span class="sxs-lookup"><span data-stu-id="21369-127">Remarks</span></span>

<span data-ttu-id="21369-128">\_無論 **SoHRequest** 是否通過健康情況檢查，驗證程式都必須傳回 S，才能完成 [**SoHRequest**](/windows/win32/api/naptypes/ns-naptypes-soh)驗證。</span><span class="sxs-lookup"><span data-stu-id="21369-128">Validators must return S\_OK if the [**SoHRequest**](/windows/win32/api/naptypes/ns-naptypes-soh) validation could be completed, regardless of whether the **SoHRequest** passed the health check.</span></span>

## <a name="requirements"></a><span data-ttu-id="21369-129">規格需求</span><span class="sxs-lookup"><span data-stu-id="21369-129">Requirements</span></span>



| <span data-ttu-id="21369-130">需求</span><span class="sxs-lookup"><span data-stu-id="21369-130">Requirement</span></span> | <span data-ttu-id="21369-131">值</span><span class="sxs-lookup"><span data-stu-id="21369-131">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="21369-132">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="21369-132">Minimum supported client</span></span><br/> | <span data-ttu-id="21369-133">都不支援</span><span class="sxs-lookup"><span data-stu-id="21369-133">None supported</span></span><br/>                                                                               |
| <span data-ttu-id="21369-134">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="21369-134">Minimum supported server</span></span><br/> | <span data-ttu-id="21369-135">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="21369-135">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="21369-136">標頭</span><span class="sxs-lookup"><span data-stu-id="21369-136">Header</span></span><br/>                   | <dl> <span data-ttu-id="21369-137"><dt>NapSystemHealthValidator。h</dt></span><span class="sxs-lookup"><span data-stu-id="21369-137"><dt>NapSystemHealthValidator.h</dt></span></span> </dl>   |
| <span data-ttu-id="21369-138">Idl</span><span class="sxs-lookup"><span data-stu-id="21369-138">IDL</span></span><br/>                      | <dl> <span data-ttu-id="21369-139"><dt>NapSystemHealthValidator .idl</dt></span><span class="sxs-lookup"><span data-stu-id="21369-139"><dt>NapSystemHealthValidator.idl</dt></span></span> </dl> |
| <span data-ttu-id="21369-140">DLL</span><span class="sxs-lookup"><span data-stu-id="21369-140">DLL</span></span><br/>                      | <dl> <span data-ttu-id="21369-141"><dt>Qshvhost.dll</dt></span><span class="sxs-lookup"><span data-stu-id="21369-141"><dt>Qshvhost.dll</dt></span></span> </dl>                 |



## <a name="see-also"></a><span data-ttu-id="21369-142">另請參閱</span><span class="sxs-lookup"><span data-stu-id="21369-142">See also</span></span>

<dl> <span data-ttu-id="21369-143"><dt>


</dt> <dt></span><span class="sxs-lookup"><span data-stu-id="21369-143"><dt>


</dt> <dt></span></span>

[<span data-ttu-id="21369-144">**INapServerCallback**</span><span class="sxs-lookup"><span data-stu-id="21369-144">**INapServerCallback**</span></span>](inapservercallback.md)
</dt> <dt>

[<span data-ttu-id="21369-145">**INapSystemHealthValidationRequest**</span><span class="sxs-lookup"><span data-stu-id="21369-145">**INapSystemHealthValidationRequest**</span></span>](inapsystemhealthvalidationrequest.md)
</dt> </dl>

 

 





