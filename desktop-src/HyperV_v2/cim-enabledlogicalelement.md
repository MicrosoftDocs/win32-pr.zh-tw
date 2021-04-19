---
description: 表示可以啟用和停用的邏輯元素。
ms.assetid: 52eed77e-f3f1-4489-8eff-a8ebebd5e1a8
title: CIM_EnabledLogicalElement 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_EnabledLogicalElement
- CIM_EnabledLogicalElement.EnabledState
- CIM_EnabledLogicalElement.OtherEnabledState
- CIM_EnabledLogicalElement.RequestedState
- CIM_EnabledLogicalElement.EnabledDefault
- CIM_EnabledLogicalElement.TimeOfLastStateChange
- CIM_EnabledLogicalElement.AvailableRequestedStates
- CIM_EnabledLogicalElement.TransitioningToState
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 9e2d7043653b219bc0d54ac7bee3393275dab673
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106974300"
---
# <a name="cim_enabledlogicalelement-class"></a><span data-ttu-id="f3c89-103">CIM \_ EnabledLogicalElement 類別</span><span class="sxs-lookup"><span data-stu-id="f3c89-103">CIM\_EnabledLogicalElement class</span></span>

<span data-ttu-id="f3c89-104">表示可以啟用和停用的邏輯元素。</span><span class="sxs-lookup"><span data-stu-id="f3c89-104">Represents a logical element that can be enabled and disabled.</span></span>

## <a name="syntax"></a><span data-ttu-id="f3c89-105">語法</span><span class="sxs-lookup"><span data-stu-id="f3c89-105">Syntax</span></span>

``` syntax
[Abstract, Version("2.22.0"), UMLPackagePath("CIM::Core::CoreElements"), AMENDMENT]
class CIM_EnabledLogicalElement : CIM_LogicalElement
{
  uint16   EnabledState = 5;
  string   OtherEnabledState;
  uint16   RequestedState = 12;
  uint16   EnabledDefault = 2;
  datetime TimeOfLastStateChange;
  uint16   AvailableRequestedStates[];
  uint16   TransitioningToState = 12;
};
```

## <a name="members"></a><span data-ttu-id="f3c89-106">成員</span><span class="sxs-lookup"><span data-stu-id="f3c89-106">Members</span></span>

<span data-ttu-id="f3c89-107">**CIM \_ EnabledLogicalElement** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="f3c89-107">The **CIM\_EnabledLogicalElement** class has these types of members:</span></span>

