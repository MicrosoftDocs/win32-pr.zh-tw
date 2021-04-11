---
description: CIM AssociatedBattery 相依性會將 \_ 電池與邏輯裝置產生關聯。 您可以使用此關聯來建立個別電池的模型，使其成為 (UPS) 的不斷電供應系統供應。
ms.assetid: f8d8b3d3-edc5-438a-8be6-3ea4d765085b
ms.tgt_platform: multiple
title: CIM_AssociatedBattery 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_AssociatedBattery
- CIM_AssociatedBattery.Dependent
- CIM_AssociatedBattery.Antecedent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 98c6394df79e53698ab6394f8572768f3728c503
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104190977"
---
# <a name="cim_associatedbattery-class"></a><span data-ttu-id="c8248-104">CIM \_ AssociatedBattery 類別</span><span class="sxs-lookup"><span data-stu-id="c8248-104">CIM\_AssociatedBattery class</span></span>

<span data-ttu-id="c8248-105">**CIM \_ AssociatedBattery** 相依性會將電池與邏輯裝置產生關聯。</span><span class="sxs-lookup"><span data-stu-id="c8248-105">The **CIM\_AssociatedBattery** dependency associates a battery with a logical device.</span></span> <span data-ttu-id="c8248-106">您可以使用此關聯來建立個別電池的模型，使其成為 (UPS) 的不斷電供應系統供應。</span><span class="sxs-lookup"><span data-stu-id="c8248-106">Use this association to model individual batteries that make up an uninterruptible power supply (UPS).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="c8248-107">DMTF (分散式管理工作強制) CIM (通用訊息模型) 類別是用來建立 WMI 類別的父類別。</span><span class="sxs-lookup"><span data-stu-id="c8248-107">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="c8248-108">WMI 目前僅支援 [CIM 2.x 版的架構](https://dmtf.org/standards/cim/schemas)。</span><span class="sxs-lookup"><span data-stu-id="c8248-108">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="c8248-109">下列語法已從受管理物件格式 (MOF) 程式碼加以簡化，並包含所有繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="c8248-109">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="c8248-110">屬性會依字母順序列出，而不是依 MOF 順序列出。</span><span class="sxs-lookup"><span data-stu-id="c8248-110">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="c8248-111">語法</span><span class="sxs-lookup"><span data-stu-id="c8248-111">Syntax</span></span>

``` syntax
[Abstract, UUID("{8502C578-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class CIM_AssociatedBattery : CIM_Dependency
{
  CIM_LogicalDevice REF Dependent;
  CIM_Battery       REF Antecedent;
};
```

## <a name="members"></a><span data-ttu-id="c8248-112">成員</span><span class="sxs-lookup"><span data-stu-id="c8248-112">Members</span></span>

<span data-ttu-id="c8248-113">**CIM \_ AssociatedBattery** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="c8248-113">The **CIM\_AssociatedBattery** class has these types of members:</span></span>

-   [<span data-ttu-id="c8248-114">屬性</span><span class="sxs-lookup"><span data-stu-id="c8248-114">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="c8248-115">屬性</span><span class="sxs-lookup"><span data-stu-id="c8248-115">Properties</span></span>

<span data-ttu-id="c8248-116">**CIM \_ AssociatedBattery** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="c8248-116">The **CIM\_AssociatedBattery** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="c8248-117">**先行**</span><span class="sxs-lookup"><span data-stu-id="c8248-117">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c8248-118">資料類型： **CIM \_ 電池**</span><span class="sxs-lookup"><span data-stu-id="c8248-118">Data type: **CIM\_Battery**</span></span>
</dt> <dt>

<span data-ttu-id="c8248-119">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="c8248-119">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c8248-120">限定詞：覆 [**寫**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Antecedent" ) </span><span class="sxs-lookup"><span data-stu-id="c8248-120">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent")</span></span>
</dt> </dl>

<span data-ttu-id="c8248-121">描述電池的 [**CIM \_ 電池**](cim-battery.md) 。</span><span class="sxs-lookup"><span data-stu-id="c8248-121">A [**CIM\_Battery**](cim-battery.md) that describes the battery.</span></span>

</dd> <dt>

<span data-ttu-id="c8248-122">**依賴**</span><span class="sxs-lookup"><span data-stu-id="c8248-122">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c8248-123">資料類型： **CIM \_ LogicalDevice**</span><span class="sxs-lookup"><span data-stu-id="c8248-123">Data type: **CIM\_LogicalDevice**</span></span>
</dt> <dt>

<span data-ttu-id="c8248-124">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="c8248-124">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c8248-125">限定詞：覆 [**寫**](/windows/desktop/WmiSdk/standard-qualifiers) ( 「相依」 ) </span><span class="sxs-lookup"><span data-stu-id="c8248-125">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependent")</span></span>
</dt> </dl>

