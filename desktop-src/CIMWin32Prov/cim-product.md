---
description: CIM \_ Product 類別是代表實體元素集合、軟體功能和其他產品（以單位形式取得）的實體類別。
ms.assetid: beb20f61-de39-4221-8d29-4727104518d5
ms.tgt_platform: multiple
title: CIM_Product 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_Product
- CIM_Product.Caption
- CIM_Product.Description
- CIM_Product.IdentifyingNumber
- CIM_Product.Name
- CIM_Product.SKUNumber
- CIM_Product.Vendor
- CIM_Product.Version
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 16c8541a18185d721bbdcbf23acaeb67adf508c7
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103688680"
---
# <a name="cim_product-class"></a><span data-ttu-id="0d179-103">CIM \_ 產品類別</span><span class="sxs-lookup"><span data-stu-id="0d179-103">CIM\_Product class</span></span>

<span data-ttu-id="0d179-104">**CIM \_ Product** 類別是代表實體元素集合、軟體功能和其他產品（以單位形式取得）的實體類別。</span><span class="sxs-lookup"><span data-stu-id="0d179-104">The **CIM\_Product** class is a concrete class that represents a collection of physical elements, software features and, other products, acquired as a unit.</span></span> <span data-ttu-id="0d179-105">取得意味著供應商與消費者之間的合約，可能會影響產品授權、支援和擔保。</span><span class="sxs-lookup"><span data-stu-id="0d179-105">Acquisition implies an agreement between the supplier and consumer, which can have implications on product licensing, support, and warranty.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="0d179-106">DMTF (分散式管理工作強制) CIM (通用訊息模型) 類別是用來建立 WMI 類別的父類別。</span><span class="sxs-lookup"><span data-stu-id="0d179-106">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="0d179-107">WMI 目前僅支援 [CIM 2.x 版的架構](https://dmtf.org/standards/cim/schemas)。</span><span class="sxs-lookup"><span data-stu-id="0d179-107">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="0d179-108">下列語法已從受控物件格式的 (MOF) 程式碼簡化，並包含其所有繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="0d179-108">The following syntax is simplified from Managed Object Format (MOF) code and includes all of its inherited properties.</span></span> <span data-ttu-id="0d179-109">屬性會依字母順序列出，而不是依 MOF 順序列出。</span><span class="sxs-lookup"><span data-stu-id="0d179-109">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="0d179-110">語法</span><span class="sxs-lookup"><span data-stu-id="0d179-110">Syntax</span></span>

``` syntax
[abstract, UUID("{FAF76B63-798C-11D2-AAD1-006008C78BC7}"), AMENDMENT]
class CIM_Product
{
  string Caption;
  string Description;
  string IdentifyingNumber;
  string Name;
  string SKUNumber;
  string Vendor;
  string Version;
};
```

## <a name="members"></a><span data-ttu-id="0d179-111">成員</span><span class="sxs-lookup"><span data-stu-id="0d179-111">Members</span></span>

<span data-ttu-id="0d179-112">**CIM \_ Product** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="0d179-112">The **CIM\_Product** class has these types of members:</span></span>

-   [<span data-ttu-id="0d179-113">屬性</span><span class="sxs-lookup"><span data-stu-id="0d179-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="0d179-114">屬性</span><span class="sxs-lookup"><span data-stu-id="0d179-114">Properties</span></span>

<span data-ttu-id="0d179-115">**CIM \_ Product** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="0d179-115">The **CIM\_Product** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="0d179-116">**標題**</span><span class="sxs-lookup"><span data-stu-id="0d179-116">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0d179-117">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="0d179-117">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0d179-118">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="0d179-118">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0d179-119">限定詞： [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64) </span><span class="sxs-lookup"><span data-stu-id="0d179-119">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="0d179-120">產品的簡短文字描述。</span><span class="sxs-lookup"><span data-stu-id="0d179-120">Short textual description for the product.</span></span>

</dd> <dt>

<span data-ttu-id="0d179-121">**說明**</span><span class="sxs-lookup"><span data-stu-id="0d179-121">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0d179-122">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="0d179-122">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0d179-123">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="0d179-123">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0d179-124">產品的文字描述。</span><span class="sxs-lookup"><span data-stu-id="0d179-124">Textual description of the product.</span></span>

</dd> <dt>

<span data-ttu-id="0d179-125">**IdentifyingNumber**</span><span class="sxs-lookup"><span data-stu-id="0d179-125">**IdentifyingNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0d179-126">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="0d179-126">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0d179-127">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="0d179-127">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0d179-128">限定詞： [**Key**](/windows/desktop/WmiSdk/key-qualifier)、 [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64) 、 [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "MIF。DMTF \| 元件 \| 001.4 ") </span><span class="sxs-lookup"><span data-stu-id="0d179-128">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.4")</span></span>
</dt> </dl>

<span data-ttu-id="0d179-129">產品識別，例如軟體序號、硬體晶片上的骰子號碼，或) 專案編號的非商業性產品 (。</span><span class="sxs-lookup"><span data-stu-id="0d179-129">Product identification, such as a serial number on software, a die number on a hardware chip, or (for noncommercial products) a project number.</span></span>

</dd> <dt>

<span data-ttu-id="0d179-130">**名稱**</span><span class="sxs-lookup"><span data-stu-id="0d179-130">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0d179-131">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="0d179-131">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0d179-132">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="0d179-132">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0d179-133">限定詞： [**Key**](/windows/desktop/WmiSdk/key-qualifier)、 [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256) 、 [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "MIF。DMTF \| 元件 \| 001.2 ") </span><span class="sxs-lookup"><span data-stu-id="0d179-133">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.2")</span></span>
</dt> </dl>

