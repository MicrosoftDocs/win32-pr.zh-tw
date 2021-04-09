---
title: Win32_TSGatewayServerSettings 類別的 EnumAuthorizationPlugins 方法
description: 列舉所有已註冊的授權外掛程式。
ms.assetid: 525b4001-b89c-43cc-986a-00db47dd5518
ms.tgt_platform: multiple
keywords:
- EnumAuthorizationPlugins 方法遠端桌面服務
- EnumAuthorizationPlugins 方法遠端桌面服務，Win32_TSGatewayServerSettings 類別
- Win32_TSGatewayServerSettings 類別遠端桌面服務，EnumAuthorizationPlugins 方法
topic_type:
- apiref
api_name:
- Win32_TSGatewayServerSettings.EnumAuthorizationPlugins
api_location:
- AagWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9d955c08f5e4f91547751b0f177681ad2abd57c8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103844379"
---
# <a name="enumauthorizationplugins-method-of-the-win32_tsgatewayserversettings-class"></a><span data-ttu-id="24ee6-106">Win32 TSGatewayServerSettings 類別的 EnumAuthorizationPlugins 方法 \_</span><span class="sxs-lookup"><span data-stu-id="24ee6-106">EnumAuthorizationPlugins method of the Win32\_TSGatewayServerSettings class</span></span>

<span data-ttu-id="24ee6-107">列舉所有已註冊的授權外掛程式。</span><span class="sxs-lookup"><span data-stu-id="24ee6-107">Enumerates all registered authorization plug-ins.</span></span>

## <a name="syntax"></a><span data-ttu-id="24ee6-108">語法</span><span class="sxs-lookup"><span data-stu-id="24ee6-108">Syntax</span></span>


```mof
uint32 EnumAuthorizationPlugins(
  [out] string PluginNames[],
  [out] string CLSIDs[],
  [out] string Descriptions[]
);
```



## <a name="parameters"></a><span data-ttu-id="24ee6-109">參數</span><span class="sxs-lookup"><span data-stu-id="24ee6-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="24ee6-110">*PluginNames* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="24ee6-110">*PluginNames* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="24ee6-111">類型：**字串 \[ \]**</span><span class="sxs-lookup"><span data-stu-id="24ee6-111">Type: **string\[\]**</span></span>

<span data-ttu-id="24ee6-112">接收已註冊授權外掛程式名稱的 **字串** 陣列。</span><span class="sxs-lookup"><span data-stu-id="24ee6-112">A **string** array that receives the names of the registered authorization plug-ins.</span></span>

</dd> <dt>

<span data-ttu-id="24ee6-113">*Clsid* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="24ee6-113">*CLSIDs* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="24ee6-114">類型：**字串 \[ \]**</span><span class="sxs-lookup"><span data-stu-id="24ee6-114">Type: **string\[\]**</span></span>

<span data-ttu-id="24ee6-115">接收已註冊授權外掛程式之 Clsid 的 **字串** 陣列。</span><span class="sxs-lookup"><span data-stu-id="24ee6-115">A **string** array that receives the CLSIDs of the registered authorization plug-ins.</span></span>

</dd> <dt>

<span data-ttu-id="24ee6-116">*描述* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="24ee6-116">*Descriptions* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="24ee6-117">類型：**字串 \[ \]**</span><span class="sxs-lookup"><span data-stu-id="24ee6-117">Type: **string\[\]**</span></span>

<span data-ttu-id="24ee6-118">接收已註冊授權外掛程式之描述的 **字串** 陣列。</span><span class="sxs-lookup"><span data-stu-id="24ee6-118">A **string** array that receives the descriptions of the registered authorization plug-ins.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="24ee6-119">傳回值</span><span class="sxs-lookup"><span data-stu-id="24ee6-119">Return value</span></span>

<span data-ttu-id="24ee6-120">類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="24ee6-120">Type: **uint32**</span></span>

