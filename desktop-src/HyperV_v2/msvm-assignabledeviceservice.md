---
description: 管理主機電腦系統上可指派的裝置。
ms.assetid: d958e978-682e-49eb-bd10-d31d9563fdbf
title: Msvm_AssignableDeviceService 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_AssignableDeviceService
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: c8aff620e9227000b2c4a03069f8a5f900a5fc82
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106998347"
---
# <a name="msvm_assignabledeviceservice-class"></a><span data-ttu-id="6fa20-103">Msvm \_ AssignableDeviceService 類別</span><span class="sxs-lookup"><span data-stu-id="6fa20-103">Msvm\_AssignableDeviceService class</span></span>

<span data-ttu-id="6fa20-104">管理主機電腦系統上可指派的裝置。</span><span class="sxs-lookup"><span data-stu-id="6fa20-104">Manages the assignable devices on a host computer system.</span></span>

<span data-ttu-id="6fa20-105">下列語法已經過受管理物件格式 (MOF) 程式碼簡化，並包含所有已繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="6fa20-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="6fa20-106">語法</span><span class="sxs-lookup"><span data-stu-id="6fa20-106">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_AssignableDeviceService : CIM_Service
{
};
```

## <a name="members"></a><span data-ttu-id="6fa20-107">成員</span><span class="sxs-lookup"><span data-stu-id="6fa20-107">Members</span></span>

<span data-ttu-id="6fa20-108">**Msvm \_ AssignableDeviceService** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="6fa20-108">The **Msvm\_AssignableDeviceService** class has these types of members:</span></span>

-   [<span data-ttu-id="6fa20-109">方法</span><span class="sxs-lookup"><span data-stu-id="6fa20-109">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="6fa20-110">方法</span><span class="sxs-lookup"><span data-stu-id="6fa20-110">Methods</span></span>

<span data-ttu-id="6fa20-111">**Msvm \_ AssignableDeviceService** 類別具有這些方法。</span><span class="sxs-lookup"><span data-stu-id="6fa20-111">The **Msvm\_AssignableDeviceService** class has these methods.</span></span>



| <span data-ttu-id="6fa20-112">方法</span><span class="sxs-lookup"><span data-stu-id="6fa20-112">Method</span></span>                                                                                    | <span data-ttu-id="6fa20-113">描述</span><span class="sxs-lookup"><span data-stu-id="6fa20-113">Description</span></span>                                                                                    |
|:------------------------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------|
| [<span data-ttu-id="6fa20-114">**DismountAssignableDevice**</span><span class="sxs-lookup"><span data-stu-id="6fa20-114">**DismountAssignableDevice**</span></span>](msvm-assignabledeviceservice-dismountassignabledevice.md) | <span data-ttu-id="6fa20-115">卸載指定的 PCI 裝置，讓它可以指派。</span><span class="sxs-lookup"><span data-stu-id="6fa20-115">Dismounts the specified PCI device so that it can be assigned.</span></span><br/>                      |
| [<span data-ttu-id="6fa20-116">**MountAssignableDevice**</span><span class="sxs-lookup"><span data-stu-id="6fa20-116">**MountAssignableDevice**</span></span>](msvm-assignabledeviceservice-mountassignabledevice.md)       | <span data-ttu-id="6fa20-117">裝載指定的 PCI 裝置，使其可供主機電腦系統使用。</span><span class="sxs-lookup"><span data-stu-id="6fa20-117">Mounts the specified PCI device so that it can be used by the host computer system.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="6fa20-118">規格需求</span><span class="sxs-lookup"><span data-stu-id="6fa20-118">Requirements</span></span>



| <span data-ttu-id="6fa20-119">需求</span><span class="sxs-lookup"><span data-stu-id="6fa20-119">Requirement</span></span> | <span data-ttu-id="6fa20-120">值</span><span class="sxs-lookup"><span data-stu-id="6fa20-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6fa20-121">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="6fa20-121">Minimum supported client</span></span><br/> | <span data-ttu-id="6fa20-122">Windows 10， \[ 僅限1703版桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="6fa20-122">Windows 10, version 1703 \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="6fa20-123">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="6fa20-123">Minimum supported server</span></span><br/> | <span data-ttu-id="6fa20-124">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="6fa20-124">Windows Server 2016</span></span><br/>                                                                          |
| <span data-ttu-id="6fa20-125">命名空間</span><span class="sxs-lookup"><span data-stu-id="6fa20-125">Namespace</span></span><br/>                | <span data-ttu-id="6fa20-126">根 \\ 虛擬化 \\ v2</span><span class="sxs-lookup"><span data-stu-id="6fa20-126">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="6fa20-127">MOF</span><span class="sxs-lookup"><span data-stu-id="6fa20-127">MOF</span></span><br/>                      | <dl> <span data-ttu-id="6fa20-128"><dt>WindowsVirtualization。</dt></span><span class="sxs-lookup"><span data-stu-id="6fa20-128"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="6fa20-129">DLL</span><span class="sxs-lookup"><span data-stu-id="6fa20-129">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6fa20-130"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="6fa20-130"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="6fa20-131">另請參閱</span><span class="sxs-lookup"><span data-stu-id="6fa20-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6fa20-132">**CIM \_ 服務**</span><span class="sxs-lookup"><span data-stu-id="6fa20-132">**CIM\_Service**</span></span>](cim-service.md)
</dt> </dl>

 

 




