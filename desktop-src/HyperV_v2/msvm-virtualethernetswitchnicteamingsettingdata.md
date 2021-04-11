---
description: 代表交換器 nic 小組設定。
ms.assetid: 7a48bdae-1953-4011-aaa8-1e3ca73494ff
title: Msvm_VirtualEthernetSwitchNicTeamingSettingData 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualEthernetSwitchNicTeamingSettingData
- Msvm_VirtualEthernetSwitchNicTeamingSettingData.TeamingMode
- Msvm_VirtualEthernetSwitchNicTeamingSettingData.LoadBalancingAlgorithm
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 45f306f9ddb388ef4e8124d7ab2c8dd125a62e01
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103695875"
---
# <a name="msvm_virtualethernetswitchnicteamingsettingdata-class"></a><span data-ttu-id="4aabc-103">Msvm \_ VirtualEthernetSwitchNicTeamingSettingData 類別</span><span class="sxs-lookup"><span data-stu-id="4aabc-103">Msvm\_VirtualEthernetSwitchNicTeamingSettingData class</span></span>

<span data-ttu-id="4aabc-104">代表交換器 nic 小組設定。</span><span class="sxs-lookup"><span data-stu-id="4aabc-104">Represents the switch nic teaming settings.</span></span>

<span data-ttu-id="4aabc-105">下列語法已經過受管理物件格式 (MOF) 程式碼簡化，並包含所有已繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="4aabc-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="4aabc-106">語法</span><span class="sxs-lookup"><span data-stu-id="4aabc-106">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), UUID("17AD26F1-DD6F-4ED9-BD2F-3750ADE6B68B"), ExtensionId("11EC6134-128A-4A23-B12F-164184B48348"), InterfaceVersion("1"), InterfaceRevision("0"), DisplayName("Ethernet Switch Nic Teaming Settings"), AMENDMENT]
class Msvm_VirtualEthernetSwitchNicTeamingSettingData : Msvm_EthernetSwitchFeatureSettingData
{
  UINT32 TeamingMode = 0;
  UINT32 LoadBalancingAlgorithm = 5;
};
```

## <a name="members"></a><span data-ttu-id="4aabc-107">成員</span><span class="sxs-lookup"><span data-stu-id="4aabc-107">Members</span></span>

<span data-ttu-id="4aabc-108">**Msvm \_ VirtualEthernetSwitchNicTeamingSettingData** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="4aabc-108">The **Msvm\_VirtualEthernetSwitchNicTeamingSettingData** class has these types of members:</span></span>

-   [<span data-ttu-id="4aabc-109">屬性</span><span class="sxs-lookup"><span data-stu-id="4aabc-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="4aabc-110">屬性</span><span class="sxs-lookup"><span data-stu-id="4aabc-110">Properties</span></span>

<span data-ttu-id="4aabc-111">**Msvm \_ VirtualEthernetSwitchNicTeamingSettingData** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="4aabc-111">The **Msvm\_VirtualEthernetSwitchNicTeamingSettingData** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="4aabc-112">**LoadBalancingAlgorithm**</span><span class="sxs-lookup"><span data-stu-id="4aabc-112">**LoadBalancingAlgorithm**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4aabc-113">資料類型： **UINT32**</span><span class="sxs-lookup"><span data-stu-id="4aabc-113">Data type: **UINT32**</span></span>
</dt> <dt>

<span data-ttu-id="4aabc-114">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="4aabc-114">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="4aabc-115">限定詞： **WmiDataId** (2) 、 **InterfaceVersion** (1) 、 **InterfaceRevision** (0) </span><span class="sxs-lookup"><span data-stu-id="4aabc-115">Qualifiers: **WmiDataId** (2), **InterfaceVersion** (1), **InterfaceRevision** (0)</span></span>
</dt> </dl>

<span data-ttu-id="4aabc-116">負載平衡演算法。</span><span class="sxs-lookup"><span data-stu-id="4aabc-116">The load balancing algorithm.</span></span>

</dd> <dt>

<span data-ttu-id="4aabc-117">**TeamingMode**</span><span class="sxs-lookup"><span data-stu-id="4aabc-117">**TeamingMode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4aabc-118">資料類型： **UINT32**</span><span class="sxs-lookup"><span data-stu-id="4aabc-118">Data type: **UINT32**</span></span>
</dt> <dt>

<span data-ttu-id="4aabc-119">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="4aabc-119">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="4aabc-120">限定詞： **WmiDataId** (1) 、 **InterfaceVersion** (1) 、 **InterfaceRevision** (0) </span><span class="sxs-lookup"><span data-stu-id="4aabc-120">Qualifiers: **WmiDataId** (1), **InterfaceVersion** (1), **InterfaceRevision** (0)</span></span>
</dt> </dl>

<span data-ttu-id="4aabc-121">小組模式。</span><span class="sxs-lookup"><span data-stu-id="4aabc-121">The teaming mode.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="4aabc-122">規格需求</span><span class="sxs-lookup"><span data-stu-id="4aabc-122">Requirements</span></span>



| <span data-ttu-id="4aabc-123">需求</span><span class="sxs-lookup"><span data-stu-id="4aabc-123">Requirement</span></span> | <span data-ttu-id="4aabc-124">值</span><span class="sxs-lookup"><span data-stu-id="4aabc-124">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4aabc-125">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="4aabc-125">Minimum supported client</span></span><br/> | <span data-ttu-id="4aabc-126">\[僅 Windows 10 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="4aabc-126">Windows 10 \[desktop apps only\]</span></span><br/>                                                             |
| <span data-ttu-id="4aabc-127">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="4aabc-127">Minimum supported server</span></span><br/> | <span data-ttu-id="4aabc-128">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="4aabc-128">Windows Server 2016</span></span><br/>                                                                          |
| <span data-ttu-id="4aabc-129">命名空間</span><span class="sxs-lookup"><span data-stu-id="4aabc-129">Namespace</span></span><br/>                | <span data-ttu-id="4aabc-130">根 \\ 虛擬化 \\ v2</span><span class="sxs-lookup"><span data-stu-id="4aabc-130">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="4aabc-131">MOF</span><span class="sxs-lookup"><span data-stu-id="4aabc-131">MOF</span></span><br/>                      | <dl> <span data-ttu-id="4aabc-132"><dt>WindowsVirtualization。</dt></span><span class="sxs-lookup"><span data-stu-id="4aabc-132"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="4aabc-133">DLL</span><span class="sxs-lookup"><span data-stu-id="4aabc-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="4aabc-134"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="4aabc-134"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="4aabc-135">另請參閱</span><span class="sxs-lookup"><span data-stu-id="4aabc-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4aabc-136">**Msvm \_ EthernetSwitchFeatureSettingData**</span><span class="sxs-lookup"><span data-stu-id="4aabc-136">**Msvm\_EthernetSwitchFeatureSettingData**</span></span>](msvm-ethernetswitchfeaturesettingdata.md)
</dt> </dl>

 

 




