---
description: 表示 VLAN 端點的設定資料。
ms.assetid: 5ef3cc55-cf27-40b4-9e94-2e2b42ca41c5
title: CIM_VLANEndpointSettingData 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_VLANEndpointSettingData
- CIM_VLANEndpointSettingData.PruneEligibleVLANList
- CIM_VLANEndpointSettingData.NativeVLAN
- CIM_VLANEndpointSettingData.DefaultVLAN
- CIM_VLANEndpointSettingData.TrunkedVLANList
- CIM_VLANEndpointSettingData.AccessVLAN
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: a510c4195c538ab9735e7544acec2c88beeaa1de
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103853164"
---
# <a name="cim_vlanendpointsettingdata-class"></a><span data-ttu-id="5638f-103">CIM \_ VLANEndpointSettingData 類別</span><span class="sxs-lookup"><span data-stu-id="5638f-103">CIM\_VLANEndpointSettingData class</span></span>

<span data-ttu-id="5638f-104">表示 VLAN 端點的設定資料。</span><span class="sxs-lookup"><span data-stu-id="5638f-104">Represents configuration data for a VLAN endpoint.</span></span>

## <a name="syntax"></a><span data-ttu-id="5638f-105">語法</span><span class="sxs-lookup"><span data-stu-id="5638f-105">Syntax</span></span>

``` syntax
[Experimental, Abstract, Version("2.11.0"), UMLPackagePath("CIM::Network::VLAN")]
class CIM_VLANEndpointSettingData : CIM_SettingData
{
  uint16 PruneEligibleVLANList[];
  uint16 NativeVLAN;
  uint16 DefaultVLAN;
  uint16 TrunkedVLANList[];
  uint16 AccessVLAN;
};
```

## <a name="members"></a><span data-ttu-id="5638f-106">成員</span><span class="sxs-lookup"><span data-stu-id="5638f-106">Members</span></span>

<span data-ttu-id="5638f-107">**CIM \_ VLANEndpointSettingData** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="5638f-107">The **CIM\_VLANEndpointSettingData** class has these types of members:</span></span>

-   [<span data-ttu-id="5638f-108">屬性</span><span class="sxs-lookup"><span data-stu-id="5638f-108">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="5638f-109">屬性</span><span class="sxs-lookup"><span data-stu-id="5638f-109">Properties</span></span>

<span data-ttu-id="5638f-110">**CIM \_ VLANEndpointSettingData** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="5638f-110">The **CIM\_VLANEndpointSettingData** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="5638f-111">**AccessVLAN**</span><span class="sxs-lookup"><span data-stu-id="5638f-111">**AccessVLAN**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5638f-112">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="5638f-112">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="5638f-113">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="5638f-113">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="5638f-114">限定詞： [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ( "[**CIM \_ VLANEndpoint**](cim-vlanendpoint.md).**OperationalEndpointMode**") </span><span class="sxs-lookup"><span data-stu-id="5638f-114">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_VLANEndpoint**](cim-vlanendpoint.md).**OperationalEndpointMode**")</span></span>
</dt> </dl>

<span data-ttu-id="5638f-115">端點的存取 VLAN。</span><span class="sxs-lookup"><span data-stu-id="5638f-115">The access VLAN for the endpoint.</span></span>

</dd> <dt>

<span data-ttu-id="5638f-116">**DefaultVLAN**</span><span class="sxs-lookup"><span data-stu-id="5638f-116">**DefaultVLAN**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5638f-117">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="5638f-117">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="5638f-118">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="5638f-118">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5638f-119">限定詞： [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ( "[**CIM \_ VLANEndpoint**](cim-vlanendpoint.md).**OperationalEndpointMode**") </span><span class="sxs-lookup"><span data-stu-id="5638f-119">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_VLANEndpoint**](cim-vlanendpoint.md).**OperationalEndpointMode**")</span></span>
</dt> </dl>

<span data-ttu-id="5638f-120">主幹端點上原生 VLAN 的預設值。</span><span class="sxs-lookup"><span data-stu-id="5638f-120">The default value for the native VLAN on the trunk endpoint.</span></span>

> [!Note]  
> <span data-ttu-id="5638f-121">只有當 VLAN 端點在 **OperationalEndpointMode** 屬性中指定的中繼模式下運作時，才會使用此屬性。</span><span class="sxs-lookup"><span data-stu-id="5638f-121">This property is only used when the VLAN endpoint is operating in trunking mode, which is specified in the **OperationalEndpointMode** property.</span></span>

 

</dd> <dt>

<span data-ttu-id="5638f-122">**NativeVLAN**</span><span class="sxs-lookup"><span data-stu-id="5638f-122">**NativeVLAN**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5638f-123">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="5638f-123">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="5638f-124">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="5638f-124">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="5638f-125">限定詞： [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ( "[**CIM \_ VLANEndpoint**](cim-vlanendpoint.md).**OperationalEndpointMode**") </span><span class="sxs-lookup"><span data-stu-id="5638f-125">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_VLANEndpoint**](cim-vlanendpoint.md).**OperationalEndpointMode**")</span></span>
</dt> </dl>

<span data-ttu-id="5638f-126">用來標記在主幹端點上收到之未標記流量的 VLAN ID。</span><span class="sxs-lookup"><span data-stu-id="5638f-126">The VLAN ID that is used to tag untagged traffic received on the trunk endpoint.</span></span>

