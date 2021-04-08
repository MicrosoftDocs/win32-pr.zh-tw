---
description: 將 Msvm \_ ReferencePointCollection 與包含的 Msvm \_ VirtualSystemReferencePoint 物件產生關聯。
ms.assetid: 826125c3-0a89-4573-ac28-88588eac248d
title: Msvm_CollectedReferencePoints 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_CollectedReferencePoints
- Msvm_CollectedReferencePoints.Collection
- Msvm_CollectedReferencePoints.Member
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 4891d4ec4c613c92c3b5d5a090f2683bfc77dc5e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103691188"
---
# <a name="msvm_collectedreferencepoints-class"></a><span data-ttu-id="b8652-103">Msvm \_ CollectedReferencePoints 類別</span><span class="sxs-lookup"><span data-stu-id="b8652-103">Msvm\_CollectedReferencePoints class</span></span>

<span data-ttu-id="b8652-104">將 [**Msvm \_ ReferencePointCollection**](msvm-referencepointcollection.md) 與包含的 [**Msvm \_ VirtualSystemReferencePoint**](msvm-virtualsystemreferencepoint.md) 物件產生關聯。</span><span class="sxs-lookup"><span data-stu-id="b8652-104">Associates the [**Msvm\_ReferencePointCollection**](msvm-referencepointcollection.md) to the contained [**Msvm\_VirtualSystemReferencePoint**](msvm-virtualsystemreferencepoint.md) objects.</span></span>

<span data-ttu-id="b8652-105">下列語法已經過受管理物件格式 (MOF) 程式碼簡化，並包含所有已繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="b8652-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="b8652-106">語法</span><span class="sxs-lookup"><span data-stu-id="b8652-106">Syntax</span></span>

``` syntax
[Association, Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_CollectedReferencePoints : CIM_CollectedMSEs
{
  Msvm_ReferencePointCollection    REF Collection;
  Msvm_VirtualSystemReferencePoint REF Member;
};
```

## <a name="members"></a><span data-ttu-id="b8652-107">成員</span><span class="sxs-lookup"><span data-stu-id="b8652-107">Members</span></span>

<span data-ttu-id="b8652-108">**Msvm \_ CollectedReferencePoints** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="b8652-108">The **Msvm\_CollectedReferencePoints** class has these types of members:</span></span>

-   [<span data-ttu-id="b8652-109">屬性</span><span class="sxs-lookup"><span data-stu-id="b8652-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="b8652-110">屬性</span><span class="sxs-lookup"><span data-stu-id="b8652-110">Properties</span></span>

<span data-ttu-id="b8652-111">**Msvm \_ CollectedReferencePoints** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="b8652-111">The **Msvm\_CollectedReferencePoints** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="b8652-112">**集合**</span><span class="sxs-lookup"><span data-stu-id="b8652-112">**Collection**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b8652-113">資料類型： **Msvm \_ ReferencePointCollection**</span><span class="sxs-lookup"><span data-stu-id="b8652-113">Data type: **Msvm\_ReferencePointCollection**</span></span>
</dt> <dt>

<span data-ttu-id="b8652-114">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="b8652-114">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b8652-115">限定詞： [**Aggregate**](/windows/desktop/WmiSdk/standard-qualifiers)、 [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Collection" ) </span><span class="sxs-lookup"><span data-stu-id="b8652-115">Qualifiers: [**Aggregate**](/windows/desktop/WmiSdk/standard-qualifiers), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Collection")</span></span>
</dt> </dl>

<span data-ttu-id="b8652-116">代表集合的 [**Msvm \_ ReferencePointCollection**](msvm-referencepointcollection.md) 群組或 ' 包 ' 物件。</span><span class="sxs-lookup"><span data-stu-id="b8652-116">An [**Msvm\_ReferencePointCollection**](msvm-referencepointcollection.md) grouping or 'bag' object that represents the collection.</span></span>

</dd> <dt>

<span data-ttu-id="b8652-117">**成員**</span><span class="sxs-lookup"><span data-stu-id="b8652-117">**Member**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b8652-118">資料類型： **Msvm \_ VirtualSystemReferencePoint**</span><span class="sxs-lookup"><span data-stu-id="b8652-118">Data type: **Msvm\_VirtualSystemReferencePoint**</span></span>
</dt> <dt>

<span data-ttu-id="b8652-119">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="b8652-119">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b8652-120">限定詞：覆 [**寫**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Member" ) </span><span class="sxs-lookup"><span data-stu-id="b8652-120">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Member")</span></span>
</dt> </dl>

<span data-ttu-id="b8652-121">包含集合成員的 [**Msvm \_ VirtualSystemReferencePoint**](msvm-virtualsystemreferencepoint.md) 。</span><span class="sxs-lookup"><span data-stu-id="b8652-121">An [**Msvm\_VirtualSystemReferencePoint**](msvm-virtualsystemreferencepoint.md) containing the members of the collection.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="b8652-122">規格需求</span><span class="sxs-lookup"><span data-stu-id="b8652-122">Requirements</span></span>



| <span data-ttu-id="b8652-123">需求</span><span class="sxs-lookup"><span data-stu-id="b8652-123">Requirement</span></span> | <span data-ttu-id="b8652-124">值</span><span class="sxs-lookup"><span data-stu-id="b8652-124">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b8652-125">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="b8652-125">Minimum supported client</span></span><br/> | <span data-ttu-id="b8652-126">\[僅 Windows 10 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="b8652-126">Windows 10 \[desktop apps only\]</span></span><br/>                                                             |
| <span data-ttu-id="b8652-127">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="b8652-127">Minimum supported server</span></span><br/> | <span data-ttu-id="b8652-128">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="b8652-128">Windows Server 2016</span></span><br/>                                                                          |
| <span data-ttu-id="b8652-129">命名空間</span><span class="sxs-lookup"><span data-stu-id="b8652-129">Namespace</span></span><br/>                | <span data-ttu-id="b8652-130">根 \\ 虛擬化 \\ v2</span><span class="sxs-lookup"><span data-stu-id="b8652-130">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="b8652-131">MOF</span><span class="sxs-lookup"><span data-stu-id="b8652-131">MOF</span></span><br/>                      | <dl> <span data-ttu-id="b8652-132"><dt>WindowsVirtualization。</dt></span><span class="sxs-lookup"><span data-stu-id="b8652-132"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="b8652-133">DLL</span><span class="sxs-lookup"><span data-stu-id="b8652-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b8652-134"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="b8652-134"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="b8652-135">另請參閱</span><span class="sxs-lookup"><span data-stu-id="b8652-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b8652-136">**CIM \_ CollectedMSEs**</span><span class="sxs-lookup"><span data-stu-id="b8652-136">**CIM\_CollectedMSEs**</span></span>](cim-collectedmses.md)
</dt> </dl>

 

