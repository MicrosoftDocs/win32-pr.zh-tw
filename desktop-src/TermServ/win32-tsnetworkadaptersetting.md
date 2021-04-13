---
title: Win32_TSNetworkAdapterSetting 類別
description: 定義 Win32 終端機類別的各種設定， \_ 包括與網路介面卡相關的屬性，以及允許的最大連接數目。
ms.assetid: b8a757e6-801b-4349-902e-76596b06df1f
ms.tgt_platform: multiple
keywords:
- Win32_TSNetworkAdapterSetting 類別遠端桌面服務
- Win32_TSNetworkAdapterSetting 類別遠端桌面服務，描述
topic_type:
- apiref
api_name:
- Win32_TSNetworkAdapterSetting
- Win32_TSNetworkAdapterSetting.Caption
- Win32_TSNetworkAdapterSetting.Description
- Win32_TSNetworkAdapterSetting.InstallDate
- Win32_TSNetworkAdapterSetting.Name
- Win32_TSNetworkAdapterSetting.Status
- Win32_TSNetworkAdapterSetting.TerminalName
- Win32_TSNetworkAdapterSetting.DeviceIDList
- Win32_TSNetworkAdapterSetting.MaximumConnections
- Win32_TSNetworkAdapterSetting.NetworkAdapterID
- Win32_TSNetworkAdapterSetting.NetworkAdapterLanaID
- Win32_TSNetworkAdapterSetting.NetworkAdapterList
- Win32_TSNetworkAdapterSetting.NetworkAdapterName
- Win32_TSNetworkAdapterSetting.PolicySourceMaximumConnections
api_location:
- TSCfgWmi.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6f2f2f1ac7d6bf4b1fd3fb5f5a92fc4fd5260a92
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104465964"
---
# <a name="win32_tsnetworkadaptersetting-class"></a><span data-ttu-id="45080-105">Win32 \_ TSNetworkAdapterSetting 類別</span><span class="sxs-lookup"><span data-stu-id="45080-105">Win32\_TSNetworkAdapterSetting class</span></span>

<span data-ttu-id="45080-106">**Win32 \_ TSNetworkAdapterSetting** WMI 類別會定義 [**win32 \_ 終端**](win32-terminal.md)機類別的各種設定，包括與網路介面卡相關的屬性，以及允許的最大連接數目。</span><span class="sxs-lookup"><span data-stu-id="45080-106">The **Win32\_TSNetworkAdapterSetting** WMI class defines various configuration settings for the [**Win32\_Terminal**](win32-terminal.md) class including properties related to the network adapter and the maximum number of connections allowed.</span></span>

<span data-ttu-id="45080-107">下列語法簡化自 MOF 程式碼，並依字母順序包含所有定義和繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="45080-107">The following syntax is simplified from MOF code and includes all defined and inherited properties, in alphabetical order.</span></span> <span data-ttu-id="45080-108">如需方法的參考資訊，請參閱本主題稍後的方法表格。</span><span class="sxs-lookup"><span data-stu-id="45080-108">For reference information on methods, see the table of methods later in this topic.</span></span>

## <a name="syntax"></a><span data-ttu-id="45080-109">語法</span><span class="sxs-lookup"><span data-stu-id="45080-109">Syntax</span></span>

``` syntax
[dynamic, provider("Win32_WIN32_TSNETWORKADAPTERSETTING_Prov"), ClassContext("local|hkey_local_machine\\SYSTEM\\CurrentControlSet\\Control\\TerminalServer\\WinStations"), AMENDMENT]
class Win32_TSNetworkAdapterSetting : Win32_TerminalSetting
{
  string   Caption;
  string   Description;
  datetime InstallDate;
  string   Name;
  string   Status;
  string   TerminalName;
  string   DeviceIDList[];
  uint32   MaximumConnections;
  string   NetworkAdapterID;
  uint32   NetworkAdapterLanaID;
  string   NetworkAdapterList[];
  string   NetworkAdapterName;
  uint32   PolicySourceMaximumConnections;
};
```

## <a name="members"></a><span data-ttu-id="45080-110">成員</span><span class="sxs-lookup"><span data-stu-id="45080-110">Members</span></span>

<span data-ttu-id="45080-111">**Win32 \_ TSNetworkAdapterSetting** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="45080-111">The **Win32\_TSNetworkAdapterSetting** class has these types of members:</span></span>

