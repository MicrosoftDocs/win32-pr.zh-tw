---
description: CIM \_ DependencyCoNtext 關聯性會將 cim 相依性 \_ 類別與一個或多個 cim 設定物件產生關聯 \_ 。 例如，電腦系統的相依性可能會根據系統所連接的網路而變更。
ms.assetid: 9f35fc41-1bfa-4018-a54c-64c875c710d4
ms.tgt_platform: multiple
title: CIM_DependencyCoNtext 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_DependencyContext
- CIM_DependencyContext.Context
- CIM_DependencyContext.Dependency
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 69319a4f4d228d484da62411060ae3fead90bb79
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103847367"
---
# <a name="cim_dependencycontext-class"></a><span data-ttu-id="48e7b-104">CIM \_ DependencyCoNtext 類別</span><span class="sxs-lookup"><span data-stu-id="48e7b-104">CIM\_DependencyContext class</span></span>

<span data-ttu-id="48e7b-105">**Cim \_ DependencyCoNtext** 關聯性會將 [**cim \_**](cim-dependency.md)相依性類別與一個或多個 [**cim \_ 設定物件**](cim-configuration.md)產生關聯。</span><span class="sxs-lookup"><span data-stu-id="48e7b-105">The **CIM\_DependencyContext** relationship associates a [**CIM\_Dependency**](cim-dependency.md) class with one or more [**CIM\_Configuration**](cim-configuration.md) objects.</span></span> <span data-ttu-id="48e7b-106">例如，電腦系統的相依性可能會根據系統所連接的網路而變更。</span><span class="sxs-lookup"><span data-stu-id="48e7b-106">For example, a computer system's dependencies can change based on the network to which the system is attached.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="48e7b-107">DMTF (分散式管理工作強制) CIM (通用訊息模型) 類別是用來建立 WMI 類別的父類別。</span><span class="sxs-lookup"><span data-stu-id="48e7b-107">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="48e7b-108">WMI 目前僅支援 [CIM 2.x 版的架構](https://dmtf.org/standards/cim/schemas)。</span><span class="sxs-lookup"><span data-stu-id="48e7b-108">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="48e7b-109">下列語法已從受管理物件格式 (MOF) 程式碼加以簡化，並包含所有繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="48e7b-109">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="48e7b-110">屬性會依字母順序列出，而不是依 MOF 順序列出。</span><span class="sxs-lookup"><span data-stu-id="48e7b-110">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="48e7b-111">語法</span><span class="sxs-lookup"><span data-stu-id="48e7b-111">Syntax</span></span>

``` syntax
[Abstract, Aggregation, Association, UUID("{A228E208-DB22-11d2-85FC-0000F8102E5F}"), AMENDMENT]
class CIM_DependencyContext
{
  CIM_Configuration REF Context;
  CIM_Dependency    REF Dependency;
};
```

## <a name="members"></a><span data-ttu-id="48e7b-112">成員</span><span class="sxs-lookup"><span data-stu-id="48e7b-112">Members</span></span>

<span data-ttu-id="48e7b-113">**CIM \_ DependencyCoNtext** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="48e7b-113">The **CIM\_DependencyContext** class has these types of members:</span></span>

-   [<span data-ttu-id="48e7b-114">屬性</span><span class="sxs-lookup"><span data-stu-id="48e7b-114">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="48e7b-115">屬性</span><span class="sxs-lookup"><span data-stu-id="48e7b-115">Properties</span></span>

<span data-ttu-id="48e7b-116">**CIM \_ DependencyCoNtext** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="48e7b-116">The **CIM\_DependencyContext** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="48e7b-117">**內容**</span><span class="sxs-lookup"><span data-stu-id="48e7b-117">**Context**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="48e7b-118">資料類型： **CIM \_** 設定</span><span class="sxs-lookup"><span data-stu-id="48e7b-118">Data type: **CIM\_Configuration**</span></span>
</dt> <dt>

<span data-ttu-id="48e7b-119">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="48e7b-119">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="48e7b-120">限定詞： [**匯總**](/windows/desktop/WmiSdk/standard-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="48e7b-120">Qualifiers: [**Aggregate**](/windows/desktop/WmiSdk/standard-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="48e7b-121">參考匯總相依性的設定物件。</span><span class="sxs-lookup"><span data-stu-id="48e7b-121">Reference to the configuration object that aggregates the dependency.</span></span>

</dd> <dt>

<span data-ttu-id="48e7b-122">**相依性**</span><span class="sxs-lookup"><span data-stu-id="48e7b-122">**Dependency**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="48e7b-123">資料類型： **CIM \_** 相依性</span><span class="sxs-lookup"><span data-stu-id="48e7b-123">Data type: **CIM\_Dependency**</span></span>
</dt> <dt>

<span data-ttu-id="48e7b-124">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="48e7b-124">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="48e7b-125">匯總相依性的參考。</span><span class="sxs-lookup"><span data-stu-id="48e7b-125">Reference to an aggregated dependency.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="48e7b-126">備註</span><span class="sxs-lookup"><span data-stu-id="48e7b-126">Remarks</span></span>

<span data-ttu-id="48e7b-127">WMI 不會執行這個類別。</span><span class="sxs-lookup"><span data-stu-id="48e7b-127">WMI does not implement this class.</span></span>

<span data-ttu-id="48e7b-128">此檔衍生自 DMTF 所發佈的 CIM 類別描述。</span><span class="sxs-lookup"><span data-stu-id="48e7b-128">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="48e7b-129">Microsoft 可能已進行變更，以更正次要錯誤、符合 Microsoft SDK 檔標準，或提供詳細資訊。</span><span class="sxs-lookup"><span data-stu-id="48e7b-129">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="48e7b-130">規格需求</span><span class="sxs-lookup"><span data-stu-id="48e7b-130">Requirements</span></span>



| <span data-ttu-id="48e7b-131">需求</span><span class="sxs-lookup"><span data-stu-id="48e7b-131">Requirement</span></span> | <span data-ttu-id="48e7b-132">值</span><span class="sxs-lookup"><span data-stu-id="48e7b-132">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="48e7b-133">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="48e7b-133">Minimum supported client</span></span><br/> | <span data-ttu-id="48e7b-134">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="48e7b-134">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="48e7b-135">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="48e7b-135">Minimum supported server</span></span><br/> | <span data-ttu-id="48e7b-136">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="48e7b-136">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="48e7b-137">命名空間</span><span class="sxs-lookup"><span data-stu-id="48e7b-137">Namespace</span></span><br/>                | <span data-ttu-id="48e7b-138">根 \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="48e7b-138">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="48e7b-139">MOF</span><span class="sxs-lookup"><span data-stu-id="48e7b-139">MOF</span></span><br/>                      | <dl> <span data-ttu-id="48e7b-140"><dt>CIMWin32 mof</dt></span><span class="sxs-lookup"><span data-stu-id="48e7b-140"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="48e7b-141">DLL</span><span class="sxs-lookup"><span data-stu-id="48e7b-141">DLL</span></span><br/>                      | <dl> <span data-ttu-id="48e7b-142"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="48e7b-142"><dt>CIMWin32.dll</dt></span></span> </dl> |



 

