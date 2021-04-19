---
description: 代表 VFP QOS 設定。
ms.assetid: e58a7a8d-0301-43ea-9338-18bc8c458e2d
title: Msvm_EthernetSwitchPortMigrationQosSettingData 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_EthernetSwitchPortMigrationQosSettingData
- Msvm_EthernetSwitchPortMigrationQosSettingData.QueueId
- Msvm_EthernetSwitchPortMigrationQosSettingData.Switch_ReservationMode
- Msvm_EthernetSwitchPortMigrationQosSettingData.Switch_LinkSpeedPercentage
- Msvm_EthernetSwitchPortMigrationQosSettingData.Switch_DefaultReservation
- Msvm_EthernetSwitchPortMigrationQosSettingData.Switch_EnableHardwareLimits
- Msvm_EthernetSwitchPortMigrationQosSettingData.Switch_EnableHardwareReservations
- Msvm_EthernetSwitchPortMigrationQosSettingData.Switch_EnableSoftwareReservations
- Msvm_EthernetSwitchPortMigrationQosSettingData.OutboundReservedValue
- Msvm_EthernetSwitchPortMigrationQosSettingData.OutboundMaximumMbps
- Msvm_EthernetSwitchPortMigrationQosSettingData.InboundMaximumMbps
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: e279b24178c33c760477995ff744a0699cea1aaf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106987218"
---
# <a name="msvm_ethernetswitchportmigrationqossettingdata-class"></a><span data-ttu-id="2d91d-103">Msvm \_ EthernetSwitchPortMigrationQosSettingData 類別</span><span class="sxs-lookup"><span data-stu-id="2d91d-103">Msvm\_EthernetSwitchPortMigrationQosSettingData class</span></span>

<span data-ttu-id="2d91d-104">代表 VFP QOS 設定。</span><span class="sxs-lookup"><span data-stu-id="2d91d-104">Represents the VFP QOS settings.</span></span>

<span data-ttu-id="2d91d-105">下列語法已經過受管理物件格式 (MOF) 程式碼簡化，並包含所有已繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="2d91d-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="2d91d-106">語法</span><span class="sxs-lookup"><span data-stu-id="2d91d-106">Syntax</span></span>

``` syntax
[Dynamic, UUID("FD2A5DE3-DC6C-4320-82A5-234D3AF55297"), Provider("VmmsWmiInstanceAndMethodProvider"), ExtensionId("E9B59CFA-2BE1-4B21-828F-B6FBDBDDC017"), InterfaceVersion("1"), InterfaceRevision("0"), DisplayName("Ethernet Switch Port VFP QOS Settings"), AMENDMENT]
class Msvm_EthernetSwitchPortMigrationQosSettingData : Msvm_EthernetSwitchPortFeatureSettingData
{
  string  QueueId = "";
  uint8   Switch_ReservationMode = 0;
  uint8   Switch_LinkSpeedPercentage = 0;
  uint64  Switch_DefaultReservation = 0;
  boolean Switch_EnableHardwareLimits = FALSE;
  boolean Switch_EnableHardwareReservations = FALSE;
  boolean Switch_EnableSoftwareReservations = TRUE;
  uint64  OutboundReservedValue = 0;
  uint64  OutboundMaximumMbps = 0;
  uint64  InboundMaximumMbps = 0;
};
```

## <a name="members"></a><span data-ttu-id="2d91d-107">成員</span><span class="sxs-lookup"><span data-stu-id="2d91d-107">Members</span></span>

<span data-ttu-id="2d91d-108">**Msvm \_ EthernetSwitchPortMigrationQosSettingData** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="2d91d-108">The **Msvm\_EthernetSwitchPortMigrationQosSettingData** class has these types of members:</span></span>

