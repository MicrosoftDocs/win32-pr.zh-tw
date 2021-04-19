---
description: 代表擴充通訊埠 ACL 設定。
ms.assetid: 357dd891-6692-4ffc-b8a8-4ece40d4af28
title: Msvm_EthernetSwitchPortExtendedAclSettingData 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_EthernetSwitchPortExtendedAclSettingData
- Msvm_EthernetSwitchPortExtendedAclSettingData.Name
- Msvm_EthernetSwitchPortExtendedAclSettingData.Direction
- Msvm_EthernetSwitchPortExtendedAclSettingData.Action
- Msvm_EthernetSwitchPortExtendedAclSettingData.LocalIPAddress
- Msvm_EthernetSwitchPortExtendedAclSettingData.RemoteIPAddress
- Msvm_EthernetSwitchPortExtendedAclSettingData.LocalPort
- Msvm_EthernetSwitchPortExtendedAclSettingData.RemotePort
- Msvm_EthernetSwitchPortExtendedAclSettingData.Protocol
- Msvm_EthernetSwitchPortExtendedAclSettingData.Weight
- Msvm_EthernetSwitchPortExtendedAclSettingData.Stateful
- Msvm_EthernetSwitchPortExtendedAclSettingData.IdleSessionTimeout
- Msvm_EthernetSwitchPortExtendedAclSettingData.IsolationID
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 25ae81e4f00e87e41170ac5713ced0d9b523c844
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "107001392"
---
# <a name="msvm_ethernetswitchportextendedaclsettingdata-class"></a><span data-ttu-id="38803-103">Msvm \_ EthernetSwitchPortExtendedAclSettingData 類別</span><span class="sxs-lookup"><span data-stu-id="38803-103">Msvm\_EthernetSwitchPortExtendedAclSettingData class</span></span>

<span data-ttu-id="38803-104">代表擴充通訊埠 ACL 設定。</span><span class="sxs-lookup"><span data-stu-id="38803-104">Represents the extended port ACL settings.</span></span>

<span data-ttu-id="38803-105">下列語法已經過受管理物件格式 (MOF) 程式碼簡化，並包含所有已繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="38803-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="38803-106">語法</span><span class="sxs-lookup"><span data-stu-id="38803-106">Syntax</span></span>

``` syntax
[Dynamic, UUID("CD168FF0-A16D-4514-B7B5-8BBBA791A928"), ExtensionId("11EC6134-128A-4A23-B12F-164184B48348"), Provider("VmmsWmiInstanceAndMethodProvider"), InterfaceVersion("1"), InterfaceRevision("0"), DisplayName("Ethernet Switch Port Extended ACL Settings"), AMENDMENT]
class Msvm_EthernetSwitchPortExtendedAclSettingData : Msvm_EthernetSwitchPortFeatureSettingData
{
  string  Name = "";
  uint8   Direction = 0;
  uint8   Action = 0;
  string  LocalIPAddress = "ANY";
  string  RemoteIPAddress = "ANY";
  string  LocalPort = "ANY";
  string  RemotePort = "ANY";
  string  Protocol = "ANY";
  Uint16  Weight = 0;
  Boolean Stateful = FALSE;
  Uint16  IdleSessionTimeout = 255;
  Uint32  IsolationID = 0;
};
```

## <a name="members"></a><span data-ttu-id="38803-107">成員</span><span class="sxs-lookup"><span data-stu-id="38803-107">Members</span></span>

<span data-ttu-id="38803-108">**Msvm \_ EthernetSwitchPortExtendedAclSettingData** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="38803-108">The **Msvm\_EthernetSwitchPortExtendedAclSettingData** class has these types of members:</span></span>