> [!Note]  
> <span data-ttu-id="5638f-127">只有當 VLAN 端點在 **SwitchEndpointMode** 屬性中指定的中繼模式下運作時，才會使用此屬性。</span><span class="sxs-lookup"><span data-stu-id="5638f-127">This property is only used when the VLAN endpoint is operating in trunking mode, which is specified in the **SwitchEndpointMode** property.</span></span>

 

</dd> <dt>

<span data-ttu-id="5638f-128">**PruneEligibleVLANList**</span><span class="sxs-lookup"><span data-stu-id="5638f-128">**PruneEligibleVLANList**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5638f-129">資料類型： **uint16** 陣列</span><span class="sxs-lookup"><span data-stu-id="5638f-129">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="5638f-130">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="5638f-130">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="5638f-131">限定詞： [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ( "[**CIM \_ VLANEndpoint**](cim-vlanendpoint.md).**OperationalEndpointMode**") </span><span class="sxs-lookup"><span data-stu-id="5638f-131">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_VLANEndpoint**](cim-vlanendpoint.md).**OperationalEndpointMode**")</span></span>
</dt> </dl>

<span data-ttu-id="5638f-132">陣列，包含系統可能會從主幹端點移除的 Vlan 識別碼。</span><span class="sxs-lookup"><span data-stu-id="5638f-132">An array that contains IDs of VLANs that the system may remove from the trunk endpoint.</span></span>

> [!Note]  
> <span data-ttu-id="5638f-133">只有當 VLAN 端點在 **OperationalEndpointMode** 屬性中指定的中繼模式下運作時，才會使用此屬性。</span><span class="sxs-lookup"><span data-stu-id="5638f-133">This property is only used when the VLAN endpoint is operating in trunking mode, which is specified in the **OperationalEndpointMode** property.</span></span>

 

</dd> <dt>

<span data-ttu-id="5638f-134">**TrunkedVLANList**</span><span class="sxs-lookup"><span data-stu-id="5638f-134">**TrunkedVLANList**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5638f-135">資料類型： **uint16** 陣列</span><span class="sxs-lookup"><span data-stu-id="5638f-135">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="5638f-136">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="5638f-136">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="5638f-137">限定詞： [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ( "[**CIM \_ VLANEndpoint**](cim-vlanendpoint.md).**OperationalEndpointMode**") </span><span class="sxs-lookup"><span data-stu-id="5638f-137">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_VLANEndpoint**](cim-vlanendpoint.md).**OperationalEndpointMode**")</span></span>
</dt> </dl>

<span data-ttu-id="5638f-138">陣列，其中包含已啟用中繼之 VLAN 端點的識別碼。</span><span class="sxs-lookup"><span data-stu-id="5638f-138">An array that contains IDs of VLAN endpoints with trunking enabled.</span></span>

> [!Note]  
> <span data-ttu-id="5638f-139">只有當 VLAN 端點在 **OperationalEndpointMode** 屬性中指定的中繼模式下運作時，才會使用此屬性。</span><span class="sxs-lookup"><span data-stu-id="5638f-139">This property is only used when the VLAN endpoint is operating in trunking mode, which is specified in the **OperationalEndpointMode** property.</span></span>

 

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="5638f-140">規格需求</span><span class="sxs-lookup"><span data-stu-id="5638f-140">Requirements</span></span>



| <span data-ttu-id="5638f-141">需求</span><span class="sxs-lookup"><span data-stu-id="5638f-141">Requirement</span></span> | <span data-ttu-id="5638f-142">值</span><span class="sxs-lookup"><span data-stu-id="5638f-142">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5638f-143">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="5638f-143">Minimum supported client</span></span><br/> | <span data-ttu-id="5638f-144">Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="5638f-144">Windows 8.1</span></span><br/>                                                                                  |
| <span data-ttu-id="5638f-145">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="5638f-145">Minimum supported server</span></span><br/> | <span data-ttu-id="5638f-146">Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="5638f-146">Windows Server 2012 R2</span></span><br/>                                                                       |
| <span data-ttu-id="5638f-147">命名空間</span><span class="sxs-lookup"><span data-stu-id="5638f-147">Namespace</span></span><br/>                | <span data-ttu-id="5638f-148">根 \\ 虛擬化 \\ v2</span><span class="sxs-lookup"><span data-stu-id="5638f-148">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="5638f-149">MOF</span><span class="sxs-lookup"><span data-stu-id="5638f-149">MOF</span></span><br/>                      | <dl> <span data-ttu-id="5638f-150"><dt>WindowsVirtualization。</dt></span><span class="sxs-lookup"><span data-stu-id="5638f-150"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="5638f-151">DLL</span><span class="sxs-lookup"><span data-stu-id="5638f-151">DLL</span></span><br/>                      | <dl> <span data-ttu-id="5638f-152"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="5638f-152"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="5638f-153">另請參閱</span><span class="sxs-lookup"><span data-stu-id="5638f-153">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5638f-154">**CIM \_ SettingData**</span><span class="sxs-lookup"><span data-stu-id="5638f-154">**CIM\_SettingData**</span></span>](cim-settingdata.md)
</dt> </dl>

 

