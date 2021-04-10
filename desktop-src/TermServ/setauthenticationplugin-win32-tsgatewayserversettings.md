---
title: Win32_TSGatewayServerSettings 類別的 SetAuthenticationPlugin 方法
description: 設定遠端桌面閘道 (RD 閘道) server 的目前驗證外掛程式。
ms.assetid: b79a5e7c-bf55-48f6-a6c0-5338e7eee2a1
ms.tgt_platform: multiple
keywords:
- SetAuthenticationPlugin 方法遠端桌面服務
- SetAuthenticationPlugin 方法遠端桌面服務，Win32_TSGatewayServerSettings 類別
- Win32_TSGatewayServerSettings 類別遠端桌面服務，SetAuthenticationPlugin 方法
topic_type:
- apiref
api_name:
- Win32_TSGatewayServerSettings.SetAuthenticationPlugin
api_location:
- AagWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f2b5b332dd288a01f96b0eb0b3a99e7e45269cdf
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103686428"
---
# <a name="setauthenticationplugin-method-of-the-win32_tsgatewayserversettings-class"></a><span data-ttu-id="39de8-106">Win32 TSGatewayServerSettings 類別的 SetAuthenticationPlugin 方法 \_</span><span class="sxs-lookup"><span data-stu-id="39de8-106">SetAuthenticationPlugin method of the Win32\_TSGatewayServerSettings class</span></span>

<span data-ttu-id="39de8-107">設定遠端桌面閘道 (RD 閘道) server 的目前驗證外掛程式。</span><span class="sxs-lookup"><span data-stu-id="39de8-107">Sets the current authentication plug-in for the Remote Desktop Gateway (RD Gateway) server.</span></span>

## <a name="syntax"></a><span data-ttu-id="39de8-108">語法</span><span class="sxs-lookup"><span data-stu-id="39de8-108">Syntax</span></span>


```mof
uint32 SetAuthenticationPlugin(
  [in] string PluginName
);
```



## <a name="parameters"></a><span data-ttu-id="39de8-109">參數</span><span class="sxs-lookup"><span data-stu-id="39de8-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="39de8-110">*PluginName* \[在\]</span><span class="sxs-lookup"><span data-stu-id="39de8-110">*PluginName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="39de8-111">類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="39de8-111">Type: **string**</span></span>

<span data-ttu-id="39de8-112">新目前驗證外掛程式的名稱。</span><span class="sxs-lookup"><span data-stu-id="39de8-112">The name of the new current authentication plug-in.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="39de8-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="39de8-113">Return value</span></span>

<span data-ttu-id="39de8-114">類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="39de8-114">Type: **uint32**</span></span>

<span data-ttu-id="39de8-115">如果方法成功，則會傳回零。</span><span class="sxs-lookup"><span data-stu-id="39de8-115">If the method succeeds, it returns zero.</span></span> <span data-ttu-id="39de8-116">如果方法失敗，則會傳回非零值。</span><span class="sxs-lookup"><span data-stu-id="39de8-116">If the method is unsuccessful, it returns a nonzero value.</span></span> <span data-ttu-id="39de8-117">如需錯誤碼清單，請參閱 [遠端桌面服務 WMI 提供者錯誤碼](terminal-services-wmi-provider-error-codes.md)。</span><span class="sxs-lookup"><span data-stu-id="39de8-117">For a list of error codes, see [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="39de8-118">備註</span><span class="sxs-lookup"><span data-stu-id="39de8-118">Remarks</span></span>

<span data-ttu-id="39de8-119">您必須呼叫 [**RecycleRpcApplicationPools**](recyclerpcapplicationpools-win32-tsgatewayserversettings.md) 方法，才能讓驗證外掛程式運作。</span><span class="sxs-lookup"><span data-stu-id="39de8-119">You must call the [**RecycleRpcApplicationPools**](recyclerpcapplicationpools-win32-tsgatewayserversettings.md) method to allow the authentication plug-in to work.</span></span>

<span data-ttu-id="39de8-120">您必須是 Administrators 群組的成員，才能呼叫這個方法。</span><span class="sxs-lookup"><span data-stu-id="39de8-120">You must be a member of the Administrators group to call this method.</span></span>

<span data-ttu-id="39de8-121">受控物件格式 (MOF) 檔包含 Windows Management Instrumentation (WMI) 類別的定義。</span><span class="sxs-lookup"><span data-stu-id="39de8-121">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="39de8-122">MOF 檔案不會安裝為 Microsoft Windows 軟體開發套件 (SDK) 的一部分。</span><span class="sxs-lookup"><span data-stu-id="39de8-122">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="39de8-123">當您使用伺服器管理員新增相關聯的角色時，它們會安裝在伺服器上。</span><span class="sxs-lookup"><span data-stu-id="39de8-123">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="39de8-124">如需 MOF 檔案的詳細資訊，請參閱 [受控物件格式 (mof) ](/windows/desktop/WmiSdk/managed-object-format--mof-)。</span><span class="sxs-lookup"><span data-stu-id="39de8-124">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="39de8-125">規格需求</span><span class="sxs-lookup"><span data-stu-id="39de8-125">Requirements</span></span>



| <span data-ttu-id="39de8-126">需求</span><span class="sxs-lookup"><span data-stu-id="39de8-126">Requirement</span></span> | <span data-ttu-id="39de8-127">值</span><span class="sxs-lookup"><span data-stu-id="39de8-127">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="39de8-128">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="39de8-128">Minimum supported client</span></span><br/> | <span data-ttu-id="39de8-129">都不支援</span><span class="sxs-lookup"><span data-stu-id="39de8-129">None supported</span></span><br/>                                                                |
| <span data-ttu-id="39de8-130">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="39de8-130">Minimum supported server</span></span><br/> | <span data-ttu-id="39de8-131">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="39de8-131">Windows Server 2008 R2</span></span><br/>                                                        |
| <span data-ttu-id="39de8-132">命名空間</span><span class="sxs-lookup"><span data-stu-id="39de8-132">Namespace</span></span><br/>                | <span data-ttu-id="39de8-133">根 \\ CIMv2 \\ microsoft-windows-terminalservices-gateway</span><span class="sxs-lookup"><span data-stu-id="39de8-133">Root\\CIMv2\\TerminalServices</span></span><br/>                                                 |
| <span data-ttu-id="39de8-134">MOF</span><span class="sxs-lookup"><span data-stu-id="39de8-134">MOF</span></span><br/>                      | <dl> <span data-ttu-id="39de8-135"><dt>TSGateway mof</dt></span><span class="sxs-lookup"><span data-stu-id="39de8-135"><dt>TSGateway.mof</dt></span></span> </dl> |
| <span data-ttu-id="39de8-136">DLL</span><span class="sxs-lookup"><span data-stu-id="39de8-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="39de8-137"><dt>AagWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="39de8-137"><dt>AagWmi.dll</dt></span></span> </dl>    |



## <a name="see-also"></a><span data-ttu-id="39de8-138">另請參閱</span><span class="sxs-lookup"><span data-stu-id="39de8-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="39de8-139">**Win32 \_ TSGatewayServerSettings**</span><span class="sxs-lookup"><span data-stu-id="39de8-139">**Win32\_TSGatewayServerSettings**</span></span>](win32-tsgatewayserversettings.md)
</dt> <dt>

[<span data-ttu-id="39de8-140">**RecycleRpcApplicationPools**</span><span class="sxs-lookup"><span data-stu-id="39de8-140">**RecycleRpcApplicationPools**</span></span>](recyclerpcapplicationpools-win32-tsgatewayserversettings.md)
</dt> </dl>

 

