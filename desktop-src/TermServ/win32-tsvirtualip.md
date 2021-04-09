---
title: Win32_TSVirtualIP 類別
description: 定義遠端桌面工作階段主機 (RD 工作階段主機) 伺服器 (IP) 虛擬化設定的網際網路通訊協定。
ms.assetid: c37d572c-f6db-438b-8290-006a623c6593
ms.tgt_platform: multiple
keywords:
- Win32_TSVirtualIP 類別遠端桌面服務
- Win32_TSVirtualIP 類別遠端桌面服務，描述
topic_type:
- apiref
api_name:
- Win32_TSVirtualIP
- Win32_TSVirtualIP.Caption
- Win32_TSVirtualIP.Description
- Win32_TSVirtualIP.InstallDate
- Win32_TSVirtualIP.Name
- Win32_TSVirtualIP.Status
- Win32_TSVirtualIP.VirtualIPActive
- Win32_TSVirtualIP.PolicySourceVirtualIPActive
- Win32_TSVirtualIP.VirtualIPMode
- Win32_TSVirtualIP.PolicySourceVirtualIPMode
- Win32_TSVirtualIP.ProgramList
- Win32_TSVirtualIP.PolicySourceProgramList
- Win32_TSVirtualIP.NetworkAdapterDescription
- Win32_TSVirtualIP.NetworkAdapterMacAddress
- Win32_TSVirtualIP.PolicySourceNetworkAdapter
- Win32_TSVirtualIP.NetworkAdapterDescriptionList
- Win32_TSVirtualIP.NetworkAdapterMacList
- Win32_TSVirtualIP.VirtualizeLoopbackAddressesEnabled
api_location:
- TSCfgWmi.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f87db04d61dda0c6034b536544362ec09e0aaa66
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103685578"
---
# <a name="win32_tsvirtualip-class"></a><span data-ttu-id="4afc0-105">Win32 \_ TSVirtualIP 類別</span><span class="sxs-lookup"><span data-stu-id="4afc0-105">Win32\_TSVirtualIP class</span></span>

<span data-ttu-id="4afc0-106">定義遠端桌面工作階段主機 (RD 工作階段主機) 伺服器 (IP) 虛擬化設定的網際網路通訊協定。</span><span class="sxs-lookup"><span data-stu-id="4afc0-106">Defines Internet protocol (IP) virtualization settings for a Remote Desktop Session Host (RD Session Host) server.</span></span>

<span data-ttu-id="4afc0-107">下列語法已經過受管理物件格式 (MOF) 程式碼簡化，並包含所有已繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="4afc0-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="4afc0-108">語法</span><span class="sxs-lookup"><span data-stu-id="4afc0-108">Syntax</span></span>

``` syntax
[dynamic, provider("Win32_WIN32_TSVIRTUALIP_Prov"), ClassContext("local|hkey_local_machine\\SYSTEM\\CurrentControlSet\\Control\\TerminalServer\\TSAppSrv\\VirtualIP"), AMENDMENT]
class Win32_TSVirtualIP : CIM_Setting
{
  string   Caption;
  string   Description;
  datetime InstallDate;
  string   Name;
  string   Status;
  uint32   VirtualIPActive;
  uint32   PolicySourceVirtualIPActive;
  uint32   VirtualIPMode;
  uint32   PolicySourceVirtualIPMode;
  string   ProgramList[];
  uint32   PolicySourceProgramList;
  string   NetworkAdapterDescription;
  string   NetworkAdapterMacAddress;
  uint32   PolicySourceNetworkAdapter;
  string   NetworkAdapterDescriptionList[];
  string   NetworkAdapterMacList[];
  uint32   VirtualizeLoopbackAddressesEnabled;
};
```

## <a name="members"></a><span data-ttu-id="4afc0-109">成員</span><span class="sxs-lookup"><span data-stu-id="4afc0-109">Members</span></span>

<span data-ttu-id="4afc0-110">**Win32 \_ TSVirtualIP** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="4afc0-110">The **Win32\_TSVirtualIP** class has these types of members:</span></span>

