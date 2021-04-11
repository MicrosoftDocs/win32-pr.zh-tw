---
title: 驗證通訊協定登錄值
description: EAP DLL 的安裝軟體可能會在 eaptypeid 底下建立下列登錄值。
ms.assetid: a5f6674d-77c8-4b88-af0e-bb62f84d8a2b
keywords:
- RAS_EAP_VALUENAME_PATH
- RAS_EAP_VALUENAME_FRIENDLY_NAME
- RAS_EAP_VALUENAME_CONFIGUI
- RAS_EAP_VALUENAME_DEFAULT_DATA
- RAS_EAP_VALUENAME_REQUIRE_CONFIGUI
- RAS_EAP_VALUENAME_CONFIG_CLSID
- RAS_EAP_VALUENAME_IDENTITY
- RAS_EAP_VALUENAME_INTERACTIVEUI
- RAS_EAP_VALUENAME_INVOKE_NAMEDLG
- RAS_EAP_VALUENAME_INVOKE_PWDDLG
- RAS_EAP_VALUENAME_ENCRYPTION
- RAS_EAP_VALUENAME_STANDALONE_SUPPORTED
- RAS_EAP_VALUENAME_ROLES_SUPPORTED
- RAS_EAP_VALUENAME_PER_POLICY_CONFIG
- RAS_EAP_VALUENAME_ISTUNNEL_METHOD
- RAS_EAP_VALUENAME_FILTER_INNERMETHODS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8091197c7b0d5c5a208bf3658bbc15284a29ac9e
ms.sourcegitcommit: c20a43b333f03175ac23823c55f3204bfe8cd243
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 11/26/2019
ms.locfileid: "104022888"
---
# <a name="authentication-protocol-registry-values"></a><span data-ttu-id="4fd63-119">驗證通訊協定登錄值</span><span class="sxs-lookup"><span data-stu-id="4fd63-119">Authentication Protocol Registry Values</span></span>

<span data-ttu-id="4fd63-120">EAP DLL 的安裝軟體可能會在 **&lt; eaptypeid &gt;** 底下建立下列登錄值。</span><span class="sxs-lookup"><span data-stu-id="4fd63-120">The setup software for the EAP DLL may create the following registry values below **&lt;eaptypeid&gt;**.</span></span> <span data-ttu-id="4fd63-121">這些登錄值定義于 Raseapif .h 標頭檔中。</span><span class="sxs-lookup"><span data-stu-id="4fd63-121">These registry values are defined in the Raseapif.h header file.</span></span> <span data-ttu-id="4fd63-122">需要 **RAS_EAP_VALUENAME_PATH** 和 **RAS_EAP_VALUENAME_FRIENDLY_NAME** 值。</span><span class="sxs-lookup"><span data-stu-id="4fd63-122">The **RAS_EAP_VALUENAME_PATH** and **RAS_EAP_VALUENAME_FRIENDLY_NAME** values are required.</span></span> <span data-ttu-id="4fd63-123">安裝軟體也可以建立其他金鑰和值。</span><span class="sxs-lookup"><span data-stu-id="4fd63-123">The setup software may create other keys and values as well.</span></span> <span data-ttu-id="4fd63-124">驗證通訊協定本身可以使用這些方法。</span><span class="sxs-lookup"><span data-stu-id="4fd63-124">These could be used by the authentication protocol itself.</span></span> <span data-ttu-id="4fd63-125">如需登錄設定的詳細資訊和範例，請參閱登錄 [值範例](registry-values-example.md)。</span><span class="sxs-lookup"><span data-stu-id="4fd63-125">For more information and an example of registry configuration, see [Registry Values Example](registry-values-example.md).</span></span>