-   [<span data-ttu-id="2d91d-109">屬性</span><span class="sxs-lookup"><span data-stu-id="2d91d-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="2d91d-110">屬性</span><span class="sxs-lookup"><span data-stu-id="2d91d-110">Properties</span></span>

<span data-ttu-id="2d91d-111">**Msvm \_ EthernetSwitchPortMigrationQosSettingData** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="2d91d-111">The **Msvm\_EthernetSwitchPortMigrationQosSettingData** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="2d91d-112">**InboundMaximumMbps**</span><span class="sxs-lookup"><span data-stu-id="2d91d-112">**InboundMaximumMbps**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2d91d-113">資料類型： **uint64**</span><span class="sxs-lookup"><span data-stu-id="2d91d-113">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="2d91d-114">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="2d91d-114">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="2d91d-115">限定詞： **WmiDataId** (10) 、 **InterfaceVersion** (1) 、 **InterfaceRevision** (0) </span><span class="sxs-lookup"><span data-stu-id="2d91d-115">Qualifiers: **WmiDataId** (10), **InterfaceVersion** (1), **InterfaceRevision** (0)</span></span>
</dt> </dl>

<span data-ttu-id="2d91d-116">輸入流量的頻寬上限值。</span><span class="sxs-lookup"><span data-stu-id="2d91d-116">The bandwidth cap value for inbound traffic.</span></span>

</dd> <dt>

<span data-ttu-id="2d91d-117">**OutboundMaximumMbps**</span><span class="sxs-lookup"><span data-stu-id="2d91d-117">**OutboundMaximumMbps**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2d91d-118">資料類型： **uint64**</span><span class="sxs-lookup"><span data-stu-id="2d91d-118">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="2d91d-119">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="2d91d-119">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="2d91d-120">限定詞： **WmiDataId** (9) 、 **InterfaceVersion** (1) 、 **InterfaceRevision** (0) </span><span class="sxs-lookup"><span data-stu-id="2d91d-120">Qualifiers: **WmiDataId** (9), **InterfaceVersion** (1), **InterfaceRevision** (0)</span></span>
</dt> </dl>

<span data-ttu-id="2d91d-121">輸出流量的頻寬上限值。</span><span class="sxs-lookup"><span data-stu-id="2d91d-121">The bandwidth cap value for outbound traffic.</span></span>

</dd> <dt>

<span data-ttu-id="2d91d-122">**OutboundReservedValue**</span><span class="sxs-lookup"><span data-stu-id="2d91d-122">**OutboundReservedValue**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2d91d-123">資料類型： **uint64**</span><span class="sxs-lookup"><span data-stu-id="2d91d-123">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="2d91d-124">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="2d91d-124">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="2d91d-125">限定詞： **WmiDataId** (8) 、 **InterfaceVersion** (1) 、 **InterfaceRevision** (0) </span><span class="sxs-lookup"><span data-stu-id="2d91d-125">Qualifiers: **WmiDataId** (8), **InterfaceVersion** (1), **InterfaceRevision** (0)</span></span>
</dt> </dl>

<span data-ttu-id="2d91d-126">頻寬保留值。</span><span class="sxs-lookup"><span data-stu-id="2d91d-126">The bandwidth reservation value.</span></span>

</dd> <dt>

<span data-ttu-id="2d91d-127">**QueueId**</span><span class="sxs-lookup"><span data-stu-id="2d91d-127">**QueueId**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2d91d-128">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="2d91d-128">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2d91d-129">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="2d91d-129">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="2d91d-130">限定詞： [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64) 、 **WmiDataId** (1) 、 **InterfaceVersion** (1) 、 **InterfaceRevision** (0) </span><span class="sxs-lookup"><span data-stu-id="2d91d-130">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), **WmiDataId** (1), **InterfaceVersion** (1), **InterfaceRevision** (0)</span></span>
</dt> </dl>

<span data-ttu-id="2d91d-131">QOS 佇列的識別碼。</span><span class="sxs-lookup"><span data-stu-id="2d91d-131">The ID of the QOS queue.</span></span>

</dd> <dt>

<span data-ttu-id="2d91d-132">**切換 \_ DefaultReservation**</span><span class="sxs-lookup"><span data-stu-id="2d91d-132">**Switch\_DefaultReservation**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2d91d-133">資料類型： **uint64**</span><span class="sxs-lookup"><span data-stu-id="2d91d-133">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="2d91d-134">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="2d91d-134">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="2d91d-135">限定詞： **WmiDataId** (4) 、 **InterfaceVersion** (1) 、 **InterfaceRevision** (0) </span><span class="sxs-lookup"><span data-stu-id="2d91d-135">Qualifiers: **WmiDataId** (4), **InterfaceVersion** (1), **InterfaceRevision** (0)</span></span>
</dt> </dl>

