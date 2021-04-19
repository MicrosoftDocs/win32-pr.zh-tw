---
title: 'INapSystemHealthValidationRequest2 介面 (NapSystemHealthValidator .h) '
description: 提供用來支援應用程式開發人員所定義之系統健全狀況驗證程式的方法。
ms.assetid: 12094203-bb6c-4028-9baf-a2a9b124ce6d
keywords:
- INapSystemHealthValidationRequest2 介面 NAP
- INapSystemHealthValidationRequest2 介面 NAP，描述
topic_type:
- apiref
api_name:
- INapSystemHealthValidationRequest2
api_location:
- qshvhost.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 12fdbfc46578a4e64a92accc46f6b910a44dd946
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106966546"
---
# <a name="inapsystemhealthvalidationrequest2-interface"></a><span data-ttu-id="18717-105">INapSystemHealthValidationRequest2 介面</span><span class="sxs-lookup"><span data-stu-id="18717-105">INapSystemHealthValidationRequest2 interface</span></span>

> [!Note]  
> <span data-ttu-id="18717-106">從 Windows 10 開始，無法使用網路存取保護平臺</span><span class="sxs-lookup"><span data-stu-id="18717-106">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="18717-107">**INapSystemHealthValidationRequest2** 介面提供的方法可用來支援應用程式開發人員所定義的系統健全狀況驗證程式。</span><span class="sxs-lookup"><span data-stu-id="18717-107">The **INapSystemHealthValidationRequest2** interface provides methods that are used to support system health validators which are defined by the application developer.</span></span>

> [!Note]  
> <span data-ttu-id="18717-108">此介面會繼承 [**INapSystemHealthValidationRequest**](inapsystemhealthvalidationrequest.md) 的所有方法，因此應該改用。</span><span class="sxs-lookup"><span data-stu-id="18717-108">This interface inherits all the methods of [**INapSystemHealthValidationRequest**](inapsystemhealthvalidationrequest.md) and should be used instead.</span></span>

 

## <a name="members"></a><span data-ttu-id="18717-109">成員</span><span class="sxs-lookup"><span data-stu-id="18717-109">Members</span></span>

<span data-ttu-id="18717-110">**INapSystemHealthValidationRequest2** 介面繼承自 [**INapSystemHealthValidationRequest**](inapsystemhealthvalidationrequest.md)。</span><span class="sxs-lookup"><span data-stu-id="18717-110">The **INapSystemHealthValidationRequest2** interface inherits from [**INapSystemHealthValidationRequest**](inapsystemhealthvalidationrequest.md).</span></span> <span data-ttu-id="18717-111">**INapSystemHealthValidationRequest2** 也有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="18717-111">**INapSystemHealthValidationRequest2** also has these types of members:</span></span>

-   [<span data-ttu-id="18717-112">方法</span><span class="sxs-lookup"><span data-stu-id="18717-112">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="18717-113">方法</span><span class="sxs-lookup"><span data-stu-id="18717-113">Methods</span></span>

<span data-ttu-id="18717-114">**INapSystemHealthValidationRequest2** 介面具有這些方法。</span><span class="sxs-lookup"><span data-stu-id="18717-114">The **INapSystemHealthValidationRequest2** interface has these methods.</span></span>



| <span data-ttu-id="18717-115">方法</span><span class="sxs-lookup"><span data-stu-id="18717-115">Method</span></span>                                                                                                    | <span data-ttu-id="18717-116">描述</span><span class="sxs-lookup"><span data-stu-id="18717-116">Description</span></span>                                                        |
|:----------------------------------------------------------------------------------------------------------|:-------------------------------------------------------------------|
| [<span data-ttu-id="18717-117">**INapSystemHealthValidationRequest2::GetConfigId**</span><span class="sxs-lookup"><span data-stu-id="18717-117">**INapSystemHealthValidationRequest2::GetConfigId**</span></span>](inapsystemhealthvalidationrequest2-getconfigid.md) | <span data-ttu-id="18717-118">捕獲驗證要求中的設定識別碼。</span><span class="sxs-lookup"><span data-stu-id="18717-118">Retrieves the configuration id in a validation request.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="18717-119">備註</span><span class="sxs-lookup"><span data-stu-id="18717-119">Remarks</span></span>

<span data-ttu-id="18717-120">如果 SHV 不支援 [**INapComponentConfig3**](inapcomponentconfig3.md)，則不適用此介面。</span><span class="sxs-lookup"><span data-stu-id="18717-120">If an SHV doesn t support [**INapComponentConfig3**](inapcomponentconfig3.md), this interface doesn t apply.</span></span>

## <a name="requirements"></a><span data-ttu-id="18717-121">規格需求</span><span class="sxs-lookup"><span data-stu-id="18717-121">Requirements</span></span>



| <span data-ttu-id="18717-122">需求</span><span class="sxs-lookup"><span data-stu-id="18717-122">Requirement</span></span> | <span data-ttu-id="18717-123">值</span><span class="sxs-lookup"><span data-stu-id="18717-123">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="18717-124">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="18717-124">Minimum supported client</span></span><br/> | <span data-ttu-id="18717-125">都不支援</span><span class="sxs-lookup"><span data-stu-id="18717-125">None supported</span></span><br/>                                                                               |
| <span data-ttu-id="18717-126">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="18717-126">Minimum supported server</span></span><br/> | <span data-ttu-id="18717-127">僅限 Windows Server 2008 R2 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="18717-127">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="18717-128">標頭</span><span class="sxs-lookup"><span data-stu-id="18717-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="18717-129"><dt>NapSystemHealthValidator。h</dt></span><span class="sxs-lookup"><span data-stu-id="18717-129"><dt>NapSystemHealthValidator.h</dt></span></span> </dl>   |
| <span data-ttu-id="18717-130">Idl</span><span class="sxs-lookup"><span data-stu-id="18717-130">IDL</span></span><br/>                      | <dl> <span data-ttu-id="18717-131"><dt>NapSystemHealthValidator .idl</dt></span><span class="sxs-lookup"><span data-stu-id="18717-131"><dt>NapSystemHealthValidator.idl</dt></span></span> </dl> |
| <span data-ttu-id="18717-132">DLL</span><span class="sxs-lookup"><span data-stu-id="18717-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="18717-133"><dt>Qshvhost.dll</dt></span><span class="sxs-lookup"><span data-stu-id="18717-133"><dt>Qshvhost.dll</dt></span></span> </dl>                 |



## <a name="see-also"></a><span data-ttu-id="18717-134">另請參閱</span><span class="sxs-lookup"><span data-stu-id="18717-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="18717-135">**INapSystemHealthValidationRequest**</span><span class="sxs-lookup"><span data-stu-id="18717-135">**INapSystemHealthValidationRequest**</span></span>](inapsystemhealthvalidationrequest.md)
</dt> <dt>

[<span data-ttu-id="18717-136">NAP 介面</span><span class="sxs-lookup"><span data-stu-id="18717-136">NAP Interfaces</span></span>](nap-interfaces.md)
</dt> <dt>

[<span data-ttu-id="18717-137">NAP 參考</span><span class="sxs-lookup"><span data-stu-id="18717-137">NAP Reference</span></span>](nap-reference.md)
</dt> </dl>

 

 





