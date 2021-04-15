---
title: Win32_TSGatewayConnectionAuthorizationPolicy 類別的 SetEnabled 方法
description: 設定啟用的屬性，可啟用或停用目前的遠端桌面服務連線授權原則 (RD \ 160;端點) 。
ms.assetid: f8c0b39e-95d4-46cf-83fb-e91b650fbb4d
ms.tgt_platform: multiple
keywords:
- SetEnabled 方法遠端桌面服務
- SetEnabled 方法遠端桌面服務，Win32_TSGatewayConnectionAuthorizationPolicy 類別
- Win32_TSGatewayConnectionAuthorizationPolicy 類別遠端桌面服務，SetEnabled 方法
topic_type:
- apiref
api_name:
- Win32_TSGatewayConnectionAuthorizationPolicy.SetEnabled
api_location:
- AagWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6584e8916db2f8070def3904d0ece6ec0ee5ae34
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104508516"
---
# <a name="setenabled-method-of-the-win32_tsgatewayconnectionauthorizationpolicy-class"></a><span data-ttu-id="52ebc-106">Win32 TSGatewayConnectionAuthorizationPolicy 類別的 SetEnabled 方法 \_</span><span class="sxs-lookup"><span data-stu-id="52ebc-106">SetEnabled method of the Win32\_TSGatewayConnectionAuthorizationPolicy class</span></span>

<span data-ttu-id="52ebc-107">設定 **Enabled** 屬性，以啟用或停用目前遠端桌面服務連接授權原則 (RD CAP) 。</span><span class="sxs-lookup"><span data-stu-id="52ebc-107">Sets the **Enabled** property, which enables or disables the current Remote Desktop Services connection authorization policy (RD CAP).</span></span>

## <a name="syntax"></a><span data-ttu-id="52ebc-108">語法</span><span class="sxs-lookup"><span data-stu-id="52ebc-108">Syntax</span></span>


```mof
uint32 SetEnabled(
  [in] boolean Enabled
);
```



## <a name="parameters"></a><span data-ttu-id="52ebc-109">參數</span><span class="sxs-lookup"><span data-stu-id="52ebc-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="52ebc-110">*已啟用* \[在\]</span><span class="sxs-lookup"><span data-stu-id="52ebc-110">*Enabled* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="52ebc-111">如果要啟用 RD CAP，則為 **True** ，如果 RD CAP 要停用，則為 **False** 。</span><span class="sxs-lookup"><span data-stu-id="52ebc-111">**True** if the RD CAP is to be enabled, **False** if the RD CAP is to be disabled.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="52ebc-112">傳回值</span><span class="sxs-lookup"><span data-stu-id="52ebc-112">Return value</span></span>

<span data-ttu-id="52ebc-113">如果方法成功，則會傳回零。</span><span class="sxs-lookup"><span data-stu-id="52ebc-113">If the method succeeds, it returns zero.</span></span> <span data-ttu-id="52ebc-114">如果方法失敗，則會傳回非零值。</span><span class="sxs-lookup"><span data-stu-id="52ebc-114">If the method is unsuccessful, it returns a nonzero value.</span></span> <span data-ttu-id="52ebc-115">如需錯誤碼清單，請參閱 [遠端桌面服務 WMI 提供者錯誤碼](terminal-services-wmi-provider-error-codes.md)。</span><span class="sxs-lookup"><span data-stu-id="52ebc-115">For a list of error codes, see [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="52ebc-116">備註</span><span class="sxs-lookup"><span data-stu-id="52ebc-116">Remarks</span></span>

<span data-ttu-id="52ebc-117">您必須是 Administrators 群組的成員，才能呼叫這個方法。</span><span class="sxs-lookup"><span data-stu-id="52ebc-117">You must be a member of the Administrators group to call this method.</span></span>

<span data-ttu-id="52ebc-118">受控物件格式 (MOF) 檔包含 Windows Management Instrumentation (WMI) 類別的定義。</span><span class="sxs-lookup"><span data-stu-id="52ebc-118">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="52ebc-119">MOF 檔案不會安裝為 Microsoft Windows 軟體開發套件 (SDK) 的一部分。</span><span class="sxs-lookup"><span data-stu-id="52ebc-119">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="52ebc-120">當您使用伺服器管理員新增相關聯的角色時，它們會安裝在伺服器上。</span><span class="sxs-lookup"><span data-stu-id="52ebc-120">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="52ebc-121">如需 MOF 檔案的詳細資訊，請參閱 [受控物件格式 (mof) ](/windows/desktop/WmiSdk/managed-object-format--mof-)。</span><span class="sxs-lookup"><span data-stu-id="52ebc-121">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="52ebc-122">規格需求</span><span class="sxs-lookup"><span data-stu-id="52ebc-122">Requirements</span></span>



| <span data-ttu-id="52ebc-123">需求</span><span class="sxs-lookup"><span data-stu-id="52ebc-123">Requirement</span></span> | <span data-ttu-id="52ebc-124">值</span><span class="sxs-lookup"><span data-stu-id="52ebc-124">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="52ebc-125">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="52ebc-125">Minimum supported client</span></span><br/> | <span data-ttu-id="52ebc-126">都不支援</span><span class="sxs-lookup"><span data-stu-id="52ebc-126">None supported</span></span><br/>                                                                |
| <span data-ttu-id="52ebc-127">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="52ebc-127">Minimum supported server</span></span><br/> | <span data-ttu-id="52ebc-128">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="52ebc-128">Windows Server 2008</span></span><br/>                                                           |
| <span data-ttu-id="52ebc-129">命名空間</span><span class="sxs-lookup"><span data-stu-id="52ebc-129">Namespace</span></span><br/>                | <span data-ttu-id="52ebc-130">根 \\ CIMv2 \\ microsoft-windows-terminalservices-gateway</span><span class="sxs-lookup"><span data-stu-id="52ebc-130">Root\\CIMv2\\TerminalServices</span></span><br/>                                                 |
| <span data-ttu-id="52ebc-131">MOF</span><span class="sxs-lookup"><span data-stu-id="52ebc-131">MOF</span></span><br/>                      | <dl> <span data-ttu-id="52ebc-132"><dt>TSGateway mof</dt></span><span class="sxs-lookup"><span data-stu-id="52ebc-132"><dt>TSGateway.mof</dt></span></span> </dl> |
| <span data-ttu-id="52ebc-133">DLL</span><span class="sxs-lookup"><span data-stu-id="52ebc-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="52ebc-134"><dt>AagWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="52ebc-134"><dt>AagWmi.dll</dt></span></span> </dl>    |



## <a name="see-also"></a><span data-ttu-id="52ebc-135">另請參閱</span><span class="sxs-lookup"><span data-stu-id="52ebc-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="52ebc-136">**Win32 \_ TSGatewayConnectionAuthorizationPolicy**</span><span class="sxs-lookup"><span data-stu-id="52ebc-136">**Win32\_TSGatewayConnectionAuthorizationPolicy**</span></span>](win32-tsgatewayconnectionauthorizationpolicy.md)
</dt> </dl>

 

