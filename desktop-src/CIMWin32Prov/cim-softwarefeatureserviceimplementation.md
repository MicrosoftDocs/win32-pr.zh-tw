---
description: CIM \_ SoftwareFeatureServiceImplementation 類別代表服務之間的關聯，以及它在軟體中的執行方式。
ms.assetid: fa80cc91-8dd7-4726-a24a-5c4dfa3e786b
ms.tgt_platform: multiple
title: CIM_SoftwareFeatureServiceImplementation 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_SoftwareFeatureServiceImplementation
- CIM_SoftwareFeatureServiceImplementation.Dependent
- CIM_SoftwareFeatureServiceImplementation.Antecedent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: dc521de933a4567c0760495880baf9251a774938
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104110177"
---
# <a name="cim_softwarefeatureserviceimplementation-class"></a><span data-ttu-id="5ecba-103">CIM \_ SoftwareFeatureServiceImplementation 類別</span><span class="sxs-lookup"><span data-stu-id="5ecba-103">CIM\_SoftwareFeatureServiceImplementation class</span></span>

<span data-ttu-id="5ecba-104">**CIM \_ SoftwareFeatureServiceImplementation** 類別代表服務之間的關聯，以及它在軟體中的執行方式。</span><span class="sxs-lookup"><span data-stu-id="5ecba-104">The **CIM\_SoftwareFeatureServiceImplementation** class represents an association between a service and how it is implemented in software.</span></span> <span data-ttu-id="5ecba-105">服務可以透過多個軟體功能提供，並與另一個功能一起運作。</span><span class="sxs-lookup"><span data-stu-id="5ecba-105">A service can be provided by more than one software feature, operating in conjunction with one another.</span></span> <span data-ttu-id="5ecba-106">此外，軟體功能可以提供多項服務。</span><span class="sxs-lookup"><span data-stu-id="5ecba-106">Additionally, a software feature can provide more than one service.</span></span> <span data-ttu-id="5ecba-107">當多個軟體功能與單一服務相關聯時，會假設這些專案會搭配運作來提供服務。</span><span class="sxs-lookup"><span data-stu-id="5ecba-107">When multiple software features are associated with a single service, it is assumed that the elements operate in conjunction to provide the service.</span></span> <span data-ttu-id="5ecba-108">如果服務有不同的執行，則每個執行都會導致服務物件的個別具現化。</span><span class="sxs-lookup"><span data-stu-id="5ecba-108">If different implementations of a service exist, each implementation would result in individual instantiations of the service object.</span></span> <span data-ttu-id="5ecba-109">然後，個別具現化會與唯一的實作為關聯。</span><span class="sxs-lookup"><span data-stu-id="5ecba-109">Individual instantiations would then have associations to the unique implementations.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="5ecba-110">DMTF (分散式管理工作強制) CIM (通用訊息模型) 類別是用來建立 WMI 類別的父類別。</span><span class="sxs-lookup"><span data-stu-id="5ecba-110">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="5ecba-111">WMI 目前僅支援 [CIM 2.x 版的架構](https://dmtf.org/standards/cim/schemas)。</span><span class="sxs-lookup"><span data-stu-id="5ecba-111">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="5ecba-112">下列語法已從受控物件格式的 (MOF) 程式碼簡化，並包含其所有繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="5ecba-112">The following syntax is simplified from Managed Object Format (MOF) code and includes all of its inherited properties.</span></span> <span data-ttu-id="5ecba-113">屬性會依字母順序列出，而不是依 MOF 順序列出。</span><span class="sxs-lookup"><span data-stu-id="5ecba-113">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="5ecba-114">語法</span><span class="sxs-lookup"><span data-stu-id="5ecba-114">Syntax</span></span>

``` syntax
[UUID("{8AC984F4-DB37-11d2-85FC-0000F8102E5F}"), Abstract, AMENDMENT]
class CIM_SoftwareFeatureServiceImplementation : CIM_Dependency
{
  CIM_Service         REF Dependent;
  CIM_SoftwareFeature REF Antecedent;
};
```

## <a name="members"></a><span data-ttu-id="5ecba-115">成員</span><span class="sxs-lookup"><span data-stu-id="5ecba-115">Members</span></span>

<span data-ttu-id="5ecba-116">**CIM \_ SoftwareFeatureServiceImplementation** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="5ecba-116">The **CIM\_SoftwareFeatureServiceImplementation** class has these types of members:</span></span>

-   [<span data-ttu-id="5ecba-117">屬性</span><span class="sxs-lookup"><span data-stu-id="5ecba-117">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="5ecba-118">屬性</span><span class="sxs-lookup"><span data-stu-id="5ecba-118">Properties</span></span>

<span data-ttu-id="5ecba-119">**CIM \_ SoftwareFeatureServiceImplementation** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="5ecba-119">The **CIM\_SoftwareFeatureServiceImplementation** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="5ecba-120">**先行**</span><span class="sxs-lookup"><span data-stu-id="5ecba-120">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5ecba-121">資料類型： **CIM \_ SoftwareFeature**</span><span class="sxs-lookup"><span data-stu-id="5ecba-121">Data type: **CIM\_SoftwareFeature**</span></span>
</dt> <dt>

<span data-ttu-id="5ecba-122">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="5ecba-122">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5ecba-123">限定詞： [**Min**](/windows/desktop/WmiSdk/standard-qualifiers) (0) ，覆 [**寫**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Antecedent" ) </span><span class="sxs-lookup"><span data-stu-id="5ecba-123">Qualifiers: [**Min**](/windows/desktop/WmiSdk/standard-qualifiers) (0), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent")</span></span>
</dt> </dl>

<span data-ttu-id="5ecba-124">描述之前的軟體功能的 [**CIM \_ SoftwareFeature**](cim-softwarefeature.md) 。</span><span class="sxs-lookup"><span data-stu-id="5ecba-124">A [**CIM\_SoftwareFeature**](cim-softwarefeature.md) that describes the antecedent software feature.</span></span>

</dd> <dt>

<span data-ttu-id="5ecba-125">**依賴**</span><span class="sxs-lookup"><span data-stu-id="5ecba-125">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5ecba-126">資料類型： **CIM \_ 服務**</span><span class="sxs-lookup"><span data-stu-id="5ecba-126">Data type: **CIM\_Service**</span></span>
</dt> <dt>

<span data-ttu-id="5ecba-127">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="5ecba-127">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5ecba-128">限定詞： [**Min**](/windows/desktop/WmiSdk/standard-qualifiers) (0) ，覆 [**寫**](/windows/desktop/WmiSdk/standard-qualifiers) ( 「相依」 ) </span><span class="sxs-lookup"><span data-stu-id="5ecba-128">Qualifiers: [**Min**](/windows/desktop/WmiSdk/standard-qualifiers) (0), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependent")</span></span>
</dt> </dl>

