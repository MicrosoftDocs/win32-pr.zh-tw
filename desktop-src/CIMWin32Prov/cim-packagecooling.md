---
description: CIM \_ PackageCooling 關聯代表在套件中安裝冷卻裝置的關聯性（例如底座或機架），以協助封裝的冷卻。
ms.assetid: 0aaae8e1-6e70-4b26-8e56-dac5657e58c1
ms.tgt_platform: multiple
title: CIM_PackageCooling 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_PackageCooling
- CIM_PackageCooling.Dependent
- CIM_PackageCooling.Antecedent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 1f88cd3f07983870bed8fd2d740f3bf9051019b4
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104510596"
---
# <a name="cim_packagecooling-class"></a><span data-ttu-id="2e12b-103">CIM \_ PackageCooling 類別</span><span class="sxs-lookup"><span data-stu-id="2e12b-103">CIM\_PackageCooling class</span></span>

<span data-ttu-id="2e12b-104">**CIM \_ PackageCooling** 關聯代表在套件中安裝冷卻裝置的關聯性（例如底座或機架），以協助封裝的冷卻。</span><span class="sxs-lookup"><span data-stu-id="2e12b-104">The **CIM\_PackageCooling** association represents the relationship in which a cooling device is installed in a package, such as a chassis or rack, to assist with the package's cooling.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="2e12b-105">DMTF (分散式管理工作強制) CIM (通用訊息模型) 類別是用來建立 WMI 類別的父類別。</span><span class="sxs-lookup"><span data-stu-id="2e12b-105">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="2e12b-106">WMI 目前僅支援 [CIM 2.x 版的架構](https://dmtf.org/standards/cim/schemas)。</span><span class="sxs-lookup"><span data-stu-id="2e12b-106">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="2e12b-107">下列語法已從受管理物件格式 (MOF) 程式碼加以簡化，並包含所有繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="2e12b-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="2e12b-108">屬性會依字母順序列出，而不是依 MOF 順序列出。</span><span class="sxs-lookup"><span data-stu-id="2e12b-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="2e12b-109">語法</span><span class="sxs-lookup"><span data-stu-id="2e12b-109">Syntax</span></span>

``` syntax
[Abstract, UUID("{FAF76B8E-798C-11D2-AAD1-006008C78BC7}"), AMENDMENT]
class CIM_PackageCooling : CIM_Dependency
{
  CIM_PhysicalPackage REF Dependent;
  CIM_CoolingDevice   REF Antecedent;
};
```

## <a name="members"></a><span data-ttu-id="2e12b-110">成員</span><span class="sxs-lookup"><span data-stu-id="2e12b-110">Members</span></span>

<span data-ttu-id="2e12b-111">**CIM \_ PackageCooling** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="2e12b-111">The **CIM\_PackageCooling** class has these types of members:</span></span>

-   [<span data-ttu-id="2e12b-112">屬性</span><span class="sxs-lookup"><span data-stu-id="2e12b-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="2e12b-113">屬性</span><span class="sxs-lookup"><span data-stu-id="2e12b-113">Properties</span></span>

<span data-ttu-id="2e12b-114">**CIM \_ PackageCooling** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="2e12b-114">The **CIM\_PackageCooling** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="2e12b-115">**先行**</span><span class="sxs-lookup"><span data-stu-id="2e12b-115">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2e12b-116">資料類型： **CIM \_ CoolingDevice**</span><span class="sxs-lookup"><span data-stu-id="2e12b-116">Data type: **CIM\_CoolingDevice**</span></span>
</dt> <dt>

<span data-ttu-id="2e12b-117">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="2e12b-117">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2e12b-118">限定詞：覆 [**寫**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Antecedent" ) </span><span class="sxs-lookup"><span data-stu-id="2e12b-118">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent")</span></span>
</dt> </dl>

<span data-ttu-id="2e12b-119">描述套件冷卻裝置的 [**CIM \_ CoolingDevice**](cim-coolingdevice.md) 。</span><span class="sxs-lookup"><span data-stu-id="2e12b-119">A [**CIM\_CoolingDevice**](cim-coolingdevice.md) that describes the cooling device for the package.</span></span>

