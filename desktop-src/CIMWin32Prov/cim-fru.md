---
description: CIM \_ FRU 類別代表廠商定義的產品和實體元素集合，與現場可更換單元相關聯 (FRU) 在客戶的位置支援、維護或升級產品。
ms.assetid: 4464ec3a-5509-4e15-9020-4abb2edd2570
ms.tgt_platform: multiple
title: CIM_FRU 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_FRU
- CIM_FRU.Caption
- CIM_FRU.Description
- CIM_FRU.FRUNumber
- CIM_FRU.IdentifyingNumber
- CIM_FRU.Name
- CIM_FRU.RevisionLevel
- CIM_FRU.Vendor
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: d163c3c223159ad8e09aa6e36d63187ff0aa97f4
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103688911"
---
# <a name="cim_fru-class"></a><span data-ttu-id="170b3-103">CIM \_ FRU 類別</span><span class="sxs-lookup"><span data-stu-id="170b3-103">CIM\_FRU class</span></span>

<span data-ttu-id="170b3-104">**CIM \_ FRU** 類別代表廠商定義的產品和實體元素集合，與現場可更換單元相關聯 (FRU) 在客戶的位置支援、維護或升級產品。</span><span class="sxs-lookup"><span data-stu-id="170b3-104">The **CIM\_FRU** class represents a vendor-defined collection of products and physical elements that are associated with a field replaceable unit (FRU) to support, maintain, or upgrade a product at the customer's location.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="170b3-105">DMTF (分散式管理工作強制) CIM (通用訊息模型) 類別是用來建立 WMI 類別的父類別。</span><span class="sxs-lookup"><span data-stu-id="170b3-105">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="170b3-106">WMI 目前僅支援 [CIM 2.x 版的架構](https://dmtf.org/standards/cim/schemas)。</span><span class="sxs-lookup"><span data-stu-id="170b3-106">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="170b3-107">下列語法已從受管理物件格式 (MOF) 程式碼加以簡化，並包含所有繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="170b3-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="170b3-108">屬性會依字母順序列出，而不是依 MOF 順序列出。</span><span class="sxs-lookup"><span data-stu-id="170b3-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="170b3-109">語法</span><span class="sxs-lookup"><span data-stu-id="170b3-109">Syntax</span></span>

``` syntax
[Abstract, UUID("{778C74EE-DB2A-11d2-85FC-0000F8102E5F}"), AMENDMENT]
class CIM_FRU
{
  string Caption;
  string Description;
  string FRUNumber;
  string IdentifyingNumber;
  string Name;
  string RevisionLevel;
  string Vendor;
};
```

## <a name="members"></a><span data-ttu-id="170b3-110">成員</span><span class="sxs-lookup"><span data-stu-id="170b3-110">Members</span></span>

<span data-ttu-id="170b3-111">**CIM \_ FRU** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="170b3-111">The **CIM\_FRU** class has these types of members:</span></span>

-   [<span data-ttu-id="170b3-112">屬性</span><span class="sxs-lookup"><span data-stu-id="170b3-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="170b3-113">屬性</span><span class="sxs-lookup"><span data-stu-id="170b3-113">Properties</span></span>

<span data-ttu-id="170b3-114">**CIM \_ FRU** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="170b3-114">The **CIM\_FRU** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="170b3-115">**標題**</span><span class="sxs-lookup"><span data-stu-id="170b3-115">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="170b3-116">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="170b3-116">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="170b3-117">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="170b3-117">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="170b3-118">限定詞： [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64) </span><span class="sxs-lookup"><span data-stu-id="170b3-118">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="170b3-119">FRU 的簡短文字描述。</span><span class="sxs-lookup"><span data-stu-id="170b3-119">Short textual description for the FRU.</span></span>

</dd> <dt>

<span data-ttu-id="170b3-120">**說明**</span><span class="sxs-lookup"><span data-stu-id="170b3-120">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="170b3-121">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="170b3-121">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="170b3-122">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="170b3-122">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="170b3-123">限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "MIF。DMTF \| FRU \| 002.3」 ) </span><span class="sxs-lookup"><span data-stu-id="170b3-123">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|FRU\|002.3")</span></span>
</dt> </dl>

<span data-ttu-id="170b3-124">FRU 的描述。</span><span class="sxs-lookup"><span data-stu-id="170b3-124">Description of the FRU.</span></span>

</dd> <dt>

<span data-ttu-id="170b3-125">**FRUNumber**</span><span class="sxs-lookup"><span data-stu-id="170b3-125">**FRUNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="170b3-126">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="170b3-126">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="170b3-127">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="170b3-127">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="170b3-128">限定詞： [**Key**](/windows/desktop/WmiSdk/key-qualifier)， [**MAPPINGSTRINGS**](/windows/desktop/WmiSdk/standard-qualifiers) ( "MIF。DMTF \| FRU \| 002.6 ") ， [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64) </span><span class="sxs-lookup"><span data-stu-id="170b3-128">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|FRU\|002.6"), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="170b3-129">FRU 訂購資訊。</span><span class="sxs-lookup"><span data-stu-id="170b3-129">FRU ordering information.</span></span>