<span data-ttu-id="2d91d-136">預設保留值。</span><span class="sxs-lookup"><span data-stu-id="2d91d-136">The default reservation value.</span></span>

</dd> <dt>

<span data-ttu-id="2d91d-137">**切換 \_ EnableHardwareLimits**</span><span class="sxs-lookup"><span data-stu-id="2d91d-137">**Switch\_EnableHardwareLimits**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2d91d-138">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="2d91d-138">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="2d91d-139">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="2d91d-139">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="2d91d-140">限定詞： **WmiDataId** (5) 、 [**Version**](/windows/desktop/WmiSdk/standard-qualifiers) (1) 、 [**修訂**](/windows/desktop/WmiSdk/standard-qualifiers) (0) </span><span class="sxs-lookup"><span data-stu-id="2d91d-140">Qualifiers: **WmiDataId** (5), [**Version**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**Revision**](/windows/desktop/WmiSdk/standard-qualifiers) (0)</span></span>
</dt> </dl>

<span data-ttu-id="2d91d-141">指出是否會嘗試硬體卸載以取得限制（如果有的話）。</span><span class="sxs-lookup"><span data-stu-id="2d91d-141">Indicates whether hardware offloads for limits are attempted if available.</span></span>

</dd> <dt>

<span data-ttu-id="2d91d-142">**切換 \_ EnableHardwareReservations**</span><span class="sxs-lookup"><span data-stu-id="2d91d-142">**Switch\_EnableHardwareReservations**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2d91d-143">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="2d91d-143">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="2d91d-144">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="2d91d-144">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="2d91d-145">限定詞： **WmiDataId** (6) 、 [**Version**](/windows/desktop/WmiSdk/standard-qualifiers) (1) 、 [**修訂**](/windows/desktop/WmiSdk/standard-qualifiers) (0) </span><span class="sxs-lookup"><span data-stu-id="2d91d-145">Qualifiers: **WmiDataId** (6), [**Version**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**Revision**](/windows/desktop/WmiSdk/standard-qualifiers) (0)</span></span>
</dt> </dl>

<span data-ttu-id="2d91d-146">指出是否會嘗試保留硬體卸載（如果有的話）。</span><span class="sxs-lookup"><span data-stu-id="2d91d-146">Indicates whether hardware offloads for reservations are attempted if available.</span></span>

</dd> <dt>

<span data-ttu-id="2d91d-147">**切換 \_ EnableSoftwareReservations**</span><span class="sxs-lookup"><span data-stu-id="2d91d-147">**Switch\_EnableSoftwareReservations**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2d91d-148">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="2d91d-148">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="2d91d-149">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="2d91d-149">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="2d91d-150">限定詞： **WmiDataId** (7) 、 **InterfaceVersion** (1) 、 **InterfaceRevision** (0) </span><span class="sxs-lookup"><span data-stu-id="2d91d-150">Qualifiers: **WmiDataId** (7), **InterfaceVersion** (1), **InterfaceRevision** (0)</span></span>
</dt> </dl>

<span data-ttu-id="2d91d-151">指出以軟體為基礎的保留是否可用。</span><span class="sxs-lookup"><span data-stu-id="2d91d-151">Indicates whether software based reservation is available.</span></span>

</dd> <dt>

<span data-ttu-id="2d91d-152">**切換 \_ LinkSpeedPercentage**</span><span class="sxs-lookup"><span data-stu-id="2d91d-152">**Switch\_LinkSpeedPercentage**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2d91d-153">資料類型： **uint8**</span><span class="sxs-lookup"><span data-stu-id="2d91d-153">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="2d91d-154">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="2d91d-154">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="2d91d-155">限定詞： **WmiDataId** (3) 、 **InterfaceVersion** (1) 、 **InterfaceRevision** (0) </span><span class="sxs-lookup"><span data-stu-id="2d91d-155">Qualifiers: **WmiDataId** (3), **InterfaceVersion** (1), **InterfaceRevision** (0)</span></span>
</dt> </dl>

