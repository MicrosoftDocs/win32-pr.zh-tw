---
description: 表示通訊協定控制器與已公開邏輯單元之間的關聯。
ms.assetid: e8bf2b32-b4a6-4963-8a50-2b06776965e8
title: CIM_ProtocolControllerForUnit 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_ProtocolControllerForUnit
- CIM_ProtocolControllerForUnit.Antecedent
- CIM_ProtocolControllerForUnit.Dependent
- CIM_ProtocolControllerForUnit.DeviceAccess
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 26020745057d5963ed4a892ba8639ac078aaa20b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106998307"
---
# <a name="cim_protocolcontrollerforunit-class"></a><span data-ttu-id="7fa09-103">CIM \_ ProtocolControllerForUnit 類別</span><span class="sxs-lookup"><span data-stu-id="7fa09-103">CIM\_ProtocolControllerForUnit class</span></span>

<span data-ttu-id="7fa09-104">表示通訊協定控制器與已公開邏輯單元之間的關聯。</span><span class="sxs-lookup"><span data-stu-id="7fa09-104">Represents an association between a protocol controller and an exposed logical unit.</span></span>

## <a name="syntax"></a><span data-ttu-id="7fa09-105">語法</span><span class="sxs-lookup"><span data-stu-id="7fa09-105">Syntax</span></span>

``` syntax
[Association, Abstract, Version("2.8.0"), UMLPackagePath("CIM::Device::ProtocolController"), AMENDMENT]
class CIM_ProtocolControllerForUnit : CIM_ProtocolControllerForDevice
{
  CIM_ProtocolController REF Antecedent;
  CIM_LogicalDevice      REF Dependent;
  uint16                     DeviceAccess;
};
```

## <a name="members"></a><span data-ttu-id="7fa09-106">成員</span><span class="sxs-lookup"><span data-stu-id="7fa09-106">Members</span></span>

<span data-ttu-id="7fa09-107">**CIM \_ ProtocolControllerForUnit** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="7fa09-107">The **CIM\_ProtocolControllerForUnit** class has these types of members:</span></span>

-   [<span data-ttu-id="7fa09-108">屬性</span><span class="sxs-lookup"><span data-stu-id="7fa09-108">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="7fa09-109">屬性</span><span class="sxs-lookup"><span data-stu-id="7fa09-109">Properties</span></span>

<span data-ttu-id="7fa09-110">**CIM \_ ProtocolControllerForUnit** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="7fa09-110">The **CIM\_ProtocolControllerForUnit** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="7fa09-111">**先行**</span><span class="sxs-lookup"><span data-stu-id="7fa09-111">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7fa09-112">資料類型： **CIM \_ ProtocolController**</span><span class="sxs-lookup"><span data-stu-id="7fa09-112">Data type: **CIM\_ProtocolController**</span></span>
</dt> <dt>

<span data-ttu-id="7fa09-113">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="7fa09-113">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7fa09-114">限定詞：覆 [**寫**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Antecedent" ) </span><span class="sxs-lookup"><span data-stu-id="7fa09-114">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent")</span></span>
</dt> </dl>

<span data-ttu-id="7fa09-115">通訊協定控制器。</span><span class="sxs-lookup"><span data-stu-id="7fa09-115">The protocol controller.</span></span>

</dd> <dt>

<span data-ttu-id="7fa09-116">**依賴**</span><span class="sxs-lookup"><span data-stu-id="7fa09-116">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7fa09-117">資料類型： **CIM \_ LogicalDevice**</span><span class="sxs-lookup"><span data-stu-id="7fa09-117">Data type: **CIM\_LogicalDevice**</span></span>
</dt> <dt>

<span data-ttu-id="7fa09-118">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="7fa09-118">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7fa09-119">限定詞：覆 [**寫**](/windows/desktop/WmiSdk/standard-qualifiers) ( 「相依」 ) </span><span class="sxs-lookup"><span data-stu-id="7fa09-119">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependent")</span></span>
</dt> </dl>

<span data-ttu-id="7fa09-120">與通訊協定控制器相關聯的邏輯單元。</span><span class="sxs-lookup"><span data-stu-id="7fa09-120">The logical unit associated with the protocol controller.</span></span>

</dd> <dt>

