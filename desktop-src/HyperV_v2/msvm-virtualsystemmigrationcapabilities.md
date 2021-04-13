---
description: 定義用戶端可以探索遷移服務所提供之方法的方式，以及虛擬系統移轉設定資料的有效範圍。
ms.assetid: 704fa81d-54a4-4d12-9b85-8836581d2784
title: Msvm_VirtualSystemMigrationCapabilities 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualSystemMigrationCapabilities
- Msvm_VirtualSystemMigrationCapabilities.InstanceID
- Msvm_VirtualSystemMigrationCapabilities.Caption
- Msvm_VirtualSystemMigrationCapabilities.Description
- Msvm_VirtualSystemMigrationCapabilities.ElementName
- Msvm_VirtualSystemMigrationCapabilities.SynchronousMethodsSupported
- Msvm_VirtualSystemMigrationCapabilities.AsynchronousMethodsSupported
- Msvm_VirtualSystemMigrationCapabilities.DestinationHostFormatsSupported
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: c89e898cbf861d2bc3643e43a8bd9089062a2d32
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104510993"
---
# <a name="msvm_virtualsystemmigrationcapabilities-class"></a><span data-ttu-id="f6119-103">Msvm \_ VirtualSystemMigrationCapabilities 類別</span><span class="sxs-lookup"><span data-stu-id="f6119-103">Msvm\_VirtualSystemMigrationCapabilities class</span></span>

<span data-ttu-id="f6119-104">定義用戶端可以探索遷移服務所提供之方法的方式，以及虛擬系統移轉設定資料的有效範圍。</span><span class="sxs-lookup"><span data-stu-id="f6119-104">Defines the means by which a client can discover the methods provided by the migration service, and valid range of virtual system migration setting data.</span></span> <span data-ttu-id="f6119-105">**Msvm \_ VirtualSystemMigrationCapabilities** 物件與 [**Msvm \_ VirtualSystemMigrationSettingData**](msvm-virtualsystemmigrationsettingdata.md)物件相關聯。</span><span class="sxs-lookup"><span data-stu-id="f6119-105">The **Msvm\_VirtualSystemMigrationCapabilities** object is associated with [**Msvm\_VirtualSystemMigrationSettingData**](msvm-virtualsystemmigrationsettingdata.md) objects.</span></span> <span data-ttu-id="f6119-106">這些關聯會定義可用的有效遷移服務範圍。</span><span class="sxs-lookup"><span data-stu-id="f6119-106">These associations define the valid range of migration services available.</span></span>

