---
description: 來賓服務介面元件與來賓服務資源之間的關聯類別。
ms.assetid: 4c16c3ab-4137-40ab-be2e-f385d8e36a41
title: Msvm_GuestServiceInterfaceSettingDataComponent 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_GuestServiceInterfaceSettingDataComponent
- Msvm_GuestServiceInterfaceSettingDataComponent.GroupComponent
- Msvm_GuestServiceInterfaceSettingDataComponent.PartComponent
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 988975fea1fd519a5e3917faeb73d345334d74b3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104191508"
---
# <a name="msvm_guestserviceinterfacesettingdatacomponent-class"></a><span data-ttu-id="36066-103">Msvm \_ GuestServiceInterfaceSettingDataComponent 類別</span><span class="sxs-lookup"><span data-stu-id="36066-103">Msvm\_GuestServiceInterfaceSettingDataComponent class</span></span>

<span data-ttu-id="36066-104">來賓服務介面元件與來賓服務資源之間的關聯類別。</span><span class="sxs-lookup"><span data-stu-id="36066-104">Association class between a guest service interface component and the guest service resource.</span></span>

<span data-ttu-id="36066-105">下列語法已經過受管理物件格式 (MOF) 程式碼簡化，並包含所有已繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="36066-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="36066-106">語法</span><span class="sxs-lookup"><span data-stu-id="36066-106">Syntax</span></span>

``` syntax
[Association, Aggregation, Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_GuestServiceInterfaceSettingDataComponent : CIM_Component
{
  Msvm_GuestServiceInterfaceComponentSettingData REF GroupComponent;
  CIM_SettingData                                REF PartComponent;
};
```

## <a name="members"></a><span data-ttu-id="36066-107">成員</span><span class="sxs-lookup"><span data-stu-id="36066-107">Members</span></span>

<span data-ttu-id="36066-108">**Msvm \_ GuestServiceInterfaceSettingDataComponent** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="36066-108">The **Msvm\_GuestServiceInterfaceSettingDataComponent** class has these types of members:</span></span>

-   [<span data-ttu-id="36066-109">屬性</span><span class="sxs-lookup"><span data-stu-id="36066-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="36066-110">屬性</span><span class="sxs-lookup"><span data-stu-id="36066-110">Properties</span></span>

<span data-ttu-id="36066-111">**Msvm \_ GuestServiceInterfaceSettingDataComponent** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="36066-111">The **Msvm\_GuestServiceInterfaceSettingDataComponent** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="36066-112">**GroupComponent**</span><span class="sxs-lookup"><span data-stu-id="36066-112">**GroupComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="36066-113">資料類型： **Msvm \_ GuestServiceInterfaceComponentSettingData**</span><span class="sxs-lookup"><span data-stu-id="36066-113">Data type: **Msvm\_GuestServiceInterfaceComponentSettingData**</span></span>
</dt> <dt>

<span data-ttu-id="36066-114">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="36066-114">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="36066-115">限定詞： [**Key**](/windows/desktop/WmiSdk/key-qualifier)、 [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ( "GroupComponent" ) </span><span class="sxs-lookup"><span data-stu-id="36066-115">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("GroupComponent")</span></span>
</dt> </dl>

<span data-ttu-id="36066-116">參考來賓服務介面元件的 [**Msvm \_ GuestServiceInterfaceComponentSettingData**](msvm-guestserviceinterfacecomponentsettingdata.md) 。</span><span class="sxs-lookup"><span data-stu-id="36066-116">A [**Msvm\_GuestServiceInterfaceComponentSettingData**](msvm-guestserviceinterfacecomponentsettingdata.md) referencing the guest service interface component.</span></span>

</dd> <dt>

<span data-ttu-id="36066-117">**PartComponent**</span><span class="sxs-lookup"><span data-stu-id="36066-117">**PartComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="36066-118">資料類型： **CIM \_ SettingData**</span><span class="sxs-lookup"><span data-stu-id="36066-118">Data type: **CIM\_SettingData**</span></span>
</dt> <dt>

<span data-ttu-id="36066-119">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="36066-119">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="36066-120">限定詞： [**Key**](/windows/desktop/WmiSdk/key-qualifier)、 [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ( "PartComponent" ) </span><span class="sxs-lookup"><span data-stu-id="36066-120">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("PartComponent")</span></span>
</dt> </dl>

<span data-ttu-id="36066-121">參考來賓服務資源的 [**CIM \_ SettingData**](cim-settingdata.md) 。</span><span class="sxs-lookup"><span data-stu-id="36066-121">A [**CIM\_SettingData**](cim-settingdata.md) that references the guest service resource.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="36066-122">規格需求</span><span class="sxs-lookup"><span data-stu-id="36066-122">Requirements</span></span>



| <span data-ttu-id="36066-123">需求</span><span class="sxs-lookup"><span data-stu-id="36066-123">Requirement</span></span> | <span data-ttu-id="36066-124">值</span><span class="sxs-lookup"><span data-stu-id="36066-124">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="36066-125">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="36066-125">Minimum supported client</span></span><br/> | <span data-ttu-id="36066-126">\[僅 Windows 10 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="36066-126">Windows 10 \[desktop apps only\]</span></span><br/>                                                             |
| <span data-ttu-id="36066-127">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="36066-127">Minimum supported server</span></span><br/> | <span data-ttu-id="36066-128">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="36066-128">Windows Server 2016</span></span><br/>                                                                          |
| <span data-ttu-id="36066-129">命名空間</span><span class="sxs-lookup"><span data-stu-id="36066-129">Namespace</span></span><br/>                | <span data-ttu-id="36066-130">根 \\ 虛擬化 \\ v2</span><span class="sxs-lookup"><span data-stu-id="36066-130">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="36066-131">MOF</span><span class="sxs-lookup"><span data-stu-id="36066-131">MOF</span></span><br/>                      | <dl> <span data-ttu-id="36066-132"><dt>WindowsVirtualization。</dt></span><span class="sxs-lookup"><span data-stu-id="36066-132"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="36066-133">DLL</span><span class="sxs-lookup"><span data-stu-id="36066-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="36066-134"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="36066-134"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="36066-135">另請參閱</span><span class="sxs-lookup"><span data-stu-id="36066-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="36066-136">**CIM \_ 元件**</span><span class="sxs-lookup"><span data-stu-id="36066-136">**CIM\_Component**</span></span>](cim-component.md)
</dt> </dl>

 

