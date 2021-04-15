---
title: Win32_TSGatewayServerSettings 類別的 EnableLogEvent 方法
description: 啟用或停用指定事件種類的記錄。
ms.assetid: e901ef51-2ae2-4123-902a-ac359f3eb959
ms.tgt_platform: multiple
keywords:
- EnableLogEvent 方法遠端桌面服務
- EnableLogEvent 方法遠端桌面服務，Win32_TSGatewayServerSettings 類別
- Win32_TSGatewayServerSettings 類別遠端桌面服務，EnableLogEvent 方法
topic_type:
- apiref
api_name:
- Win32_TSGatewayServerSettings.EnableLogEvent
api_location:
- AagWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e72f7cb8567c7f2d5c3ca79d241013e2bd64a5e2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104467041"
---
# <a name="enablelogevent-method-of-the-win32_tsgatewayserversettings-class"></a><span data-ttu-id="8fb02-106">Win32 TSGatewayServerSettings 類別的 EnableLogEvent 方法 \_</span><span class="sxs-lookup"><span data-stu-id="8fb02-106">EnableLogEvent method of the Win32\_TSGatewayServerSettings class</span></span>

<span data-ttu-id="8fb02-107">啟用或停用指定事件種類的記錄。</span><span class="sxs-lookup"><span data-stu-id="8fb02-107">Enables or disables logging of the specified event type.</span></span>

## <a name="syntax"></a><span data-ttu-id="8fb02-108">語法</span><span class="sxs-lookup"><span data-stu-id="8fb02-108">Syntax</span></span>


```mof
uint32 EnableLogEvent(
  [in] string  EventName,
  [in] boolean Enabled
);
```



## <a name="parameters"></a><span data-ttu-id="8fb02-109">參數</span><span class="sxs-lookup"><span data-stu-id="8fb02-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8fb02-110">*事件名稱* \[在\]</span><span class="sxs-lookup"><span data-stu-id="8fb02-110">*EventName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8fb02-111">活動的名稱。</span><span class="sxs-lookup"><span data-stu-id="8fb02-111">Name of the event.</span></span> <span data-ttu-id="8fb02-112">此值應該使用 [**GetLogEventName**](getlogeventname-win32-tsgatewayserversettings.md) 方法來抓取。</span><span class="sxs-lookup"><span data-stu-id="8fb02-112">This value should be retrieved by using the [**GetLogEventName**](getlogeventname-win32-tsgatewayserversettings.md) method.</span></span>

<dt>

<span data-ttu-id="8fb02-113">LogChannelDisconnect</span><span class="sxs-lookup"><span data-stu-id="8fb02-113">LogChannelDisconnect</span></span>
</dt> <dd>

<span data-ttu-id="8fb02-114">使用者已成功與資源中斷連線。</span><span class="sxs-lookup"><span data-stu-id="8fb02-114">User successfully disconnected from the resource.</span></span>

</dd> <dt>

<span data-ttu-id="8fb02-115">LogFailedChannelConnect</span><span class="sxs-lookup"><span data-stu-id="8fb02-115">LogFailedChannelConnect</span></span>
</dt> <dd>

<span data-ttu-id="8fb02-116">使用者無法連線到資源。</span><span class="sxs-lookup"><span data-stu-id="8fb02-116">User failed to connect to the resource.</span></span>

</dd> <dt>

<span data-ttu-id="8fb02-117">LogFailureNetworkAccessCheck</span><span class="sxs-lookup"><span data-stu-id="8fb02-117">LogFailureNetworkAccessCheck</span></span>
</dt> <dd>

<span data-ttu-id="8fb02-118">使用者連接授權失敗。</span><span class="sxs-lookup"><span data-stu-id="8fb02-118">User failed connection authorization.</span></span>

</dd> <dt>

<span data-ttu-id="8fb02-119">LogFailureResourceAccessCheck</span><span class="sxs-lookup"><span data-stu-id="8fb02-119">LogFailureResourceAccessCheck</span></span>
</dt> <dd>

<span data-ttu-id="8fb02-120">使用者失敗的資源授權。</span><span class="sxs-lookup"><span data-stu-id="8fb02-120">User failed resource authorization.</span></span>

</dd> <dt>

<span data-ttu-id="8fb02-121">LogSuccessChannelConnect</span><span class="sxs-lookup"><span data-stu-id="8fb02-121">LogSuccessChannelConnect</span></span>
</dt> <dd>

<span data-ttu-id="8fb02-122">使用者已成功連線至資源。</span><span class="sxs-lookup"><span data-stu-id="8fb02-122">User successfully connected to the resource.</span></span>

</dd> <dt>

<span data-ttu-id="8fb02-123">LogSuccessfulNetworkAccessCheck</span><span class="sxs-lookup"><span data-stu-id="8fb02-123">LogSuccessfulNetworkAccessCheck</span></span>
</dt> <dd>

<span data-ttu-id="8fb02-124">使用者成功傳遞連接授權。</span><span class="sxs-lookup"><span data-stu-id="8fb02-124">User successfully passed connection authorization.</span></span>

</dd> <dt>

<span data-ttu-id="8fb02-125">LogSuccessfulResourceAccessCheck</span><span class="sxs-lookup"><span data-stu-id="8fb02-125">LogSuccessfulResourceAccessCheck</span></span>
</dt> <dd>

