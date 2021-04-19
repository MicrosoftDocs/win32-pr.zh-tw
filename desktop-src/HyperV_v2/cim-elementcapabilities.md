---
description: 代表 managed 元素與其功能之間的關聯。
ms.assetid: 0e080042-4a56-40b7-acc5-cf69eb2a0604
title: CIM_ElementCapabilities 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_ElementCapabilities
- CIM_ElementCapabilities.ManagedElement
- CIM_ElementCapabilities.Capabilities
- CIM_ElementCapabilities.Characteristics
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 7c705d0bb4743d4919ca840f51b3324510558078
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106973503"
---
# <a name="cim_elementcapabilities-class"></a><span data-ttu-id="449e5-103">CIM \_ ElementCapabilities 類別</span><span class="sxs-lookup"><span data-stu-id="449e5-103">CIM\_ElementCapabilities class</span></span>

<span data-ttu-id="449e5-104">代表 managed 元素與其功能之間的關聯。</span><span class="sxs-lookup"><span data-stu-id="449e5-104">Represents an association between a managed element and its capabilities.</span></span>

## <a name="syntax"></a><span data-ttu-id="449e5-105">語法</span><span class="sxs-lookup"><span data-stu-id="449e5-105">Syntax</span></span>

``` syntax
[Association, Abstract, Version("2.24.0"), UMLPackagePath("CIM::Core::Capabilities"), AMENDMENT]
class CIM_ElementCapabilities
{
  CIM_ManagedElement REF ManagedElement;
  CIM_Capabilities   REF Capabilities;
  uint16                 Characteristics[];
};
```

## <a name="members"></a><span data-ttu-id="449e5-106">成員</span><span class="sxs-lookup"><span data-stu-id="449e5-106">Members</span></span>

<span data-ttu-id="449e5-107">**CIM \_ ElementCapabilities** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="449e5-107">The **CIM\_ElementCapabilities** class has these types of members:</span></span>

-   [<span data-ttu-id="449e5-108">屬性</span><span class="sxs-lookup"><span data-stu-id="449e5-108">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="449e5-109">屬性</span><span class="sxs-lookup"><span data-stu-id="449e5-109">Properties</span></span>

<span data-ttu-id="449e5-110">**CIM \_ ElementCapabilities** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="449e5-110">The **CIM\_ElementCapabilities** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="449e5-111">**Capabilities**</span><span class="sxs-lookup"><span data-stu-id="449e5-111">**Capabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="449e5-112">資料類型： **CIM \_ 功能**</span><span class="sxs-lookup"><span data-stu-id="449e5-112">Data type: **CIM\_Capabilities**</span></span>
</dt> <dt>

<span data-ttu-id="449e5-113">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="449e5-113">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="449e5-114">限定詞：索引 [**鍵**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="449e5-114">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="449e5-115">與 managed 元素相關聯的功能。</span><span class="sxs-lookup"><span data-stu-id="449e5-115">The capabilities associated with the managed element.</span></span>

</dd> <dt>

<span data-ttu-id="449e5-116">**特性**</span><span class="sxs-lookup"><span data-stu-id="449e5-116">**Characteristics**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="449e5-117">資料類型： **uint16** 陣列</span><span class="sxs-lookup"><span data-stu-id="449e5-117">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="449e5-118">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="449e5-118">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="449e5-119">一組有關功能的描述性資訊。</span><span class="sxs-lookup"><span data-stu-id="449e5-119">A set of descriptive information about the capabilities.</span></span>

<dt>

<span id="Default"></span><span id="default"></span><span id="DEFAULT"></span>

<span data-ttu-id="449e5-120">**預設** (2) </span><span class="sxs-lookup"><span data-stu-id="449e5-120">**Default** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Current"></span><span id="current"></span><span id="CURRENT"></span>

<span data-ttu-id="449e5-121">**目前** 的 (3) </span><span class="sxs-lookup"><span data-stu-id="449e5-121">**Current** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

<span data-ttu-id="449e5-122">**DMTF 保留** ( .。。) </span><span class="sxs-lookup"><span data-stu-id="449e5-122">**DMTF Reserved** (..)</span></span>


</dt> <dd></dd> <dt>

<span id="Vendor_Specific"></span><span id="vendor_specific"></span><span id="VENDOR_SPECIFIC"></span>

<span data-ttu-id="449e5-123">**廠商特定** (32768. 65535) </span><span class="sxs-lookup"><span data-stu-id="449e5-123">**Vendor Specific** (32768..65535)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="449e5-124">**ManagedElement**</span><span class="sxs-lookup"><span data-stu-id="449e5-124">**ManagedElement**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="449e5-125">資料類型： **CIM \_ ManagedElement**</span><span class="sxs-lookup"><span data-stu-id="449e5-125">Data type: **CIM\_ManagedElement**</span></span>
</dt> <dt>

<span data-ttu-id="449e5-126">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="449e5-126">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="449e5-127">限定詞： [**Key**](/windows/desktop/WmiSdk/key-qualifier)、 [**Min**](/windows/desktop/WmiSdk/standard-qualifiers) (1) </span><span class="sxs-lookup"><span data-stu-id="449e5-127">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**Min**](/windows/desktop/WmiSdk/standard-qualifiers) (1)</span></span>
</dt> </dl>

<span data-ttu-id="449e5-128">Managed 元素。</span><span class="sxs-lookup"><span data-stu-id="449e5-128">The managed element.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="449e5-129">規格需求</span><span class="sxs-lookup"><span data-stu-id="449e5-129">Requirements</span></span>



| <span data-ttu-id="449e5-130">需求</span><span class="sxs-lookup"><span data-stu-id="449e5-130">Requirement</span></span> | <span data-ttu-id="449e5-131">值</span><span class="sxs-lookup"><span data-stu-id="449e5-131">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="449e5-132">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="449e5-132">Minimum supported client</span></span><br/> | <span data-ttu-id="449e5-133">Windows 8</span><span class="sxs-lookup"><span data-stu-id="449e5-133">Windows 8</span></span><br/>                                                                                    |
| <span data-ttu-id="449e5-134">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="449e5-134">Minimum supported server</span></span><br/> | <span data-ttu-id="449e5-135">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="449e5-135">Windows Server 2012</span></span><br/>                                                                          |
| <span data-ttu-id="449e5-136">命名空間</span><span class="sxs-lookup"><span data-stu-id="449e5-136">Namespace</span></span><br/>                | <span data-ttu-id="449e5-137">根 \\ 虛擬化 \\ v2</span><span class="sxs-lookup"><span data-stu-id="449e5-137">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="449e5-138">MOF</span><span class="sxs-lookup"><span data-stu-id="449e5-138">MOF</span></span><br/>                      | <dl> <span data-ttu-id="449e5-139"><dt>WindowsVirtualization。</dt></span><span class="sxs-lookup"><span data-stu-id="449e5-139"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="449e5-140">DLL</span><span class="sxs-lookup"><span data-stu-id="449e5-140">DLL</span></span><br/>                      | <dl> <span data-ttu-id="449e5-141"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="449e5-141"><dt>Vmms.exe</dt></span></span> </dl>                     |



 