-   [<span data-ttu-id="38803-109">屬性</span><span class="sxs-lookup"><span data-stu-id="38803-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="38803-110">屬性</span><span class="sxs-lookup"><span data-stu-id="38803-110">Properties</span></span>

<span data-ttu-id="38803-111">**Msvm \_ EthernetSwitchPortExtendedAclSettingData** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="38803-111">The **Msvm\_EthernetSwitchPortExtendedAclSettingData** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="38803-112">**動作**</span><span class="sxs-lookup"><span data-stu-id="38803-112">**Action**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="38803-113">資料類型： **uint8**</span><span class="sxs-lookup"><span data-stu-id="38803-113">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="38803-114">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="38803-114">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="38803-115">限定詞： **WmiDataId** (3) 、 **InterfaceVersion** (1) 、 **InterfaceRevision** (0) </span><span class="sxs-lookup"><span data-stu-id="38803-115">Qualifiers: **WmiDataId** (3), **InterfaceVersion** (1), **InterfaceRevision** (0)</span></span>
</dt> </dl>

<span data-ttu-id="38803-116">擴充 ACL 的動作。</span><span class="sxs-lookup"><span data-stu-id="38803-116">The action of the extended ACL.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="38803-117">**未知** 的 (0) </span><span class="sxs-lookup"><span data-stu-id="38803-117">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Allow"></span><span id="allow"></span><span id="ALLOW"></span>

<span data-ttu-id="38803-118">**允許** (1) </span><span class="sxs-lookup"><span data-stu-id="38803-118">**Allow** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Deny"></span><span id="deny"></span><span id="DENY"></span>

<span data-ttu-id="38803-119">**拒絕** (2) </span><span class="sxs-lookup"><span data-stu-id="38803-119">**Deny** (2)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="38803-120">[方向]</span><span class="sxs-lookup"><span data-stu-id="38803-120">**Direction**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="38803-121">資料類型： **uint8**</span><span class="sxs-lookup"><span data-stu-id="38803-121">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="38803-122">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="38803-122">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="38803-123">限定詞： **WmiDataId** (2) 、 **InterfaceVersion** (1) 、 **InterfaceRevision** (0) </span><span class="sxs-lookup"><span data-stu-id="38803-123">Qualifiers: **WmiDataId** (2), **InterfaceVersion** (1), **InterfaceRevision** (0)</span></span>
</dt> </dl>

<span data-ttu-id="38803-124">指出延伸的 ACL 是否適用于連入或連出方向。</span><span class="sxs-lookup"><span data-stu-id="38803-124">Indicates if the extended ACL applies to incoming or outgoing direction.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="38803-125">**未知** 的 (0) </span><span class="sxs-lookup"><span data-stu-id="38803-125">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Incoming"></span><span id="incoming"></span><span id="INCOMING"></span>

<span data-ttu-id="38803-126">**傳入** 的 (1) </span><span class="sxs-lookup"><span data-stu-id="38803-126">**Incoming** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Outgoing"></span><span id="outgoing"></span><span id="OUTGOING"></span>

<span data-ttu-id="38803-127">連 **出** (2) </span><span class="sxs-lookup"><span data-stu-id="38803-127">**Outgoing** (2)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="38803-128">**IdleSessionTimeout**</span><span class="sxs-lookup"><span data-stu-id="38803-128">**IdleSessionTimeout**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="38803-129">資料類型： **Uint16**</span><span class="sxs-lookup"><span data-stu-id="38803-129">Data type: **Uint16**</span></span>
</dt> <dt>

<span data-ttu-id="38803-130">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="38803-130">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="38803-131">限定詞： **WmiDataId** (11) 、 **InterfaceVersion** (1) 、 **InterfaceRevision** (0) </span><span class="sxs-lookup"><span data-stu-id="38803-131">Qualifiers: **WmiDataId** (11), **InterfaceVersion** (1), **InterfaceRevision** (0)</span></span>
</dt> </dl>

<span data-ttu-id="38803-132">可設定狀態 ACL 的閒置會話超時值 (秒) 。</span><span class="sxs-lookup"><span data-stu-id="38803-132">Idle session timeout value (in seconds) for stateful ACL.</span></span>

</dd> <dt>

<span data-ttu-id="38803-133">**IsolationID**</span><span class="sxs-lookup"><span data-stu-id="38803-133">**IsolationID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="38803-134">資料類型： **Uint32**</span><span class="sxs-lookup"><span data-stu-id="38803-134">Data type: **Uint32**</span></span>
</dt> <dt>

<span data-ttu-id="38803-135">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="38803-135">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="38803-136">限定詞： **InterfaceVersion** (1) 、 **InterfaceRevision** (0) 、 **WmiDataId** (12) </span><span class="sxs-lookup"><span data-stu-id="38803-136">Qualifiers: **InterfaceVersion** (1), **InterfaceRevision** (0), **WmiDataId** (12)</span></span>
</dt> </dl>

<span data-ttu-id="38803-137">應套用擴充 ACL 的隔離識別碼。</span><span class="sxs-lookup"><span data-stu-id="38803-137">Isolation ID for which the extended ACL should be applied.</span></span>

</dd> <dt>

<span data-ttu-id="38803-138">**Server.localipaddress**</span><span class="sxs-lookup"><span data-stu-id="38803-138">**LocalIPAddress**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="38803-139">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="38803-139">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="38803-140">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="38803-140">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="38803-141">限定詞： [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (40) 、 **WmiDataId** (4) 、 **InterfaceVersion** (1) 、 **InterfaceRevision** (0) </span><span class="sxs-lookup"><span data-stu-id="38803-141">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (40), **WmiDataId** (4), **InterfaceVersion** (1), **InterfaceRevision** (0)</span></span>
</dt> </dl>

<span data-ttu-id="38803-142">本機 IP 位址。</span><span class="sxs-lookup"><span data-stu-id="38803-142">The local IP address.</span></span>

</dd> <dt>

<span data-ttu-id="38803-143">**LocalPort**</span><span class="sxs-lookup"><span data-stu-id="38803-143">**LocalPort**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="38803-144">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="38803-144">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="38803-145">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="38803-145">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="38803-146">限定詞： [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (21) 、 **WmiDataId** (6) 、 **InterfaceVersion** (1) 、 **InterfaceRevision** (0) </span><span class="sxs-lookup"><span data-stu-id="38803-146">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (21), **WmiDataId** (6), **InterfaceVersion** (1), **InterfaceRevision** (0)</span></span>
</dt> </dl>

<span data-ttu-id="38803-147">本機埠範圍。</span><span class="sxs-lookup"><span data-stu-id="38803-147">The local port range.</span></span>

</dd> <dt>

<span data-ttu-id="38803-148">**名稱**</span><span class="sxs-lookup"><span data-stu-id="38803-148">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="38803-149">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="38803-149">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="38803-150">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="38803-150">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="38803-151">限定詞： [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64) 、 **WmiDataId** (1) 、 **InterfaceVersion** (1) 、 **InterfaceRevision** (0) </span><span class="sxs-lookup"><span data-stu-id="38803-151">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), **WmiDataId** (1), **InterfaceVersion** (1), **InterfaceRevision** (0)</span></span>
</dt> </dl>

<span data-ttu-id="38803-152">擴充 ACL 的易記名稱。</span><span class="sxs-lookup"><span data-stu-id="38803-152">The friendly name of the Extended ACL.</span></span>

</dd> <dt>

<span data-ttu-id="38803-153">**通訊協定**</span><span class="sxs-lookup"><span data-stu-id="38803-153">**Protocol**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="38803-154">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="38803-154">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="38803-155">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="38803-155">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="38803-156">限定詞： [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (15) 、 **WmiDataId** (8) 、 **InterfaceVersion** (1) 、 **InterfaceRevision** (0) </span><span class="sxs-lookup"><span data-stu-id="38803-156">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (15), **WmiDataId** (8), **InterfaceVersion** (1), **InterfaceRevision** (0)</span></span>
</dt> </dl>

<span data-ttu-id="38803-157">通訊協定字串。</span><span class="sxs-lookup"><span data-stu-id="38803-157">The protocol string.</span></span>

</dd> <dt>

<span data-ttu-id="38803-158">**Server.remoteipaddress**</span><span class="sxs-lookup"><span data-stu-id="38803-158">**RemoteIPAddress**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="38803-159">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="38803-159">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="38803-160">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="38803-160">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="38803-161">限定詞： [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (40) 、 **WmiDataId** (5) 、 **InterfaceVersion** (1) 、 **InterfaceRevision** (0) </span><span class="sxs-lookup"><span data-stu-id="38803-161">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (40), **WmiDataId** (5), **InterfaceVersion** (1), **InterfaceRevision** (0)</span></span>
</dt> </dl>

<span data-ttu-id="38803-162">遠端 IP 位址。</span><span class="sxs-lookup"><span data-stu-id="38803-162">The remote IP address.</span></span>

</dd> <dt>

<span data-ttu-id="38803-163">**Server.remoteport**</span><span class="sxs-lookup"><span data-stu-id="38803-163">**RemotePort**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="38803-164">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="38803-164">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="38803-165">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="38803-165">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="38803-166">限定詞： [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (21) 、 **WmiDataId** (7) 、 **InterfaceVersion** (1) 、 **InterfaceRevision** (0) </span><span class="sxs-lookup"><span data-stu-id="38803-166">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (21), **WmiDataId** (7), **InterfaceVersion** (1), **InterfaceRevision** (0)</span></span>
</dt> </dl>

<span data-ttu-id="38803-167">遠端埠範圍。</span><span class="sxs-lookup"><span data-stu-id="38803-167">The remote port range.</span></span>

</dd> <dt>

<span data-ttu-id="38803-168">**狀態**</span><span class="sxs-lookup"><span data-stu-id="38803-168">**Stateful**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="38803-169">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="38803-169">Data type: **Boolean**</span></span>
</dt> <dt>

<span data-ttu-id="38803-170">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="38803-170">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="38803-171">限定詞： **WmiDataId** (10) 、 **InterfaceVersion** (1) 、 **InterfaceRevision** (0) </span><span class="sxs-lookup"><span data-stu-id="38803-171">Qualifiers: **WmiDataId** (10), **InterfaceVersion** (1), **InterfaceRevision** (0)</span></span>
</dt> </dl>

<span data-ttu-id="38803-172">指出擴充的 ACL 是具狀態或無狀態。</span><span class="sxs-lookup"><span data-stu-id="38803-172">Indicates if the extended ACL is stateful or stateless.</span></span>

</dd> <dt>

<span data-ttu-id="38803-173">**Weight**</span><span class="sxs-lookup"><span data-stu-id="38803-173">**Weight**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="38803-174">資料類型： **Uint16**</span><span class="sxs-lookup"><span data-stu-id="38803-174">Data type: **Uint16**</span></span>
</dt> <dt>

<span data-ttu-id="38803-175">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="38803-175">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="38803-176">限定詞： **WmiDataId** (9) 、 **InterfaceVersion** (1) 、 **InterfaceRevision** (0) </span><span class="sxs-lookup"><span data-stu-id="38803-176">Qualifiers: **WmiDataId** (9), **InterfaceVersion** (1), **InterfaceRevision** (0)</span></span>
</dt> </dl>

<span data-ttu-id="38803-177">套用至擴充 ACL 的加權。</span><span class="sxs-lookup"><span data-stu-id="38803-177">The weight applied to the extended ACL.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="38803-178">規格需求</span><span class="sxs-lookup"><span data-stu-id="38803-178">Requirements</span></span>



| <span data-ttu-id="38803-179">需求</span><span class="sxs-lookup"><span data-stu-id="38803-179">Requirement</span></span> | <span data-ttu-id="38803-180">值</span><span class="sxs-lookup"><span data-stu-id="38803-180">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="38803-181">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="38803-181">Minimum supported client</span></span><br/> | <span data-ttu-id="38803-182">Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="38803-182">Windows 8.1</span></span><br/>                                                                                  |
| <span data-ttu-id="38803-183">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="38803-183">Minimum supported server</span></span><br/> | <span data-ttu-id="38803-184">Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="38803-184">Windows Server 2012 R2</span></span><br/>                                                                       |
| <span data-ttu-id="38803-185">命名空間</span><span class="sxs-lookup"><span data-stu-id="38803-185">Namespace</span></span><br/>                | <span data-ttu-id="38803-186">根 \\ 虛擬化 \\ v2</span><span class="sxs-lookup"><span data-stu-id="38803-186">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="38803-187">MOF</span><span class="sxs-lookup"><span data-stu-id="38803-187">MOF</span></span><br/>                      | <dl> <span data-ttu-id="38803-188"><dt>WindowsVirtualization。</dt></span><span class="sxs-lookup"><span data-stu-id="38803-188"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="38803-189">DLL</span><span class="sxs-lookup"><span data-stu-id="38803-189">DLL</span></span><br/>                      | <dl> <span data-ttu-id="38803-190"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="38803-190"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="38803-191">另請參閱</span><span class="sxs-lookup"><span data-stu-id="38803-191">See also</span></span>

<dl> <dt>

[<span data-ttu-id="38803-192">**Msvm \_ EthernetSwitchPortFeatureSettingData**</span><span class="sxs-lookup"><span data-stu-id="38803-192">**Msvm\_EthernetSwitchPortFeatureSettingData**</span></span>](msvm-ethernetswitchportfeaturesettingdata.md)
</dt> </dl>

 

