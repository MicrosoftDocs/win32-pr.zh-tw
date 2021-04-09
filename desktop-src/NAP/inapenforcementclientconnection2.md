---
title: 'INapEnforcementClientConnection2 介面 (NapEnforcementClient .h) '
description: '允許用戶端連接管理。 |INapEnforcementClientConnection2 介面 (NapEnforcementClient .h) '
ms.assetid: f7b5d8cc-6a91-4e49-8957-cf67d1001089
keywords:
- INapEnforcementClientConnection2 介面 NAP
- INapEnforcementClientConnection2 介面 NAP，描述
topic_type:
- apiref
api_name:
- INapEnforcementClientConnection2
api_location:
- qagent.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3503e1bf6db01920e814b96e3daf5fe04eabc6b9
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/09/2021
ms.locfileid: "103853627"
---
# <a name="inapenforcementclientconnection2-interface"></a><span data-ttu-id="fc990-106">INapEnforcementClientConnection2 介面</span><span class="sxs-lookup"><span data-stu-id="fc990-106">INapEnforcementClientConnection2 interface</span></span>

> [!Note]  
> <span data-ttu-id="fc990-107">從 Windows 10 開始，無法使用網路存取保護平臺</span><span class="sxs-lookup"><span data-stu-id="fc990-107">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="fc990-108">**INapEnforcementClientConnection2** 提供允許用戶端連接管理的方法。</span><span class="sxs-lookup"><span data-stu-id="fc990-108">The **INapEnforcementClientConnection2** provides methods that allow for client connection management.</span></span>

> [!Note]  
> <span data-ttu-id="fc990-109">此介面會繼承 [**INapEnforcementClientConnection**](inapenforcementclientconnection.md) 的所有方法，因此應該改用。</span><span class="sxs-lookup"><span data-stu-id="fc990-109">This interface inherits all the methods of [**INapEnforcementClientConnection**](inapenforcementclientconnection.md) and should be used instead.</span></span>

 

## <a name="members"></a><span data-ttu-id="fc990-110">成員</span><span class="sxs-lookup"><span data-stu-id="fc990-110">Members</span></span>

<span data-ttu-id="fc990-111">**INapEnforcementClientConnection2** 介面繼承自 [**INapEnforcementClientConnection**](inapenforcementclientconnection.md)。</span><span class="sxs-lookup"><span data-stu-id="fc990-111">The **INapEnforcementClientConnection2** interface inherits from [**INapEnforcementClientConnection**](inapenforcementclientconnection.md).</span></span> <span data-ttu-id="fc990-112">**INapEnforcementClientConnection2** 也有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="fc990-112">**INapEnforcementClientConnection2** also has these types of members:</span></span>

