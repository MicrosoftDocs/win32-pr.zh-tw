---
title: Win32_TerminalServiceSetting 類別的 FindLicenseServers 方法
description: 列舉所有的遠端桌面授權伺服器，以及探索的方法。
ms.assetid: 0de2ee6f-6c56-4293-84da-131b433c6a9d
ms.tgt_platform: multiple
keywords:
- FindLicenseServers 方法遠端桌面服務
- FindLicenseServers 方法遠端桌面服務，Win32_TerminalServiceSetting 類別
- Win32_TerminalServiceSetting 類別遠端桌面服務，FindLicenseServers 方法
topic_type:
- apiref
api_name:
- Win32_TerminalServiceSetting.FindLicenseServers
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b83376876009a691fed233cf723f04dcc3bc3c8e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103934973"
---
# <a name="findlicenseservers-method-of-the-win32_terminalservicesetting-class"></a><span data-ttu-id="4c3a9-106">Win32 TerminalServiceSetting 類別的 FindLicenseServers 方法 \_</span><span class="sxs-lookup"><span data-stu-id="4c3a9-106">FindLicenseServers method of the Win32\_TerminalServiceSetting class</span></span>

<span data-ttu-id="4c3a9-107">列舉所有的遠端桌面授權伺服器，以及探索的方法。</span><span class="sxs-lookup"><span data-stu-id="4c3a9-107">Enumerates all of the Remote Desktop license servers, and the method of discovery.</span></span>

## <a name="syntax"></a><span data-ttu-id="4c3a9-108">語法</span><span class="sxs-lookup"><span data-stu-id="4c3a9-108">Syntax</span></span>


```mof
uint32 FindLicenseServers(
  [out] Win32_TSDiscoveredLicenseServer LicenseServersList[],
  [out] uint32                          Count
);
```



## <a name="parameters"></a><span data-ttu-id="4c3a9-109">參數</span><span class="sxs-lookup"><span data-stu-id="4c3a9-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4c3a9-110">*LicenseServersList* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="4c3a9-110">*LicenseServersList* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="4c3a9-111">[**Win32 \_ TSDiscoveredLicenseServer**](win32-tsdiscoveredlicenseserver.md)物件的清單。</span><span class="sxs-lookup"><span data-stu-id="4c3a9-111">The list of [**Win32\_TSDiscoveredLicenseServer**](win32-tsdiscoveredlicenseserver.md) objects.</span></span> <span data-ttu-id="4c3a9-112">輸出清單中的每個物件都具有遠端桌面授權伺服器的名稱，以及探索的方法。</span><span class="sxs-lookup"><span data-stu-id="4c3a9-112">Each object in the output list has the name of the Remote Desktop license server, and the method of discovery.</span></span>

</dd> <dt>

<span data-ttu-id="4c3a9-113">*計數* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="4c3a9-113">*Count* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="4c3a9-114">輸出清單中探索到的遠端桌面授權伺服器總數。</span><span class="sxs-lookup"><span data-stu-id="4c3a9-114">The total number of discovered Remote Desktop license servers in the output list.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="4c3a9-115">備註</span><span class="sxs-lookup"><span data-stu-id="4c3a9-115">Remarks</span></span>

<span data-ttu-id="4c3a9-116">若要連接到 \\ 根 \\ CIMV2 \\ microsoft-windows-terminalservices-gateway 命名空間，驗證層級必須包含封包隱私權。</span><span class="sxs-lookup"><span data-stu-id="4c3a9-116">To connect to the \\root\\CIMV2\\TerminalServices namespace, the authentication level must include packet privacy.</span></span> <span data-ttu-id="4c3a9-117">針對 C/c + + 呼叫，這是 **RPC \_ C \_ 驗證 \_ level \_ PKT \_ 隱私權** 的驗證層級。</span><span class="sxs-lookup"><span data-stu-id="4c3a9-117">For C/C++ calls, this is an authentication level of **RPC\_C\_AUTHN\_LEVEL\_PKT\_PRIVACY**.</span></span> <span data-ttu-id="4c3a9-118">針對 Visual Basic 和腳本呼叫，這是 **WbemAuthenticationLevelPktPrivacy** 或 "pktPrivacy" 的驗證層級，其值為6。</span><span class="sxs-lookup"><span data-stu-id="4c3a9-118">For Visual Basic and scripting calls, this is an authentication level of **WbemAuthenticationLevelPktPrivacy** or "pktPrivacy", with a value of 6.</span></span> <span data-ttu-id="4c3a9-119">下列 Visual Basic Scripting Edition (VBScript) 範例示範如何連接到具有封包隱私權的遠端電腦。</span><span class="sxs-lookup"><span data-stu-id="4c3a9-119">The following Visual Basic Scripting Edition (VBScript) example shows how to connect to a remote computer with packet privacy.</span></span>


