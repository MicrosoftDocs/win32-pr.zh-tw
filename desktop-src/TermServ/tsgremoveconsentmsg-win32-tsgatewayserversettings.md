---
title: Win32_TSGatewayServerSettings 類別的 TSGRemoveConsentMsg 方法
description: 移除閘道伺服器的系統管理訊息。 |Win32_TSGatewayServerSettings 類別的 TSGRemoveConsentMsg 方法
ms.assetid: 626dc9ca-d6a1-48ab-84ec-cfccb8e720c2
ms.tgt_platform: multiple
keywords:
- TSGRemoveConsentMsg 方法遠端桌面服務
- TSGRemoveConsentMsg 方法遠端桌面服務，Win32_TSGatewayServerSettings 類別
- Win32_TSGatewayServerSettings 類別遠端桌面服務，TSGRemoveConsentMsg 方法
topic_type:
- apiref
api_name:
- Win32_TSGatewayServerSettings.TSGRemoveConsentMsg
api_location:
- AagWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 24cd002ebb1a953d25cf129b4e5f3b4174842199
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/09/2021
ms.locfileid: "103853836"
---
# <a name="tsgremoveconsentmsg-method-of-the-win32_tsgatewayserversettings-class"></a><span data-ttu-id="7cac8-107">Win32 TSGatewayServerSettings 類別的 TSGRemoveConsentMsg 方法 \_</span><span class="sxs-lookup"><span data-stu-id="7cac8-107">TSGRemoveConsentMsg method of the Win32\_TSGatewayServerSettings class</span></span>

<span data-ttu-id="7cac8-108">移除閘道伺服器的系統管理訊息。</span><span class="sxs-lookup"><span data-stu-id="7cac8-108">Removes the administrative message for the gateway server.</span></span>

## <a name="syntax"></a><span data-ttu-id="7cac8-109">語法</span><span class="sxs-lookup"><span data-stu-id="7cac8-109">Syntax</span></span>


```mof
uint32 TSGRemoveConsentMsg();
```



## <a name="parameters"></a><span data-ttu-id="7cac8-110">參數</span><span class="sxs-lookup"><span data-stu-id="7cac8-110">Parameters</span></span>

<span data-ttu-id="7cac8-111">這個方法沒有任何參數。</span><span class="sxs-lookup"><span data-stu-id="7cac8-111">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="7cac8-112">傳回值</span><span class="sxs-lookup"><span data-stu-id="7cac8-112">Return value</span></span>

<span data-ttu-id="7cac8-113">類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="7cac8-113">Type: **uint32**</span></span>

<span data-ttu-id="7cac8-114">如果方法成功，則會傳回零。</span><span class="sxs-lookup"><span data-stu-id="7cac8-114">If the method succeeds, it returns zero.</span></span> <span data-ttu-id="7cac8-115">如果方法失敗，則會傳回非零值。</span><span class="sxs-lookup"><span data-stu-id="7cac8-115">If the method is unsuccessful, it returns a nonzero value.</span></span> <span data-ttu-id="7cac8-116">如需錯誤碼清單，請參閱 [遠端桌面服務 WMI 提供者錯誤碼](terminal-services-wmi-provider-error-codes.md)。</span><span class="sxs-lookup"><span data-stu-id="7cac8-116">For a list of error codes, see [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="7cac8-117">備註</span><span class="sxs-lookup"><span data-stu-id="7cac8-117">Remarks</span></span>

<span data-ttu-id="7cac8-118">您必須是 Administrators 群組的成員，才能呼叫這個方法。</span><span class="sxs-lookup"><span data-stu-id="7cac8-118">You must be a member of the Administrators group to call this method.</span></span>

<span data-ttu-id="7cac8-119">受控物件格式 (MOF) 檔包含 Windows Management Instrumentation (WMI) 類別的定義。</span><span class="sxs-lookup"><span data-stu-id="7cac8-119">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="7cac8-120">MOF 檔案不會安裝為 Microsoft Windows 軟體開發套件 (SDK) 的一部分。</span><span class="sxs-lookup"><span data-stu-id="7cac8-120">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="7cac8-121">當您使用伺服器管理員新增相關聯的角色時，它們會安裝在伺服器上。</span><span class="sxs-lookup"><span data-stu-id="7cac8-121">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="7cac8-122">如需 MOF 檔案的詳細資訊，請參閱 [受控物件格式 (mof) ](/windows/desktop/WmiSdk/managed-object-format--mof-)。</span><span class="sxs-lookup"><span data-stu-id="7cac8-122">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="7cac8-123">規格需求</span><span class="sxs-lookup"><span data-stu-id="7cac8-123">Requirements</span></span>



| <span data-ttu-id="7cac8-124">需求</span><span class="sxs-lookup"><span data-stu-id="7cac8-124">Requirement</span></span> | <span data-ttu-id="7cac8-125">值</span><span class="sxs-lookup"><span data-stu-id="7cac8-125">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="7cac8-126">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="7cac8-126">Minimum supported client</span></span><br/> | <span data-ttu-id="7cac8-127">都不支援</span><span class="sxs-lookup"><span data-stu-id="7cac8-127">None supported</span></span><br/>                                                                |
| <span data-ttu-id="7cac8-128">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="7cac8-128">Minimum supported server</span></span><br/> | <span data-ttu-id="7cac8-129">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="7cac8-129">Windows Server 2008 R2</span></span><br/>                                                        |
| <span data-ttu-id="7cac8-130">命名空間</span><span class="sxs-lookup"><span data-stu-id="7cac8-130">Namespace</span></span><br/>                | <span data-ttu-id="7cac8-131">根 \\ CIMv2 \\ microsoft-windows-terminalservices-gateway</span><span class="sxs-lookup"><span data-stu-id="7cac8-131">Root\\CIMv2\\TerminalServices</span></span><br/>                                                 |
| <span data-ttu-id="7cac8-132">MOF</span><span class="sxs-lookup"><span data-stu-id="7cac8-132">MOF</span></span><br/>                      | <dl> <span data-ttu-id="7cac8-133"><dt>TSGateway mof</dt></span><span class="sxs-lookup"><span data-stu-id="7cac8-133"><dt>TSGateway.mof</dt></span></span> </dl> |
| <span data-ttu-id="7cac8-134">DLL</span><span class="sxs-lookup"><span data-stu-id="7cac8-134">DLL</span></span><br/>                      | <dl> <span data-ttu-id="7cac8-135"><dt>AagWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7cac8-135"><dt>AagWmi.dll</dt></span></span> </dl>    |



## <a name="see-also"></a><span data-ttu-id="7cac8-136">另請參閱</span><span class="sxs-lookup"><span data-stu-id="7cac8-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7cac8-137">**Win32 \_ TSGatewayServerSettings**</span><span class="sxs-lookup"><span data-stu-id="7cac8-137">**Win32\_TSGatewayServerSettings**</span></span>](win32-tsgatewayserversettings.md)
</dt> </dl>

 

