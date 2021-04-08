---
title: Win32_TSGatewayServerSettings 類別的 SetAuthenticationPluginAndRecycleRpcApplicationPools 方法
description: 設定遠端桌面閘道 (RD 閘道) server 的目前驗證外掛程式，並在 IIS 中回收 RPC 應用程式集區。
ms.assetid: cdceaf50-3d0a-4af0-9ad5-fb43760fcf7b
ms.tgt_platform: multiple
keywords:
- SetAuthenticationPluginAndRecycleRpcApplicationPools 方法遠端桌面服務
- SetAuthenticationPluginAndRecycleRpcApplicationPools 方法遠端桌面服務，Win32_TSGatewayServerSettings 類別
- Win32_TSGatewayServerSettings 類別遠端桌面服務，SetAuthenticationPluginAndRecycleRpcApplicationPools 方法
topic_type:
- apiref
api_name:
- Win32_TSGatewayServerSettings.SetAuthenticationPluginAndRecycleRpcApplicationPools
api_location:
- AagWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b234e04c349d20ea178de12f050190b30193d444
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103685712"
---
# <a name="setauthenticationpluginandrecyclerpcapplicationpools-method-of-the-win32_tsgatewayserversettings-class"></a><span data-ttu-id="4a5eb-106">Win32 TSGatewayServerSettings 類別的 SetAuthenticationPluginAndRecycleRpcApplicationPools 方法 \_</span><span class="sxs-lookup"><span data-stu-id="4a5eb-106">SetAuthenticationPluginAndRecycleRpcApplicationPools method of the Win32\_TSGatewayServerSettings class</span></span>

<span data-ttu-id="4a5eb-107">設定遠端桌面閘道 (RD 閘道) server 的目前驗證外掛程式，並在 IIS 中回收 RPC 應用程式集區。</span><span class="sxs-lookup"><span data-stu-id="4a5eb-107">Sets the current authentication plug-in for the Remote Desktop Gateway (RD Gateway) server and recycles the RPC application pools in IIS.</span></span>

<span data-ttu-id="4a5eb-108">這個方法相當於依序呼叫 [**SetAuthenticationPlugin**](setauthenticationplugin-win32-tsgatewayserversettings.md) 和 [**RecycleRpcApplicationPools**](recyclerpcapplicationpools-win32-tsgatewayserversettings.md) 方法。</span><span class="sxs-lookup"><span data-stu-id="4a5eb-108">This method is equivalent to calling the [**SetAuthenticationPlugin**](setauthenticationplugin-win32-tsgatewayserversettings.md) and [**RecycleRpcApplicationPools**](recyclerpcapplicationpools-win32-tsgatewayserversettings.md) methods in sequence.</span></span>

## <a name="syntax"></a><span data-ttu-id="4a5eb-109">語法</span><span class="sxs-lookup"><span data-stu-id="4a5eb-109">Syntax</span></span>


```mof
uint32 SetAuthenticationPluginAndRecycleRpcApplicationPools(
  [in] string PluginName
);
```



## <a name="parameters"></a><span data-ttu-id="4a5eb-110">參數</span><span class="sxs-lookup"><span data-stu-id="4a5eb-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4a5eb-111">*PluginName* \[在\]</span><span class="sxs-lookup"><span data-stu-id="4a5eb-111">*PluginName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4a5eb-112">類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="4a5eb-112">Type: **string**</span></span>

<span data-ttu-id="4a5eb-113">驗證外掛程式的名稱</span><span class="sxs-lookup"><span data-stu-id="4a5eb-113">Name of the authentication plug-in</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4a5eb-114">傳回值</span><span class="sxs-lookup"><span data-stu-id="4a5eb-114">Return value</span></span>

<span data-ttu-id="4a5eb-115">類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="4a5eb-115">Type: **uint32**</span></span>

