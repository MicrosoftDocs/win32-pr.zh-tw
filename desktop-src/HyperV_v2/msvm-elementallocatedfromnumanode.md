---
description: 將已配置資源的實例與從中配置的實體 NUMA 節點產生關聯。
ms.assetid: 811ed19f-9084-4e30-8604-860d2bf722c7
title: Msvm_ElementAllocatedFromNumaNode 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ElementAllocatedFromNumaNode
- Msvm_ElementAllocatedFromNumaNode.Antecedent
- Msvm_ElementAllocatedFromNumaNode.Dependent
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 98940306f25d46c6af1be31133ee336765f8f1a5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103850291"
---
# <a name="msvm_elementallocatedfromnumanode-class"></a><span data-ttu-id="91d3f-103">Msvm \_ ElementAllocatedFromNumaNode 類別</span><span class="sxs-lookup"><span data-stu-id="91d3f-103">Msvm\_ElementAllocatedFromNumaNode class</span></span>

<span data-ttu-id="91d3f-104">將已配置資源的實例與從中配置的實體 NUMA 節點產生關聯。</span><span class="sxs-lookup"><span data-stu-id="91d3f-104">Associates an instance of an allocated resource with the physical NUMA node from which it was allocated.</span></span>

<span data-ttu-id="91d3f-105">下列語法已簡化受控物件格式 (MOF) 程式碼，並且包含所有繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="91d3f-105">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="91d3f-106">語法</span><span class="sxs-lookup"><span data-stu-id="91d3f-106">Syntax</span></span>

``` syntax
[Association, Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_ElementAllocatedFromNumaNode : CIM_Dependency
{
  Msvm_NumaNode      REF Antecedent;
  CIM_LogicalElement REF Dependent;
};
```

## <a name="members"></a><span data-ttu-id="91d3f-107">成員</span><span class="sxs-lookup"><span data-stu-id="91d3f-107">Members</span></span>

<span data-ttu-id="91d3f-108">**Msvm \_ ElementAllocatedFromNumaNode** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="91d3f-108">The **Msvm\_ElementAllocatedFromNumaNode** class has these types of members:</span></span>

-   [<span data-ttu-id="91d3f-109">屬性</span><span class="sxs-lookup"><span data-stu-id="91d3f-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="91d3f-110">屬性</span><span class="sxs-lookup"><span data-stu-id="91d3f-110">Properties</span></span>

<span data-ttu-id="91d3f-111">**Msvm \_ ElementAllocatedFromNumaNode** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="91d3f-111">The **Msvm\_ElementAllocatedFromNumaNode** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="91d3f-112">**先行**</span><span class="sxs-lookup"><span data-stu-id="91d3f-112">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="91d3f-113">資料類型： **[ **Msvm \_ NumaNode**](msvm-numanode.md)**</span><span class="sxs-lookup"><span data-stu-id="91d3f-113">Data type: **[**Msvm\_NumaNode**](msvm-numanode.md)**</span></span>
</dt> <dt>

<span data-ttu-id="91d3f-114">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="91d3f-114">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="91d3f-115">限定詞：覆 [**寫**](/windows/desktop/WmiSdk/standard-qualifiers) ( 「Antecedent」 ) ， [**最大**](/windows/desktop/WmiSdk/standard-qualifiers) (1) </span><span class="sxs-lookup"><span data-stu-id="91d3f-115">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent"), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1)</span></span>
</dt> </dl>

<span data-ttu-id="91d3f-116">實體 NUMA 節點。</span><span class="sxs-lookup"><span data-stu-id="91d3f-116">The physical NUMA node.</span></span>

</dd> <dt>

<span data-ttu-id="91d3f-117">**依賴**</span><span class="sxs-lookup"><span data-stu-id="91d3f-117">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="91d3f-118">資料類型： **[ **CIM \_ LogicalElement**](/windows/desktop/CIMWin32Prov/cim-logicalelement)**</span><span class="sxs-lookup"><span data-stu-id="91d3f-118">Data type: **[**CIM\_LogicalElement**](/windows/desktop/CIMWin32Prov/cim-logicalelement)**</span></span>
</dt> <dt>

<span data-ttu-id="91d3f-119">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="91d3f-119">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="91d3f-120">限定詞：覆 [**寫**](/windows/desktop/WmiSdk/standard-qualifiers) ( 「相依」 ) </span><span class="sxs-lookup"><span data-stu-id="91d3f-120">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependent")</span></span>
</dt> </dl>

<span data-ttu-id="91d3f-121">配置的資源。</span><span class="sxs-lookup"><span data-stu-id="91d3f-121">The allocated resource.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="91d3f-122">規格需求</span><span class="sxs-lookup"><span data-stu-id="91d3f-122">Requirements</span></span>



| <span data-ttu-id="91d3f-123">需求</span><span class="sxs-lookup"><span data-stu-id="91d3f-123">Requirement</span></span> | <span data-ttu-id="91d3f-124">值</span><span class="sxs-lookup"><span data-stu-id="91d3f-124">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="91d3f-125">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="91d3f-125">Minimum supported client</span></span><br/> | <span data-ttu-id="91d3f-126">\[僅 Windows 8 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="91d3f-126">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="91d3f-127">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="91d3f-127">Minimum supported server</span></span><br/> | <span data-ttu-id="91d3f-128">僅限 Windows Server 2012 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="91d3f-128">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="91d3f-129">命名空間</span><span class="sxs-lookup"><span data-stu-id="91d3f-129">Namespace</span></span><br/>                | <span data-ttu-id="91d3f-130">根 \\ 虛擬化 \\ V2</span><span class="sxs-lookup"><span data-stu-id="91d3f-130">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="91d3f-131">MOF</span><span class="sxs-lookup"><span data-stu-id="91d3f-131">MOF</span></span><br/>                      | <dl> <span data-ttu-id="91d3f-132"><dt>WindowsVirtualization。</dt></span><span class="sxs-lookup"><span data-stu-id="91d3f-132"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="91d3f-133">DLL</span><span class="sxs-lookup"><span data-stu-id="91d3f-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="91d3f-134"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="91d3f-134"><dt>Vmms.exe</dt></span></span> </dl>                     |



 