-   [<span data-ttu-id="fc990-113">方法</span><span class="sxs-lookup"><span data-stu-id="fc990-113">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="fc990-114">方法</span><span class="sxs-lookup"><span data-stu-id="fc990-114">Methods</span></span>

<span data-ttu-id="fc990-115">**INapEnforcementClientConnection2** 介面具有這些方法。</span><span class="sxs-lookup"><span data-stu-id="fc990-115">The **INapEnforcementClientConnection2** interface has these methods.</span></span>



| <span data-ttu-id="fc990-116">方法</span><span class="sxs-lookup"><span data-stu-id="fc990-116">Method</span></span>                                                                                                              | <span data-ttu-id="fc990-117">描述</span><span class="sxs-lookup"><span data-stu-id="fc990-117">Description</span></span>                                                                      |
|:--------------------------------------------------------------------------------------------------------------------|:---------------------------------------------------------------------------------|
| [<span data-ttu-id="fc990-118">**INapEnforcementClientConnection2::GetInstalledShvs**</span><span class="sxs-lookup"><span data-stu-id="fc990-118">**INapEnforcementClientConnection2::GetInstalledShvs**</span></span>](inapenforcementclientconnection2-getinstalledshvs.md)     | <span data-ttu-id="fc990-119">用來取得用戶端已安裝之 Shv 的識別碼。</span><span class="sxs-lookup"><span data-stu-id="fc990-119">Used to get the IDs of the installed SHVs for the client.</span></span><br/>             |
| [<span data-ttu-id="fc990-120">**INapEnforcementClientConnection2::GetIsolationInfoEx**</span><span class="sxs-lookup"><span data-stu-id="fc990-120">**INapEnforcementClientConnection2::GetIsolationInfoEx**</span></span>](inapenforcementclientconnection2-getisolationinfoex.md) | <span data-ttu-id="fc990-121">用來取得用戶端的隔離資訊。</span><span class="sxs-lookup"><span data-stu-id="fc990-121">Used to get the isolation information for the client.</span></span><br/>                 |
| [<span data-ttu-id="fc990-122">**INapEnforcementClientConnection2::SetInstalledShvs**</span><span class="sxs-lookup"><span data-stu-id="fc990-122">**INapEnforcementClientConnection2::SetInstalledShvs**</span></span>](inapenforcementclientconnection2-setinstalledshvs.md)     | <span data-ttu-id="fc990-123">供 NapAgent 用來設定用戶端已安裝的 SHV 識別碼。</span><span class="sxs-lookup"><span data-stu-id="fc990-123">Used by the NapAgent to set the installed SHV IDs for the client.</span></span><br/>     |
| [<span data-ttu-id="fc990-124">**INapEnforcementClientConnection2::SetIsolationInfoEx**</span><span class="sxs-lookup"><span data-stu-id="fc990-124">**INapEnforcementClientConnection2::SetIsolationInfoEx**</span></span>](inapenforcementclientconnection2-setisolationinfoex.md) | <span data-ttu-id="fc990-125">供 NapAgent 用來設定用戶端的隔離資訊。</span><span class="sxs-lookup"><span data-stu-id="fc990-125">Used by the NapAgent to set the isolation information for the client.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="fc990-126">規格需求</span><span class="sxs-lookup"><span data-stu-id="fc990-126">Requirements</span></span>



| <span data-ttu-id="fc990-127">需求</span><span class="sxs-lookup"><span data-stu-id="fc990-127">Requirement</span></span> | <span data-ttu-id="fc990-128">值</span><span class="sxs-lookup"><span data-stu-id="fc990-128">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="fc990-129">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="fc990-129">Minimum supported client</span></span><br/> | <span data-ttu-id="fc990-130">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="fc990-130">Windows Vista \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="fc990-131">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="fc990-131">Minimum supported server</span></span><br/> | <span data-ttu-id="fc990-132">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="fc990-132">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="fc990-133">標頭</span><span class="sxs-lookup"><span data-stu-id="fc990-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="fc990-134"><dt>NapEnforcementClient。h</dt></span><span class="sxs-lookup"><span data-stu-id="fc990-134"><dt>NapEnforcementClient.h</dt></span></span> </dl>   |
| <span data-ttu-id="fc990-135">Idl</span><span class="sxs-lookup"><span data-stu-id="fc990-135">IDL</span></span><br/>                      | <dl> <span data-ttu-id="fc990-136"><dt>NapEnforcementClient .idl</dt></span><span class="sxs-lookup"><span data-stu-id="fc990-136"><dt>NapEnforcementClient.idl</dt></span></span> </dl> |
| <span data-ttu-id="fc990-137">DLL</span><span class="sxs-lookup"><span data-stu-id="fc990-137">DLL</span></span><br/>                      | <dl> <span data-ttu-id="fc990-138"><dt>Qagent.dll</dt></span><span class="sxs-lookup"><span data-stu-id="fc990-138"><dt>Qagent.dll</dt></span></span> </dl>               |



## <a name="see-also"></a><span data-ttu-id="fc990-139">另請參閱</span><span class="sxs-lookup"><span data-stu-id="fc990-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fc990-140">**INapEnforcementClientConnection**</span><span class="sxs-lookup"><span data-stu-id="fc990-140">**INapEnforcementClientConnection**</span></span>](inapenforcementclientconnection.md)
</dt> <dt>

[<span data-ttu-id="fc990-141">NAP 介面</span><span class="sxs-lookup"><span data-stu-id="fc990-141">NAP Interfaces</span></span>](nap-interfaces.md)
</dt> <dt>

[<span data-ttu-id="fc990-142">NAP 參考</span><span class="sxs-lookup"><span data-stu-id="fc990-142">NAP Reference</span></span>](nap-reference.md)
</dt> </dl>

 

 





