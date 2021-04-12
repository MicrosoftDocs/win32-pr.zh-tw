---
title: 'INapClientManagement 介面 (NapManagement .h) '
description: '提供 NAP 用戶端管理的方法。 |INapClientManagement 介面 (NapManagement .h) '
ms.assetid: 9c5724db-1e85-4da5-92b7-9ff6579f9cfb
keywords:
- INapClientManagement 介面 NAP
- INapClientManagement 介面 NAP，描述
topic_type:
- apiref
api_name:
- INapClientManagement
api_location:
- qagent.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fe90158d6f1e9a864f7d19448a412d70890133d2
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/09/2021
ms.locfileid: "103945942"
---
# <a name="inapclientmanagement-interface"></a><span data-ttu-id="26d8e-106">INapClientManagement 介面</span><span class="sxs-lookup"><span data-stu-id="26d8e-106">INapClientManagement interface</span></span>

> [!Note]  
> <span data-ttu-id="26d8e-107">從 Windows 10 開始，無法使用網路存取保護平臺</span><span class="sxs-lookup"><span data-stu-id="26d8e-107">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="26d8e-108">**INapClientManagement** 介面提供 NAP 用戶端管理的方法。</span><span class="sxs-lookup"><span data-stu-id="26d8e-108">The **INapClientManagement** interface provides methods for NAP client management.</span></span>

> [!Note]  
> <span data-ttu-id="26d8e-109">[**INapClientManagement2**](inapclientmanagement2.md) 會繼承此介面的所有方法，因此應該改用。</span><span class="sxs-lookup"><span data-stu-id="26d8e-109">[**INapClientManagement2**](inapclientmanagement2.md) inherits all the methods of this interface and should be used instead.</span></span>

 

## <a name="members"></a><span data-ttu-id="26d8e-110">成員</span><span class="sxs-lookup"><span data-stu-id="26d8e-110">Members</span></span>

<span data-ttu-id="26d8e-111">**INapClientManagement** 介面繼承自 [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown)介面。</span><span class="sxs-lookup"><span data-stu-id="26d8e-111">The **INapClientManagement** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="26d8e-112">**INapClientManagement** 也有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="26d8e-112">**INapClientManagement** also has these types of members:</span></span>

