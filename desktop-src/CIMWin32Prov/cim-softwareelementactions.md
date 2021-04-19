---
description: CIM \_ SoftwareElementActions 關聯會識別 software 元素的動作。
ms.assetid: 2f8a584c-dff0-48f8-bc5f-2b833b5c0b18
ms.tgt_platform: multiple
title: CIM_SoftwareElementActions 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_SoftwareElementActions
- CIM_SoftwareElementActions.Action
- CIM_SoftwareElementActions.Element
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 1f51cc122cdf354be9611ca1cca4ebcbe1635d14
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106972331"
---
# <a name="cim_softwareelementactions-class"></a><span data-ttu-id="628db-103">CIM \_ SoftwareElementActions 類別</span><span class="sxs-lookup"><span data-stu-id="628db-103">CIM\_SoftwareElementActions class</span></span>

<span data-ttu-id="628db-104">**CIM \_ SoftwareElementActions** 關聯會識別 software 元素的動作。</span><span class="sxs-lookup"><span data-stu-id="628db-104">The **CIM\_SoftwareElementActions** association identifies the actions for a software element.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="628db-105">DMTF (分散式管理工作強制) CIM (通用訊息模型) 類別是用來建立 WMI 類別的父類別。</span><span class="sxs-lookup"><span data-stu-id="628db-105">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="628db-106">WMI 目前僅支援 [CIM 2.x 版的架構](https://dmtf.org/standards/cim/schemas)。</span><span class="sxs-lookup"><span data-stu-id="628db-106">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="628db-107">下列語法已從受控物件格式的 (MOF) 程式碼簡化，並包含其所有繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="628db-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of its inherited properties.</span></span> <span data-ttu-id="628db-108">屬性會依字母順序列出，而不是依 MOF 順序列出。</span><span class="sxs-lookup"><span data-stu-id="628db-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="628db-109">語法</span><span class="sxs-lookup"><span data-stu-id="628db-109">Syntax</span></span>

``` syntax
[UUID("{4B82D255-E3CD-11d2-8601-0000F8102E5F}"), Association, Aggregation, Abstract, AMENDMENT]
class CIM_SoftwareElementActions
{
  CIM_Action          REF Action;
  CIM_SoftwareElement REF Element;
};
```

## <a name="members"></a><span data-ttu-id="628db-110">成員</span><span class="sxs-lookup"><span data-stu-id="628db-110">Members</span></span>

<span data-ttu-id="628db-111">**CIM \_ SoftwareElementActions** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="628db-111">The **CIM\_SoftwareElementActions** class has these types of members:</span></span>

-   [<span data-ttu-id="628db-112">屬性</span><span class="sxs-lookup"><span data-stu-id="628db-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="628db-113">屬性</span><span class="sxs-lookup"><span data-stu-id="628db-113">Properties</span></span>

<span data-ttu-id="628db-114">**CIM \_ SoftwareElementActions** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="628db-114">The **CIM\_SoftwareElementActions** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="628db-115">**動作**</span><span class="sxs-lookup"><span data-stu-id="628db-115">**Action**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="628db-116">資料類型： **CIM \_ 動作**</span><span class="sxs-lookup"><span data-stu-id="628db-116">Data type: **CIM\_Action**</span></span>
</dt> <dt>

<span data-ttu-id="628db-117">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="628db-117">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="628db-118">限定詞： [**Min**](/windows/desktop/WmiSdk/standard-qualifiers) (0) 、 [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (FALSE) 、[**弱**](/windows/desktop/WmiSdk/standard-qualifiers)式</span><span class="sxs-lookup"><span data-stu-id="628db-118">Qualifiers: [**Min**](/windows/desktop/WmiSdk/standard-qualifiers) (0), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (FALSE), [**Weak**](/windows/desktop/WmiSdk/standard-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="628db-119">[**CIM \_ 動作**](cim-action.md)實例的參考。</span><span class="sxs-lookup"><span data-stu-id="628db-119">Reference to a [**CIM\_Action**](cim-action.md) instance.</span></span>

</dd> <dt>

<span data-ttu-id="628db-120">**Element**</span><span class="sxs-lookup"><span data-stu-id="628db-120">**Element**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="628db-121">資料類型： **CIM \_ SoftwareElement**</span><span class="sxs-lookup"><span data-stu-id="628db-121">Data type: **CIM\_SoftwareElement**</span></span>
</dt> <dt>

<span data-ttu-id="628db-122">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="628db-122">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="628db-123">限定詞： [**Min**](/windows/desktop/WmiSdk/standard-qualifiers) (1) 、 [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1) 、 [**Aggregate**](/windows/desktop/WmiSdk/standard-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="628db-123">Qualifiers: [**Min**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**Aggregate**](/windows/desktop/WmiSdk/standard-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="628db-124">[**CIM \_ SoftwareElement**](cim-softwareelement.md)實例的參考。</span><span class="sxs-lookup"><span data-stu-id="628db-124">Reference to a [**CIM\_SoftwareElement**](cim-softwareelement.md) instance.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="628db-125">備註</span><span class="sxs-lookup"><span data-stu-id="628db-125">Remarks</span></span>

<span data-ttu-id="628db-126">WMI 不會執行這個類別。</span><span class="sxs-lookup"><span data-stu-id="628db-126">WMI does not implement this class.</span></span> <span data-ttu-id="628db-127">針對衍生自 **CIM \_ SOFTWAREELEMENTACTIONS** 的 WMI 類別，請參閱 [Win32 類別](win32-provider.md)。</span><span class="sxs-lookup"><span data-stu-id="628db-127">For WMI classes derived from **CIM\_SoftwareElementActions**, see [Win32 Classes](win32-provider.md).</span></span>

<span data-ttu-id="628db-128">此檔衍生自 DMTF 所發佈的 CIM 類別描述。</span><span class="sxs-lookup"><span data-stu-id="628db-128">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="628db-129">Microsoft 可能已進行變更，以更正次要錯誤、符合 Microsoft SDK 檔標準，或提供詳細資訊。</span><span class="sxs-lookup"><span data-stu-id="628db-129">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="628db-130">規格需求</span><span class="sxs-lookup"><span data-stu-id="628db-130">Requirements</span></span>



| <span data-ttu-id="628db-131">需求</span><span class="sxs-lookup"><span data-stu-id="628db-131">Requirement</span></span> | <span data-ttu-id="628db-132">值</span><span class="sxs-lookup"><span data-stu-id="628db-132">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="628db-133">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="628db-133">Minimum supported client</span></span><br/> | <span data-ttu-id="628db-134">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="628db-134">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="628db-135">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="628db-135">Minimum supported server</span></span><br/> | <span data-ttu-id="628db-136">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="628db-136">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="628db-137">命名空間</span><span class="sxs-lookup"><span data-stu-id="628db-137">Namespace</span></span><br/>                | <span data-ttu-id="628db-138">根 \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="628db-138">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="628db-139">MOF</span><span class="sxs-lookup"><span data-stu-id="628db-139">MOF</span></span><br/>                      | <dl> <span data-ttu-id="628db-140"><dt>CIMWin32 mof</dt></span><span class="sxs-lookup"><span data-stu-id="628db-140"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="628db-141">DLL</span><span class="sxs-lookup"><span data-stu-id="628db-141">DLL</span></span><br/>                      | <dl> <span data-ttu-id="628db-142"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="628db-142"><dt>CIMWin32.dll</dt></span></span> </dl> |



 

