---
title: 'INapSystemHealthValidationRequest GetSoHRequest 方法 (NapSystemHealthValidator .h) '
description: 允許 (Shv) 的系統健康狀態驗證，以取得並驗證其系統健康情況代理程式 (SHA) 用戶端上所傳送的 SoHRequest 資訊。
ms.assetid: e06e07c6-7305-4171-b94e-19c360e94c67
keywords:
- GetSoHRequest 方法 NAP
- GetSoHRequest 方法 NAP，INapSystemHealthValidationRequest 介面
- INapSystemHealthValidationRequest 介面 NAP，GetSoHRequest 方法
topic_type:
- apiref
api_name:
- INapSystemHealthValidationRequest.GetSoHRequest
api_location:
- qshvhost.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 306c9307f99f91e0b0a48a1c5ffeaf19b4ea1f12
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104106416"
---
# <a name="inapsystemhealthvalidationrequestgetsohrequest-method"></a><span data-ttu-id="021da-106">INapSystemHealthValidationRequest：： GetSoHRequest 方法</span><span class="sxs-lookup"><span data-stu-id="021da-106">INapSystemHealthValidationRequest::GetSoHRequest method</span></span>

> [!Note]  
> <span data-ttu-id="021da-107">從 Windows 10 開始，無法使用網路存取保護平臺</span><span class="sxs-lookup"><span data-stu-id="021da-107">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="021da-108">**INapSystemHealthValidationRequest：： GetSoHRequest** 方法可讓 (Shv 的系統健全狀況驗證程式) 抓取和驗證用戶端上的系統健康情況代理程式 (SHA) 對應項所傳送的 [**SoHRequest**](/windows/win32/api/naptypes/ns-naptypes-soh)資訊。</span><span class="sxs-lookup"><span data-stu-id="021da-108">The **INapSystemHealthValidationRequest::GetSoHRequest** method allows System Health Validators (SHVs) to retrieve and validate the [**SoHRequest**](/windows/win32/api/naptypes/ns-naptypes-soh) information sent by their System Health Agent (SHA) counterparts on the client.</span></span>

## <a name="syntax"></a><span data-ttu-id="021da-109">語法</span><span class="sxs-lookup"><span data-stu-id="021da-109">Syntax</span></span>


```C++
HRESULT GetSoHRequest(
  [out] SoHRequest **sohRequest,
  [out] BOOL       *napSystemGenerated
);
```



## <a name="parameters"></a><span data-ttu-id="021da-110">參數</span><span class="sxs-lookup"><span data-stu-id="021da-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="021da-111">*sohRequest* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="021da-111">*sohRequest* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="021da-112">指向 [**SoHRequest**](/windows/win32/api/naptypes/ns-naptypes-soh) 結構指標的指標。</span><span class="sxs-lookup"><span data-stu-id="021da-112">A pointer to a pointer to an [**SoHRequest**](/windows/win32/api/naptypes/ns-naptypes-soh) structure.</span></span>

</dd> <dt>

<span data-ttu-id="021da-113">*napSystemGenerated* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="021da-113">*napSystemGenerated* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="021da-114">如果 NapAgent 代表 SHA 建立 SoH，則 **布林\*\*\*\*值為 TRUE** ，否則為 **FALSE** 。</span><span class="sxs-lookup"><span data-stu-id="021da-114">A **BOOL** that is **TRUE** if the SoH was created by the NapAgent on behalf of the SHA and **FALSE** otherwise.</span></span> <span data-ttu-id="021da-115">它主要用來指出對 SHV 的 SHA 失敗。</span><span class="sxs-lookup"><span data-stu-id="021da-115">It is primarily used to indicate an SHA failure to the SHV.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="021da-116">傳回值</span><span class="sxs-lookup"><span data-stu-id="021da-116">Return value</span></span>

<span data-ttu-id="021da-117">也可能傳回其他 COM 特定的錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="021da-117">Other COM-specific error codes also may be returned.</span></span>



| <span data-ttu-id="021da-118">傳回碼</span><span class="sxs-lookup"><span data-stu-id="021da-118">Return code</span></span>                                                                                     | <span data-ttu-id="021da-119">Description</span><span class="sxs-lookup"><span data-stu-id="021da-119">Description</span></span>                                                        |
|-------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <span data-ttu-id="021da-120"><dt>**S \_確定**</dt></span><span class="sxs-lookup"><span data-stu-id="021da-120"><dt>**S\_OK** </dt></span></span> </dl>           | <span data-ttu-id="021da-121">作業成功。</span><span class="sxs-lookup"><span data-stu-id="021da-121">Operation succeeded.</span></span><br/>                                    |
| <dl> <span data-ttu-id="021da-122"><dt>**E \_ACCESSDENIED**</dt></span><span class="sxs-lookup"><span data-stu-id="021da-122"><dt>**E\_ACCESSDENIED** </dt></span></span> </dl> | <span data-ttu-id="021da-123">許可權錯誤，拒絕存取。</span><span class="sxs-lookup"><span data-stu-id="021da-123">Permissions error, access denied.</span></span><br/>                       |
| <dl> <span data-ttu-id="021da-124"><dt>**E \_OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="021da-124"><dt>**E\_OUTOFMEMORY** </dt></span></span> </dl>  | <span data-ttu-id="021da-125">系統資源限制，無法執行操作。</span><span class="sxs-lookup"><span data-stu-id="021da-125">System resource limit, could not perform the operation.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="021da-126">備註</span><span class="sxs-lookup"><span data-stu-id="021da-126">Remarks</span></span>