-   [<span data-ttu-id="4afc0-111">方法</span><span class="sxs-lookup"><span data-stu-id="4afc0-111">Methods</span></span>](#methods)
-   [<span data-ttu-id="4afc0-112">屬性</span><span class="sxs-lookup"><span data-stu-id="4afc0-112">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="4afc0-113">方法</span><span class="sxs-lookup"><span data-stu-id="4afc0-113">Methods</span></span>

<span data-ttu-id="4afc0-114">**Win32 \_ TSVirtualIP** 類別具有這些方法。</span><span class="sxs-lookup"><span data-stu-id="4afc0-114">The **Win32\_TSVirtualIP** class has these methods.</span></span>



| <span data-ttu-id="4afc0-115">方法</span><span class="sxs-lookup"><span data-stu-id="4afc0-115">Method</span></span>                                                                                                   | <span data-ttu-id="4afc0-116">描述</span><span class="sxs-lookup"><span data-stu-id="4afc0-116">Description</span></span>                                                                                                                                                                  |
|:---------------------------------------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="4afc0-117">**AddProgram**</span><span class="sxs-lookup"><span data-stu-id="4afc0-117">**AddProgram**</span></span>](addprogram-win32-tsvirtualip.md)                                                       | <span data-ttu-id="4afc0-118">將程式新增至使用 IP 虛擬化的程式清單。</span><span class="sxs-lookup"><span data-stu-id="4afc0-118">Adds a program to the list of programs that use IP virtualization.</span></span><br/>                                                                                                |
| [<span data-ttu-id="4afc0-119">**RemoveProgram**</span><span class="sxs-lookup"><span data-stu-id="4afc0-119">**RemoveProgram**</span></span>](removeprogram-win32-tsvirtualip.md)                                                 | <span data-ttu-id="4afc0-120">從使用 IP 虛擬化的程式清單中移除程式。</span><span class="sxs-lookup"><span data-stu-id="4afc0-120">Removes a program from the list of programs that use IP virtualization.</span></span><br/>                                                                                           |
| [<span data-ttu-id="4afc0-121">**SelectNetworkAdapter**</span><span class="sxs-lookup"><span data-stu-id="4afc0-121">**SelectNetworkAdapter**</span></span>](selectnetworkadapter-win32-tsvirtualip.md)                                   | <span data-ttu-id="4afc0-122">設定要用於 IP 虛擬化之網路介面卡的 MAC 位址。</span><span class="sxs-lookup"><span data-stu-id="4afc0-122">Sets the MAC address of the network adapter to use for IP virtualization.</span></span><br/>                                                                                         |
| [<span data-ttu-id="4afc0-123">**SetProgramList**</span><span class="sxs-lookup"><span data-stu-id="4afc0-123">**SetProgramList**</span></span>](setprogramlist-win32-tsvirtualip.md)                                               | <span data-ttu-id="4afc0-124">覆寫使用 IP 虛擬化的程式清單。</span><span class="sxs-lookup"><span data-stu-id="4afc0-124">Overwrites the list of programs that use IP virtualization.</span></span><br/>                                                                                                       |
| [<span data-ttu-id="4afc0-125">**SetVirtualIPActive**</span><span class="sxs-lookup"><span data-stu-id="4afc0-125">**SetVirtualIPActive**</span></span>](setvirtualipactive-win32-tsvirtualip.md)                                       | <span data-ttu-id="4afc0-126">設定 **VirtualIPActive** 屬性值。</span><span class="sxs-lookup"><span data-stu-id="4afc0-126">Sets the **VirtualIPActive** property value.</span></span><br/>                                                                                                                      |
| [<span data-ttu-id="4afc0-127">**SetVirtualIPMode**</span><span class="sxs-lookup"><span data-stu-id="4afc0-127">**SetVirtualIPMode**</span></span>](setvirtualipmode-win32-tsvirtualip.md)                                           | <span data-ttu-id="4afc0-128">設定 **VirtualIPMode** 屬性值。</span><span class="sxs-lookup"><span data-stu-id="4afc0-128">Sets the **VirtualIPMode** property value.</span></span><br/>                                                                                                                        |
| [<span data-ttu-id="4afc0-129">**SetVirtualizeLoopbackAddressesEnabled**</span><span class="sxs-lookup"><span data-stu-id="4afc0-129">**SetVirtualizeLoopbackAddressesEnabled**</span></span>](setvirtualizeloopbackaddressesenabled-win32-tsvirtualip.md) | <span data-ttu-id="4afc0-130">設定 **VirtualizeLoopbackAddressesEnabled** 屬性值。</span><span class="sxs-lookup"><span data-stu-id="4afc0-130">Sets the **VirtualizeLoopbackAddressesEnabled** property value.</span></span><br/> <span data-ttu-id="4afc0-131">**Windows Server 2008 R2：** 此方法在 Windows Server 2012 之前無法使用。</span><span class="sxs-lookup"><span data-stu-id="4afc0-131">**Windows Server 2008 R2:** This method is not available prior to Windows Server 2012.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="4afc0-132">屬性</span><span class="sxs-lookup"><span data-stu-id="4afc0-132">Properties</span></span>

<span data-ttu-id="4afc0-133">**Win32 \_ TSVirtualIP** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="4afc0-133">The **Win32\_TSVirtualIP** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="4afc0-134">**標題**</span><span class="sxs-lookup"><span data-stu-id="4afc0-134">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4afc0-135">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="4afc0-135">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="4afc0-136">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="4afc0-136">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4afc0-137">限定詞： [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64) </span><span class="sxs-lookup"><span data-stu-id="4afc0-137">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="4afc0-138">簡短描述 (物件的單行字串) 。</span><span class="sxs-lookup"><span data-stu-id="4afc0-138">Short description (one-line string) of the object.</span></span>

<span data-ttu-id="4afc0-139">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。</span><span class="sxs-lookup"><span data-stu-id="4afc0-139">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="4afc0-140">**說明**</span><span class="sxs-lookup"><span data-stu-id="4afc0-140">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4afc0-141">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="4afc0-141">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="4afc0-142">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="4afc0-142">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4afc0-143">物件的描述。</span><span class="sxs-lookup"><span data-stu-id="4afc0-143">Description of the object.</span></span>

<span data-ttu-id="4afc0-144">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。</span><span class="sxs-lookup"><span data-stu-id="4afc0-144">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="4afc0-145">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="4afc0-145">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4afc0-146">資料類型： **datetime**</span><span class="sxs-lookup"><span data-stu-id="4afc0-146">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="4afc0-147">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="4afc0-147">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4afc0-148">限定詞： [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "MIF。DMTF \| 元件 \| 001.5 ") </span><span class="sxs-lookup"><span data-stu-id="4afc0-148">Qualifiers: [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5")</span></span>
</dt> </dl>

<span data-ttu-id="4afc0-149">物件的安裝日期。</span><span class="sxs-lookup"><span data-stu-id="4afc0-149">The date the object was installed.</span></span> <span data-ttu-id="4afc0-150">缺少值並不表示物件未安裝。</span><span class="sxs-lookup"><span data-stu-id="4afc0-150">A lack of a value does not indicate that the object is not installed.</span></span>

<span data-ttu-id="4afc0-151">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。</span><span class="sxs-lookup"><span data-stu-id="4afc0-151">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="4afc0-152">**名稱**</span><span class="sxs-lookup"><span data-stu-id="4afc0-152">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4afc0-153">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="4afc0-153">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="4afc0-154">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="4afc0-154">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4afc0-155">物件的名稱。</span><span class="sxs-lookup"><span data-stu-id="4afc0-155">The name of the object.</span></span>

<span data-ttu-id="4afc0-156">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。</span><span class="sxs-lookup"><span data-stu-id="4afc0-156">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="4afc0-157">**NetworkAdapterDescription**</span><span class="sxs-lookup"><span data-stu-id="4afc0-157">**NetworkAdapterDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4afc0-158">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="4afc0-158">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="4afc0-159">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="4afc0-159">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4afc0-160">網路介面卡的描述。</span><span class="sxs-lookup"><span data-stu-id="4afc0-160">The description for the network adapter.</span></span>

</dd> <dt>

<span data-ttu-id="4afc0-161">**NetworkAdapterDescriptionList**</span><span class="sxs-lookup"><span data-stu-id="4afc0-161">**NetworkAdapterDescriptionList**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4afc0-162">資料類型： **字串** 陣列</span><span class="sxs-lookup"><span data-stu-id="4afc0-162">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="4afc0-163">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="4afc0-163">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4afc0-164">可用實體網路介面卡的描述清單。</span><span class="sxs-lookup"><span data-stu-id="4afc0-164">The list of descriptions of the available physical network adapters.</span></span>

</dd> <dt>

<span data-ttu-id="4afc0-165">**NetworkAdapterMacAddress**</span><span class="sxs-lookup"><span data-stu-id="4afc0-165">**NetworkAdapterMacAddress**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4afc0-166">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="4afc0-166">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="4afc0-167">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="4afc0-167">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4afc0-168">網路介面卡的 MAC 位址。</span><span class="sxs-lookup"><span data-stu-id="4afc0-168">The MAC address of the network adapter.</span></span>

</dd> <dt>

<span data-ttu-id="4afc0-169">**NetworkAdapterMacList**</span><span class="sxs-lookup"><span data-stu-id="4afc0-169">**NetworkAdapterMacList**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4afc0-170">資料類型： **字串** 陣列</span><span class="sxs-lookup"><span data-stu-id="4afc0-170">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="4afc0-171">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="4afc0-171">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4afc0-172">可用實體網路介面卡的 MAC 地址清單。</span><span class="sxs-lookup"><span data-stu-id="4afc0-172">The list of MAC addresses of the available physical network adapters.</span></span>

</dd> <dt>

<span data-ttu-id="4afc0-173">**PolicySourceNetworkAdapter**</span><span class="sxs-lookup"><span data-stu-id="4afc0-173">**PolicySourceNetworkAdapter**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4afc0-174">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="4afc0-174">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="4afc0-175">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="4afc0-175">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4afc0-176">指出網路介面卡是否由伺服器或群組原則設定。</span><span class="sxs-lookup"><span data-stu-id="4afc0-176">Indicates whether the network adapter is configured by the server or by group policy.</span></span>

<dt>

<span data-ttu-id="4afc0-177">0 (0x0) </span><span class="sxs-lookup"><span data-stu-id="4afc0-177">0 (0x0)</span></span>
</dt> <dd>

<span data-ttu-id="4afc0-178">伺服器</span><span class="sxs-lookup"><span data-stu-id="4afc0-178">Server</span></span>

</dd> <dt>

<span data-ttu-id="4afc0-179">1 (0x1) </span><span class="sxs-lookup"><span data-stu-id="4afc0-179">1 (0x1)</span></span>
</dt> <dd>

<span data-ttu-id="4afc0-180">群組原則</span><span class="sxs-lookup"><span data-stu-id="4afc0-180">Group policy</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="4afc0-181">**PolicySourceProgramList**</span><span class="sxs-lookup"><span data-stu-id="4afc0-181">**PolicySourceProgramList**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4afc0-182">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="4afc0-182">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="4afc0-183">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="4afc0-183">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4afc0-184">指出 **ProgramList** 屬性是由伺服器或群組原則設定。</span><span class="sxs-lookup"><span data-stu-id="4afc0-184">Indicates whether the **ProgramList** property is configured by the server or by group policy.</span></span>

<dt>

<span data-ttu-id="4afc0-185">0 (0x0) </span><span class="sxs-lookup"><span data-stu-id="4afc0-185">0 (0x0)</span></span>
</dt> <dd>

<span data-ttu-id="4afc0-186">伺服器</span><span class="sxs-lookup"><span data-stu-id="4afc0-186">Server</span></span>

</dd> <dt>

<span data-ttu-id="4afc0-187">1 (0x1) </span><span class="sxs-lookup"><span data-stu-id="4afc0-187">1 (0x1)</span></span>
</dt> <dd>

<span data-ttu-id="4afc0-188">群組原則</span><span class="sxs-lookup"><span data-stu-id="4afc0-188">Group policy</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="4afc0-189">**PolicySourceVirtualIPActive**</span><span class="sxs-lookup"><span data-stu-id="4afc0-189">**PolicySourceVirtualIPActive**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4afc0-190">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="4afc0-190">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="4afc0-191">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="4afc0-191">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4afc0-192">指出 **VirtualIPActive** 屬性是由伺服器或群組原則設定。</span><span class="sxs-lookup"><span data-stu-id="4afc0-192">Indicates if the **VirtualIPActive** property is configured by the server or by group policy.</span></span>

<dt>

<span data-ttu-id="4afc0-193">0 (0x0) </span><span class="sxs-lookup"><span data-stu-id="4afc0-193">0 (0x0)</span></span>
</dt> <dd>

<span data-ttu-id="4afc0-194">伺服器</span><span class="sxs-lookup"><span data-stu-id="4afc0-194">Server</span></span>

</dd> <dt>

<span data-ttu-id="4afc0-195">1 (0x1) </span><span class="sxs-lookup"><span data-stu-id="4afc0-195">1 (0x1)</span></span>
</dt> <dd>

<span data-ttu-id="4afc0-196">群組原則</span><span class="sxs-lookup"><span data-stu-id="4afc0-196">Group policy</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="4afc0-197">**PolicySourceVirtualIPMode**</span><span class="sxs-lookup"><span data-stu-id="4afc0-197">**PolicySourceVirtualIPMode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4afc0-198">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="4afc0-198">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="4afc0-199">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="4afc0-199">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4afc0-200">指出 **VirtualIPMode** 屬性是由伺服器或群組原則設定。</span><span class="sxs-lookup"><span data-stu-id="4afc0-200">Indicates if the **VirtualIPMode** property is configured by the server or by group policy.</span></span>

<dt>

<span data-ttu-id="4afc0-201">0 (0x0) </span><span class="sxs-lookup"><span data-stu-id="4afc0-201">0 (0x0)</span></span>
</dt> <dd>

<span data-ttu-id="4afc0-202">伺服器</span><span class="sxs-lookup"><span data-stu-id="4afc0-202">Server</span></span>

</dd> <dt>

<span data-ttu-id="4afc0-203">1 (0x1) </span><span class="sxs-lookup"><span data-stu-id="4afc0-203">1 (0x1)</span></span>
</dt> <dd>

<span data-ttu-id="4afc0-204">群組原則</span><span class="sxs-lookup"><span data-stu-id="4afc0-204">Group policy</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="4afc0-205">**ProgramList**</span><span class="sxs-lookup"><span data-stu-id="4afc0-205">**ProgramList**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4afc0-206">資料類型： **字串** 陣列</span><span class="sxs-lookup"><span data-stu-id="4afc0-206">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="4afc0-207">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="4afc0-207">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4afc0-208">指定設定為使用 IP 虛擬化的程式。</span><span class="sxs-lookup"><span data-stu-id="4afc0-208">Specifies the programs that are configured to use IP virtualization.</span></span> <span data-ttu-id="4afc0-209">這可能是程式名稱或完整路徑。</span><span class="sxs-lookup"><span data-stu-id="4afc0-209">This may a program name or the full path.</span></span>

</dd> <dt>

<span data-ttu-id="4afc0-210">**狀態**</span><span class="sxs-lookup"><span data-stu-id="4afc0-210">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4afc0-211">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="4afc0-211">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="4afc0-212">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="4afc0-212">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4afc0-213">限定詞： [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10) </span><span class="sxs-lookup"><span data-stu-id="4afc0-213">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10)</span></span>
</dt> </dl>

<span data-ttu-id="4afc0-214">物件的目前狀態。</span><span class="sxs-lookup"><span data-stu-id="4afc0-214">Current status of the object.</span></span> <span data-ttu-id="4afc0-215">您可以定義各種操作和 nonoperational 狀態。</span><span class="sxs-lookup"><span data-stu-id="4afc0-215">Various operational and nonoperational statuses can be defined.</span></span> <span data-ttu-id="4afc0-216">作業狀態包括：「正常」、「降級」和「Pred 失敗」 (元素（例如啟用智慧的硬碟）可能會正常運作，但在不久的未來) 中預測失敗。</span><span class="sxs-lookup"><span data-stu-id="4afc0-216">Operational statuses include: "OK", "Degraded", and "Pred Fail" (an element, such as a SMART-enabled hard disk drive, may be functioning properly but predicting a failure in the near future).</span></span> <span data-ttu-id="4afc0-217">Nonoperational 狀態包括：「錯誤」、「開始」、「正在停止」和「服務」。</span><span class="sxs-lookup"><span data-stu-id="4afc0-217">Nonoperational statuses include: "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="4afc0-218">後者（「服務」）可以在磁片的鏡像重新同步處理期間套用，重載使用者權限清單或其他系統管理工作。</span><span class="sxs-lookup"><span data-stu-id="4afc0-218">The latter, "Service", could apply during mirror-resilvering of a disk, reload of a user permissions list, or other administrative work.</span></span> <span data-ttu-id="4afc0-219">並非所有這類工作都是線上的，但受管理的元素並不是「確定」，也不是其中一個其他狀態。</span><span class="sxs-lookup"><span data-stu-id="4afc0-219">Not all such work is on-line, yet the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="4afc0-220">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。</span><span class="sxs-lookup"><span data-stu-id="4afc0-220">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<dt>



 <span data-ttu-id="4afc0-221"> ( [確定] ) </span><span class="sxs-lookup"><span data-stu-id="4afc0-221">("OK")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="4afc0-222"> ( 「錯誤」 ) </span><span class="sxs-lookup"><span data-stu-id="4afc0-222">("Error")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="4afc0-223"> ( 「降級」 ) </span><span class="sxs-lookup"><span data-stu-id="4afc0-223">("Degraded")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="4afc0-224"> ( 「未知」 ) </span><span class="sxs-lookup"><span data-stu-id="4afc0-224">("Unknown")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="4afc0-225"> ( 「Pred 失敗」 ) </span><span class="sxs-lookup"><span data-stu-id="4afc0-225">("Pred Fail")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="4afc0-226"> ( 「開始」 ) </span><span class="sxs-lookup"><span data-stu-id="4afc0-226">("Starting")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="4afc0-227"> ( 「正在停止」 ) </span><span class="sxs-lookup"><span data-stu-id="4afc0-227">("Stopping")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="4afc0-228"> ( "Service" ) </span><span class="sxs-lookup"><span data-stu-id="4afc0-228">("Service")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="4afc0-229">**VirtualIPActive**</span><span class="sxs-lookup"><span data-stu-id="4afc0-229">**VirtualIPActive**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4afc0-230">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="4afc0-230">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="4afc0-231">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="4afc0-231">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4afc0-232">限定詞：索引 [**鍵**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="4afc0-232">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="4afc0-233">指定伺服器上的 IP 虛擬化是否為作用中狀態。</span><span class="sxs-lookup"><span data-stu-id="4afc0-233">Specifies if IP virtualization is active on the server.</span></span> <span data-ttu-id="4afc0-234">這可以是下列其中一個值。</span><span class="sxs-lookup"><span data-stu-id="4afc0-234">This can be one of the following values.</span></span>

<dt>

<span id="FALSE"></span><span id="false"></span>

<span data-ttu-id="4afc0-235"><span id="FALSE"></span><span id="false"></span>**FALSE** (0) </span><span class="sxs-lookup"><span data-stu-id="4afc0-235"><span id="FALSE"></span><span id="false"></span>**FALSE** (0)</span></span>


</dt> <dd>

<span data-ttu-id="4afc0-236">IP 虛擬化未啟用。</span><span class="sxs-lookup"><span data-stu-id="4afc0-236">IP virtualization is not active.</span></span>

</dd> <dt>

<span id="TRUE"></span><span id="true"></span>

<span data-ttu-id="4afc0-237"><span id="TRUE"></span><span id="true"></span>**TRUE** (1) </span><span class="sxs-lookup"><span data-stu-id="4afc0-237"><span id="TRUE"></span><span id="true"></span>**TRUE** (1)</span></span>


</dt> <dd>

<span data-ttu-id="4afc0-238">IP 虛擬化處於作用中狀態。</span><span class="sxs-lookup"><span data-stu-id="4afc0-238">IP virtualization is active.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="4afc0-239">**VirtualIPMode**</span><span class="sxs-lookup"><span data-stu-id="4afc0-239">**VirtualIPMode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4afc0-240">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="4afc0-240">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="4afc0-241">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="4afc0-241">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4afc0-242">指定要在伺服器上使用的 IP 虛擬化模式。</span><span class="sxs-lookup"><span data-stu-id="4afc0-242">Specifies which IP virtualization mode is being used on the server.</span></span> <span data-ttu-id="4afc0-243">這可以是下列其中一個值。</span><span class="sxs-lookup"><span data-stu-id="4afc0-243">This can be one of the following values.</span></span>

<dt>

<span id="Per-Session"></span><span id="per-session"></span><span id="PER-SESSION"></span>

<span data-ttu-id="4afc0-244"><span id="Per-Session"></span><span id="per-session"></span><span id="PER-SESSION"></span>**每個會話** (0) </span><span class="sxs-lookup"><span data-stu-id="4afc0-244"><span id="Per-Session"></span><span id="per-session"></span><span id="PER-SESSION"></span>**Per-Session** (0)</span></span>


</dt> <dd>

<span data-ttu-id="4afc0-245">IP 虛擬化模式為每個會話。</span><span class="sxs-lookup"><span data-stu-id="4afc0-245">The IP virtualization mode is per-session.</span></span>

</dd> <dt>

<span id="Per-Program"></span><span id="per-program"></span><span id="PER-PROGRAM"></span>

<span data-ttu-id="4afc0-246"><span id="Per-Program"></span><span id="per-program"></span><span id="PER-PROGRAM"></span>**每一程式** (1) </span><span class="sxs-lookup"><span data-stu-id="4afc0-246"><span id="Per-Program"></span><span id="per-program"></span><span id="PER-PROGRAM"></span>**Per-Program** (1)</span></span>


</dt> <dd>

<span data-ttu-id="4afc0-247">IP 虛擬化模式為每位使用者。</span><span class="sxs-lookup"><span data-stu-id="4afc0-247">The IP virtualization mode is per-user.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="4afc0-248">**VirtualizeLoopbackAddressesEnabled**</span><span class="sxs-lookup"><span data-stu-id="4afc0-248">**VirtualizeLoopbackAddressesEnabled**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4afc0-249">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="4afc0-249">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="4afc0-250">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="4afc0-250">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4afc0-251">指定是否啟用回送位址虛擬化。</span><span class="sxs-lookup"><span data-stu-id="4afc0-251">Specifies whether loopback address virtualization is enabled.</span></span>

<span data-ttu-id="4afc0-252">**Windows Server 2008 R2：** 此屬性在 Windows Server 2012 之前無法使用。</span><span class="sxs-lookup"><span data-stu-id="4afc0-252">**Windows Server 2008 R2:** This property is not available prior to Windows Server 2012.</span></span>

<dt>

<span id="FALSE"></span><span id="false"></span>

<span data-ttu-id="4afc0-253"><span id="FALSE"></span><span id="false"></span>**FALSE** (0) </span><span class="sxs-lookup"><span data-stu-id="4afc0-253"><span id="FALSE"></span><span id="false"></span>**FALSE** (0)</span></span>


</dt> <dd>

<span data-ttu-id="4afc0-254">未啟用</span><span class="sxs-lookup"><span data-stu-id="4afc0-254">Not enabled</span></span>

</dd> <dt>

<span id="TRUE"></span><span id="true"></span>

<span data-ttu-id="4afc0-255"><span id="TRUE"></span><span id="true"></span>**TRUE** (1) </span><span class="sxs-lookup"><span data-stu-id="4afc0-255"><span id="TRUE"></span><span id="true"></span>**TRUE** (1)</span></span>


</dt> <dd>

<span data-ttu-id="4afc0-256">已啟用</span><span class="sxs-lookup"><span data-stu-id="4afc0-256">Enabled</span></span>

</dd> </dl>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="4afc0-257">備註</span><span class="sxs-lookup"><span data-stu-id="4afc0-257">Remarks</span></span>

<span data-ttu-id="4afc0-258">受控物件格式 (MOF) 檔包含 Windows Management Instrumentation (WMI) 類別的定義。</span><span class="sxs-lookup"><span data-stu-id="4afc0-258">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="4afc0-259">MOF 檔案不會安裝為 Microsoft Windows 軟體開發套件 (SDK) 的一部分。</span><span class="sxs-lookup"><span data-stu-id="4afc0-259">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="4afc0-260">當您使用伺服器管理員新增相關聯的角色時，它們會安裝在伺服器上。</span><span class="sxs-lookup"><span data-stu-id="4afc0-260">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="4afc0-261">如需 MOF 檔案的詳細資訊，請參閱 [受控物件格式 (mof) ](/windows/desktop/WmiSdk/managed-object-format--mof-)。</span><span class="sxs-lookup"><span data-stu-id="4afc0-261">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="4afc0-262">規格需求</span><span class="sxs-lookup"><span data-stu-id="4afc0-262">Requirements</span></span>



| <span data-ttu-id="4afc0-263">需求</span><span class="sxs-lookup"><span data-stu-id="4afc0-263">Requirement</span></span> | <span data-ttu-id="4afc0-264">值</span><span class="sxs-lookup"><span data-stu-id="4afc0-264">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="4afc0-265">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="4afc0-265">Minimum supported client</span></span><br/> | <span data-ttu-id="4afc0-266">都不支援</span><span class="sxs-lookup"><span data-stu-id="4afc0-266">None supported</span></span><br/>                                                               |
| <span data-ttu-id="4afc0-267">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="4afc0-267">Minimum supported server</span></span><br/> | <span data-ttu-id="4afc0-268">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="4afc0-268">Windows Server 2008 R2</span></span><br/>                                                       |
| <span data-ttu-id="4afc0-269">命名空間</span><span class="sxs-lookup"><span data-stu-id="4afc0-269">Namespace</span></span><br/>                | <span data-ttu-id="4afc0-270">根 \\ CIMv2 \\ microsoft-windows-terminalservices-gateway</span><span class="sxs-lookup"><span data-stu-id="4afc0-270">Root\\CIMv2\\TerminalServices</span></span><br/>                                                |
| <span data-ttu-id="4afc0-271">MOF</span><span class="sxs-lookup"><span data-stu-id="4afc0-271">MOF</span></span><br/>                      | <dl> <span data-ttu-id="4afc0-272"><dt>TSCfgWmi mof</dt></span><span class="sxs-lookup"><span data-stu-id="4afc0-272"><dt>TSCfgWmi.mof</dt></span></span> </dl> |
| <span data-ttu-id="4afc0-273">DLL</span><span class="sxs-lookup"><span data-stu-id="4afc0-273">DLL</span></span><br/>                      | <dl> <span data-ttu-id="4afc0-274"><dt>TSCfgWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="4afc0-274"><dt>TSCfgWmi.dll</dt></span></span> </dl> |



 

