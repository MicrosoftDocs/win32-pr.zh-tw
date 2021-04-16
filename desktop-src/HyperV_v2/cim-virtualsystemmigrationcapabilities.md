---
description: 代表 CIM VirtualSystemMigrationService 物件的功能 \_ 。
ms.assetid: 5fe3a10b-c075-4c45-838d-0b5c2e491584
title: CIM_VirtualSystemMigrationCapabilities 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_VirtualSystemMigrationCapabilities
- CIM_VirtualSystemMigrationCapabilities.SynchronousMethodsSupported
- CIM_VirtualSystemMigrationCapabilities.AsynchronousMethodsSupported
- CIM_VirtualSystemMigrationCapabilities.DestinationHostFormatsSupported
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 1a9a9a0a0f8e9ea344c7a37ad1168dcb5e059093
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104513257"
---
# <a name="cim_virtualsystemmigrationcapabilities-class"></a><span data-ttu-id="fc7bf-103">CIM \_ VirtualSystemMigrationCapabilities 類別</span><span class="sxs-lookup"><span data-stu-id="fc7bf-103">CIM\_VirtualSystemMigrationCapabilities class</span></span>

<span data-ttu-id="fc7bf-104">代表 [**CIM \_ VirtualSystemMigrationService**](cim-virtualsystemmigrationservice.md) 物件的功能。</span><span class="sxs-lookup"><span data-stu-id="fc7bf-104">Represents the capabilities of a [**CIM\_VirtualSystemMigrationService**](cim-virtualsystemmigrationservice.md) object.</span></span>

## <a name="syntax"></a><span data-ttu-id="fc7bf-105">語法</span><span class="sxs-lookup"><span data-stu-id="fc7bf-105">Syntax</span></span>

``` syntax
[Experimental, Abstract, Version("2.17.0"), UMLPackagePath("CIM::System::Virtualization"), AMENDMENT]
class CIM_VirtualSystemMigrationCapabilities : CIM_Capabilities
{
  uint16 SynchronousMethodsSupported[];
  uint16 AsynchronousMethodsSupported[];
  uint16 DestinationHostFormatsSupported[];
};
```

## <a name="members"></a><span data-ttu-id="fc7bf-106">成員</span><span class="sxs-lookup"><span data-stu-id="fc7bf-106">Members</span></span>

<span data-ttu-id="fc7bf-107">**CIM \_ VirtualSystemMigrationCapabilities** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="fc7bf-107">The **CIM\_VirtualSystemMigrationCapabilities** class has these types of members:</span></span>

