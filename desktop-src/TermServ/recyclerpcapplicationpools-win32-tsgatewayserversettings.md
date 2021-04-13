---
title: Win32_TSGatewayServerSettings 類別的 RecycleRpcApplicationPools 方法
description: 回收 IIS 中的 RPC 應用程式集區。
ms.assetid: c7b1b797-7792-4d97-97f4-bea3b2f2495b
ms.tgt_platform: multiple
keywords:
- RecycleRpcApplicationPools 方法遠端桌面服務
- RecycleRpcApplicationPools 方法遠端桌面服務，Win32_TSGatewayServerSettings 類別
- Win32_TSGatewayServerSettings 類別遠端桌面服務，RecycleRpcApplicationPools 方法
topic_type:
- apiref
api_name:
- Win32_TSGatewayServerSettings.RecycleRpcApplicationPools
api_location:
- AagWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e1963b8dec826c72a8a5128abdfa01d4a1e841a6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104465113"
---
# <a name="recyclerpcapplicationpools-method-of-the-win32_tsgatewayserversettings-class"></a><span data-ttu-id="1352c-106">Win32 TSGatewayServerSettings 類別的 RecycleRpcApplicationPools 方法 \_</span><span class="sxs-lookup"><span data-stu-id="1352c-106">RecycleRpcApplicationPools method of the Win32\_TSGatewayServerSettings class</span></span>

<span data-ttu-id="1352c-107">回收 IIS 中的 RPC 應用程式集區。</span><span class="sxs-lookup"><span data-stu-id="1352c-107">Recycles the RPC application pools in IIS.</span></span>

## <a name="syntax"></a><span data-ttu-id="1352c-108">語法</span><span class="sxs-lookup"><span data-stu-id="1352c-108">Syntax</span></span>


```mof
uint32 RecycleRpcApplicationPools();
```



## <a name="parameters"></a><span data-ttu-id="1352c-109">參數</span><span class="sxs-lookup"><span data-stu-id="1352c-109">Parameters</span></span>

<span data-ttu-id="1352c-110">這個方法沒有任何參數。</span><span class="sxs-lookup"><span data-stu-id="1352c-110">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="1352c-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="1352c-111">Return value</span></span>

<span data-ttu-id="1352c-112">類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="1352c-112">Type: **uint32**</span></span>

<span data-ttu-id="1352c-113">如果方法成功，則會傳回零。</span><span class="sxs-lookup"><span data-stu-id="1352c-113">If the method succeeds, it returns zero.</span></span> <span data-ttu-id="1352c-114">如果方法失敗，則會傳回非零值。</span><span class="sxs-lookup"><span data-stu-id="1352c-114">If the method is unsuccessful, it returns a nonzero value.</span></span> <span data-ttu-id="1352c-115">如需錯誤碼清單，請參閱 [遠端桌面服務 WMI 提供者錯誤碼](terminal-services-wmi-provider-error-codes.md)。</span><span class="sxs-lookup"><span data-stu-id="1352c-115">For a list of error codes, see [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="1352c-116">備註</span><span class="sxs-lookup"><span data-stu-id="1352c-116">Remarks</span></span>

<span data-ttu-id="1352c-117">呼叫這個方法會導致所有現有的連接中斷。</span><span class="sxs-lookup"><span data-stu-id="1352c-117">Calling this method results in all existing connections being disconnected.</span></span>

<span data-ttu-id="1352c-118">您必須是 Administrators 群組的成員，才能呼叫這個方法。</span><span class="sxs-lookup"><span data-stu-id="1352c-118">You must be a member of the Administrators group to call this method.</span></span>

<span data-ttu-id="1352c-119">受控物件格式 (MOF) 檔包含 Windows Management Instrumentation (WMI) 類別的定義。</span><span class="sxs-lookup"><span data-stu-id="1352c-119">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="1352c-120">MOF 檔案不會安裝為 Microsoft Windows 軟體開發套件 (SDK) 的一部分。</span><span class="sxs-lookup"><span data-stu-id="1352c-120">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="1352c-121">當您使用伺服器管理員新增相關聯的角色時，它們會安裝在伺服器上。</span><span class="sxs-lookup"><span data-stu-id="1352c-121">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="1352c-122">如需 MOF 檔案的詳細資訊，請參閱 [受控物件格式 (mof) ](/windows/desktop/WmiSdk/managed-object-format--mof-)。</span><span class="sxs-lookup"><span data-stu-id="1352c-122">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="1352c-123">規格需求</span><span class="sxs-lookup"><span data-stu-id="1352c-123">Requirements</span></span>



| <span data-ttu-id="1352c-124">需求</span><span class="sxs-lookup"><span data-stu-id="1352c-124">Requirement</span></span> | <span data-ttu-id="1352c-125">值</span><span class="sxs-lookup"><span data-stu-id="1352c-125">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="1352c-126">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="1352c-126">Minimum supported client</span></span><br/> | <span data-ttu-id="1352c-127">都不支援</span><span class="sxs-lookup"><span data-stu-id="1352c-127">None supported</span></span><br/>                                                                |
| <span data-ttu-id="1352c-128">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="1352c-128">Minimum supported server</span></span><br/> | <span data-ttu-id="1352c-129">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="1352c-129">Windows Server 2008 R2</span></span><br/>                                                        |
| <span data-ttu-id="1352c-130">命名空間</span><span class="sxs-lookup"><span data-stu-id="1352c-130">Namespace</span></span><br/>                | <span data-ttu-id="1352c-131">根 \\ CIMv2 \\ microsoft-windows-terminalservices-gateway</span><span class="sxs-lookup"><span data-stu-id="1352c-131">Root\\CIMv2\\TerminalServices</span></span><br/>                                                 |
| <span data-ttu-id="1352c-132">MOF</span><span class="sxs-lookup"><span data-stu-id="1352c-132">MOF</span></span><br/>                      | <dl> <span data-ttu-id="1352c-133"><dt>TSGateway mof</dt></span><span class="sxs-lookup"><span data-stu-id="1352c-133"><dt>TSGateway.mof</dt></span></span> </dl> |
| <span data-ttu-id="1352c-134">DLL</span><span class="sxs-lookup"><span data-stu-id="1352c-134">DLL</span></span><br/>                      | <dl> <span data-ttu-id="1352c-135"><dt>AagWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="1352c-135"><dt>AagWmi.dll</dt></span></span> </dl>    |



## <a name="see-also"></a><span data-ttu-id="1352c-136">另請參閱</span><span class="sxs-lookup"><span data-stu-id="1352c-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1352c-137">**Win32 \_ TSGatewayServerSettings**</span><span class="sxs-lookup"><span data-stu-id="1352c-137">**Win32\_TSGatewayServerSettings**</span></span>](win32-tsgatewayserversettings.md)
</dt> <dt>

[<span data-ttu-id="1352c-138">**SetAuthenticationPlugin**</span><span class="sxs-lookup"><span data-stu-id="1352c-138">**SetAuthenticationPlugin**</span></span>](setauthenticationplugin-win32-tsgatewayserversettings.md)
</dt> </dl>

 

