---
description: 代表產品。 這包括此電腦系統上所使用的軟體和硬體。
ms.assetid: 6241e703-4ce9-435f-bf36-4388e38a3ea5
ms.tgt_platform: multiple
title: Win32_ComputerSystemProduct 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_ComputerSystemProduct
- Win32_ComputerSystemProduct.Caption
- Win32_ComputerSystemProduct.Description
- Win32_ComputerSystemProduct.IdentifyingNumber
- Win32_ComputerSystemProduct.Name
- Win32_ComputerSystemProduct.SKUNumber
- Win32_ComputerSystemProduct.Vendor
- Win32_ComputerSystemProduct.Version
- Win32_ComputerSystemProduct.UUID
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 8cab3dc8679c606076eca2f5cf704867aa9833c9
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104110341"
---
# <a name="win32_computersystemproduct-class"></a><span data-ttu-id="15815-104">Win32 \_ ComputerSystemProduct 類別</span><span class="sxs-lookup"><span data-stu-id="15815-104">Win32\_ComputerSystemProduct class</span></span>

<span data-ttu-id="15815-105">**Win32 \_ ComputerSystemProduct** [WMI 類別](/windows/desktop/WmiSdk/retrieving-a-class)代表產品。</span><span class="sxs-lookup"><span data-stu-id="15815-105">The **Win32\_ComputerSystemProduct** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) represents a product.</span></span> <span data-ttu-id="15815-106">這包括此電腦系統上所使用的軟體和硬體。</span><span class="sxs-lookup"><span data-stu-id="15815-106">This includes software and hardware used on this computer system.</span></span>

