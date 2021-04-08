---
title: Win32_TSGatewayConnectionAuthorizationPolicy 類別的 EnableAllowOnlySDRServers 方法
description: 用來切換 AllowOnlySDRServers 屬性。
ms.assetid: ec7f22bc-4e80-4ece-9567-5f405207480e
ms.tgt_platform: multiple
keywords:
- EnableAllowOnlySDRServers 方法遠端桌面服務
- EnableAllowOnlySDRServers 方法遠端桌面服務，Win32_TSGatewayConnectionAuthorizationPolicy 類別
- Win32_TSGatewayConnectionAuthorizationPolicy 類別遠端桌面服務，EnableAllowOnlySDRServers 方法
topic_type:
- apiref
api_name:
- Win32_TSGatewayConnectionAuthorizationPolicy.EnableAllowOnlySDRServers
api_location:
- AagWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f031cff46e0fafdce80a995d2d4778875c1d56f7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103685846"
---
# <a name="enableallowonlysdrservers-method-of-the-win32_tsgatewayconnectionauthorizationpolicy-class"></a><span data-ttu-id="5554c-106">Win32 TSGatewayConnectionAuthorizationPolicy 類別的 EnableAllowOnlySDRServers 方法 \_</span><span class="sxs-lookup"><span data-stu-id="5554c-106">EnableAllowOnlySDRServers method of the Win32\_TSGatewayConnectionAuthorizationPolicy class</span></span>

<span data-ttu-id="5554c-107">用來切換 **AllowOnlySDRServers** 屬性。</span><span class="sxs-lookup"><span data-stu-id="5554c-107">Used to toggle the **AllowOnlySDRServers** property.</span></span>

## <a name="syntax"></a><span data-ttu-id="5554c-108">語法</span><span class="sxs-lookup"><span data-stu-id="5554c-108">Syntax</span></span>


```mof
uint32 EnableAllowOnlySDRServers(
  [in] boolean AllowOnlySDRServers
);
```



## <a name="parameters"></a><span data-ttu-id="5554c-109">參數</span><span class="sxs-lookup"><span data-stu-id="5554c-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5554c-110">*AllowOnlySDRServers* \[在\]</span><span class="sxs-lookup"><span data-stu-id="5554c-110">*AllowOnlySDRServers* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5554c-111">如果設定為 **True**，則只允許連線 (SDR) RDS 伺服器來保護裝置重新導向。</span><span class="sxs-lookup"><span data-stu-id="5554c-111">If set to **True**, connections will be allowed only to secure device redirection (SDR) RDS servers.</span></span> <span data-ttu-id="5554c-112">如果設定為 **False**，則也會允許舊版 RDS 伺服器的連接</span><span class="sxs-lookup"><span data-stu-id="5554c-112">If set to **False**, connections will be allowed to older RDS servers also</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5554c-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="5554c-113">Return value</span></span>

<span data-ttu-id="5554c-114">如果方法成功，則會傳回零。</span><span class="sxs-lookup"><span data-stu-id="5554c-114">If the method succeeds, it returns zero.</span></span> <span data-ttu-id="5554c-115">如果方法失敗，則會傳回非零值。</span><span class="sxs-lookup"><span data-stu-id="5554c-115">If the method is unsuccessful, it returns a nonzero value.</span></span> <span data-ttu-id="5554c-116">如需錯誤碼清單，請參閱 [遠端桌面服務 WMI 提供者錯誤碼](terminal-services-wmi-provider-error-codes.md)。</span><span class="sxs-lookup"><span data-stu-id="5554c-116">For a list of error codes, see [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="5554c-117">規格需求</span><span class="sxs-lookup"><span data-stu-id="5554c-117">Requirements</span></span>



| <span data-ttu-id="5554c-118">需求</span><span class="sxs-lookup"><span data-stu-id="5554c-118">Requirement</span></span> | <span data-ttu-id="5554c-119">值</span><span class="sxs-lookup"><span data-stu-id="5554c-119">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="5554c-120">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="5554c-120">Minimum supported client</span></span><br/> | <span data-ttu-id="5554c-121">都不支援</span><span class="sxs-lookup"><span data-stu-id="5554c-121">None supported</span></span><br/>                                                                |
| <span data-ttu-id="5554c-122">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="5554c-122">Minimum supported server</span></span><br/> | <span data-ttu-id="5554c-123">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="5554c-123">Windows Server 2008 R2</span></span><br/>                                                        |
| <span data-ttu-id="5554c-124">命名空間</span><span class="sxs-lookup"><span data-stu-id="5554c-124">Namespace</span></span><br/>                | <span data-ttu-id="5554c-125">根 \\ cimv2 \\ microsoft-windows-terminalservices-gateway</span><span class="sxs-lookup"><span data-stu-id="5554c-125">ROOT\\cimv2\\TerminalServices</span></span><br/>                                                 |
| <span data-ttu-id="5554c-126">MOF</span><span class="sxs-lookup"><span data-stu-id="5554c-126">MOF</span></span><br/>                      | <dl> <span data-ttu-id="5554c-127"><dt>TsGateway mof</dt></span><span class="sxs-lookup"><span data-stu-id="5554c-127"><dt>TsGateway.mof</dt></span></span> </dl> |
| <span data-ttu-id="5554c-128">DLL</span><span class="sxs-lookup"><span data-stu-id="5554c-128">DLL</span></span><br/>                      | <dl> <span data-ttu-id="5554c-129"><dt>AagWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5554c-129"><dt>AagWmi.dll</dt></span></span> </dl>    |



## <a name="see-also"></a><span data-ttu-id="5554c-130">另請參閱</span><span class="sxs-lookup"><span data-stu-id="5554c-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5554c-131">**Win32 \_ TSGatewayConnectionAuthorizationPolicy**</span><span class="sxs-lookup"><span data-stu-id="5554c-131">**Win32\_TSGatewayConnectionAuthorizationPolicy**</span></span>](win32-tsgatewayconnectionauthorizationpolicy.md)
</dt> </dl>

 

 





