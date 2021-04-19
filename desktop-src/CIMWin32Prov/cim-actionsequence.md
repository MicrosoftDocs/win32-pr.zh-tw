---
description: CIM \_ ActionSequence 關聯會定義一系列的作業，這些作業會將 CIM SoftwareElementActions) 關聯 (所參考的軟體專案轉換 \_ 為下一個狀態，或從其目前的狀態中移除軟體元素。
ms.assetid: b539c424-bc2a-414b-b56c-72550004720f
ms.tgt_platform: multiple
title: CIM_ActionSequence 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_ActionSequence
- CIM_ActionSequence.Next
- CIM_ActionSequence.Prior
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 71150d1ad9785d81579d8f305fe46bc6b7e57d00
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106986255"
---
# <a name="cim_actionsequence-class"></a><span data-ttu-id="9b8d4-103">CIM \_ ActionSequence 類別</span><span class="sxs-lookup"><span data-stu-id="9b8d4-103">CIM\_ActionSequence class</span></span>

<span data-ttu-id="9b8d4-104">**Cim \_ ActionSequence** 關聯會定義一系列的作業，這些作業會將 [**CIM \_ SoftwareElementActions**](cim-softwareelementactions.md)) 關聯 (所參考的軟體專案轉換為下一個狀態，或從其目前的狀態中移除軟體元素。</span><span class="sxs-lookup"><span data-stu-id="9b8d4-104">The **CIM\_ActionSequence** association defines a series of operations that transition the software element (referenced by the [**CIM\_SoftwareElementActions**](cim-softwareelementactions.md) association) to its next state, or removes the software element from its current state.</span></span>

<span data-ttu-id="9b8d4-105">與特定軟體元素相關聯的下一個狀態動作和卸載動作必須是連續順序。</span><span class="sxs-lookup"><span data-stu-id="9b8d4-105">The next-state actions and uninstall actions associated with a particular software element must be a continuous sequence.</span></span> <span data-ttu-id="9b8d4-106">因為 **cim \_ ActionSequence** 是關聯，所以 [**cim \_ 動作**](cim-action.md) 類別上的迴圈會以「先前」動作和「下一個」動作的角色形成序列。</span><span class="sxs-lookup"><span data-stu-id="9b8d4-106">Since **CIM\_ActionSequence** is an association, the loops on the [**CIM\_Action**](cim-action.md) class, with roles for the "prior" action and "next" action, form a sequence.</span></span>

<span data-ttu-id="9b8d4-107">連續順序的需求表示：</span><span class="sxs-lookup"><span data-stu-id="9b8d4-107">The need for a continuous sequence implies:</span></span>

-   <span data-ttu-id="9b8d4-108">在下一組狀態或卸載動作中，只有一個動作沒有 **CIM \_ ActionSequence** 關聯的實例在「下一個」角色中參考它。</span><span class="sxs-lookup"><span data-stu-id="9b8d4-108">Within the set of next-state or uninstall actions, there is only one action that does not have an instance of the **CIM\_ActionSequence** association referencing it in the "next" role.</span></span> <span data-ttu-id="9b8d4-109">這是序列中的第一個動作。</span><span class="sxs-lookup"><span data-stu-id="9b8d4-109">This is the first action in the sequence.</span></span>
-   <span data-ttu-id="9b8d4-110">在下一組狀態或卸載動作中，只有一個動作沒有 **CIM \_ ActionSequence** 關聯的實例，其會在「先前」角色中參考它。</span><span class="sxs-lookup"><span data-stu-id="9b8d4-110">Within the set of next-state or uninstall actions, there is only one action that does not have an instance of the **CIM\_ActionSequence** association referencing it in the "prior" role.</span></span> <span data-ttu-id="9b8d4-111">這是序列中的最後一個動作。</span><span class="sxs-lookup"><span data-stu-id="9b8d4-111">This is the last action in the sequence.</span></span>
-   <span data-ttu-id="9b8d4-112">下一組狀態和卸載動作集合內的所有其他動作都必須參與 **CIM \_ ActionSequence** 關聯的兩個實例，一個是「先前」角色，另一個則是「下一個」角色。</span><span class="sxs-lookup"><span data-stu-id="9b8d4-112">All other actions within the set of next-state and uninstall actions must participate in two instances of the **CIM\_ActionSequence** association, one in a "prior" role and one in the "next" role.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="9b8d4-113">DMTF (分散式管理工作強制) CIM (通用訊息模型) 類別是用來建立 WMI 類別的父類別。</span><span class="sxs-lookup"><span data-stu-id="9b8d4-113">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="9b8d4-114">WMI 目前僅支援 [CIM 2.x 版的架構](https://dmtf.org/standards/cim/schemas)。</span><span class="sxs-lookup"><span data-stu-id="9b8d4-114">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="9b8d4-115">下列語法已從受管理物件格式 (MOF) 程式碼加以簡化，並包含所有繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="9b8d4-115">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="9b8d4-116">屬性會依字母順序列出，而不是依 MOF 順序列出。</span><span class="sxs-lookup"><span data-stu-id="9b8d4-116">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="9b8d4-117">語法</span><span class="sxs-lookup"><span data-stu-id="9b8d4-117">Syntax</span></span>

``` syntax
[Abstract, Association, UUID("{F127E50E-E3E0-11d2-8601-0000F8102E5F}"), AMENDMENT]
class CIM_ActionSequence
{
  CIM_Action REF Next;
  CIM_Action REF Prior;
};
```

## <a name="members"></a><span data-ttu-id="9b8d4-118">成員</span><span class="sxs-lookup"><span data-stu-id="9b8d4-118">Members</span></span>

<span data-ttu-id="9b8d4-119">**CIM \_ ActionSequence** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="9b8d4-119">The **CIM\_ActionSequence** class has these types of members:</span></span>

-   [<span data-ttu-id="9b8d4-120">屬性</span><span class="sxs-lookup"><span data-stu-id="9b8d4-120">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="9b8d4-121">屬性</span><span class="sxs-lookup"><span data-stu-id="9b8d4-121">Properties</span></span>

<span data-ttu-id="9b8d4-122">**CIM \_ ActionSequence** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="9b8d4-122">The **CIM\_ActionSequence** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="9b8d4-123">**下一步**</span><span class="sxs-lookup"><span data-stu-id="9b8d4-123">**Next**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9b8d4-124">資料類型： **CIM \_ 動作**</span><span class="sxs-lookup"><span data-stu-id="9b8d4-124">Data type: **CIM\_Action**</span></span>
</dt> <dt>

<span data-ttu-id="9b8d4-125">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="9b8d4-125">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9b8d4-126">限定詞： [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1) ， [**Min**](/windows/desktop/WmiSdk/standard-qualifiers) (0) </span><span class="sxs-lookup"><span data-stu-id="9b8d4-126">Qualifiers: [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**Min**](/windows/desktop/WmiSdk/standard-qualifiers) (0)</span></span>
</dt> </dl>

<span data-ttu-id="9b8d4-127">下一個動作的參考。</span><span class="sxs-lookup"><span data-stu-id="9b8d4-127">Reference to the next action.</span></span>

</dd> <dt>

<span data-ttu-id="9b8d4-128">**之前**</span><span class="sxs-lookup"><span data-stu-id="9b8d4-128">**Prior**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9b8d4-129">資料類型： **CIM \_ 動作**</span><span class="sxs-lookup"><span data-stu-id="9b8d4-129">Data type: **CIM\_Action**</span></span>
</dt> <dt>

<span data-ttu-id="9b8d4-130">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="9b8d4-130">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9b8d4-131">限定詞： [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1) ， [**Min**](/windows/desktop/WmiSdk/standard-qualifiers) (0) </span><span class="sxs-lookup"><span data-stu-id="9b8d4-131">Qualifiers: [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**Min**](/windows/desktop/WmiSdk/standard-qualifiers) (0)</span></span>
</dt> </dl>

<span data-ttu-id="9b8d4-132">先前動作的參考。</span><span class="sxs-lookup"><span data-stu-id="9b8d4-132">Reference to the prior action.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="9b8d4-133">備註</span><span class="sxs-lookup"><span data-stu-id="9b8d4-133">Remarks</span></span>

<span data-ttu-id="9b8d4-134">參與此關聯的 [**CIM \_ 動作**](cim-action.md) 類別必須具有與 **Direction** 屬性相同的值。</span><span class="sxs-lookup"><span data-stu-id="9b8d4-134">The [**CIM\_Action**](cim-action.md) classes participating in this association must have the same value for the **Direction** property.</span></span>

<span data-ttu-id="9b8d4-135">WMI 不會執行這個類別。</span><span class="sxs-lookup"><span data-stu-id="9b8d4-135">WMI does not implement this class.</span></span>

<span data-ttu-id="9b8d4-136">此檔衍生自 DMTF 所發佈的 CIM 類別描述。</span><span class="sxs-lookup"><span data-stu-id="9b8d4-136">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="9b8d4-137">Microsoft 可能已進行變更，以更正次要錯誤、符合 Microsoft SDK 檔標準，或提供詳細資訊。</span><span class="sxs-lookup"><span data-stu-id="9b8d4-137">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="9b8d4-138">規格需求</span><span class="sxs-lookup"><span data-stu-id="9b8d4-138">Requirements</span></span>



| <span data-ttu-id="9b8d4-139">需求</span><span class="sxs-lookup"><span data-stu-id="9b8d4-139">Requirement</span></span> | <span data-ttu-id="9b8d4-140">值</span><span class="sxs-lookup"><span data-stu-id="9b8d4-140">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="9b8d4-141">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="9b8d4-141">Minimum supported client</span></span><br/> | <span data-ttu-id="9b8d4-142">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="9b8d4-142">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="9b8d4-143">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="9b8d4-143">Minimum supported server</span></span><br/> | <span data-ttu-id="9b8d4-144">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="9b8d4-144">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="9b8d4-145">命名空間</span><span class="sxs-lookup"><span data-stu-id="9b8d4-145">Namespace</span></span><br/>                | <span data-ttu-id="9b8d4-146">根 \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="9b8d4-146">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="9b8d4-147">MOF</span><span class="sxs-lookup"><span data-stu-id="9b8d4-147">MOF</span></span><br/>                      | <dl> <span data-ttu-id="9b8d4-148"><dt>CIMWin32 mof</dt></span><span class="sxs-lookup"><span data-stu-id="9b8d4-148"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="9b8d4-149">DLL</span><span class="sxs-lookup"><span data-stu-id="9b8d4-149">DLL</span></span><br/>                      | <dl> <span data-ttu-id="9b8d4-150"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9b8d4-150"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9b8d4-151">另請參閱</span><span class="sxs-lookup"><span data-stu-id="9b8d4-151">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9b8d4-152">CIM 類別</span><span class="sxs-lookup"><span data-stu-id="9b8d4-152">CIM Classes</span></span>](/windows/desktop/WmiSdk/cimclas)
</dt> </dl>

 

