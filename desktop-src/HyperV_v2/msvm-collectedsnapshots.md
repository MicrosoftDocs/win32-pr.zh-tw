---
description: 將 Msvm \_ SnapshotCollection 與包含的 Msvm \_ VirtualSystemSettingData 物件產生關聯。
ms.assetid: 21005e8a-0bc6-4ea7-8f6f-d79803b43bc0
title: Msvm_CollectedSnapshots 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_CollectedSnapshots
- Msvm_CollectedSnapshots.Collection
- Msvm_CollectedSnapshots.Member
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 9c89e7c7390cc1f2cc0c3217fca93e3f2d2d01ec
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106979033"
---
# <a name="msvm_collectedsnapshots-class"></a><span data-ttu-id="c1879-103">Msvm \_ CollectedSnapshots 類別</span><span class="sxs-lookup"><span data-stu-id="c1879-103">Msvm\_CollectedSnapshots class</span></span>

<span data-ttu-id="c1879-104">將 [**Msvm \_ SnapshotCollection**](msvm-snapshotcollection.md) 與包含的 [**Msvm \_ VirtualSystemSettingData**](msvm-virtualsystemsettingdata.md) 物件產生關聯。</span><span class="sxs-lookup"><span data-stu-id="c1879-104">Associates the [**Msvm\_SnapshotCollection**](msvm-snapshotcollection.md) to the contained [**Msvm\_VirtualSystemSettingData**](msvm-virtualsystemsettingdata.md) objects.</span></span>

<span data-ttu-id="c1879-105">下列語法已經過受管理物件格式 (MOF) 程式碼簡化，並包含所有已繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="c1879-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="c1879-106">語法</span><span class="sxs-lookup"><span data-stu-id="c1879-106">Syntax</span></span>

``` syntax
[Association, Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_CollectedSnapshots : CIM_CollectedMSEs
{
  Msvm_SnapshotCollection       REF Collection;
  Msvm_VirtualSystemSettingData REF Member;
};
```

## <a name="members"></a><span data-ttu-id="c1879-107">成員</span><span class="sxs-lookup"><span data-stu-id="c1879-107">Members</span></span>

<span data-ttu-id="c1879-108">**Msvm \_ CollectedSnapshots** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="c1879-108">The **Msvm\_CollectedSnapshots** class has these types of members:</span></span>

-   [<span data-ttu-id="c1879-109">屬性</span><span class="sxs-lookup"><span data-stu-id="c1879-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="c1879-110">屬性</span><span class="sxs-lookup"><span data-stu-id="c1879-110">Properties</span></span>

<span data-ttu-id="c1879-111">**Msvm \_ CollectedSnapshots** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="c1879-111">The **Msvm\_CollectedSnapshots** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="c1879-112">**集合**</span><span class="sxs-lookup"><span data-stu-id="c1879-112">**Collection**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c1879-113">資料類型： **Msvm \_ SnapshotCollection**</span><span class="sxs-lookup"><span data-stu-id="c1879-113">Data type: **Msvm\_SnapshotCollection**</span></span>
</dt> <dt>

<span data-ttu-id="c1879-114">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="c1879-114">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c1879-115">限定詞： [**Aggregate**](/windows/desktop/WmiSdk/standard-qualifiers)、 [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Collection" ) </span><span class="sxs-lookup"><span data-stu-id="c1879-115">Qualifiers: [**Aggregate**](/windows/desktop/WmiSdk/standard-qualifiers), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Collection")</span></span>
</dt> </dl>

<span data-ttu-id="c1879-116">代表集合的 [**Msvm \_ SnapshotCollection**](msvm-snapshotcollection.md) 群組或 ' 包 ' 物件。</span><span class="sxs-lookup"><span data-stu-id="c1879-116">An [**Msvm\_SnapshotCollection**](msvm-snapshotcollection.md) grouping or 'bag' object that represents the collection.</span></span>

</dd> <dt>

<span data-ttu-id="c1879-117">**成員**</span><span class="sxs-lookup"><span data-stu-id="c1879-117">**Member**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c1879-118">資料類型： **Msvm \_ VirtualSystemSettingData**</span><span class="sxs-lookup"><span data-stu-id="c1879-118">Data type: **Msvm\_VirtualSystemSettingData**</span></span>
</dt> <dt>

<span data-ttu-id="c1879-119">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="c1879-119">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c1879-120">限定詞：覆 [**寫**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Member" ) </span><span class="sxs-lookup"><span data-stu-id="c1879-120">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Member")</span></span>
</dt> </dl>

<span data-ttu-id="c1879-121">包含集合成員的 [**Msvm \_ VirtualSystemSettingData**](msvm-virtualsystemsettingdata.md) 。</span><span class="sxs-lookup"><span data-stu-id="c1879-121">An [**Msvm\_VirtualSystemSettingData**](msvm-virtualsystemsettingdata.md) containing the members of the collection.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="c1879-122">規格需求</span><span class="sxs-lookup"><span data-stu-id="c1879-122">Requirements</span></span>



| <span data-ttu-id="c1879-123">需求</span><span class="sxs-lookup"><span data-stu-id="c1879-123">Requirement</span></span> | <span data-ttu-id="c1879-124">值</span><span class="sxs-lookup"><span data-stu-id="c1879-124">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c1879-125">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="c1879-125">Minimum supported client</span></span><br/> | <span data-ttu-id="c1879-126">\[僅 Windows 10 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="c1879-126">Windows 10 \[desktop apps only\]</span></span><br/>                                                             |
| <span data-ttu-id="c1879-127">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="c1879-127">Minimum supported server</span></span><br/> | <span data-ttu-id="c1879-128">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="c1879-128">Windows Server 2016</span></span><br/>                                                                          |
| <span data-ttu-id="c1879-129">命名空間</span><span class="sxs-lookup"><span data-stu-id="c1879-129">Namespace</span></span><br/>                | <span data-ttu-id="c1879-130">根 \\ 虛擬化 \\ v2</span><span class="sxs-lookup"><span data-stu-id="c1879-130">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="c1879-131">MOF</span><span class="sxs-lookup"><span data-stu-id="c1879-131">MOF</span></span><br/>                      | <dl> <span data-ttu-id="c1879-132"><dt>WindowsVirtualization。</dt></span><span class="sxs-lookup"><span data-stu-id="c1879-132"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="c1879-133">DLL</span><span class="sxs-lookup"><span data-stu-id="c1879-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c1879-134"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="c1879-134"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="c1879-135">另請參閱</span><span class="sxs-lookup"><span data-stu-id="c1879-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c1879-136">**CIM \_ CollectedMSEs**</span><span class="sxs-lookup"><span data-stu-id="c1879-136">**CIM\_CollectedMSEs**</span></span>](cim-collectedmses.md)
</dt> </dl>

 