<span data-ttu-id="24ee6-121">如果方法成功，則會傳回零。</span><span class="sxs-lookup"><span data-stu-id="24ee6-121">If the method succeeds, it returns zero.</span></span> <span data-ttu-id="24ee6-122">如果方法失敗，則會傳回非零值。</span><span class="sxs-lookup"><span data-stu-id="24ee6-122">If the method is unsuccessful, it returns a nonzero value.</span></span> <span data-ttu-id="24ee6-123">如需錯誤碼清單，請參閱 [遠端桌面服務 WMI 提供者錯誤碼](terminal-services-wmi-provider-error-codes.md)。</span><span class="sxs-lookup"><span data-stu-id="24ee6-123">For a list of error codes, see [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="24ee6-124">備註</span><span class="sxs-lookup"><span data-stu-id="24ee6-124">Remarks</span></span>

<span data-ttu-id="24ee6-125">您必須是 Administrators 群組的成員，才能呼叫這個方法。</span><span class="sxs-lookup"><span data-stu-id="24ee6-125">You must be a member of the Administrators group to call this method.</span></span>

<span data-ttu-id="24ee6-126">受控物件格式 (MOF) 檔包含 Windows Management Instrumentation (WMI) 類別的定義。</span><span class="sxs-lookup"><span data-stu-id="24ee6-126">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="24ee6-127">MOF 檔案不會安裝為 Microsoft Windows 軟體開發套件 (SDK) 的一部分。</span><span class="sxs-lookup"><span data-stu-id="24ee6-127">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="24ee6-128">當您使用伺服器管理員新增相關聯的角色時，它們會安裝在伺服器上。</span><span class="sxs-lookup"><span data-stu-id="24ee6-128">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="24ee6-129">如需 MOF 檔案的詳細資訊，請參閱 [受控物件格式 (mof) ](/windows/desktop/WmiSdk/managed-object-format--mof-)。</span><span class="sxs-lookup"><span data-stu-id="24ee6-129">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="24ee6-130">規格需求</span><span class="sxs-lookup"><span data-stu-id="24ee6-130">Requirements</span></span>



| <span data-ttu-id="24ee6-131">需求</span><span class="sxs-lookup"><span data-stu-id="24ee6-131">Requirement</span></span> | <span data-ttu-id="24ee6-132">值</span><span class="sxs-lookup"><span data-stu-id="24ee6-132">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="24ee6-133">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="24ee6-133">Minimum supported client</span></span><br/> | <span data-ttu-id="24ee6-134">都不支援</span><span class="sxs-lookup"><span data-stu-id="24ee6-134">None supported</span></span><br/>                                                                |
| <span data-ttu-id="24ee6-135">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="24ee6-135">Minimum supported server</span></span><br/> | <span data-ttu-id="24ee6-136">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="24ee6-136">Windows Server 2008 R2</span></span><br/>                                                        |
| <span data-ttu-id="24ee6-137">命名空間</span><span class="sxs-lookup"><span data-stu-id="24ee6-137">Namespace</span></span><br/>                | <span data-ttu-id="24ee6-138">根 \\ CIMv2 \\ microsoft-windows-terminalservices-gateway</span><span class="sxs-lookup"><span data-stu-id="24ee6-138">Root\\CIMv2\\TerminalServices</span></span><br/>                                                 |
| <span data-ttu-id="24ee6-139">MOF</span><span class="sxs-lookup"><span data-stu-id="24ee6-139">MOF</span></span><br/>                      | <dl> <span data-ttu-id="24ee6-140"><dt>TSGateway mof</dt></span><span class="sxs-lookup"><span data-stu-id="24ee6-140"><dt>TSGateway.mof</dt></span></span> </dl> |
| <span data-ttu-id="24ee6-141">DLL</span><span class="sxs-lookup"><span data-stu-id="24ee6-141">DLL</span></span><br/>                      | <dl> <span data-ttu-id="24ee6-142"><dt>AagWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="24ee6-142"><dt>AagWmi.dll</dt></span></span> </dl>    |



## <a name="see-also"></a><span data-ttu-id="24ee6-143">另請參閱</span><span class="sxs-lookup"><span data-stu-id="24ee6-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="24ee6-144">**Win32 \_ TSGatewayServerSettings**</span><span class="sxs-lookup"><span data-stu-id="24ee6-144">**Win32\_TSGatewayServerSettings**</span></span>](win32-tsgatewayserversettings.md)
</dt> </dl>

 

