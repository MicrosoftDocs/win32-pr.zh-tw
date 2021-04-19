---
description: CIM \_ SoftwareFeatureSoftwareElements 關聯會識別組成特定軟體功能的軟體元素。
ms.assetid: 933586c5-b85e-4136-b557-5151a48abc32
ms.tgt_platform: multiple
title: CIM_SoftwareFeatureSoftwareElements 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_SoftwareFeatureSoftwareElements
- CIM_SoftwareFeatureSoftwareElements.PartComponent
- CIM_SoftwareFeatureSoftwareElements.GroupComponent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 71712ebb3f8bf2ab2067325f16cf31af7fb1dc38
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106967032"
---
# <a name="cim_softwarefeaturesoftwareelements-class"></a><span data-ttu-id="4a044-103">CIM \_ SoftwareFeatureSoftwareElements 類別</span><span class="sxs-lookup"><span data-stu-id="4a044-103">CIM\_SoftwareFeatureSoftwareElements class</span></span>

<span data-ttu-id="4a044-104">**CIM \_ SoftwareFeatureSoftwareElements** 關聯會識別組成特定軟體功能的軟體元素。</span><span class="sxs-lookup"><span data-stu-id="4a044-104">The **CIM\_SoftwareFeatureSoftwareElements** association identifies the software elements that make up a specific software feature.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="4a044-105">DMTF (分散式管理工作強制) CIM (通用訊息模型) 類別是用來建立 WMI 類別的父類別。</span><span class="sxs-lookup"><span data-stu-id="4a044-105">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="4a044-106">WMI 目前僅支援 [CIM 2.x 版的架構](https://dmtf.org/standards/cim/schemas)。</span><span class="sxs-lookup"><span data-stu-id="4a044-106">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="4a044-107">下列語法已從受控物件格式的 (MOF) 程式碼簡化，並包含其所有繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="4a044-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of its inherited properties.</span></span> <span data-ttu-id="4a044-108">屬性會依字母順序列出，而不是依 MOF 順序列出。</span><span class="sxs-lookup"><span data-stu-id="4a044-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="4a044-109">語法</span><span class="sxs-lookup"><span data-stu-id="4a044-109">Syntax</span></span>

``` syntax
[UUID("{A91081E2-DB37-11d2-85FC-0000F8102E5F}"), Abstract, AMENDMENT]
class CIM_SoftwareFeatureSoftwareElements : CIM_Component
{
  CIM_SoftwareElement REF PartComponent;
  CIM_SoftwareFeature REF GroupComponent;
};
```

## <a name="members"></a><span data-ttu-id="4a044-110">成員</span><span class="sxs-lookup"><span data-stu-id="4a044-110">Members</span></span>

<span data-ttu-id="4a044-111">**CIM \_ SoftwareFeatureSoftwareElements** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="4a044-111">The **CIM\_SoftwareFeatureSoftwareElements** class has these types of members:</span></span>

-   [<span data-ttu-id="4a044-112">屬性</span><span class="sxs-lookup"><span data-stu-id="4a044-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="4a044-113">屬性</span><span class="sxs-lookup"><span data-stu-id="4a044-113">Properties</span></span>

<span data-ttu-id="4a044-114">**CIM \_ SoftwareFeatureSoftwareElements** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="4a044-114">The **CIM\_SoftwareFeatureSoftwareElements** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="4a044-115">**GroupComponent**</span><span class="sxs-lookup"><span data-stu-id="4a044-115">**GroupComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4a044-116">資料類型： **CIM \_ SoftwareFeature**</span><span class="sxs-lookup"><span data-stu-id="4a044-116">Data type: **CIM\_SoftwareFeature**</span></span>
</dt> <dt>

<span data-ttu-id="4a044-117">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="4a044-117">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4a044-118">限定詞： [**匯總**](/windows/desktop/WmiSdk/standard-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="4a044-118">Qualifiers: [**Aggregate**](/windows/desktop/WmiSdk/standard-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="4a044-119">群組元件。</span><span class="sxs-lookup"><span data-stu-id="4a044-119">The group component.</span></span>

<span data-ttu-id="4a044-120">這個屬性繼承自 [**CIM \_ 元件**](cim-component.md)。</span><span class="sxs-lookup"><span data-stu-id="4a044-120">This property is inherited from [**CIM\_Component**](cim-component.md).</span></span>

</dd> <dt>

<span data-ttu-id="4a044-121">**PartComponent**</span><span class="sxs-lookup"><span data-stu-id="4a044-121">**PartComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4a044-122">資料類型： **CIM \_ SoftwareElement**</span><span class="sxs-lookup"><span data-stu-id="4a044-122">Data type: **CIM\_SoftwareElement**</span></span>
</dt> <dt>

<span data-ttu-id="4a044-123">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="4a044-123">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4a044-124">元件元件。</span><span class="sxs-lookup"><span data-stu-id="4a044-124">The part component.</span></span>

<span data-ttu-id="4a044-125">這個屬性繼承自 [**CIM \_ 元件**](cim-component.md)。</span><span class="sxs-lookup"><span data-stu-id="4a044-125">This property is inherited from [**CIM\_Component**](cim-component.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="4a044-126">備註</span><span class="sxs-lookup"><span data-stu-id="4a044-126">Remarks</span></span>

<span data-ttu-id="4a044-127">**Cim \_ SoftwareFeatureSoftwareElements** 關聯衍生自 [**cim \_ 元件**](cim-component.md)。</span><span class="sxs-lookup"><span data-stu-id="4a044-127">The **CIM\_SoftwareFeatureSoftwareElements** association is derived from [**CIM\_Component**](cim-component.md).</span></span>

<span data-ttu-id="4a044-128">WMI 不會執行這個類別。</span><span class="sxs-lookup"><span data-stu-id="4a044-128">WMI does not implement this class.</span></span> <span data-ttu-id="4a044-129">針對衍生自 **CIM \_ SOFTWAREFEATURESOFTWAREELEMENTS** 的 WMI 類別，請參閱 [Win32 類別](win32-provider.md)。</span><span class="sxs-lookup"><span data-stu-id="4a044-129">For WMI classes derived from **CIM\_SoftwareFeatureSoftwareElements**, see [Win32 Classes](win32-provider.md).</span></span>

<span data-ttu-id="4a044-130">此檔衍生自 DMTF 所發佈的 CIM 類別描述。</span><span class="sxs-lookup"><span data-stu-id="4a044-130">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="4a044-131">Microsoft 可能已進行變更，以更正次要錯誤、符合 Microsoft SDK 檔標準，或提供詳細資訊。</span><span class="sxs-lookup"><span data-stu-id="4a044-131">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="4a044-132">規格需求</span><span class="sxs-lookup"><span data-stu-id="4a044-132">Requirements</span></span>



| <span data-ttu-id="4a044-133">需求</span><span class="sxs-lookup"><span data-stu-id="4a044-133">Requirement</span></span> | <span data-ttu-id="4a044-134">值</span><span class="sxs-lookup"><span data-stu-id="4a044-134">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="4a044-135">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="4a044-135">Minimum supported client</span></span><br/> | <span data-ttu-id="4a044-136">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="4a044-136">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="4a044-137">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="4a044-137">Minimum supported server</span></span><br/> | <span data-ttu-id="4a044-138">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="4a044-138">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="4a044-139">命名空間</span><span class="sxs-lookup"><span data-stu-id="4a044-139">Namespace</span></span><br/>                | <span data-ttu-id="4a044-140">根 \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="4a044-140">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="4a044-141">MOF</span><span class="sxs-lookup"><span data-stu-id="4a044-141">MOF</span></span><br/>                      | <dl> <span data-ttu-id="4a044-142"><dt>CIMWin32 mof</dt></span><span class="sxs-lookup"><span data-stu-id="4a044-142"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="4a044-143">DLL</span><span class="sxs-lookup"><span data-stu-id="4a044-143">DLL</span></span><br/>                      | <dl> <span data-ttu-id="4a044-144"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="4a044-144"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4a044-145">另請參閱</span><span class="sxs-lookup"><span data-stu-id="4a044-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4a044-146">**CIM \_ 元件**</span><span class="sxs-lookup"><span data-stu-id="4a044-146">**CIM\_Component**</span></span>](cim-component.md)
</dt> </dl>

 

