---
title: Win32_TerminalServiceSetting 類別的 GetGracePeriodDays 方法
description: 抓取遠端桌面工作階段主機 (RD 工作階段主機) 伺服器的遠端桌面服務授權寬限期內剩餘的天數。 零值表示寬限期結束。
ms.assetid: d84d7815-ee09-43d9-a370-993d23f14898
ms.tgt_platform: multiple
keywords:
- GetGracePeriodDays 方法遠端桌面服務
- GetGracePeriodDays 方法遠端桌面服務，Win32_TerminalServiceSetting 類別
- Win32_TerminalServiceSetting 類別遠端桌面服務，GetGracePeriodDays 方法
topic_type:
- apiref
api_name:
- Win32_TerminalServiceSetting.GetGracePeriodDays
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0faaf525bb74a8ac4b0164c181e5a20cfb215d7b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104317167"
---
# <a name="getgraceperioddays-method-of-the-win32_terminalservicesetting-class"></a><span data-ttu-id="968f9-107">Win32 TerminalServiceSetting 類別的 GetGracePeriodDays 方法 \_</span><span class="sxs-lookup"><span data-stu-id="968f9-107">GetGracePeriodDays method of the Win32\_TerminalServiceSetting class</span></span>

<span data-ttu-id="968f9-108">抓取遠端桌面工作階段主機 (RD 工作階段主機) 伺服器的遠端桌面服務授權寬限期內剩餘的天數。</span><span class="sxs-lookup"><span data-stu-id="968f9-108">Retrieves the number of days that are remaining in the Remote Desktop Services licensing grace period for a Remote Desktop Session Host (RD Session Host) server.</span></span> <span data-ttu-id="968f9-109">零值表示寬限期結束。</span><span class="sxs-lookup"><span data-stu-id="968f9-109">A zero value indicates that the grace period is over.</span></span>

## <a name="syntax"></a><span data-ttu-id="968f9-110">語法</span><span class="sxs-lookup"><span data-stu-id="968f9-110">Syntax</span></span>


```mof
uint32 GetGracePeriodDays(
  [out] uint32 DaysLeft
);
```



## <a name="parameters"></a><span data-ttu-id="968f9-111">參數</span><span class="sxs-lookup"><span data-stu-id="968f9-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="968f9-112">*DaysLeft* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="968f9-112">*DaysLeft* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="968f9-113">寬限期內剩餘的天數。</span><span class="sxs-lookup"><span data-stu-id="968f9-113">The number of days that are remaining in the grace period.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="968f9-114">備註</span><span class="sxs-lookup"><span data-stu-id="968f9-114">Remarks</span></span>

<span data-ttu-id="968f9-115">若要連接到 \\ 根 \\ CIMV2 \\ microsoft-windows-terminalservices-gateway 命名空間，驗證層級必須包含封包隱私權。</span><span class="sxs-lookup"><span data-stu-id="968f9-115">To connect to the \\root\\CIMV2\\TerminalServices namespace, the authentication level must include packet privacy.</span></span> <span data-ttu-id="968f9-116">針對 C/c + + 呼叫，這是 **RPC \_ C \_ 驗證 \_ level \_ PKT \_ 隱私權** 的驗證層級。</span><span class="sxs-lookup"><span data-stu-id="968f9-116">For C/C++ calls, this is an authentication level of **RPC\_C\_AUTHN\_LEVEL\_PKT\_PRIVACY**.</span></span> <span data-ttu-id="968f9-117">針對 Visual Basic 和腳本呼叫，這是 **WbemAuthenticationLevelPktPrivacy** 或 "pktPrivacy" 的驗證層級，其值為6。</span><span class="sxs-lookup"><span data-stu-id="968f9-117">For Visual Basic and scripting calls, this is an authentication level of **WbemAuthenticationLevelPktPrivacy** or "pktPrivacy", with a value of 6.</span></span> <span data-ttu-id="968f9-118">下列 Visual Basic Scripting Edition (VBScript) 範例示範如何連接到具有封包隱私權的遠端電腦。</span><span class="sxs-lookup"><span data-stu-id="968f9-118">The following Visual Basic Scripting Edition (VBScript) example shows how to connect to a remote computer with packet privacy.</span></span>


```VB
strComputer = "RemoteServer1" 
Set objServices = GetObject( _
    "winmgmts:{authenticationLevel=pktPrivacy}!Root/CIMv2/TerminalServices")
```



<span data-ttu-id="968f9-119">受控物件格式 (MOF) 檔包含 Windows Management Instrumentation (WMI) 類別的定義。</span><span class="sxs-lookup"><span data-stu-id="968f9-119">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="968f9-120">MOF 檔案不會安裝為 Microsoft Windows 軟體開發套件 (SDK) 的一部分。</span><span class="sxs-lookup"><span data-stu-id="968f9-120">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="968f9-121">當您使用伺服器管理員新增相關聯的角色時，它們會安裝在伺服器上。</span><span class="sxs-lookup"><span data-stu-id="968f9-121">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="968f9-122">如需 MOF 檔案的詳細資訊，請參閱 [受控物件格式 (mof) ](/windows/desktop/WmiSdk/managed-object-format--mof-)。</span><span class="sxs-lookup"><span data-stu-id="968f9-122">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="968f9-123">規格需求</span><span class="sxs-lookup"><span data-stu-id="968f9-123">Requirements</span></span>



| <span data-ttu-id="968f9-124">需求</span><span class="sxs-lookup"><span data-stu-id="968f9-124">Requirement</span></span> | <span data-ttu-id="968f9-125">值</span><span class="sxs-lookup"><span data-stu-id="968f9-125">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="968f9-126">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="968f9-126">Minimum supported client</span></span><br/> | <span data-ttu-id="968f9-127">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="968f9-127">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="968f9-128">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="968f9-128">Minimum supported server</span></span><br/> | <span data-ttu-id="968f9-129">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="968f9-129">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="968f9-130">命名空間</span><span class="sxs-lookup"><span data-stu-id="968f9-130">Namespace</span></span><br/>                | <span data-ttu-id="968f9-131">根 \\ CIMv2 \\ microsoft-windows-terminalservices-gateway</span><span class="sxs-lookup"><span data-stu-id="968f9-131">Root\\CIMv2\\TerminalServices</span></span><br/>                                                |
| <span data-ttu-id="968f9-132">MOF</span><span class="sxs-lookup"><span data-stu-id="968f9-132">MOF</span></span><br/>                      | <dl> <span data-ttu-id="968f9-133"><dt>TSCfgWmi mof</dt></span><span class="sxs-lookup"><span data-stu-id="968f9-133"><dt>TSCfgWmi.mof</dt></span></span> </dl> |
| <span data-ttu-id="968f9-134">DLL</span><span class="sxs-lookup"><span data-stu-id="968f9-134">DLL</span></span><br/>                      | <dl> <span data-ttu-id="968f9-135"><dt>TSCfgWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="968f9-135"><dt>TSCfgWmi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="968f9-136">另請參閱</span><span class="sxs-lookup"><span data-stu-id="968f9-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="968f9-137">**Win32 \_ TerminalServiceSetting**</span><span class="sxs-lookup"><span data-stu-id="968f9-137">**Win32\_TerminalServiceSetting**</span></span>](win32-terminalservicesetting.md)
</dt> </dl>

 

