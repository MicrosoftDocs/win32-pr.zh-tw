---
description: 代表做為單一高階實體的一組元件。
ms.assetid: 784cee32-e0ae-4632-8dac-e5110513f5c9
title: 'CIM_System 類別 (Hyper-v 管理) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_System
- CIM_System.CreationClassName
- CIM_System.Name
- CIM_System.NameFormat
- CIM_System.PrimaryOwnerName
- CIM_System.PrimaryOwnerContact
- CIM_System.Roles
- CIM_System.OtherIdentifyingInfo
- CIM_System.IdentifyingDescriptions
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: a51e56ad3e8f91200fbe5bc7e09ac2f14c4ee232
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106974630"
---
# <a name="cim_system-class-hyper-v-management"></a><span data-ttu-id="f9c46-103">CIM_System 類別 (Hyper-v 管理) </span><span class="sxs-lookup"><span data-stu-id="f9c46-103">CIM_System class (Hyper-V management)</span></span>

<span data-ttu-id="f9c46-104">代表做為單一高階實體的一組元件。</span><span class="sxs-lookup"><span data-stu-id="f9c46-104">Represents a set of components that function as a single high-level entity.</span></span>

## <a name="syntax"></a><span data-ttu-id="f9c46-105">語法</span><span class="sxs-lookup"><span data-stu-id="f9c46-105">Syntax</span></span>

``` syntax
[Abstract, Version("2.15.0"), UMLPackagePath("CIM::Core::CoreElements"), AMENDMENT]
class CIM_System : CIM_EnabledLogicalElement
{
  string CreationClassName;
  string Name;
  string NameFormat;
  string PrimaryOwnerName;
  string PrimaryOwnerContact;
  string Roles[];
  string OtherIdentifyingInfo[];
  string IdentifyingDescriptions[];
};
```

## <a name="members"></a><span data-ttu-id="f9c46-106">成員</span><span class="sxs-lookup"><span data-stu-id="f9c46-106">Members</span></span>

<span data-ttu-id="f9c46-107">**CIM \_ 系統** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="f9c46-107">The **CIM\_System** class has these types of members:</span></span>

-   [<span data-ttu-id="f9c46-108">屬性</span><span class="sxs-lookup"><span data-stu-id="f9c46-108">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="f9c46-109">屬性</span><span class="sxs-lookup"><span data-stu-id="f9c46-109">Properties</span></span>

<span data-ttu-id="f9c46-110">**CIM \_ 系統** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="f9c46-110">The **CIM\_System** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="f9c46-111">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="f9c46-111">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f9c46-112">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="f9c46-112">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f9c46-113">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="f9c46-113">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f9c46-114">限定詞： [**Key**](/windows/desktop/WmiSdk/key-qualifier)、 [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256) </span><span class="sxs-lookup"><span data-stu-id="f9c46-114">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="f9c46-115">用來建立這個類別之實例的類別名稱。</span><span class="sxs-lookup"><span data-stu-id="f9c46-115">The class name used to create an instance of this class.</span></span> <span data-ttu-id="f9c46-116">**CreationClassName** 與這個類別的其他索引鍵屬性結合，可唯一識別此類別和其子類別的實例。</span><span class="sxs-lookup"><span data-stu-id="f9c46-116">**CreationClassName** is combined with other key properties of this class to uniquely identify instances of this class and its subclasses.</span></span>

</dd> <dt>

<span data-ttu-id="f9c46-117">**IdentifyingDescriptions**</span><span class="sxs-lookup"><span data-stu-id="f9c46-117">**IdentifyingDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f9c46-118">資料類型： **字串** 陣列</span><span class="sxs-lookup"><span data-stu-id="f9c46-118">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="f9c46-119">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="f9c46-119">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f9c46-120">限定詞： [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Indexed" ) ， [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ( "**CIM \_ System**.**OtherIdentifyingInfo**") </span><span class="sxs-lookup"><span data-stu-id="f9c46-120">Qualifiers: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_System**.**OtherIdentifyingInfo**")</span></span>
</dt> </dl>

<span data-ttu-id="f9c46-121">陣列，其中包含 **OtherIdentifyingInfo** 屬性中之值的描述。</span><span class="sxs-lookup"><span data-stu-id="f9c46-121">An array that contains descriptions of the values in the **OtherIdentifyingInfo** property.</span></span> <span data-ttu-id="f9c46-122">**IdentifyingDescriptions** 中的陣列專案會對應至 **IdentifyingDescriptions** 屬性中的專案。</span><span class="sxs-lookup"><span data-stu-id="f9c46-122">The array items in **IdentifyingDescriptions** correspond to the items in the **IdentifyingDescriptions** property.</span></span>

</dd> <dt>

<span data-ttu-id="f9c46-123">**名稱**</span><span class="sxs-lookup"><span data-stu-id="f9c46-123">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f9c46-124">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="f9c46-124">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f9c46-125">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="f9c46-125">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f9c46-126">限定詞： [**Key**](/windows/desktop/WmiSdk/key-qualifier)、 [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Name" ) 、 [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256) </span><span class="sxs-lookup"><span data-stu-id="f9c46-126">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name"), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="f9c46-127">此實例在企業環境中的索引鍵。</span><span class="sxs-lookup"><span data-stu-id="f9c46-127">The key of this instance in an enterprise environment.</span></span>

</dd> <dt>

<span data-ttu-id="f9c46-128">**NameFormat**</span><span class="sxs-lookup"><span data-stu-id="f9c46-128">**NameFormat**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f9c46-129">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="f9c46-129">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f9c46-130">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="f9c46-130">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f9c46-131">限定詞： [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64) </span><span class="sxs-lookup"><span data-stu-id="f9c46-131">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="f9c46-132">Name 屬性所使用的命名慣例，以確保 **名稱** 值是唯一的。</span><span class="sxs-lookup"><span data-stu-id="f9c46-132">The naming convention used by the Name property to ensure that **Name** values are unique.</span></span>