-   [<span data-ttu-id="f3c89-108">方法</span><span class="sxs-lookup"><span data-stu-id="f3c89-108">Methods</span></span>](#methods)
-   [<span data-ttu-id="f3c89-109">屬性</span><span class="sxs-lookup"><span data-stu-id="f3c89-109">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="f3c89-110">方法</span><span class="sxs-lookup"><span data-stu-id="f3c89-110">Methods</span></span>

<span data-ttu-id="f3c89-111">**CIM \_ EnabledLogicalElement** 類別具有這些方法。</span><span class="sxs-lookup"><span data-stu-id="f3c89-111">The **CIM\_EnabledLogicalElement** class has these methods.</span></span>



| <span data-ttu-id="f3c89-112">方法</span><span class="sxs-lookup"><span data-stu-id="f3c89-112">Method</span></span>                                                                     | <span data-ttu-id="f3c89-113">描述</span><span class="sxs-lookup"><span data-stu-id="f3c89-113">Description</span></span>                                                                          |
|:---------------------------------------------------------------------------|:-------------------------------------------------------------------------------------|
| [<span data-ttu-id="f3c89-114">**RequestStateChange**</span><span class="sxs-lookup"><span data-stu-id="f3c89-114">**RequestStateChange**</span></span>](cim-enabledlogicalelement-requeststatechange.md) | <span data-ttu-id="f3c89-115">要求將元素的狀態變更為指定的值。</span><span class="sxs-lookup"><span data-stu-id="f3c89-115">Requests that the state of the element be changed to the specified value.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="f3c89-116">屬性</span><span class="sxs-lookup"><span data-stu-id="f3c89-116">Properties</span></span>

<span data-ttu-id="f3c89-117">**CIM \_ EnabledLogicalElement** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="f3c89-117">The **CIM\_EnabledLogicalElement** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="f3c89-118">**AvailableRequestedStates**</span><span class="sxs-lookup"><span data-stu-id="f3c89-118">**AvailableRequestedStates**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f3c89-119">資料類型： **uint16** 陣列</span><span class="sxs-lookup"><span data-stu-id="f3c89-119">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="f3c89-120">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="f3c89-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f3c89-121">限定詞： [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ( "**CIM \_ EnabledLogicalElement**.**RequestStateChange**"，"[**CIM \_ EnabledLogicalElementCapabilities**](cim-enabledlogicalelementcapabilities.md)。**RequestedStatesSupported**") </span><span class="sxs-lookup"><span data-stu-id="f3c89-121">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_EnabledLogicalElement**.**RequestStateChange**", "[**CIM\_EnabledLogicalElementCapabilities**](cim-enabledlogicalelementcapabilities.md).**RequestedStatesSupported**")</span></span>
</dt> </dl>

<span data-ttu-id="f3c89-122">指出 [**RequestStateChange**](cim-enabledlogicalelement-requeststatechange.md)方法的 *RequestedState* 參數可能的值。</span><span class="sxs-lookup"><span data-stu-id="f3c89-122">Indicates the possible values for the *RequestedState* parameter of the [**RequestStateChange**](cim-enabledlogicalelement-requeststatechange.md) method.</span></span>

<span data-ttu-id="f3c89-123">列出的值必須是相關聯之 **CIM \_ EnabledLogicalElementCapabilities** 實例之 **RequestedStatesSupported** 屬性中所包含之值的子集。</span><span class="sxs-lookup"><span data-stu-id="f3c89-123">The listed values must be a subset of the values that are contained in the **RequestedStatesSupported** property of the associated **CIM\_EnabledLogicalElementCapabilities** instance.</span></span> <span data-ttu-id="f3c89-124">如果實值無法判斷元素目前狀態的可能值，則這個屬性為 **Null** 。</span><span class="sxs-lookup"><span data-stu-id="f3c89-124">This property is **NULL** if the implementation cannot determine the set of possible values for the current state of the element.</span></span>

<dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="f3c89-125">**已啟用** (2) </span><span class="sxs-lookup"><span data-stu-id="f3c89-125">**Enabled** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="f3c89-126">**停用** (3) </span><span class="sxs-lookup"><span data-stu-id="f3c89-126">**Disabled** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Shut_Down"></span><span id="shut_down"></span><span id="SHUT_DOWN"></span>

<span data-ttu-id="f3c89-127">**關機** (4) </span><span class="sxs-lookup"><span data-stu-id="f3c89-127">**Shut Down** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Offline"></span><span id="offline"></span><span id="OFFLINE"></span>

<span data-ttu-id="f3c89-128">**離線** (6) </span><span class="sxs-lookup"><span data-stu-id="f3c89-128">**Offline** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Test"></span><span id="test"></span><span id="TEST"></span>

<span data-ttu-id="f3c89-129">**測試** (7) </span><span class="sxs-lookup"><span data-stu-id="f3c89-129">**Test** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Defer"></span><span id="defer"></span><span id="DEFER"></span>

<span data-ttu-id="f3c89-130">**延** 後 (8) </span><span class="sxs-lookup"><span data-stu-id="f3c89-130">**Defer** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Quiesce"></span><span id="quiesce"></span><span id="QUIESCE"></span>

<span data-ttu-id="f3c89-131">**靜止** (9) </span><span class="sxs-lookup"><span data-stu-id="f3c89-131">**Quiesce** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="Reboot"></span><span id="reboot"></span><span id="REBOOT"></span>

<span data-ttu-id="f3c89-132">**重新開機** (10) </span><span class="sxs-lookup"><span data-stu-id="f3c89-132">**Reboot** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="Reset"></span><span id="reset"></span><span id="RESET"></span>

<span data-ttu-id="f3c89-133">**重設** (11) </span><span class="sxs-lookup"><span data-stu-id="f3c89-133">**Reset** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

<span data-ttu-id="f3c89-134">**DMTF 保留** ( .。。) </span><span class="sxs-lookup"><span data-stu-id="f3c89-134">**DMTF Reserved** (..)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="f3c89-135">**EnabledDefault**</span><span class="sxs-lookup"><span data-stu-id="f3c89-135">**EnabledDefault**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f3c89-136">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="f3c89-136">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="f3c89-137">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="f3c89-137">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="f3c89-138">指出專案的已啟用狀態之系統管理員的預設或啟動設定。</span><span class="sxs-lookup"><span data-stu-id="f3c89-138">Indicates an administrator's default or startup configuration for the enabled state of an element.</span></span> <span data-ttu-id="f3c89-139">預設值 **已啟用** (2) 。</span><span class="sxs-lookup"><span data-stu-id="f3c89-139">The default value **Enabled** (2).</span></span>

<dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="f3c89-140">**已啟用** (2) </span><span class="sxs-lookup"><span data-stu-id="f3c89-140">**Enabled** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="f3c89-141">**停用** (3) </span><span class="sxs-lookup"><span data-stu-id="f3c89-141">**Disabled** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="f3c89-142">**不適用** (5) </span><span class="sxs-lookup"><span data-stu-id="f3c89-142">**Not Applicable** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled_but_Offline"></span><span id="enabled_but_offline"></span><span id="ENABLED_BUT_OFFLINE"></span>

<span data-ttu-id="f3c89-143">**已啟用但離線** (6) </span><span class="sxs-lookup"><span data-stu-id="f3c89-143">**Enabled but Offline** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="No_Default"></span><span id="no_default"></span><span id="NO_DEFAULT"></span>

<span data-ttu-id="f3c89-144">**沒有預設** (7) </span><span class="sxs-lookup"><span data-stu-id="f3c89-144">**No Default** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Quiesce"></span><span id="quiesce"></span><span id="QUIESCE"></span>

<span data-ttu-id="f3c89-145">**靜止** (9) </span><span class="sxs-lookup"><span data-stu-id="f3c89-145">**Quiesce** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

<span data-ttu-id="f3c89-146">**DMTF 保留** ( .。。) </span><span class="sxs-lookup"><span data-stu-id="f3c89-146">**DMTF Reserved** (..)</span></span>


</dt> <dd></dd> <dt>

<span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>

<span data-ttu-id="f3c89-147">**廠商保留** (32768. 65535) </span><span class="sxs-lookup"><span data-stu-id="f3c89-147">**Vendor Reserved** (32768..65535)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="f3c89-148">**EnabledState**</span><span class="sxs-lookup"><span data-stu-id="f3c89-148">**EnabledState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f3c89-149">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="f3c89-149">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="f3c89-150">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="f3c89-150">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f3c89-151">限定詞： [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ( "**CIM \_ EnabledLogicalElement**.**OtherEnabledState**") </span><span class="sxs-lookup"><span data-stu-id="f3c89-151">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_EnabledLogicalElement**.**OtherEnabledState**")</span></span>
</dt> </dl>

<span data-ttu-id="f3c89-152">指出專案的已啟用狀態。</span><span class="sxs-lookup"><span data-stu-id="f3c89-152">Indicates the enabled state of an element.</span></span> <span data-ttu-id="f3c89-153">可能的值包括狀態之間的轉換。</span><span class="sxs-lookup"><span data-stu-id="f3c89-153">Possible values include the transitions between states.</span></span> <span data-ttu-id="f3c89-154">例如， **關閉** (4) 並 **啟動** (10) 是 **啟用** 和 **停用** 之間的暫時性狀態。</span><span class="sxs-lookup"><span data-stu-id="f3c89-154">For example, **Shutting Down** (4) and **Starting** (10) are transient states between **Enabled** and **Disabled**.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="f3c89-155"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**未知** 的 (0) </span><span class="sxs-lookup"><span data-stu-id="f3c89-155"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="f3c89-156"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**其他** (1) </span><span class="sxs-lookup"><span data-stu-id="f3c89-156"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="f3c89-157"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**已啟用** (2) </span><span class="sxs-lookup"><span data-stu-id="f3c89-157"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Enabled** (2)</span></span>


</dt> <dd>

<span data-ttu-id="f3c89-158">元素是或可能正在執行命令、將會處理任何已排入佇列的命令，並將新的要求排入佇列。</span><span class="sxs-lookup"><span data-stu-id="f3c89-158">The element is or could be executing commands, will process any queued commands, and queues new requests.</span></span>

</dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="f3c89-159"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**停用** (3) </span><span class="sxs-lookup"><span data-stu-id="f3c89-159"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabled** (3)</span></span>


</dt> <dd>

<span data-ttu-id="f3c89-160">元素將不會執行命令，而且會卸載任何新的要求。</span><span class="sxs-lookup"><span data-stu-id="f3c89-160">the element will not execute commands and will drop any new requests.</span></span>

</dd> <dt>

<span id="Shutting_Down"></span><span id="shutting_down"></span><span id="SHUTTING_DOWN"></span>

<span data-ttu-id="f3c89-161"><span id="Shutting_Down"></span><span id="shutting_down"></span><span id="SHUTTING_DOWN"></span>正在 **關閉** (4) </span><span class="sxs-lookup"><span data-stu-id="f3c89-161"><span id="Shutting_Down"></span><span id="shutting_down"></span><span id="SHUTTING_DOWN"></span>**Shutting Down** (4)</span></span>


</dt> <dd>

<span data-ttu-id="f3c89-162">專案正在進入已停用狀態的進程。</span><span class="sxs-lookup"><span data-stu-id="f3c89-162">The element is in the process of going to a Disabled state.</span></span>

</dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="f3c89-163"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**不適用** (5) </span><span class="sxs-lookup"><span data-stu-id="f3c89-163"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Not Applicable** (5)</span></span>


</dt> <dd>

<span data-ttu-id="f3c89-164">元素不支援啟用或停用。</span><span class="sxs-lookup"><span data-stu-id="f3c89-164">The element does not support being enabled or disabled.</span></span>

</dd> <dt>

<span id="Enabled_but_Offline"></span><span id="enabled_but_offline"></span><span id="ENABLED_BUT_OFFLINE"></span>

<span data-ttu-id="f3c89-165"><span id="Enabled_but_Offline"></span><span id="enabled_but_offline"></span><span id="ENABLED_BUT_OFFLINE"></span>**已啟用但離線** (6) </span><span class="sxs-lookup"><span data-stu-id="f3c89-165"><span id="Enabled_but_Offline"></span><span id="enabled_but_offline"></span><span id="ENABLED_BUT_OFFLINE"></span>**Enabled but Offline** (6)</span></span>


</dt> <dd>

<span data-ttu-id="f3c89-166">元素可能正在完成命令，並會卸載任何新的要求。</span><span class="sxs-lookup"><span data-stu-id="f3c89-166">The element might be completing commands, and will drop any new requests.</span></span>

</dd> <dt>

<span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>

<span data-ttu-id="f3c89-167"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**在測試** (7) </span><span class="sxs-lookup"><span data-stu-id="f3c89-167"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In Test** (7)</span></span>


</dt> <dd>

<span data-ttu-id="f3c89-168">元素處於測試狀態。</span><span class="sxs-lookup"><span data-stu-id="f3c89-168">The element is in a test state.</span></span>

</dd> <dt>

<span id="Deferred"></span><span id="deferred"></span><span id="DEFERRED"></span>

<span data-ttu-id="f3c89-169"><span id="Deferred"></span><span id="deferred"></span><span id="DEFERRED"></span>**延** 後的 (8) </span><span class="sxs-lookup"><span data-stu-id="f3c89-169"><span id="Deferred"></span><span id="deferred"></span><span id="DEFERRED"></span>**Deferred** (8)</span></span>


</dt> <dd>

<span data-ttu-id="f3c89-170">元素可能正在完成命令，但是會將任何新的要求排在佇列中。</span><span class="sxs-lookup"><span data-stu-id="f3c89-170">The element might be completing commands, but will queue any new requests.</span></span>

</dd> <dt>

<span id="Quiesce"></span><span id="quiesce"></span><span id="QUIESCE"></span>

<span data-ttu-id="f3c89-171"><span id="Quiesce"></span><span id="quiesce"></span><span id="QUIESCE"></span>**靜止** (9) </span><span class="sxs-lookup"><span data-stu-id="f3c89-171"><span id="Quiesce"></span><span id="quiesce"></span><span id="QUIESCE"></span>**Quiesce** (9)</span></span>


</dt> <dd>

<span data-ttu-id="f3c89-172">元素已啟用但處於受限模式。</span><span class="sxs-lookup"><span data-stu-id="f3c89-172">That the element is enabled but in a restricted mode.</span></span>

</dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="f3c89-173"><span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>**開始** (10) </span><span class="sxs-lookup"><span data-stu-id="f3c89-173"><span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>**Starting** (10)</span></span>


</dt> <dd>

<span data-ttu-id="f3c89-174">元素正在進入已啟用的狀態。</span><span class="sxs-lookup"><span data-stu-id="f3c89-174">The element is in the process of going to an Enabled state.</span></span> <span data-ttu-id="f3c89-175">新的要求會排入佇列。</span><span class="sxs-lookup"><span data-stu-id="f3c89-175">New requests are queued.</span></span>

</dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

<span data-ttu-id="f3c89-176"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF 保留** (11. 32767) </span><span class="sxs-lookup"><span data-stu-id="f3c89-176"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (11..32767)</span></span>


</dt> <dd></dd> <dt>

<span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>

<span data-ttu-id="f3c89-177"><span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>**廠商保留** (32768. 65535) </span><span class="sxs-lookup"><span data-stu-id="f3c89-177"><span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>**Vendor Reserved** (32768..65535)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="f3c89-178">**OtherEnabledState**</span><span class="sxs-lookup"><span data-stu-id="f3c89-178">**OtherEnabledState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f3c89-179">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="f3c89-179">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f3c89-180">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="f3c89-180">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f3c89-181">限定詞： [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ( "**CIM \_ EnabledLogicalElement**.**EnabledState**") </span><span class="sxs-lookup"><span data-stu-id="f3c89-181">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_EnabledLogicalElement**.**EnabledState**")</span></span>
</dt> </dl>

<span data-ttu-id="f3c89-182">描述當 **EnabledState** 屬性的值是 **其他** 時，元素的狀態。</span><span class="sxs-lookup"><span data-stu-id="f3c89-182">Describes the state of the element when the value of the **EnabledState** property is **Other**.</span></span> <span data-ttu-id="f3c89-183">當 **EnabledState** 不是 **其他** 值時，這個屬性必須設定為 **Null** 。</span><span class="sxs-lookup"><span data-stu-id="f3c89-183">This property must be set to **NULL** when **EnabledState** is not **Other**.</span></span>

</dd> <dt>

<span data-ttu-id="f3c89-184">**RequestedState**</span><span class="sxs-lookup"><span data-stu-id="f3c89-184">**RequestedState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f3c89-185">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="f3c89-185">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="f3c89-186">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="f3c89-186">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f3c89-187">限定詞： [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ( "**CIM \_ EnabledLogicalElement**.**EnabledState**") </span><span class="sxs-lookup"><span data-stu-id="f3c89-187">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_EnabledLogicalElement**.**EnabledState**")</span></span>
</dt> </dl>

<span data-ttu-id="f3c89-188">表示最後要求的元素狀態。</span><span class="sxs-lookup"><span data-stu-id="f3c89-188">Indicates the last requested state for the element.</span></span> <span data-ttu-id="f3c89-189">目前的狀態是由 **EnabledState** 屬性工作表示。</span><span class="sxs-lookup"><span data-stu-id="f3c89-189">The current state is indicated by the **EnabledState** property.</span></span> <span data-ttu-id="f3c89-190">這個屬性可讓您比較最後要求和目前的狀態。</span><span class="sxs-lookup"><span data-stu-id="f3c89-190">This property enables you to compare the last requested and current states.</span></span>

> [!Note]  
> <span data-ttu-id="f3c89-191">當 **EnabledState** 屬性的值 **不適用** 時，這個屬性不會有任何意義。</span><span class="sxs-lookup"><span data-stu-id="f3c89-191">When the value of the **EnabledState** property is **Not Applicable**, this property has no meaning.</span></span>

 

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="f3c89-192"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**未知** 的 (0) </span><span class="sxs-lookup"><span data-stu-id="f3c89-192"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd>

<span data-ttu-id="f3c89-193">最後要求的元素狀態不明。</span><span class="sxs-lookup"><span data-stu-id="f3c89-193">The last requested state for the element is unknown.</span></span>

</dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="f3c89-194"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**已啟用** (2) </span><span class="sxs-lookup"><span data-stu-id="f3c89-194"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Enabled** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="f3c89-195"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**停用** (3) </span><span class="sxs-lookup"><span data-stu-id="f3c89-195"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabled** (3)</span></span>


</dt> <dd>

<span data-ttu-id="f3c89-196">要求立即停用元素，使其不會執行或接受任何命令或處理要求。</span><span class="sxs-lookup"><span data-stu-id="f3c89-196">Requests an immediate disabling of the element, such that it will not execute or accept any commands or processing requests.</span></span>

</dd> <dt>

<span id="Shut_Down"></span><span id="shut_down"></span><span id="SHUT_DOWN"></span>

<span data-ttu-id="f3c89-197"><span id="Shut_Down"></span><span id="shut_down"></span><span id="SHUT_DOWN"></span>**關機** (4) </span><span class="sxs-lookup"><span data-stu-id="f3c89-197"><span id="Shut_Down"></span><span id="shut_down"></span><span id="SHUT_DOWN"></span>**Shut Down** (4)</span></span>


</dt> <dd>

<span data-ttu-id="f3c89-198">要求有條理地轉換為停用狀態，而且可能需要移除電源，以完全清除任何現有的狀態。</span><span class="sxs-lookup"><span data-stu-id="f3c89-198">Requests an orderly transition to the Disabled state, and might involve removing power, to completely erase any existing state.</span></span>

</dd> <dt>

<span id="No_Change"></span><span id="no_change"></span><span id="NO_CHANGE"></span>

<span data-ttu-id="f3c89-199"><span id="No_Change"></span><span id="no_change"></span><span id="NO_CHANGE"></span>**沒有變更** (5) </span><span class="sxs-lookup"><span data-stu-id="f3c89-199"><span id="No_Change"></span><span id="no_change"></span><span id="NO_CHANGE"></span>**No Change** (5)</span></span>


</dt> <dd>

<span data-ttu-id="f3c89-200">已淘汰，用來表示最後要求的狀態為「未知」 (0) 。</span><span class="sxs-lookup"><span data-stu-id="f3c89-200">Deprecated in lieu of indicating the last requested state is "Unknown" (0).</span></span> <span data-ttu-id="f3c89-201">如果上次要求或預期的狀態不明，則 **RequestedState** 的值應為「未知」 (0) ，但可能會有「沒有變更」值 (5) 。</span><span class="sxs-lookup"><span data-stu-id="f3c89-201">If the last requested or desired state is unknown, **RequestedState** should have the value "Unknown" (0), but may have the value "No Change" (5).</span></span>

</dd> <dt>

<span id="Offline"></span><span id="offline"></span><span id="OFFLINE"></span>

<span data-ttu-id="f3c89-202"><span id="Offline"></span><span id="offline"></span><span id="OFFLINE"></span>**離線** (6) </span><span class="sxs-lookup"><span data-stu-id="f3c89-202"><span id="Offline"></span><span id="offline"></span><span id="OFFLINE"></span>**Offline** (6)</span></span>


</dt> <dd>

<span data-ttu-id="f3c89-203">已要求將元素轉換成已啟用但離線的 **EnabledState**。</span><span class="sxs-lookup"><span data-stu-id="f3c89-203">The element has been requested to transition to the Enabled but Offline **EnabledState**.</span></span>

</dd> <dt>

<span id="Test"></span><span id="test"></span><span id="TEST"></span>

<span data-ttu-id="f3c89-204"><span id="Test"></span><span id="test"></span><span id="TEST"></span>**測試** (7) </span><span class="sxs-lookup"><span data-stu-id="f3c89-204"><span id="Test"></span><span id="test"></span><span id="TEST"></span>**Test** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Deferred"></span><span id="deferred"></span><span id="DEFERRED"></span>

<span data-ttu-id="f3c89-205"><span id="Deferred"></span><span id="deferred"></span><span id="DEFERRED"></span>**延** 後的 (8) </span><span class="sxs-lookup"><span data-stu-id="f3c89-205"><span id="Deferred"></span><span id="deferred"></span><span id="DEFERRED"></span>**Deferred** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Quiesce"></span><span id="quiesce"></span><span id="QUIESCE"></span>

<span data-ttu-id="f3c89-206"><span id="Quiesce"></span><span id="quiesce"></span><span id="QUIESCE"></span>**靜止** (9) </span><span class="sxs-lookup"><span data-stu-id="f3c89-206"><span id="Quiesce"></span><span id="quiesce"></span><span id="QUIESCE"></span>**Quiesce** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="Reboot"></span><span id="reboot"></span><span id="REBOOT"></span>

<span data-ttu-id="f3c89-207"><span id="Reboot"></span><span id="reboot"></span><span id="REBOOT"></span>**重新開機** (10) </span><span class="sxs-lookup"><span data-stu-id="f3c89-207"><span id="Reboot"></span><span id="reboot"></span><span id="REBOOT"></span>**Reboot** (10)</span></span>


</dt> <dd>

<span data-ttu-id="f3c89-208">指的是「關機」，然後移至「已啟用」狀態。</span><span class="sxs-lookup"><span data-stu-id="f3c89-208">Refers to doing a "Shut Down" and then moving to an "Enabled" state.</span></span>

</dd> <dt>

<span id="Reset"></span><span id="reset"></span><span id="RESET"></span>

<span data-ttu-id="f3c89-209"><span id="Reset"></span><span id="reset"></span><span id="RESET"></span>**重設** (11) </span><span class="sxs-lookup"><span data-stu-id="f3c89-209"><span id="Reset"></span><span id="reset"></span><span id="RESET"></span>**Reset** (11)</span></span>


</dt> <dd>

<span data-ttu-id="f3c89-210">指出元素是先「停用」，然後是「已啟用」。</span><span class="sxs-lookup"><span data-stu-id="f3c89-210">Indicates that the element is first "Disabled" and then "Enabled".</span></span>

</dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="f3c89-211"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**不適用** (12) </span><span class="sxs-lookup"><span data-stu-id="f3c89-211"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Not Applicable** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

<span data-ttu-id="f3c89-212"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF 保留** ( .。。) </span><span class="sxs-lookup"><span data-stu-id="f3c89-212"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>


</dt> <dd></dd> <dt>

<span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>

<span data-ttu-id="f3c89-213"><span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>**廠商保留** (32768. 65535) </span><span class="sxs-lookup"><span data-stu-id="f3c89-213"><span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>**Vendor Reserved** (32768..65535)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="f3c89-214">**TimeOfLastStateChange**</span><span class="sxs-lookup"><span data-stu-id="f3c89-214">**TimeOfLastStateChange**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f3c89-215">資料類型： **datetime**</span><span class="sxs-lookup"><span data-stu-id="f3c89-215">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="f3c89-216">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="f3c89-216">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f3c89-217">指出元素上次變更狀態的時間。</span><span class="sxs-lookup"><span data-stu-id="f3c89-217">Indicates when the element last changed state.</span></span> <span data-ttu-id="f3c89-218">如果專案的狀態未變更，而且此屬性已填入，則必須將它設定為零間隔值。</span><span class="sxs-lookup"><span data-stu-id="f3c89-218">If the state of the element has not changed and this property is populated, then it must be set to a zero interval value.</span></span> <span data-ttu-id="f3c89-219">如果已要求狀態變更，但遭到拒絕或尚未處理，則必須更新屬性。</span><span class="sxs-lookup"><span data-stu-id="f3c89-219">If a state change was requested, but was rejected or is not yet processed, the property must not be updated.</span></span>

</dd> <dt>

<span data-ttu-id="f3c89-220">**TransitioningToState**</span><span class="sxs-lookup"><span data-stu-id="f3c89-220">**TransitioningToState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f3c89-221">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="f3c89-221">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="f3c89-222">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="f3c89-222">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f3c89-223">限定詞： [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ( "**CIM \_ EnabledLogicalElement**.**RequestStateChange**"，"**CIM \_ EnabledLogicalElement**。**RequestedState**"，"**CIM \_ EnabledLogicalElement**。**EnabledState**") </span><span class="sxs-lookup"><span data-stu-id="f3c89-223">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_EnabledLogicalElement**.**RequestStateChange**", "**CIM\_EnabledLogicalElement**.**RequestedState**", "**CIM\_EnabledLogicalElement**.**EnabledState**")</span></span>
</dt> </dl>

<span data-ttu-id="f3c89-224">指出實例要變更的目標狀態。</span><span class="sxs-lookup"><span data-stu-id="f3c89-224">Indicates the target state to which the instance is changing.</span></span>

<span data-ttu-id="f3c89-225">**沒有變更** 的值表示沒有正在進行的轉換。</span><span class="sxs-lookup"><span data-stu-id="f3c89-225">A value of **No Change** indicates that no transition is in progress.</span></span> <span data-ttu-id="f3c89-226">[ **不適用** ] 的值表示執行不會報告進行中的轉換。</span><span class="sxs-lookup"><span data-stu-id="f3c89-226">A value of **Not Applicable** indicates that the implementation does not report ongoing transitions.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="f3c89-227">**未知** 的 (0) </span><span class="sxs-lookup"><span data-stu-id="f3c89-227">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="f3c89-228">**已啟用** (2) </span><span class="sxs-lookup"><span data-stu-id="f3c89-228">**Enabled** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="f3c89-229">**停用** (3) </span><span class="sxs-lookup"><span data-stu-id="f3c89-229">**Disabled** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Shut_Down"></span><span id="shut_down"></span><span id="SHUT_DOWN"></span>

<span data-ttu-id="f3c89-230">**關機** (4) </span><span class="sxs-lookup"><span data-stu-id="f3c89-230">**Shut Down** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="No_Change"></span><span id="no_change"></span><span id="NO_CHANGE"></span>

<span data-ttu-id="f3c89-231">**沒有變更** (5) </span><span class="sxs-lookup"><span data-stu-id="f3c89-231">**No Change** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Offline"></span><span id="offline"></span><span id="OFFLINE"></span>

<span data-ttu-id="f3c89-232">**離線** (6) </span><span class="sxs-lookup"><span data-stu-id="f3c89-232">**Offline** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Test"></span><span id="test"></span><span id="TEST"></span>

<span data-ttu-id="f3c89-233">**測試** (7) </span><span class="sxs-lookup"><span data-stu-id="f3c89-233">**Test** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Defer"></span><span id="defer"></span><span id="DEFER"></span>

<span data-ttu-id="f3c89-234">**延** 後 (8) </span><span class="sxs-lookup"><span data-stu-id="f3c89-234">**Defer** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Quiesce"></span><span id="quiesce"></span><span id="QUIESCE"></span>

<span data-ttu-id="f3c89-235">**靜止** (9) </span><span class="sxs-lookup"><span data-stu-id="f3c89-235">**Quiesce** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="Reboot"></span><span id="reboot"></span><span id="REBOOT"></span>

<span data-ttu-id="f3c89-236">**重新開機** (10) </span><span class="sxs-lookup"><span data-stu-id="f3c89-236">**Reboot** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="Reset"></span><span id="reset"></span><span id="RESET"></span>

<span data-ttu-id="f3c89-237">**重設** (11) </span><span class="sxs-lookup"><span data-stu-id="f3c89-237">**Reset** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="f3c89-238">**不適用** (12) </span><span class="sxs-lookup"><span data-stu-id="f3c89-238">**Not Applicable** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

<span data-ttu-id="f3c89-239">**DMTF 保留** ( .。。) </span><span class="sxs-lookup"><span data-stu-id="f3c89-239">**DMTF Reserved** (..)</span></span>


<span data-ttu-id="f3c89-240"></dt> <dd></dd> </dl>

</dd> </dl></span><span class="sxs-lookup"><span data-stu-id="f3c89-240"></dt> <dd></dd> </dl>

</dd> </dl></span></span>

## <a name="requirements"></a><span data-ttu-id="f3c89-241">規格需求</span><span class="sxs-lookup"><span data-stu-id="f3c89-241">Requirements</span></span>



| <span data-ttu-id="f3c89-242">需求</span><span class="sxs-lookup"><span data-stu-id="f3c89-242">Requirement</span></span> | <span data-ttu-id="f3c89-243">值</span><span class="sxs-lookup"><span data-stu-id="f3c89-243">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f3c89-244">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="f3c89-244">Minimum supported client</span></span><br/> | <span data-ttu-id="f3c89-245">Windows 8</span><span class="sxs-lookup"><span data-stu-id="f3c89-245">Windows 8</span></span><br/>                                                                                    |
| <span data-ttu-id="f3c89-246">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="f3c89-246">Minimum supported server</span></span><br/> | <span data-ttu-id="f3c89-247">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="f3c89-247">Windows Server 2012</span></span><br/>                                                                          |
| <span data-ttu-id="f3c89-248">命名空間</span><span class="sxs-lookup"><span data-stu-id="f3c89-248">Namespace</span></span><br/>                | <span data-ttu-id="f3c89-249">根 \\ 虛擬化 \\ v2</span><span class="sxs-lookup"><span data-stu-id="f3c89-249">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="f3c89-250">MOF</span><span class="sxs-lookup"><span data-stu-id="f3c89-250">MOF</span></span><br/>                      | <dl> <span data-ttu-id="f3c89-251"><dt>WindowsVirtualization。</dt></span><span class="sxs-lookup"><span data-stu-id="f3c89-251"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="f3c89-252">DLL</span><span class="sxs-lookup"><span data-stu-id="f3c89-252">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f3c89-253"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="f3c89-253"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="f3c89-254">另請參閱</span><span class="sxs-lookup"><span data-stu-id="f3c89-254">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f3c89-255">**CIM \_ LogicalElement**</span><span class="sxs-lookup"><span data-stu-id="f3c89-255">**CIM\_LogicalElement**</span></span>](cim-logicalelement.md)
</dt> </dl>

 