-   [<span data-ttu-id="26d8e-113">方法</span><span class="sxs-lookup"><span data-stu-id="26d8e-113">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="26d8e-114">方法</span><span class="sxs-lookup"><span data-stu-id="26d8e-114">Methods</span></span>

<span data-ttu-id="26d8e-115">**INapClientManagement** 介面具有這些方法。</span><span class="sxs-lookup"><span data-stu-id="26d8e-115">The **INapClientManagement** interface has these methods.</span></span>



| <span data-ttu-id="26d8e-116">方法</span><span class="sxs-lookup"><span data-stu-id="26d8e-116">Method</span></span>                                                                                                                | <span data-ttu-id="26d8e-117">描述</span><span class="sxs-lookup"><span data-stu-id="26d8e-117">Description</span></span>                                                                   |
|:----------------------------------------------------------------------------------------------------------------------|:------------------------------------------------------------------------------|
| [<span data-ttu-id="26d8e-118">**INapClientManagement::GetNapClientInfo**</span><span class="sxs-lookup"><span data-stu-id="26d8e-118">**INapClientManagement::GetNapClientInfo**</span></span>](inapclientmanagement-getnapclientinfo.md)                               | <span data-ttu-id="26d8e-119">抓取 NAP 用戶端的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="26d8e-119">Retrieves information about a NAP client.</span></span><br/>                          |
| [<span data-ttu-id="26d8e-120">**INapClientManagement::GetRegisteredEnforcementClients**</span><span class="sxs-lookup"><span data-stu-id="26d8e-120">**INapClientManagement::GetRegisteredEnforcementClients**</span></span>](inapclientmanagement-getregisteredenforcementclients.md) | <span data-ttu-id="26d8e-121">抓取已註冊的強制用戶端的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="26d8e-121">Retrieves information about the registered enforcement clients.</span></span><br/>    |
| [<span data-ttu-id="26d8e-122">**INapClientManagement::GetRegisteredSystemHealthAgents**</span><span class="sxs-lookup"><span data-stu-id="26d8e-122">**INapClientManagement::GetRegisteredSystemHealthAgents**</span></span>](inapclientmanagement-getregisteredsystemhealthagents.md) | <span data-ttu-id="26d8e-123">取得已註冊之 SHA 的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="26d8e-123">Retrieve information about a registered SHA.</span></span><br/>                       |
| [<span data-ttu-id="26d8e-124">**INapClientManagement::GetSystemIsolationInfo**</span><span class="sxs-lookup"><span data-stu-id="26d8e-124">**INapClientManagement::GetSystemIsolationInfo**</span></span>](inapclientmanagement-getsystemisolationinfo.md)                   | <span data-ttu-id="26d8e-125">抓取 Nap 用戶端隔離狀態的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="26d8e-125">Retrieves information about the isolation state of the Nap client.</span></span><br/> |
| [<span data-ttu-id="26d8e-126">**INapClientManagement::RegisterEnforcementClient**</span><span class="sxs-lookup"><span data-stu-id="26d8e-126">**INapClientManagement::RegisterEnforcementClient**</span></span>](inapclientmanagement-registerenforcementclient.md)             | <span data-ttu-id="26d8e-127">向 NAP 系統註冊強制用戶端。</span><span class="sxs-lookup"><span data-stu-id="26d8e-127">Registers an enforcement client with the NAP system.</span></span><br/>               |
| [<span data-ttu-id="26d8e-128">**INapClientManagement::RegisterSystemHealthAgent**</span><span class="sxs-lookup"><span data-stu-id="26d8e-128">**INapClientManagement::RegisterSystemHealthAgent**</span></span>](inapclientmanagement-registersystemhealthagent.md)             | <span data-ttu-id="26d8e-129">向 NAP 系統註冊 SHA。</span><span class="sxs-lookup"><span data-stu-id="26d8e-129">Registers an SHA with the NAP system.</span></span><br/>                              |
| [<span data-ttu-id="26d8e-130">**INapClientManagement::UnregisterEnforcementClient**</span><span class="sxs-lookup"><span data-stu-id="26d8e-130">**INapClientManagement::UnregisterEnforcementClient**</span></span>](inapclientmanagement-unregisterenforcementclient.md)         | <span data-ttu-id="26d8e-131">使用 NAP 系統取消註冊強制用戶端。</span><span class="sxs-lookup"><span data-stu-id="26d8e-131">Unregisters an enforcement client with the NAP system.</span></span><br/>             |
| [<span data-ttu-id="26d8e-132">**INapClientManagement::UnregisterSystemHealthAgent**</span><span class="sxs-lookup"><span data-stu-id="26d8e-132">**INapClientManagement::UnregisterSystemHealthAgent**</span></span>](inapclientmanagement-unregistersystemhealthagent.md)         | <span data-ttu-id="26d8e-133">向 NAP 系統取消註冊 SHA。</span><span class="sxs-lookup"><span data-stu-id="26d8e-133">Unregisters an SHA with the NAP system.</span></span><br/>                            |



 

## <a name="requirements"></a><span data-ttu-id="26d8e-134">規格需求</span><span class="sxs-lookup"><span data-stu-id="26d8e-134">Requirements</span></span>



| <span data-ttu-id="26d8e-135">需求</span><span class="sxs-lookup"><span data-stu-id="26d8e-135">Requirement</span></span> | <span data-ttu-id="26d8e-136">值</span><span class="sxs-lookup"><span data-stu-id="26d8e-136">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------|
| <span data-ttu-id="26d8e-137">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="26d8e-137">Minimum supported client</span></span><br/> | <span data-ttu-id="26d8e-138">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="26d8e-138">Windows Vista \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="26d8e-139">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="26d8e-139">Minimum supported server</span></span><br/> | <span data-ttu-id="26d8e-140">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="26d8e-140">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="26d8e-141">標頭</span><span class="sxs-lookup"><span data-stu-id="26d8e-141">Header</span></span><br/>                   | <dl> <span data-ttu-id="26d8e-142"><dt>NapManagement。h</dt></span><span class="sxs-lookup"><span data-stu-id="26d8e-142"><dt>NapManagement.h</dt></span></span> </dl>   |
| <span data-ttu-id="26d8e-143">Idl</span><span class="sxs-lookup"><span data-stu-id="26d8e-143">IDL</span></span><br/>                      | <dl> <span data-ttu-id="26d8e-144"><dt>NapManagement .idl</dt></span><span class="sxs-lookup"><span data-stu-id="26d8e-144"><dt>NapManagement.idl</dt></span></span> </dl> |
| <span data-ttu-id="26d8e-145">DLL</span><span class="sxs-lookup"><span data-stu-id="26d8e-145">DLL</span></span><br/>                      | <dl> <span data-ttu-id="26d8e-146"><dt>Qagent.dll</dt></span><span class="sxs-lookup"><span data-stu-id="26d8e-146"><dt>Qagent.dll</dt></span></span> </dl>        |



## <a name="see-also"></a><span data-ttu-id="26d8e-147">另請參閱</span><span class="sxs-lookup"><span data-stu-id="26d8e-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="26d8e-148">NAP 介面</span><span class="sxs-lookup"><span data-stu-id="26d8e-148">NAP Interfaces</span></span>](nap-interfaces.md)
</dt> <dt>

[<span data-ttu-id="26d8e-149">NAP 參考</span><span class="sxs-lookup"><span data-stu-id="26d8e-149">NAP Reference</span></span>](nap-reference.md)
</dt> </dl>

 

