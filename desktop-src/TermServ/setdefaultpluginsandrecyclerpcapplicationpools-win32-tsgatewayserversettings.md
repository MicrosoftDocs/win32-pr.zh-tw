---
title: Win32_TSGatewayServerSettings 類別的 SetDefaultPluginsAndRecycleRpcApplicationPools 方法
description: 針對遠端桌面閘道 (RD 閘道) 伺服器設定目前的驗證和授權外掛程式，並在 IIS 中回收 RPC 應用程式集區。
ms.assetid: 1eac9e42-e533-4020-b2b6-571063f18c3c
ms.tgt_platform: multiple
keywords:
- SetDefaultPluginsAndRecycleRpcApplicationPools 方法遠端桌面服務
- SetDefaultPluginsAndRecycleRpcApplicationPools 方法遠端桌面服務，Win32_TSGatewayServerSettings 類別
- Win32_TSGatewayServerSettings 類別遠端桌面服務，SetDefaultPluginsAndRecycleRpcApplicationPools 方法
topic_type:
- apiref
api_name:
- Win32_TSGatewayServerSettings.SetDefaultPluginsAndRecycleRpcApplicationPools
api_location:
- AagWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3b9ead29e987b68ec3f041010be5dde64d8a2b54
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103934965"
---
# <a name="setdefaultpluginsandrecyclerpcapplicationpools-method-of-the-win32_tsgatewayserversettings-class"></a><span data-ttu-id="0e3aa-106">Win32 TSGatewayServerSettings 類別的 SetDefaultPluginsAndRecycleRpcApplicationPools 方法 \_</span><span class="sxs-lookup"><span data-stu-id="0e3aa-106">SetDefaultPluginsAndRecycleRpcApplicationPools method of the Win32\_TSGatewayServerSettings class</span></span>

<span data-ttu-id="0e3aa-107">針對遠端桌面閘道 (RD 閘道) 伺服器設定目前的驗證和授權外掛程式，並在 IIS 中回收 RPC 應用程式集區。</span><span class="sxs-lookup"><span data-stu-id="0e3aa-107">Sets the current authentication and authorization plug-ins for the Remote Desktop Gateway (RD Gateway) server and recycles the RPC application pools in IIS.</span></span>

## <a name="syntax"></a><span data-ttu-id="0e3aa-108">語法</span><span class="sxs-lookup"><span data-stu-id="0e3aa-108">Syntax</span></span>


```mof
uint32 SetDefaultPluginsAndRecycleRpcApplicationPools();
```



## <a name="parameters"></a><span data-ttu-id="0e3aa-109">參數</span><span class="sxs-lookup"><span data-stu-id="0e3aa-109">Parameters</span></span>

<span data-ttu-id="0e3aa-110">這個方法沒有任何參數。</span><span class="sxs-lookup"><span data-stu-id="0e3aa-110">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="0e3aa-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="0e3aa-111">Return value</span></span>

<span data-ttu-id="0e3aa-112">類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="0e3aa-112">Type: **uint32**</span></span>

