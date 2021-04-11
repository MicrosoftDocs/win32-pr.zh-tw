---
title: Win32_TSGeneralSetting 類別的 SetUserAuthenticationRequired 方法
description: 藉由設定 UserAuthenticationRequired 屬性的值，啟用或停用使用者必須在連接時驗證的要求。
ms.assetid: a0581326-fecc-4d23-87bf-3696c93366e8
ms.tgt_platform: multiple
keywords:
- SetUserAuthenticationRequired 方法遠端桌面服務
- SetUserAuthenticationRequired 方法遠端桌面服務，Win32_TSGeneralSetting 類別
- Win32_TSGeneralSetting 類別遠端桌面服務，SetUserAuthenticationRequired 方法
topic_type:
- apiref
api_name:
- Win32_TSGeneralSetting.SetUserAuthenticationRequired
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b39c0eb711d2146130ff0fd879953fc71fcba965
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104317428"
---
# <a name="setuserauthenticationrequired-method-of-the-win32_tsgeneralsetting-class"></a><span data-ttu-id="e2809-106">Win32 TSGeneralSetting 類別的 SetUserAuthenticationRequired 方法 \_</span><span class="sxs-lookup"><span data-stu-id="e2809-106">SetUserAuthenticationRequired method of the Win32\_TSGeneralSetting class</span></span>

<span data-ttu-id="e2809-107">藉由設定 [**Win32 \_ TSGeneralSetting**](win32-tsgeneralsetting.md)類別中 **UserAuthenticationRequired** 屬性的值，啟用或停用使用者必須在連接時驗證的要求。</span><span class="sxs-lookup"><span data-stu-id="e2809-107">Enables or disables the requirement that users must be authenticated at connection time by setting the value of the **UserAuthenticationRequired** property in the [**Win32\_TSGeneralSetting**](win32-tsgeneralsetting.md) class.</span></span> <span data-ttu-id="e2809-108">若 **為 True**，表示已啟用， **UserAuthenticationRequired** 需要在連接時進行使用者驗證，以增加伺服器保護以防止網路攻擊。</span><span class="sxs-lookup"><span data-stu-id="e2809-108">If **True**, which means enabled, **UserAuthenticationRequired** requires user authentication at connection time to increase server protection against network attacks.</span></span> <span data-ttu-id="e2809-109">只有支援 RDP 6.0 版或更高版本的遠端桌面通訊協定 (RDP) 用戶端才能連接。</span><span class="sxs-lookup"><span data-stu-id="e2809-109">Only Remote Desktop Protocol (RDP) clients that support RDP version 6.0 or higher are able to connect.</span></span> <span data-ttu-id="e2809-110">為了避免遠端使用者中斷，建議您在啟用屬性之前，先部署支援適當通訊協定版本的 RDP 用戶端。</span><span class="sxs-lookup"><span data-stu-id="e2809-110">To avoid disruptions for remote users, it is recommended that you deploy RDP clients supporting the appropriate protocol version before you enable the property.</span></span>

## <a name="syntax"></a><span data-ttu-id="e2809-111">語法</span><span class="sxs-lookup"><span data-stu-id="e2809-111">Syntax</span></span>


```mof
uint32 SetUserAuthenticationRequired(
  [in] uint32 UserAuthenticationRequired
);
```



## <a name="parameters"></a><span data-ttu-id="e2809-112">參數</span><span class="sxs-lookup"><span data-stu-id="e2809-112">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e2809-113">*UserAuthenticationRequired* \[在\]</span><span class="sxs-lookup"><span data-stu-id="e2809-113">*UserAuthenticationRequired* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e2809-114">指出是否需要使用者驗證。</span><span class="sxs-lookup"><span data-stu-id="e2809-114">Indicates whether user authentication is required.</span></span>

<dt>

<span data-ttu-id="e2809-115">0 (0x0) </span><span class="sxs-lookup"><span data-stu-id="e2809-115">0 (0x0)</span></span>
</dt> <dd>

<span data-ttu-id="e2809-116">停用使用者必須經過驗證的需求</span><span class="sxs-lookup"><span data-stu-id="e2809-116">Disable requirement that user must be authenticated</span></span>

