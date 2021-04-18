---
description: 代表虛擬系統與最近套用至虛擬系統之快照集的設定資料之間的關聯。
ms.assetid: 9231b441-20c4-468b-905f-5baabc32a8cc
title: Msvm_LastAppliedSnapshot 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_LastAppliedSnapshot
- Msvm_LastAppliedSnapshot.Antecedent
- Msvm_LastAppliedSnapshot.Dependent
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 48854d7b5aaaa6f8026f8dec14745545b0c58806
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106983486"
---
# <a name="msvm_lastappliedsnapshot-class"></a><span data-ttu-id="c39c0-103">Msvm \_ LastAppliedSnapshot 類別</span><span class="sxs-lookup"><span data-stu-id="c39c0-103">Msvm\_LastAppliedSnapshot class</span></span>

<span data-ttu-id="c39c0-104">代表虛擬系統與最近套用至虛擬系統之快照集的設定資料之間的關聯。</span><span class="sxs-lookup"><span data-stu-id="c39c0-104">Represents an association between a virtual system and the setting data of the snapshot that was most recently applied to the virtual system.</span></span>

<span data-ttu-id="c39c0-105">下列語法已簡化受控物件格式 (MOF) 程式碼，並且包含所有繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="c39c0-105">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="c39c0-106">語法</span><span class="sxs-lookup"><span data-stu-id="c39c0-106">Syntax</span></span>

``` syntax
[Association, Aggregation, Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_LastAppliedSnapshot : CIM_LastAppliedSnapshot
{
  CIM_VirtualSystemSettingData REF Antecedent;
  CIM_ComputerSystem           REF Dependent;
};
```

## <a name="members"></a><span data-ttu-id="c39c0-107">成員</span><span class="sxs-lookup"><span data-stu-id="c39c0-107">Members</span></span>

<span data-ttu-id="c39c0-108">**Msvm \_ LastAppliedSnapshot** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="c39c0-108">The **Msvm\_LastAppliedSnapshot** class has these types of members:</span></span>

-   [<span data-ttu-id="c39c0-109">屬性</span><span class="sxs-lookup"><span data-stu-id="c39c0-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="c39c0-110">屬性</span><span class="sxs-lookup"><span data-stu-id="c39c0-110">Properties</span></span>

<span data-ttu-id="c39c0-111">**Msvm \_ LastAppliedSnapshot** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="c39c0-111">The **Msvm\_LastAppliedSnapshot** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="c39c0-112">**先行**</span><span class="sxs-lookup"><span data-stu-id="c39c0-112">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c39c0-113">資料類型： **CIM \_ VirtualSystemSettingData**</span><span class="sxs-lookup"><span data-stu-id="c39c0-113">Data type: **CIM\_VirtualSystemSettingData**</span></span>
</dt> <dt>

<span data-ttu-id="c39c0-114">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="c39c0-114">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c39c0-115">限定詞：覆 **寫**、 **最小** ( 0 ) 、 **最大** ( 1 ) </span><span class="sxs-lookup"><span data-stu-id="c39c0-115">Qualifiers: **Override**, **Min** ( 0 ), **Max** ( 1 )</span></span>
</dt> </dl>

<span data-ttu-id="c39c0-116">參考 [**Msvm \_ VirtualSystemSettingData**](msvm-virtualsystemsettingdata.md) 類別的實例，該類別代表上次套用至虛擬系統的虛擬系統快照。</span><span class="sxs-lookup"><span data-stu-id="c39c0-116">Reference to an instance of the [**Msvm\_VirtualSystemSettingData**](msvm-virtualsystemsettingdata.md) class that represents the virtual system snapshot that was last applied to the virtual system.</span></span> <span data-ttu-id="c39c0-117">這個屬性繼承自 **CIM 相依 \_** 性。</span><span class="sxs-lookup"><span data-stu-id="c39c0-117">This property is inherited from **CIM\_Dependency**.</span></span>

</dd> <dt>

<span data-ttu-id="c39c0-118">**依賴**</span><span class="sxs-lookup"><span data-stu-id="c39c0-118">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c39c0-119">資料類型： **CIM \_** 未執行</span><span class="sxs-lookup"><span data-stu-id="c39c0-119">Data type: **CIM\_ComputerSystem**</span></span>
</dt> <dt>

<span data-ttu-id="c39c0-120">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="c39c0-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c39c0-121">限定詞：覆 **寫**、 **最小** ( 0 ) 、 **最大** ( 1 ) </span><span class="sxs-lookup"><span data-stu-id="c39c0-121">Qualifiers: **Override**, **Min** ( 0 ), **Max** ( 1 )</span></span>
</dt> </dl>

<span data-ttu-id="c39c0-122">參考 [**Msvm \_**](msvm-computersystem.md) 實例類別的實例，此類別代表最近套用了 **先前** 屬性所代表之虛擬系統快照集的虛擬系統。</span><span class="sxs-lookup"><span data-stu-id="c39c0-122">Reference to an instance of the [**Msvm\_ComputerSystem**](msvm-computersystem.md) class that represents the virtual system upon which the virtual system snapshot represented by the **Antecedent** property was most recently applied.</span></span> <span data-ttu-id="c39c0-123">這個屬性繼承自 **CIM 相依 \_** 性。</span><span class="sxs-lookup"><span data-stu-id="c39c0-123">This property is inherited from **CIM\_Dependency**.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="c39c0-124">規格需求</span><span class="sxs-lookup"><span data-stu-id="c39c0-124">Requirements</span></span>



| <span data-ttu-id="c39c0-125">需求</span><span class="sxs-lookup"><span data-stu-id="c39c0-125">Requirement</span></span> | <span data-ttu-id="c39c0-126">值</span><span class="sxs-lookup"><span data-stu-id="c39c0-126">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c39c0-127">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="c39c0-127">Minimum supported client</span></span><br/> | <span data-ttu-id="c39c0-128">\[僅 Windows 8 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="c39c0-128">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="c39c0-129">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="c39c0-129">Minimum supported server</span></span><br/> | <span data-ttu-id="c39c0-130">僅限 Windows Server 2012 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="c39c0-130">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="c39c0-131">命名空間</span><span class="sxs-lookup"><span data-stu-id="c39c0-131">Namespace</span></span><br/>                | <span data-ttu-id="c39c0-132">根 \\ 虛擬化 \\ V2</span><span class="sxs-lookup"><span data-stu-id="c39c0-132">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="c39c0-133">MOF</span><span class="sxs-lookup"><span data-stu-id="c39c0-133">MOF</span></span><br/>                      | <dl> <span data-ttu-id="c39c0-134"><dt>WindowsVirtualization。</dt></span><span class="sxs-lookup"><span data-stu-id="c39c0-134"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="c39c0-135">DLL</span><span class="sxs-lookup"><span data-stu-id="c39c0-135">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c39c0-136"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="c39c0-136"><dt>Vmms.exe</dt></span></span> </dl>                     |



 

 




