---
title: Win32_TSLogonSetting 類別的 SetPromptForPassword 方法
description: SetPromptForPassword 方法會設定 PromptForPassword 屬性。
ms.assetid: eeeed374-4a8a-4014-833c-d931be3ef455
ms.tgt_platform: multiple
keywords:
- SetPromptForPassword 方法遠端桌面服務
- SetPromptForPassword 方法遠端桌面服務，Win32_TSLogonSetting 類別
- Win32_TSLogonSetting 類別遠端桌面服務，SetPromptForPassword 方法
topic_type:
- apiref
api_name:
- Win32_TSLogonSetting.SetPromptForPassword
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f86dc065a143505ea81bce78d9bf787fae6b0a33
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106968180"
---
# <a name="setpromptforpassword-method-of-the-win32_tslogonsetting-class"></a><span data-ttu-id="aa71a-106">Win32 TSLogonSetting 類別的 SetPromptForPassword 方法 \_</span><span class="sxs-lookup"><span data-stu-id="aa71a-106">SetPromptForPassword method of the Win32\_TSLogonSetting class</span></span>

<span data-ttu-id="aa71a-107">**SetPromptForPassword** 方法會設定 **PromptForPassword** 屬性。</span><span class="sxs-lookup"><span data-stu-id="aa71a-107">The **SetPromptForPassword** method sets the **PromptForPassword** property.</span></span>

## <a name="syntax"></a><span data-ttu-id="aa71a-108">語法</span><span class="sxs-lookup"><span data-stu-id="aa71a-108">Syntax</span></span>


```mof
uint32 SetPromptForPassword(
  [in] uint32 PromptForPassword
);
```



## <a name="parameters"></a><span data-ttu-id="aa71a-109">參數</span><span class="sxs-lookup"><span data-stu-id="aa71a-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="aa71a-110">*PromptForPassword* \[在\]</span><span class="sxs-lookup"><span data-stu-id="aa71a-110">*PromptForPassword* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="aa71a-111">旗標停用或啟用 **PromptForPassword** 屬性。</span><span class="sxs-lookup"><span data-stu-id="aa71a-111">Flag disabling or enabling the **PromptForPassword** property.</span></span>

<dt>

<span data-ttu-id="aa71a-112">0</span><span class="sxs-lookup"><span data-stu-id="aa71a-112">0</span></span>
</dt> <dd>

<span data-ttu-id="aa71a-113">停用密碼提示。</span><span class="sxs-lookup"><span data-stu-id="aa71a-113">Disables password-prompting.</span></span>

</dd> <dt>

<span data-ttu-id="aa71a-114">1</span><span class="sxs-lookup"><span data-stu-id="aa71a-114">1</span></span>
</dt> <dd>

<span data-ttu-id="aa71a-115">啟用密碼提示。</span><span class="sxs-lookup"><span data-stu-id="aa71a-115">Enables password-prompting.</span></span>

</dd> </dl> </dd> </dl>

## <a name="return-value"></a><span data-ttu-id="aa71a-116">傳回值</span><span class="sxs-lookup"><span data-stu-id="aa71a-116">Return value</span></span>

<span data-ttu-id="aa71a-117">成功時傳回成功，否則會傳回 WMI 錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="aa71a-117">Returns Success on success, otherwise returns a WMI error code.</span></span> <span data-ttu-id="aa71a-118">如需這些值的清單，請參閱 [遠端桌面服務 WMI 提供者錯誤碼](terminal-services-wmi-provider-error-codes.md) 。</span><span class="sxs-lookup"><span data-stu-id="aa71a-118">Refer to [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md) for a list of these values.</span></span> <span data-ttu-id="aa71a-119">如果設定位於群組原則控制之下，則方法會傳回錯誤。</span><span class="sxs-lookup"><span data-stu-id="aa71a-119">The method returns an error if the setting is under group policy control.</span></span>

<dl> <dt>

<span data-ttu-id="aa71a-120">**FALSE** (0) </span><span class="sxs-lookup"><span data-stu-id="aa71a-120">**FALSE** (0)</span></span>
</dt> <dt>

<span data-ttu-id="aa71a-121">**TRUE** (1) </span><span class="sxs-lookup"><span data-stu-id="aa71a-121">**TRUE** (1)</span></span>
</dt> </dl>

## <a name="remarks"></a><span data-ttu-id="aa71a-122">備註</span><span class="sxs-lookup"><span data-stu-id="aa71a-122">Remarks</span></span>

<span data-ttu-id="aa71a-123">受控物件格式 (MOF) 檔包含 Windows Management Instrumentation (WMI) 類別的定義。</span><span class="sxs-lookup"><span data-stu-id="aa71a-123">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="aa71a-124">MOF 檔案不會安裝為 Microsoft Windows 軟體開發套件 (SDK) 的一部分。</span><span class="sxs-lookup"><span data-stu-id="aa71a-124">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="aa71a-125">當您使用伺服器管理員新增相關聯的角色時，它們會安裝在伺服器上。</span><span class="sxs-lookup"><span data-stu-id="aa71a-125">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="aa71a-126">如需 MOF 檔案的詳細資訊，請參閱 [受控物件格式 (mof) ](/windows/desktop/WmiSdk/managed-object-format--mof-)。</span><span class="sxs-lookup"><span data-stu-id="aa71a-126">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="aa71a-127">規格需求</span><span class="sxs-lookup"><span data-stu-id="aa71a-127">Requirements</span></span>



| <span data-ttu-id="aa71a-128">需求</span><span class="sxs-lookup"><span data-stu-id="aa71a-128">Requirement</span></span> | <span data-ttu-id="aa71a-129">值</span><span class="sxs-lookup"><span data-stu-id="aa71a-129">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="aa71a-130">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="aa71a-130">Minimum supported client</span></span><br/> | <span data-ttu-id="aa71a-131">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="aa71a-131">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="aa71a-132">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="aa71a-132">Minimum supported server</span></span><br/> | <span data-ttu-id="aa71a-133">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="aa71a-133">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="aa71a-134">命名空間</span><span class="sxs-lookup"><span data-stu-id="aa71a-134">Namespace</span></span><br/>                | <span data-ttu-id="aa71a-135">根 \\ CIMv2 \\ microsoft-windows-terminalservices-gateway</span><span class="sxs-lookup"><span data-stu-id="aa71a-135">Root\\CIMv2\\TerminalServices</span></span><br/>                                                |
| <span data-ttu-id="aa71a-136">MOF</span><span class="sxs-lookup"><span data-stu-id="aa71a-136">MOF</span></span><br/>                      | <dl> <span data-ttu-id="aa71a-137"><dt>TSCfgWmi mof</dt></span><span class="sxs-lookup"><span data-stu-id="aa71a-137"><dt>TSCfgWmi.mof</dt></span></span> </dl> |
| <span data-ttu-id="aa71a-138">DLL</span><span class="sxs-lookup"><span data-stu-id="aa71a-138">DLL</span></span><br/>                      | <dl> <span data-ttu-id="aa71a-139"><dt>TSCfgWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="aa71a-139"><dt>TSCfgWmi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="aa71a-140">另請參閱</span><span class="sxs-lookup"><span data-stu-id="aa71a-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="aa71a-141">**Win32 \_ TSLogonSetting**</span><span class="sxs-lookup"><span data-stu-id="aa71a-141">**Win32\_TSLogonSetting**</span></span>](win32-tslogonsetting.md)
</dt> </dl>

 