<span data-ttu-id="2d91d-156">要用於保留的連結速度百分比。</span><span class="sxs-lookup"><span data-stu-id="2d91d-156">The link speed percentage to be used for reservation.</span></span>

</dd> <dt>

<span data-ttu-id="2d91d-157">**切換 \_ ReservationMode**</span><span class="sxs-lookup"><span data-stu-id="2d91d-157">**Switch\_ReservationMode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2d91d-158">資料類型： **uint8**</span><span class="sxs-lookup"><span data-stu-id="2d91d-158">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="2d91d-159">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="2d91d-159">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="2d91d-160">限定詞： **WmiDataId** (2) 、 **InterfaceVersion** (1) 、 **InterfaceRevision** (0) </span><span class="sxs-lookup"><span data-stu-id="2d91d-160">Qualifiers: **WmiDataId** (2), **InterfaceVersion** (1), **InterfaceRevision** (0)</span></span>
</dt> </dl>

<span data-ttu-id="2d91d-161">交換器上的 QOS 保留模式。</span><span class="sxs-lookup"><span data-stu-id="2d91d-161">The QOS reservation mode on the switch.</span></span>

<dt>

<span id="Absolute"></span><span id="absolute"></span><span id="ABSOLUTE"></span>

<span data-ttu-id="2d91d-162">**絕對** (0) </span><span class="sxs-lookup"><span data-stu-id="2d91d-162">**Absolute** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Weight"></span><span id="weight"></span><span id="WEIGHT"></span>

<span data-ttu-id="2d91d-163">**權數** (1) </span><span class="sxs-lookup"><span data-stu-id="2d91d-163">**Weight** (1)</span></span>


<span data-ttu-id="2d91d-164"></dt> <dd></dd> </dl>

</dd> </dl></span><span class="sxs-lookup"><span data-stu-id="2d91d-164"></dt> <dd></dd> </dl>

</dd> </dl></span></span>

## <a name="requirements"></a><span data-ttu-id="2d91d-165">規格需求</span><span class="sxs-lookup"><span data-stu-id="2d91d-165">Requirements</span></span>



| <span data-ttu-id="2d91d-166">需求</span><span class="sxs-lookup"><span data-stu-id="2d91d-166">Requirement</span></span> | <span data-ttu-id="2d91d-167">值</span><span class="sxs-lookup"><span data-stu-id="2d91d-167">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2d91d-168">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="2d91d-168">Minimum supported client</span></span><br/> | <span data-ttu-id="2d91d-169">Windows 10， \[ 僅限1703版桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="2d91d-169">Windows 10, version 1703 \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="2d91d-170">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="2d91d-170">Minimum supported server</span></span><br/> | <span data-ttu-id="2d91d-171">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="2d91d-171">Windows Server 2016</span></span><br/>                                                                          |
| <span data-ttu-id="2d91d-172">命名空間</span><span class="sxs-lookup"><span data-stu-id="2d91d-172">Namespace</span></span><br/>                | <span data-ttu-id="2d91d-173">根 \\ 虛擬化 \\ v2</span><span class="sxs-lookup"><span data-stu-id="2d91d-173">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="2d91d-174">MOF</span><span class="sxs-lookup"><span data-stu-id="2d91d-174">MOF</span></span><br/>                      | <dl> <span data-ttu-id="2d91d-175"><dt>WindowsVirtualization。</dt></span><span class="sxs-lookup"><span data-stu-id="2d91d-175"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="2d91d-176">DLL</span><span class="sxs-lookup"><span data-stu-id="2d91d-176">DLL</span></span><br/>                      | <dl> <span data-ttu-id="2d91d-177"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="2d91d-177"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="2d91d-178">另請參閱</span><span class="sxs-lookup"><span data-stu-id="2d91d-178">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2d91d-179">**Msvm \_ EthernetSwitchPortFeatureSettingData**</span><span class="sxs-lookup"><span data-stu-id="2d91d-179">**Msvm\_EthernetSwitchPortFeatureSettingData**</span></span>](msvm-ethernetswitchportfeaturesettingdata.md)
</dt> </dl>

 

