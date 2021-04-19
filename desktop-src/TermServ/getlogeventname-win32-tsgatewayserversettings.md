---
title: Win32_TSGatewayServerSettings 類別的 GetLogEventName 方法
description: 傳回指定之記錄事件索引的記錄事件名稱。
ms.assetid: ca31ef8e-ab84-4132-a6d2-232b1e69230a
ms.tgt_platform: multiple
keywords:
- GetLogEventName 方法遠端桌面服務
- GetLogEventName 方法遠端桌面服務，Win32_TSGatewayServerSettings 類別
- Win32_TSGatewayServerSettings 類別遠端桌面服務，GetLogEventName 方法
topic_type:
- apiref
api_name:
- Win32_TSGatewayServerSettings.GetLogEventName
api_location:
- AagWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e3e9c608b7a12d3de48d75ecd5651df94d0267fc
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106976358"
---
# <a name="getlogeventname-method-of-the-win32_tsgatewayserversettings-class"></a><span data-ttu-id="c9945-106">Win32 TSGatewayServerSettings 類別的 GetLogEventName 方法 \_</span><span class="sxs-lookup"><span data-stu-id="c9945-106">GetLogEventName method of the Win32\_TSGatewayServerSettings class</span></span>

<span data-ttu-id="c9945-107">傳回指定之記錄事件索引的記錄事件名稱。</span><span class="sxs-lookup"><span data-stu-id="c9945-107">Returns the log event name for the specified log event index.</span></span>

## <a name="syntax"></a><span data-ttu-id="c9945-108">語法</span><span class="sxs-lookup"><span data-stu-id="c9945-108">Syntax</span></span>


```mof
uint32 GetLogEventName(
  [in]  uint32 EventIndex,
  [out] string EventName
);
```



## <a name="parameters"></a><span data-ttu-id="c9945-109">參數</span><span class="sxs-lookup"><span data-stu-id="c9945-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c9945-110">*EventIndex* \[在\]</span><span class="sxs-lookup"><span data-stu-id="c9945-110">*EventIndex* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c9945-111">記錄檔事件的索引。</span><span class="sxs-lookup"><span data-stu-id="c9945-111">Index of the log event.</span></span> <span data-ttu-id="c9945-112">值必須介於零到 **MaxLogEvents** 屬性的值之間。</span><span class="sxs-lookup"><span data-stu-id="c9945-112">The value must be between zero and the value of the **MaxLogEvents** property.</span></span>

</dd> <dt>

<span data-ttu-id="c9945-113">*事件名稱* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="c9945-113">*EventName* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="c9945-114">指定之事件的名稱。</span><span class="sxs-lookup"><span data-stu-id="c9945-114">Name of the specified event.</span></span> <span data-ttu-id="c9945-115">下列清單會顯示可能的值。</span><span class="sxs-lookup"><span data-stu-id="c9945-115">The following list displays the possible values.</span></span>

<dt>

<span id="LogChannelDisconnect"></span><span id="logchanneldisconnect"></span><span id="LOGCHANNELDISCONNECT"></span>

<span data-ttu-id="c9945-116"><span id="LogChannelDisconnect"></span><span id="logchanneldisconnect"></span><span id="LOGCHANNELDISCONNECT"></span>**LogChannelDisconnect**</span><span class="sxs-lookup"><span data-stu-id="c9945-116"><span id="LogChannelDisconnect"></span><span id="logchanneldisconnect"></span><span id="LOGCHANNELDISCONNECT"></span>**LogChannelDisconnect**</span></span>


</dt> <dd>

<span data-ttu-id="c9945-117">使用者已成功與資源中斷連線。</span><span class="sxs-lookup"><span data-stu-id="c9945-117">User successfully disconnected from the resource.</span></span>

</dd> <dt>

<span id="LogFailureChannelConnect"></span><span id="logfailurechannelconnect"></span><span id="LOGFAILURECHANNELCONNECT"></span>

<span data-ttu-id="c9945-118"><span id="LogFailureChannelConnect"></span><span id="logfailurechannelconnect"></span><span id="LOGFAILURECHANNELCONNECT"></span>**LogFailureChannelConnect**</span><span class="sxs-lookup"><span data-stu-id="c9945-118"><span id="LogFailureChannelConnect"></span><span id="logfailurechannelconnect"></span><span id="LOGFAILURECHANNELCONNECT"></span>**LogFailureChannelConnect**</span></span>


</dt> <dd>

<span data-ttu-id="c9945-119">使用者無法連線到資源。</span><span class="sxs-lookup"><span data-stu-id="c9945-119">User failed to connect to the resource.</span></span>

</dd> <dt>

<span id="LogFailureConnectionAuthorizationCheck"></span><span id="logfailureconnectionauthorizationcheck"></span><span id="LOGFAILURECONNECTIONAUTHORIZATIONCHECK"></span>

