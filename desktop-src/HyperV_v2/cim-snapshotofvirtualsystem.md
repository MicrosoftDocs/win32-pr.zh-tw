---
description: 讓虛擬系統與虛擬系統的快照集產生關聯。
ms.assetid: f85f6914-dbb8-42c9-a732-11d48613c15c
title: CIM_SnapshotOfVirtualSystem 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_SnapshotOfVirtualSystem
- CIM_SnapshotOfVirtualSystem.Antecedent
- CIM_SnapshotOfVirtualSystem.Dependent
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 6e8e0929f1198ececea5ea5ec144e2f7313ec35c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103944663"
---
# <a name="cim_snapshotofvirtualsystem-class"></a><span data-ttu-id="0e16a-103">CIM \_ SnapshotOfVirtualSystem 類別</span><span class="sxs-lookup"><span data-stu-id="0e16a-103">CIM\_SnapshotOfVirtualSystem class</span></span>

<span data-ttu-id="0e16a-104">讓虛擬系統與虛擬系統的快照集產生關聯。</span><span class="sxs-lookup"><span data-stu-id="0e16a-104">Associates a virtual system a snapshot of the virtual system.</span></span>

## <a name="syntax"></a><span data-ttu-id="0e16a-105">語法</span><span class="sxs-lookup"><span data-stu-id="0e16a-105">Syntax</span></span>

``` syntax
[Association, Abstract, Version("2.22.0"), AMENDMENT]
class CIM_SnapshotOfVirtualSystem : CIM_Dependency
{
  CIM_ComputerSystem           REF Antecedent;
  CIM_VirtualSystemSettingData REF Dependent;
};
```

## <a name="members"></a><span data-ttu-id="0e16a-106">成員</span><span class="sxs-lookup"><span data-stu-id="0e16a-106">Members</span></span>

<span data-ttu-id="0e16a-107">**CIM \_ SnapshotOfVirtualSystem** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="0e16a-107">The **CIM\_SnapshotOfVirtualSystem** class has these types of members:</span></span>

-   [<span data-ttu-id="0e16a-108">屬性</span><span class="sxs-lookup"><span data-stu-id="0e16a-108">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="0e16a-109">屬性</span><span class="sxs-lookup"><span data-stu-id="0e16a-109">Properties</span></span>

<span data-ttu-id="0e16a-110">**CIM \_ SnapshotOfVirtualSystem** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="0e16a-110">The **CIM\_SnapshotOfVirtualSystem** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="0e16a-111">**先行**</span><span class="sxs-lookup"><span data-stu-id="0e16a-111">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0e16a-112">資料類型： **CIM \_** 未執行</span><span class="sxs-lookup"><span data-stu-id="0e16a-112">Data type: **CIM\_ComputerSystem**</span></span>
</dt> <dt>

<span data-ttu-id="0e16a-113">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="0e16a-113">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0e16a-114">限定詞：覆 [**寫**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Antecedent" ) 、 [**Min**](/windows/desktop/WmiSdk/standard-qualifiers) (0) 、 [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1) </span><span class="sxs-lookup"><span data-stu-id="0e16a-114">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent"), [**Min**](/windows/desktop/WmiSdk/standard-qualifiers) (0), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1)</span></span>
</dt> </dl>

<span data-ttu-id="0e16a-115">代表虛擬系統的電腦系統參考。</span><span class="sxs-lookup"><span data-stu-id="0e16a-115">A reference to the computer system that represents the virtual system.</span></span>

</dd> <dt>

<span data-ttu-id="0e16a-116">**依賴**</span><span class="sxs-lookup"><span data-stu-id="0e16a-116">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0e16a-117">資料類型： **CIM \_ VirtualSystemSettingData**</span><span class="sxs-lookup"><span data-stu-id="0e16a-117">Data type: **CIM\_VirtualSystemSettingData**</span></span>
</dt> <dt>

<span data-ttu-id="0e16a-118">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="0e16a-118">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0e16a-119">限定詞：覆 [**寫**](/windows/desktop/WmiSdk/standard-qualifiers) ( 「相依」 ) </span><span class="sxs-lookup"><span data-stu-id="0e16a-119">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependent")</span></span>
</dt> </dl>

<span data-ttu-id="0e16a-120">設定資料物件的參考，該物件表示虛擬系統的快照集。</span><span class="sxs-lookup"><span data-stu-id="0e16a-120">A reference to the settings data object that represents the snapshot of the virtual system.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="0e16a-121">規格需求</span><span class="sxs-lookup"><span data-stu-id="0e16a-121">Requirements</span></span>



| <span data-ttu-id="0e16a-122">需求</span><span class="sxs-lookup"><span data-stu-id="0e16a-122">Requirement</span></span> | <span data-ttu-id="0e16a-123">值</span><span class="sxs-lookup"><span data-stu-id="0e16a-123">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0e16a-124">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="0e16a-124">Minimum supported client</span></span><br/> | <span data-ttu-id="0e16a-125">Windows 8</span><span class="sxs-lookup"><span data-stu-id="0e16a-125">Windows 8</span></span><br/>                                                                                    |
| <span data-ttu-id="0e16a-126">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="0e16a-126">Minimum supported server</span></span><br/> | <span data-ttu-id="0e16a-127">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="0e16a-127">Windows Server 2012</span></span><br/>                                                                          |
| <span data-ttu-id="0e16a-128">命名空間</span><span class="sxs-lookup"><span data-stu-id="0e16a-128">Namespace</span></span><br/>                | <span data-ttu-id="0e16a-129">根 \\ 虛擬化 \\ v2</span><span class="sxs-lookup"><span data-stu-id="0e16a-129">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="0e16a-130">MOF</span><span class="sxs-lookup"><span data-stu-id="0e16a-130">MOF</span></span><br/>                      | <dl> <span data-ttu-id="0e16a-131"><dt>WindowsVirtualization。</dt></span><span class="sxs-lookup"><span data-stu-id="0e16a-131"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="0e16a-132">DLL</span><span class="sxs-lookup"><span data-stu-id="0e16a-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="0e16a-133"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="0e16a-133"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="0e16a-134">另請參閱</span><span class="sxs-lookup"><span data-stu-id="0e16a-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0e16a-135">**CIM \_ 相依性**</span><span class="sxs-lookup"><span data-stu-id="0e16a-135">**CIM\_Dependency**</span></span>](cim-dependency.md)
</dt> </dl>

 