<span data-ttu-id="0e3aa-113">如果方法成功，則會傳回零。</span><span class="sxs-lookup"><span data-stu-id="0e3aa-113">If the method succeeds, it returns zero.</span></span> <span data-ttu-id="0e3aa-114">如果方法失敗，則會傳回非零值。</span><span class="sxs-lookup"><span data-stu-id="0e3aa-114">If the method is unsuccessful, it returns a nonzero value.</span></span> <span data-ttu-id="0e3aa-115">如需錯誤碼清單，請參閱 [遠端桌面服務 WMI 提供者錯誤碼](terminal-services-wmi-provider-error-codes.md)。</span><span class="sxs-lookup"><span data-stu-id="0e3aa-115">For a list of error codes, see [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="0e3aa-116">備註</span><span class="sxs-lookup"><span data-stu-id="0e3aa-116">Remarks</span></span>

<span data-ttu-id="0e3aa-117">呼叫這個方法會導致所有現有的連接中斷。</span><span class="sxs-lookup"><span data-stu-id="0e3aa-117">Calling this method results in all existing connections being disconnected.</span></span>

<span data-ttu-id="0e3aa-118">您必須是 Administrators 群組的成員，才能呼叫這個方法。</span><span class="sxs-lookup"><span data-stu-id="0e3aa-118">You must be a member of the Administrators group to call this method.</span></span>

<span data-ttu-id="0e3aa-119">受控物件格式 (MOF) 檔包含 Windows Management Instrumentation (WMI) 類別的定義。</span><span class="sxs-lookup"><span data-stu-id="0e3aa-119">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="0e3aa-120">MOF 檔案不會安裝為 Microsoft Windows 軟體開發套件 (SDK) 的一部分。</span><span class="sxs-lookup"><span data-stu-id="0e3aa-120">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="0e3aa-121">當您使用伺服器管理員新增相關聯的角色時，它們會安裝在伺服器上。</span><span class="sxs-lookup"><span data-stu-id="0e3aa-121">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="0e3aa-122">如需 MOF 檔案的詳細資訊，請參閱 [受控物件格式 (mof) ](/windows/desktop/WmiSdk/managed-object-format--mof-)。</span><span class="sxs-lookup"><span data-stu-id="0e3aa-122">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="0e3aa-123">規格需求</span><span class="sxs-lookup"><span data-stu-id="0e3aa-123">Requirements</span></span>



| <span data-ttu-id="0e3aa-124">需求</span><span class="sxs-lookup"><span data-stu-id="0e3aa-124">Requirement</span></span> | <span data-ttu-id="0e3aa-125">值</span><span class="sxs-lookup"><span data-stu-id="0e3aa-125">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="0e3aa-126">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="0e3aa-126">Minimum supported client</span></span><br/> | <span data-ttu-id="0e3aa-127">都不支援</span><span class="sxs-lookup"><span data-stu-id="0e3aa-127">None supported</span></span><br/>                                                                |
| <span data-ttu-id="0e3aa-128">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="0e3aa-128">Minimum supported server</span></span><br/> | <span data-ttu-id="0e3aa-129">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="0e3aa-129">Windows Server 2008 R2</span></span><br/>                                                        |
| <span data-ttu-id="0e3aa-130">命名空間</span><span class="sxs-lookup"><span data-stu-id="0e3aa-130">Namespace</span></span><br/>                | <span data-ttu-id="0e3aa-131">根 \\ CIMv2 \\ microsoft-windows-terminalservices-gateway</span><span class="sxs-lookup"><span data-stu-id="0e3aa-131">Root\\CIMv2\\TerminalServices</span></span><br/>                                                 |
| <span data-ttu-id="0e3aa-132">MOF</span><span class="sxs-lookup"><span data-stu-id="0e3aa-132">MOF</span></span><br/>                      | <dl> <span data-ttu-id="0e3aa-133"><dt>TSGateway mof</dt></span><span class="sxs-lookup"><span data-stu-id="0e3aa-133"><dt>TSGateway.mof</dt></span></span> </dl> |
| <span data-ttu-id="0e3aa-134">DLL</span><span class="sxs-lookup"><span data-stu-id="0e3aa-134">DLL</span></span><br/>                      | <dl> <span data-ttu-id="0e3aa-135"><dt>AagWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0e3aa-135"><dt>AagWmi.dll</dt></span></span> </dl>    |



## <a name="see-also"></a><span data-ttu-id="0e3aa-136">另請參閱</span><span class="sxs-lookup"><span data-stu-id="0e3aa-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0e3aa-137">**Win32 \_ TSGatewayServerSettings**</span><span class="sxs-lookup"><span data-stu-id="0e3aa-137">**Win32\_TSGatewayServerSettings**</span></span>](win32-tsgatewayserversettings.md)
</dt> </dl>

 

