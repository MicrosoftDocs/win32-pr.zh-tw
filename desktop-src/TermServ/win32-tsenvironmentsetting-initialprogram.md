---
title: Win32_TSEnvironmentSetting 類別的 InitialProgram 方法
description: InitialProgram 方法會將啟動程式的屬性（例如名稱、工作目錄和程式的路徑）設定為在登入遠端桌面工作階段主機 (RD 工作階段主機) 伺服器之後立即啟動。
ms.assetid: e53621cf-ade8-4301-acc0-232866e88488
ms.tgt_platform: multiple
keywords:
- InitialProgram 方法遠端桌面服務
- InitialProgram 方法遠端桌面服務，Win32_TSEnvironmentSetting 類別
- Win32_TSEnvironmentSetting 類別遠端桌面服務，InitialProgram 方法
topic_type:
- apiref
api_name:
- Win32_TSEnvironmentSetting.InitialProgram
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ccd41e1af990e37b8458431106bc2ec9a8489b14
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106968343"
---
# <a name="initialprogram-method-of-the-win32_tsenvironmentsetting-class"></a><span data-ttu-id="73043-106">Win32 TSEnvironmentSetting 類別的 InitialProgram 方法 \_</span><span class="sxs-lookup"><span data-stu-id="73043-106">InitialProgram method of the Win32\_TSEnvironmentSetting class</span></span>

<span data-ttu-id="73043-107">**InitialProgram** 方法會將啟動程式的屬性（例如名稱、工作目錄和程式的路徑）設定為在登入遠端桌面工作階段主機 (RD 工作階段主機) 伺服器之後立即啟動。</span><span class="sxs-lookup"><span data-stu-id="73043-107">The **InitialProgram** method sets startup program properties such as the name, working directory, and path of the program to start immediately after logon to the Remote Desktop Session Host (RD Session Host) server.</span></span>

## <a name="syntax"></a><span data-ttu-id="73043-108">語法</span><span class="sxs-lookup"><span data-stu-id="73043-108">Syntax</span></span>


```mof
uint32 InitialProgram(
  [in] string InitialProgramPath,
  [in] string Startin
);
```



## <a name="parameters"></a><span data-ttu-id="73043-109">參數</span><span class="sxs-lookup"><span data-stu-id="73043-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="73043-110">*InitialProgramPath* \[在\]</span><span class="sxs-lookup"><span data-stu-id="73043-110">*InitialProgramPath* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="73043-111">啟動程式的名稱和路徑。</span><span class="sxs-lookup"><span data-stu-id="73043-111">The name and path of the startup program.</span></span>

</dd> <dt>

<span data-ttu-id="73043-112">*Startin* \[在\]</span><span class="sxs-lookup"><span data-stu-id="73043-112">*Startin* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="73043-113">啟動程式之工作目錄的路徑。</span><span class="sxs-lookup"><span data-stu-id="73043-113">The path to the working directory of the startup program.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="73043-114">傳回值</span><span class="sxs-lookup"><span data-stu-id="73043-114">Return value</span></span>

<span data-ttu-id="73043-115">成功時傳回0，否則會傳回 WMI 錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="73043-115">Returns 0 on success, otherwise returns a WMI error code.</span></span> <span data-ttu-id="73043-116">如需這些值的清單，請參閱 [遠端桌面服務 WMI 提供者錯誤碼](terminal-services-wmi-provider-error-codes.md) 。</span><span class="sxs-lookup"><span data-stu-id="73043-116">Refer to [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md) for a list of these values.</span></span> <span data-ttu-id="73043-117">如果設定位於群組原則控制之下，則方法會傳回錯誤。</span><span class="sxs-lookup"><span data-stu-id="73043-117">The method returns an error if the setting is under group policy control.</span></span>

## <a name="remarks"></a><span data-ttu-id="73043-118">備註</span><span class="sxs-lookup"><span data-stu-id="73043-118">Remarks</span></span>

<span data-ttu-id="73043-119">受控物件格式 (MOF) 檔包含 Windows Management Instrumentation (WMI) 類別的定義。</span><span class="sxs-lookup"><span data-stu-id="73043-119">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="73043-120">MOF 檔案不會安裝為 Microsoft Windows 軟體開發套件 (SDK) 的一部分。</span><span class="sxs-lookup"><span data-stu-id="73043-120">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="73043-121">當您使用伺服器管理員新增相關聯的角色時，它們會安裝在伺服器上。</span><span class="sxs-lookup"><span data-stu-id="73043-121">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="73043-122">如需 MOF 檔案的詳細資訊，請參閱 [受控物件格式 (mof) ](/windows/desktop/WmiSdk/managed-object-format--mof-)。</span><span class="sxs-lookup"><span data-stu-id="73043-122">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="73043-123">規格需求</span><span class="sxs-lookup"><span data-stu-id="73043-123">Requirements</span></span>



| <span data-ttu-id="73043-124">需求</span><span class="sxs-lookup"><span data-stu-id="73043-124">Requirement</span></span> | <span data-ttu-id="73043-125">值</span><span class="sxs-lookup"><span data-stu-id="73043-125">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="73043-126">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="73043-126">Minimum supported client</span></span><br/> | <span data-ttu-id="73043-127">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="73043-127">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="73043-128">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="73043-128">Minimum supported server</span></span><br/> | <span data-ttu-id="73043-129">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="73043-129">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="73043-130">命名空間</span><span class="sxs-lookup"><span data-stu-id="73043-130">Namespace</span></span><br/>                | <span data-ttu-id="73043-131">根 \\ CIMv2 \\ microsoft-windows-terminalservices-gateway</span><span class="sxs-lookup"><span data-stu-id="73043-131">Root\\CIMv2\\TerminalServices</span></span><br/>                                                |
| <span data-ttu-id="73043-132">MOF</span><span class="sxs-lookup"><span data-stu-id="73043-132">MOF</span></span><br/>                      | <dl> <span data-ttu-id="73043-133"><dt>TSCfgWmi mof</dt></span><span class="sxs-lookup"><span data-stu-id="73043-133"><dt>TSCfgWmi.mof</dt></span></span> </dl> |
| <span data-ttu-id="73043-134">DLL</span><span class="sxs-lookup"><span data-stu-id="73043-134">DLL</span></span><br/>                      | <dl> <span data-ttu-id="73043-135"><dt>TSCfgWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="73043-135"><dt>TSCfgWmi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="73043-136">另請參閱</span><span class="sxs-lookup"><span data-stu-id="73043-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="73043-137">**Win32 \_ TSEnvironmentSetting**</span><span class="sxs-lookup"><span data-stu-id="73043-137">**Win32\_TSEnvironmentSetting**</span></span>](win32-tsenvironmentsetting.md)
</dt> </dl>

 

