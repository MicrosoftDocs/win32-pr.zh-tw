---
title: Win32_RDMSEnvironment 類別
description: 管理 (RDMS) 環境的遠端桌面管理服務。
ms.assetid: 8a3b10c1-d01d-4e52-8915-29159cc406cc
ms.tgt_platform: multiple
keywords:
- Win32_RDMSEnvironment 類別遠端桌面服務
- Win32_RDMSEnvironment 類別遠端桌面服務，描述
topic_type:
- apiref
api_name:
- Win32_RDMSEnvironment
api_location:
- RDMS.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9a78acb964471844be74481d1ddfa2d4cf56a173
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106967331"
---
# <a name="win32_rdmsenvironment-class"></a><span data-ttu-id="70bc7-105">Win32 \_ RDMSEnvironment 類別</span><span class="sxs-lookup"><span data-stu-id="70bc7-105">Win32\_RDMSEnvironment class</span></span>

<span data-ttu-id="70bc7-106">管理 (RDMS) 環境的遠端桌面管理服務。</span><span class="sxs-lookup"><span data-stu-id="70bc7-106">Manages a Remote Desktop Management Services (RDMS) environment.</span></span>

<span data-ttu-id="70bc7-107">下列語法已經過受管理物件格式 (MOF) 程式碼簡化，並包含所有已繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="70bc7-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="70bc7-108">語法</span><span class="sxs-lookup"><span data-stu-id="70bc7-108">Syntax</span></span>

``` syntax
[dynamic, provider("Win32_RDManagement_Prov"), AMENDMENT]
class Win32_RDMSEnvironment
{
};
```

## <a name="members"></a><span data-ttu-id="70bc7-109">成員</span><span class="sxs-lookup"><span data-stu-id="70bc7-109">Members</span></span>

<span data-ttu-id="70bc7-110">**Win32 \_ RDMSEnvironment** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="70bc7-110">The **Win32\_RDMSEnvironment** class has these types of members:</span></span>

-   [<span data-ttu-id="70bc7-111">方法</span><span class="sxs-lookup"><span data-stu-id="70bc7-111">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="70bc7-112">方法</span><span class="sxs-lookup"><span data-stu-id="70bc7-112">Methods</span></span>

<span data-ttu-id="70bc7-113">**Win32 \_ RDMSEnvironment** 類別具有這些方法。</span><span class="sxs-lookup"><span data-stu-id="70bc7-113">The **Win32\_RDMSEnvironment** class has these methods.</span></span>



| <span data-ttu-id="70bc7-114">方法</span><span class="sxs-lookup"><span data-stu-id="70bc7-114">Method</span></span>                                                                   | <span data-ttu-id="70bc7-115">描述</span><span class="sxs-lookup"><span data-stu-id="70bc7-115">Description</span></span>                                                                                          |
|:-------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="70bc7-116">**GetActiveServer**</span><span class="sxs-lookup"><span data-stu-id="70bc7-116">**GetActiveServer**</span></span>](getactiveserver-win32-rdmsenvironment.md)         | <span data-ttu-id="70bc7-117">捕獲 RDMS 環境 (FQDN) 的完整功能變數名稱。</span><span class="sxs-lookup"><span data-stu-id="70bc7-117">Retrieves the fully qualified domain name (FQDN) of the RDMS environment.</span></span><br/>                 |
| [<span data-ttu-id="70bc7-118">**GetClientAccessName**</span><span class="sxs-lookup"><span data-stu-id="70bc7-118">**GetClientAccessName**</span></span>](getclientaccessname-win32-rdmsenvironment.md) | <span data-ttu-id="70bc7-119">抓取 (DNS) 資源記錄 (RR) RDMS 環境名稱的網域名稱系統。</span><span class="sxs-lookup"><span data-stu-id="70bc7-119">Retrieves the Domain Name System (DNS) resource record (RR) name of the RDMS environment.</span></span><br/> |
| [<span data-ttu-id="70bc7-120">**SetActiveServer**</span><span class="sxs-lookup"><span data-stu-id="70bc7-120">**SetActiveServer**</span></span>](setactiveserver-win32-rdmsenvironment.md)         | <span data-ttu-id="70bc7-121">將 RDMS 環境的 FQDN 設定為目前的節點。</span><span class="sxs-lookup"><span data-stu-id="70bc7-121">Sets the FQDN of the RDMS environment to the current node.</span></span><br/>                                |
| [<span data-ttu-id="70bc7-122">**SetClientAccessName**</span><span class="sxs-lookup"><span data-stu-id="70bc7-122">**SetClientAccessName**</span></span>](setclientaccessname-win32-rdmsenvironment.md) | <span data-ttu-id="70bc7-123">更新 RDM 環境的 DNS RR 名稱。</span><span class="sxs-lookup"><span data-stu-id="70bc7-123">Updates the DNS RR name of the RDMS environment.</span></span><br/>                                          |



 

## <a name="requirements"></a><span data-ttu-id="70bc7-124">規格需求</span><span class="sxs-lookup"><span data-stu-id="70bc7-124">Requirements</span></span>



| <span data-ttu-id="70bc7-125">需求</span><span class="sxs-lookup"><span data-stu-id="70bc7-125">Requirement</span></span> | <span data-ttu-id="70bc7-126">值</span><span class="sxs-lookup"><span data-stu-id="70bc7-126">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="70bc7-127">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="70bc7-127">Minimum supported client</span></span><br/> | <span data-ttu-id="70bc7-128">都不支援</span><span class="sxs-lookup"><span data-stu-id="70bc7-128">None supported</span></span><br/>                                                                   |
| <span data-ttu-id="70bc7-129">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="70bc7-129">Minimum supported server</span></span><br/> | <span data-ttu-id="70bc7-130">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="70bc7-130">Windows Server 2012</span></span><br/>                                                              |
| <span data-ttu-id="70bc7-131">命名空間</span><span class="sxs-lookup"><span data-stu-id="70bc7-131">Namespace</span></span><br/>                | <span data-ttu-id="70bc7-132">根 \\ cimv2 \\ rdm</span><span class="sxs-lookup"><span data-stu-id="70bc7-132">Root\\cimv2\\rdms</span></span><br/>                                                                |
| <span data-ttu-id="70bc7-133">MOF</span><span class="sxs-lookup"><span data-stu-id="70bc7-133">MOF</span></span><br/>                      | <dl> <span data-ttu-id="70bc7-134"><dt>RDManagement mof</dt></span><span class="sxs-lookup"><span data-stu-id="70bc7-134"><dt>RDManagement.mof</dt></span></span> </dl> |
| <span data-ttu-id="70bc7-135">DLL</span><span class="sxs-lookup"><span data-stu-id="70bc7-135">DLL</span></span><br/>                      | <dl> <span data-ttu-id="70bc7-136"><dt>RDMS.dll</dt></span><span class="sxs-lookup"><span data-stu-id="70bc7-136"><dt>RDMS.dll</dt></span></span> </dl>         |



## <a name="see-also"></a><span data-ttu-id="70bc7-137">另請參閱</span><span class="sxs-lookup"><span data-stu-id="70bc7-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="70bc7-138">遠端桌面管理服務提供者</span><span class="sxs-lookup"><span data-stu-id="70bc7-138">Remote Desktop Management Services Provider</span></span>](rdms-api-reference.md)
</dt> </dl>

 

 





