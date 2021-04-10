---
title: 'INapSystemHealthValidationRequest 介面 (NapSystemHealthValidator .h) '
description: 用來支援應用程式開發人員所定義的系統健康狀態驗證。
ms.assetid: faa91ff5-49f5-4aec-81d7-02ec59274f23
keywords:
- INapSystemHealthValidationRequest 介面 NAP
- INapSystemHealthValidationRequest 介面 NAP，描述
topic_type:
- apiref
api_name:
- INapSystemHealthValidationRequest
api_location:
- qshvhost.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cf09f93e00401251a3d0e2296323edeb84ad6007
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103686444"
---
# <a name="inapsystemhealthvalidationrequest-interface"></a><span data-ttu-id="86307-105">INapSystemHealthValidationRequest 介面</span><span class="sxs-lookup"><span data-stu-id="86307-105">INapSystemHealthValidationRequest interface</span></span>

> [!Note]  
> <span data-ttu-id="86307-106">從 Windows 10 開始，無法使用網路存取保護平臺</span><span class="sxs-lookup"><span data-stu-id="86307-106">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="86307-107">**INapSystemHealthValidationRequest** 介面提供的方法可用來支援應用程式開發人員所定義的系統健全狀況驗證程式。</span><span class="sxs-lookup"><span data-stu-id="86307-107">The **INapSystemHealthValidationRequest** interface provides methods that are used to support system health validators which are defined by the application developer.</span></span>

> [!Note]  
> <span data-ttu-id="86307-108">[**INapSystemHealthValidationRequest2**](inapsystemhealthvalidationrequest2.md) 會繼承此介面的所有方法，因此應該改用。</span><span class="sxs-lookup"><span data-stu-id="86307-108">[**INapSystemHealthValidationRequest2**](inapsystemhealthvalidationrequest2.md) inherits all the methods of this interface and should be used instead.</span></span>

 

## <a name="members"></a><span data-ttu-id="86307-109">成員</span><span class="sxs-lookup"><span data-stu-id="86307-109">Members</span></span>

<span data-ttu-id="86307-110">**INapSystemHealthValidationRequest** 介面繼承自 [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown)介面。</span><span class="sxs-lookup"><span data-stu-id="86307-110">The **INapSystemHealthValidationRequest** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="86307-111">**INapSystemHealthValidationRequest** 也有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="86307-111">**INapSystemHealthValidationRequest** also has these types of members:</span></span>

-   [<span data-ttu-id="86307-112">方法</span><span class="sxs-lookup"><span data-stu-id="86307-112">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="86307-113">方法</span><span class="sxs-lookup"><span data-stu-id="86307-113">Methods</span></span>

<span data-ttu-id="86307-114">**INapSystemHealthValidationRequest** 介面具有這些方法。</span><span class="sxs-lookup"><span data-stu-id="86307-114">The **INapSystemHealthValidationRequest** interface has these methods.</span></span>



| <span data-ttu-id="86307-115">方法</span><span class="sxs-lookup"><span data-stu-id="86307-115">Method</span></span>                                                                                                                               | <span data-ttu-id="86307-116">描述</span><span class="sxs-lookup"><span data-stu-id="86307-116">Description</span></span>                                                                                                           |
|:-------------------------------------------------------------------------------------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="86307-117">**INapSystemHealthValidationRequest::GetCorrelationId**</span><span class="sxs-lookup"><span data-stu-id="86307-117">**INapSystemHealthValidationRequest::GetCorrelationId**</span></span>](inapsystemhealthvalidationrequest-getcorrelationid-method.md)             | <span data-ttu-id="86307-118">由驗證程式用來取出相互關聯識別碼。</span><span class="sxs-lookup"><span data-stu-id="86307-118">Used by validators to retrieve the correlation ID.</span></span> <span data-ttu-id="86307-119">然後，驗證程式必須記錄這些資訊。</span><span class="sxs-lookup"><span data-stu-id="86307-119">The validator must then log this information.</span></span><br/>           |
| [<span data-ttu-id="86307-120">**INapSystemHealthValidationRequest::GetMachineName**</span><span class="sxs-lookup"><span data-stu-id="86307-120">**INapSystemHealthValidationRequest::GetMachineName**</span></span>](inapsystemhealthvalidationrequest-getmachinename-method.md)                 | <span data-ttu-id="86307-121">由驗證程式用來取得電腦名稱稱。</span><span class="sxs-lookup"><span data-stu-id="86307-121">Used by validators to retrieve the machine name.</span></span> <span data-ttu-id="86307-122">然後，驗證程式必須記錄這些資訊。</span><span class="sxs-lookup"><span data-stu-id="86307-122">The validator must then log this information.</span></span><br/>             |
| [<span data-ttu-id="86307-123">**INapSystemHealthValidationRequest::GetPrivateData**</span><span class="sxs-lookup"><span data-stu-id="86307-123">**INapSystemHealthValidationRequest::GetPrivateData**</span></span>](inapsystemhealthvalidationrequest-getprivatedata-method.md)                 | <span data-ttu-id="86307-124">允許 NapServer 捕獲狀態資訊。</span><span class="sxs-lookup"><span data-stu-id="86307-124">Allows the NapServer to retrieve state information.</span></span><br/>                                                        |
| [<span data-ttu-id="86307-125">**INapSystemHealthValidationRequest::GetSoHRequest**</span><span class="sxs-lookup"><span data-stu-id="86307-125">**INapSystemHealthValidationRequest::GetSoHRequest**</span></span>](inapsystemhealthvalidationrequest-getsohrequest-method.md)                   | <span data-ttu-id="86307-126">允許驗證程式取出並驗證 SoHRequest 資訊。</span><span class="sxs-lookup"><span data-stu-id="86307-126">Allows Validators to retrieve and validate the SoHRequest information.</span></span><br/>                                     |
| [<span data-ttu-id="86307-127">**INapSystemHealthValidationRequest::GetSoHResponse**</span><span class="sxs-lookup"><span data-stu-id="86307-127">**INapSystemHealthValidationRequest::GetSoHResponse**</span></span>](inapsystemhealthvalidationrequest-getsohresponse-method.md)                 | <span data-ttu-id="86307-128">取得 SoHResponse 物件。</span><span class="sxs-lookup"><span data-stu-id="86307-128">Gets the SoHResponse object.</span></span><br/>                                                                               |
| [<span data-ttu-id="86307-129">**INapSystemHealthValidationRequest::GetStringCorrelationId**</span><span class="sxs-lookup"><span data-stu-id="86307-129">**INapSystemHealthValidationRequest::GetStringCorrelationId**</span></span>](inapsystemhealthvalidationrequest-getstringcorrelationid-method.md) | <span data-ttu-id="86307-130">由驗證程式用來取出唯一的交換識別碼。</span><span class="sxs-lookup"><span data-stu-id="86307-130">Used by validators to retrieve a unique exchange identifier.</span></span> <span data-ttu-id="86307-131">然後，驗證程式必須記錄這些資訊。</span><span class="sxs-lookup"><span data-stu-id="86307-131">The validator must then log this information.</span></span><br/> |
| [<span data-ttu-id="86307-132">**INapSystemHealthValidationRequest::SetPrivateData**</span><span class="sxs-lookup"><span data-stu-id="86307-132">**INapSystemHealthValidationRequest::SetPrivateData**</span></span>](inapsystemhealthvalidationrequest-setprivatedata-method.md)                 | <span data-ttu-id="86307-133">允許 NapServer 儲存狀態資訊。</span><span class="sxs-lookup"><span data-stu-id="86307-133">Allows the NapServer to store state information.</span></span><br/>                                                           |
| [<span data-ttu-id="86307-134">**INapSystemHealthValidationRequest::SetSoHResponse**</span><span class="sxs-lookup"><span data-stu-id="86307-134">**INapSystemHealthValidationRequest::SetSoHResponse**</span></span>](inapsystemhealthvalidationrequest-setsohresponse-method.md)                 | <span data-ttu-id="86307-135">允許驗證程式設定 SoHResponse。</span><span class="sxs-lookup"><span data-stu-id="86307-135">Allows validators to set the SoHResponse.</span></span><br/>                                                                  |



 