<span data-ttu-id="f6119-107">下列語法已簡化受控物件格式 (MOF) 程式碼，並且包含所有繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="f6119-107">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="f6119-108">語法</span><span class="sxs-lookup"><span data-stu-id="f6119-108">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_VirtualSystemMigrationCapabilities : CIM_VirtualSystemMigrationCapabilities
{
  string InstanceID;
  string Caption = "Migration Capabilities";
  string Description = "Virtual System Migration Capabilities";
  string ElementName;
  uint16 SynchronousMethodsSupported[];
  uint16 AsynchronousMethodsSupported[];
  uint16 DestinationHostFormatsSupported[];
};
```

## <a name="members"></a><span data-ttu-id="f6119-109">成員</span><span class="sxs-lookup"><span data-stu-id="f6119-109">Members</span></span>

<span data-ttu-id="f6119-110">**Msvm \_ VirtualSystemMigrationCapabilities** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="f6119-110">The **Msvm\_VirtualSystemMigrationCapabilities** class has these types of members:</span></span>

-   [<span data-ttu-id="f6119-111">屬性</span><span class="sxs-lookup"><span data-stu-id="f6119-111">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="f6119-112">屬性</span><span class="sxs-lookup"><span data-stu-id="f6119-112">Properties</span></span>

<span data-ttu-id="f6119-113">**Msvm \_ VirtualSystemMigrationCapabilities** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="f6119-113">The **Msvm\_VirtualSystemMigrationCapabilities** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="f6119-114">**AsynchronousMethodsSupported**</span><span class="sxs-lookup"><span data-stu-id="f6119-114">**AsynchronousMethodsSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f6119-115">資料類型： **uint16** 陣列</span><span class="sxs-lookup"><span data-stu-id="f6119-115">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="f6119-116">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="f6119-116">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f6119-117">限定詞：覆 [**寫**](/windows/desktop/WmiSdk/standard-qualifiers) ( "AsynchronousMethodsSupported" ) </span><span class="sxs-lookup"><span data-stu-id="f6119-117">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("AsynchronousMethodsSupported")</span></span>
</dt> </dl>

<span data-ttu-id="f6119-118">識別其實值可能是非同步方法;也就是說，作業不會立即完成，而且會傳回工作。</span><span class="sxs-lookup"><span data-stu-id="f6119-118">Identifies the methods whose implementation may be asynchronous; that is, the operation will not be completed immediately and will return a job.</span></span> <span data-ttu-id="f6119-119">這個屬性繼承自 **CIM \_ VirtualSystemMigrationCapabilities**。</span><span class="sxs-lookup"><span data-stu-id="f6119-119">This property is inherited from **CIM\_VirtualSystemMigrationCapabilities**.</span></span>

<dt>

<span id="MigrateVirtualSystemToHostSupported"></span><span id="migratevirtualsystemtohostsupported"></span><span id="MIGRATEVIRTUALSYSTEMTOHOSTSUPPORTED"></span>

<span data-ttu-id="f6119-120">**MigrateVirtualSystemToHostSupported** (2) </span><span class="sxs-lookup"><span data-stu-id="f6119-120">**MigrateVirtualSystemToHostSupported** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="MigrateVirtualSystemToSystemSupported"></span><span id="migratevirtualsystemtosystemsupported"></span><span id="MIGRATEVIRTUALSYSTEMTOSYSTEMSUPPORTED"></span>

<span data-ttu-id="f6119-121">**MigrateVirtualSystemToSystemSupported** (3) </span><span class="sxs-lookup"><span data-stu-id="f6119-121">**MigrateVirtualSystemToSystemSupported** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="CheckVirtualSystemIsMigratableSupported"></span><span id="checkvirtualsystemismigratablesupported"></span><span id="CHECKVIRTUALSYSTEMISMIGRATABLESUPPORTED"></span>

<span data-ttu-id="f6119-122">**CheckVirtualSystemIsMigratableSupported** (32768) </span><span class="sxs-lookup"><span data-stu-id="f6119-122">**CheckVirtualSystemIsMigratableSupported** (32768)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="f6119-123">**標題**</span><span class="sxs-lookup"><span data-stu-id="f6119-123">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f6119-124">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="f6119-124">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f6119-125">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="f6119-125">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f6119-126">物件的簡短描述。</span><span class="sxs-lookup"><span data-stu-id="f6119-126">A short description of the object.</span></span> <span data-ttu-id="f6119-127">這個屬性繼承自 [**CIM \_ ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)，一律設為「遷移功能」。</span><span class="sxs-lookup"><span data-stu-id="f6119-127">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement), and it is always set to "Migration Capabilities".</span></span>

</dd> <dt>

<span data-ttu-id="f6119-128">**說明**</span><span class="sxs-lookup"><span data-stu-id="f6119-128">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f6119-129">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="f6119-129">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f6119-130">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="f6119-130">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f6119-131">對物件的描述。</span><span class="sxs-lookup"><span data-stu-id="f6119-131">A description of the object.</span></span> <span data-ttu-id="f6119-132">這個屬性繼承自 [**CIM \_ ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)，一律設為「虛擬系統移轉功能」。</span><span class="sxs-lookup"><span data-stu-id="f6119-132">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement), and it is always set to "Virtual System Migration Capabilities".</span></span>

</dd> <dt>

<span data-ttu-id="f6119-133">**DestinationHostFormatsSupported**</span><span class="sxs-lookup"><span data-stu-id="f6119-133">**DestinationHostFormatsSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f6119-134">資料類型： **uint16** 陣列</span><span class="sxs-lookup"><span data-stu-id="f6119-134">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="f6119-135">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="f6119-135">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f6119-136">支援 [**MigrateVirtualSystemToHost**](migratevirtualsystemtohost-msvm-virtualsystemmigrationservice.md)和 [**CheckVirtualSystemIsMigratable**](checkvirtualsystemismigratable-msvm-virtualsystemmigrationservice.md)方法之 *DestinationHost* 參數的名稱格式陣列。</span><span class="sxs-lookup"><span data-stu-id="f6119-136">An array of name formats that are supported for the *DestinationHost* parameter of the [**MigrateVirtualSystemToHost**](migratevirtualsystemtohost-msvm-virtualsystemmigrationservice.md) and [**CheckVirtualSystemIsMigratable**](checkvirtualsystemismigratable-msvm-virtualsystemmigrationservice.md) methods.</span></span> <span data-ttu-id="f6119-137">這個屬性繼承自 **CIM \_ VirtualSystemMigrationCapabilities**。</span><span class="sxs-lookup"><span data-stu-id="f6119-137">This property is inherited from **CIM\_VirtualSystemMigrationCapabilities**.</span></span>



| <span data-ttu-id="f6119-138">值</span><span class="sxs-lookup"><span data-stu-id="f6119-138">Value</span></span>                                                                                                                                                                                                                                                                                                                           | <span data-ttu-id="f6119-139">意義</span><span class="sxs-lookup"><span data-stu-id="f6119-139">Meaning</span></span>                                                                      |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------|
| <span id="DomainNameFormatSupported"></span><span id="domainnameformatsupported"></span><span id="DOMAINNAMEFORMATSUPPORTED"></span><dl> <span data-ttu-id="f6119-140"><dt>**DomainNameFormatSupported**</dt> <dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="f6119-140"><dt>**DomainNameFormatSupported**</dt> <dt>2</dt></span></span> </dl>                             | <span data-ttu-id="f6119-141">根據 RFC 10353 的功能變數名稱格式支援。</span><span class="sxs-lookup"><span data-stu-id="f6119-141">Support of the domain name format according to RFC 10353.</span></span><br/>         |
| <span id="IPv4DottedDecimalFormatSupported"></span><span id="ipv4dotteddecimalformatsupported"></span><span id="IPV4DOTTEDDECIMALFORMATSUPPORTED"></span><dl> <span data-ttu-id="f6119-142"><dt>**IPv4DottedDecimalFormatSupported**</dt> <dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="f6119-142"><dt>**IPv4DottedDecimalFormatSupported**</dt> <dt>3</dt></span></span> </dl> | <span data-ttu-id="f6119-143">根據 RFC 12084 支援 IPv4 虛線十進位格式。</span><span class="sxs-lookup"><span data-stu-id="f6119-143">Support of the IPv4 dotted decimal format according to RFC 12084.</span></span><br/> |
| <span id="IPv6TextFormatSupported"></span><span id="ipv6textformatsupported"></span><span id="IPV6TEXTFORMATSUPPORTED"></span><dl> <span data-ttu-id="f6119-144"><dt>**IPv6TextFormatSupported**</dt> <dt>4</dt></span><span class="sxs-lookup"><span data-stu-id="f6119-144"><dt>**IPv6TextFormatSupported**</dt> <dt>4</dt></span></span> </dl>                                     | <span data-ttu-id="f6119-145">根據 RFC 4291 支援 IPv6 文字格式。</span><span class="sxs-lookup"><span data-stu-id="f6119-145">Support of the IPv6 text format according to RFC 4291.</span></span><br/>            |



 

</dd> <dt>

<span data-ttu-id="f6119-146">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="f6119-146">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f6119-147">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="f6119-147">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f6119-148">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="f6119-148">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f6119-149">物件的顯示名稱。</span><span class="sxs-lookup"><span data-stu-id="f6119-149">A display name for the object.</span></span> <span data-ttu-id="f6119-150">這個屬性繼承自 [**CIM \_ ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)。</span><span class="sxs-lookup"><span data-stu-id="f6119-150">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="f6119-151">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="f6119-151">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f6119-152">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="f6119-152">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f6119-153">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="f6119-153">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f6119-154">限定詞：索引 **鍵**</span><span class="sxs-lookup"><span data-stu-id="f6119-154">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="f6119-155">唯一識別此類別的實例。</span><span class="sxs-lookup"><span data-stu-id="f6119-155">Uniquely identifies an instance of this class.</span></span> <span data-ttu-id="f6119-156">這個屬性繼承自 [**CIM \_ ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)。</span><span class="sxs-lookup"><span data-stu-id="f6119-156">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="f6119-157">**SynchronousMethodsSupported**</span><span class="sxs-lookup"><span data-stu-id="f6119-157">**SynchronousMethodsSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f6119-158">資料類型： **uint16** 陣列</span><span class="sxs-lookup"><span data-stu-id="f6119-158">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="f6119-159">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="f6119-159">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f6119-160">識別可同步執行的方法;也就是說，此作業將會立即完成，而且不會傳回工作。</span><span class="sxs-lookup"><span data-stu-id="f6119-160">Identifies the methods whose implementation may be synchronous; that is, the operation will be completed immediately and will not return a job.</span></span> <span data-ttu-id="f6119-161">這個屬性繼承自 **CIM \_ VirtualSystemMigrationCapabilities**。</span><span class="sxs-lookup"><span data-stu-id="f6119-161">This property is inherited from **CIM\_VirtualSystemMigrationCapabilities**.</span></span>

<dl> <dt>

<span data-ttu-id="f6119-162"><span id="MigrateVirtualSystemToHostSupported"></span><span id="migratevirtualsystemtohostsupported"></span><span id="MIGRATEVIRTUALSYSTEMTOHOSTSUPPORTED"></span>**MigrateVirtualSystemToHostSupported** (2) </span><span class="sxs-lookup"><span data-stu-id="f6119-162"><span id="MigrateVirtualSystemToHostSupported"></span><span id="migratevirtualsystemtohostsupported"></span><span id="MIGRATEVIRTUALSYSTEMTOHOSTSUPPORTED"></span>**MigrateVirtualSystemToHostSupported** (2)</span></span>
</dt> <dt>

<span data-ttu-id="f6119-163"><span id="MigrateVirtualSystemToSystemSupported"></span><span id="migratevirtualsystemtosystemsupported"></span><span id="MIGRATEVIRTUALSYSTEMTOSYSTEMSUPPORTED"></span>**MigrateVirtualSystemToSystemSupported** (3) </span><span class="sxs-lookup"><span data-stu-id="f6119-163"><span id="MigrateVirtualSystemToSystemSupported"></span><span id="migratevirtualsystemtosystemsupported"></span><span id="MIGRATEVIRTUALSYSTEMTOSYSTEMSUPPORTED"></span>**MigrateVirtualSystemToSystemSupported** (3)</span></span>
</dt> <dt>

<span data-ttu-id="f6119-164"><span id="CheckVirtualSystemIsMigratableToHostSupported"></span><span id="checkvirtualsystemismigratabletohostsupported"></span><span id="CHECKVIRTUALSYSTEMISMIGRATABLETOHOSTSUPPORTED"></span>**CheckVirtualSystemIsMigratableToHostSupported** (4) </span><span class="sxs-lookup"><span data-stu-id="f6119-164"><span id="CheckVirtualSystemIsMigratableToHostSupported"></span><span id="checkvirtualsystemismigratabletohostsupported"></span><span id="CHECKVIRTUALSYSTEMISMIGRATABLETOHOSTSUPPORTED"></span>**CheckVirtualSystemIsMigratableToHostSupported** (4)</span></span>
</dt> <dt>

<span data-ttu-id="f6119-165"><span id="CheckVirtualSystemIsMigratableToSystemSupported"></span><span id="checkvirtualsystemismigratabletosystemsupported"></span><span id="CHECKVIRTUALSYSTEMISMIGRATABLETOSYSTEMSUPPORTED"></span>**CheckVirtualSystemIsMigratableToSystemSupported** (5) </span><span class="sxs-lookup"><span data-stu-id="f6119-165"><span id="CheckVirtualSystemIsMigratableToSystemSupported"></span><span id="checkvirtualsystemismigratabletosystemsupported"></span><span id="CHECKVIRTUALSYSTEMISMIGRATABLETOSYSTEMSUPPORTED"></span>**CheckVirtualSystemIsMigratableToSystemSupported** (5)</span></span>
</dt> <dt>

<span data-ttu-id="f6119-166"><span id="DMTF_Reserved_"></span><span id="dmtf_reserved_"></span><span id="DMTF_RESERVED_"></span>**DMTF 保留** ( .。。</span><span class="sxs-lookup"><span data-stu-id="f6119-166"><span id="DMTF_Reserved_"></span><span id="dmtf_reserved_"></span><span id="DMTF_RESERVED_"></span>**DMTF Reserved** (..</span></span> <span data-ttu-id="f6119-167">)</span><span class="sxs-lookup"><span data-stu-id="f6119-167">)</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="f6119-168">規格需求</span><span class="sxs-lookup"><span data-stu-id="f6119-168">Requirements</span></span>



| <span data-ttu-id="f6119-169">需求</span><span class="sxs-lookup"><span data-stu-id="f6119-169">Requirement</span></span> | <span data-ttu-id="f6119-170">值</span><span class="sxs-lookup"><span data-stu-id="f6119-170">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f6119-171">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="f6119-171">Minimum supported client</span></span><br/> | <span data-ttu-id="f6119-172">\[僅 Windows 8 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="f6119-172">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="f6119-173">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="f6119-173">Minimum supported server</span></span><br/> | <span data-ttu-id="f6119-174">僅限 Windows Server 2012 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="f6119-174">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="f6119-175">命名空間</span><span class="sxs-lookup"><span data-stu-id="f6119-175">Namespace</span></span><br/>                | <span data-ttu-id="f6119-176">根 \\ 虛擬化 \\ V2</span><span class="sxs-lookup"><span data-stu-id="f6119-176">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="f6119-177">MOF</span><span class="sxs-lookup"><span data-stu-id="f6119-177">MOF</span></span><br/>                      | <dl> <span data-ttu-id="f6119-178"><dt>WindowsVirtualization。</dt></span><span class="sxs-lookup"><span data-stu-id="f6119-178"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="f6119-179">DLL</span><span class="sxs-lookup"><span data-stu-id="f6119-179">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f6119-180"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="f6119-180"><dt>Vmms.exe</dt></span></span> </dl>                     |



 

