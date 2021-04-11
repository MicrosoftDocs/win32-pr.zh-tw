---
description: 描述相關聯 Msvm 的非程式的功能 \_ 。
ms.assetid: 7e3b51ba-f85d-4b83-abc6-a094d412eca1
title: Msvm_VirtualSystemCapabilities 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualSystemCapabilities
- Msvm_VirtualSystemCapabilities.InstanceID
- Msvm_VirtualSystemCapabilities.Caption
- Msvm_VirtualSystemCapabilities.Description
- Msvm_VirtualSystemCapabilities.ElementName
- Msvm_VirtualSystemCapabilities.ElementNameEditSupported
- Msvm_VirtualSystemCapabilities.MaxElementNameLen
- Msvm_VirtualSystemCapabilities.RequestedStatesSupported
- Msvm_VirtualSystemCapabilities.ElementNameMask
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 9fbd9b747e85ec1c9a1b7754f99282a7d913994e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104191160"
---
# <a name="msvm_virtualsystemcapabilities-class"></a><span data-ttu-id="d5aa2-103">Msvm \_ VirtualSystemCapabilities 類別</span><span class="sxs-lookup"><span data-stu-id="d5aa2-103">Msvm\_VirtualSystemCapabilities class</span></span>

<span data-ttu-id="d5aa2-104">描述相關聯 Msvm 的非 [**程式 \_**](msvm-computersystem.md)的功能。</span><span class="sxs-lookup"><span data-stu-id="d5aa2-104">Describes the capabilities of the associated [**Msvm\_ComputerSystem**](msvm-computersystem.md).</span></span>

