---
description: 將 Msvm \_ VirtualSystemCollection 與包含的 Msvm 不會產生的物件產生關聯 \_ 。
ms.assetid: ad783188-b60a-4271-aa2d-8050c36e70eb
title: Msvm_CollectedVirtualSystems 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_CollectedVirtualSystems
- Msvm_CollectedVirtualSystems.Collection
- Msvm_CollectedVirtualSystems.Member
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 0803eda14ffbaf21ee2bf4491bd835123b7191e1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "107001426"
---
# <a name="msvm_collectedvirtualsystems-class"></a><span data-ttu-id="998b4-103">Msvm \_ CollectedVirtualSystems 類別</span><span class="sxs-lookup"><span data-stu-id="998b4-103">Msvm\_CollectedVirtualSystems class</span></span>

<span data-ttu-id="998b4-104">將 [**Msvm \_ VirtualSystemCollection**](msvm-virtualsystemcollection.md)與包含的 Msvm 不會產生的物件產生關聯。 [**\_**](msvm-computersystem.md)</span><span class="sxs-lookup"><span data-stu-id="998b4-104">Associates the [**Msvm\_VirtualSystemCollection**](msvm-virtualsystemcollection.md) to the contained [**Msvm\_ComputerSystem**](msvm-computersystem.md) objects.</span></span>

<span data-ttu-id="998b4-105">下列語法已經過受管理物件格式 (MOF) 程式碼簡化，並包含所有已繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="998b4-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="998b4-106">語法</span><span class="sxs-lookup"><span data-stu-id="998b4-106">Syntax</span></span>

``` syntax
[Association, Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_CollectedVirtualSystems : CIM_CollectedMSEs
{
  Msvm_VirtualSystemCollection REF Collection;
  Msvm_ComputerSystem          REF Member;
};
```

## <a name="members"></a><span data-ttu-id="998b4-107">成員</span><span class="sxs-lookup"><span data-stu-id="998b4-107">Members</span></span>

<span data-ttu-id="998b4-108">**Msvm \_ CollectedVirtualSystems** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="998b4-108">The **Msvm\_CollectedVirtualSystems** class has these types of members:</span></span>

-   [<span data-ttu-id="998b4-109">屬性</span><span class="sxs-lookup"><span data-stu-id="998b4-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="998b4-110">屬性</span><span class="sxs-lookup"><span data-stu-id="998b4-110">Properties</span></span>

<span data-ttu-id="998b4-111">**Msvm \_ CollectedVirtualSystems** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="998b4-111">The **Msvm\_CollectedVirtualSystems** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="998b4-112">**集合**</span><span class="sxs-lookup"><span data-stu-id="998b4-112">**Collection**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="998b4-113">資料類型： **Msvm \_ VirtualSystemCollection**</span><span class="sxs-lookup"><span data-stu-id="998b4-113">Data type: **Msvm\_VirtualSystemCollection**</span></span>
</dt> <dt>

<span data-ttu-id="998b4-114">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="998b4-114">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="998b4-115">限定詞： [**Aggregate**](/windows/desktop/WmiSdk/standard-qualifiers)、 [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Collection" ) </span><span class="sxs-lookup"><span data-stu-id="998b4-115">Qualifiers: [**Aggregate**](/windows/desktop/WmiSdk/standard-qualifiers), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Collection")</span></span>
</dt> </dl>

<span data-ttu-id="998b4-116">代表集合的 [**Msvm \_ VirtualSystemCollection**](msvm-virtualsystemcollection.md) 群組或 ' 包 ' 物件。</span><span class="sxs-lookup"><span data-stu-id="998b4-116">An [**Msvm\_VirtualSystemCollection**](msvm-virtualsystemcollection.md) grouping or 'bag' object that represents the collection.</span></span>

</dd> <dt>

<span data-ttu-id="998b4-117">**成員**</span><span class="sxs-lookup"><span data-stu-id="998b4-117">**Member**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="998b4-118">資料類型： **Msvm \_**</span><span class="sxs-lookup"><span data-stu-id="998b4-118">Data type: **Msvm\_ComputerSystem**</span></span>
</dt> <dt>

<span data-ttu-id="998b4-119">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="998b4-119">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="998b4-120">限定詞：覆 [**寫**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Member" ) </span><span class="sxs-lookup"><span data-stu-id="998b4-120">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Member")</span></span>
</dt> </dl>

<span data-ttu-id="998b4-121">包含集合成員的 Msvm 同系統物件。 [**\_**](msvm-computersystem.md)</span><span class="sxs-lookup"><span data-stu-id="998b4-121">An [**Msvm\_ComputerSystem**](msvm-computersystem.md) object containing the members of the collection.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="998b4-122">規格需求</span><span class="sxs-lookup"><span data-stu-id="998b4-122">Requirements</span></span>



| <span data-ttu-id="998b4-123">需求</span><span class="sxs-lookup"><span data-stu-id="998b4-123">Requirement</span></span> | <span data-ttu-id="998b4-124">值</span><span class="sxs-lookup"><span data-stu-id="998b4-124">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="998b4-125">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="998b4-125">Minimum supported client</span></span><br/> | <span data-ttu-id="998b4-126">\[僅 Windows 10 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="998b4-126">Windows 10 \[desktop apps only\]</span></span><br/>                                                             |
| <span data-ttu-id="998b4-127">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="998b4-127">Minimum supported server</span></span><br/> | <span data-ttu-id="998b4-128">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="998b4-128">Windows Server 2016</span></span><br/>                                                                          |
| <span data-ttu-id="998b4-129">命名空間</span><span class="sxs-lookup"><span data-stu-id="998b4-129">Namespace</span></span><br/>                | <span data-ttu-id="998b4-130">根 \\ 虛擬化 \\ v2</span><span class="sxs-lookup"><span data-stu-id="998b4-130">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="998b4-131">MOF</span><span class="sxs-lookup"><span data-stu-id="998b4-131">MOF</span></span><br/>                      | <dl> <span data-ttu-id="998b4-132"><dt>WindowsVirtualization。</dt></span><span class="sxs-lookup"><span data-stu-id="998b4-132"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="998b4-133">DLL</span><span class="sxs-lookup"><span data-stu-id="998b4-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="998b4-134"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="998b4-134"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="998b4-135">另請參閱</span><span class="sxs-lookup"><span data-stu-id="998b4-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="998b4-136">**CIM \_ CollectedMSEs**</span><span class="sxs-lookup"><span data-stu-id="998b4-136">**CIM\_CollectedMSEs**</span></span>](cim-collectedmses.md)
</dt> </dl>

 