</dd> <dt>

<span data-ttu-id="f9c46-133">**OtherIdentifyingInfo**</span><span class="sxs-lookup"><span data-stu-id="f9c46-133">**OtherIdentifyingInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f9c46-134">資料類型： **字串** 陣列</span><span class="sxs-lookup"><span data-stu-id="f9c46-134">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="f9c46-135">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="f9c46-135">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f9c46-136">限定詞： [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Indexed" ) 、 [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256) 、 [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ( "**CIM \_ System**.**IdentifyingDescriptions**") </span><span class="sxs-lookup"><span data-stu-id="f9c46-136">Qualifiers: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed"), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_System**.**IdentifyingDescriptions**")</span></span>
</dt> </dl>

<span data-ttu-id="f9c46-137">陣列，其中包含可用來識別電腦系統的一組額外資料，除了系統名稱資訊之外。</span><span class="sxs-lookup"><span data-stu-id="f9c46-137">An array that contains a set of additional data, beyond system name information, that could be used to identify a computer system.</span></span>

</dd> <dt>

<span data-ttu-id="f9c46-138">**PrimaryOwnerContact**</span><span class="sxs-lookup"><span data-stu-id="f9c46-138">**PrimaryOwnerContact**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f9c46-139">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="f9c46-139">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f9c46-140">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="f9c46-140">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="f9c46-141">限定詞： [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256) ， [**MAPPINGSTRINGS**](/windows/desktop/WmiSdk/standard-qualifiers) (」 MIF。DMTF \| 一般資訊 \| 001.4 ") </span><span class="sxs-lookup"><span data-stu-id="f9c46-141">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|General Information\|001.4")</span></span>
</dt> </dl>

<span data-ttu-id="f9c46-142">提供如何達到主要系統擁有者的相關資訊 (例如電話號碼、電子郵件地址等) 。</span><span class="sxs-lookup"><span data-stu-id="f9c46-142">A string that provides information on how the primary system owner can be reached (for example, phone number, e-mail address, and so on).</span></span>

</dd> <dt>

<span data-ttu-id="f9c46-143">**PrimaryOwnerName**</span><span class="sxs-lookup"><span data-stu-id="f9c46-143">**PrimaryOwnerName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f9c46-144">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="f9c46-144">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f9c46-145">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="f9c46-145">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="f9c46-146">限定詞： [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64) ， [**MAPPINGSTRINGS**](/windows/desktop/WmiSdk/standard-qualifiers) (」 MIF。DMTF \| 一般資訊 \| 001.3 ") </span><span class="sxs-lookup"><span data-stu-id="f9c46-146">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|General Information\|001.3")</span></span>
</dt> </dl>

<span data-ttu-id="f9c46-147">系統主要使用者的名稱。</span><span class="sxs-lookup"><span data-stu-id="f9c46-147">The name of the primary user of the system.</span></span>

</dd> <dt>

<span data-ttu-id="f9c46-148">**角色**</span><span class="sxs-lookup"><span data-stu-id="f9c46-148">**Roles**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f9c46-149">資料類型： **字串** 陣列</span><span class="sxs-lookup"><span data-stu-id="f9c46-149">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="f9c46-150">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="f9c46-150">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="f9c46-151">陣列，其中包含系統在企業環境中所執行的角色。</span><span class="sxs-lookup"><span data-stu-id="f9c46-151">An array that contains the roles carried out by the system in an enterprise environment.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="f9c46-152">規格需求</span><span class="sxs-lookup"><span data-stu-id="f9c46-152">Requirements</span></span>



| <span data-ttu-id="f9c46-153">需求</span><span class="sxs-lookup"><span data-stu-id="f9c46-153">Requirement</span></span> | <span data-ttu-id="f9c46-154">值</span><span class="sxs-lookup"><span data-stu-id="f9c46-154">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f9c46-155">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="f9c46-155">Minimum supported client</span></span><br/> | <span data-ttu-id="f9c46-156">Windows 8</span><span class="sxs-lookup"><span data-stu-id="f9c46-156">Windows 8</span></span><br/>                                                                                    |
| <span data-ttu-id="f9c46-157">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="f9c46-157">Minimum supported server</span></span><br/> | <span data-ttu-id="f9c46-158">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="f9c46-158">Windows Server 2012</span></span><br/>                                                                          |
| <span data-ttu-id="f9c46-159">命名空間</span><span class="sxs-lookup"><span data-stu-id="f9c46-159">Namespace</span></span><br/>                | <span data-ttu-id="f9c46-160">根 \\ 虛擬化 \\ v2</span><span class="sxs-lookup"><span data-stu-id="f9c46-160">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="f9c46-161">MOF</span><span class="sxs-lookup"><span data-stu-id="f9c46-161">MOF</span></span><br/>                      | <dl> <span data-ttu-id="f9c46-162"><dt>WindowsVirtualization。</dt></span><span class="sxs-lookup"><span data-stu-id="f9c46-162"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="f9c46-163">DLL</span><span class="sxs-lookup"><span data-stu-id="f9c46-163">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f9c46-164"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="f9c46-164"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="f9c46-165">另請參閱</span><span class="sxs-lookup"><span data-stu-id="f9c46-165">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f9c46-166">**CIM \_ EnabledLogicalElement**</span><span class="sxs-lookup"><span data-stu-id="f9c46-166">**CIM\_EnabledLogicalElement**</span></span>](cim-enabledlogicalelement.md)
</dt> </dl>

 

