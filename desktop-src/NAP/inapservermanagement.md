---
title: 'INapServerManagement 介面 (NapServerManagement .h) '
description: 用來管理 NAP 伺服器。
ms.assetid: 5c4f9bf1-fe82-48f5-8aa4-5c73ab01a78a
keywords:
- INapServerManagement 介面 NAP
- INapServerManagement 介面 NAP，描述
topic_type:
- apiref
api_name:
- INapServerManagement
api_location:
- qsvrmgmt.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5a5eed03f535653a3b9244ff1aa74fe499c1bf2f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104104147"
---
# <a name="inapservermanagement-interface"></a><span data-ttu-id="ae5d3-105">INapServerManagement 介面</span><span class="sxs-lookup"><span data-stu-id="ae5d3-105">INapServerManagement interface</span></span>

> [!Note]  
> <span data-ttu-id="ae5d3-106">從 Windows 10 開始，無法使用網路存取保護平臺</span><span class="sxs-lookup"><span data-stu-id="ae5d3-106">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="ae5d3-107">**INapServerManagement** 提供用來管理 NAP 伺服器的方法。</span><span class="sxs-lookup"><span data-stu-id="ae5d3-107">The **INapServerManagement** provides methods that are used to manage the NAP Server.</span></span>

## <a name="members"></a><span data-ttu-id="ae5d3-108">成員</span><span class="sxs-lookup"><span data-stu-id="ae5d3-108">Members</span></span>

<span data-ttu-id="ae5d3-109">**INapServerManagement** 介面繼承自 [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown)介面。</span><span class="sxs-lookup"><span data-stu-id="ae5d3-109">The **INapServerManagement** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="ae5d3-110">**INapServerManagement** 也有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="ae5d3-110">**INapServerManagement** also has these types of members:</span></span>

-   [<span data-ttu-id="ae5d3-111">方法</span><span class="sxs-lookup"><span data-stu-id="ae5d3-111">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="ae5d3-112">方法</span><span class="sxs-lookup"><span data-stu-id="ae5d3-112">Methods</span></span>

<span data-ttu-id="ae5d3-113">**INapServerManagement** 介面具有這些方法。</span><span class="sxs-lookup"><span data-stu-id="ae5d3-113">The **INapServerManagement** interface has these methods.</span></span>



| <span data-ttu-id="ae5d3-114">方法</span><span class="sxs-lookup"><span data-stu-id="ae5d3-114">Method</span></span>                                                                                                                       | <span data-ttu-id="ae5d3-115">描述</span><span class="sxs-lookup"><span data-stu-id="ae5d3-115">Description</span></span>                                          |
|:-----------------------------------------------------------------------------------------------------------------------------|:-----------------------------------------------------|
| [<span data-ttu-id="ae5d3-116">**INapServerManagement::RegisterSystemHealthValidator**</span><span class="sxs-lookup"><span data-stu-id="ae5d3-116">**INapServerManagement::RegisterSystemHealthValidator**</span></span>](inapservermanagement-registersystemhealthvalidator-method.md)     | <span data-ttu-id="ae5d3-117">註冊 SHV。</span><span class="sxs-lookup"><span data-stu-id="ae5d3-117">Registers an SHV.</span></span><br/>                         |
| [<span data-ttu-id="ae5d3-118">**INapServerManagement::SetFailureCategoryMappings**</span><span class="sxs-lookup"><span data-stu-id="ae5d3-118">**INapServerManagement::SetFailureCategoryMappings**</span></span>](inapservermanagement-setfailurecategorymappings-method.md)           | <span data-ttu-id="ae5d3-119">設定 SHV 的失敗類別對應。</span><span class="sxs-lookup"><span data-stu-id="ae5d3-119">Sets the SHV's failure category mappings.</span></span><br/> |
| [<span data-ttu-id="ae5d3-120">**INapServerManagement::UnregisterSystemHealthValidator**</span><span class="sxs-lookup"><span data-stu-id="ae5d3-120">**INapServerManagement::UnregisterSystemHealthValidator**</span></span>](inapservermanagement-unregistersystemhealthvalidator-method.md) | <span data-ttu-id="ae5d3-121">從 NAP 伺服器取消註冊 SHV。</span><span class="sxs-lookup"><span data-stu-id="ae5d3-121">Deregisters an SHV from the NAP server.</span></span><br/>   |



 

## <a name="requirements"></a><span data-ttu-id="ae5d3-122">規格需求</span><span class="sxs-lookup"><span data-stu-id="ae5d3-122">Requirements</span></span>



| <span data-ttu-id="ae5d3-123">需求</span><span class="sxs-lookup"><span data-stu-id="ae5d3-123">Requirement</span></span> | <span data-ttu-id="ae5d3-124">值</span><span class="sxs-lookup"><span data-stu-id="ae5d3-124">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ae5d3-125">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="ae5d3-125">Minimum supported client</span></span><br/> | <span data-ttu-id="ae5d3-126">都不支援</span><span class="sxs-lookup"><span data-stu-id="ae5d3-126">None supported</span></span><br/>                                                                          |
| <span data-ttu-id="ae5d3-127">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="ae5d3-127">Minimum supported server</span></span><br/> | <span data-ttu-id="ae5d3-128">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="ae5d3-128">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="ae5d3-129">標頭</span><span class="sxs-lookup"><span data-stu-id="ae5d3-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="ae5d3-130"><dt>NapServerManagement。h</dt></span><span class="sxs-lookup"><span data-stu-id="ae5d3-130"><dt>NapServerManagement.h</dt></span></span> </dl>   |
| <span data-ttu-id="ae5d3-131">Idl</span><span class="sxs-lookup"><span data-stu-id="ae5d3-131">IDL</span></span><br/>                      | <dl> <span data-ttu-id="ae5d3-132"><dt>NapServerManagement .idl</dt></span><span class="sxs-lookup"><span data-stu-id="ae5d3-132"><dt>NapServerManagement.idl</dt></span></span> </dl> |
| <span data-ttu-id="ae5d3-133">DLL</span><span class="sxs-lookup"><span data-stu-id="ae5d3-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ae5d3-134"><dt>Qsvrmgmt.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ae5d3-134"><dt>Qsvrmgmt.dll</dt></span></span> </dl>            |



## <a name="see-also"></a><span data-ttu-id="ae5d3-135">另請參閱</span><span class="sxs-lookup"><span data-stu-id="ae5d3-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ae5d3-136">NAP 介面</span><span class="sxs-lookup"><span data-stu-id="ae5d3-136">NAP Interfaces</span></span>](nap-interfaces.md)
</dt> <dt>

[<span data-ttu-id="ae5d3-137">NAP 參考</span><span class="sxs-lookup"><span data-stu-id="ae5d3-137">NAP Reference</span></span>](nap-reference.md)
</dt> </dl>

 

