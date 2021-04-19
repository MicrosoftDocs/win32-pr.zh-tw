---
title: Win32_TSGatewayServerSettings 類別的 IsLogEventEnabled 方法
description: 指出是否已啟用指定的事件記錄檔類型。
ms.assetid: 4abfc56f-871a-44ef-9998-da88949a0a2d
ms.tgt_platform: multiple
keywords:
- IsLogEventEnabled 方法遠端桌面服務
- IsLogEventEnabled 方法遠端桌面服務，Win32_TSGatewayServerSettings 類別
- Win32_TSGatewayServerSettings 類別遠端桌面服務，IsLogEventEnabled 方法
topic_type:
- apiref
api_name:
- Win32_TSGatewayServerSettings.IsLogEventEnabled
api_location:
- AagWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9acefe60a9ba50c49146d25c7bccddf706f198c5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106965920"
---
# <a name="islogeventenabled-method-of-the-win32_tsgatewayserversettings-class"></a><span data-ttu-id="18141-106">Win32 TSGatewayServerSettings 類別的 IsLogEventEnabled 方法 \_</span><span class="sxs-lookup"><span data-stu-id="18141-106">IsLogEventEnabled method of the Win32\_TSGatewayServerSettings class</span></span>

<span data-ttu-id="18141-107">指出是否已啟用指定的事件記錄檔類型。</span><span class="sxs-lookup"><span data-stu-id="18141-107">Indicates whether the specified event log type is enabled.</span></span>

## <a name="syntax"></a><span data-ttu-id="18141-108">語法</span><span class="sxs-lookup"><span data-stu-id="18141-108">Syntax</span></span>


```mof
uint32 IsLogEventEnabled(
  [in]  string  EventName,
  [out] boolean Enabled
);
```



## <a name="parameters"></a><span data-ttu-id="18141-109">參數</span><span class="sxs-lookup"><span data-stu-id="18141-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="18141-110">*事件名稱* \[在\]</span><span class="sxs-lookup"><span data-stu-id="18141-110">*EventName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="18141-111">事件記錄檔類型的名稱。</span><span class="sxs-lookup"><span data-stu-id="18141-111">Name of the event log type.</span></span> <span data-ttu-id="18141-112">此值應該使用 [**GetLogEventName**](getlogeventname-win32-tsgatewayserversettings.md) 方法來抓取。</span><span class="sxs-lookup"><span data-stu-id="18141-112">This value should be retrieved by using the [**GetLogEventName**](getlogeventname-win32-tsgatewayserversettings.md) method.</span></span>

<dt>

<span data-ttu-id="18141-113">LogChannelDisconnect</span><span class="sxs-lookup"><span data-stu-id="18141-113">LogChannelDisconnect</span></span>
</dt> <dd>

<span data-ttu-id="18141-114">使用者已成功與資源中斷連線。</span><span class="sxs-lookup"><span data-stu-id="18141-114">User successfully disconnected from the resource.</span></span>

</dd> <dt>

<span data-ttu-id="18141-115">LogFailedChannelConnect</span><span class="sxs-lookup"><span data-stu-id="18141-115">LogFailedChannelConnect</span></span>
</dt> <dd>

<span data-ttu-id="18141-116">使用者無法連線到資源。</span><span class="sxs-lookup"><span data-stu-id="18141-116">User failed to connect to the resource.</span></span>

</dd> <dt>

<span data-ttu-id="18141-117">LogFailureNetworkAccessCheck</span><span class="sxs-lookup"><span data-stu-id="18141-117">LogFailureNetworkAccessCheck</span></span>
</dt> <dd>

<span data-ttu-id="18141-118">使用者連接授權失敗。</span><span class="sxs-lookup"><span data-stu-id="18141-118">User failed connection authorization.</span></span>

</dd> <dt>

<span data-ttu-id="18141-119">LogFailureResourceAccessCheck</span><span class="sxs-lookup"><span data-stu-id="18141-119">LogFailureResourceAccessCheck</span></span>
</dt> <dd>

<span data-ttu-id="18141-120">使用者失敗的資源授權。</span><span class="sxs-lookup"><span data-stu-id="18141-120">User failed resource authorization.</span></span>

</dd> <dt>

<span data-ttu-id="18141-121">LogSuccessChannelConnect</span><span class="sxs-lookup"><span data-stu-id="18141-121">LogSuccessChannelConnect</span></span>
</dt> <dd>

<span data-ttu-id="18141-122">使用者已成功連線至資源。</span><span class="sxs-lookup"><span data-stu-id="18141-122">User successfully connected to the resource.</span></span>

</dd> <dt>

<span data-ttu-id="18141-123">LogSuccessfulNetworkAccessCheck</span><span class="sxs-lookup"><span data-stu-id="18141-123">LogSuccessfulNetworkAccessCheck</span></span>
</dt> <dd>

<span data-ttu-id="18141-124">使用者成功傳遞連接授權。</span><span class="sxs-lookup"><span data-stu-id="18141-124">User successfully passed connection authorization.</span></span>

</dd> <dt>

<span data-ttu-id="18141-125">LogSuccessfulResourceAccessCheck</span><span class="sxs-lookup"><span data-stu-id="18141-125">LogSuccessfulResourceAccessCheck</span></span>
</dt> <dd>

