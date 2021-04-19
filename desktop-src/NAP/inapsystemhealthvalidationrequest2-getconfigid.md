---
title: 'INapSystemHealthValidationRequest2 GetConfigID 方法 (NapSystemHealthValidator .h) '
description: 系統健康狀態驗證 (Shv) 用來在驗證要求中取出設定識別碼。
ms.assetid: 6d5564e4-8386-444b-a859-f0c855e4ee30
keywords:
- GetConfigID 方法 NAP
- GetConfigID 方法 NAP，INapSystemHealthValidationRequest2 介面
- INapSystemHealthValidationRequest2 介面 NAP，GetConfigID 方法
topic_type:
- apiref
api_name:
- INapSystemHealthValidationRequest2.GetConfigID
api_location:
- qshvhost.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0f3b41d2f08dc117fd28e704d607c628ec73e6ac
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106967764"
---
# <a name="inapsystemhealthvalidationrequest2getconfigid-method"></a><span data-ttu-id="c70f8-106">INapSystemHealthValidationRequest2：： GetConfigID 方法</span><span class="sxs-lookup"><span data-stu-id="c70f8-106">INapSystemHealthValidationRequest2::GetConfigID method</span></span>

> [!Note]  
> <span data-ttu-id="c70f8-107">從 Windows 10 開始，無法使用網路存取保護平臺</span><span class="sxs-lookup"><span data-stu-id="c70f8-107">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="c70f8-108">**INapSystemHealthValidationRequest2：： GetConfigId** 方法是由系統健康狀態驗證 (shv) 用來在驗證要求中取出設定識別碼。</span><span class="sxs-lookup"><span data-stu-id="c70f8-108">The **INapSystemHealthValidationRequest2::GetConfigId** method is used by the System Health Validators (SHVs) to retrieve the configuration ID in a validation request.</span></span>

## <a name="syntax"></a><span data-ttu-id="c70f8-109">語法</span><span class="sxs-lookup"><span data-stu-id="c70f8-109">Syntax</span></span>


```C++
HRESULT GetConfigID(
  [out] UINT32 *configID
) const;
```



## <a name="parameters"></a><span data-ttu-id="c70f8-110">參數</span><span class="sxs-lookup"><span data-stu-id="c70f8-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c70f8-111">*configID* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="c70f8-111">*configID* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="c70f8-112">傳回時為 UINT32 的指標，其中包含 SHV 的設定識別碼。</span><span class="sxs-lookup"><span data-stu-id="c70f8-112">On return, a pointer to UINT32 that contains a configuration ID of the SHV.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c70f8-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="c70f8-113">Return value</span></span>

<span data-ttu-id="c70f8-114">根據此操作的結果，傳回下列其中一個錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="c70f8-114">Returns one of the following error codes based on the result of this operation.</span></span>



| <span data-ttu-id="c70f8-115">傳回碼</span><span class="sxs-lookup"><span data-stu-id="c70f8-115">Return code</span></span>                                                                                  | <span data-ttu-id="c70f8-116">Description</span><span class="sxs-lookup"><span data-stu-id="c70f8-116">Description</span></span>                                     |
|----------------------------------------------------------------------------------------------|-------------------------------------------------|
| <dl> <span data-ttu-id="c70f8-117"><dt>**S \_ 確定**</dt></span><span class="sxs-lookup"><span data-stu-id="c70f8-117"><dt>**S\_OK**</dt></span></span> </dl>         | <span data-ttu-id="c70f8-118">作業成功。</span><span class="sxs-lookup"><span data-stu-id="c70f8-118">Operation successful.</span></span><br/>                |
| <dl> <span data-ttu-id="c70f8-119"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="c70f8-119"><dt>**E\_INVALIDARG**</dt></span></span> </dl> | <span data-ttu-id="c70f8-120">ConfigID 參數為 **Null**。</span><span class="sxs-lookup"><span data-stu-id="c70f8-120">The configID parameter was **NULL**.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="c70f8-121">規格需求</span><span class="sxs-lookup"><span data-stu-id="c70f8-121">Requirements</span></span>



| <span data-ttu-id="c70f8-122">需求</span><span class="sxs-lookup"><span data-stu-id="c70f8-122">Requirement</span></span> | <span data-ttu-id="c70f8-123">值</span><span class="sxs-lookup"><span data-stu-id="c70f8-123">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c70f8-124">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="c70f8-124">Minimum supported client</span></span><br/> | <span data-ttu-id="c70f8-125">都不支援</span><span class="sxs-lookup"><span data-stu-id="c70f8-125">None supported</span></span><br/>                                                                               |
| <span data-ttu-id="c70f8-126">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="c70f8-126">Minimum supported server</span></span><br/> | <span data-ttu-id="c70f8-127">僅限 Windows Server 2008 R2 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="c70f8-127">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="c70f8-128">標頭</span><span class="sxs-lookup"><span data-stu-id="c70f8-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="c70f8-129"><dt>NapSystemHealthValidator。h</dt></span><span class="sxs-lookup"><span data-stu-id="c70f8-129"><dt>NapSystemHealthValidator.h</dt></span></span> </dl>   |
| <span data-ttu-id="c70f8-130">Idl</span><span class="sxs-lookup"><span data-stu-id="c70f8-130">IDL</span></span><br/>                      | <dl> <span data-ttu-id="c70f8-131"><dt>NapSystemHealthValidator .idl</dt></span><span class="sxs-lookup"><span data-stu-id="c70f8-131"><dt>NapSystemHealthValidator.idl</dt></span></span> </dl> |
| <span data-ttu-id="c70f8-132">DLL</span><span class="sxs-lookup"><span data-stu-id="c70f8-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c70f8-133"><dt>Qshvhost.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c70f8-133"><dt>Qshvhost.dll</dt></span></span> </dl>                 |



## <a name="see-also"></a><span data-ttu-id="c70f8-134">另請參閱</span><span class="sxs-lookup"><span data-stu-id="c70f8-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c70f8-135">**INapSystemHealthValidationRequest2**</span><span class="sxs-lookup"><span data-stu-id="c70f8-135">**INapSystemHealthValidationRequest2**</span></span>](inapsystemhealthvalidationrequest2.md)
</dt> </dl>

 

 





