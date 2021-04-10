---
description: CIM \_ Statistics 類別代表關聯，可將 managed 系統專案與套用至這些專案的統計群組產生關聯。
ms.assetid: fc75991b-adcd-4e47-b610-7503f6bb7c03
ms.tgt_platform: multiple
title: CIM_Statistics 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_Statistics
- CIM_Statistics.Element
- CIM_Statistics.Stats
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: b35299a52c771ee3bcb76673ef1e2164af3b3180
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103936115"
---
# <a name="cim_statistics-class"></a><span data-ttu-id="cae62-103">CIM \_ 統計資料類別</span><span class="sxs-lookup"><span data-stu-id="cae62-103">CIM\_Statistics class</span></span>

<span data-ttu-id="cae62-104">**CIM \_ Statistics** 類別代表關聯，可將 managed 系統專案與套用至這些專案的統計群組產生關聯。</span><span class="sxs-lookup"><span data-stu-id="cae62-104">The **CIM\_Statistics** class represents an association that relates managed system elements to the statistical groups that apply to them.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="cae62-105">DMTF (分散式管理工作強制) CIM (通用訊息模型) 類別是用來建立 WMI 類別的父類別。</span><span class="sxs-lookup"><span data-stu-id="cae62-105">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="cae62-106">WMI 目前僅支援 [CIM 2.x 版的架構](https://dmtf.org/standards/cim/schemas)。</span><span class="sxs-lookup"><span data-stu-id="cae62-106">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="cae62-107">下列語法已從受控物件格式的 (MOF) 程式碼簡化，並包含其所有繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="cae62-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of its inherited properties.</span></span> <span data-ttu-id="cae62-108">屬性會依字母順序列出，而不是依 MOF 順序列出。</span><span class="sxs-lookup"><span data-stu-id="cae62-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="cae62-109">語法</span><span class="sxs-lookup"><span data-stu-id="cae62-109">Syntax</span></span>

``` syntax
[Abstract, Association, UUID("{956597A3-7D80-11D2-AAD3-006008C78BC7}"), AMENDMENT]
class CIM_Statistics
{
  CIM_ManagedSystemElement   REF Element;
  CIM_StatisticalInformation REF Stats;
};
```

## <a name="members"></a><span data-ttu-id="cae62-110">成員</span><span class="sxs-lookup"><span data-stu-id="cae62-110">Members</span></span>

<span data-ttu-id="cae62-111">**CIM \_ Statistics** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="cae62-111">The **CIM\_Statistics** class has these types of members:</span></span>

-   [<span data-ttu-id="cae62-112">屬性</span><span class="sxs-lookup"><span data-stu-id="cae62-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="cae62-113">屬性</span><span class="sxs-lookup"><span data-stu-id="cae62-113">Properties</span></span>

<span data-ttu-id="cae62-114">**CIM \_ Statistics** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="cae62-114">The **CIM\_Statistics** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="cae62-115">**Element**</span><span class="sxs-lookup"><span data-stu-id="cae62-115">**Element**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cae62-116">資料類型： **CIM \_ ManagedSystemElement**</span><span class="sxs-lookup"><span data-stu-id="cae62-116">Data type: **CIM\_ManagedSystemElement**</span></span>
</dt> <dt>

<span data-ttu-id="cae62-117">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="cae62-117">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="cae62-118">參考定義統計資料或計量資料的 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md) 類別。</span><span class="sxs-lookup"><span data-stu-id="cae62-118">Reference to the [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md) class for which statistical or metric data is defined.</span></span>

</dd> <dt>

<span data-ttu-id="cae62-119">**統計**</span><span class="sxs-lookup"><span data-stu-id="cae62-119">**Stats**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cae62-120">資料類型： **CIM \_ StatisticalInformation**</span><span class="sxs-lookup"><span data-stu-id="cae62-120">Data type: **CIM\_StatisticalInformation**</span></span>
</dt> <dt>

<span data-ttu-id="cae62-121">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="cae62-121">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="cae62-122">統計資訊或物件的參考。</span><span class="sxs-lookup"><span data-stu-id="cae62-122">Reference to the statistical information or object.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="cae62-123">備註</span><span class="sxs-lookup"><span data-stu-id="cae62-123">Remarks</span></span>

<span data-ttu-id="cae62-124">WMI 不會執行這個類別。</span><span class="sxs-lookup"><span data-stu-id="cae62-124">WMI does not implement this class.</span></span>

<span data-ttu-id="cae62-125">此檔衍生自 DMTF 所發佈的 CIM 類別描述。</span><span class="sxs-lookup"><span data-stu-id="cae62-125">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="cae62-126">Microsoft 可能已進行變更，以更正次要錯誤、符合 Microsoft SDK 檔標準，或提供詳細資訊。</span><span class="sxs-lookup"><span data-stu-id="cae62-126">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="cae62-127">規格需求</span><span class="sxs-lookup"><span data-stu-id="cae62-127">Requirements</span></span>



| <span data-ttu-id="cae62-128">需求</span><span class="sxs-lookup"><span data-stu-id="cae62-128">Requirement</span></span> | <span data-ttu-id="cae62-129">值</span><span class="sxs-lookup"><span data-stu-id="cae62-129">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="cae62-130">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="cae62-130">Minimum supported client</span></span><br/> | <span data-ttu-id="cae62-131">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="cae62-131">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="cae62-132">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="cae62-132">Minimum supported server</span></span><br/> | <span data-ttu-id="cae62-133">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="cae62-133">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="cae62-134">命名空間</span><span class="sxs-lookup"><span data-stu-id="cae62-134">Namespace</span></span><br/>                | <span data-ttu-id="cae62-135">根 \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="cae62-135">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="cae62-136">MOF</span><span class="sxs-lookup"><span data-stu-id="cae62-136">MOF</span></span><br/>                      | <dl> <span data-ttu-id="cae62-137"><dt>CIMWin32 mof</dt></span><span class="sxs-lookup"><span data-stu-id="cae62-137"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="cae62-138">DLL</span><span class="sxs-lookup"><span data-stu-id="cae62-138">DLL</span></span><br/>                      | <dl> <span data-ttu-id="cae62-139"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="cae62-139"><dt>CIMWin32.dll</dt></span></span> </dl> |



 

 




