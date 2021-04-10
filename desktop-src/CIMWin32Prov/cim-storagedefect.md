---
description: CIM \_ StorageDefect 匯總會收集儲存區的儲存錯誤。
ms.assetid: 7acd3d25-4691-43cb-badc-662684989345
ms.tgt_platform: multiple
title: CIM_StorageDefect 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_StorageDefect
- CIM_StorageDefect.Error
- CIM_StorageDefect.Extent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 8e6c2be45fe2f44afa407dc72e3ae90c486593ec
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103936468"
---
# <a name="cim_storagedefect-class"></a><span data-ttu-id="5895f-103">CIM \_ StorageDefect 類別</span><span class="sxs-lookup"><span data-stu-id="5895f-103">CIM\_StorageDefect class</span></span>

<span data-ttu-id="5895f-104">**CIM \_ StorageDefect** 匯總會收集儲存區的儲存錯誤。</span><span class="sxs-lookup"><span data-stu-id="5895f-104">The **CIM\_StorageDefect** aggregation collects the storage errors for a storage extent.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="5895f-105">DMTF (分散式管理工作強制) CIM (通用訊息模型) 類別是用來建立 WMI 類別的父類別。</span><span class="sxs-lookup"><span data-stu-id="5895f-105">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="5895f-106">WMI 目前僅支援 [CIM 2.x 版的架構](https://dmtf.org/standards/cim/schemas)。</span><span class="sxs-lookup"><span data-stu-id="5895f-106">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="5895f-107">下列語法已從受控物件格式的 (MOF) 程式碼簡化，並包含其所有繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="5895f-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of its inherited properties.</span></span> <span data-ttu-id="5895f-108">屬性會依字母順序列出，而不是依 MOF 順序列出。</span><span class="sxs-lookup"><span data-stu-id="5895f-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="5895f-109">語法</span><span class="sxs-lookup"><span data-stu-id="5895f-109">Syntax</span></span>

``` syntax
[Abstract, UUID("{5CC70817-DB31-11d2-85FC-0000F8102E5F}"), Aggregation, Association, AMENDMENT]
class CIM_StorageDefect
{
  CIM_StorageError  REF Error;
  CIM_StorageExtent REF Extent;
};
```

## <a name="members"></a><span data-ttu-id="5895f-110">成員</span><span class="sxs-lookup"><span data-stu-id="5895f-110">Members</span></span>

<span data-ttu-id="5895f-111">**CIM \_ StorageDefect** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="5895f-111">The **CIM\_StorageDefect** class has these types of members:</span></span>

-   [<span data-ttu-id="5895f-112">屬性</span><span class="sxs-lookup"><span data-stu-id="5895f-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="5895f-113">屬性</span><span class="sxs-lookup"><span data-stu-id="5895f-113">Properties</span></span>

<span data-ttu-id="5895f-114">**CIM \_ StorageDefect** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="5895f-114">The **CIM\_StorageDefect** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="5895f-115">**錯誤**</span><span class="sxs-lookup"><span data-stu-id="5895f-115">**Error**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5895f-116">資料類型： **CIM \_ StorageError**</span><span class="sxs-lookup"><span data-stu-id="5895f-116">Data type: **CIM\_StorageError**</span></span>
</dt> <dt>

<span data-ttu-id="5895f-117">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="5895f-117">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5895f-118">限定詞： [**弱** 式](/windows/desktop/WmiSdk/standard-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="5895f-118">Qualifiers: [**Weak**](/windows/desktop/WmiSdk/standard-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="5895f-119">錯誤物件的參考，這個物件會定義對應于儲存區的開始和結束位址。</span><span class="sxs-lookup"><span data-stu-id="5895f-119">Reference to the error object, which defines the starting and ending addresses that are mapped out of the storage extent.</span></span>

</dd> <dt>

<span data-ttu-id="5895f-120">**Extent**</span><span class="sxs-lookup"><span data-stu-id="5895f-120">**Extent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5895f-121">資料類型： **CIM \_ StorageExtent**</span><span class="sxs-lookup"><span data-stu-id="5895f-121">Data type: **CIM\_StorageExtent**</span></span>
</dt> <dt>

<span data-ttu-id="5895f-122">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="5895f-122">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5895f-123">限定詞： [**Aggregate**](/windows/desktop/WmiSdk/standard-qualifiers)、 [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1) 、 [**Min**](/windows/desktop/WmiSdk/standard-qualifiers) (1) </span><span class="sxs-lookup"><span data-stu-id="5895f-123">Qualifiers: [**Aggregate**](/windows/desktop/WmiSdk/standard-qualifiers), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**Min**](/windows/desktop/WmiSdk/standard-qualifiers) (1)</span></span>
</dt> </dl>

<span data-ttu-id="5895f-124">參考發生錯誤的儲存區。</span><span class="sxs-lookup"><span data-stu-id="5895f-124">Reference to the storage extent on which the errors occurred.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="5895f-125">備註</span><span class="sxs-lookup"><span data-stu-id="5895f-125">Remarks</span></span>

<span data-ttu-id="5895f-126">WMI 不會執行這個類別。</span><span class="sxs-lookup"><span data-stu-id="5895f-126">WMI does not implement this class.</span></span>

<span data-ttu-id="5895f-127">此檔衍生自 DMTF 所發佈的 CIM 類別描述。</span><span class="sxs-lookup"><span data-stu-id="5895f-127">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="5895f-128">Microsoft 可能已進行變更，以更正次要錯誤、符合 Microsoft SDK 檔標準，或提供詳細資訊。</span><span class="sxs-lookup"><span data-stu-id="5895f-128">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="5895f-129">規格需求</span><span class="sxs-lookup"><span data-stu-id="5895f-129">Requirements</span></span>



| <span data-ttu-id="5895f-130">需求</span><span class="sxs-lookup"><span data-stu-id="5895f-130">Requirement</span></span> | <span data-ttu-id="5895f-131">值</span><span class="sxs-lookup"><span data-stu-id="5895f-131">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="5895f-132">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="5895f-132">Minimum supported client</span></span><br/> | <span data-ttu-id="5895f-133">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="5895f-133">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="5895f-134">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="5895f-134">Minimum supported server</span></span><br/> | <span data-ttu-id="5895f-135">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="5895f-135">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="5895f-136">命名空間</span><span class="sxs-lookup"><span data-stu-id="5895f-136">Namespace</span></span><br/>                | <span data-ttu-id="5895f-137">根 \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="5895f-137">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="5895f-138">MOF</span><span class="sxs-lookup"><span data-stu-id="5895f-138">MOF</span></span><br/>                      | <dl> <span data-ttu-id="5895f-139"><dt>CIMWin32 mof</dt></span><span class="sxs-lookup"><span data-stu-id="5895f-139"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="5895f-140">DLL</span><span class="sxs-lookup"><span data-stu-id="5895f-140">DLL</span></span><br/>                      | <dl> <span data-ttu-id="5895f-141"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5895f-141"><dt>CIMWin32.dll</dt></span></span> </dl> |



 

