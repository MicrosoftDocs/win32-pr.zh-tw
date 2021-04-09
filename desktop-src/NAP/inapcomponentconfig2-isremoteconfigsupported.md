---
title: 'INapComponentConfig2 IsRemoteConfigSupported 方法 (NapCommon .h) '
description: 是由系統健康狀態驗證 (Shv) 所執行，指出是否支援遠端設定。
ms.assetid: c4b8e60b-ed60-49ec-b4d6-4e1575e4d1a5
keywords:
- IsRemoteConfigSupported 方法 NAP
- IsRemoteConfigSupported 方法 NAP，INapComponentConfig2 介面
- INapComponentConfig2 介面 NAP，IsRemoteConfigSupported 方法
topic_type:
- apiref
api_name:
- INapComponentConfig2.IsRemoteConfigSupported
api_location:
- NapCommon.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a2d144926aafff6f5ad7e243efe2a81a2955f497
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103934171"
---
# <a name="inapcomponentconfig2isremoteconfigsupported-method"></a><span data-ttu-id="287d9-106">INapComponentConfig2：： IsRemoteConfigSupported 方法</span><span class="sxs-lookup"><span data-stu-id="287d9-106">INapComponentConfig2::IsRemoteConfigSupported method</span></span>

> [!Note]  
> <span data-ttu-id="287d9-107">從 Windows 10 開始，無法使用網路存取保護平臺</span><span class="sxs-lookup"><span data-stu-id="287d9-107">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="287d9-108">**IsRemoteConfigSupported** 方法是由系統健康狀態驗證 (shv) 來指出是否支援遠端設定。</span><span class="sxs-lookup"><span data-stu-id="287d9-108">The **IsRemoteConfigSupported** method is implemented by system health validators (SHVs) to indicate whether remote configuration is supported.</span></span>

## <a name="syntax"></a><span data-ttu-id="287d9-109">語法</span><span class="sxs-lookup"><span data-stu-id="287d9-109">Syntax</span></span>


```C++
HRESULT IsRemoteConfigSupported(
  [out] BOOL  *isSupported,
  [out] UINT8 *remoteConfigType
);
```



## <a name="parameters"></a><span data-ttu-id="287d9-110">參數</span><span class="sxs-lookup"><span data-stu-id="287d9-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="287d9-111">*isSupported* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="287d9-111">*isSupported* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="287d9-112">如果元件支援遠端設定，則為布林 **值** 的指標，如果不支援遠端設定，則為 TRUE，否則為 **FALSE** 。</span><span class="sxs-lookup"><span data-stu-id="287d9-112">A pointer to a BOOL that is set to **TRUE** if the component supports remote configuration, and **FALSE** if it does not.</span></span>

</dd> <dt>

<span data-ttu-id="287d9-113">*remoteConfigType* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="287d9-113">*remoteConfigType* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="287d9-114">使用 [**RemoteConfigurationType**](/windows/win32/api/naptypes/ne-naptypes-remoteconfigurationtype) 列舉中的值，指出支援的遠端設定類型：</span><span class="sxs-lookup"><span data-stu-id="287d9-114">Indicates the type of remote configuration supported using value from the [**RemoteConfigurationType**](/windows/win32/api/naptypes/ne-naptypes-remoteconfigurationtype) enumeration:</span></span>