<span data-ttu-id="021da-127">如果用戶端未將 [**sohRequest**](/windows/win32/api/naptypes/ns-naptypes-soh)傳送至 SHV， *sohRequest* 參數可能會傳回 **Null** 。</span><span class="sxs-lookup"><span data-stu-id="021da-127">The *sohRequest* parameter may return **NULL** if the client did not send an [**SoHRequest**](/windows/win32/api/naptypes/ns-naptypes-soh) to the SHV.</span></span> <span data-ttu-id="021da-128">在該案例中，SHV 可以在 **SoHResponse** 中填入 [**NAP \_ E \_ 缺少 \_ SOH**](nap-error-constants.md)的錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="021da-128">In that scenario the SHV can populate an **SoHResponse** with the error code of [**NAP\_E\_MISSING\_SOH**](nap-error-constants.md).</span></span>

<span data-ttu-id="021da-129">如果 *napSystemGenerated* 參數為 **TRUE**，則 *SoHRequest* 的格式如下所示：</span><span class="sxs-lookup"><span data-stu-id="021da-129">If the *napSystemGenerated* parameter is **TRUE**, the format of *SoHRequest* is as follows:</span></span>

-   <span data-ttu-id="021da-130">[**sohAttributeTypeSystemHealthId**](sohattributetype-enum.md)= <id></span><span class="sxs-lookup"><span data-stu-id="021da-130">[**sohAttributeTypeSystemHealthId**](sohattributetype-enum.md)= <id></span></span>
-   <span data-ttu-id="021da-131">[**sohAttributeTypeFailureCategory**](sohattributetype-enum.md) = [ **failureCategoryClientComponent**](/windows/win32/api/naptypes/ne-naptypes-failurecategory)</span><span class="sxs-lookup"><span data-stu-id="021da-131">[**sohAttributeTypeFailureCategory**](sohattributetype-enum.md)= [**failureCategoryClientComponent**](/windows/win32/api/naptypes/ne-naptypes-failurecategory)</span></span>
-   <span data-ttu-id="021da-132">[**sohAttributeTypeErrorCodes**](sohattributetype-enum.md)  = [ **<sha-失敗-錯誤-程式碼>**](nap-error-constants.md)</span><span class="sxs-lookup"><span data-stu-id="021da-132">[**sohAttributeTypeErrorCodes**](sohattributetype-enum.md) = [**<sha-failure-error-code>**](nap-error-constants.md)</span></span>

## <a name="requirements"></a><span data-ttu-id="021da-133">規格需求</span><span class="sxs-lookup"><span data-stu-id="021da-133">Requirements</span></span>



| <span data-ttu-id="021da-134">需求</span><span class="sxs-lookup"><span data-stu-id="021da-134">Requirement</span></span> | <span data-ttu-id="021da-135">值</span><span class="sxs-lookup"><span data-stu-id="021da-135">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="021da-136">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="021da-136">Minimum supported client</span></span><br/> | <span data-ttu-id="021da-137">都不支援</span><span class="sxs-lookup"><span data-stu-id="021da-137">None supported</span></span><br/>                                                                               |
| <span data-ttu-id="021da-138">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="021da-138">Minimum supported server</span></span><br/> | <span data-ttu-id="021da-139">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="021da-139">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="021da-140">標頭</span><span class="sxs-lookup"><span data-stu-id="021da-140">Header</span></span><br/>                   | <dl> <span data-ttu-id="021da-141"><dt>NapSystemHealthValidator。h</dt></span><span class="sxs-lookup"><span data-stu-id="021da-141"><dt>NapSystemHealthValidator.h</dt></span></span> </dl>   |
| <span data-ttu-id="021da-142">Idl</span><span class="sxs-lookup"><span data-stu-id="021da-142">IDL</span></span><br/>                      | <dl> <span data-ttu-id="021da-143"><dt>NapSystemHealthValidator .idl</dt></span><span class="sxs-lookup"><span data-stu-id="021da-143"><dt>NapSystemHealthValidator.idl</dt></span></span> </dl> |
| <span data-ttu-id="021da-144">DLL</span><span class="sxs-lookup"><span data-stu-id="021da-144">DLL</span></span><br/>                      | <dl> <span data-ttu-id="021da-145"><dt>Qshvhost.dll</dt></span><span class="sxs-lookup"><span data-stu-id="021da-145"><dt>Qshvhost.dll</dt></span></span> </dl>                 |



## <a name="see-also"></a><span data-ttu-id="021da-146">另請參閱</span><span class="sxs-lookup"><span data-stu-id="021da-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="021da-147">**INapSystemHealthValidationRequest**</span><span class="sxs-lookup"><span data-stu-id="021da-147">**INapSystemHealthValidationRequest**</span></span>](inapsystemhealthvalidationrequest.md)
</dt> </dl>

 

 