<span data-ttu-id="7fa09-121">**DeviceAccess**</span><span class="sxs-lookup"><span data-stu-id="7fa09-121">**DeviceAccess**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7fa09-122">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="7fa09-122">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="7fa09-123">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="7fa09-123">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7fa09-124">透過通訊協定控制器授與邏輯單元的存取權。</span><span class="sxs-lookup"><span data-stu-id="7fa09-124">The access rights granted to the logical unit through the protocol controller.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="7fa09-125">**未知** 的 (0) </span><span class="sxs-lookup"><span data-stu-id="7fa09-125">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Read_Write"></span><span id="read_write"></span><span id="READ_WRITE"></span>

<span data-ttu-id="7fa09-126">**讀取寫入** (2) </span><span class="sxs-lookup"><span data-stu-id="7fa09-126">**Read Write** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Read-Only"></span><span id="read-only"></span><span id="READ-ONLY"></span>

<span data-ttu-id="7fa09-127">**唯讀** (3) </span><span class="sxs-lookup"><span data-stu-id="7fa09-127">**Read-Only** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="No_Access"></span><span id="no_access"></span><span id="NO_ACCESS"></span>

<span data-ttu-id="7fa09-128">沒有 (4) 的 **存取權**</span><span class="sxs-lookup"><span data-stu-id="7fa09-128">**No Access** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

<span data-ttu-id="7fa09-129">**DMTF 保留** (5. 15999) </span><span class="sxs-lookup"><span data-stu-id="7fa09-129">**DMTF Reserved** (5..15999)</span></span>


</dt> <dd></dd> <dt>

<span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>

<span data-ttu-id="7fa09-130">**廠商保留** (16000 ) </span><span class="sxs-lookup"><span data-stu-id="7fa09-130">**Vendor Reserved** (16000..)</span></span>


<span data-ttu-id="7fa09-131"></dt> <dd></dd> </dl>

</dd> </dl></span><span class="sxs-lookup"><span data-stu-id="7fa09-131"></dt> <dd></dd> </dl>

</dd> </dl></span></span>

## <a name="requirements"></a><span data-ttu-id="7fa09-132">規格需求</span><span class="sxs-lookup"><span data-stu-id="7fa09-132">Requirements</span></span>



| <span data-ttu-id="7fa09-133">需求</span><span class="sxs-lookup"><span data-stu-id="7fa09-133">Requirement</span></span> | <span data-ttu-id="7fa09-134">值</span><span class="sxs-lookup"><span data-stu-id="7fa09-134">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7fa09-135">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="7fa09-135">Minimum supported client</span></span><br/> | <span data-ttu-id="7fa09-136">Windows 8</span><span class="sxs-lookup"><span data-stu-id="7fa09-136">Windows 8</span></span><br/>                                                                                    |
| <span data-ttu-id="7fa09-137">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="7fa09-137">Minimum supported server</span></span><br/> | <span data-ttu-id="7fa09-138">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="7fa09-138">Windows Server 2012</span></span><br/>                                                                          |
| <span data-ttu-id="7fa09-139">命名空間</span><span class="sxs-lookup"><span data-stu-id="7fa09-139">Namespace</span></span><br/>                | <span data-ttu-id="7fa09-140">根 \\ 虛擬化 \\ v2</span><span class="sxs-lookup"><span data-stu-id="7fa09-140">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="7fa09-141">MOF</span><span class="sxs-lookup"><span data-stu-id="7fa09-141">MOF</span></span><br/>                      | <dl> <span data-ttu-id="7fa09-142"><dt>WindowsVirtualization。</dt></span><span class="sxs-lookup"><span data-stu-id="7fa09-142"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="7fa09-143">DLL</span><span class="sxs-lookup"><span data-stu-id="7fa09-143">DLL</span></span><br/>                      | <dl> <span data-ttu-id="7fa09-144"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="7fa09-144"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="7fa09-145">另請參閱</span><span class="sxs-lookup"><span data-stu-id="7fa09-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7fa09-146">**CIM \_ ProtocolControllerForDevice**</span><span class="sxs-lookup"><span data-stu-id="7fa09-146">**CIM\_ProtocolControllerForDevice**</span></span>](cim-protocolcontrollerfordevice.md)
</dt> </dl>

 

