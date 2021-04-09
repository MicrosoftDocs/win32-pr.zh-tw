---
description: 將虛擬系統與從虛擬系統所捕獲的快照集產生關聯。
ms.assetid: CF1C1C04-02BC-4AC3-8327-FEE54ECE8541
title: Msvm_SnapshotOfVirtualSystem 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_SnapshotOfVirtualSystem
- Msvm_SnapshotOfVirtualSystem.Antecedent
- Msvm_SnapshotOfVirtualSystem.Dependent
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: bd006093347d7eb9354944409082a0e069b0cd54
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103943773"
---
# <a name="msvm_snapshotofvirtualsystem-class"></a><span data-ttu-id="82692-103">Msvm \_ SnapshotOfVirtualSystem 類別</span><span class="sxs-lookup"><span data-stu-id="82692-103">Msvm\_SnapshotOfVirtualSystem class</span></span>

<span data-ttu-id="82692-104">將虛擬系統與從虛擬系統所捕獲的快照集產生關聯。</span><span class="sxs-lookup"><span data-stu-id="82692-104">Associates a virtual system with a snapshot that was captured from the virtual system.</span></span>

<span data-ttu-id="82692-105">下列語法已簡化受控物件格式 (MOF) 程式碼，並且包含所有繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="82692-105">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="82692-106">語法</span><span class="sxs-lookup"><span data-stu-id="82692-106">Syntax</span></span>

``` syntax
[Association, Aggregation, Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_SnapshotOfVirtualSystem : CIM_SnapshotOfVirtualSystem
{
  Msvm_ComputerSystem           REF Antecedent;
  Msvm_VirtualSystemSettingData REF Dependent;
};
```

## <a name="members"></a><span data-ttu-id="82692-107">成員</span><span class="sxs-lookup"><span data-stu-id="82692-107">Members</span></span>

<span data-ttu-id="82692-108">**Msvm \_ SnapshotOfVirtualSystem** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="82692-108">The **Msvm\_SnapshotOfVirtualSystem** class has these types of members:</span></span>

-   [<span data-ttu-id="82692-109">屬性</span><span class="sxs-lookup"><span data-stu-id="82692-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="82692-110">屬性</span><span class="sxs-lookup"><span data-stu-id="82692-110">Properties</span></span>

<span data-ttu-id="82692-111">**Msvm \_ SnapshotOfVirtualSystem** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="82692-111">The **Msvm\_SnapshotOfVirtualSystem** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="82692-112">**先行**</span><span class="sxs-lookup"><span data-stu-id="82692-112">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="82692-113">資料類型： **[ **Msvm \_**](msvm-computersystem.md)**</span><span class="sxs-lookup"><span data-stu-id="82692-113">Data type: **[**Msvm\_ComputerSystem**](msvm-computersystem.md)**</span></span>
</dt> <dt>

<span data-ttu-id="82692-114">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="82692-114">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="82692-115">代表虛擬系統之 [**Msvm \_**](msvm-computersystem.md) 實例類別的實例參考。</span><span class="sxs-lookup"><span data-stu-id="82692-115">A reference to an instance of the [**Msvm\_ComputerSystem**](msvm-computersystem.md) class that represents the virtual system.</span></span> <span data-ttu-id="82692-116">此屬性衍生自 [**CIM 相依 \_**](/windows/desktop/CIMWin32Prov/cim-dependency)性。</span><span class="sxs-lookup"><span data-stu-id="82692-116">This property is derived from [**CIM\_Dependency**](/windows/desktop/CIMWin32Prov/cim-dependency).</span></span>

</dd> <dt>

<span data-ttu-id="82692-117">**依賴**</span><span class="sxs-lookup"><span data-stu-id="82692-117">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="82692-118">資料類型： **[ **Msvm \_ VirtualSystemSettingData**](msvm-virtualsystemsettingdata.md)**</span><span class="sxs-lookup"><span data-stu-id="82692-118">Data type: **[**Msvm\_VirtualSystemSettingData**](msvm-virtualsystemsettingdata.md)**</span></span>
</dt> <dt>

<span data-ttu-id="82692-119">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="82692-119">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="82692-120">代表快照集之 [**Msvm \_ VirtualSystemSettingData**](msvm-virtualsystemsettingdata.md) 類別實例的參考。</span><span class="sxs-lookup"><span data-stu-id="82692-120">A reference to an instance of the [**Msvm\_VirtualSystemSettingData**](msvm-virtualsystemsettingdata.md) class that represents the snapshot.</span></span> <span data-ttu-id="82692-121">此屬性衍生自 [**CIM 相依 \_**](/windows/desktop/CIMWin32Prov/cim-dependency)性。</span><span class="sxs-lookup"><span data-stu-id="82692-121">This property is derived from [**CIM\_Dependency**](/windows/desktop/CIMWin32Prov/cim-dependency).</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="82692-122">規格需求</span><span class="sxs-lookup"><span data-stu-id="82692-122">Requirements</span></span>



| <span data-ttu-id="82692-123">需求</span><span class="sxs-lookup"><span data-stu-id="82692-123">Requirement</span></span> | <span data-ttu-id="82692-124">值</span><span class="sxs-lookup"><span data-stu-id="82692-124">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="82692-125">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="82692-125">Minimum supported client</span></span><br/> | <span data-ttu-id="82692-126">\[僅 Windows 8 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="82692-126">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="82692-127">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="82692-127">Minimum supported server</span></span><br/> | <span data-ttu-id="82692-128">僅限 Windows Server 2012 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="82692-128">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="82692-129">命名空間</span><span class="sxs-lookup"><span data-stu-id="82692-129">Namespace</span></span><br/>                | <span data-ttu-id="82692-130">根 \\ 虛擬化 \\ V2</span><span class="sxs-lookup"><span data-stu-id="82692-130">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="82692-131">MOF</span><span class="sxs-lookup"><span data-stu-id="82692-131">MOF</span></span><br/>                      | <dl> <span data-ttu-id="82692-132"><dt>WindowsVirtualization。</dt></span><span class="sxs-lookup"><span data-stu-id="82692-132"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="82692-133">DLL</span><span class="sxs-lookup"><span data-stu-id="82692-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="82692-134"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="82692-134"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="82692-135">另請參閱</span><span class="sxs-lookup"><span data-stu-id="82692-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="82692-136">**CIM \_ SnapshotOfVirtualSystem**</span><span class="sxs-lookup"><span data-stu-id="82692-136">**CIM\_SnapshotOfVirtualSystem**</span></span>](cim-snapshotofvirtualsystem.md)
</dt> <dt>

[<span data-ttu-id="82692-137">**>icloudblob.createsnapshot**</span><span class="sxs-lookup"><span data-stu-id="82692-137">**CreateSnapshot**</span></span>](createsnapshot-msvm-virtualsystemsnapshotservice.md)
</dt> </dl>

 

