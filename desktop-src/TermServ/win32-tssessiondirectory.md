---
title: Win32_TSSessionDirectory 類別
description: 定義 Win32 TSSessionDirectorySetting 類別的遠端桌面連線代理人 (RD 連線代理人) 設定 \_ 。
ms.assetid: ef9042c2-4a35-49e9-b195-fb37c0919068
ms.tgt_platform: multiple
keywords:
- Win32_TSSessionDirectory 類別遠端桌面服務
- Win32_TSSessionDirectory 類別遠端桌面服務，描述
topic_type:
- apiref
api_name:
- Win32_TSSessionDirectory
- Win32_TSSessionDirectory.Caption
- Win32_TSSessionDirectory.Description
- Win32_TSSessionDirectory.InstallDate
- Win32_TSSessionDirectory.Name
- Win32_TSSessionDirectory.Status
- Win32_TSSessionDirectory.SessionDirectoryLocation
- Win32_TSSessionDirectory.PolicySourceSessionDirectoryLocation
- Win32_TSSessionDirectory.SessionDirectoryActive
- Win32_TSSessionDirectory.PolicySourceSessionDirectoryActive
- Win32_TSSessionDirectory.SessionDirectoryExposeServerIP
- Win32_TSSessionDirectory.PolicySourceSessionDirectoryExposeServerIP
- Win32_TSSessionDirectory.SessionDirectoryClusterName
- Win32_TSSessionDirectory.PolicySourceLoadBalancing
- Win32_TSSessionDirectory.GetLoadBalancingState
- Win32_TSSessionDirectory.GetServerWeight
- Win32_TSSessionDirectory.PolicySourceSessionDirectoryClusterName
- Win32_TSSessionDirectory.SessionDirectoryIPAddress
- Win32_TSSessionDirectory.GetTSRedirectorMode
- Win32_TSSessionDirectory.PolicySourceTSRedirectorMode
api_location:
- TSCfgWmi.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fb50ed77b99f415ae551dfcf69655af5c1d77501
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103934228"
---
# <a name="win32_tssessiondirectory-class"></a><span data-ttu-id="b83ad-105">Win32 \_ TSSessionDirectory 類別</span><span class="sxs-lookup"><span data-stu-id="b83ad-105">Win32\_TSSessionDirectory class</span></span>

<span data-ttu-id="b83ad-106">定義 [**Win32 \_ TSSessionDirectorySetting**](win32-tssessiondirectorysetting.md) 類別的遠端桌面連線代理人 (RD 連線代理人) 設定。</span><span class="sxs-lookup"><span data-stu-id="b83ad-106">Defines the Remote Desktop Connection Broker (RD Connection Broker) configuration settings for the [**Win32\_TSSessionDirectorySetting**](win32-tssessiondirectorysetting.md) class.</span></span>

> [!Note]  
> <span data-ttu-id="b83ad-107">在 Windows Server 2008 R2 中，終端機服務會話代理人 (TS 會話代理人) 的名稱已變更為 RD 連線代理人。</span><span class="sxs-lookup"><span data-stu-id="b83ad-107">In Windows Server 2008 R2, the name of Terminal Services Session Broker (TS Session Broker) was changed to RD Connection Broker.</span></span> <span data-ttu-id="b83ad-108">除非另有說明，否則這些屬性適用于所有支援的作業系統。</span><span class="sxs-lookup"><span data-stu-id="b83ad-108">These properties apply to all supported operating systems unless otherwise noted.</span></span>

 

<span data-ttu-id="b83ad-109">下列語法簡化自 MOF 程式碼，並依字母順序包含所有定義和繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="b83ad-109">The following syntax is simplified from MOF code and includes all defined and inherited properties, in alphabetical order.</span></span> <span data-ttu-id="b83ad-110">如需方法的參考資訊，請參閱本主題稍後的方法表格。</span><span class="sxs-lookup"><span data-stu-id="b83ad-110">For reference information about methods, see the table of methods later in this topic.</span></span>

## <a name="syntax"></a><span data-ttu-id="b83ad-111">語法</span><span class="sxs-lookup"><span data-stu-id="b83ad-111">Syntax</span></span>

``` syntax
[dynamic, provider("Win32_WIN32_TSSESSIONDIRECTORY_Prov"), ClassContext("local|hkey_local_machine\\SYSTEM\\CurrentControlSet\\Control\\TerminalServer"), AMENDMENT]
class Win32_TSSessionDirectory : CIM_Setting
{
  string   Caption;
  string   Description;
  datetime InstallDate;
  string   Name;
  string   Status;
  string   SessionDirectoryLocation;
  uint32   PolicySourceSessionDirectoryLocation;
  uint32   SessionDirectoryActive;
  uint32   PolicySourceSessionDirectoryActive;
  uint32   SessionDirectoryExposeServerIP;
  uint32   PolicySourceSessionDirectoryExposeServerIP;
  string   SessionDirectoryClusterName;
  uint32   PolicySourceLoadBalancing;
  uint32   GetLoadBalancingState;
  uint32   GetServerWeight;
  uint32   PolicySourceSessionDirectoryClusterName;
  string   SessionDirectoryIPAddress;
  uint32   GetTSRedirectorMode;
  uint32   PolicySourceTSRedirectorMode;
};
```