<span data-ttu-id="d5aa2-105">下列語法已簡化受控物件格式 (MOF) 程式碼，並且包含所有繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="d5aa2-105">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="d5aa2-106">語法</span><span class="sxs-lookup"><span data-stu-id="d5aa2-106">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_VirtualSystemCapabilities : CIM_EnabledLogicalElementCapabilities
{
  string  InstanceID;
  string  Caption = "Hyper-V Virtual System Capabilities";
  string  Description = "Defines Virtual System Capabilities";
  string  ElementName = "Hyper-V Virtual System Capabilities";
  boolean ElementNameEditSupported = True;
  unit16  MaxElementNameLen = 100;
  unit16  RequestedStatesSupported[];
  string  ElementNameMask;
};
```

## <a name="members"></a><span data-ttu-id="d5aa2-107">成員</span><span class="sxs-lookup"><span data-stu-id="d5aa2-107">Members</span></span>

<span data-ttu-id="d5aa2-108">**Msvm \_ VirtualSystemCapabilities** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="d5aa2-108">The **Msvm\_VirtualSystemCapabilities** class has these types of members:</span></span>

-   [<span data-ttu-id="d5aa2-109">屬性</span><span class="sxs-lookup"><span data-stu-id="d5aa2-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="d5aa2-110">屬性</span><span class="sxs-lookup"><span data-stu-id="d5aa2-110">Properties</span></span>

<span data-ttu-id="d5aa2-111">**Msvm \_ VirtualSystemCapabilities** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="d5aa2-111">The **Msvm\_VirtualSystemCapabilities** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="d5aa2-112">**標題**</span><span class="sxs-lookup"><span data-stu-id="d5aa2-112">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d5aa2-113">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="d5aa2-113">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d5aa2-114">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="d5aa2-114">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d5aa2-115">物件的簡短描述。</span><span class="sxs-lookup"><span data-stu-id="d5aa2-115">A short description of the object.</span></span> <span data-ttu-id="d5aa2-116">這個屬性繼承自 [**CIM \_ ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)。</span><span class="sxs-lookup"><span data-stu-id="d5aa2-116">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="d5aa2-117">**說明**</span><span class="sxs-lookup"><span data-stu-id="d5aa2-117">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d5aa2-118">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="d5aa2-118">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d5aa2-119">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="d5aa2-119">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d5aa2-120">對物件的描述。</span><span class="sxs-lookup"><span data-stu-id="d5aa2-120">A description of the object.</span></span> <span data-ttu-id="d5aa2-121">這個屬性繼承自 [**CIM \_ ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)。</span><span class="sxs-lookup"><span data-stu-id="d5aa2-121">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="d5aa2-122">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="d5aa2-122">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d5aa2-123">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="d5aa2-123">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d5aa2-124">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="d5aa2-124">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d5aa2-125">物件的顯示名稱。</span><span class="sxs-lookup"><span data-stu-id="d5aa2-125">A display name for the object.</span></span> <span data-ttu-id="d5aa2-126">這個屬性繼承自 [**CIM \_ ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)。</span><span class="sxs-lookup"><span data-stu-id="d5aa2-126">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="d5aa2-127">**ElementNameEditSupported**</span><span class="sxs-lookup"><span data-stu-id="d5aa2-127">**ElementNameEditSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d5aa2-128">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="d5aa2-128">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="d5aa2-129">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="d5aa2-129">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d5aa2-130">指出是否可以修改 **ElementName** 屬性。</span><span class="sxs-lookup"><span data-stu-id="d5aa2-130">Indicates whether the **ElementName** property can be modified.</span></span> <span data-ttu-id="d5aa2-131">這個屬性繼承自 **CIM \_ EnabledLogicalElementCapabilities**。</span><span class="sxs-lookup"><span data-stu-id="d5aa2-131">This property is inherited from **CIM\_EnabledLogicalElementCapabilities**.</span></span>

</dd> <dt>

<span data-ttu-id="d5aa2-132">**ElementNameMask**</span><span class="sxs-lookup"><span data-stu-id="d5aa2-132">**ElementNameMask**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d5aa2-133">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="d5aa2-133">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d5aa2-134">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="d5aa2-134">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d5aa2-135">指定 **ElementName** 的限制，以正則運算式表示。</span><span class="sxs-lookup"><span data-stu-id="d5aa2-135">Specifies the restrictions on **ElementName**, expressed as a regular expression.</span></span> <span data-ttu-id="d5aa2-136">這個屬性繼承自 **CIM \_ EnabledLogicalElementCapabilities**。</span><span class="sxs-lookup"><span data-stu-id="d5aa2-136">This property is inherited from **CIM\_EnabledLogicalElementCapabilities**.</span></span>

</dd> <dt>

<span data-ttu-id="d5aa2-137">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="d5aa2-137">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d5aa2-138">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="d5aa2-138">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d5aa2-139">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="d5aa2-139">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d5aa2-140">限定詞：索引 **鍵**</span><span class="sxs-lookup"><span data-stu-id="d5aa2-140">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="d5aa2-141">唯一識別此類別的實例。</span><span class="sxs-lookup"><span data-stu-id="d5aa2-141">Uniquely identifies an instance of this class.</span></span> <span data-ttu-id="d5aa2-142">這個屬性繼承自 [**CIM \_ ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)。</span><span class="sxs-lookup"><span data-stu-id="d5aa2-142">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="d5aa2-143">**MaxElementNameLen**</span><span class="sxs-lookup"><span data-stu-id="d5aa2-143">**MaxElementNameLen**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d5aa2-144">資料類型： **unit16**</span><span class="sxs-lookup"><span data-stu-id="d5aa2-144">Data type: **unit16**</span></span>
</dt> <dt>

<span data-ttu-id="d5aa2-145">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="d5aa2-145">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d5aa2-146">限定詞： **int32.maxvalue** (256) </span><span class="sxs-lookup"><span data-stu-id="d5aa2-146">Qualifiers: **MaxValue** (256)</span></span>
</dt> </dl>

<span data-ttu-id="d5aa2-147">指定 **ElementName** 屬性支援的最大長度。</span><span class="sxs-lookup"><span data-stu-id="d5aa2-147">Specifies the maximum supported length of the **ElementName** property.</span></span> <span data-ttu-id="d5aa2-148">這個屬性繼承自 **CIM \_ EnabledLogicalElementCapabilities**。</span><span class="sxs-lookup"><span data-stu-id="d5aa2-148">This property is inherited from **CIM\_EnabledLogicalElementCapabilities**.</span></span>

</dd> <dt>

<span data-ttu-id="d5aa2-149">**RequestedStatesSupported**</span><span class="sxs-lookup"><span data-stu-id="d5aa2-149">**RequestedStatesSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d5aa2-150">資料類型： **unit16** 陣列</span><span class="sxs-lookup"><span data-stu-id="d5aa2-150">Data type: **unit16** array</span></span>
</dt> <dt>

<span data-ttu-id="d5aa2-151">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="d5aa2-151">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d5aa2-152">指出在啟用的邏輯元素上使用 **RequestStateChange** 方法時，可以要求的可能狀態。</span><span class="sxs-lookup"><span data-stu-id="d5aa2-152">Indicates the possible states that can be requested when using the **RequestStateChange** method on the enabled logical element.</span></span> <span data-ttu-id="d5aa2-153">這個屬性繼承自 **CIM \_ EnabledLogicalElementCapabilities**。</span><span class="sxs-lookup"><span data-stu-id="d5aa2-153">This property is inherited from **CIM\_EnabledLogicalElementCapabilities**.</span></span>



| <span data-ttu-id="d5aa2-154">值</span><span class="sxs-lookup"><span data-stu-id="d5aa2-154">Value</span></span>                                                                         | <span data-ttu-id="d5aa2-155">意義</span><span class="sxs-lookup"><span data-stu-id="d5aa2-155">Meaning</span></span>              |
|-------------------------------------------------------------------------------|----------------------|
| <dl> <span data-ttu-id="d5aa2-156"><dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="d5aa2-156"><dt>2</dt></span></span> </dl>  | <span data-ttu-id="d5aa2-157">已啟用</span><span class="sxs-lookup"><span data-stu-id="d5aa2-157">Enabled</span></span><br/>   |
| <dl> <span data-ttu-id="d5aa2-158"><dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="d5aa2-158"><dt>3</dt></span></span> </dl>  | <span data-ttu-id="d5aa2-159">禁用</span><span class="sxs-lookup"><span data-stu-id="d5aa2-159">Disables</span></span><br/>  |
| <dl> <span data-ttu-id="d5aa2-160"><dt>4</dt></span><span class="sxs-lookup"><span data-stu-id="d5aa2-160"><dt>4</dt></span></span> </dl>  | <span data-ttu-id="d5aa2-161">關閉</span><span class="sxs-lookup"><span data-stu-id="d5aa2-161">Shut Down</span></span><br/> |
| <dl> <span data-ttu-id="d5aa2-162"><dt>6</dt></span><span class="sxs-lookup"><span data-stu-id="d5aa2-162"><dt>6</dt></span></span> </dl>  | <span data-ttu-id="d5aa2-163">離線</span><span class="sxs-lookup"><span data-stu-id="d5aa2-163">Offline</span></span><br/>   |
| <dl> <span data-ttu-id="d5aa2-164"><dt>7</dt></span><span class="sxs-lookup"><span data-stu-id="d5aa2-164"><dt>7</dt></span></span> </dl>  | <span data-ttu-id="d5aa2-165">測試</span><span class="sxs-lookup"><span data-stu-id="d5aa2-165">Test</span></span><br/>      |
| <dl> <span data-ttu-id="d5aa2-166"><dt>8</dt></span><span class="sxs-lookup"><span data-stu-id="d5aa2-166"><dt>8</dt></span></span> </dl>  | <span data-ttu-id="d5aa2-167">推遲</span><span class="sxs-lookup"><span data-stu-id="d5aa2-167">Defer</span></span><br/>     |
| <dl> <span data-ttu-id="d5aa2-168"><dt>9</dt></span><span class="sxs-lookup"><span data-stu-id="d5aa2-168"><dt>9</dt></span></span> </dl>  | <span data-ttu-id="d5aa2-169">靜止</span><span class="sxs-lookup"><span data-stu-id="d5aa2-169">Quiesce</span></span><br/>   |
| <dl> <span data-ttu-id="d5aa2-170"><dt>10</dt></span><span class="sxs-lookup"><span data-stu-id="d5aa2-170"><dt>10</dt></span></span> </dl> | <span data-ttu-id="d5aa2-171">重新啟動</span><span class="sxs-lookup"><span data-stu-id="d5aa2-171">Reboot</span></span><br/>    |
| <dl> <span data-ttu-id="d5aa2-172"><dt>11</dt></span><span class="sxs-lookup"><span data-stu-id="d5aa2-172"><dt>11</dt></span></span> </dl> | <span data-ttu-id="d5aa2-173">重設</span><span class="sxs-lookup"><span data-stu-id="d5aa2-173">Reset</span></span><br/>     |



 

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="d5aa2-174">規格需求</span><span class="sxs-lookup"><span data-stu-id="d5aa2-174">Requirements</span></span>



| <span data-ttu-id="d5aa2-175">需求</span><span class="sxs-lookup"><span data-stu-id="d5aa2-175">Requirement</span></span> | <span data-ttu-id="d5aa2-176">值</span><span class="sxs-lookup"><span data-stu-id="d5aa2-176">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d5aa2-177">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="d5aa2-177">Minimum supported client</span></span><br/> | <span data-ttu-id="d5aa2-178">\[僅 Windows 8 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="d5aa2-178">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="d5aa2-179">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="d5aa2-179">Minimum supported server</span></span><br/> | <span data-ttu-id="d5aa2-180">僅限 Windows Server 2012 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="d5aa2-180">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="d5aa2-181">命名空間</span><span class="sxs-lookup"><span data-stu-id="d5aa2-181">Namespace</span></span><br/>                | <span data-ttu-id="d5aa2-182">根 \\ 虛擬化 \\ V2</span><span class="sxs-lookup"><span data-stu-id="d5aa2-182">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="d5aa2-183">MOF</span><span class="sxs-lookup"><span data-stu-id="d5aa2-183">MOF</span></span><br/>                      | <dl> <span data-ttu-id="d5aa2-184"><dt>WindowsVirtualization。</dt></span><span class="sxs-lookup"><span data-stu-id="d5aa2-184"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="d5aa2-185">DLL</span><span class="sxs-lookup"><span data-stu-id="d5aa2-185">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d5aa2-186"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="d5aa2-186"><dt>Vmms.exe</dt></span></span> </dl>                     |



 

