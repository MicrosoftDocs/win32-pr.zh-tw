---
description: 將 Msvm \_ SnapshotCollection 與對應的 Msvm \_ VirtualSystemCollection 物件產生關聯。
ms.assetid: 4dbfe21f-e700-4266-aedb-236c57c424f6
title: Msvm_SnapshotOfVirtualSystemCollection 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_SnapshotOfVirtualSystemCollection
- Msvm_SnapshotOfVirtualSystemCollection.Antecedent
- Msvm_SnapshotOfVirtualSystemCollection.Dependent
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: ae3c9c146cea8a8af98f4d3071ee7339d53eb6b1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103848512"
---
# <a name="msvm_snapshotofvirtualsystemcollection-class"></a><span data-ttu-id="e575e-103">Msvm \_ SnapshotOfVirtualSystemCollection 類別</span><span class="sxs-lookup"><span data-stu-id="e575e-103">Msvm\_SnapshotOfVirtualSystemCollection class</span></span>

<span data-ttu-id="e575e-104">將 [**Msvm \_ SnapshotCollection**](msvm-snapshotcollection.md) 與對應的 [**Msvm \_ VirtualSystemCollection**](msvm-virtualsystemcollection.md) 物件產生關聯。</span><span class="sxs-lookup"><span data-stu-id="e575e-104">Associates the [**Msvm\_SnapshotCollection**](msvm-snapshotcollection.md) to the corresponding [**Msvm\_VirtualSystemCollection**](msvm-virtualsystemcollection.md) objects.</span></span>

<span data-ttu-id="e575e-105">下列語法已經過受管理物件格式 (MOF) 程式碼簡化，並包含所有已繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="e575e-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="e575e-106">語法</span><span class="sxs-lookup"><span data-stu-id="e575e-106">Syntax</span></span>

``` syntax
[Association, Aggregation, Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_SnapshotOfVirtualSystemCollection : CIM_Dependency
{
  CIM_CollectionOfMSEs REF Antecedent;
  CIM_Collection       REF Dependent;
};
```

## <a name="members"></a><span data-ttu-id="e575e-107">成員</span><span class="sxs-lookup"><span data-stu-id="e575e-107">Members</span></span>

<span data-ttu-id="e575e-108">**Msvm \_ SnapshotOfVirtualSystemCollection** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="e575e-108">The **Msvm\_SnapshotOfVirtualSystemCollection** class has these types of members:</span></span>

-   [<span data-ttu-id="e575e-109">屬性</span><span class="sxs-lookup"><span data-stu-id="e575e-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="e575e-110">屬性</span><span class="sxs-lookup"><span data-stu-id="e575e-110">Properties</span></span>

<span data-ttu-id="e575e-111">**Msvm \_ SnapshotOfVirtualSystemCollection** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="e575e-111">The **Msvm\_SnapshotOfVirtualSystemCollection** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="e575e-112">**先行**</span><span class="sxs-lookup"><span data-stu-id="e575e-112">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e575e-113">資料類型： **CIM \_ CollectionOfMSEs**</span><span class="sxs-lookup"><span data-stu-id="e575e-113">Data type: **CIM\_CollectionOfMSEs**</span></span>
</dt> <dt>

<span data-ttu-id="e575e-114">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="e575e-114">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e575e-115">限定詞： [**Key**](/windows/desktop/WmiSdk/key-qualifier)、 [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Antecedent" ) </span><span class="sxs-lookup"><span data-stu-id="e575e-115">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent")</span></span>
</dt> </dl>

<span data-ttu-id="e575e-116">[**CIM \_ CollectionOfMSEs**](cim-collectionofmses.md) ，表示此關聯中的獨立物件。</span><span class="sxs-lookup"><span data-stu-id="e575e-116">A [**CIM\_CollectionOfMSEs**](cim-collectionofmses.md) that represents the independent object in this association.</span></span>

</dd> <dt>

<span data-ttu-id="e575e-117">**依賴**</span><span class="sxs-lookup"><span data-stu-id="e575e-117">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e575e-118">資料類型： **CIM \_ 集合**</span><span class="sxs-lookup"><span data-stu-id="e575e-118">Data type: **CIM\_Collection**</span></span>
</dt> <dt>

<span data-ttu-id="e575e-119">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="e575e-119">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e575e-120">限定詞： [**Key**](/windows/desktop/WmiSdk/key-qualifier)、 [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ( 「相依」 ) </span><span class="sxs-lookup"><span data-stu-id="e575e-120">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependent")</span></span>
</dt> </dl>

<span data-ttu-id="e575e-121">[**CIM \_ 集合**](cim-collection.md)，表示相依于前面的物件 **。**</span><span class="sxs-lookup"><span data-stu-id="e575e-121">A [**CIM\_Collection**](cim-collection.md) that represents the object that is dependent on the **Antecedent.**</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="e575e-122">規格需求</span><span class="sxs-lookup"><span data-stu-id="e575e-122">Requirements</span></span>



| <span data-ttu-id="e575e-123">需求</span><span class="sxs-lookup"><span data-stu-id="e575e-123">Requirement</span></span> | <span data-ttu-id="e575e-124">值</span><span class="sxs-lookup"><span data-stu-id="e575e-124">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e575e-125">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="e575e-125">Minimum supported client</span></span><br/> | <span data-ttu-id="e575e-126">\[僅 Windows 10 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="e575e-126">Windows 10 \[desktop apps only\]</span></span><br/>                                                             |
| <span data-ttu-id="e575e-127">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="e575e-127">Minimum supported server</span></span><br/> | <span data-ttu-id="e575e-128">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="e575e-128">Windows Server 2016</span></span><br/>                                                                          |
| <span data-ttu-id="e575e-129">命名空間</span><span class="sxs-lookup"><span data-stu-id="e575e-129">Namespace</span></span><br/>                | <span data-ttu-id="e575e-130">根 \\ 虛擬化 \\ v2</span><span class="sxs-lookup"><span data-stu-id="e575e-130">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="e575e-131">MOF</span><span class="sxs-lookup"><span data-stu-id="e575e-131">MOF</span></span><br/>                      | <dl> <span data-ttu-id="e575e-132"><dt>WindowsVirtualization。</dt></span><span class="sxs-lookup"><span data-stu-id="e575e-132"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="e575e-133">DLL</span><span class="sxs-lookup"><span data-stu-id="e575e-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e575e-134"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="e575e-134"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="e575e-135">另請參閱</span><span class="sxs-lookup"><span data-stu-id="e575e-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e575e-136">**CIM \_ 相依性**</span><span class="sxs-lookup"><span data-stu-id="e575e-136">**CIM\_Dependency**</span></span>](cim-dependency.md)
</dt> </dl>

 

