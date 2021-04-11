---
description: 描述相關聯 Msvm ExternalEthernetPort 的功能 \_ 。
ms.assetid: 63731b62-b1c7-4dd9-b906-03225bbc3154
title: Msvm_ExternalEthernetPortCapabilities 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ExternalEthernetPortCapabilities
- Msvm_ExternalEthernetPortCapabilities.InstanceID
- Msvm_ExternalEthernetPortCapabilities.Caption
- Msvm_ExternalEthernetPortCapabilities.Description
- Msvm_ExternalEthernetPortCapabilities.ElementName
- Msvm_ExternalEthernetPortCapabilities.IOVSupport
- Msvm_ExternalEthernetPortCapabilities.IOVSupportReasons
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 748b207151fb1d11b013af7c736de52bbe5bec8b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103848204"
---
# <a name="msvm_externalethernetportcapabilities-class"></a><span data-ttu-id="d3b8d-103">Msvm \_ ExternalEthernetPortCapabilities 類別</span><span class="sxs-lookup"><span data-stu-id="d3b8d-103">Msvm\_ExternalEthernetPortCapabilities class</span></span>

<span data-ttu-id="d3b8d-104">描述相關聯 [**Msvm \_ ExternalEthernetPort**](msvm-externalethernetport.md)的功能。</span><span class="sxs-lookup"><span data-stu-id="d3b8d-104">Describes the capabilities of the associated [**Msvm\_ExternalEthernetPort**](msvm-externalethernetport.md).</span></span>