<span data-ttu-id="c8248-126">[**CIM \_ LogicalDevice**](cim-logicaldevice.md) ，其中包含需要或與電池相關聯的邏輯裝置。</span><span class="sxs-lookup"><span data-stu-id="c8248-126">A [**CIM\_LogicalDevice**](cim-logicaldevice.md) that contains the logical device needing or associated with the battery.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="c8248-127">備註</span><span class="sxs-lookup"><span data-stu-id="c8248-127">Remarks</span></span>

<span data-ttu-id="c8248-128">**Cim \_ AssociatedBattery** 類別衍生自 cim 相依 [**性 \_**](cim-dependency.md)。</span><span class="sxs-lookup"><span data-stu-id="c8248-128">The **CIM\_AssociatedBattery** class is derived from [**CIM\_Dependency**](cim-dependency.md).</span></span>

<span data-ttu-id="c8248-129">WMI 不會執行這個類別。</span><span class="sxs-lookup"><span data-stu-id="c8248-129">WMI does not implement this class.</span></span> <span data-ttu-id="c8248-130">如需衍生自 **CIM \_ AssociatedBattery** 之類別的詳細資訊，請參閱 [Win32 類別](win32-provider.md)。</span><span class="sxs-lookup"><span data-stu-id="c8248-130">For more information about classes derived from **CIM\_AssociatedBattery**, see [Win32 Classes](win32-provider.md).</span></span>

<span data-ttu-id="c8248-131">此檔衍生自 DMTF 所發佈的 CIM 類別描述。</span><span class="sxs-lookup"><span data-stu-id="c8248-131">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="c8248-132">Microsoft 可能已進行變更，以更正次要錯誤、符合 Microsoft SDK 檔標準，或提供詳細資訊。</span><span class="sxs-lookup"><span data-stu-id="c8248-132">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="c8248-133">規格需求</span><span class="sxs-lookup"><span data-stu-id="c8248-133">Requirements</span></span>



| <span data-ttu-id="c8248-134">需求</span><span class="sxs-lookup"><span data-stu-id="c8248-134">Requirement</span></span> | <span data-ttu-id="c8248-135">值</span><span class="sxs-lookup"><span data-stu-id="c8248-135">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="c8248-136">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="c8248-136">Minimum supported client</span></span><br/> | <span data-ttu-id="c8248-137">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="c8248-137">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="c8248-138">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="c8248-138">Minimum supported server</span></span><br/> | <span data-ttu-id="c8248-139">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="c8248-139">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="c8248-140">命名空間</span><span class="sxs-lookup"><span data-stu-id="c8248-140">Namespace</span></span><br/>                | <span data-ttu-id="c8248-141">根 \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="c8248-141">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="c8248-142">MOF</span><span class="sxs-lookup"><span data-stu-id="c8248-142">MOF</span></span><br/>                      | <dl> <span data-ttu-id="c8248-143"><dt>CIMWin32 mof</dt></span><span class="sxs-lookup"><span data-stu-id="c8248-143"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="c8248-144">DLL</span><span class="sxs-lookup"><span data-stu-id="c8248-144">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c8248-145"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c8248-145"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c8248-146">另請參閱</span><span class="sxs-lookup"><span data-stu-id="c8248-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c8248-147">**CIM \_ 相依性**</span><span class="sxs-lookup"><span data-stu-id="c8248-147">**CIM\_Dependency**</span></span>](cim-dependency.md)
</dt> </dl>

 

