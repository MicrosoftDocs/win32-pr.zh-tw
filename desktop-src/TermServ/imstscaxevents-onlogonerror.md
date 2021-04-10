---
title: IMsTscAxEvents OnLogonError 方法
description: 發生登入錯誤或其他登入事件時呼叫。
ms.assetid: 5af9656b-f99b-4535-ab83-6ecc9bc41808
ms.tgt_platform: multiple
keywords:
- OnLogonError 方法遠端桌面服務
- OnLogonError 方法遠端桌面服務，IMsTscAxEvents 介面
- IMsTscAxEvents 介面遠端桌面服務，OnLogonError 方法
topic_type:
- apiref
api_name:
- IMsTscAxEvents.OnLogonError
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f45fe23c992f14a421c00a4feefd9c4ed95aff07
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103686062"
---
# <a name="imstscaxeventsonlogonerror-method"></a><span data-ttu-id="0a9ac-106">IMsTscAxEvents：： OnLogonError 方法</span><span class="sxs-lookup"><span data-stu-id="0a9ac-106">IMsTscAxEvents::OnLogonError method</span></span>

<span data-ttu-id="0a9ac-107">發生登入錯誤或其他登入事件時呼叫。</span><span class="sxs-lookup"><span data-stu-id="0a9ac-107">Called when a logon error or other logon event occurs.</span></span>

## <a name="syntax"></a><span data-ttu-id="0a9ac-108">語法</span><span class="sxs-lookup"><span data-stu-id="0a9ac-108">Syntax</span></span>


```C++
void OnLogonError(
  [in] LONG lError
);
```



## <a name="parameters"></a><span data-ttu-id="0a9ac-109">參數</span><span class="sxs-lookup"><span data-stu-id="0a9ac-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0a9ac-110">*lError* \[在\]</span><span class="sxs-lookup"><span data-stu-id="0a9ac-110">*lError* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0a9ac-111">登入錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="0a9ac-111">The logon error code.</span></span> <span data-ttu-id="0a9ac-112">這份程式代碼清單並不詳盡。</span><span class="sxs-lookup"><span data-stu-id="0a9ac-112">This list of codes is not exhaustive.</span></span>

<dt>

<span id="ARBITRATION_CODE_BUMP_OPTIONS"></span><span id="arbitration_code_bump_options"></span>

<span data-ttu-id="0a9ac-113"><span id="ARBITRATION_CODE_BUMP_OPTIONS"></span><span id="arbitration_code_bump_options"></span>**仲裁 \_程式碼的 \_ \_ 選項** (-5 (0xFFFFFFFB) ) </span><span class="sxs-lookup"><span data-stu-id="0a9ac-113"><span id="ARBITRATION_CODE_BUMP_OPTIONS"></span><span id="arbitration_code_bump_options"></span>**ARBITRATION\_CODE\_BUMP\_OPTIONS** (-5 (0xFFFFFFFB))</span></span>


</dt> <dd>

<span data-ttu-id="0a9ac-114">Winlogon 正在顯示 **會話競爭** 對話方塊。</span><span class="sxs-lookup"><span data-stu-id="0a9ac-114">Winlogon is displaying the **Session Contention** dialog box.</span></span>

</dd> <dt>

<span id="ARBITRATION_CODE_CONTINUE_LOGON"></span><span id="arbitration_code_continue_logon"></span>

<span data-ttu-id="0a9ac-115"><span id="ARBITRATION_CODE_CONTINUE_LOGON"></span><span id="arbitration_code_continue_logon"></span>**仲裁 \_程式碼 \_ 繼續 \_ 登** 入 (-2 (0xFFFFFFFE) ) </span><span class="sxs-lookup"><span data-stu-id="0a9ac-115"><span id="ARBITRATION_CODE_CONTINUE_LOGON"></span><span id="arbitration_code_continue_logon"></span>**ARBITRATION\_CODE\_CONTINUE\_LOGON** (-2 (0xFFFFFFFE))</span></span>