<span data-ttu-id="d3b8d-105">下列語法已簡化受控物件格式 (MOF) 程式碼，並且包含所有繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="d3b8d-105">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="d3b8d-106">語法</span><span class="sxs-lookup"><span data-stu-id="d3b8d-106">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_ExternalEthernetPortCapabilities : CIM_Capabilities
{
  string  InstanceID;
  string  Caption = "Ethernet Port Capabilities";
  string  Description = "Describes the capabilities of the Microsoft External Ethernet Port";
  string  ElementName = "Ethernet Port Capabilities";
  boolean IOVSupport;
  string  IOVSupportReasons[];
};
```

## <a name="members"></a><span data-ttu-id="d3b8d-107">成員</span><span class="sxs-lookup"><span data-stu-id="d3b8d-107">Members</span></span>

<span data-ttu-id="d3b8d-108">**Msvm \_ ExternalEthernetPortCapabilities** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="d3b8d-108">The **Msvm\_ExternalEthernetPortCapabilities** class has these types of members:</span></span>

-   [<span data-ttu-id="d3b8d-109">屬性</span><span class="sxs-lookup"><span data-stu-id="d3b8d-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="d3b8d-110">屬性</span><span class="sxs-lookup"><span data-stu-id="d3b8d-110">Properties</span></span>

<span data-ttu-id="d3b8d-111">**Msvm \_ ExternalEthernetPortCapabilities** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="d3b8d-111">The **Msvm\_ExternalEthernetPortCapabilities** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="d3b8d-112">**標題**</span><span class="sxs-lookup"><span data-stu-id="d3b8d-112">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d3b8d-113">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="d3b8d-113">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d3b8d-114">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="d3b8d-114">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d3b8d-115">物件的簡短描述。</span><span class="sxs-lookup"><span data-stu-id="d3b8d-115">A short description of the object.</span></span> <span data-ttu-id="d3b8d-116">這個屬性繼承自 [**CIM \_ ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)，一律設定為「乙太網路埠功能」。</span><span class="sxs-lookup"><span data-stu-id="d3b8d-116">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement), and it is always set to "Ethernet Port Capabilities".</span></span>

</dd> <dt>

<span data-ttu-id="d3b8d-117">**說明**</span><span class="sxs-lookup"><span data-stu-id="d3b8d-117">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d3b8d-118">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="d3b8d-118">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d3b8d-119">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="d3b8d-119">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d3b8d-120">對物件的描述。</span><span class="sxs-lookup"><span data-stu-id="d3b8d-120">A description of the object.</span></span> <span data-ttu-id="d3b8d-121">這個屬性繼承自 [**CIM \_ ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)，一律設定為「描述 Microsoft External Ethernet 埠的功能」。</span><span class="sxs-lookup"><span data-stu-id="d3b8d-121">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement), and it is always set to "Describes the capabilities of the Microsoft External Ethernet Port".</span></span>

</dd> <dt>

<span data-ttu-id="d3b8d-122">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="d3b8d-122">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d3b8d-123">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="d3b8d-123">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d3b8d-124">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="d3b8d-124">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d3b8d-125">物件的顯示名稱。</span><span class="sxs-lookup"><span data-stu-id="d3b8d-125">A display name for the object.</span></span> <span data-ttu-id="d3b8d-126">這個屬性繼承自 [**CIM \_ ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)，一律設定為「乙太網路埠功能」。</span><span class="sxs-lookup"><span data-stu-id="d3b8d-126">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement), and it is always set to "Ethernet Port Capabilities".</span></span>

</dd> <dt>

<span data-ttu-id="d3b8d-127">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="d3b8d-127">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d3b8d-128">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="d3b8d-128">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d3b8d-129">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="d3b8d-129">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d3b8d-130">限定詞：索引 **鍵**</span><span class="sxs-lookup"><span data-stu-id="d3b8d-130">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="d3b8d-131">唯一識別此類別的實例。</span><span class="sxs-lookup"><span data-stu-id="d3b8d-131">Uniquely identifies an instance of this class.</span></span> <span data-ttu-id="d3b8d-132">這個屬性繼承自 [**CIM \_ ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)。</span><span class="sxs-lookup"><span data-stu-id="d3b8d-132">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="d3b8d-133">**IOVSupport**</span><span class="sxs-lookup"><span data-stu-id="d3b8d-133">**IOVSupport**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d3b8d-134">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="d3b8d-134">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="d3b8d-135">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="d3b8d-135">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d3b8d-136">布林值，指出網路介面卡是否支援 i/o 虛擬化 (的) 。</span><span class="sxs-lookup"><span data-stu-id="d3b8d-136">A boolean value that indicates whether I/O virtualization (IOV) is supported by the network adapter.</span></span> <span data-ttu-id="d3b8d-137">如果該值為 **True**，則網路介面卡支援 sr-iov，而且 **IOVSupportReasons** 屬性將會是空的。</span><span class="sxs-lookup"><span data-stu-id="d3b8d-137">If the value is **True**, then IOV is supported by the network adapter and the **IOVSupportReasons** property will be empty.</span></span> <span data-ttu-id="d3b8d-138">否則， **IOVSupportReasons** 屬性將會有無法支援 sr-iov 的原因。</span><span class="sxs-lookup"><span data-stu-id="d3b8d-138">Otherwise the **IOVSupportReasons** property will have the reasons why IOV cannot be supported.</span></span>

</dd> <dt>

<span data-ttu-id="d3b8d-139">**IOVSupportReasons**</span><span class="sxs-lookup"><span data-stu-id="d3b8d-139">**IOVSupportReasons**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d3b8d-140">資料類型： **字串** 陣列</span><span class="sxs-lookup"><span data-stu-id="d3b8d-140">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="d3b8d-141">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="d3b8d-141">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d3b8d-142">字串陣列，指出不支援 SR-IOV 的可能原因。</span><span class="sxs-lookup"><span data-stu-id="d3b8d-142">An array of strings that indicates the possible reasons why IOV is not supported.</span></span> <span data-ttu-id="d3b8d-143">如果 **IOVSupport** 的值為 **True**，此陣列將會是空的。</span><span class="sxs-lookup"><span data-stu-id="d3b8d-143">If the value of **IOVSupport** is **True**, this array will be empty.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="d3b8d-144">規格需求</span><span class="sxs-lookup"><span data-stu-id="d3b8d-144">Requirements</span></span>



| <span data-ttu-id="d3b8d-145">需求</span><span class="sxs-lookup"><span data-stu-id="d3b8d-145">Requirement</span></span> | <span data-ttu-id="d3b8d-146">值</span><span class="sxs-lookup"><span data-stu-id="d3b8d-146">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d3b8d-147">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="d3b8d-147">Minimum supported client</span></span><br/> | <span data-ttu-id="d3b8d-148">\[僅 Windows 8 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="d3b8d-148">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="d3b8d-149">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="d3b8d-149">Minimum supported server</span></span><br/> | <span data-ttu-id="d3b8d-150">僅限 Windows Server 2012 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="d3b8d-150">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="d3b8d-151">命名空間</span><span class="sxs-lookup"><span data-stu-id="d3b8d-151">Namespace</span></span><br/>                | <span data-ttu-id="d3b8d-152">根 \\ 虛擬化 \\ V2</span><span class="sxs-lookup"><span data-stu-id="d3b8d-152">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="d3b8d-153">MOF</span><span class="sxs-lookup"><span data-stu-id="d3b8d-153">MOF</span></span><br/>                      | <dl> <span data-ttu-id="d3b8d-154"><dt>WindowsVirtualization。</dt></span><span class="sxs-lookup"><span data-stu-id="d3b8d-154"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="d3b8d-155">DLL</span><span class="sxs-lookup"><span data-stu-id="d3b8d-155">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d3b8d-156"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="d3b8d-156"><dt>Vmms.exe</dt></span></span> </dl>                     |



 

