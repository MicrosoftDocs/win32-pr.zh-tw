---
description: 描述相關聯之 CIM EnabledLogicalElement 物件屬性的限制 \_ 。
ms.assetid: debce40c-9a0e-43a7-88fa-9336afd52e17
title: CIM_EnabledLogicalElementCapabilities 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_EnabledLogicalElementCapabilities
- CIM_EnabledLogicalElementCapabilities.ElementNameEditSupported
- CIM_EnabledLogicalElementCapabilities.MaxElementNameLen
- CIM_EnabledLogicalElementCapabilities.RequestedStatesSupported
- CIM_EnabledLogicalElementCapabilities.ElementNameMask
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 35f400643e01821667c999342603fd402a3ae419
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106991868"
---
# <a name="cim_enabledlogicalelementcapabilities-class"></a><span data-ttu-id="205fa-103">CIM \_ EnabledLogicalElementCapabilities 類別</span><span class="sxs-lookup"><span data-stu-id="205fa-103">CIM\_EnabledLogicalElementCapabilities class</span></span>

<span data-ttu-id="205fa-104">描述相關聯之 [**CIM \_ EnabledLogicalElement**](cim-enabledlogicalelement.md) 物件屬性的限制。</span><span class="sxs-lookup"><span data-stu-id="205fa-104">Describes the restrictions on the properties of an associated [**CIM\_EnabledLogicalElement**](cim-enabledlogicalelement.md) object.</span></span>

## <a name="syntax"></a><span data-ttu-id="205fa-105">語法</span><span class="sxs-lookup"><span data-stu-id="205fa-105">Syntax</span></span>

``` syntax
[Abstract, Version("2.22.0"), UMLPackagePath("CIM::Core::Capabilities"), AMENDMENT]
class CIM_EnabledLogicalElementCapabilities : CIM_Capabilities
{
  boolean ElementNameEditSupported;
  uint16  MaxElementNameLen;
  uint16  RequestedStatesSupported[];
  string  ElementNameMask;
};
```

## <a name="members"></a><span data-ttu-id="205fa-106">成員</span><span class="sxs-lookup"><span data-stu-id="205fa-106">Members</span></span>

<span data-ttu-id="205fa-107">**CIM \_ EnabledLogicalElementCapabilities** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="205fa-107">The **CIM\_EnabledLogicalElementCapabilities** class has these types of members:</span></span>

-   [<span data-ttu-id="205fa-108">屬性</span><span class="sxs-lookup"><span data-stu-id="205fa-108">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="205fa-109">屬性</span><span class="sxs-lookup"><span data-stu-id="205fa-109">Properties</span></span>

<span data-ttu-id="205fa-110">**CIM \_ EnabledLogicalElementCapabilities** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="205fa-110">The **CIM\_EnabledLogicalElementCapabilities** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="205fa-111">**ElementNameEditSupported**</span><span class="sxs-lookup"><span data-stu-id="205fa-111">**ElementNameEditSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="205fa-112">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="205fa-112">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="205fa-113">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="205fa-113">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="205fa-114">限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "FC-SWAPI。INCITS-T11 \| SWAPI \_ UNIT \_ CONFIG \_ CAPS \_ T \| EditName ") ， [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ ManagedElement**](cim-managedelement.md)。**ElementName**") </span><span class="sxs-lookup"><span data-stu-id="205fa-114">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("FC-SWAPI.INCITS-T11\|SWAPI\_UNIT\_CONFIG\_CAPS\_T\|EditName"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_ManagedElement**](cim-managedelement.md).**ElementName**")</span></span>
</dt> </dl>

<span data-ttu-id="205fa-115">如果已啟用的邏輯元素的 **ElementName** 屬性可以修改，則 **為 true** ;否則 **為 false**。</span><span class="sxs-lookup"><span data-stu-id="205fa-115">**true** if the **ElementName** property of the enabled logical element can be modified; otherwise, **false**.</span></span>

</dd> <dt>

