---
description: 代表來賓通訊服務的設定。
ms.assetid: c36d3002-d43e-4284-b765-2795c941f023
title: Msvm_GuestCommunicationServiceSettingData 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_GuestCommunicationServiceSettingData
- Msvm_GuestCommunicationServiceSettingData.Name
- Msvm_GuestCommunicationServiceSettingData.EnabledStatePolicy
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: c5506689f5b266c428a790774c1fb98a1b0413b2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104113636"
---
# <a name="msvm_guestcommunicationservicesettingdata-class"></a><span data-ttu-id="7317b-103">Msvm \_ GuestCommunicationServiceSettingData 類別</span><span class="sxs-lookup"><span data-stu-id="7317b-103">Msvm\_GuestCommunicationServiceSettingData class</span></span>

<span data-ttu-id="7317b-104">代表來賓通訊服務的設定。</span><span class="sxs-lookup"><span data-stu-id="7317b-104">Represents the settings of the guest communication service.</span></span>

<span data-ttu-id="7317b-105">下列語法已經過受管理物件格式 (MOF) 程式碼簡化，並包含所有已繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="7317b-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="7317b-106">語法</span><span class="sxs-lookup"><span data-stu-id="7317b-106">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_GuestCommunicationServiceSettingData : CIM_SettingData
{
  string Name;
  uint16 EnabledStatePolicy;
};
```

## <a name="members"></a><span data-ttu-id="7317b-107">成員</span><span class="sxs-lookup"><span data-stu-id="7317b-107">Members</span></span>

<span data-ttu-id="7317b-108">**Msvm \_ GuestCommunicationServiceSettingData** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="7317b-108">The **Msvm\_GuestCommunicationServiceSettingData** class has these types of members:</span></span>

-   [<span data-ttu-id="7317b-109">屬性</span><span class="sxs-lookup"><span data-stu-id="7317b-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="7317b-110">屬性</span><span class="sxs-lookup"><span data-stu-id="7317b-110">Properties</span></span>

<span data-ttu-id="7317b-111">**Msvm \_ GuestCommunicationServiceSettingData** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="7317b-111">The **Msvm\_GuestCommunicationServiceSettingData** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="7317b-112">**EnabledStatePolicy**</span><span class="sxs-lookup"><span data-stu-id="7317b-112">**EnabledStatePolicy**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7317b-113">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="7317b-113">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="7317b-114">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="7317b-114">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="7317b-115">EnabledStatePolicy 是一個整數列舉，表示 **Msvm \_ GuestCommunicationServiceSettingData** 的啟用、停用或預設狀態。</span><span class="sxs-lookup"><span data-stu-id="7317b-115">EnabledStatePolicy is an integer enumeration that indicates the enabled, disabled or default state of the **Msvm\_GuestCommunicationServiceSettingData**.</span></span>

<dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="7317b-116"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**已啟用** (2) </span><span class="sxs-lookup"><span data-stu-id="7317b-116"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Enabled** (2)</span></span>


</dt> <dd>

<span data-ttu-id="7317b-117">通訊服務設定為 [已啟用] 狀態。</span><span class="sxs-lookup"><span data-stu-id="7317b-117">The communication service is set to the enabled state.</span></span>

</dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="7317b-118"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**停用** (3) </span><span class="sxs-lookup"><span data-stu-id="7317b-118"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabled** (3)</span></span>


</dt> <dd>

<span data-ttu-id="7317b-119">通訊服務設定為停用狀態。</span><span class="sxs-lookup"><span data-stu-id="7317b-119">The communication service is set to the disabled state.</span></span>

</dd> <dt>

<span id="Deferred"></span><span id="deferred"></span><span id="DEFERRED"></span>

<span data-ttu-id="7317b-120"><span id="Deferred"></span><span id="deferred"></span><span id="DEFERRED"></span>**延** 後的 (8) </span><span class="sxs-lookup"><span data-stu-id="7317b-120"><span id="Deferred"></span><span id="deferred"></span><span id="DEFERRED"></span>**Deferred** (8)</span></span>


</dt> <dd>

<span data-ttu-id="7317b-121">通訊服務狀態取決於 **Msvm \_ GuestCommunicationServiceSettingData** 中的 **DefaultEnabledStatePolicy** 。</span><span class="sxs-lookup"><span data-stu-id="7317b-121">The communication service state depends on **DefaultEnabledStatePolicy** in **Msvm\_GuestCommunicationServiceSettingData**.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="7317b-122">**名稱**</span><span class="sxs-lookup"><span data-stu-id="7317b-122">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7317b-123">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="7317b-123">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7317b-124">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="7317b-124">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7317b-125">服務的 GUID。</span><span class="sxs-lookup"><span data-stu-id="7317b-125">The GUID of the service.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="7317b-126">規格需求</span><span class="sxs-lookup"><span data-stu-id="7317b-126">Requirements</span></span>



| <span data-ttu-id="7317b-127">需求</span><span class="sxs-lookup"><span data-stu-id="7317b-127">Requirement</span></span> | <span data-ttu-id="7317b-128">值</span><span class="sxs-lookup"><span data-stu-id="7317b-128">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7317b-129">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="7317b-129">Minimum supported client</span></span><br/> | <span data-ttu-id="7317b-130">\[僅 Windows 10 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="7317b-130">Windows 10 \[desktop apps only\]</span></span><br/>                                                             |
| <span data-ttu-id="7317b-131">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="7317b-131">Minimum supported server</span></span><br/> | <span data-ttu-id="7317b-132">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="7317b-132">Windows Server 2016</span></span><br/>                                                                          |
| <span data-ttu-id="7317b-133">命名空間</span><span class="sxs-lookup"><span data-stu-id="7317b-133">Namespace</span></span><br/>                | <span data-ttu-id="7317b-134">根 \\ 虛擬化 \\ v2</span><span class="sxs-lookup"><span data-stu-id="7317b-134">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="7317b-135">MOF</span><span class="sxs-lookup"><span data-stu-id="7317b-135">MOF</span></span><br/>                      | <dl> <span data-ttu-id="7317b-136"><dt>WindowsVirtualization。</dt></span><span class="sxs-lookup"><span data-stu-id="7317b-136"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="7317b-137">DLL</span><span class="sxs-lookup"><span data-stu-id="7317b-137">DLL</span></span><br/>                      | <dl> <span data-ttu-id="7317b-138"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="7317b-138"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="7317b-139">另請參閱</span><span class="sxs-lookup"><span data-stu-id="7317b-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7317b-140">**CIM \_ SettingData**</span><span class="sxs-lookup"><span data-stu-id="7317b-140">**CIM\_SettingData**</span></span>](cim-settingdata.md)
</dt> </dl>

 

 