[<span data-ttu-id="4fd63-126">RAS_EAP_VALUENAME_PATH</span><span class="sxs-lookup"><span data-stu-id="4fd63-126">RAS_EAP_VALUENAME_PATH</span></span>](#ras_eap_valuename_path)

[<span data-ttu-id="4fd63-127">RAS_EAP_VALUENAME_FRIENDLY_NAME</span><span class="sxs-lookup"><span data-stu-id="4fd63-127">RAS_EAP_VALUENAME_FRIENDLY_NAME</span></span>](#ras_eap_valuename_friendly_name)

[<span data-ttu-id="4fd63-128">RAS_EAP_VALUENAME_CONFIGUI</span><span class="sxs-lookup"><span data-stu-id="4fd63-128">RAS_EAP_VALUENAME_CONFIGUI</span></span>](#ras_eap_valuename_configui)

[<span data-ttu-id="4fd63-129">RAS_EAP_VALUENAME_DEFAULT_DATA</span><span class="sxs-lookup"><span data-stu-id="4fd63-129">RAS_EAP_VALUENAME_DEFAULT_DATA</span></span>](#ras_eap_valuename_default_data)

[<span data-ttu-id="4fd63-130">RAS_EAP_VALUENAME_REQUIRE_CONFIGUI</span><span class="sxs-lookup"><span data-stu-id="4fd63-130">RAS_EAP_VALUENAME_REQUIRE_CONFIGUI</span></span>](#ras_eap_valuename_require_configui)

[<span data-ttu-id="4fd63-131">RAS_EAP_VALUENAME_CONFIG_CLSID</span><span class="sxs-lookup"><span data-stu-id="4fd63-131">RAS_EAP_VALUENAME_CONFIG_CLSID</span></span>](#ras_eap_valuename_config_clsid)

[<span data-ttu-id="4fd63-132">RAS_EAP_VALUENAME_IDENTITY</span><span class="sxs-lookup"><span data-stu-id="4fd63-132">RAS_EAP_VALUENAME_IDENTITY</span></span>](#ras_eap_valuename_identity)

<span data-ttu-id="4fd63-133">[RAS_EAP_VALUENAME_INTERACTIVEUI](#ras_eap_valuename_interactiveui)我</span><span class="sxs-lookup"><span data-stu-id="4fd63-133">[RAS_EAP_VALUENAME_INTERACTIVEUI](#ras_eap_valuename_interactiveui)I</span></span>

[<span data-ttu-id="4fd63-134">RAS_EAP_VALUENAME_INVOKE_NAMEDLG</span><span class="sxs-lookup"><span data-stu-id="4fd63-134">RAS_EAP_VALUENAME_INVOKE_NAMEDLG</span></span>](#ras_eap_valuename_invoke_namedlg)

[<span data-ttu-id="4fd63-135">RAS_EAP_VALUENAME_INVOKE_PWDDLG</span><span class="sxs-lookup"><span data-stu-id="4fd63-135">RAS_EAP_VALUENAME_INVOKE_PWDDLG</span></span>](#ras_eap_valuename_invoke_pwddlg)

[<span data-ttu-id="4fd63-136">RAS_EAP_VALUENAME_ENCRYPTION</span><span class="sxs-lookup"><span data-stu-id="4fd63-136">RAS_EAP_VALUENAME_ENCRYPTION</span></span>](#ras_eap_valuename_encryption)

[<span data-ttu-id="4fd63-137">RAS_EAP_VALUENAME_STANDALONE_SUPPORTED</span><span class="sxs-lookup"><span data-stu-id="4fd63-137">RAS_EAP_VALUENAME_STANDALONE_SUPPORTED</span></span>](#ras_eap_valuename_standalone_supported)

[<span data-ttu-id="4fd63-138">RAS_EAP_VALUENAME_ROLES_SUPPORTED</span><span class="sxs-lookup"><span data-stu-id="4fd63-138">RAS_EAP_VALUENAME_ROLES_SUPPORTED</span></span>](#ras_eap_valuename_roles_supported)

[<span data-ttu-id="4fd63-139">RAS_EAP_VALUENAME_PER_POLICY_CONFIG</span><span class="sxs-lookup"><span data-stu-id="4fd63-139">RAS_EAP_VALUENAME_PER_POLICY_CONFIG</span></span>](#ras_eap_valuename_per_policy_config)

[<span data-ttu-id="4fd63-140">RAS_EAP_VALUENAME_ISTUNNEL_METHOD</span><span class="sxs-lookup"><span data-stu-id="4fd63-140">RAS_EAP_VALUENAME_ISTUNNEL_METHOD</span></span>](#ras_eap_valuename_istunnel_method)

[<span data-ttu-id="4fd63-141">RAS_EAP_VALUENAME_FILTER_INNERMETHODS</span><span class="sxs-lookup"><span data-stu-id="4fd63-141">RAS_EAP_VALUENAME_FILTER_INNERMETHODS</span></span>](#ras_eap_valuename_filter_innermethods)

## <a name="ras_eap_valuename_path"></a><span data-ttu-id="4fd63-142">RAS_EAP_VALUENAME_PATH</span><span class="sxs-lookup"><span data-stu-id="4fd63-142">RAS_EAP_VALUENAME_PATH</span></span>

| <span data-ttu-id="4fd63-143">常數值</span><span class="sxs-lookup"><span data-stu-id="4fd63-143">Constant value</span></span> | <span data-ttu-id="4fd63-144">路徑</span><span class="sxs-lookup"><span data-stu-id="4fd63-144">Path</span></span>                               |
|----------------|------------------------------------|
| <span data-ttu-id="4fd63-145">類型</span><span class="sxs-lookup"><span data-stu-id="4fd63-145">Type</span></span>           | <span data-ttu-id="4fd63-146"> REG_EXPAND_SZ </span><span class="sxs-lookup"><span data-stu-id="4fd63-146">REG_EXPAND_SZ</span></span>                    |
| <span data-ttu-id="4fd63-147">Description</span><span class="sxs-lookup"><span data-stu-id="4fd63-147">Description</span></span>    | <span data-ttu-id="4fd63-148">指定 EAP DLL 的路徑。</span><span class="sxs-lookup"><span data-stu-id="4fd63-148">Specifies the path to the EAP DLL.</span></span> |

## <a name="ras_eap_valuename_friendly_name"></a><span data-ttu-id="4fd63-149">RAS_EAP_VALUENAME_FRIENDLY_NAME</span><span class="sxs-lookup"><span data-stu-id="4fd63-149">RAS_EAP_VALUENAME_FRIENDLY_NAME</span></span>

| <span data-ttu-id="4fd63-150">常數值</span><span class="sxs-lookup"><span data-stu-id="4fd63-150">Constant value</span></span> | <span data-ttu-id="4fd63-151">FriendlyName</span><span class="sxs-lookup"><span data-stu-id="4fd63-151">FriendlyName</span></span>                                                                                                                                                      |
|----------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4fd63-152">類型</span><span class="sxs-lookup"><span data-stu-id="4fd63-152">Type</span></span>           | <span data-ttu-id="4fd63-153">REG_SZ</span><span class="sxs-lookup"><span data-stu-id="4fd63-153">REG_SZ</span></span>                                                                                                                                                           |
| <span data-ttu-id="4fd63-154">Description</span><span class="sxs-lookup"><span data-stu-id="4fd63-154">Description</span></span>    | <span data-ttu-id="4fd63-155">指定驗證通訊協定的易記名稱。</span><span class="sxs-lookup"><span data-stu-id="4fd63-155">Specifies a friendly name for the authentication protocol.</span></span> <span data-ttu-id="4fd63-156">這個名稱會出現在 EAP 應用程式使用者介面中，以供撥號和無線執行。</span><span class="sxs-lookup"><span data-stu-id="4fd63-156">This name appears in the EAP application user interface for both dial-up and wireless implementations.</span></span> |

## <a name="ras_eap_valuename_configui"></a><span data-ttu-id="4fd63-157">RAS_EAP_VALUENAME_CONFIGUI</span><span class="sxs-lookup"><span data-stu-id="4fd63-157">RAS_EAP_VALUENAME_CONFIGUI</span></span>

| <span data-ttu-id="4fd63-158">常數值</span><span class="sxs-lookup"><span data-stu-id="4fd63-158">Constant value</span></span> | <span data-ttu-id="4fd63-159">ConfigUIPath</span><span class="sxs-lookup"><span data-stu-id="4fd63-159">ConfigUIPath</span></span>                                                                                                                      |
|----------------|-----------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4fd63-160">類型</span><span class="sxs-lookup"><span data-stu-id="4fd63-160">Type</span></span>           | <span data-ttu-id="4fd63-161"> REG_EXPAND_SZ </span><span class="sxs-lookup"><span data-stu-id="4fd63-161">REG_EXPAND_SZ</span></span>                                                                                                                   |
| <span data-ttu-id="4fd63-162">Description</span><span class="sxs-lookup"><span data-stu-id="4fd63-162">Description</span></span>    | <span data-ttu-id="4fd63-163">指定在用戶端上執行設定使用者介面之 DLL 的路徑，因為此 UI 僅供用戶端使用。</span><span class="sxs-lookup"><span data-stu-id="4fd63-163">Specifies the path to the DLL that implements the configuration user interface on the client, because this UI is for client only.</span></span> |

## <a name="ras_eap_valuename_default_data"></a><span data-ttu-id="4fd63-164">RAS_EAP_VALUENAME_DEFAULT_DATA</span><span class="sxs-lookup"><span data-stu-id="4fd63-164">RAS_EAP_VALUENAME_DEFAULT_DATA</span></span>

| <span data-ttu-id="4fd63-165">常數值</span><span class="sxs-lookup"><span data-stu-id="4fd63-165">Constant value</span></span> | <span data-ttu-id="4fd63-166">ConfigData</span><span class="sxs-lookup"><span data-stu-id="4fd63-166">ConfigData</span></span>                                                            |
|----------------|-----------------------------------------------------------------------|
| <span data-ttu-id="4fd63-167">類型</span><span class="sxs-lookup"><span data-stu-id="4fd63-167">Type</span></span>           | <span data-ttu-id="4fd63-168">REG_BINARY</span><span class="sxs-lookup"><span data-stu-id="4fd63-168">REG_BINARY</span></span>                                                           |
| <span data-ttu-id="4fd63-169">Description</span><span class="sxs-lookup"><span data-stu-id="4fd63-169">Description</span></span>    | <span data-ttu-id="4fd63-170">指定驗證通訊協定的預設設定資料。</span><span class="sxs-lookup"><span data-stu-id="4fd63-170">Specifies default configuration data for the authentication protocol.</span></span> |

## <a name="ras_eap_valuename_require_configui"></a><span data-ttu-id="4fd63-171">RAS_EAP_VALUENAME_REQUIRE_CONFIGUI</span><span class="sxs-lookup"><span data-stu-id="4fd63-171">RAS_EAP_VALUENAME_REQUIRE_CONFIGUI</span></span>

| <span data-ttu-id="4fd63-172">常數值</span><span class="sxs-lookup"><span data-stu-id="4fd63-172">Constant value</span></span> | <span data-ttu-id="4fd63-173">RequireConfigUI</span><span class="sxs-lookup"><span data-stu-id="4fd63-173">RequireConfigUI</span></span>                                                                                                                                                                                                                                          |
|----------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4fd63-174">類型</span><span class="sxs-lookup"><span data-stu-id="4fd63-174">Type</span></span>           | <span data-ttu-id="4fd63-175">REG_DWORD</span><span class="sxs-lookup"><span data-stu-id="4fd63-175">REG_DWORD</span></span>                                                                                                                                                                                                                                               |
| <span data-ttu-id="4fd63-176">Description</span><span class="sxs-lookup"><span data-stu-id="4fd63-176">Description</span></span>    | <span data-ttu-id="4fd63-177">指定使用者是否必須在 EAP 用戶端應用程式使用者介面中提供設定資料。</span><span class="sxs-lookup"><span data-stu-id="4fd63-177">Specifies whether the user must provide configuration data in the EAP client application user interface.</span></span> <span data-ttu-id="4fd63-178">如果此值為1，則不允許使用者離開 EAP 用戶端應用程式 UI，而不提供設定資料。</span><span class="sxs-lookup"><span data-stu-id="4fd63-178">If this value is 1, the user is not allowed to exit the EAP client application UI without providing configuration data.</span></span> <span data-ttu-id="4fd63-179">預設值為 0。</span><span class="sxs-lookup"><span data-stu-id="4fd63-179">The default value is 0.</span></span> |

## <a name="ras_eap_valuename_config_clsid"></a><span data-ttu-id="4fd63-180">RAS_EAP_VALUENAME_CONFIG_CLSID</span><span class="sxs-lookup"><span data-stu-id="4fd63-180">RAS_EAP_VALUENAME_CONFIG_CLSID</span></span>

| <span data-ttu-id="4fd63-181">常數值</span><span class="sxs-lookup"><span data-stu-id="4fd63-181">Constant value</span></span> | <span data-ttu-id="4fd63-182">ConfigCLSID</span><span class="sxs-lookup"><span data-stu-id="4fd63-182">ConfigCLSID</span></span>                                                   |
|----------------|---------------------------------------------------------------|
| <span data-ttu-id="4fd63-183">類型</span><span class="sxs-lookup"><span data-stu-id="4fd63-183">Type</span></span>           | <span data-ttu-id="4fd63-184">REG_SZ</span><span class="sxs-lookup"><span data-stu-id="4fd63-184">REG_SZ</span></span>                                                       |
| <span data-ttu-id="4fd63-185">Description</span><span class="sxs-lookup"><span data-stu-id="4fd63-185">Description</span></span>    | <span data-ttu-id="4fd63-186">指定伺服器上設定 UI 的類別識別碼。</span><span class="sxs-lookup"><span data-stu-id="4fd63-186">Specifies the class ID of the configuration UI on the server.</span></span> |

## <a name="ras_eap_valuename_identity"></a><span data-ttu-id="4fd63-187">RAS_EAP_VALUENAME_IDENTITY</span><span class="sxs-lookup"><span data-stu-id="4fd63-187">RAS_EAP_VALUENAME_IDENTITY</span></span>

| <span data-ttu-id="4fd63-188">常數值</span><span class="sxs-lookup"><span data-stu-id="4fd63-188">Constant value</span></span> | <span data-ttu-id="4fd63-189">IdentityPath</span><span class="sxs-lookup"><span data-stu-id="4fd63-189">IdentityPath</span></span>                                                                                                                           |
|----------------|----------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4fd63-190">類型</span><span class="sxs-lookup"><span data-stu-id="4fd63-190">Type</span></span>           | <span data-ttu-id="4fd63-191"> REG_EXPAND_SZ </span><span class="sxs-lookup"><span data-stu-id="4fd63-191">REG_EXPAND_SZ</span></span>                                                                                                                        |
| <span data-ttu-id="4fd63-192">Description</span><span class="sxs-lookup"><span data-stu-id="4fd63-192">Description</span></span>    | <span data-ttu-id="4fd63-193">指定可在用戶端上執行函式以取得使用者身分識別之 DLL 的路徑，因為此 UI 僅供用戶端使用。</span><span class="sxs-lookup"><span data-stu-id="4fd63-193">Specifies the path to the DLL that implements functions to obtain the user identity on the client, because this UI is for client only.</span></span> |

## <a name="ras_eap_valuename_interactiveui"></a><span data-ttu-id="4fd63-194">RAS_EAP_VALUENAME_INTERACTIVEUI</span><span class="sxs-lookup"><span data-stu-id="4fd63-194">RAS_EAP_VALUENAME_INTERACTIVEUI</span></span>

| <span data-ttu-id="4fd63-195">常數值</span><span class="sxs-lookup"><span data-stu-id="4fd63-195">Constant value</span></span> | <span data-ttu-id="4fd63-196">InteractiveUIPath</span><span class="sxs-lookup"><span data-stu-id="4fd63-196">InteractiveUIPath</span></span>                                                                                                               |
|----------------|---------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4fd63-197">類型</span><span class="sxs-lookup"><span data-stu-id="4fd63-197">Type</span></span>           | <span data-ttu-id="4fd63-198"> REG_EXPAND_SZ </span><span class="sxs-lookup"><span data-stu-id="4fd63-198">REG_EXPAND_SZ</span></span>                                                                                                                 |
| <span data-ttu-id="4fd63-199">Description</span><span class="sxs-lookup"><span data-stu-id="4fd63-199">Description</span></span>    | <span data-ttu-id="4fd63-200">指定在用戶端上執行互動式使用者介面之 DLL 的路徑，因為此 UI 僅供用戶端使用。</span><span class="sxs-lookup"><span data-stu-id="4fd63-200">Specifies the path to the DLL that implements the interactive user interface on the client, because this UI is for client only.</span></span> |

## <a name="ras_eap_valuename_invoke_namedlg"></a><span data-ttu-id="4fd63-201">RAS_EAP_VALUENAME_INVOKE_NAMEDLG</span><span class="sxs-lookup"><span data-stu-id="4fd63-201">RAS_EAP_VALUENAME_INVOKE_NAMEDLG</span></span>

| <span data-ttu-id="4fd63-202">常數值</span><span class="sxs-lookup"><span data-stu-id="4fd63-202">Constant value</span></span> | <span data-ttu-id="4fd63-203">InvokeUsernameDialog</span><span class="sxs-lookup"><span data-stu-id="4fd63-203">InvokeUsernameDialog</span></span>                                                                                                                                                                                   |
|----------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4fd63-204">類型</span><span class="sxs-lookup"><span data-stu-id="4fd63-204">Type</span></span>           | <span data-ttu-id="4fd63-205">REG_DWORD</span><span class="sxs-lookup"><span data-stu-id="4fd63-205">REG_DWORD</span></span>                                                                                                                                                                                             |
| <span data-ttu-id="4fd63-206">Description</span><span class="sxs-lookup"><span data-stu-id="4fd63-206">Description</span></span>    | <span data-ttu-id="4fd63-207">指定 RAS 是否應顯示標準的 Windows NT/Windows 2000 使用者名稱對話方塊 (值為 1) 或叫用 [**RasEapGetIdentity**](/previous-versions/windows/desktop/api/Raseapif/nf-raseapif-raseapgetidentity) (值為 0) 。</span><span class="sxs-lookup"><span data-stu-id="4fd63-207">Specifies whether RAS should display the standard Windows NT/Windows 2000 user name dialog (value of 1) or invoke [**RasEapGetIdentity**](/previous-versions/windows/desktop/api/Raseapif/nf-raseapif-raseapgetidentity) (value of 0).</span></span> <span data-ttu-id="4fd63-208">預設值為 1。</span><span class="sxs-lookup"><span data-stu-id="4fd63-208">The default value is 1.</span></span> |

## <a name="ras_eap_valuename_invoke_pwddlg"></a><span data-ttu-id="4fd63-209">RAS_EAP_VALUENAME_INVOKE_PWDDLG</span><span class="sxs-lookup"><span data-stu-id="4fd63-209">RAS_EAP_VALUENAME_INVOKE_PWDDLG</span></span>

| <span data-ttu-id="4fd63-210">常數值</span><span class="sxs-lookup"><span data-stu-id="4fd63-210">Constant value</span></span> | <span data-ttu-id="4fd63-211">InvokePasswordDialog</span><span class="sxs-lookup"><span data-stu-id="4fd63-211">InvokePasswordDialog</span></span>                                                                                                                                                                        |
|----------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4fd63-212">類型</span><span class="sxs-lookup"><span data-stu-id="4fd63-212">Type</span></span>           | <span data-ttu-id="4fd63-213">REG_DWORD</span><span class="sxs-lookup"><span data-stu-id="4fd63-213">REG_DWORD</span></span>                                                                                                                                                                                  |
| <span data-ttu-id="4fd63-214">Description</span><span class="sxs-lookup"><span data-stu-id="4fd63-214">Description</span></span>    | <span data-ttu-id="4fd63-215">指定 RAS 是否應顯示標準的 Windows NT/Windows 2000 密碼對話方塊。</span><span class="sxs-lookup"><span data-stu-id="4fd63-215">Specifies whether RAS should display the standard Windows NT/Windows 2000 password dialog.</span></span> <span data-ttu-id="4fd63-216">如果這個值存在且為0，RAS 將不會顯示密碼對話方塊。</span><span class="sxs-lookup"><span data-stu-id="4fd63-216">If this value exists and is 0, RAS will not display the password dialog.</span></span> <span data-ttu-id="4fd63-217">預設值為 1。</span><span class="sxs-lookup"><span data-stu-id="4fd63-217">The default value is 1.</span></span> |


## <a name="ras_eap_valuename_encryption"></a><span data-ttu-id="4fd63-218">RAS_EAP_VALUENAME_ENCRYPTION</span><span class="sxs-lookup"><span data-stu-id="4fd63-218">RAS_EAP_VALUENAME_ENCRYPTION</span></span>

| <span data-ttu-id="4fd63-219">常數值</span><span class="sxs-lookup"><span data-stu-id="4fd63-219">Constant value</span></span> | <span data-ttu-id="4fd63-220">MPPEEncryptionSupported</span><span class="sxs-lookup"><span data-stu-id="4fd63-220">MPPEEncryptionSupported</span></span>                                                                                                                                                                       |
|----------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4fd63-221">類型</span><span class="sxs-lookup"><span data-stu-id="4fd63-221">Type</span></span>           | <span data-ttu-id="4fd63-222">REG_DWORD</span><span class="sxs-lookup"><span data-stu-id="4fd63-222">REG_DWORD</span></span>                                                                                                                                                                                    |
| <span data-ttu-id="4fd63-223">Description</span><span class="sxs-lookup"><span data-stu-id="4fd63-223">Description</span></span>    | <span data-ttu-id="4fd63-224">如果這個值是1，則驗證通訊協定可以產生 Microsoft 點對點加密 (MPPE) 加密樣式的金鑰。</span><span class="sxs-lookup"><span data-stu-id="4fd63-224">If this value is 1, the authentication protocol can generate keys for the Microsoft Point-to-Point Encryption (MPPE) style of encryption.</span></span> <span data-ttu-id="4fd63-225">可能的值為0或1。</span><span class="sxs-lookup"><span data-stu-id="4fd63-225">Possible values are 0 or 1.</span></span> <span data-ttu-id="4fd63-226">預設值為 0。</span><span class="sxs-lookup"><span data-stu-id="4fd63-226">The default value is 0.</span></span> |

## <a name="ras_eap_valuename_standalone_supported"></a><span data-ttu-id="4fd63-227">RAS_EAP_VALUENAME_STANDALONE_SUPPORTED</span><span class="sxs-lookup"><span data-stu-id="4fd63-227">RAS_EAP_VALUENAME_STANDALONE_SUPPORTED</span></span>

| <span data-ttu-id="4fd63-228">常數值</span><span class="sxs-lookup"><span data-stu-id="4fd63-228">Constant value</span></span> | <span data-ttu-id="4fd63-229">StandaloneSupported</span><span class="sxs-lookup"><span data-stu-id="4fd63-229">StandaloneSupported</span></span>                                                                                                                                                            |
|----------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4fd63-230">類型</span><span class="sxs-lookup"><span data-stu-id="4fd63-230">Type</span></span>           | <span data-ttu-id="4fd63-231">REG_DWORD</span><span class="sxs-lookup"><span data-stu-id="4fd63-231">REG_DWORD</span></span>                                                                                                                                                                     |
| <span data-ttu-id="4fd63-232">Description</span><span class="sxs-lookup"><span data-stu-id="4fd63-232">Description</span></span>    | <span data-ttu-id="4fd63-233">指定獨立 Windows 2000 伺服器是否支援此驗證通訊協定。</span><span class="sxs-lookup"><span data-stu-id="4fd63-233">Specifies whether this authentication protocol is supported on a standalone Windows 2000 Server.</span></span> <span data-ttu-id="4fd63-234">值為0表示不支援 EAP。</span><span class="sxs-lookup"><span data-stu-id="4fd63-234">A value of 0 indicates that the EAP is not supported.</span></span> <span data-ttu-id="4fd63-235">預設值為 1。</span><span class="sxs-lookup"><span data-stu-id="4fd63-235">The default value is 1.</span></span> |

## <a name="ras_eap_valuename_roles_supported"></a><span data-ttu-id="4fd63-236">RAS_EAP_VALUENAME_ROLES_SUPPORTED</span><span class="sxs-lookup"><span data-stu-id="4fd63-236">RAS_EAP_VALUENAME_ROLES_SUPPORTED</span></span>

| <span data-ttu-id="4fd63-237">常數值</span><span class="sxs-lookup"><span data-stu-id="4fd63-237">Constant Value</span></span> | <span data-ttu-id="4fd63-238">RolesSupported</span><span class="sxs-lookup"><span data-stu-id="4fd63-238">RolesSupported</span></span>                                                                                                                                                                                                                             |
|----------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4fd63-239">類型</span><span class="sxs-lookup"><span data-stu-id="4fd63-239">Type</span></span>           | <span data-ttu-id="4fd63-240">REG_DWORD</span><span class="sxs-lookup"><span data-stu-id="4fd63-240">REG_DWORD</span></span>                                                                                                                                                                                                                                 |
| <span data-ttu-id="4fd63-241">Description</span><span class="sxs-lookup"><span data-stu-id="4fd63-241">Description</span></span>    | <span data-ttu-id="4fd63-242">指定 EAP 支援的各種角色。</span><span class="sxs-lookup"><span data-stu-id="4fd63-242">Specifies the various roles the EAP supports.</span></span> <span data-ttu-id="4fd63-243">這指出是否可在伺服器或用戶端上使用它， (VPN) 或 PEAP 的 RAS 連線是否支援。</span><span class="sxs-lookup"><span data-stu-id="4fd63-243">This indicates whether it can be used on a server or a client, whether it is supported for RAS connections (VPN) or PEAP.</span></span> <span data-ttu-id="4fd63-244">預設行為是在 PEAP 和 EAP 中顯示 EAP 方法。</span><span class="sxs-lookup"><span data-stu-id="4fd63-244">The default behavior is to show the EAP method in PEAP and in EAP.</span></span> |

## <a name="ras_eap_valuename_per_policy_config"></a><span data-ttu-id="4fd63-245">RAS_EAP_VALUENAME_PER_POLICY_CONFIG</span><span class="sxs-lookup"><span data-stu-id="4fd63-245">RAS_EAP_VALUENAME_PER_POLICY_CONFIG</span></span>

| <span data-ttu-id="4fd63-246">常數值</span><span class="sxs-lookup"><span data-stu-id="4fd63-246">Constant Value</span></span> | <span data-ttu-id="4fd63-247">PerPolicyConfig</span><span class="sxs-lookup"><span data-stu-id="4fd63-247">PerPolicyConfig</span></span> |
|----------------|-----------------|
| <span data-ttu-id="4fd63-248">類型</span><span class="sxs-lookup"><span data-stu-id="4fd63-248">Type</span></span>           | <span data-ttu-id="4fd63-249">REG_DWORD</span><span class="sxs-lookup"><span data-stu-id="4fd63-249">REG_DWORD</span></span>      |
| <span data-ttu-id="4fd63-250">Description</span><span class="sxs-lookup"><span data-stu-id="4fd63-250">Description</span></span>    |                 |

## <a name="ras_eap_valuename_istunnel_method"></a><span data-ttu-id="4fd63-251">RAS_EAP_VALUENAME_ISTUNNEL_METHOD</span><span class="sxs-lookup"><span data-stu-id="4fd63-251">RAS_EAP_VALUENAME_ISTUNNEL_METHOD</span></span>

<span data-ttu-id="4fd63-252">此登錄值不在使用中。</span><span class="sxs-lookup"><span data-stu-id="4fd63-252">This registry value is not in use.</span></span>

## <a name="ras_eap_valuename_filter_innermethods"></a><span data-ttu-id="4fd63-253">RAS_EAP_VALUENAME_FILTER_INNERMETHODS</span><span class="sxs-lookup"><span data-stu-id="4fd63-253">RAS_EAP_VALUENAME_FILTER_INNERMETHODS</span></span>

<span data-ttu-id="4fd63-254">此登錄值不在使用中。</span><span class="sxs-lookup"><span data-stu-id="4fd63-254">This registry value is not in use.</span></span>

