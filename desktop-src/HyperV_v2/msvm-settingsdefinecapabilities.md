---
description: 提供功能實例與資源的最小值、最大值、增量和預設設定之間的連結。
ms.assetid: 3B09ED8A-D4D0-41E2-B807-96AD8E990773
title: Msvm_SettingsDefineCapabilities 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_SettingsDefineCapabilities
- Msvm_SettingsDefineCapabilities.SupportStatement
- Msvm_SettingsDefineCapabilities.GroupComponent
- Msvm_SettingsDefineCapabilities.PartComponent
- Msvm_SettingsDefineCapabilities.PropertyPolicy
- Msvm_SettingsDefineCapabilities.ValueRole
- Msvm_SettingsDefineCapabilities.ValueRange
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 7a312d3453b783c3d72f909ec6cb0b37d83feb9f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106966753"
---
# <a name="msvm_settingsdefinecapabilities-class"></a><span data-ttu-id="1ebd1-103">Msvm \_ SettingsDefineCapabilities 類別</span><span class="sxs-lookup"><span data-stu-id="1ebd1-103">Msvm\_SettingsDefineCapabilities class</span></span>

<span data-ttu-id="1ebd1-104">提供功能實例與資源的最小值、最大值、增量和預設設定之間的連結。</span><span class="sxs-lookup"><span data-stu-id="1ebd1-104">Provides a link between the capabilities instance and the minimum, maximum, incremental, and default settings for a resource.</span></span>

<span data-ttu-id="1ebd1-105">下列語法已簡化受控物件格式 (MOF) 程式碼，並且包含所有繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="1ebd1-105">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="1ebd1-106">語法</span><span class="sxs-lookup"><span data-stu-id="1ebd1-106">Syntax</span></span>

``` syntax
[Association, Aggregation, Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_SettingsDefineCapabilities : CIM_SettingsDefineCapabilities
{
  uint16               SupportStatement;
  CIM_Capabilities REF GroupComponent;
  CIM_SettingData  REF PartComponent;
  uint16               PropertyPolicy = 0;
  uint16               ValueRole = 3;
  uint16               ValueRange = 0;
};
```

## <a name="members"></a><span data-ttu-id="1ebd1-107">成員</span><span class="sxs-lookup"><span data-stu-id="1ebd1-107">Members</span></span>

<span data-ttu-id="1ebd1-108">**Msvm \_ SettingsDefineCapabilities** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="1ebd1-108">The **Msvm\_SettingsDefineCapabilities** class has these types of members:</span></span>

