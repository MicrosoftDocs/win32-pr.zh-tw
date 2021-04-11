---
description: CIM \_ StatisticalInformation 類別是適用于一或多個 managed 系統專案之統計資料或計量的任意集合的根類別。
ms.assetid: ecc3b310-c553-416b-b4e3-705965557945
ms.tgt_platform: multiple
title: CIM_StatisticalInformation 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_StatisticalInformation
- CIM_StatisticalInformation.Caption
- CIM_StatisticalInformation.Description
- CIM_StatisticalInformation.Name
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: b6eda3e2463c880a58c4e23a6d09dcab99417ead
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103847561"
---
# <a name="cim_statisticalinformation-class"></a><span data-ttu-id="ce790-103">CIM \_ StatisticalInformation 類別</span><span class="sxs-lookup"><span data-stu-id="ce790-103">CIM\_StatisticalInformation class</span></span>

<span data-ttu-id="ce790-104">**CIM \_ StatisticalInformation** 類別是適用于一或多個 managed 系統專案之統計資料或計量的任意集合的根類別。</span><span class="sxs-lookup"><span data-stu-id="ce790-104">The **CIM\_StatisticalInformation** class is a root class for the arbitrary collection of statistical data or metrics applicable to one or more managed system elements.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="ce790-105">DMTF (分散式管理工作強制) CIM (通用訊息模型) 類別是用來建立 WMI 類別的父類別。</span><span class="sxs-lookup"><span data-stu-id="ce790-105">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="ce790-106">WMI 目前僅支援 [CIM 2.x 版的架構](https://dmtf.org/standards/cim/schemas)。</span><span class="sxs-lookup"><span data-stu-id="ce790-106">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="ce790-107">下列語法已從受控物件格式的 (MOF) 程式碼簡化，並包含其所有繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="ce790-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of its inherited properties.</span></span> <span data-ttu-id="ce790-108">屬性會依字母順序列出，而不是依 MOF 順序列出。</span><span class="sxs-lookup"><span data-stu-id="ce790-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="ce790-109">語法</span><span class="sxs-lookup"><span data-stu-id="ce790-109">Syntax</span></span>

``` syntax
[Abstract, UUID("{956597A1-7D80-11D2-AAD3-006008C78BC7}"), AMENDMENT]
class CIM_StatisticalInformation
{
  string Caption;
  string Description;
  string Name;
};
```

## <a name="members"></a><span data-ttu-id="ce790-110">成員</span><span class="sxs-lookup"><span data-stu-id="ce790-110">Members</span></span>

<span data-ttu-id="ce790-111">**CIM \_ StatisticalInformation** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="ce790-111">The **CIM\_StatisticalInformation** class has these types of members:</span></span>

-   [<span data-ttu-id="ce790-112">屬性</span><span class="sxs-lookup"><span data-stu-id="ce790-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="ce790-113">屬性</span><span class="sxs-lookup"><span data-stu-id="ce790-113">Properties</span></span>

<span data-ttu-id="ce790-114">**CIM \_ StatisticalInformation** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="ce790-114">The **CIM\_StatisticalInformation** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="ce790-115">**標題**</span><span class="sxs-lookup"><span data-stu-id="ce790-115">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ce790-116">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="ce790-116">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ce790-117">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="ce790-117">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ce790-118">限定詞： [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64) </span><span class="sxs-lookup"><span data-stu-id="ce790-118">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="ce790-119">統計資料或度量的簡短文字描述。</span><span class="sxs-lookup"><span data-stu-id="ce790-119">Short textual description for the statistic or metric.</span></span>

</dd> <dt>

<span data-ttu-id="ce790-120">**說明**</span><span class="sxs-lookup"><span data-stu-id="ce790-120">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ce790-121">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="ce790-121">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ce790-122">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="ce790-122">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ce790-123">統計資料或度量的文字描述。</span><span class="sxs-lookup"><span data-stu-id="ce790-123">Textual description of the statistic or metric.</span></span>

</dd> <dt>

<span data-ttu-id="ce790-124">**名稱**</span><span class="sxs-lookup"><span data-stu-id="ce790-124">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ce790-125">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="ce790-125">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ce790-126">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="ce790-126">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ce790-127">限定詞： [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256) </span><span class="sxs-lookup"><span data-stu-id="ce790-127">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="ce790-128">統計資料或度量已知的標籤。</span><span class="sxs-lookup"><span data-stu-id="ce790-128">Label by which the statistic or metric is known.</span></span> <span data-ttu-id="ce790-129">子類別化時，可以將這個屬性覆寫為索引鍵屬性。</span><span class="sxs-lookup"><span data-stu-id="ce790-129">When subclassed, this property can be overridden to be a key property.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="ce790-130">備註</span><span class="sxs-lookup"><span data-stu-id="ce790-130">Remarks</span></span>

<span data-ttu-id="ce790-131">WMI 不會執行這個類別。</span><span class="sxs-lookup"><span data-stu-id="ce790-131">WMI does not implement this class.</span></span> <span data-ttu-id="ce790-132">針對衍生自 **CIM \_ STATISTICALINFORMATION** 的 WMI 類別，請參閱 [Win32 類別](win32-provider.md)。</span><span class="sxs-lookup"><span data-stu-id="ce790-132">For WMI classes derived from **CIM\_StatisticalInformation**, see [Win32 Classes](win32-provider.md).</span></span>

<span data-ttu-id="ce790-133">此檔衍生自 DMTF 所發佈的 CIM 類別描述。</span><span class="sxs-lookup"><span data-stu-id="ce790-133">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="ce790-134">Microsoft 可能已進行變更，以更正次要錯誤、符合 Microsoft SDK 檔標準，或提供詳細資訊。</span><span class="sxs-lookup"><span data-stu-id="ce790-134">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="ce790-135">規格需求</span><span class="sxs-lookup"><span data-stu-id="ce790-135">Requirements</span></span>



| <span data-ttu-id="ce790-136">需求</span><span class="sxs-lookup"><span data-stu-id="ce790-136">Requirement</span></span> | <span data-ttu-id="ce790-137">值</span><span class="sxs-lookup"><span data-stu-id="ce790-137">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="ce790-138">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="ce790-138">Minimum supported client</span></span><br/> | <span data-ttu-id="ce790-139">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="ce790-139">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="ce790-140">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="ce790-140">Minimum supported server</span></span><br/> | <span data-ttu-id="ce790-141">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="ce790-141">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="ce790-142">命名空間</span><span class="sxs-lookup"><span data-stu-id="ce790-142">Namespace</span></span><br/>                | <span data-ttu-id="ce790-143">根 \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="ce790-143">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="ce790-144">MOF</span><span class="sxs-lookup"><span data-stu-id="ce790-144">MOF</span></span><br/>                      | <dl> <span data-ttu-id="ce790-145"><dt>CIMWin32 mof</dt></span><span class="sxs-lookup"><span data-stu-id="ce790-145"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="ce790-146">DLL</span><span class="sxs-lookup"><span data-stu-id="ce790-146">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ce790-147"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ce790-147"><dt>CIMWin32.dll</dt></span></span> </dl> |



 