<span data-ttu-id="8fb02-126">使用者已成功傳遞資源授權。</span><span class="sxs-lookup"><span data-stu-id="8fb02-126">User successfully passed resource authorization.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="8fb02-127">*已啟用* \[在\]</span><span class="sxs-lookup"><span data-stu-id="8fb02-127">*Enabled* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8fb02-128">指定是否應啟用或停用事件。</span><span class="sxs-lookup"><span data-stu-id="8fb02-128">Specifies whether the event should be enabled or disabled.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8fb02-129">傳回值</span><span class="sxs-lookup"><span data-stu-id="8fb02-129">Return value</span></span>

<span data-ttu-id="8fb02-130">如果方法成功，則會傳回零。</span><span class="sxs-lookup"><span data-stu-id="8fb02-130">If the method succeeds, it returns zero.</span></span> <span data-ttu-id="8fb02-131">如果方法失敗，則會傳回非零值。</span><span class="sxs-lookup"><span data-stu-id="8fb02-131">If the method is unsuccessful, it returns a nonzero value.</span></span> <span data-ttu-id="8fb02-132">如需錯誤碼清單，請參閱 [遠端桌面服務 WMI 提供者錯誤碼](terminal-services-wmi-provider-error-codes.md)。</span><span class="sxs-lookup"><span data-stu-id="8fb02-132">For a list of error codes, see [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="8fb02-133">備註</span><span class="sxs-lookup"><span data-stu-id="8fb02-133">Remarks</span></span>

<span data-ttu-id="8fb02-134">您必須是 Administrators 群組的成員，才能呼叫這個方法。</span><span class="sxs-lookup"><span data-stu-id="8fb02-134">You must be a member of the Administrators group to call this method.</span></span>

<span data-ttu-id="8fb02-135">受控物件格式 (MOF) 檔包含 Windows Management Instrumentation (WMI) 類別的定義。</span><span class="sxs-lookup"><span data-stu-id="8fb02-135">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="8fb02-136">MOF 檔案不會安裝為 Microsoft Windows 軟體開發套件 (SDK) 的一部分。</span><span class="sxs-lookup"><span data-stu-id="8fb02-136">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="8fb02-137">當您使用伺服器管理員新增相關聯的角色時，它們會安裝在伺服器上。</span><span class="sxs-lookup"><span data-stu-id="8fb02-137">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="8fb02-138">如需 MOF 檔案的詳細資訊，請參閱 [受控物件格式 (mof) ](/windows/desktop/WmiSdk/managed-object-format--mof-)。</span><span class="sxs-lookup"><span data-stu-id="8fb02-138">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="8fb02-139">規格需求</span><span class="sxs-lookup"><span data-stu-id="8fb02-139">Requirements</span></span>



| <span data-ttu-id="8fb02-140">需求</span><span class="sxs-lookup"><span data-stu-id="8fb02-140">Requirement</span></span> | <span data-ttu-id="8fb02-141">值</span><span class="sxs-lookup"><span data-stu-id="8fb02-141">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="8fb02-142">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="8fb02-142">Minimum supported client</span></span><br/> | <span data-ttu-id="8fb02-143">都不支援</span><span class="sxs-lookup"><span data-stu-id="8fb02-143">None supported</span></span><br/>                                                                |
| <span data-ttu-id="8fb02-144">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="8fb02-144">Minimum supported server</span></span><br/> | <span data-ttu-id="8fb02-145">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="8fb02-145">Windows Server 2008</span></span><br/>                                                           |
| <span data-ttu-id="8fb02-146">命名空間</span><span class="sxs-lookup"><span data-stu-id="8fb02-146">Namespace</span></span><br/>                | <span data-ttu-id="8fb02-147">根 \\ CIMv2 \\ microsoft-windows-terminalservices-gateway</span><span class="sxs-lookup"><span data-stu-id="8fb02-147">Root\\CIMv2\\TerminalServices</span></span><br/>                                                 |
| <span data-ttu-id="8fb02-148">MOF</span><span class="sxs-lookup"><span data-stu-id="8fb02-148">MOF</span></span><br/>                      | <dl> <span data-ttu-id="8fb02-149"><dt>TSGateway mof</dt></span><span class="sxs-lookup"><span data-stu-id="8fb02-149"><dt>TSGateway.mof</dt></span></span> </dl> |
| <span data-ttu-id="8fb02-150">DLL</span><span class="sxs-lookup"><span data-stu-id="8fb02-150">DLL</span></span><br/>                      | <dl> <span data-ttu-id="8fb02-151"><dt>AagWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="8fb02-151"><dt>AagWmi.dll</dt></span></span> </dl>    |



## <a name="see-also"></a><span data-ttu-id="8fb02-152">另請參閱</span><span class="sxs-lookup"><span data-stu-id="8fb02-152">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8fb02-153">**Win32 \_ TSGatewayServerSettings**</span><span class="sxs-lookup"><span data-stu-id="8fb02-153">**Win32\_TSGatewayServerSettings**</span></span>](win32-tsgatewayserversettings.md)
</dt> <dt>

[<span data-ttu-id="8fb02-154">**GetLogEventName**</span><span class="sxs-lookup"><span data-stu-id="8fb02-154">**GetLogEventName**</span></span>](getlogeventname-win32-tsgatewayserversettings.md)
</dt> </dl>

 

