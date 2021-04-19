---
description: 表示 PCI Express 埠已設定的狀態。
ms.assetid: adb03dd7-5a47-47e6-a4e4-28224164150c
title: Msvm_PciExpressSettingData 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_PciExpressSettingData
- Msvm_PciExpressSettingData.VirtualFunctions
- Msvm_PciExpressSettingData.VirtualSystemIdentifiers
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: c092cbc119506c4c52bc0565cd969426feffc481
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106983891"
---
# <a name="msvm_pciexpresssettingdata-class"></a><span data-ttu-id="1b151-103">Msvm \_ PciExpressSettingData 類別</span><span class="sxs-lookup"><span data-stu-id="1b151-103">Msvm\_PciExpressSettingData class</span></span>

<span data-ttu-id="1b151-104">表示 PCI Express 埠已設定的狀態。</span><span class="sxs-lookup"><span data-stu-id="1b151-104">Represents the configured state of a PCI Express port.</span></span>

<span data-ttu-id="1b151-105">下列語法已經過受管理物件格式 (MOF) 程式碼簡化，並包含所有已繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="1b151-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="1b151-106">語法</span><span class="sxs-lookup"><span data-stu-id="1b151-106">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_PciExpressSettingData : CIM_ResourceAllocationSettingData
{
  uint16 VirtualFunctions[];
  string VirtualSystemIdentifiers[];
};
```

## <a name="members"></a><span data-ttu-id="1b151-107">成員</span><span class="sxs-lookup"><span data-stu-id="1b151-107">Members</span></span>

<span data-ttu-id="1b151-108">**Msvm \_ PciExpressSettingData** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="1b151-108">The **Msvm\_PciExpressSettingData** class has these types of members:</span></span>

-   [<span data-ttu-id="1b151-109">屬性</span><span class="sxs-lookup"><span data-stu-id="1b151-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="1b151-110">屬性</span><span class="sxs-lookup"><span data-stu-id="1b151-110">Properties</span></span>

<span data-ttu-id="1b151-111">**Msvm \_ PciExpressSettingData** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="1b151-111">The **Msvm\_PciExpressSettingData** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="1b151-112">**VirtualFunctions**</span><span class="sxs-lookup"><span data-stu-id="1b151-112">**VirtualFunctions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1b151-113">資料類型： **uint16** 陣列</span><span class="sxs-lookup"><span data-stu-id="1b151-113">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="1b151-114">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="1b151-114">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="1b151-115">要指派給 VM 的虛擬函式編號。</span><span class="sxs-lookup"><span data-stu-id="1b151-115">The virtual function number to assign to the VM.</span></span>

</dd> <dt>

<span data-ttu-id="1b151-116">**VirtualSystemIdentifiers**</span><span class="sxs-lookup"><span data-stu-id="1b151-116">**VirtualSystemIdentifiers**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1b151-117">資料類型： **字串** 陣列</span><span class="sxs-lookup"><span data-stu-id="1b151-117">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="1b151-118">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="1b151-118">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1b151-119">限定詞： [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ( 「已編制索引」 ) </span><span class="sxs-lookup"><span data-stu-id="1b151-119">Qualifiers: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed")</span></span>
</dt> </dl>

<span data-ttu-id="1b151-120">此資源之識別碼的自由格式字串陣列，會呈現給虛擬電腦系統的作業系統。</span><span class="sxs-lookup"><span data-stu-id="1b151-120">A free-form string array of identifiers of this resource presented to the virtual computer system's operating system.</span></span> <span data-ttu-id="1b151-121">每個索引的索引和值都是以每個資源為基礎來定義 (也就是每個列舉的 **ResourceType** 值) 。</span><span class="sxs-lookup"><span data-stu-id="1b151-121">The indexes and values per index are defined on a per resource basis (that is, for each enumerated **ResourceType** value).</span></span> <span data-ttu-id="1b151-122">這個屬性會設定為 "GUID"。</span><span class="sxs-lookup"><span data-stu-id="1b151-122">This property is set to "GUID".</span></span>

<span data-ttu-id="1b151-123">這是唯讀屬性，但是可以使用 sd 類別的 [**ModifyVirtualSystemResources**](/previous-versions/windows/desktop/virtual/modifyvirtualsystemresources-msvm-virtualsystemmanagementservice) 方法來變更。</span><span class="sxs-lookup"><span data-stu-id="1b151-123">This is a read-only property, but it can be changed using the [**ModifyVirtualSystemResources**](/previous-versions/windows/desktop/virtual/modifyvirtualsystemresources-msvm-virtualsystemmanagementservice) method of the sd class.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="1b151-124">規格需求</span><span class="sxs-lookup"><span data-stu-id="1b151-124">Requirements</span></span>



| <span data-ttu-id="1b151-125">需求</span><span class="sxs-lookup"><span data-stu-id="1b151-125">Requirement</span></span> | <span data-ttu-id="1b151-126">值</span><span class="sxs-lookup"><span data-stu-id="1b151-126">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1b151-127">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="1b151-127">Minimum supported client</span></span><br/> | <span data-ttu-id="1b151-128">Windows 10， \[ 僅限1703版桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="1b151-128">Windows 10, version 1703 \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="1b151-129">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="1b151-129">Minimum supported server</span></span><br/> | <span data-ttu-id="1b151-130">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="1b151-130">Windows Server 2016</span></span><br/>                                                                          |
| <span data-ttu-id="1b151-131">命名空間</span><span class="sxs-lookup"><span data-stu-id="1b151-131">Namespace</span></span><br/>                | <span data-ttu-id="1b151-132">根 \\ 虛擬化 \\ v2</span><span class="sxs-lookup"><span data-stu-id="1b151-132">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="1b151-133">MOF</span><span class="sxs-lookup"><span data-stu-id="1b151-133">MOF</span></span><br/>                      | <dl> <span data-ttu-id="1b151-134"><dt>WindowsVirtualization。</dt></span><span class="sxs-lookup"><span data-stu-id="1b151-134"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="1b151-135">DLL</span><span class="sxs-lookup"><span data-stu-id="1b151-135">DLL</span></span><br/>                      | <dl> <span data-ttu-id="1b151-136"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="1b151-136"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="1b151-137">另請參閱</span><span class="sxs-lookup"><span data-stu-id="1b151-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1b151-138">**CIM \_ ResourceAllocationSettingData**</span><span class="sxs-lookup"><span data-stu-id="1b151-138">**CIM\_ResourceAllocationSettingData**</span></span>](cim-resourceallocationsettingdata.md)
</dt> </dl>

 

