---
title: 'INapComponentConfig 介面 (NapCommon .h) '
description: 針對 (Shv) 的系統健全狀況驗證程式提供 NAP 系統組態方法。
ms.assetid: 979b5c34-8efe-4c48-8236-53fbd25d4249
keywords:
- INapComponentConfig 介面 NAP
- INapComponentConfig 介面 NAP，描述
topic_type:
- apiref
api_name:
- INapComponentConfig
api_location:
- NapCommon.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 63a13ae74ba1de79803ff4a2d3716eec7fe934a1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104384390"
---
# <a name="inapcomponentconfig-interface"></a><span data-ttu-id="82af5-105">INapComponentConfig 介面</span><span class="sxs-lookup"><span data-stu-id="82af5-105">INapComponentConfig interface</span></span>

> [!Note]  
> <span data-ttu-id="82af5-106">從 Windows 10 開始，無法使用網路存取保護平臺</span><span class="sxs-lookup"><span data-stu-id="82af5-106">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="82af5-107">**INapComponentConfig** 介面會為 (shv) 的系統健全狀況驗證程式提供 NAP 系統組態方法。</span><span class="sxs-lookup"><span data-stu-id="82af5-107">The **INapComponentConfig** interface provides NAP system configuration methods for system health validators (SHVs).</span></span>

> [!Note]  
> <span data-ttu-id="82af5-108">[**INapComponentConfig2**](inapcomponentconfig2.md) 和 [**INapComponentConfig3**](inapcomponentconfig3.md) 會繼承此介面的所有方法，因此應該改用。</span><span class="sxs-lookup"><span data-stu-id="82af5-108">[**INapComponentConfig2**](inapcomponentconfig2.md) and [**INapComponentConfig3**](inapcomponentconfig3.md) inherit all the methods of this interface and should be used instead.</span></span>

 

## <a name="members"></a><span data-ttu-id="82af5-109">成員</span><span class="sxs-lookup"><span data-stu-id="82af5-109">Members</span></span>

<span data-ttu-id="82af5-110">**INapComponentConfig** 介面繼承自 [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown)介面。</span><span class="sxs-lookup"><span data-stu-id="82af5-110">The **INapComponentConfig** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="82af5-111">**INapComponentConfig** 也有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="82af5-111">**INapComponentConfig** also has these types of members:</span></span>

-   [<span data-ttu-id="82af5-112">方法</span><span class="sxs-lookup"><span data-stu-id="82af5-112">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="82af5-113">方法</span><span class="sxs-lookup"><span data-stu-id="82af5-113">Methods</span></span>

<span data-ttu-id="82af5-114">**INapComponentConfig** 介面具有這些方法。</span><span class="sxs-lookup"><span data-stu-id="82af5-114">The **INapComponentConfig** interface has these methods.</span></span>



| <span data-ttu-id="82af5-115">方法</span><span class="sxs-lookup"><span data-stu-id="82af5-115">Method</span></span>                                                                          | <span data-ttu-id="82af5-116">描述</span><span class="sxs-lookup"><span data-stu-id="82af5-116">Description</span></span>                                                                          |
|:--------------------------------------------------------------------------------|:-------------------------------------------------------------------------------------|
| [<span data-ttu-id="82af5-117">**INapComponentConfig::GetConfig**</span><span class="sxs-lookup"><span data-stu-id="82af5-117">**INapComponentConfig::GetConfig**</span></span>](inapcomponentconfig-getconfig.md)         | <span data-ttu-id="82af5-118">捕獲 SHV 元件設定。</span><span class="sxs-lookup"><span data-stu-id="82af5-118">Retrieves the SHV component configuration.</span></span><br/>                                |
| [<span data-ttu-id="82af5-119">**INapComponentConfig::InvokeUI**</span><span class="sxs-lookup"><span data-stu-id="82af5-119">**INapComponentConfig::InvokeUI**</span></span>](inapcomponentconfig-invokeui.md)           | <span data-ttu-id="82af5-120">啟動 SHV 元件的自訂使用者介面。</span><span class="sxs-lookup"><span data-stu-id="82af5-120">Launches the customized user interface for an SHV component.</span></span><br/>              |
| [<span data-ttu-id="82af5-121">**INapComponentConfig::IsUISupported**</span><span class="sxs-lookup"><span data-stu-id="82af5-121">**INapComponentConfig::IsUISupported**</span></span>](inapcomponentconfig-isuisupported.md) | <span data-ttu-id="82af5-122">指定 SHV 元件是否支援自訂的使用者介面。</span><span class="sxs-lookup"><span data-stu-id="82af5-122">Specifies whether the SHV component supports a customized user interface.</span></span><br/> |
| [<span data-ttu-id="82af5-123">**INapComponentConfig::SetConfig**</span><span class="sxs-lookup"><span data-stu-id="82af5-123">**INapComponentConfig::SetConfig**</span></span>](inapcomponentconfig-setconfig.md)         | <span data-ttu-id="82af5-124">設定 SHV 元件設定。</span><span class="sxs-lookup"><span data-stu-id="82af5-124">Sets the SHV component configuration.</span></span><br/>                                     |



 

## <a name="remarks"></a><span data-ttu-id="82af5-125">備註</span><span class="sxs-lookup"><span data-stu-id="82af5-125">Remarks</span></span>

<span data-ttu-id="82af5-126">系統健康情況代理程式 (Sha) 或隔離強制用戶端 (Qec) 不應執行此介面。</span><span class="sxs-lookup"><span data-stu-id="82af5-126">This interface should not be implemented by system health agents (SHAs) or quarantine enforcement clients (QECs).</span></span>

## <a name="requirements"></a><span data-ttu-id="82af5-127">規格需求</span><span class="sxs-lookup"><span data-stu-id="82af5-127">Requirements</span></span>



| <span data-ttu-id="82af5-128">需求</span><span class="sxs-lookup"><span data-stu-id="82af5-128">Requirement</span></span> | <span data-ttu-id="82af5-129">值</span><span class="sxs-lookup"><span data-stu-id="82af5-129">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="82af5-130">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="82af5-130">Minimum supported client</span></span><br/> | <span data-ttu-id="82af5-131">都不支援</span><span class="sxs-lookup"><span data-stu-id="82af5-131">None supported</span></span><br/>                                                                |
| <span data-ttu-id="82af5-132">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="82af5-132">Minimum supported server</span></span><br/> | <span data-ttu-id="82af5-133">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="82af5-133">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="82af5-134">標頭</span><span class="sxs-lookup"><span data-stu-id="82af5-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="82af5-135"><dt>NapCommon。h</dt></span><span class="sxs-lookup"><span data-stu-id="82af5-135"><dt>NapCommon.h</dt></span></span> </dl>   |
| <span data-ttu-id="82af5-136">Idl</span><span class="sxs-lookup"><span data-stu-id="82af5-136">IDL</span></span><br/>                      | <dl> <span data-ttu-id="82af5-137"><dt>NapCommon .idl</dt></span><span class="sxs-lookup"><span data-stu-id="82af5-137"><dt>NapCommon.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="82af5-138">另請參閱</span><span class="sxs-lookup"><span data-stu-id="82af5-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="82af5-139">NAP 介面</span><span class="sxs-lookup"><span data-stu-id="82af5-139">NAP Interfaces</span></span>](nap-interfaces.md)
</dt> <dt>

[<span data-ttu-id="82af5-140">NAP 參考</span><span class="sxs-lookup"><span data-stu-id="82af5-140">NAP Reference</span></span>](nap-reference.md)
</dt> </dl>

 

