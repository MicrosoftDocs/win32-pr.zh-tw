---
description: CIM \_ AllocatedResource 類別代表邏輯裝置與系統資源之間的關聯，並指出資源已指派給裝置。
ms.assetid: e1702635-32f5-4280-8c02-3940fd858106
ms.tgt_platform: multiple
title: CIM_AllocatedResource 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_AllocatedResource
- CIM_AllocatedResource.Dependent
- CIM_AllocatedResource.Antecedent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: e4191315b76553a8c23b94c04d9649cceb131855
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104111101"
---
# <a name="cim_allocatedresource-class"></a><span data-ttu-id="81201-103">CIM \_ AllocatedResource 類別</span><span class="sxs-lookup"><span data-stu-id="81201-103">CIM\_AllocatedResource class</span></span>

<span data-ttu-id="81201-104">**CIM \_ AllocatedResource** 類別代表邏輯裝置與系統資源之間的關聯，並指出資源已指派給裝置。</span><span class="sxs-lookup"><span data-stu-id="81201-104">The **CIM\_AllocatedResource** class represents an association between logical devices and system resources and indicates that the resource is assigned to the device.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="81201-105">DMTF (分散式管理工作強制) CIM (通用訊息模型) 類別是用來建立 WMI 類別的父類別。</span><span class="sxs-lookup"><span data-stu-id="81201-105">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="81201-106">WMI 目前僅支援 [CIM 2.x 版的架構](https://dmtf.org/standards/cim/schemas)。</span><span class="sxs-lookup"><span data-stu-id="81201-106">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="81201-107">下列語法是簡化自 MOF 程式碼，且包含所有繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="81201-107">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="81201-108">語法</span><span class="sxs-lookup"><span data-stu-id="81201-108">Syntax</span></span>

``` syntax
[Abstract, UUID("{8502C579-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class CIM_AllocatedResource : CIM_Dependency
{
  CIM_LogicalDevice  REF Dependent;
  CIM_SystemResource REF Antecedent;
};
```

## <a name="members"></a><span data-ttu-id="81201-109">成員</span><span class="sxs-lookup"><span data-stu-id="81201-109">Members</span></span>

<span data-ttu-id="81201-110">**CIM \_ AllocatedResource** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="81201-110">The **CIM\_AllocatedResource** class has these types of members:</span></span>

-   [<span data-ttu-id="81201-111">屬性</span><span class="sxs-lookup"><span data-stu-id="81201-111">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="81201-112">屬性</span><span class="sxs-lookup"><span data-stu-id="81201-112">Properties</span></span>

<span data-ttu-id="81201-113">**CIM \_ AllocatedResource** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="81201-113">The **CIM\_AllocatedResource** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="81201-114">**先行**</span><span class="sxs-lookup"><span data-stu-id="81201-114">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="81201-115">資料類型： **CIM \_ SystemResource**</span><span class="sxs-lookup"><span data-stu-id="81201-115">Data type: **CIM\_SystemResource**</span></span>
</dt> <dt>

<span data-ttu-id="81201-116">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="81201-116">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="81201-117">限定詞：覆 [**寫**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Antecedent" ) </span><span class="sxs-lookup"><span data-stu-id="81201-117">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent")</span></span>
</dt> </dl>

<span data-ttu-id="81201-118">描述資源的 [**CIM \_ SystemResource**](cim-systemresource.md) 。</span><span class="sxs-lookup"><span data-stu-id="81201-118">A [**CIM\_SystemResource**](cim-systemresource.md) that describes the resource.</span></span>

</dd> <dt>

<span data-ttu-id="81201-119">**依賴**</span><span class="sxs-lookup"><span data-stu-id="81201-119">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="81201-120">資料類型： **CIM \_ LogicalDevice**</span><span class="sxs-lookup"><span data-stu-id="81201-120">Data type: **CIM\_LogicalDevice**</span></span>
</dt> <dt>

<span data-ttu-id="81201-121">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="81201-121">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="81201-122">限定詞：覆 [**寫**](/windows/desktop/WmiSdk/standard-qualifiers) ( 「相依」 ) </span><span class="sxs-lookup"><span data-stu-id="81201-122">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependent")</span></span>
</dt> </dl>

<span data-ttu-id="81201-123">[**CIM \_ LogicalDevice**](cim-logicaldevice.md) ，其中包含指派給資源的邏輯裝置。</span><span class="sxs-lookup"><span data-stu-id="81201-123">A [**CIM\_LogicalDevice**](cim-logicaldevice.md) that contains the logical device to which the resource is assigned.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="81201-124">備註</span><span class="sxs-lookup"><span data-stu-id="81201-124">Remarks</span></span>

<span data-ttu-id="81201-125">**Cim \_ AllocatedResource** 類別衍生自 cim 相依 [**性 \_**](cim-dependency.md)。</span><span class="sxs-lookup"><span data-stu-id="81201-125">The **CIM\_AllocatedResource** class is derived from [**CIM\_Dependency**](cim-dependency.md).</span></span>

<span data-ttu-id="81201-126">WMI 不會執行這個類別。</span><span class="sxs-lookup"><span data-stu-id="81201-126">WMI does not implement this class.</span></span> <span data-ttu-id="81201-127">如需衍生自 **CIM \_ AllocatedResource** 之類別的詳細資訊，請參閱 [Win32 類別](win32-provider.md)。</span><span class="sxs-lookup"><span data-stu-id="81201-127">For more information about classes derived from **CIM\_AllocatedResource**, see [Win32 Classes](win32-provider.md).</span></span>

<span data-ttu-id="81201-128">此檔衍生自 DMTF 所發佈的 CIM 類別描述。</span><span class="sxs-lookup"><span data-stu-id="81201-128">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="81201-129">Microsoft 可能已進行變更，以更正次要錯誤、符合 Microsoft SDK 檔標準，或提供詳細資訊。</span><span class="sxs-lookup"><span data-stu-id="81201-129">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="81201-130">規格需求</span><span class="sxs-lookup"><span data-stu-id="81201-130">Requirements</span></span>



| <span data-ttu-id="81201-131">需求</span><span class="sxs-lookup"><span data-stu-id="81201-131">Requirement</span></span> | <span data-ttu-id="81201-132">值</span><span class="sxs-lookup"><span data-stu-id="81201-132">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="81201-133">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="81201-133">Minimum supported client</span></span><br/> | <span data-ttu-id="81201-134">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="81201-134">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="81201-135">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="81201-135">Minimum supported server</span></span><br/> | <span data-ttu-id="81201-136">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="81201-136">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="81201-137">命名空間</span><span class="sxs-lookup"><span data-stu-id="81201-137">Namespace</span></span><br/>                | <span data-ttu-id="81201-138">根 \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="81201-138">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="81201-139">MOF</span><span class="sxs-lookup"><span data-stu-id="81201-139">MOF</span></span><br/>                      | <dl> <span data-ttu-id="81201-140"><dt>CIMWin32 mof</dt></span><span class="sxs-lookup"><span data-stu-id="81201-140"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="81201-141">DLL</span><span class="sxs-lookup"><span data-stu-id="81201-141">DLL</span></span><br/>                      | <dl> <span data-ttu-id="81201-142"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="81201-142"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="81201-143">另請參閱</span><span class="sxs-lookup"><span data-stu-id="81201-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="81201-144">**CIM \_ 相依性**</span><span class="sxs-lookup"><span data-stu-id="81201-144">**CIM\_Dependency**</span></span>](cim-dependency.md)
</dt> </dl>

 