</dt> <dd>

<span data-ttu-id="0a9ac-116">Winlogon 正在繼續進行登入程式。</span><span class="sxs-lookup"><span data-stu-id="0a9ac-116">Winlogon is continuing with the logon process.</span></span>

</dd> <dt>

<span id="ARBITRATION_CODE_CONTINUE_TERMINATE"></span><span id="arbitration_code_continue_terminate"></span>

<span data-ttu-id="0a9ac-117"><span id="ARBITRATION_CODE_CONTINUE_TERMINATE"></span><span id="arbitration_code_continue_terminate"></span>**仲裁 \_程式碼 \_ 繼續 \_ 終止** (-3 (0xFFFFFFFD) ) </span><span class="sxs-lookup"><span data-stu-id="0a9ac-117"><span id="ARBITRATION_CODE_CONTINUE_TERMINATE"></span><span id="arbitration_code_continue_terminate"></span>**ARBITRATION\_CODE\_CONTINUE\_TERMINATE** (-3 (0xFFFFFFFD))</span></span>


</dt> <dd>

<span data-ttu-id="0a9ac-118">Winlogon 以無訊息方式結束。</span><span class="sxs-lookup"><span data-stu-id="0a9ac-118">Winlogon is ending silently.</span></span>

</dd> <dt>

<span id="ARBITRATION_CODE_NOPERM_DIALOG"></span><span id="arbitration_code_noperm_dialog"></span>

<span data-ttu-id="0a9ac-119"><span id="ARBITRATION_CODE_NOPERM_DIALOG"></span><span id="arbitration_code_noperm_dialog"></span>**仲裁 \_程式碼 \_ NOPERM \_ 對話方塊** (-6 (0xFFFFFFFA) ) </span><span class="sxs-lookup"><span data-stu-id="0a9ac-119"><span id="ARBITRATION_CODE_NOPERM_DIALOG"></span><span id="arbitration_code_noperm_dialog"></span>**ARBITRATION\_CODE\_NOPERM\_DIALOG** (-6 (0xFFFFFFFA))</span></span>


</dt> <dd>

<span data-ttu-id="0a9ac-120">Winlogon 正在顯示 [ **無許可權** ] 對話方塊。</span><span class="sxs-lookup"><span data-stu-id="0a9ac-120">Winlogon is displaying the **No Permissions** dialog box.</span></span>

</dd> <dt>

<span id="ARBITRATION_CODE_REFUSED_DIALOG"></span><span id="arbitration_code_refused_dialog"></span>

<span data-ttu-id="0a9ac-121"><span id="ARBITRATION_CODE_REFUSED_DIALOG"></span><span id="arbitration_code_refused_dialog"></span>**仲裁 \_程式碼 \_ 拒絕 \_ 對話方塊** (-7 (0xFFFFFFF9) ) </span><span class="sxs-lookup"><span data-stu-id="0a9ac-121"><span id="ARBITRATION_CODE_REFUSED_DIALOG"></span><span id="arbitration_code_refused_dialog"></span>**ARBITRATION\_CODE\_REFUSED\_DIALOG** (-7 (0xFFFFFFF9))</span></span>


</dt> <dd>

<span data-ttu-id="0a9ac-122">Winlogon 顯示 [ **拒絕中斷** 連線] 對話方塊。</span><span class="sxs-lookup"><span data-stu-id="0a9ac-122">Winlogon is displaying the **Disconnect Refused** dialog box.</span></span>

</dd> <dt>

<span id="ARBITRATION_CODE_RECONN_OPTIONS"></span><span id="arbitration_code_reconn_options"></span>

