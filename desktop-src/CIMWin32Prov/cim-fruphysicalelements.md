---
description: CIM \_ FRUPhysicalElements 類別代表組成現場可更換單元 (FRU) 的實體元素。
ms.assetid: ecdb19a8-5169-4370-8d2d-a21a0021ea5b
ms.tgt_platform: multiple
title: CIM_FRUPhysicalElements 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_FRUPhysicalElements
- CIM_FRUPhysicalElements.Component
- CIM_FRUPhysicalElements.FRU
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 5c47160b9053a323f693d76f5b84d922c5120992
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103936312"
---
# <a name="cim_fruphysicalelements-class"></a><span data-ttu-id="202c7-103">CIM \_ FRUPhysicalElements 類別</span><span class="sxs-lookup"><span data-stu-id="202c7-103">CIM\_FRUPhysicalElements class</span></span>

<span data-ttu-id="202c7-104">**CIM \_ FRUPhysicalElements** 類別代表組成現場可更換單元 (FRU) 的實體元素。</span><span class="sxs-lookup"><span data-stu-id="202c7-104">The **CIM\_FRUPhysicalElements** class represents the physical elements that make up a field replaceable unit (FRU).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="202c7-105">DMTF (分散式管理工作強制) CIM (通用訊息模型) 類別是用來建立 WMI 類別的父類別。</span><span class="sxs-lookup"><span data-stu-id="202c7-105">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="202c7-106">WMI 目前僅支援 [CIM 2.x 版的架構](https://dmtf.org/standards/cim/schemas)。</span><span class="sxs-lookup"><span data-stu-id="202c7-106">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="202c7-107">下列語法已從受管理物件格式 (MOF) 程式碼加以簡化，並包含所有繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="202c7-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="202c7-108">屬性會依字母順序列出，而不是依 MOF 順序列出。</span><span class="sxs-lookup"><span data-stu-id="202c7-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="202c7-109">語法</span><span class="sxs-lookup"><span data-stu-id="202c7-109">Syntax</span></span>

``` syntax
[Abstract, UUID("{977E36CA-DB2A-11d2-85FC-0000F8102E5F}"), Aggregation, Association, AMENDMENT]
class CIM_FRUPhysicalElements
{
  CIM_PhysicalElement REF Component;
  CIM_FRU             REF FRU;
};
```

## <a name="members"></a><span data-ttu-id="202c7-110">成員</span><span class="sxs-lookup"><span data-stu-id="202c7-110">Members</span></span>

<span data-ttu-id="202c7-111">**CIM \_ FRUPhysicalElements** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="202c7-111">The **CIM\_FRUPhysicalElements** class has these types of members:</span></span>

-   [<span data-ttu-id="202c7-112">屬性</span><span class="sxs-lookup"><span data-stu-id="202c7-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="202c7-113">屬性</span><span class="sxs-lookup"><span data-stu-id="202c7-113">Properties</span></span>

<span data-ttu-id="202c7-114">**CIM \_ FRUPhysicalElements** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="202c7-114">The **CIM\_FRUPhysicalElements** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="202c7-115">**元件**</span><span class="sxs-lookup"><span data-stu-id="202c7-115">**Component**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="202c7-116">資料類型： **CIM \_ PhysicalElement**</span><span class="sxs-lookup"><span data-stu-id="202c7-116">Data type: **CIM\_PhysicalElement**</span></span>
</dt> <dt>

<span data-ttu-id="202c7-117">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="202c7-117">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="202c7-118">參考屬於 FRU 一部分的實體元素。</span><span class="sxs-lookup"><span data-stu-id="202c7-118">Reference to a physical element that is a part of the FRU.</span></span>

</dd> <dt>

<span data-ttu-id="202c7-119">**FRU**</span><span class="sxs-lookup"><span data-stu-id="202c7-119">**FRU**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="202c7-120">資料類型： **CIM \_ FRU**</span><span class="sxs-lookup"><span data-stu-id="202c7-120">Data type: **CIM\_FRU**</span></span>
</dt> <dt>

<span data-ttu-id="202c7-121">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="202c7-121">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="202c7-122">限定詞： [**Aggregate**](/windows/desktop/WmiSdk/standard-qualifiers)、 [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1) </span><span class="sxs-lookup"><span data-stu-id="202c7-122">Qualifiers: [**Aggregate**](/windows/desktop/WmiSdk/standard-qualifiers), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1)</span></span>
</dt> </dl>

<span data-ttu-id="202c7-123">FRU 的參考。</span><span class="sxs-lookup"><span data-stu-id="202c7-123">Reference to the FRU.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="202c7-124">備註</span><span class="sxs-lookup"><span data-stu-id="202c7-124">Remarks</span></span>

<span data-ttu-id="202c7-125">WMI 不會執行這個類別。</span><span class="sxs-lookup"><span data-stu-id="202c7-125">WMI does not implement this class.</span></span>

<span data-ttu-id="202c7-126">此檔衍生自 DMTF 所發佈的 CIM 類別描述。</span><span class="sxs-lookup"><span data-stu-id="202c7-126">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="202c7-127">Microsoft 可能已進行變更，以更正次要錯誤、符合 Microsoft SDK 檔標準，或提供詳細資訊。</span><span class="sxs-lookup"><span data-stu-id="202c7-127">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="202c7-128">規格需求</span><span class="sxs-lookup"><span data-stu-id="202c7-128">Requirements</span></span>



| <span data-ttu-id="202c7-129">需求</span><span class="sxs-lookup"><span data-stu-id="202c7-129">Requirement</span></span> | <span data-ttu-id="202c7-130">值</span><span class="sxs-lookup"><span data-stu-id="202c7-130">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="202c7-131">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="202c7-131">Minimum supported client</span></span><br/> | <span data-ttu-id="202c7-132">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="202c7-132">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="202c7-133">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="202c7-133">Minimum supported server</span></span><br/> | <span data-ttu-id="202c7-134">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="202c7-134">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="202c7-135">命名空間</span><span class="sxs-lookup"><span data-stu-id="202c7-135">Namespace</span></span><br/>                | <span data-ttu-id="202c7-136">根 \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="202c7-136">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="202c7-137">MOF</span><span class="sxs-lookup"><span data-stu-id="202c7-137">MOF</span></span><br/>                      | <dl> <span data-ttu-id="202c7-138"><dt>CIMWin32 mof</dt></span><span class="sxs-lookup"><span data-stu-id="202c7-138"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="202c7-139">DLL</span><span class="sxs-lookup"><span data-stu-id="202c7-139">DLL</span></span><br/>                      | <dl> <span data-ttu-id="202c7-140"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="202c7-140"><dt>CIMWin32.dll</dt></span></span> </dl> |



 

