---
description: 描述虛擬綜合顯示控制器的設定資料。
ms.assetid: cea79b24-4175-49db-a8b4-a9efb1fd0b96
title: Msvm_SyntheticDisplayControllerSettingData 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_SyntheticDisplayControllerSettingData
- Msvm_SyntheticDisplayControllerSettingData.ResolutionType
- Msvm_SyntheticDisplayControllerSettingData.HorizontalResolution
- Msvm_SyntheticDisplayControllerSettingData.VerticalResolution
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 52935800eda641eb9015247e9320f33f22b40251
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104192116"
---
# <a name="msvm_syntheticdisplaycontrollersettingdata-class"></a><span data-ttu-id="d69df-103">Msvm \_ SyntheticDisplayControllerSettingData 類別</span><span class="sxs-lookup"><span data-stu-id="d69df-103">Msvm\_SyntheticDisplayControllerSettingData class</span></span>

<span data-ttu-id="d69df-104">描述虛擬綜合顯示控制器的設定資料。</span><span class="sxs-lookup"><span data-stu-id="d69df-104">Describes the setting data for a virtual synthetic display controller.</span></span>

<span data-ttu-id="d69df-105">下列語法是簡化自 MOF 程式碼，且包含所有繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="d69df-105">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="d69df-106">語法</span><span class="sxs-lookup"><span data-stu-id="d69df-106">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_SyntheticDisplayControllerSettingData : CIM_ResourceAllocationSettingData
{
  uint8  ResolutionType;
  uint16 HorizontalResolution;
  uint16 VerticalResolution;
};
```

## <a name="members"></a><span data-ttu-id="d69df-107">成員</span><span class="sxs-lookup"><span data-stu-id="d69df-107">Members</span></span>

<span data-ttu-id="d69df-108">**Msvm \_ SyntheticDisplayControllerSettingData** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="d69df-108">The **Msvm\_SyntheticDisplayControllerSettingData** class has these types of members:</span></span>

-   [<span data-ttu-id="d69df-109">屬性</span><span class="sxs-lookup"><span data-stu-id="d69df-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="d69df-110">屬性</span><span class="sxs-lookup"><span data-stu-id="d69df-110">Properties</span></span>

<span data-ttu-id="d69df-111">**Msvm \_ SyntheticDisplayControllerSettingData** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="d69df-111">The **Msvm\_SyntheticDisplayControllerSettingData** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="d69df-112">**HorizontalResolution**</span><span class="sxs-lookup"><span data-stu-id="d69df-112">**HorizontalResolution**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d69df-113">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="d69df-113">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="d69df-114">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="d69df-114">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="d69df-115">水準解析度。</span><span class="sxs-lookup"><span data-stu-id="d69df-115">The horizontal resolution.</span></span>

</dd> <dt>

<span data-ttu-id="d69df-116">**ResolutionType**</span><span class="sxs-lookup"><span data-stu-id="d69df-116">**ResolutionType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d69df-117">資料類型： **uint8**</span><span class="sxs-lookup"><span data-stu-id="d69df-117">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="d69df-118">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="d69df-118">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d69df-119">解決類型。</span><span class="sxs-lookup"><span data-stu-id="d69df-119">The resolution type.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="d69df-120"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**未知** 的 (0) </span><span class="sxs-lookup"><span data-stu-id="d69df-120"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="d69df-121"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**其他** (1) </span><span class="sxs-lookup"><span data-stu-id="d69df-121"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Maximum"></span><span id="maximum"></span><span id="MAXIMUM"></span>

<span data-ttu-id="d69df-122"><span id="Maximum"></span><span id="maximum"></span><span id="MAXIMUM"></span>**最大** (2) </span><span class="sxs-lookup"><span data-stu-id="d69df-122"><span id="Maximum"></span><span id="maximum"></span><span id="MAXIMUM"></span>**Maximum** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Single"></span><span id="single"></span><span id="SINGLE"></span>

<span data-ttu-id="d69df-123"><span id="Single"></span><span id="single"></span><span id="SINGLE"></span>**單一** (3) </span><span class="sxs-lookup"><span data-stu-id="d69df-123"><span id="Single"></span><span id="single"></span><span id="SINGLE"></span>**Single** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Default"></span><span id="default"></span><span id="DEFAULT"></span>

<span data-ttu-id="d69df-124"><span id="Default"></span><span id="default"></span><span id="DEFAULT"></span>**預設** (4) </span><span class="sxs-lookup"><span data-stu-id="d69df-124"><span id="Default"></span><span id="default"></span><span id="DEFAULT"></span>**Default** (4)</span></span>


</dt> <dd>

> [!Note]  
> <span data-ttu-id="d69df-125">在 Windows 10 1703 版中新增。</span><span class="sxs-lookup"><span data-stu-id="d69df-125">Added in Windows 10, version 1703.</span></span>

 

</dd> </dl>

</dd> <dt>

<span data-ttu-id="d69df-126">**VerticalResolution**</span><span class="sxs-lookup"><span data-stu-id="d69df-126">**VerticalResolution**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d69df-127">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="d69df-127">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="d69df-128">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="d69df-128">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="d69df-129">垂直解析度。</span><span class="sxs-lookup"><span data-stu-id="d69df-129">The vertical resolution.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="d69df-130">規格需求</span><span class="sxs-lookup"><span data-stu-id="d69df-130">Requirements</span></span>



| <span data-ttu-id="d69df-131">需求</span><span class="sxs-lookup"><span data-stu-id="d69df-131">Requirement</span></span> | <span data-ttu-id="d69df-132">值</span><span class="sxs-lookup"><span data-stu-id="d69df-132">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d69df-133">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="d69df-133">Minimum supported client</span></span><br/> | <span data-ttu-id="d69df-134">\[僅 Windows 10 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="d69df-134">Windows 10 \[desktop apps only\]</span></span><br/>                                                             |
| <span data-ttu-id="d69df-135">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="d69df-135">Minimum supported server</span></span><br/> | <span data-ttu-id="d69df-136">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="d69df-136">Windows Server 2016</span></span><br/>                                                                          |
| <span data-ttu-id="d69df-137">命名空間</span><span class="sxs-lookup"><span data-stu-id="d69df-137">Namespace</span></span><br/>                | <span data-ttu-id="d69df-138">根 \\ 虛擬化 \\ v2</span><span class="sxs-lookup"><span data-stu-id="d69df-138">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="d69df-139">MOF</span><span class="sxs-lookup"><span data-stu-id="d69df-139">MOF</span></span><br/>                      | <dl> <span data-ttu-id="d69df-140"><dt>WindowsVirtualization。</dt></span><span class="sxs-lookup"><span data-stu-id="d69df-140"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="d69df-141">DLL</span><span class="sxs-lookup"><span data-stu-id="d69df-141">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d69df-142"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="d69df-142"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="d69df-143">另請參閱</span><span class="sxs-lookup"><span data-stu-id="d69df-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d69df-144">**CIM \_ ResourceAllocationSettingData**</span><span class="sxs-lookup"><span data-stu-id="d69df-144">**CIM\_ResourceAllocationSettingData**</span></span>](cim-resourceallocationsettingdata.md)
</dt> </dl>

 

 




