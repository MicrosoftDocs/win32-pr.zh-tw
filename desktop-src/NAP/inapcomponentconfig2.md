---
title: 'INapComponentConfig2 介面 (NapCommon .h) '
description: 提供適用于系統健全狀況驗證程式的 NAP 系統組態方法 (Shv) 從遠端設定 NPS) 使用者介面的網路原則 (伺服器。
ms.assetid: 35150184-300c-4ea4-bff9-b3c33fa3156b
keywords:
- INapComponentConfig2 介面 NAP
- INapComponentConfig2 介面 NAP，描述
topic_type:
- apiref
api_name:
- INapComponentConfig2
api_location:
- NapCommon.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 29bd6fbea7696d0e4d5eacefd028ce7d33e549e0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106965708"
---
# <a name="inapcomponentconfig2-interface"></a><span data-ttu-id="6727c-105">INapComponentConfig2 介面</span><span class="sxs-lookup"><span data-stu-id="6727c-105">INapComponentConfig2 interface</span></span>

> [!Note]  
> <span data-ttu-id="6727c-106">從 Windows 10 開始，無法使用網路存取保護平臺</span><span class="sxs-lookup"><span data-stu-id="6727c-106">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="6727c-107">**INapComponentConfig2** 介面會為系統健康狀態驗證 (SHV 提供 NAP 系統組態方法，) 在遠端 (NPS) 使用者介面設定網路原則伺服器。</span><span class="sxs-lookup"><span data-stu-id="6727c-107">The **INapComponentConfig2** interface provides NAP system configuration methods for system health validators (SHVs) to configure a network policy server (NPS) user interface remotely.</span></span>

> [!Note]  
> <span data-ttu-id="6727c-108">此介面會繼承 [**INapComponentConfig**](inapcomponentconfig.md) 的所有方法，因此應該改用。</span><span class="sxs-lookup"><span data-stu-id="6727c-108">This interface inherits all the methods of [**INapComponentConfig**](inapcomponentconfig.md) and should be used instead.</span></span>

 

## <a name="members"></a><span data-ttu-id="6727c-109">成員</span><span class="sxs-lookup"><span data-stu-id="6727c-109">Members</span></span>

<span data-ttu-id="6727c-110">**INapComponentConfig2** 介面繼承自 [**INapComponentConfig**](inapcomponentconfig.md)。</span><span class="sxs-lookup"><span data-stu-id="6727c-110">The **INapComponentConfig2** interface inherits from [**INapComponentConfig**](inapcomponentconfig.md).</span></span> <span data-ttu-id="6727c-111">**INapComponentConfig2** 也有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="6727c-111">**INapComponentConfig2** also has these types of members:</span></span>

-   [<span data-ttu-id="6727c-112">方法</span><span class="sxs-lookup"><span data-stu-id="6727c-112">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="6727c-113">方法</span><span class="sxs-lookup"><span data-stu-id="6727c-113">Methods</span></span>

<span data-ttu-id="6727c-114">**INapComponentConfig2** 介面具有這些方法。</span><span class="sxs-lookup"><span data-stu-id="6727c-114">The **INapComponentConfig2** interface has these methods.</span></span>



| <span data-ttu-id="6727c-115">方法</span><span class="sxs-lookup"><span data-stu-id="6727c-115">Method</span></span>                                                                                                | <span data-ttu-id="6727c-116">描述</span><span class="sxs-lookup"><span data-stu-id="6727c-116">Description</span></span>                                                                                                                                                                |
|:------------------------------------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="6727c-117">**INapComponentConfig2::InvokeUIForMachine**</span><span class="sxs-lookup"><span data-stu-id="6727c-117">**INapComponentConfig2::InvokeUIForMachine**</span></span>](inapcomponentconfig2-invokeuiformachine.md)           | <span data-ttu-id="6727c-118">視需要由 Shv 所執行，以直接在指定的電腦上管理遠端設定。</span><span class="sxs-lookup"><span data-stu-id="6727c-118">Implemented by SHVs as needed to manage remote configuration directly on the machine specified.</span></span><br/>                                                                 |
| [<span data-ttu-id="6727c-119">**INapComponentConfig2::InvokeUIFromConfigBlob**</span><span class="sxs-lookup"><span data-stu-id="6727c-119">**INapComponentConfig2::InvokeUIFromConfigBlob**</span></span>](inapcomponentconfig2-invokeuifromconfigblob.md)   | <span data-ttu-id="6727c-120">視需要由 Shv 所執行，以在記憶體中載入遠端電腦的設定，並顯示允許操作設定資料的 UI。</span><span class="sxs-lookup"><span data-stu-id="6727c-120">Implemented by SHVs as needed to load the configuration of the remote machine in memory and to display a UI that allows manipulation of the configuration data.</span></span><br/> |
| [<span data-ttu-id="6727c-121">**INapComponentConfig2::IsRemoteConfigSupported**</span><span class="sxs-lookup"><span data-stu-id="6727c-121">**INapComponentConfig2::IsRemoteConfigSupported**</span></span>](inapcomponentconfig2-isremoteconfigsupported.md) | <span data-ttu-id="6727c-122">由 Shv 執行以指出是否支援遠端設定。</span><span class="sxs-lookup"><span data-stu-id="6727c-122">Implemented by SHVs to indicate whether remote configuration is supported.</span></span><br/>                                                                                      |



 

## <a name="remarks"></a><span data-ttu-id="6727c-123">備註</span><span class="sxs-lookup"><span data-stu-id="6727c-123">Remarks</span></span>

<span data-ttu-id="6727c-124">系統健康情況代理程式 (Sha) 或隔離強制用戶端 (Qec) 不應執行此介面。</span><span class="sxs-lookup"><span data-stu-id="6727c-124">This interface should not be implemented by system health agents (SHAs) or quarantine enforcement clients (QECs).</span></span>

## <a name="requirements"></a><span data-ttu-id="6727c-125">規格需求</span><span class="sxs-lookup"><span data-stu-id="6727c-125">Requirements</span></span>



| <span data-ttu-id="6727c-126">需求</span><span class="sxs-lookup"><span data-stu-id="6727c-126">Requirement</span></span> | <span data-ttu-id="6727c-127">值</span><span class="sxs-lookup"><span data-stu-id="6727c-127">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="6727c-128">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="6727c-128">Minimum supported client</span></span><br/> | <span data-ttu-id="6727c-129">都不支援</span><span class="sxs-lookup"><span data-stu-id="6727c-129">None supported</span></span><br/>                                                                |
| <span data-ttu-id="6727c-130">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="6727c-130">Minimum supported server</span></span><br/> | <span data-ttu-id="6727c-131">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="6727c-131">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="6727c-132">標頭</span><span class="sxs-lookup"><span data-stu-id="6727c-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="6727c-133"><dt>NapCommon。h</dt></span><span class="sxs-lookup"><span data-stu-id="6727c-133"><dt>NapCommon.h</dt></span></span> </dl>   |
| <span data-ttu-id="6727c-134">Idl</span><span class="sxs-lookup"><span data-stu-id="6727c-134">IDL</span></span><br/>                      | <dl> <span data-ttu-id="6727c-135"><dt>NapCommon .idl</dt></span><span class="sxs-lookup"><span data-stu-id="6727c-135"><dt>NapCommon.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6727c-136">另請參閱</span><span class="sxs-lookup"><span data-stu-id="6727c-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6727c-137">**INapComponentConfig**</span><span class="sxs-lookup"><span data-stu-id="6727c-137">**INapComponentConfig**</span></span>](inapcomponentconfig.md)
</dt> <dt>

[<span data-ttu-id="6727c-138">NAP 介面</span><span class="sxs-lookup"><span data-stu-id="6727c-138">NAP Interfaces</span></span>](nap-interfaces.md)
</dt> <dt>

[<span data-ttu-id="6727c-139">NAP 參考</span><span class="sxs-lookup"><span data-stu-id="6727c-139">NAP Reference</span></span>](nap-reference.md)
</dt> </dl>

 

 