<span data-ttu-id="c9945-120"><span id="LogFailureConnectionAuthorizationCheck"></span><span id="logfailureconnectionauthorizationcheck"></span><span id="LOGFAILURECONNECTIONAUTHORIZATIONCHECK"></span>**LogFailureConnectionAuthorizationCheck**</span><span class="sxs-lookup"><span data-stu-id="c9945-120"><span id="LogFailureConnectionAuthorizationCheck"></span><span id="logfailureconnectionauthorizationcheck"></span><span id="LOGFAILURECONNECTIONAUTHORIZATIONCHECK"></span>**LogFailureConnectionAuthorizationCheck**</span></span>


</dt> <dd>

<span data-ttu-id="c9945-121">使用者連接授權失敗。</span><span class="sxs-lookup"><span data-stu-id="c9945-121">User failed connection authorization.</span></span>

</dd> <dt>

<span id="LogFailureResourceAuthorizationCheck"></span><span id="logfailureresourceauthorizationcheck"></span><span id="LOGFAILURERESOURCEAUTHORIZATIONCHECK"></span>

<span data-ttu-id="c9945-122"><span id="LogFailureResourceAuthorizationCheck"></span><span id="logfailureresourceauthorizationcheck"></span><span id="LOGFAILURERESOURCEAUTHORIZATIONCHECK"></span>**LogFailureResourceAuthorizationCheck**</span><span class="sxs-lookup"><span data-stu-id="c9945-122"><span id="LogFailureResourceAuthorizationCheck"></span><span id="logfailureresourceauthorizationcheck"></span><span id="LOGFAILURERESOURCEAUTHORIZATIONCHECK"></span>**LogFailureResourceAuthorizationCheck**</span></span>


</dt> <dd>

<span data-ttu-id="c9945-123">使用者失敗的資源授權。</span><span class="sxs-lookup"><span data-stu-id="c9945-123">User failed resource authorization.</span></span>

</dd> <dt>

<span id="LogSuccessfulChannelConnect"></span><span id="logsuccessfulchannelconnect"></span><span id="LOGSUCCESSFULCHANNELCONNECT"></span>

<span data-ttu-id="c9945-124"><span id="LogSuccessfulChannelConnect"></span><span id="logsuccessfulchannelconnect"></span><span id="LOGSUCCESSFULCHANNELCONNECT"></span>**LogSuccessfulChannelConnect**</span><span class="sxs-lookup"><span data-stu-id="c9945-124"><span id="LogSuccessfulChannelConnect"></span><span id="logsuccessfulchannelconnect"></span><span id="LOGSUCCESSFULCHANNELCONNECT"></span>**LogSuccessfulChannelConnect**</span></span>


</dt> <dd>

<span data-ttu-id="c9945-125">使用者已成功連線至資源。</span><span class="sxs-lookup"><span data-stu-id="c9945-125">User successfully connected to the resource.</span></span>

</dd> <dt>

<span id="LogSuccessfulConnectionAuthorizationCheck"></span><span id="logsuccessfulconnectionauthorizationcheck"></span><span id="LOGSUCCESSFULCONNECTIONAUTHORIZATIONCHECK"></span>

<span data-ttu-id="c9945-126"><span id="LogSuccessfulConnectionAuthorizationCheck"></span><span id="logsuccessfulconnectionauthorizationcheck"></span><span id="LOGSUCCESSFULCONNECTIONAUTHORIZATIONCHECK"></span>**LogSuccessfulConnectionAuthorizationCheck**</span><span class="sxs-lookup"><span data-stu-id="c9945-126"><span id="LogSuccessfulConnectionAuthorizationCheck"></span><span id="logsuccessfulconnectionauthorizationcheck"></span><span id="LOGSUCCESSFULCONNECTIONAUTHORIZATIONCHECK"></span>**LogSuccessfulConnectionAuthorizationCheck**</span></span>


</dt> <dd>

<span data-ttu-id="c9945-127">使用者成功傳遞連接授權。</span><span class="sxs-lookup"><span data-stu-id="c9945-127">User successfully passed connection authorization.</span></span>

</dd> <dt>

<span id="LogSuccessfulResourceAuthorizationCheck"></span><span id="logsuccessfulresourceauthorizationcheck"></span><span id="LOGSUCCESSFULRESOURCEAUTHORIZATIONCHECK"></span>

<span data-ttu-id="c9945-128"><span id="LogSuccessfulResourceAuthorizationCheck"></span><span id="logsuccessfulresourceauthorizationcheck"></span><span id="LOGSUCCESSFULRESOURCEAUTHORIZATIONCHECK"></span>**LogSuccessfulResourceAuthorizationCheck**</span><span class="sxs-lookup"><span data-stu-id="c9945-128"><span id="LogSuccessfulResourceAuthorizationCheck"></span><span id="logsuccessfulresourceauthorizationcheck"></span><span id="LOGSUCCESSFULRESOURCEAUTHORIZATIONCHECK"></span>**LogSuccessfulResourceAuthorizationCheck**</span></span>


</dt> <dd>

<span data-ttu-id="c9945-129">使用者已成功傳遞資源授權。</span><span class="sxs-lookup"><span data-stu-id="c9945-129">User successfully passed resource authorization.</span></span>