<span data-ttu-id="15815-107">下列語法已經過受管理物件格式 (MOF) 程式碼簡化，並包含所有已繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="15815-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="15815-108">屬性會依字母順序列出，而不是依 MOF 順序列出。</span><span class="sxs-lookup"><span data-stu-id="15815-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="15815-109">語法</span><span class="sxs-lookup"><span data-stu-id="15815-109">Syntax</span></span>

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{FAF76B96-798C-11D2-AAD1-006008C78BC7}"), AMENDMENT]
class Win32_ComputerSystemProduct : CIM_Product
{
  string Caption;
  string Description;
  string IdentifyingNumber;
  string Name;
  string SKUNumber;
  string Vendor;
  string Version;
  string UUID;
};
```

## <a name="members"></a><span data-ttu-id="15815-110">成員</span><span class="sxs-lookup"><span data-stu-id="15815-110">Members</span></span>

<span data-ttu-id="15815-111">**Win32 \_ ComputerSystemProduct** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="15815-111">The **Win32\_ComputerSystemProduct** class has these types of members:</span></span>

-   [<span data-ttu-id="15815-112">屬性</span><span class="sxs-lookup"><span data-stu-id="15815-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="15815-113">屬性</span><span class="sxs-lookup"><span data-stu-id="15815-113">Properties</span></span>

<span data-ttu-id="15815-114">**Win32 \_ ComputerSystemProduct** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="15815-114">The **Win32\_ComputerSystemProduct** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="15815-115">**標題**</span><span class="sxs-lookup"><span data-stu-id="15815-115">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="15815-116">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="15815-116">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="15815-117">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="15815-117">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="15815-118">限定詞： [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64) </span><span class="sxs-lookup"><span data-stu-id="15815-118">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="15815-119">產品的簡短文字描述。</span><span class="sxs-lookup"><span data-stu-id="15815-119">Short textual description for the product.</span></span>

<span data-ttu-id="15815-120">這個屬性繼承自 [**CIM \_ 產品**](cim-product.md)。</span><span class="sxs-lookup"><span data-stu-id="15815-120">This property is inherited from [**CIM\_Product**](cim-product.md).</span></span>

</dd> <dt>

<span data-ttu-id="15815-121">**說明**</span><span class="sxs-lookup"><span data-stu-id="15815-121">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="15815-122">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="15815-122">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="15815-123">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="15815-123">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="15815-124">產品的文字描述。</span><span class="sxs-lookup"><span data-stu-id="15815-124">Textual description of the product.</span></span>

<span data-ttu-id="15815-125">這個屬性繼承自 [**CIM \_ 產品**](cim-product.md)。</span><span class="sxs-lookup"><span data-stu-id="15815-125">This property is inherited from [**CIM\_Product**](cim-product.md).</span></span>

</dd> <dt>

<span data-ttu-id="15815-126">**IdentifyingNumber**</span><span class="sxs-lookup"><span data-stu-id="15815-126">**IdentifyingNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="15815-127">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="15815-127">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="15815-128">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="15815-128">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="15815-129">限定詞： [**Key**](/windows/desktop/WmiSdk/key-qualifier)、 [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64) 、 [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "MIF。DMTF \| 元件 \| 001.4 ") </span><span class="sxs-lookup"><span data-stu-id="15815-129">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.4")</span></span>
</dt> </dl>

<span data-ttu-id="15815-130">產品識別，例如軟體序號、硬體晶片上的骰子號碼，或) 專案編號的非商業性產品 (。</span><span class="sxs-lookup"><span data-stu-id="15815-130">Product identification, such as a serial number on software, a die number on a hardware chip, or (for noncommercial products) a project number.</span></span>

<span data-ttu-id="15815-131">這個屬性繼承自 [**CIM \_ 產品**](cim-product.md)。</span><span class="sxs-lookup"><span data-stu-id="15815-131">This property is inherited from [**CIM\_Product**](cim-product.md).</span></span>

</dd> <dt>

<span data-ttu-id="15815-132">**名稱**</span><span class="sxs-lookup"><span data-stu-id="15815-132">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="15815-133">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="15815-133">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="15815-134">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="15815-134">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="15815-135">限定詞： [**Key**](/windows/desktop/WmiSdk/key-qualifier)、 [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256) 、 [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "MIF。DMTF \| 元件 \| 001.2 ") </span><span class="sxs-lookup"><span data-stu-id="15815-135">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.2")</span></span>
</dt> </dl>

<span data-ttu-id="15815-136">常用的產品名稱。</span><span class="sxs-lookup"><span data-stu-id="15815-136">Commonly used product name.</span></span>

<span data-ttu-id="15815-137">這個屬性繼承自 [**CIM \_ 產品**](cim-product.md)。</span><span class="sxs-lookup"><span data-stu-id="15815-137">This property is inherited from [**CIM\_Product**](cim-product.md).</span></span>

</dd> <dt>

<span data-ttu-id="15815-138">**SKUNumber**</span><span class="sxs-lookup"><span data-stu-id="15815-138">**SKUNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="15815-139">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="15815-139">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="15815-140">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="15815-140">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="15815-141">限定詞： [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64) </span><span class="sxs-lookup"><span data-stu-id="15815-141">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="15815-142">產品的庫存單位 (SKU) 資訊。</span><span class="sxs-lookup"><span data-stu-id="15815-142">Product's stock-keeping unit (SKU) information.</span></span>

<span data-ttu-id="15815-143">這個屬性繼承自 [**CIM \_ 產品**](cim-product.md)。</span><span class="sxs-lookup"><span data-stu-id="15815-143">This property is inherited from [**CIM\_Product**](cim-product.md).</span></span>

</dd> <dt>

<span data-ttu-id="15815-144">**Uuid**</span><span class="sxs-lookup"><span data-stu-id="15815-144">**UUID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="15815-145">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="15815-145">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="15815-146">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="15815-146">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="15815-147">限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "SMBIOS \| Type 1 \| UUID" ) </span><span class="sxs-lookup"><span data-stu-id="15815-147">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("SMBIOS\|Type 1\|UUID")</span></span>
</dt> </dl>

<span data-ttu-id="15815-148">此產品 (UUID) 的通用唯一識別碼。</span><span class="sxs-lookup"><span data-stu-id="15815-148">Universally unique identifier (UUID) for this product.</span></span> <span data-ttu-id="15815-149">UUID 是128位的識別碼，保證與其他產生的 Uuid 不同。</span><span class="sxs-lookup"><span data-stu-id="15815-149">A UUID is a 128-bit identifier that is guaranteed to be different from other generated UUIDs.</span></span> <span data-ttu-id="15815-150">如果 UUID 無法使用，則會使用所有零的 UUID。</span><span class="sxs-lookup"><span data-stu-id="15815-150">If a UUID is not available, a UUID of all zeros is used.</span></span>

<span data-ttu-id="15815-151">此值來自 SMBIOS 資訊中 **系統資訊** 結構的 **UUID** 成員。</span><span class="sxs-lookup"><span data-stu-id="15815-151">This value comes from the **UUID** member of the **System Information** structure in the SMBIOS information.</span></span>

</dd> <dt>

<span data-ttu-id="15815-152">**廠商**</span><span class="sxs-lookup"><span data-stu-id="15815-152">**Vendor**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="15815-153">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="15815-153">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="15815-154">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="15815-154">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="15815-155">限定詞： [**CIM \_ 金鑰**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)、 [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256) 、 [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) (」 MIF。DMTF \| 元件 \| 001.1 ") </span><span class="sxs-lookup"><span data-stu-id="15815-155">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.1")</span></span>
</dt> </dl>

<span data-ttu-id="15815-156">產品供應商的名稱，或銷售產品的實體 (製造商、轉售商、OEM 等) 。</span><span class="sxs-lookup"><span data-stu-id="15815-156">Name of the product's supplier, or the entity selling the product (the manufacturer, reseller, OEM, and so on).</span></span>

<span data-ttu-id="15815-157">這個屬性繼承自 [**CIM \_ 產品**](cim-product.md)。</span><span class="sxs-lookup"><span data-stu-id="15815-157">This property is inherited from [**CIM\_Product**](cim-product.md).</span></span>

</dd> <dt>

<span data-ttu-id="15815-158">**版本**</span><span class="sxs-lookup"><span data-stu-id="15815-158">**Version**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="15815-159">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="15815-159">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="15815-160">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="15815-160">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="15815-161">限定詞： [**Key**](/windows/desktop/WmiSdk/key-qualifier)、 [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64) 、 [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "MIF。DMTF \| 元件 \| 001.3 ") </span><span class="sxs-lookup"><span data-stu-id="15815-161">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.3")</span></span>
</dt> </dl>

<span data-ttu-id="15815-162">產品版本資訊。</span><span class="sxs-lookup"><span data-stu-id="15815-162">Product version information.</span></span>

<span data-ttu-id="15815-163">這個屬性繼承自 [**CIM \_ 產品**](cim-product.md)。</span><span class="sxs-lookup"><span data-stu-id="15815-163">This property is inherited from [**CIM\_Product**](cim-product.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="15815-164">備註</span><span class="sxs-lookup"><span data-stu-id="15815-164">Remarks</span></span>

<span data-ttu-id="15815-165">**Win32 \_ ComputerSystemProduct** 類別衍生自 [**CIM \_ 產品**](cim-product.md)。</span><span class="sxs-lookup"><span data-stu-id="15815-165">The **Win32\_ComputerSystemProduct** class is derived from [**CIM\_Product**](cim-product.md).</span></span>

## <a name="examples"></a><span data-ttu-id="15815-166">範例</span><span class="sxs-lookup"><span data-stu-id="15815-166">Examples</span></span>

<span data-ttu-id="15815-167">TechNet 資源庫上的 [Get-BrokenHardware.ps1](https://Gallery.TechNet.Microsoft.Com/dbb678f4-b95b-45c3-bc8b-2ae2d052448e) PowerShell 範例會使用 **Win32 \_ COMPUTERSYSTEMPRODUCT** ，以使用 WMI 抓取無法運作的硬體清單。</span><span class="sxs-lookup"><span data-stu-id="15815-167">The [Get-BrokenHardware.ps1](https://Gallery.TechNet.Microsoft.Com/dbb678f4-b95b-45c3-bc8b-2ae2d052448e) PowerShell sample on TechNet Gallery uses to **Win32\_ComputerSystemProduct** to retrieve a list of non-working hardware using WMI.</span></span>

## <a name="requirements"></a><span data-ttu-id="15815-168">規格需求</span><span class="sxs-lookup"><span data-stu-id="15815-168">Requirements</span></span>



| <span data-ttu-id="15815-169">需求</span><span class="sxs-lookup"><span data-stu-id="15815-169">Requirement</span></span> | <span data-ttu-id="15815-170">值</span><span class="sxs-lookup"><span data-stu-id="15815-170">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="15815-171">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="15815-171">Minimum supported client</span></span><br/> | <span data-ttu-id="15815-172">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="15815-172">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="15815-173">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="15815-173">Minimum supported server</span></span><br/> | <span data-ttu-id="15815-174">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="15815-174">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="15815-175">命名空間</span><span class="sxs-lookup"><span data-stu-id="15815-175">Namespace</span></span><br/>                | <span data-ttu-id="15815-176">根 \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="15815-176">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="15815-177">MOF</span><span class="sxs-lookup"><span data-stu-id="15815-177">MOF</span></span><br/>                      | <dl> <span data-ttu-id="15815-178"><dt>CIMWin32 mof</dt></span><span class="sxs-lookup"><span data-stu-id="15815-178"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="15815-179">DLL</span><span class="sxs-lookup"><span data-stu-id="15815-179">DLL</span></span><br/>                      | <dl> <span data-ttu-id="15815-180"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="15815-180"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="15815-181">另請參閱</span><span class="sxs-lookup"><span data-stu-id="15815-181">See also</span></span>

<dl> <dt>

[<span data-ttu-id="15815-182">**CIM \_ 產品**</span><span class="sxs-lookup"><span data-stu-id="15815-182">**CIM\_Product**</span></span>](cim-product.md)
</dt> <dt>

<span data-ttu-id="15815-183">[作業系統類別](/previous-versions//aa392727(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="15815-183">[Operating System Classes](/previous-versions//aa392727(v=vs.85))</span></span>
</dt> </dl>

 

