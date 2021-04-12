---
title: Win32_TSGatewayServerSettings 類別的 SetCertificate 方法
description: 在 IIS 中設定埠443的 HTTPS 系結憑證雜湊。
ms.assetid: b5f794bc-17b1-401a-92d8-c9bbe5d0d05f
ms.tgt_platform: multiple
keywords:
- SetCertificate 方法遠端桌面服務
- SetCertificate 方法遠端桌面服務，Win32_TSGatewayServerSettings 類別
- Win32_TSGatewayServerSettings 類別遠端桌面服務，SetCertificate 方法
topic_type:
- apiref
api_name:
- Win32_TSGatewayServerSettings.SetCertificate
api_location:
- AagWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9b1da7e3abcca671b0c8bf70461c77d56e68cf68
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104105846"
---
# <a name="setcertificate-method-of-the-win32_tsgatewayserversettings-class"></a><span data-ttu-id="0f962-106">Win32 TSGatewayServerSettings 類別的 SetCertificate 方法 \_</span><span class="sxs-lookup"><span data-stu-id="0f962-106">SetCertificate method of the Win32\_TSGatewayServerSettings class</span></span>

<span data-ttu-id="0f962-107">在 IIS 中設定埠443的 HTTPS 系結憑證雜湊。</span><span class="sxs-lookup"><span data-stu-id="0f962-107">Sets the certificate hash for HTTPS binding on port 443 in IIS.</span></span>

## <a name="syntax"></a><span data-ttu-id="0f962-108">語法</span><span class="sxs-lookup"><span data-stu-id="0f962-108">Syntax</span></span>


```mof
uint32 SetCertificate(
  [in] uint8 CertHash[]
);
```



## <a name="parameters"></a><span data-ttu-id="0f962-109">參數</span><span class="sxs-lookup"><span data-stu-id="0f962-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0f962-110">*CertHash* \[在\]</span><span class="sxs-lookup"><span data-stu-id="0f962-110">*CertHash* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0f962-111">類型： **uint8 \[ \]**</span><span class="sxs-lookup"><span data-stu-id="0f962-111">Type: **uint8\[\]**</span></span>

<span data-ttu-id="0f962-112">新的憑證雜湊。</span><span class="sxs-lookup"><span data-stu-id="0f962-112">The new certificate hash.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0f962-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="0f962-113">Return value</span></span>

<span data-ttu-id="0f962-114">類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="0f962-114">Type: **uint32**</span></span>

<span data-ttu-id="0f962-115">如果方法成功，則會傳回零。</span><span class="sxs-lookup"><span data-stu-id="0f962-115">If the method succeeds, it returns zero.</span></span> <span data-ttu-id="0f962-116">如果方法失敗，則會傳回非零值。</span><span class="sxs-lookup"><span data-stu-id="0f962-116">If the method is unsuccessful, it returns a nonzero value.</span></span> <span data-ttu-id="0f962-117">如需錯誤碼清單，請參閱 [遠端桌面服務 WMI 提供者錯誤碼](terminal-services-wmi-provider-error-codes.md)。</span><span class="sxs-lookup"><span data-stu-id="0f962-117">For a list of error codes, see [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="0f962-118">備註</span><span class="sxs-lookup"><span data-stu-id="0f962-118">Remarks</span></span>

<span data-ttu-id="0f962-119">使用這個方法設定憑證雜湊之後，您必須呼叫 [**Configure**](configure-win32-tsgatewayserversettings.md) 方法來完成設定程式。</span><span class="sxs-lookup"><span data-stu-id="0f962-119">After the certificate hash has been set with this method, you must call the [**Configure**](configure-win32-tsgatewayserversettings.md) method to complete the configuration process.</span></span>

<span data-ttu-id="0f962-120">您必須是 Administrators 群組的成員，才能呼叫這個方法。</span><span class="sxs-lookup"><span data-stu-id="0f962-120">You must be a member of the Administrators group to call this method.</span></span>

<span data-ttu-id="0f962-121">受控物件格式 (MOF) 檔包含 Windows Management Instrumentation (WMI) 類別的定義。</span><span class="sxs-lookup"><span data-stu-id="0f962-121">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="0f962-122">MOF 檔案不會安裝為 Microsoft Windows 軟體開發套件 (SDK) 的一部分。</span><span class="sxs-lookup"><span data-stu-id="0f962-122">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="0f962-123">當您使用伺服器管理員新增相關聯的角色時，它們會安裝在伺服器上。</span><span class="sxs-lookup"><span data-stu-id="0f962-123">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="0f962-124">如需 MOF 檔案的詳細資訊，請參閱 [受控物件格式 (mof) ](/windows/desktop/WmiSdk/managed-object-format--mof-)。</span><span class="sxs-lookup"><span data-stu-id="0f962-124">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="0f962-125">規格需求</span><span class="sxs-lookup"><span data-stu-id="0f962-125">Requirements</span></span>



| <span data-ttu-id="0f962-126">需求</span><span class="sxs-lookup"><span data-stu-id="0f962-126">Requirement</span></span> | <span data-ttu-id="0f962-127">值</span><span class="sxs-lookup"><span data-stu-id="0f962-127">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="0f962-128">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="0f962-128">Minimum supported client</span></span><br/> | <span data-ttu-id="0f962-129">都不支援</span><span class="sxs-lookup"><span data-stu-id="0f962-129">None supported</span></span><br/>                                                                |
| <span data-ttu-id="0f962-130">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="0f962-130">Minimum supported server</span></span><br/> | <span data-ttu-id="0f962-131">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="0f962-131">Windows Server 2008 R2</span></span><br/>                                                        |
| <span data-ttu-id="0f962-132">命名空間</span><span class="sxs-lookup"><span data-stu-id="0f962-132">Namespace</span></span><br/>                | <span data-ttu-id="0f962-133">根 \\ CIMv2 \\ microsoft-windows-terminalservices-gateway</span><span class="sxs-lookup"><span data-stu-id="0f962-133">Root\\CIMv2\\TerminalServices</span></span><br/>                                                 |
| <span data-ttu-id="0f962-134">MOF</span><span class="sxs-lookup"><span data-stu-id="0f962-134">MOF</span></span><br/>                      | <dl> <span data-ttu-id="0f962-135"><dt>TSGateway mof</dt></span><span class="sxs-lookup"><span data-stu-id="0f962-135"><dt>TSGateway.mof</dt></span></span> </dl> |
| <span data-ttu-id="0f962-136">DLL</span><span class="sxs-lookup"><span data-stu-id="0f962-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="0f962-137"><dt>AagWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0f962-137"><dt>AagWmi.dll</dt></span></span> </dl>    |



## <a name="see-also"></a><span data-ttu-id="0f962-138">另請參閱</span><span class="sxs-lookup"><span data-stu-id="0f962-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0f962-139">**Win32 \_ TSGatewayServerSettings**</span><span class="sxs-lookup"><span data-stu-id="0f962-139">**Win32\_TSGatewayServerSettings**</span></span>](win32-tsgatewayserversettings.md)
</dt> </dl>

 

