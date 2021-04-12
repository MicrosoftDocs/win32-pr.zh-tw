---
title: Win32_TSLogonSetting 類別的 ExplicitLogon 方法
description: ExplicitLogon 方法會設定要用於驗證的認證。
ms.assetid: cfd43396-0d66-4d5e-81c8-5c0e66422dc5
ms.tgt_platform: multiple
keywords:
- ExplicitLogon 方法遠端桌面服務
- ExplicitLogon 方法遠端桌面服務，Win32_TSLogonSetting 類別
- Win32_TSLogonSetting 類別遠端桌面服務，ExplicitLogon 方法
topic_type:
- apiref
api_name:
- Win32_TSLogonSetting.ExplicitLogon
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ef72b6b0f0ede0954a6fc74030a9f0f1d4976935
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104384958"
---
# <a name="explicitlogon-method-of-the-win32_tslogonsetting-class"></a><span data-ttu-id="0d66d-106">Win32 TSLogonSetting 類別的 ExplicitLogon 方法 \_</span><span class="sxs-lookup"><span data-stu-id="0d66d-106">ExplicitLogon method of the Win32\_TSLogonSetting class</span></span>

<span data-ttu-id="0d66d-107">**ExplicitLogon** 方法會設定要用於驗證的認證。</span><span class="sxs-lookup"><span data-stu-id="0d66d-107">The **ExplicitLogon** method sets the credentials to use for authentication.</span></span>

## <a name="syntax"></a><span data-ttu-id="0d66d-108">語法</span><span class="sxs-lookup"><span data-stu-id="0d66d-108">Syntax</span></span>


```mof
uint32 ExplicitLogon(
  [in] string UserName,
  [in] string Domain,
  [in] string Password
);
```



## <a name="parameters"></a><span data-ttu-id="0d66d-109">參數</span><span class="sxs-lookup"><span data-stu-id="0d66d-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0d66d-110">使用者 *名稱* \[在\]</span><span class="sxs-lookup"><span data-stu-id="0d66d-110">*UserName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0d66d-111">使用者名稱登入認證。</span><span class="sxs-lookup"><span data-stu-id="0d66d-111">The user name logon credential.</span></span>

</dd> <dt>

<span data-ttu-id="0d66d-112">*網域* \[在\]</span><span class="sxs-lookup"><span data-stu-id="0d66d-112">*Domain* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0d66d-113">網域登入認證。</span><span class="sxs-lookup"><span data-stu-id="0d66d-113">The domain logon credential.</span></span>

</dd> <dt>

<span data-ttu-id="0d66d-114">*密碼* \[在\]</span><span class="sxs-lookup"><span data-stu-id="0d66d-114">*Password* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0d66d-115">密碼登入認證。</span><span class="sxs-lookup"><span data-stu-id="0d66d-115">The password logon credential.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0d66d-116">傳回值</span><span class="sxs-lookup"><span data-stu-id="0d66d-116">Return value</span></span>

<span data-ttu-id="0d66d-117">成功時傳回成功，否則會傳回 WMI 錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="0d66d-117">Returns Success on success, otherwise returns a WMI error code.</span></span> <span data-ttu-id="0d66d-118">如需這些值的清單，請參閱 [遠端桌面服務 WMI 提供者錯誤碼](terminal-services-wmi-provider-error-codes.md) 。</span><span class="sxs-lookup"><span data-stu-id="0d66d-118">Refer to [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md) for a list of these values.</span></span> <span data-ttu-id="0d66d-119">如果設定位於群組原則控制之下，則方法會傳回錯誤。</span><span class="sxs-lookup"><span data-stu-id="0d66d-119">The method returns an error if the setting is under group policy control.</span></span>

## <a name="remarks"></a><span data-ttu-id="0d66d-120">備註</span><span class="sxs-lookup"><span data-stu-id="0d66d-120">Remarks</span></span>

<span data-ttu-id="0d66d-121">受控物件格式 (MOF) 檔包含 Windows Management Instrumentation (WMI) 類別的定義。</span><span class="sxs-lookup"><span data-stu-id="0d66d-121">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="0d66d-122">MOF 檔案不會安裝為 Microsoft Windows 軟體開發套件 (SDK) 的一部分。</span><span class="sxs-lookup"><span data-stu-id="0d66d-122">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="0d66d-123">當您使用伺服器管理員新增相關聯的角色時，它們會安裝在伺服器上。</span><span class="sxs-lookup"><span data-stu-id="0d66d-123">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="0d66d-124">如需 MOF 檔案的詳細資訊，請參閱 [受控物件格式 (mof) ](/windows/desktop/WmiSdk/managed-object-format--mof-)。</span><span class="sxs-lookup"><span data-stu-id="0d66d-124">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="0d66d-125">規格需求</span><span class="sxs-lookup"><span data-stu-id="0d66d-125">Requirements</span></span>



| <span data-ttu-id="0d66d-126">需求</span><span class="sxs-lookup"><span data-stu-id="0d66d-126">Requirement</span></span> | <span data-ttu-id="0d66d-127">值</span><span class="sxs-lookup"><span data-stu-id="0d66d-127">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="0d66d-128">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="0d66d-128">Minimum supported client</span></span><br/> | <span data-ttu-id="0d66d-129">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="0d66d-129">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="0d66d-130">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="0d66d-130">Minimum supported server</span></span><br/> | <span data-ttu-id="0d66d-131">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="0d66d-131">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="0d66d-132">命名空間</span><span class="sxs-lookup"><span data-stu-id="0d66d-132">Namespace</span></span><br/>                | <span data-ttu-id="0d66d-133">根 \\ CIMv2 \\ microsoft-windows-terminalservices-gateway</span><span class="sxs-lookup"><span data-stu-id="0d66d-133">Root\\CIMv2\\TerminalServices</span></span><br/>                                                |
| <span data-ttu-id="0d66d-134">MOF</span><span class="sxs-lookup"><span data-stu-id="0d66d-134">MOF</span></span><br/>                      | <dl> <span data-ttu-id="0d66d-135"><dt>TSCfgWmi mof</dt></span><span class="sxs-lookup"><span data-stu-id="0d66d-135"><dt>TSCfgWmi.mof</dt></span></span> </dl> |
| <span data-ttu-id="0d66d-136">DLL</span><span class="sxs-lookup"><span data-stu-id="0d66d-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="0d66d-137"><dt>TSCfgWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0d66d-137"><dt>TSCfgWmi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0d66d-138">另請參閱</span><span class="sxs-lookup"><span data-stu-id="0d66d-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0d66d-139">**Win32 \_ TSLogonSetting**</span><span class="sxs-lookup"><span data-stu-id="0d66d-139">**Win32\_TSLogonSetting**</span></span>](win32-tslogonsetting.md)
</dt> </dl>

 

