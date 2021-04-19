---
description: 代表 Microsoft Windows Hyper-v 平臺的虛擬裝置服務。
ms.assetid: 865D83E1-0FC6-4F96-94BB-AA5116890127
title: Msvm_VirtualSystemResourceComponent 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualSystemResourceComponent
- Msvm_VirtualSystemResourceComponent.Name
- Msvm_VirtualSystemResourceComponent.CLSID
- Msvm_VirtualSystemResourceComponent.Context
- Msvm_VirtualSystemResourceComponent.Enabled
- Msvm_VirtualSystemResourceComponent.AdditionalClassNames
- Msvm_VirtualSystemResourceComponent.Type
- Msvm_VirtualSystemResourceComponent.HotAdd
- Msvm_VirtualSystemResourceComponent.HotRemove
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 81c2d31a6497325ac77003ded266333518de890a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106970771"
---
# <a name="msvm_virtualsystemresourcecomponent-class"></a><span data-ttu-id="556b4-103">Msvm \_ VirtualSystemResourceComponent 類別</span><span class="sxs-lookup"><span data-stu-id="556b4-103">Msvm\_VirtualSystemResourceComponent class</span></span>

<span data-ttu-id="556b4-104">代表 Microsoft Windows Hyper-v 平臺的虛擬裝置服務。</span><span class="sxs-lookup"><span data-stu-id="556b4-104">Represents a virtual device service of the Microsoft Windows Hyper-V platform.</span></span>

<span data-ttu-id="556b4-105">下列語法已簡化受控物件格式 (MOF) 程式碼，並且包含所有繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="556b4-105">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="556b4-106">語法</span><span class="sxs-lookup"><span data-stu-id="556b4-106">Syntax</span></span>

``` syntax
class Msvm_VirtualSystemResourceComponent : Msvm_VirtualizationComponent
{
  string  Name;
  string  CLSID;
  uint32  Context = 1;
  boolean Enabled = True;
  string  AdditionalClassNames[];
  uint16  Type = 1;
  boolean HotAdd = False;
  boolean HotRemove = False;
};
```

## <a name="members"></a><span data-ttu-id="556b4-107">成員</span><span class="sxs-lookup"><span data-stu-id="556b4-107">Members</span></span>

<span data-ttu-id="556b4-108">**Msvm \_ VirtualSystemResourceComponent** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="556b4-108">The **Msvm\_VirtualSystemResourceComponent** class has these types of members:</span></span>

