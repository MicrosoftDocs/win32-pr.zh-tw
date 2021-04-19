---
description: CIM VirtualSystemSettingData 的實例 \_ 和 cim VirtualSystemSettingData 實例之間的關聯， \_ 代表這個物件所依據的最新快照集。
ms.assetid: f6e93c22-077b-4604-8d0d-9584b1f4dce1
ms.tgt_platform: multiple
title: CIM_ParentChildSettingData 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_ParentChildSettingData
- Root\CIMV2.CIM_ParentChildSettingData.Antecedent
- Root\CIMV2.CIM_ParentChildSettingData.Dependent
- Root\CIMV2.CIM_ParentChildSettingData.Parent
- Root\CIMV2.CIM_ParentChildSettingData.Child
api_type:
- Schema
api_location:
- Root\CIMV2
ms.openlocfilehash: 9b2b866c3d5ae15d3f5a97c971e8efec75e9164c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106993404"
---
# <a name="cim_parentchildsettingdata-class"></a><span data-ttu-id="a95d6-103">CIM \_ ParentChildSettingData 類別</span><span class="sxs-lookup"><span data-stu-id="a95d6-103">CIM\_ParentChildSettingData class</span></span>

<span data-ttu-id="a95d6-104">[**Cim \_ VirtualSystemSettingData**](/previous-versions/windows/desktop/clushyperv/cim-virtualsystemsettingdata)的實例和 **cim \_ VirtualSystemSettingData** 實例之間的關聯，代表這個物件所依據的最新快照集。</span><span class="sxs-lookup"><span data-stu-id="a95d6-104">An association between an instance of [**CIM\_VirtualSystemSettingData**](/previous-versions/windows/desktop/clushyperv/cim-virtualsystemsettingdata) and the **CIM\_VirtualSystemSettingData** instance which represents the most recent snapshot upon which this object is based.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="a95d6-105">DMTF (分散式管理工作強制) CIM (通用訊息模型) 類別是用來建立 WMI 類別的父類別。</span><span class="sxs-lookup"><span data-stu-id="a95d6-105">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="a95d6-106">WMI 目前僅支援 [CIM 2.x 版的架構](https://dmtf.org/standards/cim/schemas)。</span><span class="sxs-lookup"><span data-stu-id="a95d6-106">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="a95d6-107">下列語法已經過受管理物件格式 (MOF) 程式碼簡化，並包含所有已繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="a95d6-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="a95d6-108">語法</span><span class="sxs-lookup"><span data-stu-id="a95d6-108">Syntax</span></span>

``` syntax
class CIM_ParentChildSettingData : CIM_Dependency
{
  CIM_ManagedSystemElement     REF Antecedent;
  CIM_ManagedSystemElement     REF Dependent;
  CIM_VirtualSystemSettingData REF Parent;
  CIM_VirtualSystemSettingData REF Child;
};
```

## <a name="members"></a><span data-ttu-id="a95d6-109">成員</span><span class="sxs-lookup"><span data-stu-id="a95d6-109">Members</span></span>

<span data-ttu-id="a95d6-110">**CIM \_ ParentChildSettingData** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="a95d6-110">The **CIM\_ParentChildSettingData** class has these types of members:</span></span>

-   [<span data-ttu-id="a95d6-111">屬性</span><span class="sxs-lookup"><span data-stu-id="a95d6-111">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="a95d6-112">屬性</span><span class="sxs-lookup"><span data-stu-id="a95d6-112">Properties</span></span>

<span data-ttu-id="a95d6-113">**CIM \_ ParentChildSettingData** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="a95d6-113">The **CIM\_ParentChildSettingData** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="a95d6-114">**先行**</span><span class="sxs-lookup"><span data-stu-id="a95d6-114">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a95d6-115">資料類型： **CIM \_ ManagedSystemElement**</span><span class="sxs-lookup"><span data-stu-id="a95d6-115">Data type: **CIM\_ManagedSystemElement**</span></span>
</dt> <dt>

<span data-ttu-id="a95d6-116">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="a95d6-116">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a95d6-117">參考此關聯中的獨立物件。</span><span class="sxs-lookup"><span data-stu-id="a95d6-117">Reference to the independent object in this association.</span></span>

<span data-ttu-id="a95d6-118">這個屬性繼承自 [**CIM 相依 \_**](/windows/desktop/CIMWin32Prov/cim-dependency)性。</span><span class="sxs-lookup"><span data-stu-id="a95d6-118">This property is inherited from [**CIM\_Dependency**](/windows/desktop/CIMWin32Prov/cim-dependency).</span></span>

</dd> <dt>

<span data-ttu-id="a95d6-119">**子系**</span><span class="sxs-lookup"><span data-stu-id="a95d6-119">**Child**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a95d6-120">資料類型： **CIM \_ VirtualSystemSettingData**</span><span class="sxs-lookup"><span data-stu-id="a95d6-120">Data type: **CIM\_VirtualSystemSettingData**</span></span>
</dt> <dt>

<span data-ttu-id="a95d6-121">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="a95d6-121">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a95d6-122">虛擬系統的設定資料，代表父系的子系。</span><span class="sxs-lookup"><span data-stu-id="a95d6-122">The setting data for the virtual system which represents the child of the Parent.</span></span>

</dd> <dt>

<span data-ttu-id="a95d6-123">**依賴**</span><span class="sxs-lookup"><span data-stu-id="a95d6-123">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a95d6-124">資料類型： **CIM \_ ManagedSystemElement**</span><span class="sxs-lookup"><span data-stu-id="a95d6-124">Data type: **CIM\_ManagedSystemElement**</span></span>
</dt> <dt>

<span data-ttu-id="a95d6-125">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="a95d6-125">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a95d6-126">相依于 **Antecedent** 屬性之物件的參考。</span><span class="sxs-lookup"><span data-stu-id="a95d6-126">Reference to the object that is dependent on the **Antecedent** property.</span></span>

<span data-ttu-id="a95d6-127">這個屬性繼承自 [**CIM 相依 \_**](/windows/desktop/CIMWin32Prov/cim-dependency)性。</span><span class="sxs-lookup"><span data-stu-id="a95d6-127">This property is inherited from [**CIM\_Dependency**](/windows/desktop/CIMWin32Prov/cim-dependency).</span></span>

</dd> <dt>

<span data-ttu-id="a95d6-128">**父系**</span><span class="sxs-lookup"><span data-stu-id="a95d6-128">**Parent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a95d6-129">資料類型： **CIM \_ VirtualSystemSettingData**</span><span class="sxs-lookup"><span data-stu-id="a95d6-129">Data type: **CIM\_VirtualSystemSettingData**</span></span>
</dt> <dt>

<span data-ttu-id="a95d6-130">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="a95d6-130">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a95d6-131">子設定資料所依據的快照集設定資料。</span><span class="sxs-lookup"><span data-stu-id="a95d6-131">The snapshot setting data upon which the Child setting data is based.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="a95d6-132">規格需求</span><span class="sxs-lookup"><span data-stu-id="a95d6-132">Requirements</span></span>



| <span data-ttu-id="a95d6-133">需求</span><span class="sxs-lookup"><span data-stu-id="a95d6-133">Requirement</span></span> | <span data-ttu-id="a95d6-134">值</span><span class="sxs-lookup"><span data-stu-id="a95d6-134">Value</span></span> |
|----------------------|------------------------|
| <span data-ttu-id="a95d6-135">命名空間</span><span class="sxs-lookup"><span data-stu-id="a95d6-135">Namespace</span></span><br/> | <span data-ttu-id="a95d6-136">根 \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="a95d6-136">Root\\CIMV2</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="a95d6-137">另請參閱</span><span class="sxs-lookup"><span data-stu-id="a95d6-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a95d6-138">**CIM \_ 相依性**</span><span class="sxs-lookup"><span data-stu-id="a95d6-138">**CIM\_Dependency**</span></span>](/windows/desktop/CIMWin32Prov/cim-dependency)
</dt> </dl>

 

