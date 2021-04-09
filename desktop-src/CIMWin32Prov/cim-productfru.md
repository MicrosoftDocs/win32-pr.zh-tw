---
description: CIM \_ ProductFRU 類別代表產品與現場可更換單元之間的關聯 (FRU) ，其提供已被取代之產品元件的相關資訊。
ms.assetid: 15d682e5-cd90-4fc4-8fff-e3fe1d2a0ac4
ms.tgt_platform: multiple
title: CIM_ProductFRU 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_ProductFRU
- CIM_ProductFRU.FRU
- CIM_ProductFRU.Product
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: b141d16adb50c5bc3f8d6be682a90aa4921061ef
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104110372"
---
# <a name="cim_productfru-class"></a><span data-ttu-id="60cb8-103">CIM \_ ProductFRU 類別</span><span class="sxs-lookup"><span data-stu-id="60cb8-103">CIM\_ProductFRU class</span></span>

<span data-ttu-id="60cb8-104">**CIM \_ ProductFRU** 類別代表產品與現場可更換單元之間的關聯 (FRU) ，其提供已被取代之產品元件的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="60cb8-104">The **CIM\_ProductFRU** class represents an association between the product and a field replaceable unit (FRU), which provides information about product components that have been, or are being replaced.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="60cb8-105">DMTF (分散式管理工作強制) CIM (通用訊息模型) 類別是用來建立 WMI 類別的父類別。</span><span class="sxs-lookup"><span data-stu-id="60cb8-105">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="60cb8-106">WMI 目前僅支援 [CIM 2.x 版的架構](https://dmtf.org/standards/cim/schemas)。</span><span class="sxs-lookup"><span data-stu-id="60cb8-106">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="60cb8-107">下列語法已從受控物件格式的 (MOF) 程式碼簡化，並包含其所有繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="60cb8-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of its inherited properties.</span></span> <span data-ttu-id="60cb8-108">屬性會依字母順序列出，而不是依 MOF 順序列出。</span><span class="sxs-lookup"><span data-stu-id="60cb8-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="60cb8-109">語法</span><span class="sxs-lookup"><span data-stu-id="60cb8-109">Syntax</span></span>

``` syntax
[Abstract, UUID("{EB98A1B2-DB36-11d2-85FC-0000F8102E5F}"), Association, AMENDMENT]
class CIM_ProductFRU
{
  CIM_FRU     REF FRU;
  CIM_Product REF Product;
};
```

## <a name="members"></a><span data-ttu-id="60cb8-110">成員</span><span class="sxs-lookup"><span data-stu-id="60cb8-110">Members</span></span>

<span data-ttu-id="60cb8-111">**CIM \_ ProductFRU** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="60cb8-111">The **CIM\_ProductFRU** class has these types of members:</span></span>

-   [<span data-ttu-id="60cb8-112">屬性</span><span class="sxs-lookup"><span data-stu-id="60cb8-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="60cb8-113">屬性</span><span class="sxs-lookup"><span data-stu-id="60cb8-113">Properties</span></span>

<span data-ttu-id="60cb8-114">**CIM \_ ProductFRU** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="60cb8-114">The **CIM\_ProductFRU** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="60cb8-115">**FRU**</span><span class="sxs-lookup"><span data-stu-id="60cb8-115">**FRU**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="60cb8-116">資料類型： **CIM \_ FRU**</span><span class="sxs-lookup"><span data-stu-id="60cb8-116">Data type: **CIM\_FRU**</span></span>
</dt> <dt>

<span data-ttu-id="60cb8-117">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="60cb8-117">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="60cb8-118">FRU 的參考。</span><span class="sxs-lookup"><span data-stu-id="60cb8-118">Reference to the FRU.</span></span>

</dd> <dt>

<span data-ttu-id="60cb8-119">**產品**</span><span class="sxs-lookup"><span data-stu-id="60cb8-119">**Product**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="60cb8-120">資料類型： **CIM \_ 產品**</span><span class="sxs-lookup"><span data-stu-id="60cb8-120">Data type: **CIM\_Product**</span></span>
</dt> <dt>

<span data-ttu-id="60cb8-121">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="60cb8-121">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="60cb8-122">限定詞： [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1) </span><span class="sxs-lookup"><span data-stu-id="60cb8-122">Qualifiers: [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1)</span></span>
</dt> </dl>

<span data-ttu-id="60cb8-123">要套用 FRU 的產品參考。</span><span class="sxs-lookup"><span data-stu-id="60cb8-123">Reference to the product to which the FRU is applied.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="60cb8-124">備註</span><span class="sxs-lookup"><span data-stu-id="60cb8-124">Remarks</span></span>

<span data-ttu-id="60cb8-125">WMI 不會執行這個類別。</span><span class="sxs-lookup"><span data-stu-id="60cb8-125">WMI does not implement this class.</span></span>

<span data-ttu-id="60cb8-126">此檔衍生自 DMTF 所發佈的 CIM 類別描述。</span><span class="sxs-lookup"><span data-stu-id="60cb8-126">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="60cb8-127">Microsoft 可能已進行變更，以更正次要錯誤、符合 Microsoft SDK 檔標準，或提供詳細資訊。</span><span class="sxs-lookup"><span data-stu-id="60cb8-127">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="60cb8-128">規格需求</span><span class="sxs-lookup"><span data-stu-id="60cb8-128">Requirements</span></span>



| <span data-ttu-id="60cb8-129">需求</span><span class="sxs-lookup"><span data-stu-id="60cb8-129">Requirement</span></span> | <span data-ttu-id="60cb8-130">值</span><span class="sxs-lookup"><span data-stu-id="60cb8-130">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="60cb8-131">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="60cb8-131">Minimum supported client</span></span><br/> | <span data-ttu-id="60cb8-132">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="60cb8-132">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="60cb8-133">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="60cb8-133">Minimum supported server</span></span><br/> | <span data-ttu-id="60cb8-134">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="60cb8-134">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="60cb8-135">命名空間</span><span class="sxs-lookup"><span data-stu-id="60cb8-135">Namespace</span></span><br/>                | <span data-ttu-id="60cb8-136">根 \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="60cb8-136">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="60cb8-137">MOF</span><span class="sxs-lookup"><span data-stu-id="60cb8-137">MOF</span></span><br/>                      | <dl> <span data-ttu-id="60cb8-138"><dt>CIMWin32 mof</dt></span><span class="sxs-lookup"><span data-stu-id="60cb8-138"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="60cb8-139">DLL</span><span class="sxs-lookup"><span data-stu-id="60cb8-139">DLL</span></span><br/>                      | <dl> <span data-ttu-id="60cb8-140"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="60cb8-140"><dt>CIMWin32.dll</dt></span></span> </dl> |



 