</dd> <dt>

<span data-ttu-id="170b3-130">**IdentifyingNumber**</span><span class="sxs-lookup"><span data-stu-id="170b3-130">**IdentifyingNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="170b3-131">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="170b3-131">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="170b3-132">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="170b3-132">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="170b3-133">限定詞： [**Key**](/windows/desktop/WmiSdk/key-qualifier)， [**MAPPINGSTRINGS**](/windows/desktop/WmiSdk/standard-qualifiers) ( "MIF。DMTF \| FRU \| 002.7 ") ， [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64) </span><span class="sxs-lookup"><span data-stu-id="170b3-133">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|FRU\|002.7"), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="170b3-134">識別軟體，例如序號或硬體晶片上的骰子編號。</span><span class="sxs-lookup"><span data-stu-id="170b3-134">Identification on software, such as a serial number, or a die number on a hardware chip.</span></span>

</dd> <dt>

<span data-ttu-id="170b3-135">**名稱**</span><span class="sxs-lookup"><span data-stu-id="170b3-135">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="170b3-136">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="170b3-136">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="170b3-137">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="170b3-137">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="170b3-138">限定詞： [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256) </span><span class="sxs-lookup"><span data-stu-id="170b3-138">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="170b3-139">已知物件的標籤。</span><span class="sxs-lookup"><span data-stu-id="170b3-139">Label by which the object is known.</span></span>

</dd> <dt>

<span data-ttu-id="170b3-140">**RevisionLevel**</span><span class="sxs-lookup"><span data-stu-id="170b3-140">**RevisionLevel**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="170b3-141">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="170b3-141">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="170b3-142">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="170b3-142">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="170b3-143">限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "MIF。DMTF \| FRU \| 002.8 ") ， [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64) </span><span class="sxs-lookup"><span data-stu-id="170b3-143">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|FRU\|002.8"), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="170b3-144">FRU 的修訂層級。</span><span class="sxs-lookup"><span data-stu-id="170b3-144">Revision level of the FRU.</span></span>

</dd> <dt>

<span data-ttu-id="170b3-145">**廠商**</span><span class="sxs-lookup"><span data-stu-id="170b3-145">**Vendor**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="170b3-146">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="170b3-146">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="170b3-147">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="170b3-147">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="170b3-148">限定詞： [**Key**](/windows/desktop/WmiSdk/key-qualifier)， [**MAPPINGSTRINGS**](/windows/desktop/WmiSdk/standard-qualifiers) ( "MIF。DMTF \| FRU \| 002.4 ") ， [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256) </span><span class="sxs-lookup"><span data-stu-id="170b3-148">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|FRU\|002.4"), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="170b3-149">供應商的名稱。</span><span class="sxs-lookup"><span data-stu-id="170b3-149">Name of the supplier.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="170b3-150">備註</span><span class="sxs-lookup"><span data-stu-id="170b3-150">Remarks</span></span>

<span data-ttu-id="170b3-151">WMI 不會執行這個類別。</span><span class="sxs-lookup"><span data-stu-id="170b3-151">WMI does not implement this class.</span></span>

<span data-ttu-id="170b3-152">此檔衍生自 DMTF 所發佈的 CIM 類別描述。</span><span class="sxs-lookup"><span data-stu-id="170b3-152">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="170b3-153">Microsoft 可能已進行變更，以更正次要錯誤、符合 Microsoft SDK 檔標準，或提供詳細資訊。</span><span class="sxs-lookup"><span data-stu-id="170b3-153">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="170b3-154">規格需求</span><span class="sxs-lookup"><span data-stu-id="170b3-154">Requirements</span></span>



| <span data-ttu-id="170b3-155">需求</span><span class="sxs-lookup"><span data-stu-id="170b3-155">Requirement</span></span> | <span data-ttu-id="170b3-156">值</span><span class="sxs-lookup"><span data-stu-id="170b3-156">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="170b3-157">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="170b3-157">Minimum supported client</span></span><br/> | <span data-ttu-id="170b3-158">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="170b3-158">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="170b3-159">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="170b3-159">Minimum supported server</span></span><br/> | <span data-ttu-id="170b3-160">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="170b3-160">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="170b3-161">命名空間</span><span class="sxs-lookup"><span data-stu-id="170b3-161">Namespace</span></span><br/>                | <span data-ttu-id="170b3-162">根 \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="170b3-162">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="170b3-163">MOF</span><span class="sxs-lookup"><span data-stu-id="170b3-163">MOF</span></span><br/>                      | <dl> <span data-ttu-id="170b3-164"><dt>CIMWin32 mof</dt></span><span class="sxs-lookup"><span data-stu-id="170b3-164"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="170b3-165">DLL</span><span class="sxs-lookup"><span data-stu-id="170b3-165">DLL</span></span><br/>                      | <dl> <span data-ttu-id="170b3-166"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="170b3-166"><dt>CIMWin32.dll</dt></span></span> </dl> |



 