<span data-ttu-id="4a5eb-116">如果方法成功，則會傳回零。</span><span class="sxs-lookup"><span data-stu-id="4a5eb-116">If the method succeeds, it returns zero.</span></span> <span data-ttu-id="4a5eb-117">如果方法失敗，則會傳回非零值。</span><span class="sxs-lookup"><span data-stu-id="4a5eb-117">If the method is unsuccessful, it returns a nonzero value.</span></span> <span data-ttu-id="4a5eb-118">如需錯誤碼清單，請參閱 [遠端桌面服務 WMI 提供者錯誤碼](terminal-services-wmi-provider-error-codes.md)。</span><span class="sxs-lookup"><span data-stu-id="4a5eb-118">For a list of error codes, see [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="4a5eb-119">備註</span><span class="sxs-lookup"><span data-stu-id="4a5eb-119">Remarks</span></span>

<span data-ttu-id="4a5eb-120">呼叫這個方法會導致所有現有的連接中斷。</span><span class="sxs-lookup"><span data-stu-id="4a5eb-120">Calling this method results in all existing connections being disconnected.</span></span>

<span data-ttu-id="4a5eb-121">您必須是 Administrators 群組的成員，才能呼叫這個方法。</span><span class="sxs-lookup"><span data-stu-id="4a5eb-121">You must be a member of the Administrators group to call this method.</span></span>

<span data-ttu-id="4a5eb-122">受控物件格式 (MOF) 檔包含 Windows Management Instrumentation (WMI) 類別的定義。</span><span class="sxs-lookup"><span data-stu-id="4a5eb-122">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="4a5eb-123">MOF 檔案不會安裝為 Microsoft Windows 軟體開發套件 (SDK) 的一部分。</span><span class="sxs-lookup"><span data-stu-id="4a5eb-123">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="4a5eb-124">當您使用伺服器管理員新增相關聯的角色時，它們會安裝在伺服器上。</span><span class="sxs-lookup"><span data-stu-id="4a5eb-124">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="4a5eb-125">如需 MOF 檔案的詳細資訊，請參閱 [受控物件格式 (mof) ](/windows/desktop/WmiSdk/managed-object-format--mof-)。</span><span class="sxs-lookup"><span data-stu-id="4a5eb-125">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="4a5eb-126">規格需求</span><span class="sxs-lookup"><span data-stu-id="4a5eb-126">Requirements</span></span>



| <span data-ttu-id="4a5eb-127">需求</span><span class="sxs-lookup"><span data-stu-id="4a5eb-127">Requirement</span></span> | <span data-ttu-id="4a5eb-128">值</span><span class="sxs-lookup"><span data-stu-id="4a5eb-128">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="4a5eb-129">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="4a5eb-129">Minimum supported client</span></span><br/> | <span data-ttu-id="4a5eb-130">都不支援</span><span class="sxs-lookup"><span data-stu-id="4a5eb-130">None supported</span></span><br/>                                                                |
| <span data-ttu-id="4a5eb-131">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="4a5eb-131">Minimum supported server</span></span><br/> | <span data-ttu-id="4a5eb-132">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="4a5eb-132">Windows Server 2008 R2</span></span><br/>                                                        |
| <span data-ttu-id="4a5eb-133">命名空間</span><span class="sxs-lookup"><span data-stu-id="4a5eb-133">Namespace</span></span><br/>                | <span data-ttu-id="4a5eb-134">根 \\ CIMv2 \\ microsoft-windows-terminalservices-gateway</span><span class="sxs-lookup"><span data-stu-id="4a5eb-134">Root\\CIMv2\\TerminalServices</span></span><br/>                                                 |
| <span data-ttu-id="4a5eb-135">MOF</span><span class="sxs-lookup"><span data-stu-id="4a5eb-135">MOF</span></span><br/>                      | <dl> <span data-ttu-id="4a5eb-136"><dt>TSGateway mof</dt></span><span class="sxs-lookup"><span data-stu-id="4a5eb-136"><dt>TSGateway.mof</dt></span></span> </dl> |
| <span data-ttu-id="4a5eb-137">DLL</span><span class="sxs-lookup"><span data-stu-id="4a5eb-137">DLL</span></span><br/>                      | <dl> <span data-ttu-id="4a5eb-138"><dt>AagWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="4a5eb-138"><dt>AagWmi.dll</dt></span></span> </dl>    |



## <a name="see-also"></a><span data-ttu-id="4a5eb-139">另請參閱</span><span class="sxs-lookup"><span data-stu-id="4a5eb-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4a5eb-140">**Win32 \_ TSGatewayServerSettings**</span><span class="sxs-lookup"><span data-stu-id="4a5eb-140">**Win32\_TSGatewayServerSettings**</span></span>](win32-tsgatewayserversettings.md)
</dt> <dt>

[<span data-ttu-id="4a5eb-141">**SetAuthenticationPlugin**</span><span class="sxs-lookup"><span data-stu-id="4a5eb-141">**SetAuthenticationPlugin**</span></span>](setauthenticationplugin-win32-tsgatewayserversettings.md)
</dt> <dt>

[<span data-ttu-id="4a5eb-142">**RecycleRpcApplicationPools**</span><span class="sxs-lookup"><span data-stu-id="4a5eb-142">**RecycleRpcApplicationPools**</span></span>](recyclerpcapplicationpools-win32-tsgatewayserversettings.md)
</dt> </dl>

 

