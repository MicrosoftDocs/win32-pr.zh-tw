---
description: CIM \_ SoftwareElementChecks 關聯類別會將 software 元素與功能可能需要的條件或位置資訊產生關聯。
ms.assetid: ff130fe9-ddb2-4e4f-86d3-53f1d8ed14aa
ms.tgt_platform: multiple
title: CIM_SoftwareElementChecks 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_SoftwareElementChecks
- CIM_SoftwareElementChecks.Check
- CIM_SoftwareElementChecks.Element
- CIM_SoftwareElementChecks.Phase
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: ea6fcb02794174e825994f70270745741c9b7713
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103847152"
---
# <a name="cim_softwareelementchecks-class"></a><span data-ttu-id="975f2-103">CIM \_ SoftwareElementChecks 類別</span><span class="sxs-lookup"><span data-stu-id="975f2-103">CIM\_SoftwareElementChecks class</span></span>

<span data-ttu-id="975f2-104">**CIM \_ SoftwareElementChecks** 關聯類別會將 software 元素與功能可能需要的條件或位置資訊產生關聯。</span><span class="sxs-lookup"><span data-stu-id="975f2-104">The **CIM\_SoftwareElementChecks** association class relates a software element with condition or location information that a feature may require.</span></span>

<span data-ttu-id="975f2-105">因為處於已就緒狀態的軟體專案無法轉換成另一個狀態，所以 **階段** 屬性的值會限制為處於隨時可用狀態的 [**CIM \_ SoftwareElement**](cim-softwareelement.md) 物件狀態。</span><span class="sxs-lookup"><span data-stu-id="975f2-105">Because software elements in a ready-to-run state cannot transition into another state, the value of the **Phase** property is restricted to in-state for [**CIM\_SoftwareElement**](cim-softwareelement.md) objects in a ready-to-run state.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="975f2-106">DMTF (分散式管理工作強制) CIM (通用訊息模型) 類別是用來建立 WMI 類別的父類別。</span><span class="sxs-lookup"><span data-stu-id="975f2-106">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="975f2-107">WMI 目前僅支援 [CIM 2.x 版的架構](https://dmtf.org/standards/cim/schemas)。</span><span class="sxs-lookup"><span data-stu-id="975f2-107">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="975f2-108">下列語法已從受控物件格式的 (MOF) 程式碼簡化，並包含其所有繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="975f2-108">The following syntax is simplified from Managed Object Format (MOF) code and includes all of its inherited properties.</span></span> <span data-ttu-id="975f2-109">屬性會依字母順序列出，而不是依 MOF 順序列出。</span><span class="sxs-lookup"><span data-stu-id="975f2-109">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="975f2-110">語法</span><span class="sxs-lookup"><span data-stu-id="975f2-110">Syntax</span></span>

``` syntax
[UUID("{24783E8A-DB31-11d2-85FC-0000F8102E5F}"), Association, Aggregation, Abstract, AMENDMENT]
class CIM_SoftwareElementChecks
{
  CIM_Check           REF Check;
  CIM_SoftwareElement REF Element;
  uint16                  Phase;
};
```

## <a name="members"></a><span data-ttu-id="975f2-111">成員</span><span class="sxs-lookup"><span data-stu-id="975f2-111">Members</span></span>

<span data-ttu-id="975f2-112">**CIM \_ SoftwareElementChecks** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="975f2-112">The **CIM\_SoftwareElementChecks** class has these types of members:</span></span>

-   [<span data-ttu-id="975f2-113">屬性</span><span class="sxs-lookup"><span data-stu-id="975f2-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="975f2-114">屬性</span><span class="sxs-lookup"><span data-stu-id="975f2-114">Properties</span></span>

<span data-ttu-id="975f2-115">**CIM \_ SoftwareElementChecks** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="975f2-115">The **CIM\_SoftwareElementChecks** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="975f2-116">**檢查**</span><span class="sxs-lookup"><span data-stu-id="975f2-116">**Check**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="975f2-117">資料類型： **CIM \_ 檢查**</span><span class="sxs-lookup"><span data-stu-id="975f2-117">Data type: **CIM\_Check**</span></span>
</dt> <dt>

<span data-ttu-id="975f2-118">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="975f2-118">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="975f2-119">限定詞： [**Min**](/windows/desktop/WmiSdk/standard-qualifiers) (0) 、 [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (FALSE) 、[**弱**](/windows/desktop/WmiSdk/standard-qualifiers)式</span><span class="sxs-lookup"><span data-stu-id="975f2-119">Qualifiers: [**Min**](/windows/desktop/WmiSdk/standard-qualifiers) (0), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (FALSE), [**Weak**](/windows/desktop/WmiSdk/standard-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="975f2-120">檢查的參考。</span><span class="sxs-lookup"><span data-stu-id="975f2-120">Reference to the check.</span></span>

</dd> <dt>

<span data-ttu-id="975f2-121">**Element**</span><span class="sxs-lookup"><span data-stu-id="975f2-121">**Element**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="975f2-122">資料類型： **CIM \_ SoftwareElement**</span><span class="sxs-lookup"><span data-stu-id="975f2-122">Data type: **CIM\_SoftwareElement**</span></span>
</dt> <dt>

<span data-ttu-id="975f2-123">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="975f2-123">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="975f2-124">限定詞： [**Min**](/windows/desktop/WmiSdk/standard-qualifiers) (1) 、 [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1) 、 [**Aggregate**](/windows/desktop/WmiSdk/standard-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="975f2-124">Qualifiers: [**Min**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**Aggregate**](/windows/desktop/WmiSdk/standard-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="975f2-125">元素的參考。</span><span class="sxs-lookup"><span data-stu-id="975f2-125">Reference to the element.</span></span>

</dd> <dt>

<span data-ttu-id="975f2-126">**階段**</span><span class="sxs-lookup"><span data-stu-id="975f2-126">**Phase**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="975f2-127">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="975f2-127">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="975f2-128">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="975f2-128">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="975f2-129">指出參考的檢查是否為狀態檢查或下一次狀態檢查。</span><span class="sxs-lookup"><span data-stu-id="975f2-129">Indicates whether the referenced check is an in-state check or a next-state check.</span></span>

<dt>

<span id="In-State"></span><span id="in-state"></span><span id="IN-STATE"></span>

<span data-ttu-id="975f2-130">**狀態** (0) </span><span class="sxs-lookup"><span data-stu-id="975f2-130">**In-State** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Next-State"></span><span id="next-state"></span><span id="NEXT-STATE"></span>

<span data-ttu-id="975f2-131">**下一步-狀態** (1) </span><span class="sxs-lookup"><span data-stu-id="975f2-131">**Next-State** (1)</span></span>


<span data-ttu-id="975f2-132"></dt> <dd></dd> </dl>

</dd> </dl></span><span class="sxs-lookup"><span data-stu-id="975f2-132"></dt> <dd></dd> </dl>

</dd> </dl></span></span>

## <a name="remarks"></a><span data-ttu-id="975f2-133">備註</span><span class="sxs-lookup"><span data-stu-id="975f2-133">Remarks</span></span>

<span data-ttu-id="975f2-134">WMI 不會執行這個類別。</span><span class="sxs-lookup"><span data-stu-id="975f2-134">WMI does not implement this class.</span></span> <span data-ttu-id="975f2-135">針對衍生自 **CIM \_ SOFTWAREELEMENTCHECKS** 的 WMI 類別，請參閱 [Win32 類別](win32-provider.md)。</span><span class="sxs-lookup"><span data-stu-id="975f2-135">For WMI classes derived from **CIM\_SoftwareElementChecks**, see [Win32 Classes](win32-provider.md).</span></span>

<span data-ttu-id="975f2-136">此檔衍生自 DMTF 所發佈的 CIM 類別描述。</span><span class="sxs-lookup"><span data-stu-id="975f2-136">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="975f2-137">Microsoft 可能已進行變更，以更正次要錯誤、符合 Microsoft SDK 檔標準，或提供詳細資訊。</span><span class="sxs-lookup"><span data-stu-id="975f2-137">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="975f2-138">規格需求</span><span class="sxs-lookup"><span data-stu-id="975f2-138">Requirements</span></span>



| <span data-ttu-id="975f2-139">需求</span><span class="sxs-lookup"><span data-stu-id="975f2-139">Requirement</span></span> | <span data-ttu-id="975f2-140">值</span><span class="sxs-lookup"><span data-stu-id="975f2-140">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="975f2-141">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="975f2-141">Minimum supported client</span></span><br/> | <span data-ttu-id="975f2-142">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="975f2-142">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="975f2-143">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="975f2-143">Minimum supported server</span></span><br/> | <span data-ttu-id="975f2-144">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="975f2-144">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="975f2-145">命名空間</span><span class="sxs-lookup"><span data-stu-id="975f2-145">Namespace</span></span><br/>                | <span data-ttu-id="975f2-146">根 \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="975f2-146">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="975f2-147">MOF</span><span class="sxs-lookup"><span data-stu-id="975f2-147">MOF</span></span><br/>                      | <dl> <span data-ttu-id="975f2-148"><dt>CIMWin32 mof</dt></span><span class="sxs-lookup"><span data-stu-id="975f2-148"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="975f2-149">DLL</span><span class="sxs-lookup"><span data-stu-id="975f2-149">DLL</span></span><br/>                      | <dl> <span data-ttu-id="975f2-150"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="975f2-150"><dt>CIMWin32.dll</dt></span></span> </dl> |



 

