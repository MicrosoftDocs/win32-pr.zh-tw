---
description: 表示虛擬系統與系統最新快照之間的關聯。 只有在使用快照集建立虛擬系統，或是從虛擬系統建立快照集時，此關聯才會存在。
ms.assetid: e6040818-84cf-4cec-ab7b-a733fe5d01d2
title: CIM_MostCurrentSnapshotInBranch 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_MostCurrentSnapshotInBranch
- CIM_MostCurrentSnapshotInBranch.Antecedent
- CIM_MostCurrentSnapshotInBranch.Dependent
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 078a7c9f1669a2aa0449dce01022eba0eadcb2c3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106983443"
---
# <a name="cim_mostcurrentsnapshotinbranch-class"></a><span data-ttu-id="d0c63-104">CIM \_ MostCurrentSnapshotInBranch 類別</span><span class="sxs-lookup"><span data-stu-id="d0c63-104">CIM\_MostCurrentSnapshotInBranch class</span></span>

<span data-ttu-id="d0c63-105">表示虛擬系統與系統最新快照之間的關聯。</span><span class="sxs-lookup"><span data-stu-id="d0c63-105">Represents an association between a virtual system and the most current snapshot of the system.</span></span> <span data-ttu-id="d0c63-106">只有在使用快照集建立虛擬系統，或是從虛擬系統建立快照集時，此關聯才會存在。</span><span class="sxs-lookup"><span data-stu-id="d0c63-106">This association can only exist if the virtual system was create using a snapshot or if a snapshot was created from the virtual system.</span></span>

## <a name="syntax"></a><span data-ttu-id="d0c63-107">語法</span><span class="sxs-lookup"><span data-stu-id="d0c63-107">Syntax</span></span>

``` syntax
[Association, Experimental, Version("2.16.0"), AMENDMENT]
class CIM_MostCurrentSnapshotInBranch : CIM_Dependency
{
  CIM_ComputerSystem           REF Antecedent;
  CIM_VirtualSystemSettingData REF Dependent;
};
```

## <a name="members"></a><span data-ttu-id="d0c63-108">成員</span><span class="sxs-lookup"><span data-stu-id="d0c63-108">Members</span></span>

<span data-ttu-id="d0c63-109">**CIM \_ MostCurrentSnapshotInBranch** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="d0c63-109">The **CIM\_MostCurrentSnapshotInBranch** class has these types of members:</span></span>

-   [<span data-ttu-id="d0c63-110">屬性</span><span class="sxs-lookup"><span data-stu-id="d0c63-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="d0c63-111">屬性</span><span class="sxs-lookup"><span data-stu-id="d0c63-111">Properties</span></span>

<span data-ttu-id="d0c63-112">**CIM \_ MostCurrentSnapshotInBranch** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="d0c63-112">The **CIM\_MostCurrentSnapshotInBranch** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="d0c63-113">**先行**</span><span class="sxs-lookup"><span data-stu-id="d0c63-113">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d0c63-114">資料類型： **CIM \_** 未執行</span><span class="sxs-lookup"><span data-stu-id="d0c63-114">Data type: **CIM\_ComputerSystem**</span></span>
</dt> <dt>

<span data-ttu-id="d0c63-115">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="d0c63-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d0c63-116">限定詞：覆 [**寫**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Antecedent" ) 、 [**Min**](/windows/desktop/WmiSdk/standard-qualifiers) (0) 、 [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1) </span><span class="sxs-lookup"><span data-stu-id="d0c63-116">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent"), [**Min**](/windows/desktop/WmiSdk/standard-qualifiers) (0), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1)</span></span>
</dt> </dl>

<span data-ttu-id="d0c63-117">代表虛擬系統之 CIM 系統 [**實例 \_**](cim-computersystem.md) 的參考。</span><span class="sxs-lookup"><span data-stu-id="d0c63-117">A reference to the instance of [**CIM\_ComputerSystem**](cim-computersystem.md) that represents the virtual system.</span></span>

</dd> <dt>

<span data-ttu-id="d0c63-118">**依賴**</span><span class="sxs-lookup"><span data-stu-id="d0c63-118">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d0c63-119">資料類型： **CIM \_ VirtualSystemSettingData**</span><span class="sxs-lookup"><span data-stu-id="d0c63-119">Data type: **CIM\_VirtualSystemSettingData**</span></span>
</dt> <dt>

<span data-ttu-id="d0c63-120">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="d0c63-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d0c63-121">限定詞：覆 [**寫**](/windows/desktop/WmiSdk/standard-qualifiers) ( 「相依」 ) 、 [**最小**](/windows/desktop/WmiSdk/standard-qualifiers) (0) 、 [**最大**](/windows/desktop/WmiSdk/standard-qualifiers) (1) </span><span class="sxs-lookup"><span data-stu-id="d0c63-121">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependent"), [**Min**](/windows/desktop/WmiSdk/standard-qualifiers) (0), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1)</span></span>
</dt> </dl>

<span data-ttu-id="d0c63-122">表示虛擬系統快照集之 [**CIM \_ VirtualSystemSettingData**](cim-virtualsystemsettingdata.md) 實例的參考。</span><span class="sxs-lookup"><span data-stu-id="d0c63-122">A reference to the instance of [**CIM\_VirtualSystemSettingData**](cim-virtualsystemsettingdata.md) that represents the virtual system snapshot.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="d0c63-123">規格需求</span><span class="sxs-lookup"><span data-stu-id="d0c63-123">Requirements</span></span>



| <span data-ttu-id="d0c63-124">需求</span><span class="sxs-lookup"><span data-stu-id="d0c63-124">Requirement</span></span> | <span data-ttu-id="d0c63-125">值</span><span class="sxs-lookup"><span data-stu-id="d0c63-125">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d0c63-126">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="d0c63-126">Minimum supported client</span></span><br/> | <span data-ttu-id="d0c63-127">Windows 8</span><span class="sxs-lookup"><span data-stu-id="d0c63-127">Windows 8</span></span><br/>                                                                                    |
| <span data-ttu-id="d0c63-128">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="d0c63-128">Minimum supported server</span></span><br/> | <span data-ttu-id="d0c63-129">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="d0c63-129">Windows Server 2012</span></span><br/>                                                                          |
| <span data-ttu-id="d0c63-130">命名空間</span><span class="sxs-lookup"><span data-stu-id="d0c63-130">Namespace</span></span><br/>                | <span data-ttu-id="d0c63-131">根 \\ 虛擬化 \\ v2</span><span class="sxs-lookup"><span data-stu-id="d0c63-131">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="d0c63-132">MOF</span><span class="sxs-lookup"><span data-stu-id="d0c63-132">MOF</span></span><br/>                      | <dl> <span data-ttu-id="d0c63-133"><dt>WindowsVirtualization。</dt></span><span class="sxs-lookup"><span data-stu-id="d0c63-133"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="d0c63-134">DLL</span><span class="sxs-lookup"><span data-stu-id="d0c63-134">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d0c63-135"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="d0c63-135"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="d0c63-136">另請參閱</span><span class="sxs-lookup"><span data-stu-id="d0c63-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d0c63-137">**CIM \_ 相依性**</span><span class="sxs-lookup"><span data-stu-id="d0c63-137">**CIM\_Dependency**</span></span>](cim-dependency.md)
</dt> </dl>

 

