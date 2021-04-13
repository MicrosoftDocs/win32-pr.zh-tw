---
title: Win32_TSDiscoveredLicenseServer 類別
description: 提供探索到的遠端桌面授權伺服器的詳細資料。
ms.assetid: 88523f30-26ad-4f78-a214-f54b7bc1c676
ms.tgt_platform: multiple
keywords:
- Win32_TSDiscoveredLicenseServer 類別遠端桌面服務
- Win32_TSDiscoveredLicenseServer 類別遠端桌面服務，描述
topic_type:
- apiref
api_name:
- Win32_TSDiscoveredLicenseServer
- Win32_TSDiscoveredLicenseServer.LicenseServer
- Win32_TSDiscoveredLicenseServer.HowDiscovered
- Win32_TSDiscoveredLicenseServer.IsLSAvailable
- Win32_TSDiscoveredLicenseServer.IsAdminOnLS
- Win32_TSDiscoveredLicenseServer.IssuingCALs
api_location:
- TSCfgWmi.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d633031df533068f2cf5da65f2f6820a93c78513
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104466713"
---
# <a name="win32_tsdiscoveredlicenseserver-class"></a><span data-ttu-id="42561-105">Win32 \_ TSDiscoveredLicenseServer 類別</span><span class="sxs-lookup"><span data-stu-id="42561-105">Win32\_TSDiscoveredLicenseServer class</span></span>

<span data-ttu-id="42561-106">提供探索到的遠端桌面授權伺服器的詳細資料。</span><span class="sxs-lookup"><span data-stu-id="42561-106">Provides details about the discovered Remote Desktop license server.</span></span>

## <a name="syntax"></a><span data-ttu-id="42561-107">語法</span><span class="sxs-lookup"><span data-stu-id="42561-107">Syntax</span></span>

``` syntax
[abstract, AMENDMENT]
class Win32_TSDiscoveredLicenseServer
{
  string LicenseServer;
  uint32 HowDiscovered;
  uint32 IsLSAvailable;
  uint32 IsAdminOnLS;
  uint32 IssuingCALs;
};
```

## <a name="members"></a><span data-ttu-id="42561-108">成員</span><span class="sxs-lookup"><span data-stu-id="42561-108">Members</span></span>

<span data-ttu-id="42561-109">**Win32 \_ TSDiscoveredLicenseServer** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="42561-109">The **Win32\_TSDiscoveredLicenseServer** class has these types of members:</span></span>

