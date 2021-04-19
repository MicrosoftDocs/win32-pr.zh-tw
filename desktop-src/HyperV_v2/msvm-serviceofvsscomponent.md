---
description: Msvm \_ VssComponent 實例和 Msvm VssService 實例之間的關聯 \_ ，代表在 VSS 元件上執行作業的服務。
ms.assetid: 19fdf2e3-48c4-452b-89d0-ec0b8681fca2
title: Msvm_ServiceOfVssComponent 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ServiceOfVssComponent
- Msvm_ServiceOfVssComponent.Antecedent
- Msvm_ServiceOfVssComponent.Dependent
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 5787dcdd4d8ce1aeefdc1fbafb2c156aec4d467a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106987230"
---
# <a name="msvm_serviceofvsscomponent-class"></a><span data-ttu-id="4e3b0-103">Msvm \_ ServiceOfVssComponent 類別</span><span class="sxs-lookup"><span data-stu-id="4e3b0-103">Msvm\_ServiceOfVssComponent class</span></span>

<span data-ttu-id="4e3b0-104">[**Msvm \_ VssComponent**](msvm-vsscomponent.md)實例和 [**Msvm \_ VssService**](msvm-vssservice.md)實例之間的關聯，代表在 VSS 元件上執行作業的服務。</span><span class="sxs-lookup"><span data-stu-id="4e3b0-104">An association between an instance of [**Msvm\_VssComponent**](msvm-vsscomponent.md) and an instance of [**Msvm\_VssService**](msvm-vssservice.md) that represents a service for performing operations on the VSS component.</span></span>

<span data-ttu-id="4e3b0-105">下列語法已經過受管理物件格式 (MOF) 程式碼簡化，並包含所有已繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="4e3b0-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="4e3b0-106">語法</span><span class="sxs-lookup"><span data-stu-id="4e3b0-106">Syntax</span></span>

``` syntax
[Association, Aggregation, Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_ServiceOfVssComponent : CIM_Dependency
{
  Msvm_VssComponent REF Antecedent;
  Msvm_VssService   REF Dependent;
};
```

## <a name="members"></a><span data-ttu-id="4e3b0-107">成員</span><span class="sxs-lookup"><span data-stu-id="4e3b0-107">Members</span></span>

<span data-ttu-id="4e3b0-108">**Msvm \_ ServiceOfVssComponent** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="4e3b0-108">The **Msvm\_ServiceOfVssComponent** class has these types of members:</span></span>

-   [<span data-ttu-id="4e3b0-109">屬性</span><span class="sxs-lookup"><span data-stu-id="4e3b0-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="4e3b0-110">屬性</span><span class="sxs-lookup"><span data-stu-id="4e3b0-110">Properties</span></span>

<span data-ttu-id="4e3b0-111">**Msvm \_ ServiceOfVssComponent** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="4e3b0-111">The **Msvm\_ServiceOfVssComponent** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="4e3b0-112">**先行**</span><span class="sxs-lookup"><span data-stu-id="4e3b0-112">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4e3b0-113">資料類型： **Msvm \_ VssComponent**</span><span class="sxs-lookup"><span data-stu-id="4e3b0-113">Data type: **Msvm\_VssComponent**</span></span>
</dt> <dt>

<span data-ttu-id="4e3b0-114">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="4e3b0-114">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4e3b0-115">限定詞：覆 [**寫**](/windows/desktop/WmiSdk/standard-qualifiers) ( 「CIM 相依性 \_ 。前面」 ) </span><span class="sxs-lookup"><span data-stu-id="4e3b0-115">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("CIM\_Dependency.Antecedent")</span></span>
</dt> </dl>

<span data-ttu-id="4e3b0-116">代表 VSS 元件的 [**Msvm \_ VssComponent**](msvm-vsscomponent.md) 。</span><span class="sxs-lookup"><span data-stu-id="4e3b0-116">A, [**Msvm\_VssComponent**](msvm-vsscomponent.md) that represents the VSS component.</span></span>

</dd> <dt>

<span data-ttu-id="4e3b0-117">**依賴**</span><span class="sxs-lookup"><span data-stu-id="4e3b0-117">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4e3b0-118">資料類型： **Msvm \_ VssService**</span><span class="sxs-lookup"><span data-stu-id="4e3b0-118">Data type: **Msvm\_VssService**</span></span>
</dt> <dt>

<span data-ttu-id="4e3b0-119">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="4e3b0-119">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4e3b0-120">限定詞：覆 [**寫**](/windows/desktop/WmiSdk/standard-qualifiers) ( 「CIM 相依性依存」 \_ ) </span><span class="sxs-lookup"><span data-stu-id="4e3b0-120">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("CIM\_Dependency.Dependent")</span></span>
</dt> </dl>

<span data-ttu-id="4e3b0-121">代表 VSS IC 服務的 [**Msvm \_ VssService**](msvm-vssservice.md) 。</span><span class="sxs-lookup"><span data-stu-id="4e3b0-121">An [**Msvm\_VssService**](msvm-vssservice.md) that represents the VSS IC service.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="4e3b0-122">規格需求</span><span class="sxs-lookup"><span data-stu-id="4e3b0-122">Requirements</span></span>



| <span data-ttu-id="4e3b0-123">需求</span><span class="sxs-lookup"><span data-stu-id="4e3b0-123">Requirement</span></span> | <span data-ttu-id="4e3b0-124">值</span><span class="sxs-lookup"><span data-stu-id="4e3b0-124">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4e3b0-125">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="4e3b0-125">Minimum supported client</span></span><br/> | <span data-ttu-id="4e3b0-126">\[僅 Windows 10 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="4e3b0-126">Windows 10 \[desktop apps only\]</span></span><br/>                                                             |
| <span data-ttu-id="4e3b0-127">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="4e3b0-127">Minimum supported server</span></span><br/> | <span data-ttu-id="4e3b0-128">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="4e3b0-128">Windows Server 2016</span></span><br/>                                                                          |
| <span data-ttu-id="4e3b0-129">命名空間</span><span class="sxs-lookup"><span data-stu-id="4e3b0-129">Namespace</span></span><br/>                | <span data-ttu-id="4e3b0-130">根 \\ 虛擬化 \\ v2</span><span class="sxs-lookup"><span data-stu-id="4e3b0-130">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="4e3b0-131">MOF</span><span class="sxs-lookup"><span data-stu-id="4e3b0-131">MOF</span></span><br/>                      | <dl> <span data-ttu-id="4e3b0-132"><dt>WindowsVirtualization。</dt></span><span class="sxs-lookup"><span data-stu-id="4e3b0-132"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="4e3b0-133">DLL</span><span class="sxs-lookup"><span data-stu-id="4e3b0-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="4e3b0-134"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="4e3b0-134"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="4e3b0-135">另請參閱</span><span class="sxs-lookup"><span data-stu-id="4e3b0-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4e3b0-136">**CIM \_ 相依性**</span><span class="sxs-lookup"><span data-stu-id="4e3b0-136">**CIM\_Dependency**</span></span>](cim-dependency.md)
</dt> </dl>

 

