---
description: CIM \_ HostedBootSAP 類別會定義 cim BootSAP 類別的裝載單一電腦系統 \_ 。
ms.assetid: 2113de13-e7af-4a1c-ba80-27e2c57af8a0
ms.tgt_platform: multiple
title: CIM_HostedBootSAP 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_HostedBootSAP
- CIM_HostedBootSAP.Dependent
- CIM_HostedBootSAP.Antecedent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 12e801f420ca2c56cc8960175391cdd9a669a00d
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103936310"
---
# <a name="cim_hostedbootsap-class"></a><span data-ttu-id="bc702-103">CIM \_ HostedBootSAP 類別</span><span class="sxs-lookup"><span data-stu-id="bc702-103">CIM\_HostedBootSAP class</span></span>

<span data-ttu-id="bc702-104">**Cim \_ HostedBootSAP** 類別會定義 [**cim \_ BootSAP**](cim-bootsap.md)類別的裝載單一電腦系統。</span><span class="sxs-lookup"><span data-stu-id="bc702-104">The **CIM\_HostedBootSAP** class defines the hosting unitary computer system for a [**CIM\_BootSAP**](cim-bootsap.md) class.</span></span> <span data-ttu-id="bc702-105">由於此關聯性是從 [**cim \_ HostedAccessPoint**](cim-hostedaccesspoint.md)子類別化，因此它會繼承針對 [**cim \_ ServiceAccessPoint**](cim-serviceaccesspoint.md)定義的範圍/命名配置，其中存取點會延遲至其主機系統。</span><span class="sxs-lookup"><span data-stu-id="bc702-105">Since this relationship is subclassed from [**CIM\_HostedAccessPoint**](cim-hostedaccesspoint.md), it inherits the scoping/naming scheme defined for [**CIM\_ServiceAccessPoint**](cim-serviceaccesspoint.md), where an access point defers to its hosting system.</span></span> <span data-ttu-id="bc702-106">在此情況下， **CIM \_ BootSAP** 必須延後至其裝載的 [**CIM \_ UnitaryComputerSystem**](cim-unitarycomputersystem.md) 類別。</span><span class="sxs-lookup"><span data-stu-id="bc702-106">In this case, **CIM\_BootSAP** must defer to its hosting [**CIM\_UnitaryComputerSystem**](cim-unitarycomputersystem.md) class.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="bc702-107">DMTF (分散式管理工作強制) CIM (通用訊息模型) 類別是用來建立 WMI 類別的父類別。</span><span class="sxs-lookup"><span data-stu-id="bc702-107">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="bc702-108">WMI 目前僅支援 [CIM 2.x 版的架構](https://dmtf.org/standards/cim/schemas)。</span><span class="sxs-lookup"><span data-stu-id="bc702-108">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="bc702-109">下列語法已從受管理物件格式 (MOF) 程式碼加以簡化，並包含所有繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="bc702-109">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="bc702-110">屬性會依字母順序列出，而不是依 MOF 順序列出。</span><span class="sxs-lookup"><span data-stu-id="bc702-110">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="bc702-111">語法</span><span class="sxs-lookup"><span data-stu-id="bc702-111">Syntax</span></span>

``` syntax
[Abstract, UUID("{625B4512-DB36-11d2-85FC-0000F8102E5F}"), AMENDMENT]
class CIM_HostedBootSAP : CIM_HostedAccessPoint
{
  CIM_BootSAP               REF Dependent;
  CIM_UnitaryComputerSystem REF Antecedent;
};
```

## <a name="members"></a><span data-ttu-id="bc702-112">成員</span><span class="sxs-lookup"><span data-stu-id="bc702-112">Members</span></span>

<span data-ttu-id="bc702-113">**CIM \_ HostedBootSAP** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="bc702-113">The **CIM\_HostedBootSAP** class has these types of members:</span></span>

-   [<span data-ttu-id="bc702-114">屬性</span><span class="sxs-lookup"><span data-stu-id="bc702-114">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="bc702-115">屬性</span><span class="sxs-lookup"><span data-stu-id="bc702-115">Properties</span></span>

<span data-ttu-id="bc702-116">**CIM \_ HostedBootSAP** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="bc702-116">The **CIM\_HostedBootSAP** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="bc702-117">**先行**</span><span class="sxs-lookup"><span data-stu-id="bc702-117">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bc702-118">資料類型： **CIM \_ UnitaryComputerSystem**</span><span class="sxs-lookup"><span data-stu-id="bc702-118">Data type: **CIM\_UnitaryComputerSystem**</span></span>
</dt> <dt>

<span data-ttu-id="bc702-119">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="bc702-119">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="bc702-120">限定詞：覆 [**寫**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Antecedent" ) </span><span class="sxs-lookup"><span data-stu-id="bc702-120">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent")</span></span>
</dt> </dl>

<span data-ttu-id="bc702-121">描述單一電腦系統的 [**CIM \_ UnitaryComputerSystem**](cim-unitarycomputersystem.md) 。</span><span class="sxs-lookup"><span data-stu-id="bc702-121">A [**CIM\_UnitaryComputerSystem**](cim-unitarycomputersystem.md) that describes the unitary computer system.</span></span>

</dd> <dt>

<span data-ttu-id="bc702-122">**依賴**</span><span class="sxs-lookup"><span data-stu-id="bc702-122">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bc702-123">資料類型： **CIM \_ BootSAP**</span><span class="sxs-lookup"><span data-stu-id="bc702-123">Data type: **CIM\_BootSAP**</span></span>
</dt> <dt>

<span data-ttu-id="bc702-124">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="bc702-124">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="bc702-125">限定詞：覆 [**寫**](/windows/desktop/WmiSdk/standard-qualifiers) ( 「相依」 ) </span><span class="sxs-lookup"><span data-stu-id="bc702-125">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependent")</span></span>
</dt> </dl>

<span data-ttu-id="bc702-126">[**CIM \_ BootSAP**](cim-bootsap.md) ，描述裝載于單一電腦系統上的開機 SAP。</span><span class="sxs-lookup"><span data-stu-id="bc702-126">A [**CIM\_BootSAP**](cim-bootsap.md) that describes the Boot SAP hosted on the unitary computer system.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="bc702-127">備註</span><span class="sxs-lookup"><span data-stu-id="bc702-127">Remarks</span></span>

<span data-ttu-id="bc702-128">**Cim \_ HostedBootSAP** 類別衍生自 [**cim \_ HostedAccessPoint**](cim-hostedaccesspoint.md)。</span><span class="sxs-lookup"><span data-stu-id="bc702-128">The **CIM\_HostedBootSAP** class is derived from [**CIM\_HostedAccessPoint**](cim-hostedaccesspoint.md).</span></span>

<span data-ttu-id="bc702-129">WMI 不會執行這個類別。</span><span class="sxs-lookup"><span data-stu-id="bc702-129">WMI does not implement this class.</span></span>

<span data-ttu-id="bc702-130">此檔衍生自 DMTF 所發佈的 CIM 類別描述。</span><span class="sxs-lookup"><span data-stu-id="bc702-130">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="bc702-131">Microsoft 可能已進行變更，以更正次要錯誤、符合 Microsoft SDK 檔標準，或提供詳細資訊。</span><span class="sxs-lookup"><span data-stu-id="bc702-131">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="bc702-132">規格需求</span><span class="sxs-lookup"><span data-stu-id="bc702-132">Requirements</span></span>



| <span data-ttu-id="bc702-133">需求</span><span class="sxs-lookup"><span data-stu-id="bc702-133">Requirement</span></span> | <span data-ttu-id="bc702-134">值</span><span class="sxs-lookup"><span data-stu-id="bc702-134">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="bc702-135">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="bc702-135">Minimum supported client</span></span><br/> | <span data-ttu-id="bc702-136">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="bc702-136">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="bc702-137">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="bc702-137">Minimum supported server</span></span><br/> | <span data-ttu-id="bc702-138">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="bc702-138">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="bc702-139">命名空間</span><span class="sxs-lookup"><span data-stu-id="bc702-139">Namespace</span></span><br/>                | <span data-ttu-id="bc702-140">根 \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="bc702-140">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="bc702-141">MOF</span><span class="sxs-lookup"><span data-stu-id="bc702-141">MOF</span></span><br/>                      | <dl> <span data-ttu-id="bc702-142"><dt>CIMWin32 mof</dt></span><span class="sxs-lookup"><span data-stu-id="bc702-142"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="bc702-143">DLL</span><span class="sxs-lookup"><span data-stu-id="bc702-143">DLL</span></span><br/>                      | <dl> <span data-ttu-id="bc702-144"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="bc702-144"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="bc702-145">另請參閱</span><span class="sxs-lookup"><span data-stu-id="bc702-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bc702-146">**CIM \_ HostedAccessPoint**</span><span class="sxs-lookup"><span data-stu-id="bc702-146">**CIM\_HostedAccessPoint**</span></span>](cim-hostedaccesspoint.md)
</dt> </dl>

 