```VB
strComputer = "RemoteServer1" 
Set objServices = GetObject( _
    "winmgmts:{authenticationLevel=pktPrivacy}!Root/CIMv2/TerminalServices")
```



<span data-ttu-id="4c3a9-120">受控物件格式 (MOF) 檔包含 Windows Management Instrumentation (WMI) 類別的定義。</span><span class="sxs-lookup"><span data-stu-id="4c3a9-120">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="4c3a9-121">MOF 檔案不會安裝為 Microsoft Windows 軟體開發套件 (SDK) 的一部分。</span><span class="sxs-lookup"><span data-stu-id="4c3a9-121">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="4c3a9-122">當您使用伺服器管理員新增相關聯的角色時，它們會安裝在伺服器上。</span><span class="sxs-lookup"><span data-stu-id="4c3a9-122">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="4c3a9-123">如需 MOF 檔案的詳細資訊，請參閱 [受控物件格式 (mof) ](/windows/desktop/WmiSdk/managed-object-format--mof-)。</span><span class="sxs-lookup"><span data-stu-id="4c3a9-123">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="4c3a9-124">規格需求</span><span class="sxs-lookup"><span data-stu-id="4c3a9-124">Requirements</span></span>



| <span data-ttu-id="4c3a9-125">需求</span><span class="sxs-lookup"><span data-stu-id="4c3a9-125">Requirement</span></span> | <span data-ttu-id="4c3a9-126">值</span><span class="sxs-lookup"><span data-stu-id="4c3a9-126">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="4c3a9-127">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="4c3a9-127">Minimum supported client</span></span><br/> | <span data-ttu-id="4c3a9-128">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="4c3a9-128">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="4c3a9-129">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="4c3a9-129">Minimum supported server</span></span><br/> | <span data-ttu-id="4c3a9-130">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="4c3a9-130">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="4c3a9-131">命名空間</span><span class="sxs-lookup"><span data-stu-id="4c3a9-131">Namespace</span></span><br/>                | <span data-ttu-id="4c3a9-132">根 \\ CIMv2 \\ microsoft-windows-terminalservices-gateway</span><span class="sxs-lookup"><span data-stu-id="4c3a9-132">Root\\CIMv2\\TerminalServices</span></span><br/>                                                |
| <span data-ttu-id="4c3a9-133">MOF</span><span class="sxs-lookup"><span data-stu-id="4c3a9-133">MOF</span></span><br/>                      | <dl> <span data-ttu-id="4c3a9-134"><dt>TSCfgWmi mof</dt></span><span class="sxs-lookup"><span data-stu-id="4c3a9-134"><dt>TSCfgWmi.mof</dt></span></span> </dl> |
| <span data-ttu-id="4c3a9-135">DLL</span><span class="sxs-lookup"><span data-stu-id="4c3a9-135">DLL</span></span><br/>                      | <dl> <span data-ttu-id="4c3a9-136"><dt>TSCfgWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="4c3a9-136"><dt>TSCfgWmi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4c3a9-137">另請參閱</span><span class="sxs-lookup"><span data-stu-id="4c3a9-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4c3a9-138">**Win32 \_ TerminalServiceSetting**</span><span class="sxs-lookup"><span data-stu-id="4c3a9-138">**Win32\_TerminalServiceSetting**</span></span>](win32-terminalservicesetting.md)
</dt> </dl>

 

