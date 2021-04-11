---
description: CIM \_ HostedJobDestination 類別代表作業目的地與其所在系統之間的關聯。 系統可能會裝載許多作業佇列。 作業目的地會延後到裝載系統。
ms.assetid: 5d853826-1f27-417b-a053-5e0ee9816376
ms.tgt_platform: multiple
title: CIM_HostedJobDestination 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_HostedJobDestination
- CIM_HostedJobDestination.Dependent
- CIM_HostedJobDestination.Antecedent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: c22e911c6b0adcc38de11fd2410e4797c9381a25
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104187758"
---
# <a name="cim_hostedjobdestination-class"></a><span data-ttu-id="0d15e-105">CIM \_ HostedJobDestination 類別</span><span class="sxs-lookup"><span data-stu-id="0d15e-105">CIM\_HostedJobDestination class</span></span>

<span data-ttu-id="0d15e-106">**CIM \_ HostedJobDestination** 類別代表作業目的地與其所在系統之間的關聯。</span><span class="sxs-lookup"><span data-stu-id="0d15e-106">The **CIM\_HostedJobDestination** class represents an association between a job destination and the system on which it resides.</span></span> <span data-ttu-id="0d15e-107">系統可能會裝載許多作業佇列。</span><span class="sxs-lookup"><span data-stu-id="0d15e-107">A system may host many job queues.</span></span> <span data-ttu-id="0d15e-108">作業目的地會延後到裝載系統。</span><span class="sxs-lookup"><span data-stu-id="0d15e-108">Job destinations defer to the hosting system.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="0d15e-109">DMTF (分散式管理工作強制) CIM (通用訊息模型) 類別是用來建立 WMI 類別的父類別。</span><span class="sxs-lookup"><span data-stu-id="0d15e-109">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="0d15e-110">WMI 目前僅支援 [CIM 2.x 版的架構](https://dmtf.org/standards/cim/schemas)。</span><span class="sxs-lookup"><span data-stu-id="0d15e-110">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="0d15e-111">下列語法已從受管理物件格式 (MOF) 程式碼加以簡化，並包含所有繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="0d15e-111">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="0d15e-112">屬性會依字母順序列出，而不是依 MOF 順序列出。</span><span class="sxs-lookup"><span data-stu-id="0d15e-112">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="0d15e-113">語法</span><span class="sxs-lookup"><span data-stu-id="0d15e-113">Syntax</span></span>

``` syntax
[Abstract, UUID("{7880DD16-DB36-11d2-85FC-0000F8102E5F}"), AMENDMENT]
class CIM_HostedJobDestination : CIM_Dependency
{
  CIM_JobDestination REF Dependent;
  CIM_System         REF Antecedent;
};
```

## <a name="members"></a><span data-ttu-id="0d15e-114">成員</span><span class="sxs-lookup"><span data-stu-id="0d15e-114">Members</span></span>

<span data-ttu-id="0d15e-115">**CIM \_ HostedJobDestination** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="0d15e-115">The **CIM\_HostedJobDestination** class has these types of members:</span></span>

-   [<span data-ttu-id="0d15e-116">屬性</span><span class="sxs-lookup"><span data-stu-id="0d15e-116">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="0d15e-117">屬性</span><span class="sxs-lookup"><span data-stu-id="0d15e-117">Properties</span></span>

<span data-ttu-id="0d15e-118">**CIM \_ HostedJobDestination** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="0d15e-118">The **CIM\_HostedJobDestination** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="0d15e-119">**先行**</span><span class="sxs-lookup"><span data-stu-id="0d15e-119">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0d15e-120">資料類型： **CIM \_ 系統**</span><span class="sxs-lookup"><span data-stu-id="0d15e-120">Data type: **CIM\_System**</span></span>
</dt> <dt>

<span data-ttu-id="0d15e-121">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="0d15e-121">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0d15e-122">限定詞： [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1) 、 [**Min**](/windows/desktop/WmiSdk/standard-qualifiers) (1) 、覆 [**寫**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Antecedent" ) </span><span class="sxs-lookup"><span data-stu-id="0d15e-122">Qualifiers: [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**Min**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent")</span></span>
</dt> </dl>

<span data-ttu-id="0d15e-123">描述裝載系統的 [**CIM \_ 系統**](cim-system.md) 。</span><span class="sxs-lookup"><span data-stu-id="0d15e-123">A [**CIM\_System**](cim-system.md) that describes the hosting system.</span></span>

</dd> <dt>

<span data-ttu-id="0d15e-124">**依賴**</span><span class="sxs-lookup"><span data-stu-id="0d15e-124">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0d15e-125">資料類型： **CIM \_ JobDestination**</span><span class="sxs-lookup"><span data-stu-id="0d15e-125">Data type: **CIM\_JobDestination**</span></span>
</dt> <dt>

<span data-ttu-id="0d15e-126">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="0d15e-126">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0d15e-127">限定詞：覆 [**寫**](/windows/desktop/WmiSdk/standard-qualifiers) ( 「相依」 ) 、[**弱**](/windows/desktop/WmiSdk/standard-qualifiers)式</span><span class="sxs-lookup"><span data-stu-id="0d15e-127">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependent"), [**Weak**](/windows/desktop/WmiSdk/standard-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="0d15e-128">[**CIM \_ JobDestination**](cim-jobdestination.md) ，描述系統上裝載的作業目的地。</span><span class="sxs-lookup"><span data-stu-id="0d15e-128">A [**CIM\_JobDestination**](cim-jobdestination.md) describing the job destination hosted on the system.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="0d15e-129">備註</span><span class="sxs-lookup"><span data-stu-id="0d15e-129">Remarks</span></span>

<span data-ttu-id="0d15e-130">**CIM \_HostedJobDestination** 衍生自 [**CIM 相依 \_**](cim-dependency.md)性。</span><span class="sxs-lookup"><span data-stu-id="0d15e-130">**CIM\_HostedJobDestination** is derived from [**CIM\_Dependency**](cim-dependency.md).</span></span>

<span data-ttu-id="0d15e-131">WMI 不會執行這個類別。</span><span class="sxs-lookup"><span data-stu-id="0d15e-131">WMI does not implement this class.</span></span>

<span data-ttu-id="0d15e-132">此檔衍生自 DMTF 所發佈的 CIM 類別描述。</span><span class="sxs-lookup"><span data-stu-id="0d15e-132">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="0d15e-133">Microsoft 可能已進行變更，以更正次要錯誤、符合 Microsoft SDK 檔標準，或提供詳細資訊。</span><span class="sxs-lookup"><span data-stu-id="0d15e-133">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="0d15e-134">規格需求</span><span class="sxs-lookup"><span data-stu-id="0d15e-134">Requirements</span></span>



| <span data-ttu-id="0d15e-135">需求</span><span class="sxs-lookup"><span data-stu-id="0d15e-135">Requirement</span></span> | <span data-ttu-id="0d15e-136">值</span><span class="sxs-lookup"><span data-stu-id="0d15e-136">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="0d15e-137">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="0d15e-137">Minimum supported client</span></span><br/> | <span data-ttu-id="0d15e-138">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="0d15e-138">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="0d15e-139">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="0d15e-139">Minimum supported server</span></span><br/> | <span data-ttu-id="0d15e-140">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="0d15e-140">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="0d15e-141">命名空間</span><span class="sxs-lookup"><span data-stu-id="0d15e-141">Namespace</span></span><br/>                | <span data-ttu-id="0d15e-142">根 \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="0d15e-142">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="0d15e-143">MOF</span><span class="sxs-lookup"><span data-stu-id="0d15e-143">MOF</span></span><br/>                      | <dl> <span data-ttu-id="0d15e-144"><dt>CIMWin32 mof</dt></span><span class="sxs-lookup"><span data-stu-id="0d15e-144"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="0d15e-145">DLL</span><span class="sxs-lookup"><span data-stu-id="0d15e-145">DLL</span></span><br/>                      | <dl> <span data-ttu-id="0d15e-146"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0d15e-146"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0d15e-147">另請參閱</span><span class="sxs-lookup"><span data-stu-id="0d15e-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0d15e-148">**CIM \_ 相依性**</span><span class="sxs-lookup"><span data-stu-id="0d15e-148">**CIM\_Dependency**</span></span>](cim-dependency.md)
</dt> </dl>

 

