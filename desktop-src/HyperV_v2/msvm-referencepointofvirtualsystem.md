---
description: 將 Msvm \_ VirtualSystemReferencePoint 與對應的 Msvm \_ VirtualSystem 物件產生關聯。
ms.assetid: 5a9cb099-c0ae-4088-a64c-f2720a6cb9c8
title: Msvm_ReferencePointOfVirtualSystem 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ReferencePointOfVirtualSystem
- Msvm_ReferencePointOfVirtualSystem.Antecedent
- Msvm_ReferencePointOfVirtualSystem.Dependent
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 8debe1931154c5c7a7868e8ee301daf977076b57
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103693239"
---
# <a name="msvm_referencepointofvirtualsystem-class"></a><span data-ttu-id="6524b-103">Msvm \_ ReferencePointOfVirtualSystem 類別</span><span class="sxs-lookup"><span data-stu-id="6524b-103">Msvm\_ReferencePointOfVirtualSystem class</span></span>

<span data-ttu-id="6524b-104">將 [**Msvm \_ VirtualSystemReferencePoint**](msvm-virtualsystemreferencepoint.md) 與對應的 [**Msvm \_ VirtualSystem**](msvm-virtualsystemresourcecomponent.md) 物件產生關聯。</span><span class="sxs-lookup"><span data-stu-id="6524b-104">Associates the [**Msvm\_VirtualSystemReferencePoint**](msvm-virtualsystemreferencepoint.md) to the corresponding [**Msvm\_VirtualSystem**](msvm-virtualsystemresourcecomponent.md) objects.</span></span>

<span data-ttu-id="6524b-105">下列語法已經過受管理物件格式 (MOF) 程式碼簡化，並包含所有已繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="6524b-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="6524b-106">語法</span><span class="sxs-lookup"><span data-stu-id="6524b-106">Syntax</span></span>

``` syntax
[Association, Aggregation, Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_ReferencePointOfVirtualSystem : CIM_Dependency
{
  Msvm_ComputerSystem              REF Antecedent;
  Msvm_VirtualSystemReferencePoint REF Dependent;
};
```

## <a name="members"></a><span data-ttu-id="6524b-107">成員</span><span class="sxs-lookup"><span data-stu-id="6524b-107">Members</span></span>

<span data-ttu-id="6524b-108">**Msvm \_ ReferencePointOfVirtualSystem** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="6524b-108">The **Msvm\_ReferencePointOfVirtualSystem** class has these types of members:</span></span>

-   [<span data-ttu-id="6524b-109">屬性</span><span class="sxs-lookup"><span data-stu-id="6524b-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="6524b-110">屬性</span><span class="sxs-lookup"><span data-stu-id="6524b-110">Properties</span></span>

<span data-ttu-id="6524b-111">**Msvm \_ ReferencePointOfVirtualSystem** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="6524b-111">The **Msvm\_ReferencePointOfVirtualSystem** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="6524b-112">**先行**</span><span class="sxs-lookup"><span data-stu-id="6524b-112">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6524b-113">資料類型： **Msvm \_**</span><span class="sxs-lookup"><span data-stu-id="6524b-113">Data type: **Msvm\_ComputerSystem**</span></span>
</dt> <dt>

<span data-ttu-id="6524b-114">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="6524b-114">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6524b-115">限定詞： [**Key**](/windows/desktop/WmiSdk/key-qualifier)、 [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Antecedent" ) </span><span class="sxs-lookup"><span data-stu-id="6524b-115">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent")</span></span>
</dt> </dl>

<span data-ttu-id="6524b-116">Msvm，表示此關聯中的獨立物件。 [**\_**](msvm-computersystem.md)</span><span class="sxs-lookup"><span data-stu-id="6524b-116">An [**Msvm\_ComputerSystem**](msvm-computersystem.md) that represents the independent object in this association.</span></span>

</dd> <dt>

<span data-ttu-id="6524b-117">**依賴**</span><span class="sxs-lookup"><span data-stu-id="6524b-117">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6524b-118">資料類型： **Msvm \_ VirtualSystemReferencePoint**</span><span class="sxs-lookup"><span data-stu-id="6524b-118">Data type: **Msvm\_VirtualSystemReferencePoint**</span></span>
</dt> <dt>

<span data-ttu-id="6524b-119">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="6524b-119">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6524b-120">限定詞： [**Key**](/windows/desktop/WmiSdk/key-qualifier)、 [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ( 「相依」 ) </span><span class="sxs-lookup"><span data-stu-id="6524b-120">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependent")</span></span>
</dt> </dl>

<span data-ttu-id="6524b-121">代表 **相依于前** 一個物件之物件的 [**Msvm \_ VirtualSystemReferencePoint**](msvm-virtualsystemreferencepoint.md) 。</span><span class="sxs-lookup"><span data-stu-id="6524b-121">An [**Msvm\_VirtualSystemReferencePoint**](msvm-virtualsystemreferencepoint.md) that represents the object that is dependent on the **Antecedent**.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="6524b-122">規格需求</span><span class="sxs-lookup"><span data-stu-id="6524b-122">Requirements</span></span>



| <span data-ttu-id="6524b-123">需求</span><span class="sxs-lookup"><span data-stu-id="6524b-123">Requirement</span></span> | <span data-ttu-id="6524b-124">值</span><span class="sxs-lookup"><span data-stu-id="6524b-124">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6524b-125">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="6524b-125">Minimum supported client</span></span><br/> | <span data-ttu-id="6524b-126">\[僅 Windows 10 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="6524b-126">Windows 10 \[desktop apps only\]</span></span><br/>                                                             |
| <span data-ttu-id="6524b-127">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="6524b-127">Minimum supported server</span></span><br/> | <span data-ttu-id="6524b-128">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="6524b-128">Windows Server 2016</span></span><br/>                                                                          |
| <span data-ttu-id="6524b-129">命名空間</span><span class="sxs-lookup"><span data-stu-id="6524b-129">Namespace</span></span><br/>                | <span data-ttu-id="6524b-130">根 \\ 虛擬化 \\ v2</span><span class="sxs-lookup"><span data-stu-id="6524b-130">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="6524b-131">MOF</span><span class="sxs-lookup"><span data-stu-id="6524b-131">MOF</span></span><br/>                      | <dl> <span data-ttu-id="6524b-132"><dt>WindowsVirtualization。</dt></span><span class="sxs-lookup"><span data-stu-id="6524b-132"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="6524b-133">DLL</span><span class="sxs-lookup"><span data-stu-id="6524b-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6524b-134"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="6524b-134"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="6524b-135">另請參閱</span><span class="sxs-lookup"><span data-stu-id="6524b-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6524b-136">**CIM \_ 相依性**</span><span class="sxs-lookup"><span data-stu-id="6524b-136">**CIM\_Dependency**</span></span>](cim-dependency.md)
</dt> </dl>

 

