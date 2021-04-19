---
title: Win32_TerminalServiceSetting 類別的 GetWinstationDriverNames 方法
description: 抓取 Winstation 驅動程式名稱的清單。
ms.assetid: 578c2a07-17e7-4bd6-b520-942cd48ee40f
ms.tgt_platform: multiple
keywords:
- GetWinstationDriverNames 方法遠端桌面服務
- GetWinstationDriverNames 方法遠端桌面服務，Win32_TerminalServiceSetting 類別
- Win32_TerminalServiceSetting 類別遠端桌面服務，GetWinstationDriverNames 方法
topic_type:
- apiref
api_name:
- Win32_TerminalServiceSetting.GetWinstationDriverNames
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 41bc0157f368edf129f578765c1b8d73f6f48a33
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106966299"
---
# <a name="getwinstationdrivernames-method-of-the-win32_terminalservicesetting-class"></a><span data-ttu-id="577df-106">Win32 TerminalServiceSetting 類別的 GetWinstationDriverNames 方法 \_</span><span class="sxs-lookup"><span data-stu-id="577df-106">GetWinstationDriverNames method of the Win32\_TerminalServiceSetting class</span></span>

<span data-ttu-id="577df-107">抓取 Winstation 驅動程式名稱的清單。</span><span class="sxs-lookup"><span data-stu-id="577df-107">Retrieves a list of Winstation driver names.</span></span>

## <a name="syntax"></a><span data-ttu-id="577df-108">語法</span><span class="sxs-lookup"><span data-stu-id="577df-108">Syntax</span></span>


```mof
uint32 GetWinstationDriverNames(
  [out] string WinstaDriverNames[]
);
```



## <a name="parameters"></a><span data-ttu-id="577df-109">參數</span><span class="sxs-lookup"><span data-stu-id="577df-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="577df-110">*WinstaDriverNames* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="577df-110">*WinstaDriverNames* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="577df-111">Winstation 驅動程式名稱的清單。</span><span class="sxs-lookup"><span data-stu-id="577df-111">The list of Winstation driver names.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="577df-112">備註</span><span class="sxs-lookup"><span data-stu-id="577df-112">Remarks</span></span>

<span data-ttu-id="577df-113">若要連接到 \\ 根 \\ CIMV2 \\ microsoft-windows-terminalservices-gateway 命名空間，驗證層級必須包含封包隱私權。</span><span class="sxs-lookup"><span data-stu-id="577df-113">To connect to the \\root\\CIMV2\\TerminalServices namespace, the authentication level must include packet privacy.</span></span> <span data-ttu-id="577df-114">針對 C/c + + 呼叫，這是 **RPC \_ C \_ 驗證 \_ level \_ PKT \_ 隱私權** 的驗證層級。</span><span class="sxs-lookup"><span data-stu-id="577df-114">For C/C++ calls, this is an authentication level of **RPC\_C\_AUTHN\_LEVEL\_PKT\_PRIVACY**.</span></span> <span data-ttu-id="577df-115">針對 Visual Basic 和腳本呼叫，這是 **WbemAuthenticationLevelPktPrivacy** 或 "pktPrivacy" 的驗證層級，其值為6。</span><span class="sxs-lookup"><span data-stu-id="577df-115">For Visual Basic and scripting calls, this is an authentication level of **WbemAuthenticationLevelPktPrivacy** or "pktPrivacy", with a value of 6.</span></span> <span data-ttu-id="577df-116">下列 Visual Basic Scripting Edition (VBScript) 範例示範如何連接到具有封包隱私權的遠端電腦。</span><span class="sxs-lookup"><span data-stu-id="577df-116">The following Visual Basic Scripting Edition (VBScript) example shows how to connect to a remote computer with packet privacy.</span></span>


```VB
strComputer = "RemoteServer1" 
Set objServices = GetObject( _
    "winmgmts:{authenticationLevel=pktPrivacy}!Root/CIMv2/TerminalServices")
```



<span data-ttu-id="577df-117">受控物件格式 (MOF) 檔包含 Windows Management Instrumentation (WMI) 類別的定義。</span><span class="sxs-lookup"><span data-stu-id="577df-117">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="577df-118">MOF 檔案不會安裝為 Microsoft Windows 軟體開發套件 (SDK) 的一部分。</span><span class="sxs-lookup"><span data-stu-id="577df-118">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="577df-119">當您使用伺服器管理員新增相關聯的角色時，它們會安裝在伺服器上。</span><span class="sxs-lookup"><span data-stu-id="577df-119">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="577df-120">如需 MOF 檔案的詳細資訊，請參閱 [受控物件格式 (mof) ](/windows/desktop/WmiSdk/managed-object-format--mof-)。</span><span class="sxs-lookup"><span data-stu-id="577df-120">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="577df-121">規格需求</span><span class="sxs-lookup"><span data-stu-id="577df-121">Requirements</span></span>



| <span data-ttu-id="577df-122">需求</span><span class="sxs-lookup"><span data-stu-id="577df-122">Requirement</span></span> | <span data-ttu-id="577df-123">值</span><span class="sxs-lookup"><span data-stu-id="577df-123">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="577df-124">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="577df-124">Minimum supported client</span></span><br/> | <span data-ttu-id="577df-125">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="577df-125">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="577df-126">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="577df-126">Minimum supported server</span></span><br/> | <span data-ttu-id="577df-127">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="577df-127">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="577df-128">命名空間</span><span class="sxs-lookup"><span data-stu-id="577df-128">Namespace</span></span><br/>                | <span data-ttu-id="577df-129">根 \\ CIMv2 \\ microsoft-windows-terminalservices-gateway</span><span class="sxs-lookup"><span data-stu-id="577df-129">Root\\CIMv2\\TerminalServices</span></span><br/>                                                |
| <span data-ttu-id="577df-130">MOF</span><span class="sxs-lookup"><span data-stu-id="577df-130">MOF</span></span><br/>                      | <dl> <span data-ttu-id="577df-131"><dt>TSCfgWmi mof</dt></span><span class="sxs-lookup"><span data-stu-id="577df-131"><dt>TSCfgWmi.mof</dt></span></span> </dl> |
| <span data-ttu-id="577df-132">DLL</span><span class="sxs-lookup"><span data-stu-id="577df-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="577df-133"><dt>TSCfgWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="577df-133"><dt>TSCfgWmi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="577df-134">另請參閱</span><span class="sxs-lookup"><span data-stu-id="577df-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="577df-135">**Win32 \_ TerminalServiceSetting**</span><span class="sxs-lookup"><span data-stu-id="577df-135">**Win32\_TerminalServiceSetting**</span></span>](win32-terminalservicesetting.md)
</dt> </dl>

 

