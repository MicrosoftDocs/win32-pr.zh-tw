---
title: Win32_TerminalServiceSetting 類別的 CanAccessLicenseServer 方法
description: CanAccessLicenseServer 已無法再使用。
ms.assetid: b09fa901-8ae1-431e-8d97-27ee84a84779
ms.tgt_platform: multiple
keywords:
- CanAccessLicenseServer 方法遠端桌面服務
- CanAccessLicenseServer 方法遠端桌面服務，Win32_TerminalServiceSetting 類別
- Win32_TerminalServiceSetting 類別遠端桌面服務，CanAccessLicenseServer 方法
topic_type:
- apiref
api_name:
- Win32_TerminalServiceSetting.CanAccessLicenseServer
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6ffa5bd0e108c0ccceed6890adedea7901834804
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104094123"
---
# <a name="canaccesslicenseserver-method-of-the-win32_terminalservicesetting-class"></a><span data-ttu-id="f675d-106">Win32 TerminalServiceSetting 類別的 CanAccessLicenseServer 方法 \_</span><span class="sxs-lookup"><span data-stu-id="f675d-106">CanAccessLicenseServer method of the Win32\_TerminalServiceSetting class</span></span>

<span data-ttu-id="f675d-107">\[**CanAccessLicenseServer** 不再適用于 Windows Server 2008 R2。\]</span><span class="sxs-lookup"><span data-stu-id="f675d-107">\[**CanAccessLicenseServer** is no longer available for use as of Windows Server 2008 R2.\]</span></span>

<span data-ttu-id="f675d-108">\* \* Windows Server 2008： \* \*</span><span class="sxs-lookup"><span data-stu-id="f675d-108">\*\*Windows Server 2008:  \*\*</span></span>