-   [<span data-ttu-id="42561-110">屬性</span><span class="sxs-lookup"><span data-stu-id="42561-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="42561-111">屬性</span><span class="sxs-lookup"><span data-stu-id="42561-111">Properties</span></span>

<span data-ttu-id="42561-112">**Win32 \_ TSDiscoveredLicenseServer** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="42561-112">The **Win32\_TSDiscoveredLicenseServer** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="42561-113">**HowDiscovered**</span><span class="sxs-lookup"><span data-stu-id="42561-113">**HowDiscovered**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="42561-114">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="42561-114">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="42561-115">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="42561-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="42561-116">限定詞：已 [**淘汰**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="42561-116">Qualifiers: [**DEPRECATED**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="42561-117">這個屬性不再受到支援。</span><span class="sxs-lookup"><span data-stu-id="42561-117">This property is no longer supported.</span></span>

<span data-ttu-id="42561-118">**Windows Server 2008：** 遠端桌面授權伺服器探索方法。</span><span class="sxs-lookup"><span data-stu-id="42561-118">**Windows Server 2008:** The Remote Desktop license server discovery method.</span></span>

<dt>

<span id="GroupPolicyConfigured"></span><span id="grouppolicyconfigured"></span><span id="GROUPPOLICYCONFIGURED"></span>

<span data-ttu-id="42561-119"><span id="GroupPolicyConfigured"></span><span id="grouppolicyconfigured"></span><span id="GROUPPOLICYCONFIGURED"></span>**GroupPolicyConfigured** (0) </span><span class="sxs-lookup"><span data-stu-id="42561-119"><span id="GroupPolicyConfigured"></span><span id="grouppolicyconfigured"></span><span id="GROUPPOLICYCONFIGURED"></span>**GroupPolicyConfigured** (0)</span></span>


</dt> <dd>

<span data-ttu-id="42561-120">使用群組原則探索到授權伺服器。</span><span class="sxs-lookup"><span data-stu-id="42561-120">The license server was discovered by using group policy.</span></span>

</dd> <dt>

<span id="RegistryConfigured"></span><span id="registryconfigured"></span><span id="REGISTRYCONFIGURED"></span>

<span data-ttu-id="42561-121"><span id="RegistryConfigured"></span><span id="registryconfigured"></span><span id="REGISTRYCONFIGURED"></span>**RegistryConfigured** (1) </span><span class="sxs-lookup"><span data-stu-id="42561-121"><span id="RegistryConfigured"></span><span id="registryconfigured"></span><span id="REGISTRYCONFIGURED"></span>**RegistryConfigured** (1)</span></span>


</dt> <dd>

<span data-ttu-id="42561-122">使用登錄設定探索到授權伺服器。</span><span class="sxs-lookup"><span data-stu-id="42561-122">The license server was discovered by using a registry setting.</span></span>

</dd> <dt>

<span id="WorkgroupDiscovery"></span><span id="workgroupdiscovery"></span><span id="WORKGROUPDISCOVERY"></span>

<span data-ttu-id="42561-123"><span id="WorkgroupDiscovery"></span><span id="workgroupdiscovery"></span><span id="WORKGROUPDISCOVERY"></span>**WorkgroupDiscovery** (2) </span><span class="sxs-lookup"><span data-stu-id="42561-123"><span id="WorkgroupDiscovery"></span><span id="workgroupdiscovery"></span><span id="WORKGROUPDISCOVERY"></span>**WorkgroupDiscovery** (2)</span></span>


</dt> <dd>

<span data-ttu-id="42561-124">使用工作組探索領域探索到授權伺服器。</span><span class="sxs-lookup"><span data-stu-id="42561-124">The license server was discovered by using the workgroup discovery scope.</span></span>

</dd> <dt>

<span id="DomainDiscovery"></span><span id="domaindiscovery"></span><span id="DOMAINDISCOVERY"></span>

<span data-ttu-id="42561-125"><span id="DomainDiscovery"></span><span id="domaindiscovery"></span><span id="DOMAINDISCOVERY"></span>**DomainDiscovery** (3) </span><span class="sxs-lookup"><span data-stu-id="42561-125"><span id="DomainDiscovery"></span><span id="domaindiscovery"></span><span id="DOMAINDISCOVERY"></span>**DomainDiscovery** (3)</span></span>


</dt> <dd>

<span data-ttu-id="42561-126">使用網域探索領域探索到授權伺服器。</span><span class="sxs-lookup"><span data-stu-id="42561-126">The license server was discovered by using the domain discovery scope.</span></span>

</dd> <dt>

<span id="EnterpriseDiscovery"></span><span id="enterprisediscovery"></span><span id="ENTERPRISEDISCOVERY"></span>

<span data-ttu-id="42561-127"><span id="EnterpriseDiscovery"></span><span id="enterprisediscovery"></span><span id="ENTERPRISEDISCOVERY"></span>**EnterpriseDiscovery** (4) </span><span class="sxs-lookup"><span data-stu-id="42561-127"><span id="EnterpriseDiscovery"></span><span id="enterprisediscovery"></span><span id="ENTERPRISEDISCOVERY"></span>**EnterpriseDiscovery** (4)</span></span>


</dt> <dd>

<span data-ttu-id="42561-128">使用樹系探索領域探索到授權伺服器。</span><span class="sxs-lookup"><span data-stu-id="42561-128">The license server was discovered by using the forest discovery scope.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="42561-129">**IsAdminOnLS**</span><span class="sxs-lookup"><span data-stu-id="42561-129">**IsAdminOnLS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="42561-130">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="42561-130">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="42561-131">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="42561-131">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="42561-132">指出用來執行腳本的帳戶或使用 **Win32 \_ TSDiscoveredLicenseServer** 類別的 .exe 檔案，是否具有授權伺服器的系統管理員存取權。</span><span class="sxs-lookup"><span data-stu-id="42561-132">Indicates whether the account that is being used to run the script or .exe file that is using the **Win32\_TSDiscoveredLicenseServer** class has administrator access to the license server.</span></span>

<dt>

<span id="No"></span><span id="no"></span><span id="NO"></span>

<span data-ttu-id="42561-133"><span id="No"></span><span id="no"></span><span id="NO"></span>**無** (0) </span><span class="sxs-lookup"><span data-stu-id="42561-133"><span id="No"></span><span id="no"></span><span id="NO"></span>**No** (0)</span></span>


</dt> <dd>

<span data-ttu-id="42561-134">使用的帳戶沒有授權伺服器的系統管理員存取權。</span><span class="sxs-lookup"><span data-stu-id="42561-134">The account that is being used does not have administrator access to the license server.</span></span>

</dd> <dt>

<span id="Yes"></span><span id="yes"></span><span id="YES"></span>

<span data-ttu-id="42561-135"><span id="Yes"></span><span id="yes"></span><span id="YES"></span>**是** (1) </span><span class="sxs-lookup"><span data-stu-id="42561-135"><span id="Yes"></span><span id="yes"></span><span id="YES"></span>**Yes** (1)</span></span>


</dt> <dd>

<span data-ttu-id="42561-136">使用的帳戶具有授權伺服器的系統管理員存取權。</span><span class="sxs-lookup"><span data-stu-id="42561-136">The account that is being used has administrator access to the license server.</span></span>

</dd> <dt>

<span id="Dont_know"></span><span id="dont_know"></span><span id="DONT_KNOW"></span>

<span data-ttu-id="42561-137"><span id="Dont_know"></span><span id="dont_know"></span><span id="DONT_KNOW"></span>不 **知道** (2) </span><span class="sxs-lookup"><span data-stu-id="42561-137"><span id="Dont_know"></span><span id="dont_know"></span><span id="DONT_KNOW"></span>**Dont know** (2)</span></span>


</dt> <dd>

<span data-ttu-id="42561-138">無法判斷所使用的帳戶是否具有授權伺服器的系統管理員存取權。</span><span class="sxs-lookup"><span data-stu-id="42561-138">It cannot be determined whether the account that is being used has administrator access to the license server.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="42561-139">**IsLSAvailable**</span><span class="sxs-lookup"><span data-stu-id="42561-139">**IsLSAvailable**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="42561-140">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="42561-140">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="42561-141">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="42561-141">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="42561-142">指出授權伺服器是否可用 (是否 \[ 可以對伺服器) 進行遠端程序呼叫 RPC \] 連接。</span><span class="sxs-lookup"><span data-stu-id="42561-142">Indicates whether the license server is available (whether a remote procedure call \[RPC\] connection can be made to the server).</span></span>

<dt>

<span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>

<span data-ttu-id="42561-143"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span> (0) **無法使用**</span><span class="sxs-lookup"><span data-stu-id="42561-143"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Not Available** (0)</span></span>


</dt> <dd>

<span data-ttu-id="42561-144">授權伺服器無法使用。</span><span class="sxs-lookup"><span data-stu-id="42561-144">The license server is not available.</span></span>

</dd> <dt>

<span id="Available"></span><span id="available"></span><span id="AVAILABLE"></span>

<span data-ttu-id="42561-145"><span id="Available"></span><span id="available"></span><span id="AVAILABLE"></span>**可用** (1) </span><span class="sxs-lookup"><span data-stu-id="42561-145"><span id="Available"></span><span id="available"></span><span id="AVAILABLE"></span>**Available** (1)</span></span>


</dt> <dd>

<span data-ttu-id="42561-146">授權伺服器可供使用。</span><span class="sxs-lookup"><span data-stu-id="42561-146">The license server is available.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="42561-147">**IssuingCALs**</span><span class="sxs-lookup"><span data-stu-id="42561-147">**IssuingCALs**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="42561-148">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="42561-148">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="42561-149">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="42561-149">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="42561-150">指出是否允許授權伺服器發出遠端桌面服務用戶端存取授權 (RDS Cal) 到 RD 工作階段主機伺服器。</span><span class="sxs-lookup"><span data-stu-id="42561-150">Indicates whether the license server is allowed to issue Remote Desktop Services client access licenses (RDS CALs) to the RD Session Host server.</span></span>

<dt>

<span id="Not_Allowed"></span><span id="not_allowed"></span><span id="NOT_ALLOWED"></span>

<span data-ttu-id="42561-151"><span id="Not_Allowed"></span><span id="not_allowed"></span><span id="NOT_ALLOWED"></span>**不允許** (0) </span><span class="sxs-lookup"><span data-stu-id="42561-151"><span id="Not_Allowed"></span><span id="not_allowed"></span><span id="NOT_ALLOWED"></span>**Not Allowed** (0)</span></span>


</dt> <dd>

<span data-ttu-id="42561-152">授權伺服器不能對 RD 工作階段主機伺服器發出 RDS Cal。</span><span class="sxs-lookup"><span data-stu-id="42561-152">The license server is not allowed to issue RDS CALs to the RD Session Host server.</span></span>

</dd> <dt>

<span id="Allowed"></span><span id="allowed"></span><span id="ALLOWED"></span>

<span data-ttu-id="42561-153"><span id="Allowed"></span><span id="allowed"></span><span id="ALLOWED"></span>**允許** 的 (1) </span><span class="sxs-lookup"><span data-stu-id="42561-153"><span id="Allowed"></span><span id="allowed"></span><span id="ALLOWED"></span>**Allowed** (1)</span></span>


</dt> <dd>

<span data-ttu-id="42561-154">授權伺服器可對 RD 工作階段主機伺服器發出 RDS Cal。</span><span class="sxs-lookup"><span data-stu-id="42561-154">The license server is allowed to issue RDS CALs to the RD Session Host server.</span></span>

</dd> <dt>

<span id="Dont_know"></span><span id="dont_know"></span><span id="DONT_KNOW"></span>

<span data-ttu-id="42561-155"><span id="Dont_know"></span><span id="dont_know"></span><span id="DONT_KNOW"></span>不 **知道** (2) </span><span class="sxs-lookup"><span data-stu-id="42561-155"><span id="Dont_know"></span><span id="dont_know"></span><span id="DONT_KNOW"></span>**Dont know** (2)</span></span>


</dt> <dd>

<span data-ttu-id="42561-156">無法判斷授權伺服器是否允許對 RD 工作階段主機伺服器發出 RDS Cal。</span><span class="sxs-lookup"><span data-stu-id="42561-156">It cannot be determined whether the license server is allowed to issue RDS CALs to the RD Session Host server.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="42561-157">**LicenseServer**</span><span class="sxs-lookup"><span data-stu-id="42561-157">**LicenseServer**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="42561-158">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="42561-158">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="42561-159">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="42561-159">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="42561-160">限定詞：索引 [**鍵**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="42561-160">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="42561-161">探索到的遠端桌面授權伺服器名稱。</span><span class="sxs-lookup"><span data-stu-id="42561-161">Name of the discovered Remote Desktop license server.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="42561-162">備註</span><span class="sxs-lookup"><span data-stu-id="42561-162">Remarks</span></span>

<span data-ttu-id="42561-163">若要連接到 \\ 根 \\ CIMV2 \\ microsoft-windows-terminalservices-gateway 命名空間，驗證層級必須包含封包隱私權。</span><span class="sxs-lookup"><span data-stu-id="42561-163">To connect to the \\root\\CIMV2\\TerminalServices namespace, the authentication level must include packet privacy.</span></span> <span data-ttu-id="42561-164">針對 C/c + + 呼叫，這是 **RPC \_ C \_ 驗證 \_ level \_ PKT \_ 隱私權** 的驗證層級。</span><span class="sxs-lookup"><span data-stu-id="42561-164">For C/C++ calls, this is an authentication level of **RPC\_C\_AUTHN\_LEVEL\_PKT\_PRIVACY**.</span></span> <span data-ttu-id="42561-165">針對 Visual Basic 和腳本呼叫，這是 **WbemAuthenticationLevelPktPrivacy** 或 "pktPrivacy" 的驗證層級，其值為6。</span><span class="sxs-lookup"><span data-stu-id="42561-165">For Visual Basic and scripting calls, this is an authentication level of **WbemAuthenticationLevelPktPrivacy** or "pktPrivacy", with a value of 6.</span></span> <span data-ttu-id="42561-166">下列 Visual Basic Scripting Edition (VBScript) 範例示範如何連接到具有封包隱私權的遠端電腦。</span><span class="sxs-lookup"><span data-stu-id="42561-166">The following Visual Basic Scripting Edition (VBScript) example shows how to connect to a remote computer with packet privacy.</span></span>


```VB
strComputer = "RemoteServer1" 
Set objServices = GetObject( _
    "winmgmts:{authenticationLevel=pktPrivacy}!Root/CIMv2/TerminalServices")
```



<span data-ttu-id="42561-167">受控物件格式 (MOF) 檔包含 Windows Management Instrumentation (WMI) 類別的定義。</span><span class="sxs-lookup"><span data-stu-id="42561-167">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="42561-168">MOF 檔案不會安裝為 Microsoft Windows 軟體開發套件 (SDK) 的一部分。</span><span class="sxs-lookup"><span data-stu-id="42561-168">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="42561-169">當您使用伺服器管理員新增相關聯的角色時，它們會安裝在伺服器上。</span><span class="sxs-lookup"><span data-stu-id="42561-169">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="42561-170">如需 MOF 檔案的詳細資訊，請參閱 [受控物件格式 (mof) ](/windows/desktop/WmiSdk/managed-object-format--mof-)。</span><span class="sxs-lookup"><span data-stu-id="42561-170">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="42561-171">規格需求</span><span class="sxs-lookup"><span data-stu-id="42561-171">Requirements</span></span>



| <span data-ttu-id="42561-172">需求</span><span class="sxs-lookup"><span data-stu-id="42561-172">Requirement</span></span> | <span data-ttu-id="42561-173">值</span><span class="sxs-lookup"><span data-stu-id="42561-173">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="42561-174">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="42561-174">Minimum supported client</span></span><br/> | <span data-ttu-id="42561-175">都不支援</span><span class="sxs-lookup"><span data-stu-id="42561-175">None supported</span></span><br/>                                                               |
| <span data-ttu-id="42561-176">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="42561-176">Minimum supported server</span></span><br/> | <span data-ttu-id="42561-177">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="42561-177">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="42561-178">命名空間</span><span class="sxs-lookup"><span data-stu-id="42561-178">Namespace</span></span><br/>                | <span data-ttu-id="42561-179">根 \\ CIMv2 \\ microsoft-windows-terminalservices-gateway</span><span class="sxs-lookup"><span data-stu-id="42561-179">Root\\CIMv2\\TerminalServices</span></span><br/>                                                |
| <span data-ttu-id="42561-180">MOF</span><span class="sxs-lookup"><span data-stu-id="42561-180">MOF</span></span><br/>                      | <dl> <span data-ttu-id="42561-181"><dt>TSCfgWmi mof</dt></span><span class="sxs-lookup"><span data-stu-id="42561-181"><dt>TSCfgWmi.mof</dt></span></span> </dl> |
| <span data-ttu-id="42561-182">DLL</span><span class="sxs-lookup"><span data-stu-id="42561-182">DLL</span></span><br/>                      | <dl> <span data-ttu-id="42561-183"><dt>TSCfgWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="42561-183"><dt>TSCfgWmi.dll</dt></span></span> </dl> |



 

