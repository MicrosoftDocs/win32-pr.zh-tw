---
description: CIM \_ ComputerSystemPackage 類別代表一種關聯，可明確定義單一電腦系統與一或多個實體套件之間的關聯性。
ms.assetid: a91bf09d-0768-4d2a-a0e5-16237b2e6ddc
ms.tgt_platform: multiple
title: CIM_ComputerSystemPackage 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_ComputerSystemPackage
- CIM_ComputerSystemPackage.Dependent
- CIM_ComputerSystemPackage.Antecedent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: a5a2f166c4494b6120bfc5e2aaedeaba4721b155
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103936357"
---
# <a name="cim_computersystempackage-class"></a><span data-ttu-id="08d37-103">CIM \_ ComputerSystemPackage 類別</span><span class="sxs-lookup"><span data-stu-id="08d37-103">CIM\_ComputerSystemPackage class</span></span>

<span data-ttu-id="08d37-104">**CIM \_ ComputerSystemPackage** 類別代表一種關聯，可明確定義單一電腦系統與一或多個實體套件之間的關聯性。</span><span class="sxs-lookup"><span data-stu-id="08d37-104">The **CIM\_ComputerSystemPackage** class represents an association that explicitly defines the relationship between unitary computer systems and one or more physical packages.</span></span> <span data-ttu-id="08d37-105">關聯類似于實體元素實現邏輯裝置的方式。</span><span class="sxs-lookup"><span data-stu-id="08d37-105">The association is similar to the way that logical devices are realized by physical elements.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="08d37-106">DMTF (分散式管理工作強制) CIM (通用訊息模型) 類別是用來建立 WMI 類別的父類別。</span><span class="sxs-lookup"><span data-stu-id="08d37-106">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="08d37-107">WMI 目前僅支援 [CIM 2.x 版的架構](https://dmtf.org/standards/cim/schemas)。</span><span class="sxs-lookup"><span data-stu-id="08d37-107">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="08d37-108">下列語法已從受管理物件格式 (MOF) 程式碼加以簡化，並包含所有繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="08d37-108">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="08d37-109">屬性會依字母順序列出，而不是依 MOF 順序列出。</span><span class="sxs-lookup"><span data-stu-id="08d37-109">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="08d37-110">語法</span><span class="sxs-lookup"><span data-stu-id="08d37-110">Syntax</span></span>

``` syntax
[Abstract, UUID("{FAF76B8D-798C-11D2-AAD1-006008C78BC7}"), AMENDMENT]
class CIM_ComputerSystemPackage : CIM_Dependency
{
  CIM_UnitaryComputerSystem REF Dependent;
  CIM_PhysicalPackage       REF Antecedent;
};
```

## <a name="members"></a><span data-ttu-id="08d37-111">成員</span><span class="sxs-lookup"><span data-stu-id="08d37-111">Members</span></span>

<span data-ttu-id="08d37-112">**CIM \_ ComputerSystemPackage** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="08d37-112">The **CIM\_ComputerSystemPackage** class has these types of members:</span></span>

-   [<span data-ttu-id="08d37-113">屬性</span><span class="sxs-lookup"><span data-stu-id="08d37-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="08d37-114">屬性</span><span class="sxs-lookup"><span data-stu-id="08d37-114">Properties</span></span>

<span data-ttu-id="08d37-115">**CIM \_ ComputerSystemPackage** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="08d37-115">The **CIM\_ComputerSystemPackage** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="08d37-116">**先行**</span><span class="sxs-lookup"><span data-stu-id="08d37-116">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="08d37-117">資料類型： **CIM \_ PhysicalPackage**</span><span class="sxs-lookup"><span data-stu-id="08d37-117">Data type: **CIM\_PhysicalPackage**</span></span>
</dt> <dt>

<span data-ttu-id="08d37-118">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="08d37-118">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="08d37-119">限定詞：覆 [**寫**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Antecedent" ) </span><span class="sxs-lookup"><span data-stu-id="08d37-119">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent")</span></span>
</dt> </dl>

<span data-ttu-id="08d37-120">[**CIM \_ PhysicalPackage**](cim-physicalpackage.md) ，描述可實現單一電腦系統的實體封裝 (s) 。</span><span class="sxs-lookup"><span data-stu-id="08d37-120">A [**CIM\_PhysicalPackage**](cim-physicalpackage.md) that describes the physical package(s) that realize a unitary computer system.</span></span>

</dd> <dt>

<span data-ttu-id="08d37-121">**依賴**</span><span class="sxs-lookup"><span data-stu-id="08d37-121">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="08d37-122">資料類型： **CIM \_ UnitaryComputerSystem**</span><span class="sxs-lookup"><span data-stu-id="08d37-122">Data type: **CIM\_UnitaryComputerSystem**</span></span>
</dt> <dt>

<span data-ttu-id="08d37-123">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="08d37-123">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="08d37-124">限定詞：覆 [**寫**](/windows/desktop/WmiSdk/standard-qualifiers) ( 「相依」 ) </span><span class="sxs-lookup"><span data-stu-id="08d37-124">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependent")</span></span>
</dt> </dl>

<span data-ttu-id="08d37-125">描述單一電腦系統的 [**CIM \_ UnitaryComputerSystem**](cim-unitarycomputersystem.md) 。</span><span class="sxs-lookup"><span data-stu-id="08d37-125">A [**CIM\_UnitaryComputerSystem**](cim-unitarycomputersystem.md) that describes the unitary computer system.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="08d37-126">備註</span><span class="sxs-lookup"><span data-stu-id="08d37-126">Remarks</span></span>

<span data-ttu-id="08d37-127">**Cim \_ ComputerSystemPackage** 類別衍生自 cim 相依 [**性 \_**](cim-dependency.md)。</span><span class="sxs-lookup"><span data-stu-id="08d37-127">The **CIM\_ComputerSystemPackage** class is derived from [**CIM\_Dependency**](cim-dependency.md).</span></span>

<span data-ttu-id="08d37-128">WMI 不會執行這個類別。</span><span class="sxs-lookup"><span data-stu-id="08d37-128">WMI does not implement this class.</span></span>

<span data-ttu-id="08d37-129">此檔衍生自 DMTF 所發佈的 CIM 類別描述。</span><span class="sxs-lookup"><span data-stu-id="08d37-129">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="08d37-130">Microsoft 可能已進行變更，以更正次要錯誤、符合 Microsoft SDK 檔標準，或提供詳細資訊。</span><span class="sxs-lookup"><span data-stu-id="08d37-130">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="08d37-131">規格需求</span><span class="sxs-lookup"><span data-stu-id="08d37-131">Requirements</span></span>



| <span data-ttu-id="08d37-132">需求</span><span class="sxs-lookup"><span data-stu-id="08d37-132">Requirement</span></span> | <span data-ttu-id="08d37-133">值</span><span class="sxs-lookup"><span data-stu-id="08d37-133">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="08d37-134">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="08d37-134">Minimum supported client</span></span><br/> | <span data-ttu-id="08d37-135">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="08d37-135">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="08d37-136">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="08d37-136">Minimum supported server</span></span><br/> | <span data-ttu-id="08d37-137">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="08d37-137">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="08d37-138">命名空間</span><span class="sxs-lookup"><span data-stu-id="08d37-138">Namespace</span></span><br/>                | <span data-ttu-id="08d37-139">根 \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="08d37-139">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="08d37-140">MOF</span><span class="sxs-lookup"><span data-stu-id="08d37-140">MOF</span></span><br/>                      | <dl> <span data-ttu-id="08d37-141"><dt>CIMWin32 mof</dt></span><span class="sxs-lookup"><span data-stu-id="08d37-141"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="08d37-142">DLL</span><span class="sxs-lookup"><span data-stu-id="08d37-142">DLL</span></span><br/>                      | <dl> <span data-ttu-id="08d37-143"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="08d37-143"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="08d37-144">另請參閱</span><span class="sxs-lookup"><span data-stu-id="08d37-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="08d37-145">**CIM \_ 相依性**</span><span class="sxs-lookup"><span data-stu-id="08d37-145">**CIM\_Dependency**</span></span>](cim-dependency.md)
</dt> </dl>

 