</dd> <dt>

<span data-ttu-id="e2809-117">1 (0x1) </span><span class="sxs-lookup"><span data-stu-id="e2809-117">1 (0x1)</span></span>
</dt> <dd>

<span data-ttu-id="e2809-118">啟用使用者必須經過驗證的需求。</span><span class="sxs-lookup"><span data-stu-id="e2809-118">Enables requirement that user must be authenticated.</span></span>

</dd> </dl> </dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e2809-119">傳回值</span><span class="sxs-lookup"><span data-stu-id="e2809-119">Return value</span></span>

<span data-ttu-id="e2809-120">成功時傳回0，否則會傳回 WMI 錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="e2809-120">Returns 0 on success, otherwise returns a WMI error code.</span></span> <span data-ttu-id="e2809-121">如需這些值的清單，請參閱 [遠端桌面服務 WMI 提供者錯誤碼](terminal-services-wmi-provider-error-codes.md) 。</span><span class="sxs-lookup"><span data-stu-id="e2809-121">Refer to [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md) for a list of these values.</span></span>

## <a name="remarks"></a><span data-ttu-id="e2809-122">備註</span><span class="sxs-lookup"><span data-stu-id="e2809-122">Remarks</span></span>

<span data-ttu-id="e2809-123">受控物件格式 (MOF) 檔包含 Windows Management Instrumentation (WMI) 類別的定義。</span><span class="sxs-lookup"><span data-stu-id="e2809-123">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="e2809-124">MOF 檔案不會安裝為 Microsoft Windows 軟體開發套件 (SDK) 的一部分。</span><span class="sxs-lookup"><span data-stu-id="e2809-124">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="e2809-125">當您使用伺服器管理員新增相關聯的角色時，它們會安裝在伺服器上。</span><span class="sxs-lookup"><span data-stu-id="e2809-125">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="e2809-126">如需 MOF 檔案的詳細資訊，請參閱 [受控物件格式 (mof) ](/windows/desktop/WmiSdk/managed-object-format--mof-)。</span><span class="sxs-lookup"><span data-stu-id="e2809-126">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="e2809-127">規格需求</span><span class="sxs-lookup"><span data-stu-id="e2809-127">Requirements</span></span>



| <span data-ttu-id="e2809-128">需求</span><span class="sxs-lookup"><span data-stu-id="e2809-128">Requirement</span></span> | <span data-ttu-id="e2809-129">值</span><span class="sxs-lookup"><span data-stu-id="e2809-129">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="e2809-130">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="e2809-130">Minimum supported client</span></span><br/> | <span data-ttu-id="e2809-131">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="e2809-131">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="e2809-132">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="e2809-132">Minimum supported server</span></span><br/> | <span data-ttu-id="e2809-133">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="e2809-133">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="e2809-134">命名空間</span><span class="sxs-lookup"><span data-stu-id="e2809-134">Namespace</span></span><br/>                | <span data-ttu-id="e2809-135">根 \\ CIMv2 \\ microsoft-windows-terminalservices-gateway</span><span class="sxs-lookup"><span data-stu-id="e2809-135">Root\\CIMv2\\TerminalServices</span></span><br/>                                                |
| <span data-ttu-id="e2809-136">MOF</span><span class="sxs-lookup"><span data-stu-id="e2809-136">MOF</span></span><br/>                      | <dl> <span data-ttu-id="e2809-137"><dt>TSCfgWmi mof</dt></span><span class="sxs-lookup"><span data-stu-id="e2809-137"><dt>TSCfgWmi.mof</dt></span></span> </dl> |
| <span data-ttu-id="e2809-138">DLL</span><span class="sxs-lookup"><span data-stu-id="e2809-138">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e2809-139"><dt>TSCfgWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e2809-139"><dt>TSCfgWmi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e2809-140">另請參閱</span><span class="sxs-lookup"><span data-stu-id="e2809-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e2809-141">**Win32 \_ TSGeneralSetting**</span><span class="sxs-lookup"><span data-stu-id="e2809-141">**Win32\_TSGeneralSetting**</span></span>](win32-tsgeneralsetting.md)
</dt> </dl>

 