| <span data-ttu-id="287d9-115">值</span><span class="sxs-lookup"><span data-stu-id="287d9-115">Value</span></span>                                                                                                 | <span data-ttu-id="287d9-116">意義</span><span class="sxs-lookup"><span data-stu-id="287d9-116">Meaning</span></span>                                                                                                                                                                                                                                                                                         |
|-------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="287d9-117"><dt>remoteConfigTypeMachine</dt></span><span class="sxs-lookup"><span data-stu-id="287d9-117"><dt>remoteConfigTypeMachine</dt></span></span> </dl>    | <span data-ttu-id="287d9-118">[**InvokeUIForMachine**](inapcomponentconfig2-invokeuiformachine.md) 會實作為。</span><span class="sxs-lookup"><span data-stu-id="287d9-118">[**InvokeUIForMachine**](inapcomponentconfig2-invokeuiformachine.md) is implemented.</span></span><br/>                                                                                                                                                                                                |
| <dl> <span data-ttu-id="287d9-119"><dt>remoteConfigTypeConfigBlob</dt></span><span class="sxs-lookup"><span data-stu-id="287d9-119"><dt>remoteConfigTypeConfigBlob</dt></span></span> </dl> | <span data-ttu-id="287d9-120">[**InvokeUIFromConfigBlob**](inapcomponentconfig2-invokeuifromconfigblob.md) 會實作為。</span><span class="sxs-lookup"><span data-stu-id="287d9-120">[**InvokeUIFromConfigBlob**](inapcomponentconfig2-invokeuifromconfigblob.md) is implemented.</span></span> <span data-ttu-id="287d9-121">您可以使用 DCOM 從遠端呼叫 [**INapComponentConfig：： GetConfig**](inapcomponentconfig-getconfig.md)和 [**INapComponentConfig：： SetConfig**](inapcomponentconfig-setconfig.md) 。</span><span class="sxs-lookup"><span data-stu-id="287d9-121">[**INapComponentConfig::GetConfig**](inapcomponentconfig-getconfig.md) and [**INapComponentConfig::SetConfig**](inapcomponentconfig-setconfig.md) can be called remotely using DCOM.</span></span><br/> |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="287d9-122">傳回值</span><span class="sxs-lookup"><span data-stu-id="287d9-122">Return value</span></span>

<span data-ttu-id="287d9-123">\_如果成功或其中一個標準 Windows 錯誤碼，則會傳回 S OK。</span><span class="sxs-lookup"><span data-stu-id="287d9-123">Returns S\_OK if successful, or one of the standard Windows error codes.</span></span>

## <a name="remarks"></a><span data-ttu-id="287d9-124">備註</span><span class="sxs-lookup"><span data-stu-id="287d9-124">Remarks</span></span>

<span data-ttu-id="287d9-125">如果 [**InvokeUIForMachine**](inapcomponentconfig2-invokeuiformachine.md) 和 [**InvokeUIFromConfigBlob**](inapcomponentconfig2-invokeuifromconfigblob.md) 都未執行，則無法遠端設定 SHV。</span><span class="sxs-lookup"><span data-stu-id="287d9-125">If neither [**InvokeUIForMachine**](inapcomponentconfig2-invokeuiformachine.md) nor [**InvokeUIFromConfigBlob**](inapcomponentconfig2-invokeuifromconfigblob.md) are implemented, remote configuration of the SHV is not possible.</span></span>

## <a name="requirements"></a><span data-ttu-id="287d9-126">規格需求</span><span class="sxs-lookup"><span data-stu-id="287d9-126">Requirements</span></span>



| <span data-ttu-id="287d9-127">需求</span><span class="sxs-lookup"><span data-stu-id="287d9-127">Requirement</span></span> | <span data-ttu-id="287d9-128">值</span><span class="sxs-lookup"><span data-stu-id="287d9-128">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="287d9-129">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="287d9-129">Minimum supported client</span></span><br/> | <span data-ttu-id="287d9-130">都不支援</span><span class="sxs-lookup"><span data-stu-id="287d9-130">None supported</span></span><br/>                                                                |
| <span data-ttu-id="287d9-131">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="287d9-131">Minimum supported server</span></span><br/> | <span data-ttu-id="287d9-132">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="287d9-132">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="287d9-133">標頭</span><span class="sxs-lookup"><span data-stu-id="287d9-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="287d9-134"><dt>NapCommon。h</dt></span><span class="sxs-lookup"><span data-stu-id="287d9-134"><dt>NapCommon.h</dt></span></span> </dl>   |
| <span data-ttu-id="287d9-135">Idl</span><span class="sxs-lookup"><span data-stu-id="287d9-135">IDL</span></span><br/>                      | <dl> <span data-ttu-id="287d9-136"><dt>NapCommon .idl</dt></span><span class="sxs-lookup"><span data-stu-id="287d9-136"><dt>NapCommon.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="287d9-137">另請參閱</span><span class="sxs-lookup"><span data-stu-id="287d9-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="287d9-138">**INapComponentConfig2**</span><span class="sxs-lookup"><span data-stu-id="287d9-138">**INapComponentConfig2**</span></span>](inapcomponentconfig2.md)
</dt> </dl>

 

 