</dd> <dt>

<span data-ttu-id="2e12b-120">**依賴**</span><span class="sxs-lookup"><span data-stu-id="2e12b-120">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2e12b-121">資料類型： **CIM \_ PhysicalPackage**</span><span class="sxs-lookup"><span data-stu-id="2e12b-121">Data type: **CIM\_PhysicalPackage**</span></span>
</dt> <dt>

<span data-ttu-id="2e12b-122">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="2e12b-122">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2e12b-123">限定詞：覆 [**寫**](/windows/desktop/WmiSdk/standard-qualifiers) ( 「相依」 ) </span><span class="sxs-lookup"><span data-stu-id="2e12b-123">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependent")</span></span>
</dt> </dl>

<span data-ttu-id="2e12b-124">[**CIM \_ PhysicalPackage**](cim-physicalpackage.md) ，描述其環境已冷卻的實體套件。</span><span class="sxs-lookup"><span data-stu-id="2e12b-124">A [**CIM\_PhysicalPackage**](cim-physicalpackage.md) that describes the physical package whose environment is cooled.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="2e12b-125">備註</span><span class="sxs-lookup"><span data-stu-id="2e12b-125">Remarks</span></span>

<span data-ttu-id="2e12b-126">**CIM \_PackageCooling** 衍生自 [**CIM 相依 \_**](cim-dependency.md)性。</span><span class="sxs-lookup"><span data-stu-id="2e12b-126">**CIM\_PackageCooling** is derived from [**CIM\_Dependency**](cim-dependency.md).</span></span>

<span data-ttu-id="2e12b-127">WMI 不會執行這個類別。</span><span class="sxs-lookup"><span data-stu-id="2e12b-127">WMI does not implement this class.</span></span>

<span data-ttu-id="2e12b-128">此檔衍生自 DMTF 所發佈的 CIM 類別描述。</span><span class="sxs-lookup"><span data-stu-id="2e12b-128">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="2e12b-129">Microsoft 可能已進行變更，以更正次要錯誤、符合 Microsoft SDK 檔標準，或提供詳細資訊。</span><span class="sxs-lookup"><span data-stu-id="2e12b-129">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="2e12b-130">規格需求</span><span class="sxs-lookup"><span data-stu-id="2e12b-130">Requirements</span></span>



| <span data-ttu-id="2e12b-131">需求</span><span class="sxs-lookup"><span data-stu-id="2e12b-131">Requirement</span></span> | <span data-ttu-id="2e12b-132">值</span><span class="sxs-lookup"><span data-stu-id="2e12b-132">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="2e12b-133">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="2e12b-133">Minimum supported client</span></span><br/> | <span data-ttu-id="2e12b-134">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="2e12b-134">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="2e12b-135">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="2e12b-135">Minimum supported server</span></span><br/> | <span data-ttu-id="2e12b-136">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="2e12b-136">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="2e12b-137">命名空間</span><span class="sxs-lookup"><span data-stu-id="2e12b-137">Namespace</span></span><br/>                | <span data-ttu-id="2e12b-138">根 \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="2e12b-138">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="2e12b-139">MOF</span><span class="sxs-lookup"><span data-stu-id="2e12b-139">MOF</span></span><br/>                      | <dl> <span data-ttu-id="2e12b-140"><dt>CIMWin32 mof</dt></span><span class="sxs-lookup"><span data-stu-id="2e12b-140"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="2e12b-141">DLL</span><span class="sxs-lookup"><span data-stu-id="2e12b-141">DLL</span></span><br/>                      | <dl> <span data-ttu-id="2e12b-142"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="2e12b-142"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2e12b-143">另請參閱</span><span class="sxs-lookup"><span data-stu-id="2e12b-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2e12b-144">**CIM \_ 相依性**</span><span class="sxs-lookup"><span data-stu-id="2e12b-144">**CIM\_Dependency**</span></span>](cim-dependency.md)
</dt> </dl>

 