</dd> </dl> </dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c9945-130">傳回值</span><span class="sxs-lookup"><span data-stu-id="c9945-130">Return value</span></span>

<span data-ttu-id="c9945-131">如果方法成功，則會傳回零。</span><span class="sxs-lookup"><span data-stu-id="c9945-131">If the method succeeds, it returns zero.</span></span> <span data-ttu-id="c9945-132">如果方法失敗，則會傳回非零值。</span><span class="sxs-lookup"><span data-stu-id="c9945-132">If the method is unsuccessful, it returns a nonzero value.</span></span> <span data-ttu-id="c9945-133">如需錯誤碼清單，請參閱 [遠端桌面服務 WMI 提供者錯誤碼](terminal-services-wmi-provider-error-codes.md)。</span><span class="sxs-lookup"><span data-stu-id="c9945-133">For a list of error codes, see [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="c9945-134">備註</span><span class="sxs-lookup"><span data-stu-id="c9945-134">Remarks</span></span>

<span data-ttu-id="c9945-135">您必須是 Administrators 群組的成員，才能呼叫這個方法。</span><span class="sxs-lookup"><span data-stu-id="c9945-135">You must be a member of the Administrators group to call this method.</span></span>

<span data-ttu-id="c9945-136">受控物件格式 (MOF) 檔包含 Windows Management Instrumentation (WMI) 類別的定義。</span><span class="sxs-lookup"><span data-stu-id="c9945-136">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="c9945-137">MOF 檔案不會安裝為 Microsoft Windows 軟體開發套件 (SDK) 的一部分。</span><span class="sxs-lookup"><span data-stu-id="c9945-137">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="c9945-138">當您使用伺服器管理員新增相關聯的角色時，它們會安裝在伺服器上。</span><span class="sxs-lookup"><span data-stu-id="c9945-138">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="c9945-139">如需 MOF 檔案的詳細資訊，請參閱 [受控物件格式 (mof) ](/windows/desktop/WmiSdk/managed-object-format--mof-)。</span><span class="sxs-lookup"><span data-stu-id="c9945-139">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="c9945-140">規格需求</span><span class="sxs-lookup"><span data-stu-id="c9945-140">Requirements</span></span>



| <span data-ttu-id="c9945-141">需求</span><span class="sxs-lookup"><span data-stu-id="c9945-141">Requirement</span></span> | <span data-ttu-id="c9945-142">值</span><span class="sxs-lookup"><span data-stu-id="c9945-142">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="c9945-143">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="c9945-143">Minimum supported client</span></span><br/> | <span data-ttu-id="c9945-144">都不支援</span><span class="sxs-lookup"><span data-stu-id="c9945-144">None supported</span></span><br/>                                                                |
| <span data-ttu-id="c9945-145">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="c9945-145">Minimum supported server</span></span><br/> | <span data-ttu-id="c9945-146">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="c9945-146">Windows Server 2008</span></span><br/>                                                           |
| <span data-ttu-id="c9945-147">命名空間</span><span class="sxs-lookup"><span data-stu-id="c9945-147">Namespace</span></span><br/>                | <span data-ttu-id="c9945-148">根 \\ CIMv2 \\ microsoft-windows-terminalservices-gateway</span><span class="sxs-lookup"><span data-stu-id="c9945-148">Root\\CIMv2\\TerminalServices</span></span><br/>                                                 |
| <span data-ttu-id="c9945-149">MOF</span><span class="sxs-lookup"><span data-stu-id="c9945-149">MOF</span></span><br/>                      | <dl> <span data-ttu-id="c9945-150"><dt>TSGateway mof</dt></span><span class="sxs-lookup"><span data-stu-id="c9945-150"><dt>TSGateway.mof</dt></span></span> </dl> |
| <span data-ttu-id="c9945-151">DLL</span><span class="sxs-lookup"><span data-stu-id="c9945-151">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c9945-152"><dt>AagWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c9945-152"><dt>AagWmi.dll</dt></span></span> </dl>    |



## <a name="see-also"></a><span data-ttu-id="c9945-153">另請參閱</span><span class="sxs-lookup"><span data-stu-id="c9945-153">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c9945-154">**Win32 \_ TSGatewayServerSettings**</span><span class="sxs-lookup"><span data-stu-id="c9945-154">**Win32\_TSGatewayServerSettings**</span></span>](win32-tsgatewayserversettings.md)
</dt> <dt>

[<span data-ttu-id="c9945-155">**EnableLogEvent**</span><span class="sxs-lookup"><span data-stu-id="c9945-155">**EnableLogEvent**</span></span>](enablelogevent-win32-tsgatewayserversettings.md)
</dt> <dt>

[<span data-ttu-id="c9945-156">**IsLogEventEnabled**</span><span class="sxs-lookup"><span data-stu-id="c9945-156">**IsLogEventEnabled**</span></span>](islogeventenabled-win32-tsgatewayserversettings.md)
</dt> </dl>

 

