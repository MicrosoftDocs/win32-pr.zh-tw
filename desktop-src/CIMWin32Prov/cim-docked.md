---
description: CIM 停駐 \_ 關聯表示兩個底座之間的關聯性。 例如，膝上型電腦 (一種底座) 可停駐在銜接站 (另一種類型的底座) 。 這是明確描述的一般關聯性。
ms.assetid: 72cb36bb-f79e-4d1a-a859-4024031e4ebc
ms.tgt_platform: multiple
title: CIM_Docked 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_Docked
- CIM_Docked.Dependent
- CIM_Docked.Antecedent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 899b85d63293861f0a36df3d3c30610f8cff05ac
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103688923"
---
# <a name="cim_docked-class"></a><span data-ttu-id="0f3db-105">CIM 停駐 \_ 類別</span><span class="sxs-lookup"><span data-stu-id="0f3db-105">CIM\_Docked class</span></span>

<span data-ttu-id="0f3db-106">**CIM 停 \_** 駐關聯表示兩個底座之間的關聯性。</span><span class="sxs-lookup"><span data-stu-id="0f3db-106">The **CIM\_Docked** association represents the relationship between two chassis.</span></span> <span data-ttu-id="0f3db-107">例如，膝上型電腦 (一種底座) 可停駐在銜接站 (另一種類型的底座) 。</span><span class="sxs-lookup"><span data-stu-id="0f3db-107">For example, a laptop (a type of chassis) can be docked in a docking station (another type of chassis).</span></span> <span data-ttu-id="0f3db-108">這是明確描述的一般關聯性。</span><span class="sxs-lookup"><span data-stu-id="0f3db-108">This typical relationship is explicitly described.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="0f3db-109">DMTF (分散式管理工作強制) CIM (通用訊息模型) 類別是用來建立 WMI 類別的父類別。</span><span class="sxs-lookup"><span data-stu-id="0f3db-109">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="0f3db-110">WMI 目前僅支援 [CIM 2.x 版的架構](https://dmtf.org/standards/cim/schemas)。</span><span class="sxs-lookup"><span data-stu-id="0f3db-110">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="0f3db-111">下列語法是簡化自 MOF 程式碼，且包含所有繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="0f3db-111">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="0f3db-112">語法</span><span class="sxs-lookup"><span data-stu-id="0f3db-112">Syntax</span></span>

``` syntax
[Abstract, MappingStrings("MIF.DMTF|Dynamic States|001.2"), UUID("{FAF76B75-798C-11D2-AAD1-006008C78BC7}"), AMENDMENT]
class CIM_Docked : CIM_Dependency
{
  CIM_Chassis REF Dependent;
  CIM_Chassis REF Antecedent;
};
```

## <a name="members"></a><span data-ttu-id="0f3db-113">成員</span><span class="sxs-lookup"><span data-stu-id="0f3db-113">Members</span></span>

<span data-ttu-id="0f3db-114">**CIM 停 \_** 駐類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="0f3db-114">The **CIM\_Docked** class has these types of members:</span></span>

-   [<span data-ttu-id="0f3db-115">屬性</span><span class="sxs-lookup"><span data-stu-id="0f3db-115">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="0f3db-116">屬性</span><span class="sxs-lookup"><span data-stu-id="0f3db-116">Properties</span></span>

<span data-ttu-id="0f3db-117">**CIM 停 \_** 駐類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="0f3db-117">The **CIM\_Docked** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="0f3db-118">**先行**</span><span class="sxs-lookup"><span data-stu-id="0f3db-118">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0f3db-119">資料類型： **CIM \_ 底座**</span><span class="sxs-lookup"><span data-stu-id="0f3db-119">Data type: **CIM\_Chassis**</span></span>
</dt> <dt>

<span data-ttu-id="0f3db-120">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="0f3db-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0f3db-121">限定詞：覆 [**寫**](/windows/desktop/WmiSdk/standard-qualifiers) ( 「Antecedent」 ) ， [**最大**](/windows/desktop/WmiSdk/standard-qualifiers) (1) </span><span class="sxs-lookup"><span data-stu-id="0f3db-121">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent"), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1)</span></span>
</dt> </dl>

<span data-ttu-id="0f3db-122">描述銜接站的 [**CIM \_ 底座**](cim-chassis.md) 。</span><span class="sxs-lookup"><span data-stu-id="0f3db-122">A [**CIM\_Chassis**](cim-chassis.md) describing the docking station.</span></span>

</dd> <dt>

<span data-ttu-id="0f3db-123">**依賴**</span><span class="sxs-lookup"><span data-stu-id="0f3db-123">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0f3db-124">資料類型： **CIM \_ 底座**</span><span class="sxs-lookup"><span data-stu-id="0f3db-124">Data type: **CIM\_Chassis**</span></span>
</dt> <dt>

<span data-ttu-id="0f3db-125">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="0f3db-125">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0f3db-126">限定詞：覆 [**寫**](/windows/desktop/WmiSdk/standard-qualifiers) ( 「相依」 ) ， [**最大**](/windows/desktop/WmiSdk/standard-qualifiers) (1) </span><span class="sxs-lookup"><span data-stu-id="0f3db-126">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependent"), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1)</span></span>
</dt> </dl>