<span data-ttu-id="5ecba-129">描述相依服務的 [**CIM \_ 服務**](cim-service.md) 。</span><span class="sxs-lookup"><span data-stu-id="5ecba-129">A [**CIM\_Service**](cim-service.md) that describes the dependent service.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="5ecba-130">備註</span><span class="sxs-lookup"><span data-stu-id="5ecba-130">Remarks</span></span>

<span data-ttu-id="5ecba-131">**Cim \_ SoftwareFeatureServiceImplementation** 類別衍生自 cim 相依 [**性 \_**](cim-dependency.md)。</span><span class="sxs-lookup"><span data-stu-id="5ecba-131">The **CIM\_SoftwareFeatureServiceImplementation** class is derived from [**CIM\_Dependency**](cim-dependency.md).</span></span>

<span data-ttu-id="5ecba-132">WMI 不會執行這個類別。</span><span class="sxs-lookup"><span data-stu-id="5ecba-132">WMI does not implement this class.</span></span>

<span data-ttu-id="5ecba-133">此檔衍生自 DMTF 所發佈的 CIM 類別描述。</span><span class="sxs-lookup"><span data-stu-id="5ecba-133">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="5ecba-134">Microsoft 可能已進行變更，以更正次要錯誤、符合 Microsoft SDK 檔標準，或提供詳細資訊。</span><span class="sxs-lookup"><span data-stu-id="5ecba-134">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="5ecba-135">規格需求</span><span class="sxs-lookup"><span data-stu-id="5ecba-135">Requirements</span></span>



| <span data-ttu-id="5ecba-136">需求</span><span class="sxs-lookup"><span data-stu-id="5ecba-136">Requirement</span></span> | <span data-ttu-id="5ecba-137">值</span><span class="sxs-lookup"><span data-stu-id="5ecba-137">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="5ecba-138">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="5ecba-138">Minimum supported client</span></span><br/> | <span data-ttu-id="5ecba-139">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="5ecba-139">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="5ecba-140">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="5ecba-140">Minimum supported server</span></span><br/> | <span data-ttu-id="5ecba-141">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="5ecba-141">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="5ecba-142">命名空間</span><span class="sxs-lookup"><span data-stu-id="5ecba-142">Namespace</span></span><br/>                | <span data-ttu-id="5ecba-143">根 \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="5ecba-143">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="5ecba-144">MOF</span><span class="sxs-lookup"><span data-stu-id="5ecba-144">MOF</span></span><br/>                      | <dl> <span data-ttu-id="5ecba-145"><dt>CIMWin32 mof</dt></span><span class="sxs-lookup"><span data-stu-id="5ecba-145"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="5ecba-146">DLL</span><span class="sxs-lookup"><span data-stu-id="5ecba-146">DLL</span></span><br/>                      | <dl> <span data-ttu-id="5ecba-147"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5ecba-147"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5ecba-148">另請參閱</span><span class="sxs-lookup"><span data-stu-id="5ecba-148">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5ecba-149">**CIM \_ 相依性**</span><span class="sxs-lookup"><span data-stu-id="5ecba-149">**CIM\_Dependency**</span></span>](cim-dependency.md)
</dt> </dl>

 