## <a name="members"></a><span data-ttu-id="b83ad-112">成員</span><span class="sxs-lookup"><span data-stu-id="b83ad-112">Members</span></span>

<span data-ttu-id="b83ad-113">**Win32 \_ TSSessionDirectory** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="b83ad-113">The **Win32\_TSSessionDirectory** class has these types of members:</span></span>

-   [<span data-ttu-id="b83ad-114">方法</span><span class="sxs-lookup"><span data-stu-id="b83ad-114">Methods</span></span>](#methods)
-   [<span data-ttu-id="b83ad-115">屬性</span><span class="sxs-lookup"><span data-stu-id="b83ad-115">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="b83ad-116">方法</span><span class="sxs-lookup"><span data-stu-id="b83ad-116">Methods</span></span>

<span data-ttu-id="b83ad-117">**Win32 \_ TSSessionDirectory** 類別具有這些方法。</span><span class="sxs-lookup"><span data-stu-id="b83ad-117">The **Win32\_TSSessionDirectory** class has these methods.</span></span>



| <span data-ttu-id="b83ad-118">方法</span><span class="sxs-lookup"><span data-stu-id="b83ad-118">Method</span></span>                                                                                                  | <span data-ttu-id="b83ad-119">描述</span><span class="sxs-lookup"><span data-stu-id="b83ad-119">Description</span></span>                                                                                                  |
|:--------------------------------------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="b83ad-120">**CreateUserDiskTemplate**</span><span class="sxs-lookup"><span data-stu-id="b83ad-120">**CreateUserDiskTemplate**</span></span>](createuserdisktemplate-win32-tssessiondirectory.md)                       | <span data-ttu-id="b83ad-121">建立使用者磁片範本。</span><span class="sxs-lookup"><span data-stu-id="b83ad-121">Creates a user disk template.</span></span><br/>                                                                     |
| [<span data-ttu-id="b83ad-122">**DisableUserVhd**</span><span class="sxs-lookup"><span data-stu-id="b83ad-122">**DisableUserVhd**</span></span>](disableuservhd-win32-tssessiondirectory.md)                                       | <span data-ttu-id="b83ad-123">停用使用者設定檔 VHD。</span><span class="sxs-lookup"><span data-stu-id="b83ad-123">Disables a user profile VHD.</span></span><br/>                                                                      |
| [<span data-ttu-id="b83ad-124">**EnableUserVhd**</span><span class="sxs-lookup"><span data-stu-id="b83ad-124">**EnableUserVhd**</span></span>](enableuservhd-win32-tssessiondirectory.md)                                         | <span data-ttu-id="b83ad-125">在 RDSH 伺服器上啟用使用者設定檔 VHD。</span><span class="sxs-lookup"><span data-stu-id="b83ad-125">Enables a user profile VHD on an RDSH server.</span></span><br/>                                                     |
| [<span data-ttu-id="b83ad-126">**GetCurrentRedirectableAddresses**</span><span class="sxs-lookup"><span data-stu-id="b83ad-126">**GetCurrentRedirectableAddresses**</span></span>](getcurrentredirectableaddresses-win32-tssessiondirectory.md)     | <span data-ttu-id="b83ad-127">取得目前設定的 DNS 合格地址清單和重新導向類型。</span><span class="sxs-lookup"><span data-stu-id="b83ad-127">Obtains the currently configured list of DNS eligible addresses, and the redirection type.</span></span><br/>        |
| [<span data-ttu-id="b83ad-128">**GetRedirectableAddresses**</span><span class="sxs-lookup"><span data-stu-id="b83ad-128">**GetRedirectableAddresses**</span></span>](getredirectableaddresses-win32-tssessiondirectory.md)                   | <span data-ttu-id="b83ad-129">取得 DNS 合格位址的完整清單。</span><span class="sxs-lookup"><span data-stu-id="b83ad-129">Obtains the entire list of DNS eligible addresses.</span></span><br/>                                                |
| [<span data-ttu-id="b83ad-130">**PingSessionDirectory**</span><span class="sxs-lookup"><span data-stu-id="b83ad-130">**PingSessionDirectory**</span></span>](pingsessiondirectory-win32-tssessiondirectory.md)                           | <span data-ttu-id="b83ad-131">檢查 RD 連線代理人伺服器是否可供使用。</span><span class="sxs-lookup"><span data-stu-id="b83ad-131">Checks whether the RD Connection Broker server is available.</span></span><br/>                                      |
| [<span data-ttu-id="b83ad-132">**SetCurrentRedirectableAddresses**</span><span class="sxs-lookup"><span data-stu-id="b83ad-132">**SetCurrentRedirectableAddresses**</span></span>](setcurrentredirectableaddresses-win32-tssessiondirectory.md)     | <span data-ttu-id="b83ad-133">設定 DNS 合格位址和重新導向類型的已設定清單。</span><span class="sxs-lookup"><span data-stu-id="b83ad-133">Sets the configured list of DNS eligible addresses, and the redirection type.</span></span><br/>                     |
| [<span data-ttu-id="b83ad-134">**SetLoadBalancingState**</span><span class="sxs-lookup"><span data-stu-id="b83ad-134">**SetLoadBalancingState**</span></span>](setloadbalancingstate-win32-tssessiondirectory.md)                         | <span data-ttu-id="b83ad-135">設定值，指出伺服器是否將參與 RD 連線代理人負載平衡。</span><span class="sxs-lookup"><span data-stu-id="b83ad-135">Sets the value to indicate if the server will participate in RD Connection Broker load balancing.</span></span><br/> |
| [<span data-ttu-id="b83ad-136">**SetServerWeight**</span><span class="sxs-lookup"><span data-stu-id="b83ad-136">**SetServerWeight**</span></span>](setserverweight-win32-tssessiondirectory.md)                                     | <span data-ttu-id="b83ad-137">設定 RD 連線代理人負載平衡的伺服器加權值。</span><span class="sxs-lookup"><span data-stu-id="b83ad-137">Sets the server weight value for RD Connection Broker load balancing.</span></span><br/>                             |
| [<span data-ttu-id="b83ad-138">**SetSessionDirectoryActive**</span><span class="sxs-lookup"><span data-stu-id="b83ad-138">**SetSessionDirectoryActive**</span></span>](win32-tssessiondirectory-setsessiondirectoryactive.md)                 | <span data-ttu-id="b83ad-139">停用並啟用 RD 連線代理人。</span><span class="sxs-lookup"><span data-stu-id="b83ad-139">Disables and enables the RD Connection Broker.</span></span><br/>                                                    |
| [<span data-ttu-id="b83ad-140">**SetSessionDirectoryExposeServerIP**</span><span class="sxs-lookup"><span data-stu-id="b83ad-140">**SetSessionDirectoryExposeServerIP**</span></span>](win32-tssessiondirectory-setsessiondirectoryexposeserverip.md) | <span data-ttu-id="b83ad-141">設定 **SessionDirectoryExposeServerIP** 屬性。</span><span class="sxs-lookup"><span data-stu-id="b83ad-141">Sets the **SessionDirectoryExposeServerIP** property.</span></span><br/>                                             |
| [<span data-ttu-id="b83ad-142">**SetSessionDirectoryProperty**</span><span class="sxs-lookup"><span data-stu-id="b83ad-142">**SetSessionDirectoryProperty**</span></span>](win32-tssessiondirectory-setsessiondirectoryproperty.md)             | <span data-ttu-id="b83ad-143">設定 **SessionDirectoryLocation** 屬性或 **SessionDirectoryClusterName** 屬性。</span><span class="sxs-lookup"><span data-stu-id="b83ad-143">Sets the **SessionDirectoryLocation** property or the **SessionDirectoryClusterName** property.</span></span><br/>   |
| [<span data-ttu-id="b83ad-144">**SetTSRedirectorMode**</span><span class="sxs-lookup"><span data-stu-id="b83ad-144">**SetTSRedirectorMode**</span></span>](settsredirectormode-win32-tssessiondirectory.md)                             | <span data-ttu-id="b83ad-145">這個方法無法使用。</span><span class="sxs-lookup"><span data-stu-id="b83ad-145">This method is not available.</span></span><br/>                                                                     |



 

### <a name="properties"></a><span data-ttu-id="b83ad-146">屬性</span><span class="sxs-lookup"><span data-stu-id="b83ad-146">Properties</span></span>

<span data-ttu-id="b83ad-147">**Win32 \_ TSSessionDirectory** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="b83ad-147">The **Win32\_TSSessionDirectory** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="b83ad-148">**標題**</span><span class="sxs-lookup"><span data-stu-id="b83ad-148">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b83ad-149">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="b83ad-149">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b83ad-150">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="b83ad-150">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b83ad-151">限定詞： [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64) </span><span class="sxs-lookup"><span data-stu-id="b83ad-151">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="b83ad-152">簡短描述 (物件的單行字串) 。</span><span class="sxs-lookup"><span data-stu-id="b83ad-152">Short description (one-line string) of the object.</span></span>

<span data-ttu-id="b83ad-153">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。</span><span class="sxs-lookup"><span data-stu-id="b83ad-153">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="b83ad-154">**說明**</span><span class="sxs-lookup"><span data-stu-id="b83ad-154">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b83ad-155">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="b83ad-155">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b83ad-156">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="b83ad-156">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b83ad-157">物件的描述。</span><span class="sxs-lookup"><span data-stu-id="b83ad-157">Description of the object.</span></span>

<span data-ttu-id="b83ad-158">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。</span><span class="sxs-lookup"><span data-stu-id="b83ad-158">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="b83ad-159">**GetLoadBalancingState**</span><span class="sxs-lookup"><span data-stu-id="b83ad-159">**GetLoadBalancingState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b83ad-160">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="b83ad-160">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="b83ad-161">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="b83ad-161">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b83ad-162">指出伺服器是否設定為參與 RD 連線代理人負載平衡。</span><span class="sxs-lookup"><span data-stu-id="b83ad-162">Indicates if the server is configured to participate in RD Connection Broker load balancing.</span></span>

<dt>

<span data-ttu-id="b83ad-163">0</span><span class="sxs-lookup"><span data-stu-id="b83ad-163">0</span></span>
</dt> <dd>

<span data-ttu-id="b83ad-164">伺服器未設定為參與 RD 連線代理人負載平衡。</span><span class="sxs-lookup"><span data-stu-id="b83ad-164">The server is not configured to participate in RD Connection Broker load balancing.</span></span>

</dd> <dt>

<span data-ttu-id="b83ad-165">1</span><span class="sxs-lookup"><span data-stu-id="b83ad-165">1</span></span>
</dt> <dd>

<span data-ttu-id="b83ad-166">伺服器設定為參與 RD 連線代理人負載平衡。</span><span class="sxs-lookup"><span data-stu-id="b83ad-166">The server is configured to participate in RD Connection Broker load balancing.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="b83ad-167">**GetServerWeight**</span><span class="sxs-lookup"><span data-stu-id="b83ad-167">**GetServerWeight**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b83ad-168">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="b83ad-168">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="b83ad-169">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="b83ad-169">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b83ad-170">抓取 RD 連線代理人負載平衡中使用的伺服器加權值。</span><span class="sxs-lookup"><span data-stu-id="b83ad-170">Retrieves the server weight value that is used in RD Connection Broker load balancing.</span></span>

</dd> <dt>

<span data-ttu-id="b83ad-171">**GetTSRedirectorMode**</span><span class="sxs-lookup"><span data-stu-id="b83ad-171">**GetTSRedirectorMode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b83ad-172">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="b83ad-172">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="b83ad-173">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="b83ad-173">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b83ad-174">指出伺服器是否已設定為做為遠端桌面服務的重新導向程式。</span><span class="sxs-lookup"><span data-stu-id="b83ad-174">Indicates if the server is configured to act as a Remote Desktop Services redirector.</span></span>

<dt>

<span data-ttu-id="b83ad-175">0</span><span class="sxs-lookup"><span data-stu-id="b83ad-175">0</span></span>
</dt> <dd>

<span data-ttu-id="b83ad-176">伺服器設定為作為遠端桌面服務的重新導向器。</span><span class="sxs-lookup"><span data-stu-id="b83ad-176">The server is configured to act as a Remote Desktop Services redirector.</span></span>

</dd> <dt>

<span data-ttu-id="b83ad-177">1</span><span class="sxs-lookup"><span data-stu-id="b83ad-177">1</span></span>
</dt> <dd>

<span data-ttu-id="b83ad-178">伺服器未設定為做為遠端桌面服務的重新導向器。</span><span class="sxs-lookup"><span data-stu-id="b83ad-178">The server is not configured to act as a Remote Desktop Services redirector.</span></span>

</dd> </dl>

<span data-ttu-id="b83ad-179">**Windows Server 2008：** 無法使用這個屬性。</span><span class="sxs-lookup"><span data-stu-id="b83ad-179">**Windows Server 2008:** This property is not available.</span></span>

</dd> <dt>

<span data-ttu-id="b83ad-180">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="b83ad-180">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b83ad-181">資料類型： **datetime**</span><span class="sxs-lookup"><span data-stu-id="b83ad-181">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="b83ad-182">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="b83ad-182">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b83ad-183">限定詞： [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "MIF。DMTF \| 元件 \| 001.5 ") </span><span class="sxs-lookup"><span data-stu-id="b83ad-183">Qualifiers: [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5")</span></span>
</dt> </dl>

<span data-ttu-id="b83ad-184">物件的安裝日期。</span><span class="sxs-lookup"><span data-stu-id="b83ad-184">The date the object was installed.</span></span> <span data-ttu-id="b83ad-185">缺少值並不表示物件未安裝。</span><span class="sxs-lookup"><span data-stu-id="b83ad-185">A lack of a value does not indicate that the object is not installed.</span></span>

<span data-ttu-id="b83ad-186">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。</span><span class="sxs-lookup"><span data-stu-id="b83ad-186">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="b83ad-187">**名稱**</span><span class="sxs-lookup"><span data-stu-id="b83ad-187">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b83ad-188">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="b83ad-188">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b83ad-189">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="b83ad-189">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b83ad-190">物件的名稱。</span><span class="sxs-lookup"><span data-stu-id="b83ad-190">The name of the object.</span></span>

<span data-ttu-id="b83ad-191">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。</span><span class="sxs-lookup"><span data-stu-id="b83ad-191">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="b83ad-192">**PolicySourceLoadBalancing**</span><span class="sxs-lookup"><span data-stu-id="b83ad-192">**PolicySourceLoadBalancing**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b83ad-193">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="b83ad-193">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="b83ad-194">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="b83ad-194">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b83ad-195">指出 **GetLoadBalancingState** 屬性是由伺服器或群組原則設定。</span><span class="sxs-lookup"><span data-stu-id="b83ad-195">Indicates if the **GetLoadBalancingState** property is configured by the server or by group policy.</span></span>

<dt>

<span data-ttu-id="b83ad-196">0 (0x0) </span><span class="sxs-lookup"><span data-stu-id="b83ad-196">0 (0x0)</span></span>
</dt> <dd>

<span data-ttu-id="b83ad-197">伺服器</span><span class="sxs-lookup"><span data-stu-id="b83ad-197">Server</span></span>

</dd> <dt>

<span data-ttu-id="b83ad-198">1 (0x1) </span><span class="sxs-lookup"><span data-stu-id="b83ad-198">1 (0x1)</span></span>
</dt> <dd>

<span data-ttu-id="b83ad-199">群組原則</span><span class="sxs-lookup"><span data-stu-id="b83ad-199">Group policy</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="b83ad-200">**PolicySourceSessionDirectoryActive**</span><span class="sxs-lookup"><span data-stu-id="b83ad-200">**PolicySourceSessionDirectoryActive**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b83ad-201">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="b83ad-201">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="b83ad-202">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="b83ad-202">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b83ad-203">指出 **SessionDirectoryActive** 屬性是由伺服器或群組原則設定。</span><span class="sxs-lookup"><span data-stu-id="b83ad-203">Indicates if the **SessionDirectoryActive** property is configured by the server or by group policy.</span></span>

<dt>

<span data-ttu-id="b83ad-204">0 (0x0) </span><span class="sxs-lookup"><span data-stu-id="b83ad-204">0 (0x0)</span></span>
</dt> <dd>

<span data-ttu-id="b83ad-205">伺服器</span><span class="sxs-lookup"><span data-stu-id="b83ad-205">Server</span></span>

</dd> <dt>

<span data-ttu-id="b83ad-206">1 (0x1) </span><span class="sxs-lookup"><span data-stu-id="b83ad-206">1 (0x1)</span></span>
</dt> <dd>

<span data-ttu-id="b83ad-207">群組原則</span><span class="sxs-lookup"><span data-stu-id="b83ad-207">Group policy</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="b83ad-208">**PolicySourceSessionDirectoryClusterName**</span><span class="sxs-lookup"><span data-stu-id="b83ad-208">**PolicySourceSessionDirectoryClusterName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b83ad-209">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="b83ad-209">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="b83ad-210">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="b83ad-210">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b83ad-211">指出 **SessionDirectoryClusterName** 屬性是由伺服器或群組原則設定。</span><span class="sxs-lookup"><span data-stu-id="b83ad-211">Indicates if the **SessionDirectoryClusterName** property is configured by the server or by group policy.</span></span>

<dt>

<span data-ttu-id="b83ad-212">0 (0x0) </span><span class="sxs-lookup"><span data-stu-id="b83ad-212">0 (0x0)</span></span>
</dt> <dd>

<span data-ttu-id="b83ad-213">伺服器</span><span class="sxs-lookup"><span data-stu-id="b83ad-213">Server</span></span>

</dd> <dt>

<span data-ttu-id="b83ad-214">1 (0x1) </span><span class="sxs-lookup"><span data-stu-id="b83ad-214">1 (0x1)</span></span>
</dt> <dd>

<span data-ttu-id="b83ad-215">群組原則</span><span class="sxs-lookup"><span data-stu-id="b83ad-215">Group policy</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="b83ad-216">**PolicySourceSessionDirectoryExposeServerIP**</span><span class="sxs-lookup"><span data-stu-id="b83ad-216">**PolicySourceSessionDirectoryExposeServerIP**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b83ad-217">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="b83ad-217">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="b83ad-218">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="b83ad-218">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b83ad-219">指出 **SessionDirectoryExposeServerIP** 屬性是由伺服器或群組原則設定。</span><span class="sxs-lookup"><span data-stu-id="b83ad-219">Indicates if the **SessionDirectoryExposeServerIP** property is configured by the server or by group policy.</span></span>

<dt>

<span data-ttu-id="b83ad-220">0 (0x0) </span><span class="sxs-lookup"><span data-stu-id="b83ad-220">0 (0x0)</span></span>
</dt> <dd>

<span data-ttu-id="b83ad-221">伺服器</span><span class="sxs-lookup"><span data-stu-id="b83ad-221">Server</span></span>

</dd> <dt>

<span data-ttu-id="b83ad-222">1 (0x1) </span><span class="sxs-lookup"><span data-stu-id="b83ad-222">1 (0x1)</span></span>
</dt> <dd>

<span data-ttu-id="b83ad-223">群組原則</span><span class="sxs-lookup"><span data-stu-id="b83ad-223">Group policy</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="b83ad-224">**PolicySourceSessionDirectoryLocation**</span><span class="sxs-lookup"><span data-stu-id="b83ad-224">**PolicySourceSessionDirectoryLocation**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b83ad-225">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="b83ad-225">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="b83ad-226">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="b83ad-226">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b83ad-227">指出 **SessionDirectoryLocation** 屬性是由伺服器或群組原則設定。</span><span class="sxs-lookup"><span data-stu-id="b83ad-227">Indicates if the **SessionDirectoryLocation** property is configured by the server or by group policy.</span></span>

<dt>

<span data-ttu-id="b83ad-228">0 (0x0) </span><span class="sxs-lookup"><span data-stu-id="b83ad-228">0 (0x0)</span></span>
</dt> <dd>

<span data-ttu-id="b83ad-229">伺服器</span><span class="sxs-lookup"><span data-stu-id="b83ad-229">Server</span></span>

</dd> <dt>

<span data-ttu-id="b83ad-230">1 (0x1) </span><span class="sxs-lookup"><span data-stu-id="b83ad-230">1 (0x1)</span></span>
</dt> <dd>

<span data-ttu-id="b83ad-231">群組原則</span><span class="sxs-lookup"><span data-stu-id="b83ad-231">Group policy</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="b83ad-232">**PolicySourceTSRedirectorMode**</span><span class="sxs-lookup"><span data-stu-id="b83ad-232">**PolicySourceTSRedirectorMode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b83ad-233">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="b83ad-233">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="b83ad-234">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="b83ad-234">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b83ad-235">無法使用這個屬性。</span><span class="sxs-lookup"><span data-stu-id="b83ad-235">This property is not available.</span></span>

<span data-ttu-id="b83ad-236">**Windows Server 2008 R2：** 指出 **GetTSRedirectorMode** 屬性是由伺服器或群組原則設定。</span><span class="sxs-lookup"><span data-stu-id="b83ad-236">**Windows Server 2008 R2:** Indicates if the **GetTSRedirectorMode** property is configured by the server or by group policy.</span></span>

<dt>

<span data-ttu-id="b83ad-237">0 (0x0) </span><span class="sxs-lookup"><span data-stu-id="b83ad-237">0 (0x0)</span></span>
</dt> <dd>

<span data-ttu-id="b83ad-238">伺服器</span><span class="sxs-lookup"><span data-stu-id="b83ad-238">Server</span></span>

</dd> <dt>

<span data-ttu-id="b83ad-239">1 (0x1) </span><span class="sxs-lookup"><span data-stu-id="b83ad-239">1 (0x1)</span></span>
</dt> <dd>

<span data-ttu-id="b83ad-240">群組原則</span><span class="sxs-lookup"><span data-stu-id="b83ad-240">Group policy</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="b83ad-241">**SessionDirectoryActive**</span><span class="sxs-lookup"><span data-stu-id="b83ad-241">**SessionDirectoryActive**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b83ad-242">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="b83ad-242">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="b83ad-243">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="b83ad-243">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b83ad-244">限定詞：索引 [**鍵**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="b83ad-244">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="b83ad-245">指定遠端桌面服務是否參與 RD 連線代理人。</span><span class="sxs-lookup"><span data-stu-id="b83ad-245">Specifies if Remote Desktop Services participates in the RD Connection Broker.</span></span>

<dt>

<span id="FALSE"></span><span id="false"></span>

<span data-ttu-id="b83ad-246"><span id="FALSE"></span><span id="false"></span>**FALSE** (0) </span><span class="sxs-lookup"><span data-stu-id="b83ad-246"><span id="FALSE"></span><span id="false"></span>**FALSE** (0)</span></span>


</dt> <dd>

<span data-ttu-id="b83ad-247">RD 連線代理人中的遠端桌面服務參與已停用。</span><span class="sxs-lookup"><span data-stu-id="b83ad-247">Remote Desktop Services participation in the RD Connection Broker is disabled.</span></span>

</dd> <dt>

<span id="TRUE"></span><span id="true"></span>

<span data-ttu-id="b83ad-248"><span id="TRUE"></span><span id="true"></span>**TRUE** (1) </span><span class="sxs-lookup"><span data-stu-id="b83ad-248"><span id="TRUE"></span><span id="true"></span>**TRUE** (1)</span></span>


</dt> <dd>

<span data-ttu-id="b83ad-249">已啟用遠端桌面服務參與 RD 連線代理人。</span><span class="sxs-lookup"><span data-stu-id="b83ad-249">Remote Desktop Services participation in the RD Connection Broker is enabled.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="b83ad-250">**SessionDirectoryClusterName**</span><span class="sxs-lookup"><span data-stu-id="b83ad-250">**SessionDirectoryClusterName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b83ad-251">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="b83ad-251">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b83ad-252">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="b83ad-252">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b83ad-253">RD 工作階段主機伺服器所屬叢集的虛擬 IP 位址。</span><span class="sxs-lookup"><span data-stu-id="b83ad-253">The virtual IP address of the cluster to which the RD Session Host server belongs.</span></span>

</dd> <dt>

<span data-ttu-id="b83ad-254">**SessionDirectoryExposeServerIP**</span><span class="sxs-lookup"><span data-stu-id="b83ad-254">**SessionDirectoryExposeServerIP**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b83ad-255">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="b83ad-255">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="b83ad-256">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="b83ad-256">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b83ad-257">指定是否允許抓取 RD 連線代理人的 IP 位址。</span><span class="sxs-lookup"><span data-stu-id="b83ad-257">Specifies if retrieval of the IP address of the RD Connection Broker is allowed.</span></span>

<dt>

<span id="FALSE"></span><span id="false"></span>

<span data-ttu-id="b83ad-258"><span id="FALSE"></span><span id="false"></span>**FALSE** (0) </span><span class="sxs-lookup"><span data-stu-id="b83ad-258"><span id="FALSE"></span><span id="false"></span>**FALSE** (0)</span></span>


</dt> <dd>

<span data-ttu-id="b83ad-259">已拒絕抓取。</span><span class="sxs-lookup"><span data-stu-id="b83ad-259">Retrieval is denied.</span></span>

</dd> <dt>

<span id="TRUE"></span><span id="true"></span>

<span data-ttu-id="b83ad-260"><span id="TRUE"></span><span id="true"></span>**TRUE** (1) </span><span class="sxs-lookup"><span data-stu-id="b83ad-260"><span id="TRUE"></span><span id="true"></span>**TRUE** (1)</span></span>


</dt> <dd>

<span data-ttu-id="b83ad-261">允許抓取。</span><span class="sxs-lookup"><span data-stu-id="b83ad-261">Retrieval is allowed.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="b83ad-262">**SessionDirectoryIPAddress**</span><span class="sxs-lookup"><span data-stu-id="b83ad-262">**SessionDirectoryIPAddress**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b83ad-263">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="b83ad-263">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b83ad-264">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="b83ad-264">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="b83ad-265">會話目錄所使用之 LAN 介面卡的 IP 位址。</span><span class="sxs-lookup"><span data-stu-id="b83ad-265">The IP address of the LAN adapter used by the session directory.</span></span>

</dd> <dt>

<span data-ttu-id="b83ad-266">**SessionDirectoryLocation**</span><span class="sxs-lookup"><span data-stu-id="b83ad-266">**SessionDirectoryLocation**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b83ad-267">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="b83ad-267">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b83ad-268">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="b83ad-268">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b83ad-269">RD 連線代理人服務執行所在之伺服器的網路 DNS 名稱或 IP 位址。</span><span class="sxs-lookup"><span data-stu-id="b83ad-269">The network DNS name or IP address of the server where the RD Connection Broker service is running.</span></span>

</dd> <dt>

<span data-ttu-id="b83ad-270">**狀態**</span><span class="sxs-lookup"><span data-stu-id="b83ad-270">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b83ad-271">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="b83ad-271">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b83ad-272">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="b83ad-272">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b83ad-273">限定詞： [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10) </span><span class="sxs-lookup"><span data-stu-id="b83ad-273">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10)</span></span>
</dt> </dl>

<span data-ttu-id="b83ad-274">物件的目前狀態。</span><span class="sxs-lookup"><span data-stu-id="b83ad-274">Current status of the object.</span></span> <span data-ttu-id="b83ad-275">您可以定義各種操作和 nonoperational 狀態。</span><span class="sxs-lookup"><span data-stu-id="b83ad-275">Various operational and nonoperational statuses can be defined.</span></span> <span data-ttu-id="b83ad-276">作業狀態包括：「正常」、「降級」和「Pred 失敗」 (元素（例如啟用智慧的硬碟）可能會正常運作，但在不久的未來) 中預測失敗。</span><span class="sxs-lookup"><span data-stu-id="b83ad-276">Operational statuses include: "OK", "Degraded", and "Pred Fail" (an element, such as a SMART-enabled hard disk drive, may be functioning properly but predicting a failure in the near future).</span></span> <span data-ttu-id="b83ad-277">Nonoperational 狀態包括：「錯誤」、「開始」、「正在停止」和「服務」。</span><span class="sxs-lookup"><span data-stu-id="b83ad-277">Nonoperational statuses include: "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="b83ad-278">後者（「服務」）可以在磁片的鏡像重新同步處理期間套用，重載使用者權限清單或其他系統管理工作。</span><span class="sxs-lookup"><span data-stu-id="b83ad-278">The latter, "Service", could apply during mirror-resilvering of a disk, reload of a user permissions list, or other administrative work.</span></span> <span data-ttu-id="b83ad-279">並非所有這類工作都是線上的，但受管理的元素並不是「確定」，也不是其中一個其他狀態。</span><span class="sxs-lookup"><span data-stu-id="b83ad-279">Not all such work is on-line, yet the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="b83ad-280">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。</span><span class="sxs-lookup"><span data-stu-id="b83ad-280">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<dt>



 <span data-ttu-id="b83ad-281"> ( [確定] ) </span><span class="sxs-lookup"><span data-stu-id="b83ad-281">("OK")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="b83ad-282"> ( 「錯誤」 ) </span><span class="sxs-lookup"><span data-stu-id="b83ad-282">("Error")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="b83ad-283"> ( 「降級」 ) </span><span class="sxs-lookup"><span data-stu-id="b83ad-283">("Degraded")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="b83ad-284"> ( 「未知」 ) </span><span class="sxs-lookup"><span data-stu-id="b83ad-284">("Unknown")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="b83ad-285"> ( 「Pred 失敗」 ) </span><span class="sxs-lookup"><span data-stu-id="b83ad-285">("Pred Fail")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="b83ad-286"> ( 「開始」 ) </span><span class="sxs-lookup"><span data-stu-id="b83ad-286">("Starting")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="b83ad-287"> ( 「正在停止」 ) </span><span class="sxs-lookup"><span data-stu-id="b83ad-287">("Stopping")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="b83ad-288"> ( "Service" ) </span><span class="sxs-lookup"><span data-stu-id="b83ad-288">("Service")</span></span>


<span data-ttu-id="b83ad-289"></dt> <dd></dd> </dl>

</dd> </dl></span><span class="sxs-lookup"><span data-stu-id="b83ad-289"></dt> <dd></dd> </dl>

</dd> </dl></span></span>

## <a name="remarks"></a><span data-ttu-id="b83ad-290">備註</span><span class="sxs-lookup"><span data-stu-id="b83ad-290">Remarks</span></span>

<span data-ttu-id="b83ad-291">若要連接到 \\ \\ 根 \\ CIMV2 \\ microsoft-windows-terminalservices-gateway 命名空間，驗證層級必須包含封包隱私權。</span><span class="sxs-lookup"><span data-stu-id="b83ad-291">To connect to the \\\\root\\CIMV2\\TerminalServices namespace, the authentication level must include packet privacy.</span></span> <span data-ttu-id="b83ad-292">針對 C/c + + 呼叫，這是 **RPC \_ C \_ 驗證 \_ level \_ PKT \_ 隱私權** 的驗證層級。</span><span class="sxs-lookup"><span data-stu-id="b83ad-292">For C/C++ calls, this is an authentication level of **RPC\_C\_AUTHN\_LEVEL\_PKT\_PRIVACY**.</span></span> <span data-ttu-id="b83ad-293">針對 Visual Basic 和腳本呼叫，這是 **WbemAuthenticationLevelPktPrivacy** 或 "pktPrivacy" 的驗證層級，其值為六。</span><span class="sxs-lookup"><span data-stu-id="b83ad-293">For Visual Basic and scripting calls, this is an authentication level of **WbemAuthenticationLevelPktPrivacy** or "pktPrivacy", with a value of six.</span></span>

<span data-ttu-id="b83ad-294">下列 Visual Basic Scripting Edition (VBScript) 範例示範如何連接到具有封包隱私權的遠端電腦。</span><span class="sxs-lookup"><span data-stu-id="b83ad-294">The following Visual Basic Scripting Edition (VBScript) example shows how to connect to a remote computer with packet privacy.</span></span>


```VB
strComputer = "RemoteServer1" 
Set objServices = GetObject( _
    "winmgmts:{authenticationLevel=pktPrivacy}!Root/CIMv2/TerminalServices")
```



<span data-ttu-id="b83ad-295">在 Windows Server 2008 中，終端機服務會話目錄功能的名稱已變更為終端機服務會話代理程式。</span><span class="sxs-lookup"><span data-stu-id="b83ad-295">In Windows Server 2008, the name of the Terminal Services Session Directory feature was changed to Terminal Services Session Broker.</span></span>

<span data-ttu-id="b83ad-296">在 Windows Server 2008 R2 中，終端機服務會話代理人功能的名稱已變更為遠端桌面連線代理人。</span><span class="sxs-lookup"><span data-stu-id="b83ad-296">In Windows Server 2008 R2, the name of the Terminal Services Session Broker feature was changed to Remote Desktop Connection Broker.</span></span>

<span data-ttu-id="b83ad-297">受控物件格式 (MOF) 檔包含 Windows Management Instrumentation (WMI) 類別的定義。</span><span class="sxs-lookup"><span data-stu-id="b83ad-297">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="b83ad-298">MOF 檔案不會安裝為 Microsoft Windows 軟體開發套件 (SDK) 的一部分。</span><span class="sxs-lookup"><span data-stu-id="b83ad-298">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="b83ad-299">當您使用伺服器管理員新增相關聯的角色時，它們會安裝在伺服器上。</span><span class="sxs-lookup"><span data-stu-id="b83ad-299">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="b83ad-300">如需 MOF 檔案的詳細資訊，請參閱 [受控物件格式 (mof) ](/windows/desktop/WmiSdk/managed-object-format--mof-)。</span><span class="sxs-lookup"><span data-stu-id="b83ad-300">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="b83ad-301">規格需求</span><span class="sxs-lookup"><span data-stu-id="b83ad-301">Requirements</span></span>



| <span data-ttu-id="b83ad-302">需求</span><span class="sxs-lookup"><span data-stu-id="b83ad-302">Requirement</span></span> | <span data-ttu-id="b83ad-303">值</span><span class="sxs-lookup"><span data-stu-id="b83ad-303">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="b83ad-304">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="b83ad-304">Minimum supported client</span></span><br/> | <span data-ttu-id="b83ad-305">都不支援</span><span class="sxs-lookup"><span data-stu-id="b83ad-305">None supported</span></span><br/>                                                               |
| <span data-ttu-id="b83ad-306">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="b83ad-306">Minimum supported server</span></span><br/> | <span data-ttu-id="b83ad-307">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="b83ad-307">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="b83ad-308">命名空間</span><span class="sxs-lookup"><span data-stu-id="b83ad-308">Namespace</span></span><br/>                | <span data-ttu-id="b83ad-309">根 \\ CIMv2 \\ microsoft-windows-terminalservices-gateway</span><span class="sxs-lookup"><span data-stu-id="b83ad-309">Root\\CIMv2\\TerminalServices</span></span><br/>                                                |
| <span data-ttu-id="b83ad-310">MOF</span><span class="sxs-lookup"><span data-stu-id="b83ad-310">MOF</span></span><br/>                      | <dl> <span data-ttu-id="b83ad-311"><dt>TSCfgWmi mof</dt></span><span class="sxs-lookup"><span data-stu-id="b83ad-311"><dt>TSCfgWmi.mof</dt></span></span> </dl> |
| <span data-ttu-id="b83ad-312">DLL</span><span class="sxs-lookup"><span data-stu-id="b83ad-312">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b83ad-313"><dt>TSCfgWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b83ad-313"><dt>TSCfgWmi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b83ad-314">另請參閱</span><span class="sxs-lookup"><span data-stu-id="b83ad-314">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b83ad-315">**CIM \_ 設定**</span><span class="sxs-lookup"><span data-stu-id="b83ad-315">**CIM\_Setting**</span></span>](cim-setting.md)
</dt> <dt>

[<span data-ttu-id="b83ad-316">**Win32 \_ TSSessionDirectorySetting**</span><span class="sxs-lookup"><span data-stu-id="b83ad-316">**Win32\_TSSessionDirectorySetting**</span></span>](win32-tssessiondirectorysetting.md)
</dt> </dl>

 

