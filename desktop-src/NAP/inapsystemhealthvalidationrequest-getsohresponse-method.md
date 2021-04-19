---
title: 'INapSystemHealthValidationRequest GetSoHResponse 方法 (NapSystemHealthValidator .h) '
description: 抓取 SoHResponse。
ms.assetid: 7db9d134-5cd4-4a6c-8576-843b9a920864
keywords:
- GetSoHResponse 方法 NAP
- GetSoHResponse 方法 NAP，INapSystemHealthValidationRequest 介面
- INapSystemHealthValidationRequest 介面 NAP，GetSoHResponse 方法
topic_type:
- apiref
api_name:
- INapSystemHealthValidationRequest.GetSoHResponse
api_location:
- qshvhost.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cc10174edc2bcb9df8e61c98305e42633d2b984b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "107001313"
---
# <a name="inapsystemhealthvalidationrequestgetsohresponse-method"></a><span data-ttu-id="b6b86-106">INapSystemHealthValidationRequest：： GetSoHResponse 方法</span><span class="sxs-lookup"><span data-stu-id="b6b86-106">INapSystemHealthValidationRequest::GetSoHResponse method</span></span>

> [!Note]  
> <span data-ttu-id="b6b86-107">從 Windows 10 開始，無法使用網路存取保護平臺</span><span class="sxs-lookup"><span data-stu-id="b6b86-107">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="b6b86-108">**INapSystemHealthValidationRequest：： GetSoHResponse** 方法會捕獲 [**SoHResponse**](/windows/win32/api/naptypes/ns-naptypes-soh)。</span><span class="sxs-lookup"><span data-stu-id="b6b86-108">The **INapSystemHealthValidationRequest::GetSoHResponse** method retrieves the [**SoHResponse**](/windows/win32/api/naptypes/ns-naptypes-soh).</span></span>

## <a name="syntax"></a><span data-ttu-id="b6b86-109">語法</span><span class="sxs-lookup"><span data-stu-id="b6b86-109">Syntax</span></span>


```C++
HRESULT GetSoHResponse(
  [out] SoHResponse **sohResponse
);
```



## <a name="parameters"></a><span data-ttu-id="b6b86-110">參數</span><span class="sxs-lookup"><span data-stu-id="b6b86-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b6b86-111">*sohResponse* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="b6b86-111">*sohResponse* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="b6b86-112">所接收 [**SoHResponse**](/windows/win32/api/naptypes/ns-naptypes-soh)指標的指標。</span><span class="sxs-lookup"><span data-stu-id="b6b86-112">A pointer to a pointer to the received [**SoHResponse**](/windows/win32/api/naptypes/ns-naptypes-soh).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b6b86-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="b6b86-113">Return value</span></span>

<span data-ttu-id="b6b86-114">也可能傳回其他 COM 特定的錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="b6b86-114">Other COM-specific error codes also may be returned.</span></span>



| <span data-ttu-id="b6b86-115">傳回碼</span><span class="sxs-lookup"><span data-stu-id="b6b86-115">Return code</span></span>                                                                                     | <span data-ttu-id="b6b86-116">Description</span><span class="sxs-lookup"><span data-stu-id="b6b86-116">Description</span></span>                                                        |
|-------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <span data-ttu-id="b6b86-117"><dt>**S \_確定**</dt></span><span class="sxs-lookup"><span data-stu-id="b6b86-117"><dt>**S\_OK** </dt></span></span> </dl>           | <span data-ttu-id="b6b86-118">作業成功。</span><span class="sxs-lookup"><span data-stu-id="b6b86-118">Operation succeeded.</span></span><br/>                                    |
| <dl> <span data-ttu-id="b6b86-119"><dt>**E \_ACCESSDENIED**</dt></span><span class="sxs-lookup"><span data-stu-id="b6b86-119"><dt>**E\_ACCESSDENIED** </dt></span></span> </dl> | <span data-ttu-id="b6b86-120">許可權錯誤，拒絕存取。</span><span class="sxs-lookup"><span data-stu-id="b6b86-120">Permissions error, access denied.</span></span><br/>                       |
| <dl> <span data-ttu-id="b6b86-121"><dt>**E \_OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="b6b86-121"><dt>**E\_OUTOFMEMORY** </dt></span></span> </dl>  | <span data-ttu-id="b6b86-122">系統資源限制，無法執行操作。</span><span class="sxs-lookup"><span data-stu-id="b6b86-122">System resource limit, could not perform the operation.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="b6b86-123">規格需求</span><span class="sxs-lookup"><span data-stu-id="b6b86-123">Requirements</span></span>



| <span data-ttu-id="b6b86-124">需求</span><span class="sxs-lookup"><span data-stu-id="b6b86-124">Requirement</span></span> | <span data-ttu-id="b6b86-125">值</span><span class="sxs-lookup"><span data-stu-id="b6b86-125">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b6b86-126">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="b6b86-126">Minimum supported client</span></span><br/> | <span data-ttu-id="b6b86-127">都不支援</span><span class="sxs-lookup"><span data-stu-id="b6b86-127">None supported</span></span><br/>                                                                               |
| <span data-ttu-id="b6b86-128">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="b6b86-128">Minimum supported server</span></span><br/> | <span data-ttu-id="b6b86-129">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="b6b86-129">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="b6b86-130">標頭</span><span class="sxs-lookup"><span data-stu-id="b6b86-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="b6b86-131"><dt>NapSystemHealthValidator。h</dt></span><span class="sxs-lookup"><span data-stu-id="b6b86-131"><dt>NapSystemHealthValidator.h</dt></span></span> </dl>   |
| <span data-ttu-id="b6b86-132">Idl</span><span class="sxs-lookup"><span data-stu-id="b6b86-132">IDL</span></span><br/>                      | <dl> <span data-ttu-id="b6b86-133"><dt>NapSystemHealthValidator .idl</dt></span><span class="sxs-lookup"><span data-stu-id="b6b86-133"><dt>NapSystemHealthValidator.idl</dt></span></span> </dl> |
| <span data-ttu-id="b6b86-134">DLL</span><span class="sxs-lookup"><span data-stu-id="b6b86-134">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b6b86-135"><dt>Qshvhost.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b6b86-135"><dt>Qshvhost.dll</dt></span></span> </dl>                 |



## <a name="see-also"></a><span data-ttu-id="b6b86-136">另請參閱</span><span class="sxs-lookup"><span data-stu-id="b6b86-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b6b86-137">**INapSystemHealthValidationRequest**</span><span class="sxs-lookup"><span data-stu-id="b6b86-137">**INapSystemHealthValidationRequest**</span></span>](inapsystemhealthvalidationrequest.md)
</dt> </dl>

 

 





