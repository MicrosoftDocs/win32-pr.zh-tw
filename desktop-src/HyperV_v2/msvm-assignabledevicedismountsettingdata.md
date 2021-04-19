---
description: 代表要匯入的虛擬系統設定。 由 Msvm AssignableDeviceService 類別的卸載方法所使用 \_ 。
ms.assetid: 49892e21-3e8d-4644-8cde-72966927f350
title: Msvm_AssignableDeviceDismountSettingData 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_AssignableDeviceDismountSettingData
- Msvm_AssignableDeviceDismountSettingData.DeviceInstancePath
- Msvm_AssignableDeviceDismountSettingData.DeviceLocationPath
- Msvm_AssignableDeviceDismountSettingData.RequireAcsSupport
- Msvm_AssignableDeviceDismountSettingData.RequireDeviceMitigations
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: c5783ed9611c16d875211f29d364fe3eaff29b57
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106990320"
---
# <a name="msvm_assignabledevicedismountsettingdata-class"></a><span data-ttu-id="17c7a-104">Msvm \_ AssignableDeviceDismountSettingData 類別</span><span class="sxs-lookup"><span data-stu-id="17c7a-104">Msvm\_AssignableDeviceDismountSettingData class</span></span>

<span data-ttu-id="17c7a-105">代表要匯入的虛擬系統設定。</span><span class="sxs-lookup"><span data-stu-id="17c7a-105">Represents the settings of a virtual system to import.</span></span> <span data-ttu-id="17c7a-106">由 [**Msvm \_ AssignableDeviceService**](msvm-assignabledeviceservice.md)類別的 [**卸載**](msvm-assignabledeviceservice-dismountassignabledevice.md)方法所使用。</span><span class="sxs-lookup"><span data-stu-id="17c7a-106">Used by the [**Dismount**](msvm-assignabledeviceservice-dismountassignabledevice.md) method of the [**Msvm\_AssignableDeviceService**](msvm-assignabledeviceservice.md) class.</span></span>

<span data-ttu-id="17c7a-107">下列語法已經過受管理物件格式 (MOF) 程式碼簡化，並包含所有已繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="17c7a-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="17c7a-108">語法</span><span class="sxs-lookup"><span data-stu-id="17c7a-108">Syntax</span></span>

``` syntax
[AMENDMENT]
class Msvm_AssignableDeviceDismountSettingData : CIM_SettingData
{
  string  DeviceInstancePath;
  string  DeviceLocationPath;
  boolean RequireAcsSupport;
  boolean RequireDeviceMitigations;
};
```

## <a name="members"></a><span data-ttu-id="17c7a-109">成員</span><span class="sxs-lookup"><span data-stu-id="17c7a-109">Members</span></span>

<span data-ttu-id="17c7a-110">**Msvm \_ AssignableDeviceDismountSettingData** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="17c7a-110">The **Msvm\_AssignableDeviceDismountSettingData** class has these types of members:</span></span>

-   [<span data-ttu-id="17c7a-111">屬性</span><span class="sxs-lookup"><span data-stu-id="17c7a-111">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="17c7a-112">屬性</span><span class="sxs-lookup"><span data-stu-id="17c7a-112">Properties</span></span>

<span data-ttu-id="17c7a-113">**Msvm \_ AssignableDeviceDismountSettingData** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="17c7a-113">The **Msvm\_AssignableDeviceDismountSettingData** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="17c7a-114">**DeviceInstancePath**</span><span class="sxs-lookup"><span data-stu-id="17c7a-114">**DeviceInstancePath**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="17c7a-115">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="17c7a-115">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="17c7a-116">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="17c7a-116">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="17c7a-117">PNP 裝置實例識別碼。</span><span class="sxs-lookup"><span data-stu-id="17c7a-117">PNP device instance ID.</span></span>

</dd> <dt>

<span data-ttu-id="17c7a-118">**DeviceLocationPath**</span><span class="sxs-lookup"><span data-stu-id="17c7a-118">**DeviceLocationPath**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="17c7a-119">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="17c7a-119">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="17c7a-120">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="17c7a-120">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="17c7a-121">PNP 裝置位置路徑。</span><span class="sxs-lookup"><span data-stu-id="17c7a-121">PNP device location path.</span></span>

</dd> <dt>

<span data-ttu-id="17c7a-122">**RequireAcsSupport**</span><span class="sxs-lookup"><span data-stu-id="17c7a-122">**RequireAcsSupport**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="17c7a-123">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="17c7a-123">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="17c7a-124">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="17c7a-124">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="17c7a-125">指出是否應該先備妥必要的 ACS 支援，才能允許進行卸載。</span><span class="sxs-lookup"><span data-stu-id="17c7a-125">Indicates if the requisite ACS support should be in place before permitting the dismount.</span></span>

</dd> <dt>

<span data-ttu-id="17c7a-126">**RequireDeviceMitigations**</span><span class="sxs-lookup"><span data-stu-id="17c7a-126">**RequireDeviceMitigations**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="17c7a-127">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="17c7a-127">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="17c7a-128">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="17c7a-128">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="17c7a-129">指出是否應該先備妥裝置緩和措施，才能允許卸載。</span><span class="sxs-lookup"><span data-stu-id="17c7a-129">Indicates if device mitigations should be in place before permitting the dismount.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="17c7a-130">規格需求</span><span class="sxs-lookup"><span data-stu-id="17c7a-130">Requirements</span></span>



| <span data-ttu-id="17c7a-131">需求</span><span class="sxs-lookup"><span data-stu-id="17c7a-131">Requirement</span></span> | <span data-ttu-id="17c7a-132">值</span><span class="sxs-lookup"><span data-stu-id="17c7a-132">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="17c7a-133">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="17c7a-133">Minimum supported client</span></span><br/> | <span data-ttu-id="17c7a-134">Windows 10， \[ 僅限1703版桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="17c7a-134">Windows 10, version 1703 \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="17c7a-135">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="17c7a-135">Minimum supported server</span></span><br/> | <span data-ttu-id="17c7a-136">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="17c7a-136">Windows Server 2016</span></span><br/>                                                                          |
| <span data-ttu-id="17c7a-137">命名空間</span><span class="sxs-lookup"><span data-stu-id="17c7a-137">Namespace</span></span><br/>                | <span data-ttu-id="17c7a-138">根 \\ 虛擬化 \\ v2</span><span class="sxs-lookup"><span data-stu-id="17c7a-138">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="17c7a-139">MOF</span><span class="sxs-lookup"><span data-stu-id="17c7a-139">MOF</span></span><br/>                      | <dl> <span data-ttu-id="17c7a-140"><dt>WindowsVirtualization。</dt></span><span class="sxs-lookup"><span data-stu-id="17c7a-140"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="17c7a-141">DLL</span><span class="sxs-lookup"><span data-stu-id="17c7a-141">DLL</span></span><br/>                      | <dl> <span data-ttu-id="17c7a-142"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="17c7a-142"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="17c7a-143">另請參閱</span><span class="sxs-lookup"><span data-stu-id="17c7a-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="17c7a-144">**CIM \_ SettingData**</span><span class="sxs-lookup"><span data-stu-id="17c7a-144">**CIM\_SettingData**</span></span>](cim-settingdata.md)
</dt> </dl>

 

 