<span data-ttu-id="0a9ac-123"><span id="ARBITRATION_CODE_RECONN_OPTIONS"></span><span id="arbitration_code_reconn_options"></span>**仲裁 \_程式碼 \_ RECONN \_ 選項** (-4 (0xFFFFFFFC) ) </span><span class="sxs-lookup"><span data-stu-id="0a9ac-123"><span id="ARBITRATION_CODE_RECONN_OPTIONS"></span><span id="arbitration_code_reconn_options"></span>**ARBITRATION\_CODE\_RECONN\_OPTIONS** (-4 (0xFFFFFFFC))</span></span>


</dt> <dd>

<span data-ttu-id="0a9ac-124">Winlogon 正在顯示 [ **重新連接** ] 對話方塊。</span><span class="sxs-lookup"><span data-stu-id="0a9ac-124">Winlogon is displaying the **Reconnect** dialog box.</span></span>

</dd> <dt>

<span id="ERROR_CODE_ACCESS_DENIED"></span><span id="error_code_access_denied"></span>

<span data-ttu-id="0a9ac-125"><span id="ERROR_CODE_ACCESS_DENIED"></span><span id="error_code_access_denied"></span>**錯誤 \_\_ \_ 拒絕程式碼存取** (-1 (0xffffffff) ) </span><span class="sxs-lookup"><span data-stu-id="0a9ac-125"><span id="ERROR_CODE_ACCESS_DENIED"></span><span id="error_code_access_denied"></span>**ERROR\_CODE\_ACCESS\_DENIED** (-1 (0xFFFFFFFF))</span></span>


</dt> <dd>

<span data-ttu-id="0a9ac-126">使用者被拒絕存取。</span><span class="sxs-lookup"><span data-stu-id="0a9ac-126">The user was denied access.</span></span>

</dd> <dt>

<span id="LOGON_FAILED_BAD_PASSWORD"></span><span id="logon_failed_bad_password"></span>

<span data-ttu-id="0a9ac-127"><span id="LOGON_FAILED_BAD_PASSWORD"></span><span id="logon_failed_bad_password"></span>**登 \_ 入失敗 \_ 的 \_ 密碼錯誤** (0 (0x0) ) </span><span class="sxs-lookup"><span data-stu-id="0a9ac-127"><span id="LOGON_FAILED_BAD_PASSWORD"></span><span id="logon_failed_bad_password"></span>**LOGON\_FAILED\_BAD\_PASSWORD** (0 (0x0))</span></span>


</dt> <dd>

<span data-ttu-id="0a9ac-128">登入失敗，因為登入認證無效。</span><span class="sxs-lookup"><span data-stu-id="0a9ac-128">The logon failed because the logon credentials are not valid.</span></span>

</dd> <dt>

<span id="LOGON_FAILED_OTHER"></span><span id="logon_failed_other"></span>

<span data-ttu-id="0a9ac-129"><span id="LOGON_FAILED_OTHER"></span><span id="logon_failed_other"></span>**登 \_ 入失敗的 \_ 其他** (2 (0x2) ) </span><span class="sxs-lookup"><span data-stu-id="0a9ac-129"><span id="LOGON_FAILED_OTHER"></span><span id="logon_failed_other"></span>**LOGON\_FAILED\_OTHER** (2 (0x2))</span></span>


</dt> <dd>

<span data-ttu-id="0a9ac-130">發生另一個登入或後置登入錯誤。</span><span class="sxs-lookup"><span data-stu-id="0a9ac-130">Another logon or post-logon error occurred.</span></span> <span data-ttu-id="0a9ac-131">遠端桌面用戶端會向使用者顯示登入畫面。</span><span class="sxs-lookup"><span data-stu-id="0a9ac-131">The Remote Desktop client displays a logon screen to the user.</span></span>

</dd> <dt>

<span id="LOGON_FAILED_UPDATE_PASSWORD"></span><span id="logon_failed_update_password"></span>