<span data-ttu-id="0f3db-127">描述固定膝上型電腦的 [**CIM \_ 底座**](cim-chassis.md) 。</span><span class="sxs-lookup"><span data-stu-id="0f3db-127">A [**CIM\_Chassis**](cim-chassis.md) describing the docked laptop.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="0f3db-128">備註</span><span class="sxs-lookup"><span data-stu-id="0f3db-128">Remarks</span></span>

<span data-ttu-id="0f3db-129">**Cim 停 \_ 駐** 類別衍生自 [**cim 相依 \_**](cim-dependency.md)性。</span><span class="sxs-lookup"><span data-stu-id="0f3db-129">The **CIM\_Docked** class is derived from [**CIM\_Dependency**](cim-dependency.md).</span></span>

<span data-ttu-id="0f3db-130">WMI 不會執行這個類別。</span><span class="sxs-lookup"><span data-stu-id="0f3db-130">WMI does not implement this class.</span></span>

<span data-ttu-id="0f3db-131">此檔衍生自 DMTF 所發佈的 CIM 類別描述。</span><span class="sxs-lookup"><span data-stu-id="0f3db-131">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="0f3db-132">Microsoft 可能已進行變更，以更正次要錯誤、符合 Microsoft SDK 檔標準，或提供詳細資訊。</span><span class="sxs-lookup"><span data-stu-id="0f3db-132">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="0f3db-133">規格需求</span><span class="sxs-lookup"><span data-stu-id="0f3db-133">Requirements</span></span>



| <span data-ttu-id="0f3db-134">需求</span><span class="sxs-lookup"><span data-stu-id="0f3db-134">Requirement</span></span> | <span data-ttu-id="0f3db-135">值</span><span class="sxs-lookup"><span data-stu-id="0f3db-135">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="0f3db-136">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="0f3db-136">Minimum supported client</span></span><br/> | <span data-ttu-id="0f3db-137">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="0f3db-137">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="0f3db-138">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="0f3db-138">Minimum supported server</span></span><br/> | <span data-ttu-id="0f3db-139">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="0f3db-139">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="0f3db-140">命名空間</span><span class="sxs-lookup"><span data-stu-id="0f3db-140">Namespace</span></span><br/>                | <span data-ttu-id="0f3db-141">根 \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="0f3db-141">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="0f3db-142">MOF</span><span class="sxs-lookup"><span data-stu-id="0f3db-142">MOF</span></span><br/>                      | <dl> <span data-ttu-id="0f3db-143"><dt>CIMWin32 mof</dt></span><span class="sxs-lookup"><span data-stu-id="0f3db-143"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="0f3db-144">DLL</span><span class="sxs-lookup"><span data-stu-id="0f3db-144">DLL</span></span><br/>                      | <dl> <span data-ttu-id="0f3db-145"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0f3db-145"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0f3db-146">另請參閱</span><span class="sxs-lookup"><span data-stu-id="0f3db-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0f3db-147">**CIM \_ 相依性**</span><span class="sxs-lookup"><span data-stu-id="0f3db-147">**CIM\_Dependency**</span></span>](cim-dependency.md)
</dt> </dl>

 

