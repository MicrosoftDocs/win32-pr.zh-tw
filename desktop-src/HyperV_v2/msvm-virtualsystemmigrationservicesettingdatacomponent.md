---
description: 用來表示虛擬系統移轉服務之虛擬系統移轉網路設定的關聯。
ms.assetid: 5704dce7-1db3-4049-8c61-58bfa9596766
title: Msvm_VirtualSystemMigrationServiceSettingDataComponent 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualSystemMigrationServiceSettingDataComponent
- Msvm_VirtualSystemMigrationServiceSettingDataComponent.GroupComponent
- Msvm_VirtualSystemMigrationServiceSettingDataComponent.PartComponent
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 1ba69ebd6cfd50b30923db2ecc87e7e5aeebcaa5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106997482"
---
# <a name="msvm_virtualsystemmigrationservicesettingdatacomponent-class"></a><span data-ttu-id="38f4c-103">Msvm \_ VirtualSystemMigrationServiceSettingDataComponent 類別</span><span class="sxs-lookup"><span data-stu-id="38f4c-103">Msvm\_VirtualSystemMigrationServiceSettingDataComponent class</span></span>

<span data-ttu-id="38f4c-104">用來表示虛擬系統移轉服務之虛擬系統移轉網路設定的關聯。</span><span class="sxs-lookup"><span data-stu-id="38f4c-104">An association used to represent virtual system migration network settings of the virtual system migration service.</span></span>

<span data-ttu-id="38f4c-105">下列語法已簡化受控物件格式 (MOF) 程式碼，並且包含所有繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="38f4c-105">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="38f4c-106">語法</span><span class="sxs-lookup"><span data-stu-id="38f4c-106">Syntax</span></span>

``` syntax
[Association, Aggregation, Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_VirtualSystemMigrationServiceSettingDataComponent : CIM_Component
{
  Msvm_VirtualSystemMigrationServiceSettingData REF GroupComponent;
  Msvm_VirtualSystemMigrationNetworkSettingData REF PartComponent;
};
```

## <a name="members"></a><span data-ttu-id="38f4c-107">成員</span><span class="sxs-lookup"><span data-stu-id="38f4c-107">Members</span></span>

<span data-ttu-id="38f4c-108">**Msvm \_ VirtualSystemMigrationServiceSettingDataComponent** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="38f4c-108">The **Msvm\_VirtualSystemMigrationServiceSettingDataComponent** class has these types of members:</span></span>

-   [<span data-ttu-id="38f4c-109">屬性</span><span class="sxs-lookup"><span data-stu-id="38f4c-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="38f4c-110">屬性</span><span class="sxs-lookup"><span data-stu-id="38f4c-110">Properties</span></span>

<span data-ttu-id="38f4c-111">**Msvm \_ VirtualSystemMigrationServiceSettingDataComponent** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="38f4c-111">The **Msvm\_VirtualSystemMigrationServiceSettingDataComponent** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="38f4c-112">**GroupComponent**</span><span class="sxs-lookup"><span data-stu-id="38f4c-112">**GroupComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="38f4c-113">資料類型： **Msvm \_ VirtualSystemMigrationServiceSettingData**</span><span class="sxs-lookup"><span data-stu-id="38f4c-113">Data type: **Msvm\_VirtualSystemMigrationServiceSettingData**</span></span>
</dt> <dt>

<span data-ttu-id="38f4c-114">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="38f4c-114">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="38f4c-115">限定詞：索引 [**鍵**](/windows/desktop/WmiSdk/key-qualifier)、覆 [**寫**](/windows/desktop/WmiSdk/standard-qualifiers) ( "GroupComponent" ) 、 [**匯總**](/windows/desktop/WmiSdk/standard-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="38f4c-115">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("GroupComponent"), [**Aggregate**](/windows/desktop/WmiSdk/standard-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="38f4c-116">代表遷移服務設定之 [**Msvm \_ VirtualSystemMigrationServiceSettingData**](msvm-virtualsystemmigrationservicesettingdata.md) 類別實例的參考。</span><span class="sxs-lookup"><span data-stu-id="38f4c-116">A reference to an instance of the [**Msvm\_VirtualSystemMigrationServiceSettingData**](msvm-virtualsystemmigrationservicesettingdata.md) class that represents the migration service settings.</span></span>

</dd> <dt>

<span data-ttu-id="38f4c-117">**PartComponent**</span><span class="sxs-lookup"><span data-stu-id="38f4c-117">**PartComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="38f4c-118">資料類型： **Msvm \_ VirtualSystemMigrationNetworkSettingData**</span><span class="sxs-lookup"><span data-stu-id="38f4c-118">Data type: **Msvm\_VirtualSystemMigrationNetworkSettingData**</span></span>
</dt> <dt>

<span data-ttu-id="38f4c-119">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="38f4c-119">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="38f4c-120">限定詞： [**Key**](/windows/desktop/WmiSdk/key-qualifier)、 [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ( "PartComponent" ) </span><span class="sxs-lookup"><span data-stu-id="38f4c-120">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("PartComponent")</span></span>
</dt> </dl>

<span data-ttu-id="38f4c-121">代表遷移網路設定之 [**Msvm \_ VirtualSystemMigrationNetworkSettingData**](msvm-virtualsystemmigrationnetworksettingdata.md) 類別實例的參考。</span><span class="sxs-lookup"><span data-stu-id="38f4c-121">A reference to an instance of the [**Msvm\_VirtualSystemMigrationNetworkSettingData**](msvm-virtualsystemmigrationnetworksettingdata.md) class that represents the migration network settings.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="38f4c-122">規格需求</span><span class="sxs-lookup"><span data-stu-id="38f4c-122">Requirements</span></span>



| <span data-ttu-id="38f4c-123">需求</span><span class="sxs-lookup"><span data-stu-id="38f4c-123">Requirement</span></span> | <span data-ttu-id="38f4c-124">值</span><span class="sxs-lookup"><span data-stu-id="38f4c-124">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="38f4c-125">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="38f4c-125">Minimum supported client</span></span><br/> | <span data-ttu-id="38f4c-126">\[僅 Windows 8 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="38f4c-126">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="38f4c-127">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="38f4c-127">Minimum supported server</span></span><br/> | <span data-ttu-id="38f4c-128">僅限 Windows Server 2012 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="38f4c-128">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="38f4c-129">命名空間</span><span class="sxs-lookup"><span data-stu-id="38f4c-129">Namespace</span></span><br/>                | <span data-ttu-id="38f4c-130">根 \\ 虛擬化 \\ V2</span><span class="sxs-lookup"><span data-stu-id="38f4c-130">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="38f4c-131">MOF</span><span class="sxs-lookup"><span data-stu-id="38f4c-131">MOF</span></span><br/>                      | <dl> <span data-ttu-id="38f4c-132"><dt>WindowsVirtualization。</dt></span><span class="sxs-lookup"><span data-stu-id="38f4c-132"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="38f4c-133">DLL</span><span class="sxs-lookup"><span data-stu-id="38f4c-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="38f4c-134"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="38f4c-134"><dt>Vmms.exe</dt></span></span> </dl>                     |



 