<span data-ttu-id="205fa-116">**ElementNameMask**</span><span class="sxs-lookup"><span data-stu-id="205fa-116">**ElementNameMask**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="205fa-117">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="205fa-117">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="205fa-118">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="205fa-118">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="205fa-119">限定詞： [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ( "**CIM \_ EnabledLogicalElementCapabilities**.**MaxElementNameLen**") </span><span class="sxs-lookup"><span data-stu-id="205fa-119">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_EnabledLogicalElementCapabilities**.**MaxElementNameLen**")</span></span>
</dt> </dl>

<span data-ttu-id="205fa-120">正則運算式，指出 enable 邏輯專案之 **ElementName** 屬性的限制。</span><span class="sxs-lookup"><span data-stu-id="205fa-120">A regular expression that indicates the restrictions on the **ElementName** property of the enable logical element.</span></span> <span data-ttu-id="205fa-121">See *DMTF standard ABNF with the Management Profile Specification Usage Guide*, appendix C for the permitted syntax.</span><span class="sxs-lookup"><span data-stu-id="205fa-121">See *DMTF standard ABNF with the Management Profile Specification Usage Guide*, appendix C for the permitted syntax.</span></span>

> [!Note]  
> <span data-ttu-id="205fa-122">如果這個屬性和 enable 邏輯元素的 **ElementNameMask** 屬性描述 **ElementName** 的最大長度，則會使用較小的值。</span><span class="sxs-lookup"><span data-stu-id="205fa-122">If this property and the **ElementNameMask** property of the enable logical element describe the maximum length of **ElementName**, the smaller value is used.</span></span>

 

</dd> <dt>

<span data-ttu-id="205fa-123">**MaxElementNameLen**</span><span class="sxs-lookup"><span data-stu-id="205fa-123">**MaxElementNameLen**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="205fa-124">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="205fa-124">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="205fa-125">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="205fa-125">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="205fa-126">限定詞： [**int32.maxvalue**](/windows/desktop/WmiSdk/standard-qualifiers) (256) ， [**MAPPINGSTRINGS**](/windows/desktop/WmiSdk/standard-qualifiers) ( "FC-SWAPI。INCITS-T11 \| SWAPI \_ UNIT \_ CONFIG \_ CAPS \_ T \| MaxNameChars ") ， [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) (" cim \_ FCSwitchCapabilities. ElementNameEditSupported "，"**cim \_ EnabledLogicalElementCapabilities**.**ElementNameMask**") </span><span class="sxs-lookup"><span data-stu-id="205fa-126">Qualifiers: [**MaxValue**](/windows/desktop/WmiSdk/standard-qualifiers) (256), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("FC-SWAPI.INCITS-T11\|SWAPI\_UNIT\_CONFIG\_CAPS\_T\|MaxNameChars"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("CIM\_FCSwitchCapabilities.ElementNameEditSupported", "**CIM\_EnabledLogicalElementCapabilities**.**ElementNameMask**")</span></span>
</dt> </dl>

<span data-ttu-id="205fa-127">已啟用之邏輯元素的 **ElementName** 屬性支援的最大長度。</span><span class="sxs-lookup"><span data-stu-id="205fa-127">The maximum supported length of the **ElementName** property of the enabled logical element.</span></span>

</dd> <dt>

<span data-ttu-id="205fa-128">**RequestedStatesSupported**</span><span class="sxs-lookup"><span data-stu-id="205fa-128">**RequestedStatesSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="205fa-129">資料類型： **uint16** 陣列</span><span class="sxs-lookup"><span data-stu-id="205fa-129">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="205fa-130">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="205fa-130">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="205fa-131">限定詞： [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ( "[**CIM \_ EnabledLogicalElement**](cim-enabledlogicalelement.md).**RequestStateChange**」 ) </span><span class="sxs-lookup"><span data-stu-id="205fa-131">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_EnabledLogicalElement**](cim-enabledlogicalelement.md).**RequestStateChange**")</span></span>
</dt> </dl>

<span data-ttu-id="205fa-132">可由 [**RequestStateChange**](cim-enabledlogicalelement-requeststatechange.md) 方法在啟用的邏輯元素上要求的可能狀態。</span><span class="sxs-lookup"><span data-stu-id="205fa-132">The possible states that can be requested on the enabled logical element by the [**RequestStateChange**](cim-enabledlogicalelement-requeststatechange.md) method.</span></span>

<dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="205fa-133">**已啟用** (2) </span><span class="sxs-lookup"><span data-stu-id="205fa-133">**Enabled** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="205fa-134">**停用** (3) </span><span class="sxs-lookup"><span data-stu-id="205fa-134">**Disabled** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Shut_Down"></span><span id="shut_down"></span><span id="SHUT_DOWN"></span>

<span data-ttu-id="205fa-135">**關機** (4) </span><span class="sxs-lookup"><span data-stu-id="205fa-135">**Shut Down** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Offline"></span><span id="offline"></span><span id="OFFLINE"></span>

<span data-ttu-id="205fa-136">**離線** (6) </span><span class="sxs-lookup"><span data-stu-id="205fa-136">**Offline** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Test"></span><span id="test"></span><span id="TEST"></span>

<span data-ttu-id="205fa-137">**測試** (7) </span><span class="sxs-lookup"><span data-stu-id="205fa-137">**Test** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Defer"></span><span id="defer"></span><span id="DEFER"></span>

<span data-ttu-id="205fa-138">**延** 後 (8) </span><span class="sxs-lookup"><span data-stu-id="205fa-138">**Defer** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Quiesce"></span><span id="quiesce"></span><span id="QUIESCE"></span>

<span data-ttu-id="205fa-139">**靜止** (9) </span><span class="sxs-lookup"><span data-stu-id="205fa-139">**Quiesce** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="Reboot"></span><span id="reboot"></span><span id="REBOOT"></span>

<span data-ttu-id="205fa-140">**重新開機** (10) </span><span class="sxs-lookup"><span data-stu-id="205fa-140">**Reboot** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="Reset"></span><span id="reset"></span><span id="RESET"></span>

<span data-ttu-id="205fa-141">**重設** (11) </span><span class="sxs-lookup"><span data-stu-id="205fa-141">**Reset** (11)</span></span>


<span data-ttu-id="205fa-142"></dt> <dd></dd> </dl>

</dd> </dl></span><span class="sxs-lookup"><span data-stu-id="205fa-142"></dt> <dd></dd> </dl>

</dd> </dl></span></span>

## <a name="requirements"></a><span data-ttu-id="205fa-143">規格需求</span><span class="sxs-lookup"><span data-stu-id="205fa-143">Requirements</span></span>



| <span data-ttu-id="205fa-144">需求</span><span class="sxs-lookup"><span data-stu-id="205fa-144">Requirement</span></span> | <span data-ttu-id="205fa-145">值</span><span class="sxs-lookup"><span data-stu-id="205fa-145">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="205fa-146">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="205fa-146">Minimum supported client</span></span><br/> | <span data-ttu-id="205fa-147">Windows 8</span><span class="sxs-lookup"><span data-stu-id="205fa-147">Windows 8</span></span><br/>                                                                                    |
| <span data-ttu-id="205fa-148">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="205fa-148">Minimum supported server</span></span><br/> | <span data-ttu-id="205fa-149">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="205fa-149">Windows Server 2012</span></span><br/>                                                                          |
| <span data-ttu-id="205fa-150">命名空間</span><span class="sxs-lookup"><span data-stu-id="205fa-150">Namespace</span></span><br/>                | <span data-ttu-id="205fa-151">根 \\ 虛擬化 \\ v2</span><span class="sxs-lookup"><span data-stu-id="205fa-151">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="205fa-152">MOF</span><span class="sxs-lookup"><span data-stu-id="205fa-152">MOF</span></span><br/>                      | <dl> <span data-ttu-id="205fa-153"><dt>WindowsVirtualization。</dt></span><span class="sxs-lookup"><span data-stu-id="205fa-153"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="205fa-154">DLL</span><span class="sxs-lookup"><span data-stu-id="205fa-154">DLL</span></span><br/>                      | <dl> <span data-ttu-id="205fa-155"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="205fa-155"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="205fa-156">另請參閱</span><span class="sxs-lookup"><span data-stu-id="205fa-156">See also</span></span>

<dl> <dt>

[<span data-ttu-id="205fa-157">**CIM \_ 功能**</span><span class="sxs-lookup"><span data-stu-id="205fa-157">**CIM\_Capabilities**</span></span>](cim-capabilities.md)
</dt> </dl>

 