-   [<span data-ttu-id="556b4-109">屬性</span><span class="sxs-lookup"><span data-stu-id="556b4-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="556b4-110">屬性</span><span class="sxs-lookup"><span data-stu-id="556b4-110">Properties</span></span>

<span data-ttu-id="556b4-111">**Msvm \_ VirtualSystemResourceComponent** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="556b4-111">The **Msvm\_VirtualSystemResourceComponent** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="556b4-112">**AdditionalClassNames**</span><span class="sxs-lookup"><span data-stu-id="556b4-112">**AdditionalClassNames**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="556b4-113">資料類型： **字串** 陣列</span><span class="sxs-lookup"><span data-stu-id="556b4-113">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="556b4-114">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="556b4-114">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="556b4-115">字串陣列，其中包含這個 **Msvm \_ VirtualSystemResourceComponent** 實例所呈現的其他非關聯類別。</span><span class="sxs-lookup"><span data-stu-id="556b4-115">An array of strings containing additional non-association classes surfaced by this **Msvm\_VirtualSystemResourceComponent** instance.</span></span> <span data-ttu-id="556b4-116">這些類別都必須衍生自 [**cim \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice) 或 [**cim \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)。</span><span class="sxs-lookup"><span data-stu-id="556b4-116">These classes must derive from neither [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice) nor [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="556b4-117">**Clsid**</span><span class="sxs-lookup"><span data-stu-id="556b4-117">**CLSID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="556b4-118">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="556b4-118">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="556b4-119">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="556b4-119">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="556b4-120">GUID，表示服務 COM 物件的類別識別碼。</span><span class="sxs-lookup"><span data-stu-id="556b4-120">A GUID that represents the class identifier of the service's COM object.</span></span> <span data-ttu-id="556b4-121">這個屬性繼承自 [**Msvm \_ VirtualizationComponent**](msvm-virtualizationcomponent.md)。</span><span class="sxs-lookup"><span data-stu-id="556b4-121">This property is inherited from [**Msvm\_VirtualizationComponent**](msvm-virtualizationcomponent.md).</span></span>

</dd> <dt>

<span data-ttu-id="556b4-122">**內容**</span><span class="sxs-lookup"><span data-stu-id="556b4-122">**Context**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="556b4-123">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="556b4-123">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="556b4-124">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="556b4-124">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="556b4-125">新建立的物件將在其中執行的內容。</span><span class="sxs-lookup"><span data-stu-id="556b4-125">The context in which the newly created object will run.</span></span> <span data-ttu-id="556b4-126">此值會在 *dwClsCoNtext* 參數中傳遞至 [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance)。</span><span class="sxs-lookup"><span data-stu-id="556b4-126">This value is passed in the *dwClsContext* parameter to [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance).</span></span> <span data-ttu-id="556b4-127">這個屬性繼承自 [**Msvm \_ VirtualizationComponent**](msvm-virtualizationcomponent.md)，而且一律設定為1。</span><span class="sxs-lookup"><span data-stu-id="556b4-127">This property is inherited from [**Msvm\_VirtualizationComponent**](msvm-virtualizationcomponent.md), and it is always set to 1.</span></span>

</dd> <dt>

<span data-ttu-id="556b4-128">**Enabled**</span><span class="sxs-lookup"><span data-stu-id="556b4-128">**Enabled**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="556b4-129">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="556b4-129">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="556b4-130">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="556b4-130">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="556b4-131">如果這個實例已啟用，而且可以用來完成用戶端要求，則為 **True** 。否則 **為 False**。</span><span class="sxs-lookup"><span data-stu-id="556b4-131">**True** if this instance is enabled and can be used to complete client requests; otherwise, **False**.</span></span> <span data-ttu-id="556b4-132">這個屬性繼承自 [**Msvm \_ VirtualizationComponent**](msvm-virtualizationcomponent.md)，而且一律設定為 **True**。</span><span class="sxs-lookup"><span data-stu-id="556b4-132">This property is inherited from [**Msvm\_VirtualizationComponent**](msvm-virtualizationcomponent.md), and it is always set to **True**.</span></span>

</dd> <dt>

<span data-ttu-id="556b4-133">**HotAdd**</span><span class="sxs-lookup"><span data-stu-id="556b4-133">**HotAdd**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="556b4-134">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="556b4-134">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="556b4-135">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="556b4-135">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="556b4-136">如果這個實例可以熱新增至虛擬機器，則為 **True** ;否則 **為 False**。</span><span class="sxs-lookup"><span data-stu-id="556b4-136">**True** if this instance can be hot-added to a virtual machine; otherwise, **False**.</span></span> <span data-ttu-id="556b4-137">預設值為 **False**。</span><span class="sxs-lookup"><span data-stu-id="556b4-137">The default is **False**.</span></span>

</dd> <dt>

<span data-ttu-id="556b4-138">**HotRemove**</span><span class="sxs-lookup"><span data-stu-id="556b4-138">**HotRemove**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="556b4-139">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="556b4-139">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="556b4-140">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="556b4-140">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="556b4-141">如果可以從虛擬機器熱移除這個實例，則為 **True** ;否則 **為 False**。</span><span class="sxs-lookup"><span data-stu-id="556b4-141">**True** if this instance can be hot-removed from a virtual machine; otherwise, **False**.</span></span> <span data-ttu-id="556b4-142">預設值為 **False**。</span><span class="sxs-lookup"><span data-stu-id="556b4-142">The default is **False**.</span></span>

</dd> <dt>

<span data-ttu-id="556b4-143">**名稱**</span><span class="sxs-lookup"><span data-stu-id="556b4-143">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="556b4-144">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="556b4-144">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="556b4-145">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="556b4-145">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="556b4-146">限定詞：索引 **鍵**</span><span class="sxs-lookup"><span data-stu-id="556b4-146">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="556b4-147">可唯一識別服務的語言中性字元串。</span><span class="sxs-lookup"><span data-stu-id="556b4-147">A language-neutral string that uniquely identifies the service.</span></span> <span data-ttu-id="556b4-148">建議採用下列格式來防止命名衝突：「廠商 \| 元件 \| 版本」。</span><span class="sxs-lookup"><span data-stu-id="556b4-148">The following format is suggested to prevent naming conflicts: "vendor\|component\|version".</span></span> <span data-ttu-id="556b4-149">例如，此名稱代表 Microsoft 模擬網路埠元件的1.0 版：「Microsoft EmulatedNetworkPortComponent v1.0 \| 」 \| 。</span><span class="sxs-lookup"><span data-stu-id="556b4-149">For example, this name represents version 1.0 of the Microsoft Emulated Network Port Component: "Microsoft\|EmulatedNetworkPortComponent\|V1.0".</span></span> <span data-ttu-id="556b4-150">這個屬性繼承自 [**Msvm \_ VirtualizationComponent**](msvm-virtualizationcomponent.md)。</span><span class="sxs-lookup"><span data-stu-id="556b4-150">This property is inherited from [**Msvm\_VirtualizationComponent**](msvm-virtualizationcomponent.md).</span></span>

</dd> <dt>

<span data-ttu-id="556b4-151">**型別**</span><span class="sxs-lookup"><span data-stu-id="556b4-151">**Type**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="556b4-152">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="556b4-152">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="556b4-153">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="556b4-153">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="556b4-154">使用虛擬裝置在此處描述的 WMI 物件的關聯性。</span><span class="sxs-lookup"><span data-stu-id="556b4-154">The relationship of the WMI object that is described here with the virtual device.</span></span>



| <span data-ttu-id="556b4-155">值</span><span class="sxs-lookup"><span data-stu-id="556b4-155">Value</span></span>                                                                                                                                                                                                                                                           | <span data-ttu-id="556b4-156">意義</span><span class="sxs-lookup"><span data-stu-id="556b4-156">Meaning</span></span>                                                                                                                                                                                                        |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="_Not_Changeable_"></span><span id="_not_changeable_"></span><span id="_NOT_CHANGEABLE_"></span><dl> <span data-ttu-id="556b4-157">「<dt>**不可**</dt>變更」 <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="556b4-157"><dt>**"Not Changeable"**</dt> <dt>0</dt></span></span> </dl> |                                                                                                                                                                                                                |
| <span id="_Singleton_"></span><span id="_singleton_"></span><span id="_SINGLETON_"></span><dl> <span data-ttu-id="556b4-158">「 <dt>**Singleton**</dt> 」 <dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="556b4-158"><dt>**"Singleton"**</dt> <dt>1</dt></span></span> </dl>                     | <span data-ttu-id="556b4-159">Singleton 是最上層的 WMI 物件，它會與虛擬裝置系結1:1，且每個虛擬機器只能存在一次。</span><span class="sxs-lookup"><span data-stu-id="556b4-159">Singleton is a top level WMI object that is tied 1:1 with a Virtual Device and can only exist once per virtual machine.</span></span> <span data-ttu-id="556b4-160">這是預設值。</span><span class="sxs-lookup"><span data-stu-id="556b4-160">This is the default value.</span></span><br/>                                                  |
| <span id="_MultiInstance_"></span><span id="_multiinstance_"></span><span id="_MULTIINSTANCE_"></span><dl> <span data-ttu-id="556b4-161"><dt>**"多重實例"**</dt> <dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="556b4-161"><dt>**"MultiInstance"**</dt> <dt>2</dt></span></span> </dl>     | <span data-ttu-id="556b4-162">多重實例是最上層的 WMI 物件，每個虛擬機器可以多次存在，並與虛擬裝置系結1:1。</span><span class="sxs-lookup"><span data-stu-id="556b4-162">MultiInstance is a top level WMI object that can exist multiple times per virtual machine and is tied 1:1 with a Virtual Device.</span></span><br/>                                                                    |
| <span id="_Subdevice_"></span><span id="_subdevice_"></span><span id="_SUBDEVICE_"></span><dl> <span data-ttu-id="556b4-163"><dt>**"Subdevice"**</dt> <dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="556b4-163"><dt>**"Subdevice"**</dt> <dt>3</dt></span></span> </dl>                     | <span data-ttu-id="556b4-164">Subdevice 是沒有父參考的 WMI 物件，但只能由一個虛擬裝置所控制，每個虛擬機器只能存在一次。</span><span class="sxs-lookup"><span data-stu-id="556b4-164">Subdevice is a WMI object that has not parent reference but is controlled by only one Virtual Device that can exist only once per virtual machine.</span></span> <span data-ttu-id="556b4-165">但是 WMI 物件可以有倍數的時間。</span><span class="sxs-lookup"><span data-stu-id="556b4-165">The WMI object though can exist multiples times.</span></span><br/> |



 

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="556b4-166">備註</span><span class="sxs-lookup"><span data-stu-id="556b4-166">Remarks</span></span>

<span data-ttu-id="556b4-167">存取 **Msvm \_ VirtualSystemResourceComponent** 類別可能受 UAC 篩選所限制。</span><span class="sxs-lookup"><span data-stu-id="556b4-167">Access to the **Msvm\_VirtualSystemResourceComponent** class might be restricted by UAC Filtering.</span></span> <span data-ttu-id="556b4-168">如需詳細資訊，請參閱 [使用者帳戶控制和 WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi)。</span><span class="sxs-lookup"><span data-stu-id="556b4-168">For more information, see [User Account Control and WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span></span>

## <a name="requirements"></a><span data-ttu-id="556b4-169">規格需求</span><span class="sxs-lookup"><span data-stu-id="556b4-169">Requirements</span></span>



| <span data-ttu-id="556b4-170">需求</span><span class="sxs-lookup"><span data-stu-id="556b4-170">Requirement</span></span> | <span data-ttu-id="556b4-171">值</span><span class="sxs-lookup"><span data-stu-id="556b4-171">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="556b4-172">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="556b4-172">Minimum supported client</span></span><br/> | <span data-ttu-id="556b4-173">\[僅 Windows 8 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="556b4-173">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="556b4-174">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="556b4-174">Minimum supported server</span></span><br/> | <span data-ttu-id="556b4-175">僅限 Windows Server 2012 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="556b4-175">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="556b4-176">用戶端支援結束</span><span class="sxs-lookup"><span data-stu-id="556b4-176">End of client support</span></span><br/>    | <span data-ttu-id="556b4-177">Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="556b4-177">Windows 8.1</span></span><br/>                                                                                  |
| <span data-ttu-id="556b4-178">伺服器支援結束</span><span class="sxs-lookup"><span data-stu-id="556b4-178">End of server support</span></span><br/>    | <span data-ttu-id="556b4-179">Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="556b4-179">Windows Server 2012 R2</span></span><br/>                                                                       |
| <span data-ttu-id="556b4-180">命名空間</span><span class="sxs-lookup"><span data-stu-id="556b4-180">Namespace</span></span><br/>                | <span data-ttu-id="556b4-181">根 \\ 虛擬化 \\ V2</span><span class="sxs-lookup"><span data-stu-id="556b4-181">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="556b4-182">MOF</span><span class="sxs-lookup"><span data-stu-id="556b4-182">MOF</span></span><br/>                      | <dl> <span data-ttu-id="556b4-183"><dt>WindowsVirtualization。</dt></span><span class="sxs-lookup"><span data-stu-id="556b4-183"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="556b4-184">DLL</span><span class="sxs-lookup"><span data-stu-id="556b4-184">DLL</span></span><br/>                      | <dl> <span data-ttu-id="556b4-185"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="556b4-185"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="556b4-186">另請參閱</span><span class="sxs-lookup"><span data-stu-id="556b4-186">See also</span></span>

<dl> <dt>

[<span data-ttu-id="556b4-187">**Msvm \_ VirtualizationComponent**</span><span class="sxs-lookup"><span data-stu-id="556b4-187">**Msvm\_VirtualizationComponent**</span></span>](/windows/desktop/HyperV_v2/msvm-virtualizationcomponent)
</dt> <dt>

[<span data-ttu-id="556b4-188">**Msvm \_ VirtualizationComponent**</span><span class="sxs-lookup"><span data-stu-id="556b4-188">**Msvm\_VirtualizationComponent**</span></span>](msvm-virtualizationcomponent.md)
</dt> </dl>

 

