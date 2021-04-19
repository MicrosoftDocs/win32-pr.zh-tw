---
title: 'INapServerInfo 介面 (NapServerManagement .h) '
description: 管理用戶端 (例如 WMI 提供者或命令列工具，) 用來查詢 NAP 伺服器系統的狀態。
ms.assetid: 3c6d3f76-ea63-4cb2-bac7-e5668e50b7a7
keywords:
- INapServerInfo 介面 NAP
- INapServerInfo 介面 NAP，描述
topic_type:
- apiref
api_name:
- INapServerInfo
api_location:
- qsvrmgmt.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ec17e3303fe4af4d359279de6c5fa7aa5f34d409
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106968356"
---
# <a name="inapserverinfo-interface"></a><span data-ttu-id="f5d54-105">INapServerInfo 介面</span><span class="sxs-lookup"><span data-stu-id="f5d54-105">INapServerInfo interface</span></span>

> [!Note]  
> <span data-ttu-id="f5d54-106">從 Windows 10 開始，無法使用網路存取保護平臺</span><span class="sxs-lookup"><span data-stu-id="f5d54-106">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="f5d54-107">**INapServerInfo** 提供管理用戶端 (的方法，例如 WMI 提供者或命令列工具，) 用來查詢 NAP 伺服器系統的狀態。</span><span class="sxs-lookup"><span data-stu-id="f5d54-107">The **INapServerInfo** provides methods that Management clients (for example, WMI providers or command-line tools) use to query the status of the NAP server system.</span></span>

## <a name="members"></a><span data-ttu-id="f5d54-108">成員</span><span class="sxs-lookup"><span data-stu-id="f5d54-108">Members</span></span>

<span data-ttu-id="f5d54-109">**INapServerInfo** 介面繼承自 [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown)介面。</span><span class="sxs-lookup"><span data-stu-id="f5d54-109">The **INapServerInfo** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="f5d54-110">**INapServerInfo** 也有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="f5d54-110">**INapServerInfo** also has these types of members:</span></span>

-   [<span data-ttu-id="f5d54-111">方法</span><span class="sxs-lookup"><span data-stu-id="f5d54-111">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="f5d54-112">方法</span><span class="sxs-lookup"><span data-stu-id="f5d54-112">Methods</span></span>

<span data-ttu-id="f5d54-113">**INapServerInfo** 介面具有這些方法。</span><span class="sxs-lookup"><span data-stu-id="f5d54-113">The **INapServerInfo** interface has these methods.</span></span>



| <span data-ttu-id="f5d54-114">方法</span><span class="sxs-lookup"><span data-stu-id="f5d54-114">Method</span></span>                                                                                                                   | <span data-ttu-id="f5d54-115">描述</span><span class="sxs-lookup"><span data-stu-id="f5d54-115">Description</span></span>                                                             |
|:-------------------------------------------------------------------------------------------------------------------------|:------------------------------------------------------------------------|
| [<span data-ttu-id="f5d54-116">**INapServerInfo::GetFailureCategoryMappings**</span><span class="sxs-lookup"><span data-stu-id="f5d54-116">**INapServerInfo::GetFailureCategoryMappings**</span></span>](inapserverinfo-getfailurecategorymappings-method.md)                   | <span data-ttu-id="f5d54-117">抓取指定 SHV 的失敗類別對應。</span><span class="sxs-lookup"><span data-stu-id="f5d54-117">Retrieves the failure category mappings for a specified SHV.</span></span><br/> |
| [<span data-ttu-id="f5d54-118">**INapServerInfo::GetNapServerInfo**</span><span class="sxs-lookup"><span data-stu-id="f5d54-118">**INapServerInfo::GetNapServerInfo**</span></span>](inapserverinfo-getnapserverinfo-method.md)                                       | <span data-ttu-id="f5d54-119">抓取 NAP 伺服器的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="f5d54-119">Retrieves information about the NAP server.</span></span><br/>                  |
| [<span data-ttu-id="f5d54-120">**INapServerInfo::GetRegisteredSystemHealthValidators**</span><span class="sxs-lookup"><span data-stu-id="f5d54-120">**INapServerInfo::GetRegisteredSystemHealthValidators**</span></span>](inapserverinfo-getregisteredsystemhealthvalidators-method.md) | <span data-ttu-id="f5d54-121">抓取已註冊的 Shv 清單。</span><span class="sxs-lookup"><span data-stu-id="f5d54-121">Retrieves a list of registered SHVs.</span></span><br/>                         |



 

## <a name="remarks"></a><span data-ttu-id="f5d54-122">備註</span><span class="sxs-lookup"><span data-stu-id="f5d54-122">Remarks</span></span>

<span data-ttu-id="f5d54-123">這些方法只提供有關系統上 NAP 伺服器及其元件的靜態資訊。</span><span class="sxs-lookup"><span data-stu-id="f5d54-123">These methods provide only static information about the NAP Server and its components on the system.</span></span>

## <a name="requirements"></a><span data-ttu-id="f5d54-124">規格需求</span><span class="sxs-lookup"><span data-stu-id="f5d54-124">Requirements</span></span>



| <span data-ttu-id="f5d54-125">需求</span><span class="sxs-lookup"><span data-stu-id="f5d54-125">Requirement</span></span> | <span data-ttu-id="f5d54-126">值</span><span class="sxs-lookup"><span data-stu-id="f5d54-126">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f5d54-127">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="f5d54-127">Minimum supported client</span></span><br/> | <span data-ttu-id="f5d54-128">都不支援</span><span class="sxs-lookup"><span data-stu-id="f5d54-128">None supported</span></span><br/>                                                                          |
| <span data-ttu-id="f5d54-129">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="f5d54-129">Minimum supported server</span></span><br/> | <span data-ttu-id="f5d54-130">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="f5d54-130">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="f5d54-131">標頭</span><span class="sxs-lookup"><span data-stu-id="f5d54-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="f5d54-132"><dt>NapServerManagement。h</dt></span><span class="sxs-lookup"><span data-stu-id="f5d54-132"><dt>NapServerManagement.h</dt></span></span> </dl>   |
| <span data-ttu-id="f5d54-133">Idl</span><span class="sxs-lookup"><span data-stu-id="f5d54-133">IDL</span></span><br/>                      | <dl> <span data-ttu-id="f5d54-134"><dt>NapServerManagement .idl</dt></span><span class="sxs-lookup"><span data-stu-id="f5d54-134"><dt>NapServerManagement.idl</dt></span></span> </dl> |
| <span data-ttu-id="f5d54-135">DLL</span><span class="sxs-lookup"><span data-stu-id="f5d54-135">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f5d54-136"><dt>Qsvrmgmt.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f5d54-136"><dt>Qsvrmgmt.dll</dt></span></span> </dl>            |



## <a name="see-also"></a><span data-ttu-id="f5d54-137">另請參閱</span><span class="sxs-lookup"><span data-stu-id="f5d54-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f5d54-138">NAP 介面</span><span class="sxs-lookup"><span data-stu-id="f5d54-138">NAP Interfaces</span></span>](nap-interfaces.md)
</dt> <dt>

[<span data-ttu-id="f5d54-139">NAP 參考</span><span class="sxs-lookup"><span data-stu-id="f5d54-139">NAP Reference</span></span>](nap-reference.md)
</dt> </dl>

 