-   [<span data-ttu-id="fc7bf-108">屬性</span><span class="sxs-lookup"><span data-stu-id="fc7bf-108">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="fc7bf-109">屬性</span><span class="sxs-lookup"><span data-stu-id="fc7bf-109">Properties</span></span>

<span data-ttu-id="fc7bf-110">**CIM \_ VirtualSystemMigrationCapabilities** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="fc7bf-110">The **CIM\_VirtualSystemMigrationCapabilities** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="fc7bf-111">**AsynchronousMethodsSupported**</span><span class="sxs-lookup"><span data-stu-id="fc7bf-111">**AsynchronousMethodsSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fc7bf-112">資料類型： **uint16** 陣列</span><span class="sxs-lookup"><span data-stu-id="fc7bf-112">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="fc7bf-113">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="fc7bf-113">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="fc7bf-114">陣列，指出非同步作業所支援的 [**CIM \_ VirtualSystemMigrationService**](cim-virtualsystemmigrationservice.md) 方法。</span><span class="sxs-lookup"><span data-stu-id="fc7bf-114">An array that indicates the [**CIM\_VirtualSystemMigrationService**](cim-virtualsystemmigrationservice.md) methods that are supported for asynchronous operations.</span></span>

<dt>

<span id="MigrateVirtualSystemToHostSupported"></span><span id="migratevirtualsystemtohostsupported"></span><span id="MIGRATEVIRTUALSYSTEMTOHOSTSUPPORTED"></span>

<span data-ttu-id="fc7bf-115">**MigrateVirtualSystemToHostSupported** (2) </span><span class="sxs-lookup"><span data-stu-id="fc7bf-115">**MigrateVirtualSystemToHostSupported** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="MigrateVirtualSystemToSystemSupported"></span><span id="migratevirtualsystemtosystemsupported"></span><span id="MIGRATEVIRTUALSYSTEMTOSYSTEMSUPPORTED"></span>

<span data-ttu-id="fc7bf-116">**MigrateVirtualSystemToSystemSupported** (3) </span><span class="sxs-lookup"><span data-stu-id="fc7bf-116">**MigrateVirtualSystemToSystemSupported** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

<span data-ttu-id="fc7bf-117">**DMTF 保留** ( .。。) </span><span class="sxs-lookup"><span data-stu-id="fc7bf-117">**DMTF Reserved** (..)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="fc7bf-118">**DestinationHostFormatsSupported**</span><span class="sxs-lookup"><span data-stu-id="fc7bf-118">**DestinationHostFormatsSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fc7bf-119">資料類型： **uint16** 陣列</span><span class="sxs-lookup"><span data-stu-id="fc7bf-119">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="fc7bf-120">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="fc7bf-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="fc7bf-121">限定詞： [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ( "[**CIM \_ VirtualSystemMigrationService**](cim-virtualsystemmigrationservice.md).**MigrateVirtualSystemToHost (DestinationHost)**"，"**CIM \_ VirtualSystemMigrationService**。**CheckVirtualSystemIsMigratableToHost (DestinationHost)**」 ) </span><span class="sxs-lookup"><span data-stu-id="fc7bf-121">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_VirtualSystemMigrationService**](cim-virtualsystemmigrationservice.md).**MigrateVirtualSystemToHost(DestinationHost)**", "**CIM\_VirtualSystemMigrationService**.**CheckVirtualSystemIsMigratableToHost(DestinationHost)**")</span></span>
</dt> </dl>

<span data-ttu-id="fc7bf-122">陣列，其中包含 [**CIM \_ VirtualSystemMigrationService**](cim-virtualsystemmigrationservice.md)物件之 [**MigrateVirtualSystemToHost**](cim-virtualsystemmigrationservice-migratevirtualsystemtohost.md)和 [**CheckVirtualSystemIsMigratableToHost**](cim-virtualsystemmigrationservice-checkvirtualsystemismigratabletohost.md)方法的 *DestinationHost* 參數所支援的格式。</span><span class="sxs-lookup"><span data-stu-id="fc7bf-122">An array that contains the supported formats for the *DestinationHost* parameter of the [**MigrateVirtualSystemToHost**](cim-virtualsystemmigrationservice-migratevirtualsystemtohost.md) and [**CheckVirtualSystemIsMigratableToHost**](cim-virtualsystemmigrationservice-checkvirtualsystemismigratabletohost.md) methods for the [**CIM\_VirtualSystemMigrationService**](cim-virtualsystemmigrationservice.md) object.</span></span>

<dt>

<span id="DomainNameFormatSupported"></span><span id="domainnameformatsupported"></span><span id="DOMAINNAMEFORMATSUPPORTED"></span>

<span data-ttu-id="fc7bf-123"><span id="DomainNameFormatSupported"></span><span id="domainnameformatsupported"></span><span id="DOMAINNAMEFORMATSUPPORTED"></span>**DomainNameFormatSupported** (2) </span><span class="sxs-lookup"><span data-stu-id="fc7bf-123"><span id="DomainNameFormatSupported"></span><span id="domainnameformatsupported"></span><span id="DOMAINNAMEFORMATSUPPORTED"></span>**DomainNameFormatSupported** (2)</span></span>


</dt> <dd>

<span data-ttu-id="fc7bf-124">根據 RFC 1035 支援功能變數名稱文字格式。</span><span class="sxs-lookup"><span data-stu-id="fc7bf-124">Support of the Domain Name text format according to RFC 1035.</span></span>

</dd> <dt>

<span id="IPv4DottedDecimalFormatSupported"></span><span id="ipv4dotteddecimalformatsupported"></span><span id="IPV4DOTTEDDECIMALFORMATSUPPORTED"></span>

<span data-ttu-id="fc7bf-125"><span id="IPv4DottedDecimalFormatSupported"></span><span id="ipv4dotteddecimalformatsupported"></span><span id="IPV4DOTTEDDECIMALFORMATSUPPORTED"></span>**IPv4DottedDecimalFormatSupported** (3) </span><span class="sxs-lookup"><span data-stu-id="fc7bf-125"><span id="IPv4DottedDecimalFormatSupported"></span><span id="ipv4dotteddecimalformatsupported"></span><span id="IPV4DOTTEDDECIMALFORMATSUPPORTED"></span>**IPv4DottedDecimalFormatSupported** (3)</span></span>


</dt> <dd>

<span data-ttu-id="fc7bf-126">根據 RFC 1208 支援 IPv4 虛線十進位格式。</span><span class="sxs-lookup"><span data-stu-id="fc7bf-126">Support of the IPv4 dotted decimal format according to RFC 1208.</span></span>

</dd> <dt>

<span id="IPv6TextFormatSupported"></span><span id="ipv6textformatsupported"></span><span id="IPV6TEXTFORMATSUPPORTED"></span>

<span data-ttu-id="fc7bf-127"><span id="IPv6TextFormatSupported"></span><span id="ipv6textformatsupported"></span><span id="IPV6TEXTFORMATSUPPORTED"></span>**IPv6TextFormatSupported** (4) </span><span class="sxs-lookup"><span data-stu-id="fc7bf-127"><span id="IPv6TextFormatSupported"></span><span id="ipv6textformatsupported"></span><span id="IPV6TEXTFORMATSUPPORTED"></span>**IPv6TextFormatSupported** (4)</span></span>


</dt> <dd>

<span data-ttu-id="fc7bf-128">根據 RFC 4291 支援 IPv6 文字格式</span><span class="sxs-lookup"><span data-stu-id="fc7bf-128">Support of the IPv6 text format according to RFC 4291</span></span>

</dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

<span data-ttu-id="fc7bf-129"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF 保留** ( .。。) </span><span class="sxs-lookup"><span data-stu-id="fc7bf-129"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="fc7bf-130">**SynchronousMethodsSupported**</span><span class="sxs-lookup"><span data-stu-id="fc7bf-130">**SynchronousMethodsSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fc7bf-131">資料類型： **uint16** 陣列</span><span class="sxs-lookup"><span data-stu-id="fc7bf-131">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="fc7bf-132">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="fc7bf-132">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="fc7bf-133">陣列，指出同步作業支援的 [**CIM \_ VirtualSystemMigrationService**](cim-virtualsystemmigrationservice.md) 方法。</span><span class="sxs-lookup"><span data-stu-id="fc7bf-133">An array that indicates the [**CIM\_VirtualSystemMigrationService**](cim-virtualsystemmigrationservice.md) methods that are supported for synchronous operations.</span></span>

<span data-ttu-id="fc7bf-134">列舉其實值可能是同步的方法識別碼：也就是說，此作業可能會立即完成，因此，方法可能不會傳回工作。</span><span class="sxs-lookup"><span data-stu-id="fc7bf-134">Enumeration of method identifiers whose implementation may be synchronous; that is, the operation may complete immediately and therefore the method may not return a job.</span></span>

<dt>

<span id="MigrateVirtualSystemToHostSupported"></span><span id="migratevirtualsystemtohostsupported"></span><span id="MIGRATEVIRTUALSYSTEMTOHOSTSUPPORTED"></span>

<span data-ttu-id="fc7bf-135">**MigrateVirtualSystemToHostSupported** (2) </span><span class="sxs-lookup"><span data-stu-id="fc7bf-135">**MigrateVirtualSystemToHostSupported** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="MigrateVirtualSystemToSystemSupported"></span><span id="migratevirtualsystemtosystemsupported"></span><span id="MIGRATEVIRTUALSYSTEMTOSYSTEMSUPPORTED"></span>

<span data-ttu-id="fc7bf-136">**MigrateVirtualSystemToSystemSupported** (3) </span><span class="sxs-lookup"><span data-stu-id="fc7bf-136">**MigrateVirtualSystemToSystemSupported** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="CheckVirtualSystemIsMigratableToHostSupported"></span><span id="checkvirtualsystemismigratabletohostsupported"></span><span id="CHECKVIRTUALSYSTEMISMIGRATABLETOHOSTSUPPORTED"></span>

<span data-ttu-id="fc7bf-137">**CheckVirtualSystemIsMigratableToHostSupported** (4) </span><span class="sxs-lookup"><span data-stu-id="fc7bf-137">**CheckVirtualSystemIsMigratableToHostSupported** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="CheckVirtualSystemIsMigratableToSystemSupported"></span><span id="checkvirtualsystemismigratabletosystemsupported"></span><span id="CHECKVIRTUALSYSTEMISMIGRATABLETOSYSTEMSUPPORTED"></span>

<span data-ttu-id="fc7bf-138">**CheckVirtualSystemIsMigratableToSystemSupported** (5) </span><span class="sxs-lookup"><span data-stu-id="fc7bf-138">**CheckVirtualSystemIsMigratableToSystemSupported** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

<span data-ttu-id="fc7bf-139">**DMTF 保留** ( .。。) </span><span class="sxs-lookup"><span data-stu-id="fc7bf-139">**DMTF Reserved** (..)</span></span>


<span data-ttu-id="fc7bf-140"></dt> <dd></dd> </dl>

</dd> </dl></span><span class="sxs-lookup"><span data-stu-id="fc7bf-140"></dt> <dd></dd> </dl>

</dd> </dl></span></span>

## <a name="requirements"></a><span data-ttu-id="fc7bf-141">規格需求</span><span class="sxs-lookup"><span data-stu-id="fc7bf-141">Requirements</span></span>



| <span data-ttu-id="fc7bf-142">需求</span><span class="sxs-lookup"><span data-stu-id="fc7bf-142">Requirement</span></span> | <span data-ttu-id="fc7bf-143">值</span><span class="sxs-lookup"><span data-stu-id="fc7bf-143">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="fc7bf-144">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="fc7bf-144">Minimum supported client</span></span><br/> | <span data-ttu-id="fc7bf-145">Windows 8</span><span class="sxs-lookup"><span data-stu-id="fc7bf-145">Windows 8</span></span><br/>                                                                                    |
| <span data-ttu-id="fc7bf-146">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="fc7bf-146">Minimum supported server</span></span><br/> | <span data-ttu-id="fc7bf-147">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="fc7bf-147">Windows Server 2012</span></span><br/>                                                                          |
| <span data-ttu-id="fc7bf-148">命名空間</span><span class="sxs-lookup"><span data-stu-id="fc7bf-148">Namespace</span></span><br/>                | <span data-ttu-id="fc7bf-149">根 \\ 虛擬化 \\ v2</span><span class="sxs-lookup"><span data-stu-id="fc7bf-149">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="fc7bf-150">MOF</span><span class="sxs-lookup"><span data-stu-id="fc7bf-150">MOF</span></span><br/>                      | <dl> <span data-ttu-id="fc7bf-151"><dt>WindowsVirtualization。</dt></span><span class="sxs-lookup"><span data-stu-id="fc7bf-151"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="fc7bf-152">DLL</span><span class="sxs-lookup"><span data-stu-id="fc7bf-152">DLL</span></span><br/>                      | <dl> <span data-ttu-id="fc7bf-153"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="fc7bf-153"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="fc7bf-154">另請參閱</span><span class="sxs-lookup"><span data-stu-id="fc7bf-154">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fc7bf-155">**CIM \_ 功能**</span><span class="sxs-lookup"><span data-stu-id="fc7bf-155">**CIM\_Capabilities**</span></span>](cim-capabilities.md)
</dt> </dl>

 

