---
title: Win32_TSGatewayConnectionAuthorizationPolicy 類別的 SetSessionTimeout 方法
description: 設定 SessionTimeout 和 SessionTimeoutAction 屬性。
ms.assetid: 11491c97-3ef8-46c1-9504-696c613e374e
ms.tgt_platform: multiple
keywords:
- SetSessionTimeout 方法遠端桌面服務
- SetSessionTimeout 方法遠端桌面服務，Win32_TSGatewayConnectionAuthorizationPolicy 類別
- Win32_TSGatewayConnectionAuthorizationPolicy 類別遠端桌面服務，SetSessionTimeout 方法
topic_type:
- apiref
api_name:
- Win32_TSGatewayConnectionAuthorizationPolicy.SetSessionTimeout
api_location:
- AagWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a8e544b59ae4fe0b74d0c120e6884ab81743cac6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104508831"
---
# <a name="setsessiontimeout-method-of-the-win32_tsgatewayconnectionauthorizationpolicy-class"></a><span data-ttu-id="28838-106">Win32 TSGatewayConnectionAuthorizationPolicy 類別的 SetSessionTimeout 方法 \_</span><span class="sxs-lookup"><span data-stu-id="28838-106">SetSessionTimeout method of the Win32\_TSGatewayConnectionAuthorizationPolicy class</span></span>

<span data-ttu-id="28838-107">設定 **SessionTimeout** 和 **SessionTimeoutAction** 屬性。</span><span class="sxs-lookup"><span data-stu-id="28838-107">Sets the **SessionTimeout** and **SessionTimeoutAction** properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="28838-108">語法</span><span class="sxs-lookup"><span data-stu-id="28838-108">Syntax</span></span>


```mof
uint32 SetSessionTimeout(
  [in] uint32 SessionTimeout,
  [in] uint32 SessionTimeoutAction
);
```



## <a name="parameters"></a><span data-ttu-id="28838-109">參數</span><span class="sxs-lookup"><span data-stu-id="28838-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="28838-110">*SessionTimeout* \[在\]</span><span class="sxs-lookup"><span data-stu-id="28838-110">*SessionTimeout* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="28838-111">類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="28838-111">Type: **uint32**</span></span>

<span data-ttu-id="28838-112">新的超時值（以分鐘為單位）。</span><span class="sxs-lookup"><span data-stu-id="28838-112">The new timeout value, in minutes.</span></span> <span data-ttu-id="28838-113">值為0表示沒有任何超時時間。</span><span class="sxs-lookup"><span data-stu-id="28838-113">A value of 0 means there is no timeout.</span></span>

</dd> <dt>

<span data-ttu-id="28838-114">*SessionTimeoutAction* \[在\]</span><span class="sxs-lookup"><span data-stu-id="28838-114">*SessionTimeoutAction* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="28838-115">類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="28838-115">Type: **uint32**</span></span>

<span data-ttu-id="28838-116">指定在會話超時時要採取的動作。</span><span class="sxs-lookup"><span data-stu-id="28838-116">Specifies the action to be taken in case of a session timeout.</span></span> <span data-ttu-id="28838-117">這可以是下列其中一個值。</span><span class="sxs-lookup"><span data-stu-id="28838-117">This can be one of the following values.</span></span>

<dt>

<span data-ttu-id="28838-118">0</span><span class="sxs-lookup"><span data-stu-id="28838-118">0</span></span>
</dt> <dd>

<span data-ttu-id="28838-119">中斷會話的連線。</span><span class="sxs-lookup"><span data-stu-id="28838-119">Disconnect the session.</span></span>

</dd> <dt>

<span data-ttu-id="28838-120">1</span><span class="sxs-lookup"><span data-stu-id="28838-120">1</span></span>
</dt> <dd>

<span data-ttu-id="28838-121">嘗試重新授權會話。</span><span class="sxs-lookup"><span data-stu-id="28838-121">Attempt to re-authorize the session.</span></span>

</dd> </dl> </dd> </dl>

## <a name="return-value"></a><span data-ttu-id="28838-122">傳回值</span><span class="sxs-lookup"><span data-stu-id="28838-122">Return value</span></span>

<span data-ttu-id="28838-123">類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="28838-123">Type: **uint32**</span></span>