<span data-ttu-id="0a9ac-132"><span id="LOGON_FAILED_UPDATE_PASSWORD"></span><span id="logon_failed_update_password"></span>**登 \_ 入無法 \_ 更新 \_ 密碼** (1 (0x1) ) </span><span class="sxs-lookup"><span data-stu-id="0a9ac-132"><span id="LOGON_FAILED_UPDATE_PASSWORD"></span><span id="logon_failed_update_password"></span>**LOGON\_FAILED\_UPDATE\_PASSWORD** (1 (0x1))</span></span>


</dt> <dd>

<span data-ttu-id="0a9ac-133">密碼已過期。</span><span class="sxs-lookup"><span data-stu-id="0a9ac-133">The password is expired.</span></span> <span data-ttu-id="0a9ac-134">使用者必須更新其密碼，才能繼續登入。</span><span class="sxs-lookup"><span data-stu-id="0a9ac-134">The user must update their password to continue logging on.</span></span>

</dd> <dt>

<span id="LOGON_WARNING"></span><span id="logon_warning"></span>

<span data-ttu-id="0a9ac-135"><span id="LOGON_WARNING"></span><span id="logon_warning"></span>**登 \_ 入警告** (3 (0x3) ) </span><span class="sxs-lookup"><span data-stu-id="0a9ac-135"><span id="LOGON_WARNING"></span><span id="logon_warning"></span>**LOGON\_WARNING** (3 (0x3))</span></span>


</dt> <dd>

<span data-ttu-id="0a9ac-136">遠端桌面用戶端會顯示一個對話方塊，其中包含使用者的重要資訊。</span><span class="sxs-lookup"><span data-stu-id="0a9ac-136">The Remote Desktop client displays a dialog box that contains important information for the user.</span></span>

</dd> <dt>

<span id="STATUS_ACCOUNT_RESTRICTION"></span><span id="status_account_restriction"></span>

<span data-ttu-id="0a9ac-137"><span id="STATUS_ACCOUNT_RESTRICTION"></span><span id="status_account_restriction"></span>**狀態 \_帳戶 \_ 限制** (-1073741714 (0xC000006E) ) </span><span class="sxs-lookup"><span data-stu-id="0a9ac-137"><span id="STATUS_ACCOUNT_RESTRICTION"></span><span id="status_account_restriction"></span>**STATUS\_ACCOUNT\_RESTRICTION** (-1073741714 (0xC000006E))</span></span>


</dt> <dd>

<span data-ttu-id="0a9ac-138">使用者名稱和驗證資訊是有效的，但因為使用者帳戶的限制，而導致驗證遭到封鎖，例如時間限制。</span><span class="sxs-lookup"><span data-stu-id="0a9ac-138">The user name and authentication information are valid, but authentication was blocked due to restrictions on the user account, such as time-of-day restrictions.</span></span>

</dd> <dt>

<span id="STATUS_LOGON_FAILURE"></span><span id="status_logon_failure"></span>

<span data-ttu-id="0a9ac-139"><span id="STATUS_LOGON_FAILURE"></span><span id="status_logon_failure"></span>**狀態 \_登入 \_ 失敗** (-1073741715 (0xC000006D) ) </span><span class="sxs-lookup"><span data-stu-id="0a9ac-139"><span id="STATUS_LOGON_FAILURE"></span><span id="status_logon_failure"></span>**STATUS\_LOGON\_FAILURE** (-1073741715 (0xC000006D))</span></span>


</dt> <dd>

<span data-ttu-id="0a9ac-140">嘗試的登入無效。</span><span class="sxs-lookup"><span data-stu-id="0a9ac-140">The attempted logon is not valid.</span></span> <span data-ttu-id="0a9ac-141">這是因為使用者名稱不正確或驗證資訊不正確。</span><span class="sxs-lookup"><span data-stu-id="0a9ac-141">This is due to either an incorrect user name or incorrect authentication information.</span></span>

</dd> <dt>

<span id="STATUS_PASSWORD_MUST_CHANGE"></span><span id="status_password_must_change"></span>

