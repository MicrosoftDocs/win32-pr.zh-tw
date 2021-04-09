---
title: Win32_TerminalServiceSetting 類別的 GetDomain 方法
description: 抓取遠端桌面工作階段主機 (RD 工作階段主機) 伺服器為其成員之網域的名稱。
ms.assetid: 11d58068-56df-4040-b7ba-afdd55bd417a
ms.tgt_platform: multiple
keywords:
- GetDomain 方法遠端桌面服務
- GetDomain 方法遠端桌面服務，Win32_TerminalServiceSetting 類別
- Win32_TerminalServiceSetting 類別遠端桌面服務，GetDomain 方法
topic_type:
- apiref
api_name:
- Win32_TerminalServiceSetting.GetDomain
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c8e9b2e5ba62f12c67a753cf8e5c41e8296b31e9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103934004"
---
# <a name="getdomain-method-of-the-win32_terminalservicesetting-class"></a><span data-ttu-id="80e05-106">Win32 TerminalServiceSetting 類別的 GetDomain 方法 \_</span><span class="sxs-lookup"><span data-stu-id="80e05-106">GetDomain method of the Win32\_TerminalServiceSetting class</span></span>

<span data-ttu-id="80e05-107">抓取遠端桌面工作階段主機 (RD 工作階段主機) 伺服器為其成員之網域的名稱。</span><span class="sxs-lookup"><span data-stu-id="80e05-107">Retrieves the name of the domain that the Remote Desktop Session Host (RD Session Host) server is a member of.</span></span>

## <a name="syntax"></a><span data-ttu-id="80e05-108">語法</span><span class="sxs-lookup"><span data-stu-id="80e05-108">Syntax</span></span>


```mof
uint32 GetDomain(
  [out] string Domain
);
```



## <a name="parameters"></a><span data-ttu-id="80e05-109">參數</span><span class="sxs-lookup"><span data-stu-id="80e05-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="80e05-110">*網域* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="80e05-110">*Domain* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="80e05-111">RD 工作階段主機伺服器的功能變數名稱。</span><span class="sxs-lookup"><span data-stu-id="80e05-111">The domain name of the RD Session Host server.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="80e05-112">備註</span><span class="sxs-lookup"><span data-stu-id="80e05-112">Remarks</span></span>

<span data-ttu-id="80e05-113">若要連接到 \\ 根 \\ CIMV2 \\ microsoft-windows-terminalservices-gateway 命名空間，驗證層級必須包含封包隱私權。</span><span class="sxs-lookup"><span data-stu-id="80e05-113">To connect to the \\root\\CIMV2\\TerminalServices namespace, the authentication level must include packet privacy.</span></span> <span data-ttu-id="80e05-114">針對 C/c + + 呼叫，這是 **RPC \_ C \_ 驗證 \_ level \_ PKT \_ 隱私權** 的驗證層級。</span><span class="sxs-lookup"><span data-stu-id="80e05-114">For C/C++ calls, this is an authentication level of **RPC\_C\_AUTHN\_LEVEL\_PKT\_PRIVACY**.</span></span> <span data-ttu-id="80e05-115">針對 Visual Basic 和腳本呼叫，這是 **WbemAuthenticationLevelPktPrivacy** 或 "pktPrivacy" 的驗證層級，其值為6。</span><span class="sxs-lookup"><span data-stu-id="80e05-115">For Visual Basic and scripting calls, this is an authentication level of **WbemAuthenticationLevelPktPrivacy** or "pktPrivacy", with a value of 6.</span></span> <span data-ttu-id="80e05-116">下列 Visual Basic Scripting Edition (VBScript) 範例示範如何連接到具有封包隱私權的遠端電腦。</span><span class="sxs-lookup"><span data-stu-id="80e05-116">The following Visual Basic Scripting Edition (VBScript) example shows how to connect to a remote computer with packet privacy.</span></span>


```VB
strComputer = "RemoteServer1" 
Set objServices = GetObject( _
    "winmgmts:{authenticationLevel=pktPrivacy}!Root/CIMv2/TerminalServices")
```



<span data-ttu-id="80e05-117">受控物件格式 (MOF) 檔包含 Windows Management Instrumentation (WMI) 類別的定義。</span><span class="sxs-lookup"><span data-stu-id="80e05-117">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="80e05-118">MOF 檔案不會安裝為 Microsoft Windows 軟體開發套件 (SDK) 的一部分。</span><span class="sxs-lookup"><span data-stu-id="80e05-118">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="80e05-119">當您使用伺服器管理員新增相關聯的角色時，它們會安裝在伺服器上。</span><span class="sxs-lookup"><span data-stu-id="80e05-119">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="80e05-120">如需 MOF 檔案的詳細資訊，請參閱 [受控物件格式 (mof) ](/windows/desktop/WmiSdk/managed-object-format--mof-)。</span><span class="sxs-lookup"><span data-stu-id="80e05-120">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="80e05-121">規格需求</span><span class="sxs-lookup"><span data-stu-id="80e05-121">Requirements</span></span>



| <span data-ttu-id="80e05-122">需求</span><span class="sxs-lookup"><span data-stu-id="80e05-122">Requirement</span></span> | <span data-ttu-id="80e05-123">值</span><span class="sxs-lookup"><span data-stu-id="80e05-123">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="80e05-124">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="80e05-124">Minimum supported client</span></span><br/> | <span data-ttu-id="80e05-125">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="80e05-125">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="80e05-126">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="80e05-126">Minimum supported server</span></span><br/> | <span data-ttu-id="80e05-127">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="80e05-127">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="80e05-128">命名空間</span><span class="sxs-lookup"><span data-stu-id="80e05-128">Namespace</span></span><br/>                | <span data-ttu-id="80e05-129">根 \\ CIMv2 \\ microsoft-windows-terminalservices-gateway</span><span class="sxs-lookup"><span data-stu-id="80e05-129">Root\\CIMv2\\TerminalServices</span></span><br/>                                                |
| <span data-ttu-id="80e05-130">MOF</span><span class="sxs-lookup"><span data-stu-id="80e05-130">MOF</span></span><br/>                      | <dl> <span data-ttu-id="80e05-131"><dt>TSCfgWmi mof</dt></span><span class="sxs-lookup"><span data-stu-id="80e05-131"><dt>TSCfgWmi.mof</dt></span></span> </dl> |
| <span data-ttu-id="80e05-132">DLL</span><span class="sxs-lookup"><span data-stu-id="80e05-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="80e05-133"><dt>TSCfgWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="80e05-133"><dt>TSCfgWmi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="80e05-134">另請參閱</span><span class="sxs-lookup"><span data-stu-id="80e05-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="80e05-135">**Win32 \_ TerminalServiceSetting**</span><span class="sxs-lookup"><span data-stu-id="80e05-135">**Win32\_TerminalServiceSetting**</span></span>](win32-terminalservicesetting.md)
</dt> </dl>

 