<span data-ttu-id="28838-124">如果方法成功，則會傳回零。</span><span class="sxs-lookup"><span data-stu-id="28838-124">If the method succeeds, it returns zero.</span></span> <span data-ttu-id="28838-125">如果方法失敗，則會傳回非零值。</span><span class="sxs-lookup"><span data-stu-id="28838-125">If the method is unsuccessful, it returns a nonzero value.</span></span> <span data-ttu-id="28838-126">如需錯誤碼清單，請參閱 [遠端桌面服務 WMI 提供者錯誤碼](terminal-services-wmi-provider-error-codes.md)。</span><span class="sxs-lookup"><span data-stu-id="28838-126">For a list of error codes, see [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="28838-127">備註</span><span class="sxs-lookup"><span data-stu-id="28838-127">Remarks</span></span>

<span data-ttu-id="28838-128">您必須是 Administrators 群組的成員，才能呼叫這個方法。</span><span class="sxs-lookup"><span data-stu-id="28838-128">You must be a member of the Administrators group to call this method.</span></span>

<span data-ttu-id="28838-129">受控物件格式 (MOF) 檔包含 Windows Management Instrumentation (WMI) 類別的定義。</span><span class="sxs-lookup"><span data-stu-id="28838-129">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="28838-130">MOF 檔案不會安裝為 Microsoft Windows 軟體開發套件 (SDK) 的一部分。</span><span class="sxs-lookup"><span data-stu-id="28838-130">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="28838-131">當您使用伺服器管理員新增相關聯的角色時，它們會安裝在伺服器上。</span><span class="sxs-lookup"><span data-stu-id="28838-131">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="28838-132">如需 MOF 檔案的詳細資訊，請參閱 [受控物件格式 (mof) ](/windows/desktop/WmiSdk/managed-object-format--mof-)。</span><span class="sxs-lookup"><span data-stu-id="28838-132">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="28838-133">規格需求</span><span class="sxs-lookup"><span data-stu-id="28838-133">Requirements</span></span>



| <span data-ttu-id="28838-134">需求</span><span class="sxs-lookup"><span data-stu-id="28838-134">Requirement</span></span> | <span data-ttu-id="28838-135">值</span><span class="sxs-lookup"><span data-stu-id="28838-135">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="28838-136">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="28838-136">Minimum supported client</span></span><br/> | <span data-ttu-id="28838-137">都不支援</span><span class="sxs-lookup"><span data-stu-id="28838-137">None supported</span></span><br/>                                                                |
| <span data-ttu-id="28838-138">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="28838-138">Minimum supported server</span></span><br/> | <span data-ttu-id="28838-139">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="28838-139">Windows Server 2008 R2</span></span><br/>                                                        |
| <span data-ttu-id="28838-140">命名空間</span><span class="sxs-lookup"><span data-stu-id="28838-140">Namespace</span></span><br/>                | <span data-ttu-id="28838-141">根 \\ CIMv2 \\ microsoft-windows-terminalservices-gateway</span><span class="sxs-lookup"><span data-stu-id="28838-141">Root\\CIMv2\\TerminalServices</span></span><br/>                                                 |
| <span data-ttu-id="28838-142">MOF</span><span class="sxs-lookup"><span data-stu-id="28838-142">MOF</span></span><br/>                      | <dl> <span data-ttu-id="28838-143"><dt>TSGateway mof</dt></span><span class="sxs-lookup"><span data-stu-id="28838-143"><dt>TSGateway.mof</dt></span></span> </dl> |
| <span data-ttu-id="28838-144">DLL</span><span class="sxs-lookup"><span data-stu-id="28838-144">DLL</span></span><br/>                      | <dl> <span data-ttu-id="28838-145"><dt>AagWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="28838-145"><dt>AagWmi.dll</dt></span></span> </dl>    |



## <a name="see-also"></a><span data-ttu-id="28838-146">另請參閱</span><span class="sxs-lookup"><span data-stu-id="28838-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="28838-147">**Win32 \_ TSGatewayConnectionAuthorizationPolicy**</span><span class="sxs-lookup"><span data-stu-id="28838-147">**Win32\_TSGatewayConnectionAuthorizationPolicy**</span></span>](win32-tsgatewayconnectionauthorizationpolicy.md)
</dt> </dl>

 

