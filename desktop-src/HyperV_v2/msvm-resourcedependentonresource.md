---
description: 建立 \_ 代表資源配置的 CIM ResourceAllocationSettingData 實例取決於另一個資源配置。
ms.assetid: 567ee36a-d47b-444d-8d2f-425873f95bef
title: Msvm_ResourceDependentOnResource 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ResourceDependentOnResource
- Msvm_ResourceDependentOnResource.Antecedent
- Msvm_ResourceDependentOnResource.Dependent
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 29cf3b607449c6a9145568e3ee858248af3c4248
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106980347"
---
# <a name="msvm_resourcedependentonresource-class"></a><span data-ttu-id="6c8c3-103">Msvm \_ ResourceDependentOnResource 類別</span><span class="sxs-lookup"><span data-stu-id="6c8c3-103">Msvm\_ResourceDependentOnResource class</span></span>

<span data-ttu-id="6c8c3-104">建立代表資源配置的 [**CIM \_ ResourceAllocationSettingData**](cim-resourceallocationsettingdata.md) 實例取決於另一個資源配置。</span><span class="sxs-lookup"><span data-stu-id="6c8c3-104">Establishes that a [**CIM\_ResourceAllocationSettingData**](cim-resourceallocationsettingdata.md) instance representing a resource allocation depends on another resource allocation.</span></span>

<span data-ttu-id="6c8c3-105">下列語法已經過受管理物件格式 (MOF) 程式碼簡化，並包含所有已繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="6c8c3-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="6c8c3-106">語法</span><span class="sxs-lookup"><span data-stu-id="6c8c3-106">Syntax</span></span>

``` syntax
[Association, Aggregation, Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_ResourceDependentOnResource : CIM_Dependency
{
  CIM_ResourceAllocationSettingData REF Antecedent;
  CIM_ResourceAllocationSettingData REF Dependent;
};
```

## <a name="members"></a><span data-ttu-id="6c8c3-107">成員</span><span class="sxs-lookup"><span data-stu-id="6c8c3-107">Members</span></span>

<span data-ttu-id="6c8c3-108">**Msvm \_ ResourceDependentOnResource** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="6c8c3-108">The **Msvm\_ResourceDependentOnResource** class has these types of members:</span></span>

-   [<span data-ttu-id="6c8c3-109">屬性</span><span class="sxs-lookup"><span data-stu-id="6c8c3-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="6c8c3-110">屬性</span><span class="sxs-lookup"><span data-stu-id="6c8c3-110">Properties</span></span>

<span data-ttu-id="6c8c3-111">**Msvm \_ ResourceDependentOnResource** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="6c8c3-111">The **Msvm\_ResourceDependentOnResource** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="6c8c3-112">**先行**</span><span class="sxs-lookup"><span data-stu-id="6c8c3-112">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6c8c3-113">資料類型： **CIM \_ ResourceAllocationSettingData**</span><span class="sxs-lookup"><span data-stu-id="6c8c3-113">Data type: **CIM\_ResourceAllocationSettingData**</span></span>
</dt> <dt>

<span data-ttu-id="6c8c3-114">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="6c8c3-114">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6c8c3-115">限定詞： [**Key**](/windows/desktop/WmiSdk/key-qualifier)、 [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Antecedent" ) </span><span class="sxs-lookup"><span data-stu-id="6c8c3-115">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent")</span></span>
</dt> </dl>

<span data-ttu-id="6c8c3-116">[**CIM \_ ResourceAllocationSettingData**](cim-resourceallocationsettingdata.md) ，表示此關聯中的獨立資源。</span><span class="sxs-lookup"><span data-stu-id="6c8c3-116">A [**CIM\_ResourceAllocationSettingData**](cim-resourceallocationsettingdata.md) that represents the independent resource in this association.</span></span>

</dd> <dt>

<span data-ttu-id="6c8c3-117">**依賴**</span><span class="sxs-lookup"><span data-stu-id="6c8c3-117">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6c8c3-118">資料類型： **CIM \_ ResourceAllocationSettingData**</span><span class="sxs-lookup"><span data-stu-id="6c8c3-118">Data type: **CIM\_ResourceAllocationSettingData**</span></span>
</dt> <dt>

<span data-ttu-id="6c8c3-119">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="6c8c3-119">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6c8c3-120">限定詞： [**Key**](/windows/desktop/WmiSdk/key-qualifier)、 [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ( 「相依」 ) </span><span class="sxs-lookup"><span data-stu-id="6c8c3-120">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependent")</span></span>
</dt> </dl>

<span data-ttu-id="6c8c3-121">[**CIM \_ ResourceAllocationSettingData**](cim-resourceallocationsettingdata.md) ，表示相依于前一項的資源。</span><span class="sxs-lookup"><span data-stu-id="6c8c3-121">A [**CIM\_ResourceAllocationSettingData**](cim-resourceallocationsettingdata.md) that represents the resource that is dependent on the Antecedent.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="6c8c3-122">規格需求</span><span class="sxs-lookup"><span data-stu-id="6c8c3-122">Requirements</span></span>



| <span data-ttu-id="6c8c3-123">需求</span><span class="sxs-lookup"><span data-stu-id="6c8c3-123">Requirement</span></span> | <span data-ttu-id="6c8c3-124">值</span><span class="sxs-lookup"><span data-stu-id="6c8c3-124">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6c8c3-125">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="6c8c3-125">Minimum supported client</span></span><br/> | <span data-ttu-id="6c8c3-126">\[僅 Windows 10 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="6c8c3-126">Windows 10 \[desktop apps only\]</span></span><br/>                                                             |
| <span data-ttu-id="6c8c3-127">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="6c8c3-127">Minimum supported server</span></span><br/> | <span data-ttu-id="6c8c3-128">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="6c8c3-128">Windows Server 2016</span></span><br/>                                                                          |
| <span data-ttu-id="6c8c3-129">命名空間</span><span class="sxs-lookup"><span data-stu-id="6c8c3-129">Namespace</span></span><br/>                | <span data-ttu-id="6c8c3-130">根 \\ 虛擬化 \\ v2</span><span class="sxs-lookup"><span data-stu-id="6c8c3-130">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="6c8c3-131">MOF</span><span class="sxs-lookup"><span data-stu-id="6c8c3-131">MOF</span></span><br/>                      | <dl> <span data-ttu-id="6c8c3-132"><dt>WindowsVirtualization。</dt></span><span class="sxs-lookup"><span data-stu-id="6c8c3-132"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="6c8c3-133">DLL</span><span class="sxs-lookup"><span data-stu-id="6c8c3-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6c8c3-134"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="6c8c3-134"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="6c8c3-135">另請參閱</span><span class="sxs-lookup"><span data-stu-id="6c8c3-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6c8c3-136">**CIM \_ 相依性**</span><span class="sxs-lookup"><span data-stu-id="6c8c3-136">**CIM\_Dependency**</span></span>](cim-dependency.md)
</dt> </dl>

 

