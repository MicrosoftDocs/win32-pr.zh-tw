---
description: 表示安全性服務。 它是用來設定虛擬系統安全性設定。
ms.assetid: 00097d81-9fea-4b84-b5dd-e45af46d6e0a
title: Msvm_SecurityService 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_SecurityService
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: cc7b15af3d3033487464fe7b29a93dc649ffbd62
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103944373"
---
# <a name="msvm_securityservice-class"></a><span data-ttu-id="1972c-104">Msvm \_ SecurityService 類別</span><span class="sxs-lookup"><span data-stu-id="1972c-104">Msvm\_SecurityService class</span></span>

<span data-ttu-id="1972c-105">表示安全性服務。</span><span class="sxs-lookup"><span data-stu-id="1972c-105">Represents the security service.</span></span> <span data-ttu-id="1972c-106">它是用來設定虛擬系統安全性設定。</span><span class="sxs-lookup"><span data-stu-id="1972c-106">It is used for configuring virtual system security settings.</span></span>

<span data-ttu-id="1972c-107">下列語法已經過受管理物件格式 (MOF) 程式碼簡化，並包含所有已繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="1972c-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="1972c-108">語法</span><span class="sxs-lookup"><span data-stu-id="1972c-108">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_SecurityService : CIM_Service
{
};
```

## <a name="members"></a><span data-ttu-id="1972c-109">成員</span><span class="sxs-lookup"><span data-stu-id="1972c-109">Members</span></span>

<span data-ttu-id="1972c-110">**Msvm \_ SecurityService** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="1972c-110">The **Msvm\_SecurityService** class has these types of members:</span></span>

-   [<span data-ttu-id="1972c-111">方法</span><span class="sxs-lookup"><span data-stu-id="1972c-111">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="1972c-112">方法</span><span class="sxs-lookup"><span data-stu-id="1972c-112">Methods</span></span>

<span data-ttu-id="1972c-113">**Msvm \_ SecurityService** 類別具有這些方法。</span><span class="sxs-lookup"><span data-stu-id="1972c-113">The **Msvm\_SecurityService** class has these methods.</span></span>



| <span data-ttu-id="1972c-114">方法</span><span class="sxs-lookup"><span data-stu-id="1972c-114">Method</span></span>                                                                                            | <span data-ttu-id="1972c-115">描述</span><span class="sxs-lookup"><span data-stu-id="1972c-115">Description</span></span>                                                             |
|:--------------------------------------------------------------------------------------------------|:------------------------------------------------------------------------|
| [<span data-ttu-id="1972c-116">**GetKeyProtector**</span><span class="sxs-lookup"><span data-stu-id="1972c-116">**GetKeyProtector**</span></span>](msvm-securityservice-getkeyprotector.md)                                   | <span data-ttu-id="1972c-117">取得虛擬系統金鑰保護裝置的方法。</span><span class="sxs-lookup"><span data-stu-id="1972c-117">Method to retrieve the key protector for a virtual system.</span></span><br/>   |
| [<span data-ttu-id="1972c-118">**ModifySecuritySettings**</span><span class="sxs-lookup"><span data-stu-id="1972c-118">**ModifySecuritySettings**</span></span>](msvm-securityservice-modifysecuritysettings.md)                     | <span data-ttu-id="1972c-119">修改虛擬機器的目前安全性設定。</span><span class="sxs-lookup"><span data-stu-id="1972c-119">Modifies the current security settings of a virtual machine.</span></span><br/> |
| [<span data-ttu-id="1972c-120">**RestoreLastKnownGoodKeyProtector**</span><span class="sxs-lookup"><span data-stu-id="1972c-120">**RestoreLastKnownGoodKeyProtector**</span></span>](msvm-securityservice-restorelastknowngoodkeyprotector.md) | <span data-ttu-id="1972c-121">還原到最後一個已知良好的金鑰保護裝置的方法。</span><span class="sxs-lookup"><span data-stu-id="1972c-121">Method to restore back to the last known good key protector.</span></span><br/> |
| [<span data-ttu-id="1972c-122">**SetKeyProtector**</span><span class="sxs-lookup"><span data-stu-id="1972c-122">**SetKeyProtector**</span></span>](msvm-securityservice-setkeyprotector.md)                                   | <span data-ttu-id="1972c-123">為虛擬系統設定金鑰保護裝置的方法。</span><span class="sxs-lookup"><span data-stu-id="1972c-123">Method to set the key protector for a virtual system.</span></span><br/>        |
| [<span data-ttu-id="1972c-124">**SetSecurityPolicy**</span><span class="sxs-lookup"><span data-stu-id="1972c-124">**SetSecurityPolicy**</span></span>](msvm-securityservice-setsecuritypolicy.md)                               | <span data-ttu-id="1972c-125">為虛擬系統設定金鑰保護裝置的方法。</span><span class="sxs-lookup"><span data-stu-id="1972c-125">Method to set the key protector for a virtual system.</span></span><br/>        |
| [<span data-ttu-id="1972c-126">**StartService**</span><span class="sxs-lookup"><span data-stu-id="1972c-126">**StartService**</span></span>](msvm-securityservice-startservice.md)                                         | <span data-ttu-id="1972c-127">啟動服務。</span><span class="sxs-lookup"><span data-stu-id="1972c-127">Starts the service.</span></span><br/>                                          |
| [<span data-ttu-id="1972c-128">**StopService**</span><span class="sxs-lookup"><span data-stu-id="1972c-128">**StopService**</span></span>](msvm-securityservice-stopservice.md)                                           | <span data-ttu-id="1972c-129">停止服務。</span><span class="sxs-lookup"><span data-stu-id="1972c-129">Stops the service.</span></span><br/>                                           |



 

## <a name="requirements"></a><span data-ttu-id="1972c-130">規格需求</span><span class="sxs-lookup"><span data-stu-id="1972c-130">Requirements</span></span>



| <span data-ttu-id="1972c-131">需求</span><span class="sxs-lookup"><span data-stu-id="1972c-131">Requirement</span></span> | <span data-ttu-id="1972c-132">值</span><span class="sxs-lookup"><span data-stu-id="1972c-132">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1972c-133">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="1972c-133">Minimum supported client</span></span><br/> | <span data-ttu-id="1972c-134">Windows 10， \[ 僅限1703版桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="1972c-134">Windows 10, version 1703 \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="1972c-135">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="1972c-135">Minimum supported server</span></span><br/> | <span data-ttu-id="1972c-136">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="1972c-136">Windows Server 2016</span></span><br/>                                                                          |
| <span data-ttu-id="1972c-137">命名空間</span><span class="sxs-lookup"><span data-stu-id="1972c-137">Namespace</span></span><br/>                | <span data-ttu-id="1972c-138">根 \\ 虛擬化 \\ v2</span><span class="sxs-lookup"><span data-stu-id="1972c-138">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="1972c-139">MOF</span><span class="sxs-lookup"><span data-stu-id="1972c-139">MOF</span></span><br/>                      | <dl> <span data-ttu-id="1972c-140"><dt>WindowsVirtualization。</dt></span><span class="sxs-lookup"><span data-stu-id="1972c-140"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="1972c-141">DLL</span><span class="sxs-lookup"><span data-stu-id="1972c-141">DLL</span></span><br/>                      | <dl> <span data-ttu-id="1972c-142"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="1972c-142"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="1972c-143">另請參閱</span><span class="sxs-lookup"><span data-stu-id="1972c-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1972c-144">**CIM \_ 服務**</span><span class="sxs-lookup"><span data-stu-id="1972c-144">**CIM\_Service**</span></span>](cim-service.md)
</dt> </dl>

 

 