-   [<span data-ttu-id="1ebd1-109">屬性</span><span class="sxs-lookup"><span data-stu-id="1ebd1-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="1ebd1-110">屬性</span><span class="sxs-lookup"><span data-stu-id="1ebd1-110">Properties</span></span>

<span data-ttu-id="1ebd1-111">**Msvm \_ SettingsDefineCapabilities** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="1ebd1-111">The **Msvm\_SettingsDefineCapabilities** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="1ebd1-112">**GroupComponent**</span><span class="sxs-lookup"><span data-stu-id="1ebd1-112">**GroupComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1ebd1-113">資料類型： **[ **CIM \_ 功能**](/previous-versions//cc136806(v=vs.85))**</span><span class="sxs-lookup"><span data-stu-id="1ebd1-113">Data type: **[**CIM\_Capabilities**](/previous-versions//cc136806(v=vs.85))**</span></span>
</dt> <dt>

<span data-ttu-id="1ebd1-114">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="1ebd1-114">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1ebd1-115">功能實例。</span><span class="sxs-lookup"><span data-stu-id="1ebd1-115">The capabilities instance.</span></span> <span data-ttu-id="1ebd1-116">這個屬性繼承自 [**CIM \_ SettingsDefineCapabilities**](/previous-versions//cc136913(v=vs.85))。</span><span class="sxs-lookup"><span data-stu-id="1ebd1-116">This property is inherited from [**CIM\_SettingsDefineCapabilities**](/previous-versions//cc136913(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="1ebd1-117">**PartComponent**</span><span class="sxs-lookup"><span data-stu-id="1ebd1-117">**PartComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1ebd1-118">資料類型： **[ **CIM \_ SettingData**](/previous-versions//cc136911(v=vs.85))**</span><span class="sxs-lookup"><span data-stu-id="1ebd1-118">Data type: **[**CIM\_SettingData**](/previous-versions//cc136911(v=vs.85))**</span></span>
</dt> <dt>

<span data-ttu-id="1ebd1-119">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="1ebd1-119">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1ebd1-120">用來定義相關聯功能實例的設定。</span><span class="sxs-lookup"><span data-stu-id="1ebd1-120">A setting used to define the associated capabilities instance.</span></span> <span data-ttu-id="1ebd1-121">這個屬性繼承自 [**CIM \_ SettingsDefineCapabilities**](/previous-versions//cc136913(v=vs.85))。</span><span class="sxs-lookup"><span data-stu-id="1ebd1-121">This property is inherited from [**CIM\_SettingsDefineCapabilities**](/previous-versions//cc136913(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="1ebd1-122">**PropertyPolicy**</span><span class="sxs-lookup"><span data-stu-id="1ebd1-122">**PropertyPolicy**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1ebd1-123">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="1ebd1-123">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="1ebd1-124">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="1ebd1-124">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1ebd1-125">指出是否將關聯設定資料實例的非 null、非索引鍵屬性單獨處理，或視為相互關聯的集合。</span><span class="sxs-lookup"><span data-stu-id="1ebd1-125">Indicates whether the non-null, non-key properties of the associated setting data instance are treated independently or as a correlated set.</span></span> <span data-ttu-id="1ebd1-126">這個屬性繼承自 [**CIM \_ SettingsDefineCapabilities**](/previous-versions//cc136913(v=vs.85)) ，且一律設定為 0 (獨立) 。</span><span class="sxs-lookup"><span data-stu-id="1ebd1-126">This property is inherited from [**CIM\_SettingsDefineCapabilities**](/previous-versions//cc136913(v=vs.85)) and it is always set to 0 (Independent).</span></span>

</dd> <dt>

<span data-ttu-id="1ebd1-127">**SupportStatement**</span><span class="sxs-lookup"><span data-stu-id="1ebd1-127">**SupportStatement**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1ebd1-128">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="1ebd1-128">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="1ebd1-129">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="1ebd1-129">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1ebd1-130">識別支援語句。</span><span class="sxs-lookup"><span data-stu-id="1ebd1-130">Identifies the support statement.</span></span>

> [!Note]  
> <span data-ttu-id="1ebd1-131">這個屬性是在 Windows 10 1703 版中加入的。</span><span class="sxs-lookup"><span data-stu-id="1ebd1-131">This property was added in Windows 10, version 1703.</span></span>

 

<dt>

<span id="Production"></span><span id="production"></span><span id="PRODUCTION"></span>

<span data-ttu-id="1ebd1-132"><span id="Production"></span><span id="production"></span><span id="PRODUCTION"></span>**生產** (0) </span><span class="sxs-lookup"><span data-stu-id="1ebd1-132"><span id="Production"></span><span id="production"></span><span id="PRODUCTION"></span>**Production** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Prerelease"></span><span id="prerelease"></span><span id="PRERELEASE"></span>

<span data-ttu-id="1ebd1-133"><span id="Prerelease"></span><span id="prerelease"></span><span id="PRERELEASE"></span>**發行** 前版本 (1) </span><span class="sxs-lookup"><span data-stu-id="1ebd1-133"><span id="Prerelease"></span><span id="prerelease"></span><span id="PRERELEASE"></span>**Prerelease** (1)</span></span>


</dt> <dd>

> [!Note]  
> <span data-ttu-id="1ebd1-134">在 Windows 10 1703 版中 **非生產** 。</span><span class="sxs-lookup"><span data-stu-id="1ebd1-134">Was **NonProduction** in Windows 10, version 1703.</span></span>

 

</dd> <dt>

<span id="Reserved"></span><span id="reserved"></span><span id="RESERVED"></span>

<span data-ttu-id="1ebd1-135"><span id="Reserved"></span><span id="reserved"></span><span id="RESERVED"></span>**保留** 的 (。) </span><span class="sxs-lookup"><span data-stu-id="1ebd1-135"><span id="Reserved"></span><span id="reserved"></span><span id="RESERVED"></span>**Reserved** (..)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="1ebd1-136">**ValueRange**</span><span class="sxs-lookup"><span data-stu-id="1ebd1-136">**ValueRange**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1ebd1-137">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="1ebd1-137">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="1ebd1-138">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="1ebd1-138">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1ebd1-139">關於設定資料的所有非 null、非索引鍵屬性之解釋的任何進一步的語法。</span><span class="sxs-lookup"><span data-stu-id="1ebd1-139">Any further semantics on the interpretation of all non-null, non-key properties of the setting data.</span></span> <span data-ttu-id="1ebd1-140">這個屬性繼承自 [**CIM \_ SettingsDefineCapabilities**](/previous-versions//cc136913(v=vs.85))。</span><span class="sxs-lookup"><span data-stu-id="1ebd1-140">This property is inherited from [**CIM\_SettingsDefineCapabilities**](/previous-versions//cc136913(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="1ebd1-141">**ValueRole**</span><span class="sxs-lookup"><span data-stu-id="1ebd1-141">**ValueRole**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1ebd1-142">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="1ebd1-142">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="1ebd1-143">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="1ebd1-143">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1ebd1-144">設定資料之非 null、非索引鍵屬性的解讀上的任何進一步語義。</span><span class="sxs-lookup"><span data-stu-id="1ebd1-144">Any further semantics on the interpretation of the non-null, non-key properties of the setting data.</span></span> <span data-ttu-id="1ebd1-145">這個屬性繼承自 [**CIM \_ SettingsDefineCapabilities**](/previous-versions//cc136913(v=vs.85))。</span><span class="sxs-lookup"><span data-stu-id="1ebd1-145">This property is inherited from [**CIM\_SettingsDefineCapabilities**](/previous-versions//cc136913(v=vs.85)).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="1ebd1-146">備註</span><span class="sxs-lookup"><span data-stu-id="1ebd1-146">Remarks</span></span>

<span data-ttu-id="1ebd1-147">**ValueRole** 和 **ValueRange** 屬性的值會用於下列配對：</span><span class="sxs-lookup"><span data-stu-id="1ebd1-147">The values for the **ValueRole** and **ValueRange** properties are used in the following pairs:</span></span>

-   <span data-ttu-id="1ebd1-148">Point/Default (0/0) </span><span class="sxs-lookup"><span data-stu-id="1ebd1-148">Point/Default (0/0)</span></span>
-   <span data-ttu-id="1ebd1-149">最低/支援 (1/3) </span><span class="sxs-lookup"><span data-stu-id="1ebd1-149">Minimums/Supported (1/3)</span></span>
-   <span data-ttu-id="1ebd1-150">最大/支援 (2/3) </span><span class="sxs-lookup"><span data-stu-id="1ebd1-150">Maximums/Supported (2/3)</span></span>
-   <span data-ttu-id="1ebd1-151">遞增/支援 (3/3) 。</span><span class="sxs-lookup"><span data-stu-id="1ebd1-151">Increments/Supported (3/3).</span></span>

<span data-ttu-id="1ebd1-152">「點」表示 **PartComponent** 物件上的每個屬性都代表平臺預設值。</span><span class="sxs-lookup"><span data-stu-id="1ebd1-152">"Point" means that each of the properties on the **PartComponent** object represents the platform default.</span></span>

<span data-ttu-id="1ebd1-153">「最小值」和「最大值」表示 **PartComponent** 物件上的每個屬性都代表這些屬性的最小和最大可能值，這些屬性是根據您目前的電腦設定所支援的平臺。</span><span class="sxs-lookup"><span data-stu-id="1ebd1-153">"Minimums" and "Maximums" mean that each of the properties on the **PartComponent** object represent the smallest and largest possible values for these properties that are supported by the platform based on your current machine configuration.</span></span>

<span data-ttu-id="1ebd1-154">「遞增」表示您可以增加或減少設定的資料細微性。</span><span class="sxs-lookup"><span data-stu-id="1ebd1-154">"Increments" indicates the granularity at which you can increase or decrease the settings.</span></span>

<span data-ttu-id="1ebd1-155">存取 **Msvm \_ SettingsDefineCapabilities** 類別可能受 UAC 篩選所限制。</span><span class="sxs-lookup"><span data-stu-id="1ebd1-155">Access to the **Msvm\_SettingsDefineCapabilities** class might be restricted by UAC Filtering.</span></span> <span data-ttu-id="1ebd1-156">如需詳細資訊，請參閱 [使用者帳戶控制和 WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi)。</span><span class="sxs-lookup"><span data-stu-id="1ebd1-156">For more information, see [User Account Control and WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span></span>

## <a name="requirements"></a><span data-ttu-id="1ebd1-157">規格需求</span><span class="sxs-lookup"><span data-stu-id="1ebd1-157">Requirements</span></span>



| <span data-ttu-id="1ebd1-158">需求</span><span class="sxs-lookup"><span data-stu-id="1ebd1-158">Requirement</span></span> | <span data-ttu-id="1ebd1-159">值</span><span class="sxs-lookup"><span data-stu-id="1ebd1-159">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1ebd1-160">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="1ebd1-160">Minimum supported client</span></span><br/> | <span data-ttu-id="1ebd1-161">\[僅 Windows 8 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="1ebd1-161">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="1ebd1-162">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="1ebd1-162">Minimum supported server</span></span><br/> | <span data-ttu-id="1ebd1-163">僅限 Windows Server 2012 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="1ebd1-163">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="1ebd1-164">命名空間</span><span class="sxs-lookup"><span data-stu-id="1ebd1-164">Namespace</span></span><br/>                | <span data-ttu-id="1ebd1-165">根 \\ 虛擬化 \\ V2</span><span class="sxs-lookup"><span data-stu-id="1ebd1-165">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="1ebd1-166">MOF</span><span class="sxs-lookup"><span data-stu-id="1ebd1-166">MOF</span></span><br/>                      | <dl> <span data-ttu-id="1ebd1-167"><dt>WindowsVirtualization。</dt></span><span class="sxs-lookup"><span data-stu-id="1ebd1-167"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="1ebd1-168">DLL</span><span class="sxs-lookup"><span data-stu-id="1ebd1-168">DLL</span></span><br/>                      | <dl> <span data-ttu-id="1ebd1-169"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="1ebd1-169"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="1ebd1-170">另請參閱</span><span class="sxs-lookup"><span data-stu-id="1ebd1-170">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1ebd1-171">**CIM \_ SettingsDefineCapabilities**</span><span class="sxs-lookup"><span data-stu-id="1ebd1-171">**CIM\_SettingsDefineCapabilities**</span></span>](cim-settingsdefinecapabilities.md)
</dt> <dt>

<span data-ttu-id="1ebd1-172">[**CIM \_ SettingsDefineCapabilities**](/previous-versions//cc136913(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="1ebd1-172">[**CIM\_SettingsDefineCapabilities**](/previous-versions//cc136913(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="1ebd1-173">**Msvm \_ SettingsDefineCapabilities (V1)**</span><span class="sxs-lookup"><span data-stu-id="1ebd1-173">**Msvm\_SettingsDefineCapabilities (V1)**</span></span>](/previous-versions/windows/desktop/virtual/msvm-settingsdefinecapabilities)
</dt> <dt>

[<span data-ttu-id="1ebd1-174">資源管理類別</span><span class="sxs-lookup"><span data-stu-id="1ebd1-174">Resource Management Classes</span></span>](resource-management-classes.md)
</dt> </dl>

 