<span data-ttu-id="18141-126">使用者已成功傳遞資源授權。</span><span class="sxs-lookup"><span data-stu-id="18141-126">User successfully passed resource authorization.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="18141-127">*已啟用* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="18141-127">*Enabled* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="18141-128">指出是否已啟用指定的事件記錄檔類型。</span><span class="sxs-lookup"><span data-stu-id="18141-128">Indicates whether the specified event log type is enabled.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="18141-129">傳回值</span><span class="sxs-lookup"><span data-stu-id="18141-129">Return value</span></span>

<span data-ttu-id="18141-130">如果方法成功，則會傳回零。</span><span class="sxs-lookup"><span data-stu-id="18141-130">If the method succeeds, it returns zero.</span></span> <span data-ttu-id="18141-131">如果方法失敗，則會傳回非零值。</span><span class="sxs-lookup"><span data-stu-id="18141-131">If the method is unsuccessful, it returns a nonzero value.</span></span> <span data-ttu-id="18141-132">如需錯誤碼清單，請參閱 [遠端桌面服務 WMI 提供者錯誤碼](terminal-services-wmi-provider-error-codes.md)。</span><span class="sxs-lookup"><span data-stu-id="18141-132">For a list of error codes, see [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="18141-133">備註</span><span class="sxs-lookup"><span data-stu-id="18141-133">Remarks</span></span>

<span data-ttu-id="18141-134">您必須是 Administrators 群組的成員，才能呼叫這個方法。</span><span class="sxs-lookup"><span data-stu-id="18141-134">You must be a member of the Administrators group to call this method.</span></span>

<span data-ttu-id="18141-135">受控物件格式 (MOF) 檔包含 Windows Management Instrumentation (WMI) 類別的定義。</span><span class="sxs-lookup"><span data-stu-id="18141-135">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="18141-136">MOF 檔案不會安裝為 Microsoft Windows 軟體開發套件 (SDK) 的一部分。</span><span class="sxs-lookup"><span data-stu-id="18141-136">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="18141-137">當您使用伺服器管理員新增相關聯的角色時，它們會安裝在伺服器上。</span><span class="sxs-lookup"><span data-stu-id="18141-137">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="18141-138">如需 MOF 檔案的詳細資訊，請參閱 [受控物件格式 (mof) ](/windows/desktop/WmiSdk/managed-object-format--mof-)。</span><span class="sxs-lookup"><span data-stu-id="18141-138">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="18141-139">規格需求</span><span class="sxs-lookup"><span data-stu-id="18141-139">Requirements</span></span>



| <span data-ttu-id="18141-140">需求</span><span class="sxs-lookup"><span data-stu-id="18141-140">Requirement</span></span> | <span data-ttu-id="18141-141">值</span><span class="sxs-lookup"><span data-stu-id="18141-141">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="18141-142">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="18141-142">Minimum supported client</span></span><br/> | <span data-ttu-id="18141-143">都不支援</span><span class="sxs-lookup"><span data-stu-id="18141-143">None supported</span></span><br/>                                                                |
| <span data-ttu-id="18141-144">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="18141-144">Minimum supported server</span></span><br/> | <span data-ttu-id="18141-145">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="18141-145">Windows Server 2008</span></span><br/>                                                           |
| <span data-ttu-id="18141-146">命名空間</span><span class="sxs-lookup"><span data-stu-id="18141-146">Namespace</span></span><br/>                | <span data-ttu-id="18141-147">根 \\ CIMv2 \\ microsoft-windows-terminalservices-gateway</span><span class="sxs-lookup"><span data-stu-id="18141-147">Root\\CIMv2\\TerminalServices</span></span><br/>                                                 |
| <span data-ttu-id="18141-148">MOF</span><span class="sxs-lookup"><span data-stu-id="18141-148">MOF</span></span><br/>                      | <dl> <span data-ttu-id="18141-149"><dt>TSGateway mof</dt></span><span class="sxs-lookup"><span data-stu-id="18141-149"><dt>TSGateway.mof</dt></span></span> </dl> |
| <span data-ttu-id="18141-150">DLL</span><span class="sxs-lookup"><span data-stu-id="18141-150">DLL</span></span><br/>                      | <dl> <span data-ttu-id="18141-151"><dt>AagWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="18141-151"><dt>AagWmi.dll</dt></span></span> </dl>    |



## <a name="see-also"></a><span data-ttu-id="18141-152">另請參閱</span><span class="sxs-lookup"><span data-stu-id="18141-152">See also</span></span>

<dl> <dt>

[<span data-ttu-id="18141-153">**Win32 \_ TSGatewayServerSettings**</span><span class="sxs-lookup"><span data-stu-id="18141-153">**Win32\_TSGatewayServerSettings**</span></span>](win32-tsgatewayserversettings.md)
</dt> <dt>

[<span data-ttu-id="18141-154">**GetLogEventName**</span><span class="sxs-lookup"><span data-stu-id="18141-154">**GetLogEventName**</span></span>](getlogeventname-win32-tsgatewayserversettings.md)
</dt> </dl>

 