## <a name="requirements"></a><span data-ttu-id="86307-136">規格需求</span><span class="sxs-lookup"><span data-stu-id="86307-136">Requirements</span></span>



| <span data-ttu-id="86307-137">需求</span><span class="sxs-lookup"><span data-stu-id="86307-137">Requirement</span></span> | <span data-ttu-id="86307-138">值</span><span class="sxs-lookup"><span data-stu-id="86307-138">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="86307-139">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="86307-139">Minimum supported client</span></span><br/> | <span data-ttu-id="86307-140">都不支援</span><span class="sxs-lookup"><span data-stu-id="86307-140">None supported</span></span><br/>                                                                               |
| <span data-ttu-id="86307-141">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="86307-141">Minimum supported server</span></span><br/> | <span data-ttu-id="86307-142">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="86307-142">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="86307-143">標頭</span><span class="sxs-lookup"><span data-stu-id="86307-143">Header</span></span><br/>                   | <dl> <span data-ttu-id="86307-144"><dt>NapSystemHealthValidator。h</dt></span><span class="sxs-lookup"><span data-stu-id="86307-144"><dt>NapSystemHealthValidator.h</dt></span></span> </dl>   |
| <span data-ttu-id="86307-145">Idl</span><span class="sxs-lookup"><span data-stu-id="86307-145">IDL</span></span><br/>                      | <dl> <span data-ttu-id="86307-146"><dt>NapSystemHealthValidator .idl</dt></span><span class="sxs-lookup"><span data-stu-id="86307-146"><dt>NapSystemHealthValidator.idl</dt></span></span> </dl> |
| <span data-ttu-id="86307-147">DLL</span><span class="sxs-lookup"><span data-stu-id="86307-147">DLL</span></span><br/>                      | <dl> <span data-ttu-id="86307-148"><dt>Qshvhost.dll</dt></span><span class="sxs-lookup"><span data-stu-id="86307-148"><dt>Qshvhost.dll</dt></span></span> </dl>                 |



## <a name="see-also"></a><span data-ttu-id="86307-149">另請參閱</span><span class="sxs-lookup"><span data-stu-id="86307-149">See also</span></span>

<dl> <dt>

[<span data-ttu-id="86307-150">NAP 介面</span><span class="sxs-lookup"><span data-stu-id="86307-150">NAP Interfaces</span></span>](nap-interfaces.md)
</dt> <dt>

[<span data-ttu-id="86307-151">NAP 參考</span><span class="sxs-lookup"><span data-stu-id="86307-151">NAP Reference</span></span>](nap-reference.md)
</dt> </dl>

 