<span data-ttu-id="f675d-109">決定是否允許遠端桌面工作階段主機 (RD 工作階段主機) 伺服器根據下列內容，向遠端桌面授權伺服器要求遠端桌面服務的用戶端存取授權 (：</span><span class="sxs-lookup"><span data-stu-id="f675d-109">Determines whether the Remote Desktop Session Host (RD Session Host) server is allowed to request Remote Desktop Services client access licenses (RDS CALs) from a Remote Desktop license server based on the following:</span></span>

-   <span data-ttu-id="f675d-110">遠端桌面授權伺服器上的 [授權伺服器安全性群組] 群組原則設定。</span><span class="sxs-lookup"><span data-stu-id="f675d-110">The "license server security group" group policy setting on the Remote Desktop license server.</span></span>
-   <span data-ttu-id="f675d-111">授權伺服器上終端機伺服器電腦本機群組的成員資格。</span><span class="sxs-lookup"><span data-stu-id="f675d-111">Membership in the Terminal Server Computers local group on the license server.</span></span>

## <a name="syntax"></a><span data-ttu-id="f675d-112">語法</span><span class="sxs-lookup"><span data-stu-id="f675d-112">Syntax</span></span>


```mof
uint32 CanAccessLicenseServer(
  [in]  string ServerName,
  [out] uint32 AccessAllowed
);
```



## <a name="parameters"></a><span data-ttu-id="f675d-113">參數</span><span class="sxs-lookup"><span data-stu-id="f675d-113">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f675d-114">*ServerName* \[在\]</span><span class="sxs-lookup"><span data-stu-id="f675d-114">*ServerName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f675d-115">遠端桌面授權伺服器的名稱。</span><span class="sxs-lookup"><span data-stu-id="f675d-115">The name of the Remote Desktop license server.</span></span>

</dd> <dt>

<span data-ttu-id="f675d-116">*AccessAllowed* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="f675d-116">*AccessAllowed* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="f675d-117">是否允許 RD 工作階段主機伺服器向授權伺服器要求 RDS Cal。</span><span class="sxs-lookup"><span data-stu-id="f675d-117">Whether the RD Session Host server is allowed to request RDS CALs from the license server.</span></span>

<dt>

<span data-ttu-id="f675d-118">0</span><span class="sxs-lookup"><span data-stu-id="f675d-118">0</span></span>
</dt> <dd>

<span data-ttu-id="f675d-119">允許要求。</span><span class="sxs-lookup"><span data-stu-id="f675d-119">The request is allowed.</span></span>

</dd> <dt>

<span data-ttu-id="f675d-120">1</span><span class="sxs-lookup"><span data-stu-id="f675d-120">1</span></span>
</dt> <dd>

<span data-ttu-id="f675d-121">不允許此要求。</span><span class="sxs-lookup"><span data-stu-id="f675d-121">The request is not allowed.</span></span>

</dd> </dl> </dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f675d-122">傳回值</span><span class="sxs-lookup"><span data-stu-id="f675d-122">Return value</span></span>

<span data-ttu-id="f675d-123">如果 RD 工作階段主機伺服器具有授權伺服器的存取權，則會傳回 **S \_ OK** 。</span><span class="sxs-lookup"><span data-stu-id="f675d-123">Returns **S\_OK** if the RD Session Host server has access to the license server.</span></span> <span data-ttu-id="f675d-124">如果 RD 工作階段主機伺服器無法存取授權伺服器，則傳回 **\_ FALSE** 。</span><span class="sxs-lookup"><span data-stu-id="f675d-124">Returns **S\_FALSE** if the RD Session Host server does not have access to the license server.</span></span>

## <a name="remarks"></a><span data-ttu-id="f675d-125">備註</span><span class="sxs-lookup"><span data-stu-id="f675d-125">Remarks</span></span>

<span data-ttu-id="f675d-126">[授權伺服器安全性群組] 原則設定可讓您指定允許與授權伺服器連線的 RD 工作階段主機伺服器取得 RDS Cal。</span><span class="sxs-lookup"><span data-stu-id="f675d-126">The "license server security group" policy setting allows you to specify the RD Session Host servers that are permitted to contact the license server to obtain RDS CALs.</span></span> <span data-ttu-id="f675d-127">如果授權伺服器上已啟用此原則設定，授權伺服器將只會回應電腦帳戶是授權伺服器上終端機伺服器電腦本機群組成員之 RD 工作階段主機伺服器的 RDS CAL 要求。</span><span class="sxs-lookup"><span data-stu-id="f675d-127">If the policy setting is enabled on the license server, the license server will only respond to RDS CAL requests from RD Session Host servers whose computer accounts are members of the Terminal Server Computers local group on the license server.</span></span>

<span data-ttu-id="f675d-128">若要連接到 \\ 根 \\ CIMV2 \\ microsoft-windows-terminalservices-gateway 命名空間，驗證層級必須包含封包隱私權。</span><span class="sxs-lookup"><span data-stu-id="f675d-128">To connect to the \\root\\CIMV2\\TerminalServices namespace, the authentication level must include packet privacy.</span></span> <span data-ttu-id="f675d-129">針對 C/c + + 呼叫，這是 **RPC \_ C \_ 驗證 \_ level \_ PKT \_ 隱私權** 的驗證層級。</span><span class="sxs-lookup"><span data-stu-id="f675d-129">For C/C++ calls, this is an authentication level of **RPC\_C\_AUTHN\_LEVEL\_PKT\_PRIVACY**.</span></span> <span data-ttu-id="f675d-130">針對 Visual Basic 和腳本呼叫，這是 **WbemAuthenticationLevelPktPrivacy** 或 "pktPrivacy" 的驗證層級，其值為6。</span><span class="sxs-lookup"><span data-stu-id="f675d-130">For Visual Basic and scripting calls, this is an authentication level of **WbemAuthenticationLevelPktPrivacy** or "pktPrivacy", with a value of 6.</span></span> <span data-ttu-id="f675d-131">下列 Visual Basic Scripting Edition (VBScript) 範例示範如何連接到具有封包隱私權的遠端電腦。</span><span class="sxs-lookup"><span data-stu-id="f675d-131">The following Visual Basic Scripting Edition (VBScript) example shows how to connect to a remote computer with packet privacy.</span></span>


```VB
strComputer = "RemoteServer1" 
Set objServices = GetObject( _
    "winmgmts:{authenticationLevel=pktPrivacy}!Root/CIMv2/TerminalServices")
```



<span data-ttu-id="f675d-132">受控物件格式 (MOF) 檔包含 Windows Management Instrumentation (WMI) 類別的定義。</span><span class="sxs-lookup"><span data-stu-id="f675d-132">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="f675d-133">MOF 檔案不會安裝為 Microsoft Windows 軟體開發套件 (SDK) 的一部分。</span><span class="sxs-lookup"><span data-stu-id="f675d-133">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="f675d-134">當您使用伺服器管理員新增相關聯的角色時，它們會安裝在伺服器上。</span><span class="sxs-lookup"><span data-stu-id="f675d-134">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="f675d-135">如需 MOF 檔案的詳細資訊，請參閱 [受控物件格式 (mof) ](/windows/desktop/WmiSdk/managed-object-format--mof-)。</span><span class="sxs-lookup"><span data-stu-id="f675d-135">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="f675d-136">規格需求</span><span class="sxs-lookup"><span data-stu-id="f675d-136">Requirements</span></span>



| <span data-ttu-id="f675d-137">需求</span><span class="sxs-lookup"><span data-stu-id="f675d-137">Requirement</span></span> | <span data-ttu-id="f675d-138">值</span><span class="sxs-lookup"><span data-stu-id="f675d-138">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="f675d-139">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="f675d-139">Minimum supported client</span></span><br/> | <span data-ttu-id="f675d-140">都不支援</span><span class="sxs-lookup"><span data-stu-id="f675d-140">None supported</span></span><br/>                                                               |
| <span data-ttu-id="f675d-141">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="f675d-141">Minimum supported server</span></span><br/> | <span data-ttu-id="f675d-142">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="f675d-142">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="f675d-143">用戶端支援結束</span><span class="sxs-lookup"><span data-stu-id="f675d-143">End of client support</span></span><br/>    | <span data-ttu-id="f675d-144">都不支援</span><span class="sxs-lookup"><span data-stu-id="f675d-144">None supported</span></span><br/>                                                               |
| <span data-ttu-id="f675d-145">伺服器支援結束</span><span class="sxs-lookup"><span data-stu-id="f675d-145">End of server support</span></span><br/>    | <span data-ttu-id="f675d-146">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="f675d-146">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="f675d-147">命名空間</span><span class="sxs-lookup"><span data-stu-id="f675d-147">Namespace</span></span><br/>                | <span data-ttu-id="f675d-148">根 \\ CIMv2 \\ microsoft-windows-terminalservices-gateway</span><span class="sxs-lookup"><span data-stu-id="f675d-148">Root\\CIMv2\\TerminalServices</span></span><br/>                                                |
| <span data-ttu-id="f675d-149">MOF</span><span class="sxs-lookup"><span data-stu-id="f675d-149">MOF</span></span><br/>                      | <dl> <span data-ttu-id="f675d-150"><dt>TSCfgWmi mof</dt></span><span class="sxs-lookup"><span data-stu-id="f675d-150"><dt>TSCfgWmi.mof</dt></span></span> </dl> |
| <span data-ttu-id="f675d-151">DLL</span><span class="sxs-lookup"><span data-stu-id="f675d-151">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f675d-152"><dt>TSCfgWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f675d-152"><dt>TSCfgWmi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f675d-153">另請參閱</span><span class="sxs-lookup"><span data-stu-id="f675d-153">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f675d-154">**Win32 \_ TerminalServiceSetting**</span><span class="sxs-lookup"><span data-stu-id="f675d-154">**Win32\_TerminalServiceSetting**</span></span>](win32-terminalservicesetting.md)
</dt> </dl>

 

