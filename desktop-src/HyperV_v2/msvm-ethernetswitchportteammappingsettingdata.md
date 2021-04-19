---
description: 表示埠小組對應功能設定資料。
ms.assetid: 7c9a392d-c95e-4b0d-8201-e50adabd21b2
title: Msvm_EthernetSwitchPortTeamMappingSettingData 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_EthernetSwitchPortTeamMappingSettingData
- Msvm_EthernetSwitchPortTeamMappingSettingData.NetAdapterName
- Msvm_EthernetSwitchPortTeamMappingSettingData.NetAdapterDeviceId
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 3f0d7385499dcdf6e84c361de03950a4e78be0a9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106982118"
---
# <a name="msvm_ethernetswitchportteammappingsettingdata-class"></a><span data-ttu-id="77d77-103">Msvm \_ EthernetSwitchPortTeamMappingSettingData 類別</span><span class="sxs-lookup"><span data-stu-id="77d77-103">Msvm\_EthernetSwitchPortTeamMappingSettingData class</span></span>

<span data-ttu-id="77d77-104">表示埠小組對應功能設定資料。</span><span class="sxs-lookup"><span data-stu-id="77d77-104">Represents the port team mapping feature setting data.</span></span>

<span data-ttu-id="77d77-105">下列語法已經過受管理物件格式 (MOF) 程式碼簡化，並包含所有已繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="77d77-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="77d77-106">語法</span><span class="sxs-lookup"><span data-stu-id="77d77-106">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), UUID("8D45D4BD-8C18-435C-98A7-D632A7C618FF"), ExtensionId("11EC6134-128A-4A23-B12F-164184B48348"), InterfaceVersion("1"), InterfaceRevision("0"), DisplayName("Ethernet Switch Port Team Mapping Settings"), AMENDMENT]
class Msvm_EthernetSwitchPortTeamMappingSettingData : Msvm_EthernetSwitchPortFeatureSettingData
{
  string NetAdapterName = "";
  string NetAdapterDeviceId = "";
};
```

## <a name="members"></a><span data-ttu-id="77d77-107">成員</span><span class="sxs-lookup"><span data-stu-id="77d77-107">Members</span></span>

<span data-ttu-id="77d77-108">**Msvm \_ EthernetSwitchPortTeamMappingSettingData** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="77d77-108">The **Msvm\_EthernetSwitchPortTeamMappingSettingData** class has these types of members:</span></span>

-   [<span data-ttu-id="77d77-109">屬性</span><span class="sxs-lookup"><span data-stu-id="77d77-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="77d77-110">屬性</span><span class="sxs-lookup"><span data-stu-id="77d77-110">Properties</span></span>

<span data-ttu-id="77d77-111">**Msvm \_ EthernetSwitchPortTeamMappingSettingData** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="77d77-111">The **Msvm\_EthernetSwitchPortTeamMappingSettingData** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="77d77-112">**NetAdapterDeviceId**</span><span class="sxs-lookup"><span data-stu-id="77d77-112">**NetAdapterDeviceId**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="77d77-113">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="77d77-113">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="77d77-114">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="77d77-114">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="77d77-115">限定詞： [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (127) 、 **WmiDataId** (2) 、 **InterfaceVersion** (1) 、 **InterfaceRevision** (0) </span><span class="sxs-lookup"><span data-stu-id="77d77-115">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (127), **WmiDataId** (2), **InterfaceVersion** (1), **InterfaceRevision** (0)</span></span>
</dt> </dl>

<span data-ttu-id="77d77-116">慣用對應之實體介面卡的裝置識別碼。</span><span class="sxs-lookup"><span data-stu-id="77d77-116">Device ID of the preferred mapped physical adapter.</span></span>

</dd> <dt>

<span data-ttu-id="77d77-117">**NetAdapterName**</span><span class="sxs-lookup"><span data-stu-id="77d77-117">**NetAdapterName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="77d77-118">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="77d77-118">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="77d77-119">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="77d77-119">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="77d77-120">限定詞： [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (127) 、 **WmiDataId** (1) 、 **InterfaceVersion** (1) 、 **InterfaceRevision** (0) </span><span class="sxs-lookup"><span data-stu-id="77d77-120">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (127), **WmiDataId** (1), **InterfaceVersion** (1), **InterfaceRevision** (0)</span></span>
</dt> </dl>

<span data-ttu-id="77d77-121">慣用對應實體介面卡的名稱。</span><span class="sxs-lookup"><span data-stu-id="77d77-121">Name of the preferred mapped physical adapter.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="77d77-122">規格需求</span><span class="sxs-lookup"><span data-stu-id="77d77-122">Requirements</span></span>



| <span data-ttu-id="77d77-123">需求</span><span class="sxs-lookup"><span data-stu-id="77d77-123">Requirement</span></span> | <span data-ttu-id="77d77-124">值</span><span class="sxs-lookup"><span data-stu-id="77d77-124">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="77d77-125">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="77d77-125">Minimum supported client</span></span><br/> | <span data-ttu-id="77d77-126">Windows 10， \[ 僅限1703版桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="77d77-126">Windows 10, version 1703 \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="77d77-127">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="77d77-127">Minimum supported server</span></span><br/> | <span data-ttu-id="77d77-128">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="77d77-128">Windows Server 2016</span></span><br/>                                                                          |
| <span data-ttu-id="77d77-129">命名空間</span><span class="sxs-lookup"><span data-stu-id="77d77-129">Namespace</span></span><br/>                | <span data-ttu-id="77d77-130">根 \\ 虛擬化 \\ v2</span><span class="sxs-lookup"><span data-stu-id="77d77-130">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="77d77-131">MOF</span><span class="sxs-lookup"><span data-stu-id="77d77-131">MOF</span></span><br/>                      | <dl> <span data-ttu-id="77d77-132"><dt>WindowsVirtualization。</dt></span><span class="sxs-lookup"><span data-stu-id="77d77-132"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="77d77-133">DLL</span><span class="sxs-lookup"><span data-stu-id="77d77-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="77d77-134"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="77d77-134"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="77d77-135">另請參閱</span><span class="sxs-lookup"><span data-stu-id="77d77-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="77d77-136">**Msvm \_ EthernetSwitchPortFeatureSettingData**</span><span class="sxs-lookup"><span data-stu-id="77d77-136">**Msvm\_EthernetSwitchPortFeatureSettingData**</span></span>](msvm-ethernetswitchportfeaturesettingdata.md)
</dt> </dl>

 