<span data-ttu-id="0d179-134">常用的產品名稱。</span><span class="sxs-lookup"><span data-stu-id="0d179-134">Commonly used product name.</span></span>

</dd> <dt>

<span data-ttu-id="0d179-135">**SKUNumber**</span><span class="sxs-lookup"><span data-stu-id="0d179-135">**SKUNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0d179-136">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="0d179-136">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0d179-137">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="0d179-137">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0d179-138">限定詞： [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64) </span><span class="sxs-lookup"><span data-stu-id="0d179-138">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="0d179-139">產品的庫存單位 (SKU) 資訊。</span><span class="sxs-lookup"><span data-stu-id="0d179-139">Product's stock-keeping unit (SKU) information.</span></span>

</dd> <dt>

<span data-ttu-id="0d179-140">**廠商**</span><span class="sxs-lookup"><span data-stu-id="0d179-140">**Vendor**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0d179-141">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="0d179-141">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0d179-142">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="0d179-142">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0d179-143">限定詞： [**CIM \_ 金鑰**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)、 [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256) 、 [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) (」 MIF。DMTF \| 元件 \| 001.1 ") </span><span class="sxs-lookup"><span data-stu-id="0d179-143">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.1")</span></span>
</dt> </dl>

<span data-ttu-id="0d179-144">產品供應商的名稱，或銷售產品的實體 (製造商、轉售商、OEM 等) 。</span><span class="sxs-lookup"><span data-stu-id="0d179-144">Name of the product's supplier, or the entity selling the product (the manufacturer, reseller, OEM, and so on).</span></span>

</dd> <dt>

<span data-ttu-id="0d179-145">**版本**</span><span class="sxs-lookup"><span data-stu-id="0d179-145">**Version**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0d179-146">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="0d179-146">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0d179-147">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="0d179-147">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0d179-148">限定詞： [**Key**](/windows/desktop/WmiSdk/key-qualifier)、 [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64) 、 [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "MIF。DMTF \| 元件 \| 001.3 ") </span><span class="sxs-lookup"><span data-stu-id="0d179-148">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.3")</span></span>
</dt> </dl>

<span data-ttu-id="0d179-149">產品版本資訊。</span><span class="sxs-lookup"><span data-stu-id="0d179-149">Product version information.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="0d179-150">備註</span><span class="sxs-lookup"><span data-stu-id="0d179-150">Remarks</span></span>

<span data-ttu-id="0d179-151">WMI 不會執行這個類別。</span><span class="sxs-lookup"><span data-stu-id="0d179-151">WMI does not implement this class.</span></span> <span data-ttu-id="0d179-152">針對衍生自 **CIM \_ 產品** 的 WMI 類別，請參閱 [Win32 類別](win32-provider.md)。</span><span class="sxs-lookup"><span data-stu-id="0d179-152">For WMI classes that are derived from **CIM\_Product**, see [Win32 Classes](win32-provider.md).</span></span>

<span data-ttu-id="0d179-153">此檔衍生自 DMTF 所發佈的 CIM 類別描述。</span><span class="sxs-lookup"><span data-stu-id="0d179-153">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="0d179-154">Microsoft 可能已進行變更，以更正次要錯誤、符合 Microsoft SDK 檔標準，或提供詳細資訊。</span><span class="sxs-lookup"><span data-stu-id="0d179-154">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="0d179-155">規格需求</span><span class="sxs-lookup"><span data-stu-id="0d179-155">Requirements</span></span>



| <span data-ttu-id="0d179-156">需求</span><span class="sxs-lookup"><span data-stu-id="0d179-156">Requirement</span></span> | <span data-ttu-id="0d179-157">值</span><span class="sxs-lookup"><span data-stu-id="0d179-157">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="0d179-158">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="0d179-158">Minimum supported client</span></span><br/> | <span data-ttu-id="0d179-159">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="0d179-159">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="0d179-160">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="0d179-160">Minimum supported server</span></span><br/> | <span data-ttu-id="0d179-161">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="0d179-161">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="0d179-162">命名空間</span><span class="sxs-lookup"><span data-stu-id="0d179-162">Namespace</span></span><br/>                | <span data-ttu-id="0d179-163">根 \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="0d179-163">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="0d179-164">MOF</span><span class="sxs-lookup"><span data-stu-id="0d179-164">MOF</span></span><br/>                      | <dl> <span data-ttu-id="0d179-165"><dt>CIMWin32 mof</dt></span><span class="sxs-lookup"><span data-stu-id="0d179-165"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="0d179-166">DLL</span><span class="sxs-lookup"><span data-stu-id="0d179-166">DLL</span></span><br/>                      | <dl> <span data-ttu-id="0d179-167"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0d179-167"><dt>CIMWin32.dll</dt></span></span> </dl> |



 