<span data-ttu-id="0a9ac-142"><span id="STATUS_PASSWORD_MUST_CHANGE"></span><span id="status_password_must_change"></span>**狀態 \_密碼 \_ 必須 \_ 變更** (-1073741276 (0xC0000224) ) </span><span class="sxs-lookup"><span data-stu-id="0a9ac-142"><span id="STATUS_PASSWORD_MUST_CHANGE"></span><span id="status_password_must_change"></span>**STATUS\_PASSWORD\_MUST\_CHANGE** (-1073741276 (0xC0000224))</span></span>


</dt> <dd>

<span data-ttu-id="0a9ac-143">密碼已過期。</span><span class="sxs-lookup"><span data-stu-id="0a9ac-143">The password is expired.</span></span> <span data-ttu-id="0a9ac-144">使用者必須更新其密碼，才能繼續登入。</span><span class="sxs-lookup"><span data-stu-id="0a9ac-144">The user must update their password to continue logging on.</span></span>

</dd> </dl> </dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0a9ac-145">傳回值</span><span class="sxs-lookup"><span data-stu-id="0a9ac-145">Return value</span></span>

<span data-ttu-id="0a9ac-146">這個方法不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="0a9ac-146">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="0a9ac-147">備註</span><span class="sxs-lookup"><span data-stu-id="0a9ac-147">Remarks</span></span>

<span data-ttu-id="0a9ac-148">在事件接收中執行此方法，以接收已發生登入錯誤的通知。</span><span class="sxs-lookup"><span data-stu-id="0a9ac-148">Implement this method in your event sink to receive notification that a logon error has occurred.</span></span>

<span data-ttu-id="0a9ac-149">這份程式代碼清單並不詳盡。</span><span class="sxs-lookup"><span data-stu-id="0a9ac-149">This list of codes is not exhaustive.</span></span>

## <a name="requirements"></a><span data-ttu-id="0a9ac-150">規格需求</span><span class="sxs-lookup"><span data-stu-id="0a9ac-150">Requirements</span></span>



| <span data-ttu-id="0a9ac-151">需求</span><span class="sxs-lookup"><span data-stu-id="0a9ac-151">Requirement</span></span> | <span data-ttu-id="0a9ac-152">值</span><span class="sxs-lookup"><span data-stu-id="0a9ac-152">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="0a9ac-153">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="0a9ac-153">Minimum supported client</span></span><br/> | <span data-ttu-id="0a9ac-154">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="0a9ac-154">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="0a9ac-155">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="0a9ac-155">Minimum supported server</span></span><br/> | <span data-ttu-id="0a9ac-156">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="0a9ac-156">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="0a9ac-157">類型程式庫</span><span class="sxs-lookup"><span data-stu-id="0a9ac-157">Type library</span></span><br/>             | <dl> <span data-ttu-id="0a9ac-158"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0a9ac-158"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="0a9ac-159">DLL</span><span class="sxs-lookup"><span data-stu-id="0a9ac-159">DLL</span></span><br/>                      | <dl> <span data-ttu-id="0a9ac-160"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0a9ac-160"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="0a9ac-161">IID</span><span class="sxs-lookup"><span data-stu-id="0a9ac-161">IID</span></span><br/>                      | <span data-ttu-id="0a9ac-162">IMsTscAxEvents 定義為336d5562-efa8-482e-8cb3-c5c0fc7a7db6</span><span class="sxs-lookup"><span data-stu-id="0a9ac-162">IMsTscAxEvents is defined as 336d5562-efa8-482e-8cb3-c5c0fc7a7db6</span></span><br/>           |



## <a name="see-also"></a><span data-ttu-id="0a9ac-163">另請參閱</span><span class="sxs-lookup"><span data-stu-id="0a9ac-163">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0a9ac-164">**IMsTscAxEvents**</span><span class="sxs-lookup"><span data-stu-id="0a9ac-164">**IMsTscAxEvents**</span></span>](imstscaxevents-interface.md)
</dt> </dl>

 

 