-   [<span data-ttu-id="45080-112">方法</span><span class="sxs-lookup"><span data-stu-id="45080-112">Methods</span></span>](#methods)
-   [<span data-ttu-id="45080-113">屬性</span><span class="sxs-lookup"><span data-stu-id="45080-113">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="45080-114">方法</span><span class="sxs-lookup"><span data-stu-id="45080-114">Methods</span></span>

<span data-ttu-id="45080-115">**Win32 \_ TSNetworkAdapterSetting** 類別具有這些方法。</span><span class="sxs-lookup"><span data-stu-id="45080-115">The **Win32\_TSNetworkAdapterSetting** class has these methods.</span></span>



| <span data-ttu-id="45080-116">方法</span><span class="sxs-lookup"><span data-stu-id="45080-116">Method</span></span>                                                                                     | <span data-ttu-id="45080-117">描述</span><span class="sxs-lookup"><span data-stu-id="45080-117">Description</span></span>                                                                                              |
|:-------------------------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="45080-118">**SelectAllNetworkAdapters**</span><span class="sxs-lookup"><span data-stu-id="45080-118">**SelectAllNetworkAdapters**</span></span>](win32-tsnetworkadaptersetting-selectallnetworkadapters.md) | <span data-ttu-id="45080-119">選取所有網路介面卡。</span><span class="sxs-lookup"><span data-stu-id="45080-119">Selects all network adapters.</span></span><br/>                                                                 |
| [<span data-ttu-id="45080-120">**SelectNetworkAdapterIP**</span><span class="sxs-lookup"><span data-stu-id="45080-120">**SelectNetworkAdapterIP**</span></span>](win32-tsnetworkadaptersetting-selectnetworkadapterip.md)     | <span data-ttu-id="45080-121">選取以介面卡的 IP 位址為基礎的網路介面卡。</span><span class="sxs-lookup"><span data-stu-id="45080-121">Selects a network adapter based on the adapter's IP address.</span></span><br/>                                  |
| [<span data-ttu-id="45080-122">**SetNetworkAdapterLanaID**</span><span class="sxs-lookup"><span data-stu-id="45080-122">**SetNetworkAdapterLanaID**</span></span>](setnetworkadapterlanaid-win32-tsnetworkadaptersetting.md)   | <span data-ttu-id="45080-123">指定要設定的網路介面卡 (LANA) 號碼的 NetBIOS 局域網路介面卡。</span><span class="sxs-lookup"><span data-stu-id="45080-123">Specifies the NetBIOS Local Area Network Adapter (LANA) number of the network adapter to set.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="45080-124">屬性</span><span class="sxs-lookup"><span data-stu-id="45080-124">Properties</span></span>

<span data-ttu-id="45080-125">**Win32 \_ TSNetworkAdapterSetting** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="45080-125">The **Win32\_TSNetworkAdapterSetting** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="45080-126">**標題**</span><span class="sxs-lookup"><span data-stu-id="45080-126">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="45080-127">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="45080-127">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="45080-128">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="45080-128">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="45080-129">限定詞： [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64) </span><span class="sxs-lookup"><span data-stu-id="45080-129">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="45080-130">簡短描述 (物件的單行字串) 。</span><span class="sxs-lookup"><span data-stu-id="45080-130">Short description (one-line string) of the object.</span></span>

<span data-ttu-id="45080-131">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。</span><span class="sxs-lookup"><span data-stu-id="45080-131">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="45080-132">**說明**</span><span class="sxs-lookup"><span data-stu-id="45080-132">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="45080-133">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="45080-133">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="45080-134">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="45080-134">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="45080-135">物件的描述。</span><span class="sxs-lookup"><span data-stu-id="45080-135">Description of the object.</span></span>

<span data-ttu-id="45080-136">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。</span><span class="sxs-lookup"><span data-stu-id="45080-136">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="45080-137">**DeviceIDList**</span><span class="sxs-lookup"><span data-stu-id="45080-137">**DeviceIDList**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="45080-138">資料類型： **字串** 陣列</span><span class="sxs-lookup"><span data-stu-id="45080-138">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="45080-139">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="45080-139">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="45080-140">在 **NetworkAdapterList** 屬性陣列中傳回的實體網路介面卡順序傳回之可用裝置識別碼的字串陣列。</span><span class="sxs-lookup"><span data-stu-id="45080-140">String array of available device IDs returned in the order of physical network adapters returned in the **NetworkAdapterList** property array.</span></span> <span data-ttu-id="45080-141">裝置識別碼值是 [**Win32 \_ NetworkAdapter**](/windows/desktop/CIMWin32Prov/win32-networkadapter)中的 **DeviceID** 屬性</span><span class="sxs-lookup"><span data-stu-id="45080-141">The device ID value is the **DeviceID** property in [**Win32\_NetworkAdapter**](/windows/desktop/CIMWin32Prov/win32-networkadapter)</span></span>

</dd> <dt>

<span data-ttu-id="45080-142">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="45080-142">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="45080-143">資料類型： **datetime**</span><span class="sxs-lookup"><span data-stu-id="45080-143">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="45080-144">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="45080-144">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="45080-145">限定詞： [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "MIF。DMTF \| 元件 \| 001.5 ") </span><span class="sxs-lookup"><span data-stu-id="45080-145">Qualifiers: [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5")</span></span>
</dt> </dl>

<span data-ttu-id="45080-146">物件的安裝日期。</span><span class="sxs-lookup"><span data-stu-id="45080-146">The date the object was installed.</span></span> <span data-ttu-id="45080-147">缺少值並不表示物件未安裝。</span><span class="sxs-lookup"><span data-stu-id="45080-147">A lack of a value does not indicate that the object is not installed.</span></span>

<span data-ttu-id="45080-148">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。</span><span class="sxs-lookup"><span data-stu-id="45080-148">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="45080-149">**MaximumConnections**</span><span class="sxs-lookup"><span data-stu-id="45080-149">**MaximumConnections**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="45080-150">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="45080-150">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="45080-151">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="45080-151">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="45080-152">允許的最大連接數目。</span><span class="sxs-lookup"><span data-stu-id="45080-152">The maximum number of connections allowed.</span></span> <span data-ttu-id="45080-153">值 **MAXINT** 代表不限數目的連接。</span><span class="sxs-lookup"><span data-stu-id="45080-153">The value **MAXINT** denotes an unlimited number of connections.</span></span>

</dd> <dt>

<span data-ttu-id="45080-154">**名稱**</span><span class="sxs-lookup"><span data-stu-id="45080-154">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="45080-155">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="45080-155">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="45080-156">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="45080-156">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="45080-157">物件的名稱。</span><span class="sxs-lookup"><span data-stu-id="45080-157">The name of the object.</span></span>

<span data-ttu-id="45080-158">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。</span><span class="sxs-lookup"><span data-stu-id="45080-158">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="45080-159">**NetworkAdapterID**</span><span class="sxs-lookup"><span data-stu-id="45080-159">**NetworkAdapterID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="45080-160">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="45080-160">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="45080-161">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="45080-161">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="45080-162">GUID，代表要設定之網路介面卡的識別碼。</span><span class="sxs-lookup"><span data-stu-id="45080-162">The GUID that represents the ID of the network adapter to set.</span></span> <span data-ttu-id="45080-163">由所有零組成的 **GUID** 表示所有網路介面卡。</span><span class="sxs-lookup"><span data-stu-id="45080-163">A **GUID** that consists of all zeros denotes all network adapters.</span></span>

</dd> <dt>

<span data-ttu-id="45080-164">**NetworkAdapterLanaID**</span><span class="sxs-lookup"><span data-stu-id="45080-164">**NetworkAdapterLanaID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="45080-165">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="45080-165">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="45080-166">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="45080-166">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="45080-167">NetBIOS 局域網路介面卡 (LANA) 用來識別指派給終端機之網路介面卡的網路介面卡編號。</span><span class="sxs-lookup"><span data-stu-id="45080-167">NetBIOS Local Area Network Adapter (LANA) number of the network adapter that is used to identify the network adapter assigned to the terminal.</span></span>

</dd> <dt>

<span data-ttu-id="45080-168">**NetworkAdapterList**</span><span class="sxs-lookup"><span data-stu-id="45080-168">**NetworkAdapterList**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="45080-169">資料類型： **字串** 陣列</span><span class="sxs-lookup"><span data-stu-id="45080-169">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="45080-170">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="45080-170">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="45080-171">可用實體網路介面卡的字串陣列和對應的裝置識別碼。</span><span class="sxs-lookup"><span data-stu-id="45080-171">String array of available physical network adapters and the corresponding device IDs.</span></span> <span data-ttu-id="45080-172">裝置識別碼是 [**Win32 \_ NetworkAdapter**](/windows/desktop/CIMWin32Prov/win32-networkadapter)中的 **DeviceID** 屬性。</span><span class="sxs-lookup"><span data-stu-id="45080-172">The device IDs are the **DeviceID** property in [**Win32\_NetworkAdapter**](/windows/desktop/CIMWin32Prov/win32-networkadapter).</span></span>

</dd> <dt>

<span data-ttu-id="45080-173">**NetworkAdapterName**</span><span class="sxs-lookup"><span data-stu-id="45080-173">**NetworkAdapterName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="45080-174">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="45080-174">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="45080-175">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="45080-175">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="45080-176">要設定之網路介面卡的描述。</span><span class="sxs-lookup"><span data-stu-id="45080-176">Description of the network adapter to set.</span></span> <span data-ttu-id="45080-177">此值位於 [**Win32 \_ >networkadapterconfiguration**](/windows/desktop/CIMWin32Prov/win32-networkadapterconfiguration)中。</span><span class="sxs-lookup"><span data-stu-id="45080-177">This value is in [**Win32\_NetworkAdapterConfiguration**](/windows/desktop/CIMWin32Prov/win32-networkadapterconfiguration).</span></span>

</dd> <dt>

<span data-ttu-id="45080-178">**PolicySourceMaximumConnections**</span><span class="sxs-lookup"><span data-stu-id="45080-178">**PolicySourceMaximumConnections**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="45080-179">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="45080-179">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="45080-180">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="45080-180">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="45080-181">指出 **MaximumConnections** 屬性是由伺服器、群組原則或預設設定。</span><span class="sxs-lookup"><span data-stu-id="45080-181">Indicates whether the **MaximumConnections** property is configured by the server, group policy, or by default.</span></span>

<dt>

<span data-ttu-id="45080-182">0</span><span class="sxs-lookup"><span data-stu-id="45080-182">0</span></span>
</dt> <dd>

<span data-ttu-id="45080-183">伺服器</span><span class="sxs-lookup"><span data-stu-id="45080-183">Server</span></span>

</dd> <dt>

<span data-ttu-id="45080-184">1</span><span class="sxs-lookup"><span data-stu-id="45080-184">1</span></span>
</dt> <dd>

<span data-ttu-id="45080-185">群組原則</span><span class="sxs-lookup"><span data-stu-id="45080-185">Group policy</span></span>

</dd> <dt>

<span data-ttu-id="45080-186">2</span><span class="sxs-lookup"><span data-stu-id="45080-186">2</span></span>
</dt> <dd>

<span data-ttu-id="45080-187">預設</span><span class="sxs-lookup"><span data-stu-id="45080-187">Default</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="45080-188">**狀態**</span><span class="sxs-lookup"><span data-stu-id="45080-188">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="45080-189">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="45080-189">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="45080-190">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="45080-190">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="45080-191">限定詞： [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10) </span><span class="sxs-lookup"><span data-stu-id="45080-191">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10)</span></span>
</dt> </dl>

<span data-ttu-id="45080-192">物件的目前狀態。</span><span class="sxs-lookup"><span data-stu-id="45080-192">Current status of the object.</span></span> <span data-ttu-id="45080-193">您可以定義各種操作和 nonoperational 狀態。</span><span class="sxs-lookup"><span data-stu-id="45080-193">Various operational and nonoperational statuses can be defined.</span></span> <span data-ttu-id="45080-194">作業狀態包括：「正常」、「降級」和「Pred 失敗」 (元素（例如啟用智慧的硬碟）可能會正常運作，但在不久的未來) 中預測失敗。</span><span class="sxs-lookup"><span data-stu-id="45080-194">Operational statuses include: "OK", "Degraded", and "Pred Fail" (an element, such as a SMART-enabled hard disk drive, may be functioning properly but predicting a failure in the near future).</span></span> <span data-ttu-id="45080-195">Nonoperational 狀態包括：「錯誤」、「開始」、「正在停止」和「服務」。</span><span class="sxs-lookup"><span data-stu-id="45080-195">Nonoperational statuses include: "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="45080-196">後者（「服務」）可以在磁片的鏡像重新同步處理期間套用，重載使用者權限清單或其他系統管理工作。</span><span class="sxs-lookup"><span data-stu-id="45080-196">The latter, "Service", could apply during mirror-resilvering of a disk, reload of a user permissions list, or other administrative work.</span></span> <span data-ttu-id="45080-197">並非所有這類工作都是線上的，但受管理的元素並不是「確定」，也不是其中一個其他狀態。</span><span class="sxs-lookup"><span data-stu-id="45080-197">Not all such work is on-line, yet the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="45080-198">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。</span><span class="sxs-lookup"><span data-stu-id="45080-198">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<dt>



 <span data-ttu-id="45080-199"> ( [確定] ) </span><span class="sxs-lookup"><span data-stu-id="45080-199">("OK")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="45080-200"> ( 「錯誤」 ) </span><span class="sxs-lookup"><span data-stu-id="45080-200">("Error")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="45080-201"> ( 「降級」 ) </span><span class="sxs-lookup"><span data-stu-id="45080-201">("Degraded")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="45080-202"> ( 「未知」 ) </span><span class="sxs-lookup"><span data-stu-id="45080-202">("Unknown")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="45080-203"> ( 「Pred 失敗」 ) </span><span class="sxs-lookup"><span data-stu-id="45080-203">("Pred Fail")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="45080-204"> ( 「開始」 ) </span><span class="sxs-lookup"><span data-stu-id="45080-204">("Starting")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="45080-205"> ( 「正在停止」 ) </span><span class="sxs-lookup"><span data-stu-id="45080-205">("Stopping")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="45080-206"> ( "Service" ) </span><span class="sxs-lookup"><span data-stu-id="45080-206">("Service")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="45080-207">**TerminalName**</span><span class="sxs-lookup"><span data-stu-id="45080-207">**TerminalName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="45080-208">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="45080-208">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="45080-209">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="45080-209">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="45080-210">終端機的名稱。</span><span class="sxs-lookup"><span data-stu-id="45080-210">The name of the terminal.</span></span>

<span data-ttu-id="45080-211">這個屬性繼承自 [**Win32 \_ TerminalSetting**](win32-terminalsetting.md)。</span><span class="sxs-lookup"><span data-stu-id="45080-211">This property is inherited from [**Win32\_TerminalSetting**](win32-terminalsetting.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="45080-212">備註</span><span class="sxs-lookup"><span data-stu-id="45080-212">Remarks</span></span>

<span data-ttu-id="45080-213">請注意，與主控台會話相關聯的 Winstations 無法存取此類別的方法和屬性。</span><span class="sxs-lookup"><span data-stu-id="45080-213">Be aware that Winstations associated with the console session cannot access the methods and properties of this class.</span></span> <span data-ttu-id="45080-214">如果嘗試將 "Console" 指定為 TerminalName 屬性的值，則此物件的方法會傳回 **\_ \_ 不 \_ 支援的 WBEM E**。</span><span class="sxs-lookup"><span data-stu-id="45080-214">If an attempt is made to do so by specifying "Console" as the value of the TerminalName property, methods of this object return **WBEM\_E\_NOT\_SUPPORTED**.</span></span> <span data-ttu-id="45080-215">如果視窗工作站嘗試呼叫此物件的方法來新增或修改 LocalSystem、LocalService 或 NetworkService 帳戶的安全性屬性，也會傳回此錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="45080-215">This error code is also returned if a window station attempts to call methods of this object to add or modify the security properties of the LocalSystem, LocalService, or NetworkService accounts.</span></span>

<span data-ttu-id="45080-216">若要連接到「根 \\ CIMV2 \\ microsoft-windows-terminalservices-gateway」命名空間，驗證層級必須包含封包隱私權。</span><span class="sxs-lookup"><span data-stu-id="45080-216">To connect to the "Root\\CIMV2\\TerminalServices" namespace, the authentication level must include packet privacy.</span></span> <span data-ttu-id="45080-217">針對 C/c + + 呼叫，這是 **RPC \_ C \_ 驗證 \_ level \_ PKT \_ 隱私權** 的驗證層級。</span><span class="sxs-lookup"><span data-stu-id="45080-217">For C/C++ calls, this is an authentication level of **RPC\_C\_AUTHN\_LEVEL\_PKT\_PRIVACY**.</span></span> <span data-ttu-id="45080-218">針對 Visual Basic 和腳本呼叫，這是 **WbemAuthenticationLevelPktPrivacy** 或 "pktPrivacy" 的驗證層級，其值為6。</span><span class="sxs-lookup"><span data-stu-id="45080-218">For Visual Basic and scripting calls, this is an authentication level of **WbemAuthenticationLevelPktPrivacy** or "pktPrivacy", with a value of 6.</span></span> <span data-ttu-id="45080-219">下列 Visual Basic Scripting Edition (VBScript) 範例示範如何連接到具有封包隱私權的遠端電腦。</span><span class="sxs-lookup"><span data-stu-id="45080-219">The following Visual Basic Scripting Edition (VBScript) example shows how to connect to a remote computer with packet privacy.</span></span>


```VB
strComputer = "RemoteServer1" 
Set objServices = GetObject( _
    "winmgmts:{authenticationLevel=pktPrivacy}!Root/CIMv2/TerminalServices")
```



<span data-ttu-id="45080-220">受控物件格式 (MOF) 檔包含 Windows Management Instrumentation (WMI) 類別的定義。</span><span class="sxs-lookup"><span data-stu-id="45080-220">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="45080-221">MOF 檔案不會安裝為 Microsoft Windows 軟體開發套件 (SDK) 的一部分。</span><span class="sxs-lookup"><span data-stu-id="45080-221">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="45080-222">當您使用伺服器管理員新增相關聯的角色時，它們會安裝在伺服器上。</span><span class="sxs-lookup"><span data-stu-id="45080-222">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="45080-223">如需 MOF 檔案的詳細資訊，請參閱 [受控物件格式 (mof) ](/windows/desktop/WmiSdk/managed-object-format--mof-)。</span><span class="sxs-lookup"><span data-stu-id="45080-223">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="45080-224">規格需求</span><span class="sxs-lookup"><span data-stu-id="45080-224">Requirements</span></span>



| <span data-ttu-id="45080-225">需求</span><span class="sxs-lookup"><span data-stu-id="45080-225">Requirement</span></span> | <span data-ttu-id="45080-226">值</span><span class="sxs-lookup"><span data-stu-id="45080-226">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="45080-227">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="45080-227">Minimum supported client</span></span><br/> | <span data-ttu-id="45080-228">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="45080-228">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="45080-229">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="45080-229">Minimum supported server</span></span><br/> | <span data-ttu-id="45080-230">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="45080-230">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="45080-231">命名空間</span><span class="sxs-lookup"><span data-stu-id="45080-231">Namespace</span></span><br/>                | <span data-ttu-id="45080-232">根 \\ CIMv2 \\ microsoft-windows-terminalservices-gateway</span><span class="sxs-lookup"><span data-stu-id="45080-232">Root\\CIMv2\\TerminalServices</span></span><br/>                                                |
| <span data-ttu-id="45080-233">MOF</span><span class="sxs-lookup"><span data-stu-id="45080-233">MOF</span></span><br/>                      | <dl> <span data-ttu-id="45080-234"><dt>TSCfgWmi mof</dt></span><span class="sxs-lookup"><span data-stu-id="45080-234"><dt>TSCfgWmi.mof</dt></span></span> </dl> |
| <span data-ttu-id="45080-235">DLL</span><span class="sxs-lookup"><span data-stu-id="45080-235">DLL</span></span><br/>                      | <dl> <span data-ttu-id="45080-236"><dt>TSCfgWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="45080-236"><dt>TSCfgWmi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="45080-237">另請參閱</span><span class="sxs-lookup"><span data-stu-id="45080-237">See also</span></span>

<dl> <dt>

[<span data-ttu-id="45080-238">**Win32 \_ NetworkAdapter**</span><span class="sxs-lookup"><span data-stu-id="45080-238">**Win32\_NetworkAdapter**</span></span>](/windows/desktop/CIMWin32Prov/win32-networkadapter)
</dt> <dt>

[<span data-ttu-id="45080-239">**Win32 \_ >networkadapterconfiguration**</span><span class="sxs-lookup"><span data-stu-id="45080-239">**Win32\_NetworkAdapterConfiguration**</span></span>](/windows/desktop/CIMWin32Prov/win32-networkadapterconfiguration)
</dt> <dt>

[<span data-ttu-id="45080-240">**Win32 \_ TerminalSetting**</span><span class="sxs-lookup"><span data-stu-id="45080-240">**Win32\_TerminalSetting**</span></span>](win32-terminalsetting.md)
</dt> <dt>

[<span data-ttu-id="45080-241">**Win32 \_ TSNetworkAdapterListSetting**</span><span class="sxs-lookup"><span data-stu-id="45080-241">**Win32\_TSNetworkAdapterListSetting**</span></span>](win32-tsnetworkadapterlistsetting.md)
</dt> </dl>

 

