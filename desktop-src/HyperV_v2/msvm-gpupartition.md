---
description: 代表 GPU 分割區的狀態。
ms.assetid: 319b37d5-b5f0-4251-9482-316347a9015b
title: Msvm_GpuPartition 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_GpuPartition
- Msvm_GpuPartition.DeviceInstancePath
- Msvm_GpuPartition.PartitionId
- Msvm_GpuPartition.PartitionVfLuid
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: cc0975644609832c692f5522cc756240f7a5bff6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106983323"
---
# <a name="msvm_gpupartition-class"></a><span data-ttu-id="66048-103">Msvm \_ GpuPartition 類別</span><span class="sxs-lookup"><span data-stu-id="66048-103">Msvm\_GpuPartition class</span></span>

<span data-ttu-id="66048-104">代表 GPU 分割區的狀態。</span><span class="sxs-lookup"><span data-stu-id="66048-104">Represents the state of the GPU partition.</span></span>

<span data-ttu-id="66048-105">下列語法已經過受管理物件格式 (MOF) 程式碼簡化，並包含所有已繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="66048-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="66048-106">語法</span><span class="sxs-lookup"><span data-stu-id="66048-106">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_GpuPartition : CIM_LogicalDevice
{
  string DeviceInstancePath;
  uint16 PartitionId;
  string PartitionVfLuid;
};
```

## <a name="members"></a><span data-ttu-id="66048-107">成員</span><span class="sxs-lookup"><span data-stu-id="66048-107">Members</span></span>

<span data-ttu-id="66048-108">**Msvm \_ GpuPartition** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="66048-108">The **Msvm\_GpuPartition** class has these types of members:</span></span>

-   [<span data-ttu-id="66048-109">屬性</span><span class="sxs-lookup"><span data-stu-id="66048-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="66048-110">屬性</span><span class="sxs-lookup"><span data-stu-id="66048-110">Properties</span></span>

<span data-ttu-id="66048-111">**Msvm \_ GpuPartition** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="66048-111">The **Msvm\_GpuPartition** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="66048-112">**DeviceInstancePath**</span><span class="sxs-lookup"><span data-stu-id="66048-112">**DeviceInstancePath**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="66048-113">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="66048-113">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="66048-114">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="66048-114">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="66048-115">包含識別 GPU 磁碟分割裝置之裝置實例路徑的字串。</span><span class="sxs-lookup"><span data-stu-id="66048-115">A string containing the device instance path that identifies the GPU partition device.</span></span>

</dd> <dt>

<span data-ttu-id="66048-116">**PartitionId**</span><span class="sxs-lookup"><span data-stu-id="66048-116">**PartitionId**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="66048-117">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="66048-117">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="66048-118">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="66048-118">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="66048-119">GPU 分割區裝置的分割區識別碼。</span><span class="sxs-lookup"><span data-stu-id="66048-119">The partition ID of the GPU partition device.</span></span>

</dd> <dt>

<span data-ttu-id="66048-120">**PartitionVfLuid**</span><span class="sxs-lookup"><span data-stu-id="66048-120">**PartitionVfLuid**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="66048-121">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="66048-121">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="66048-122">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="66048-122">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="66048-123">代表 GPU 磁碟分割的虛擬函數 LUID。</span><span class="sxs-lookup"><span data-stu-id="66048-123">The virtual function LUID, which represents a GPU partition.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="66048-124">規格需求</span><span class="sxs-lookup"><span data-stu-id="66048-124">Requirements</span></span>



| <span data-ttu-id="66048-125">需求</span><span class="sxs-lookup"><span data-stu-id="66048-125">Requirement</span></span> | <span data-ttu-id="66048-126">值</span><span class="sxs-lookup"><span data-stu-id="66048-126">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="66048-127">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="66048-127">Minimum supported client</span></span><br/> | <span data-ttu-id="66048-128">Windows 10， \[ 僅限1703版桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="66048-128">Windows 10, version 1703 \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="66048-129">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="66048-129">Minimum supported server</span></span><br/> | <span data-ttu-id="66048-130">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="66048-130">Windows Server 2016</span></span><br/>                                                                          |
| <span data-ttu-id="66048-131">命名空間</span><span class="sxs-lookup"><span data-stu-id="66048-131">Namespace</span></span><br/>                | <span data-ttu-id="66048-132">根 \\ 虛擬化 \\ v2</span><span class="sxs-lookup"><span data-stu-id="66048-132">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="66048-133">MOF</span><span class="sxs-lookup"><span data-stu-id="66048-133">MOF</span></span><br/>                      | <dl> <span data-ttu-id="66048-134"><dt>WindowsVirtualization。</dt></span><span class="sxs-lookup"><span data-stu-id="66048-134"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="66048-135">DLL</span><span class="sxs-lookup"><span data-stu-id="66048-135">DLL</span></span><br/>                      | <dl> <span data-ttu-id="66048-136"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="66048-136"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="66048-137">另請參閱</span><span class="sxs-lookup"><span data-stu-id="66048-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="66048-138">**CIM \_ LogicalDevice**</span><span class="sxs-lookup"><span data-stu-id="66048-138">**CIM\_LogicalDevice**</span></span>](cim-logicaldevice.md)
</dt> </dl>

 

 




