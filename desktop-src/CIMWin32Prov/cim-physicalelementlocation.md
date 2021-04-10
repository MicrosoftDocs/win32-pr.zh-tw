---
description: CIM \_ PhysicalElementLocation 類別會將實體元素與 CIM \_ 位置物件產生關聯，以供清查或取代之用。
ms.assetid: d1698c1a-0eda-4e32-9a29-fb741b987671
ms.tgt_platform: multiple
title: CIM_PhysicalElementLocation 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_PhysicalElementLocation
- CIM_PhysicalElementLocation.Element
- CIM_PhysicalElementLocation.PhysicalLocation
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 5e47460a3563d9b7a86aa6ee65704fcb0a422c39
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104111268"
---
# <a name="cim_physicalelementlocation-class"></a><span data-ttu-id="b6e57-103">CIM \_ PhysicalElementLocation 類別</span><span class="sxs-lookup"><span data-stu-id="b6e57-103">CIM\_PhysicalElementLocation class</span></span>

<span data-ttu-id="b6e57-104">**Cim \_ PhysicalElementLocation** 類別會將實體元素與 [**CIM \_ 位置**](cim-location.md)物件產生關聯，以供清查或取代之用。</span><span class="sxs-lookup"><span data-stu-id="b6e57-104">The **CIM\_PhysicalElementLocation** class associates a physical element with a [**CIM\_Location**](cim-location.md) object for inventory or replacement purposes.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="b6e57-105">DMTF (分散式管理工作強制) CIM (通用訊息模型) 類別是用來建立 WMI 類別的父類別。</span><span class="sxs-lookup"><span data-stu-id="b6e57-105">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="b6e57-106">WMI 目前僅支援 [CIM 2.x 版的架構](https://dmtf.org/standards/cim/schemas)。</span><span class="sxs-lookup"><span data-stu-id="b6e57-106">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="b6e57-107">下列語法已從受控物件格式的 (MOF) 程式碼簡化，並包含其所有繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="b6e57-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of its inherited properties.</span></span> <span data-ttu-id="b6e57-108">屬性會依字母順序列出，而不是依 MOF 順序列出。</span><span class="sxs-lookup"><span data-stu-id="b6e57-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="b6e57-109">語法</span><span class="sxs-lookup"><span data-stu-id="b6e57-109">Syntax</span></span>

``` syntax
[Abstract, Association, UUID("{FAF76B68-798C-11D2-AAD1-006008C78BC7}"), AMENDMENT]
class CIM_PhysicalElementLocation
{
  CIM_PhysicalElement REF Element;
  CIM_Location        REF PhysicalLocation;
};
```

## <a name="members"></a><span data-ttu-id="b6e57-110">成員</span><span class="sxs-lookup"><span data-stu-id="b6e57-110">Members</span></span>

<span data-ttu-id="b6e57-111">**CIM \_ PhysicalElementLocation** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="b6e57-111">The **CIM\_PhysicalElementLocation** class has these types of members:</span></span>

-   [<span data-ttu-id="b6e57-112">屬性</span><span class="sxs-lookup"><span data-stu-id="b6e57-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="b6e57-113">屬性</span><span class="sxs-lookup"><span data-stu-id="b6e57-113">Properties</span></span>

<span data-ttu-id="b6e57-114">**CIM \_ PhysicalElementLocation** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="b6e57-114">The **CIM\_PhysicalElementLocation** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="b6e57-115">**Element**</span><span class="sxs-lookup"><span data-stu-id="b6e57-115">**Element**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b6e57-116">資料類型： **CIM \_ PhysicalElement**</span><span class="sxs-lookup"><span data-stu-id="b6e57-116">Data type: **CIM\_PhysicalElement**</span></span>
</dt> <dt>

<span data-ttu-id="b6e57-117">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="b6e57-117">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b6e57-118">指定位置之實體元素的參考。</span><span class="sxs-lookup"><span data-stu-id="b6e57-118">Reference to the physical element whose location is specified.</span></span>

</dd> <dt>

<span data-ttu-id="b6e57-119">**PhysicalLocation**</span><span class="sxs-lookup"><span data-stu-id="b6e57-119">**PhysicalLocation**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b6e57-120">資料類型： **CIM \_ 位置**</span><span class="sxs-lookup"><span data-stu-id="b6e57-120">Data type: **CIM\_Location**</span></span>
</dt> <dt>

<span data-ttu-id="b6e57-121">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="b6e57-121">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b6e57-122">限定詞： [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1) </span><span class="sxs-lookup"><span data-stu-id="b6e57-122">Qualifiers: [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1)</span></span>
</dt> </dl>

<span data-ttu-id="b6e57-123">實體元素位置的參考。</span><span class="sxs-lookup"><span data-stu-id="b6e57-123">Reference to the physical element's location.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="b6e57-124">備註</span><span class="sxs-lookup"><span data-stu-id="b6e57-124">Remarks</span></span>

<span data-ttu-id="b6e57-125">WMI 不會執行這個類別。</span><span class="sxs-lookup"><span data-stu-id="b6e57-125">WMI does not implement this class.</span></span>

<span data-ttu-id="b6e57-126">此檔衍生自 DMTF 所發佈的 CIM 類別描述。</span><span class="sxs-lookup"><span data-stu-id="b6e57-126">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="b6e57-127">Microsoft 可能已進行變更，以更正次要錯誤、符合 Microsoft SDK 檔標準，或提供詳細資訊。</span><span class="sxs-lookup"><span data-stu-id="b6e57-127">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="b6e57-128">規格需求</span><span class="sxs-lookup"><span data-stu-id="b6e57-128">Requirements</span></span>



| <span data-ttu-id="b6e57-129">需求</span><span class="sxs-lookup"><span data-stu-id="b6e57-129">Requirement</span></span> | <span data-ttu-id="b6e57-130">值</span><span class="sxs-lookup"><span data-stu-id="b6e57-130">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="b6e57-131">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="b6e57-131">Minimum supported client</span></span><br/> | <span data-ttu-id="b6e57-132">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="b6e57-132">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="b6e57-133">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="b6e57-133">Minimum supported server</span></span><br/> | <span data-ttu-id="b6e57-134">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="b6e57-134">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="b6e57-135">命名空間</span><span class="sxs-lookup"><span data-stu-id="b6e57-135">Namespace</span></span><br/>                | <span data-ttu-id="b6e57-136">根 \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="b6e57-136">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="b6e57-137">MOF</span><span class="sxs-lookup"><span data-stu-id="b6e57-137">MOF</span></span><br/>                      | <dl> <span data-ttu-id="b6e57-138"><dt>CIMWin32 mof</dt></span><span class="sxs-lookup"><span data-stu-id="b6e57-138"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="b6e57-139">DLL</span><span class="sxs-lookup"><span data-stu-id="b6e57-139">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b6e57-140"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b6e57-140"><dt>CIMWin32.dll</dt></span></span> </dl> |



 

