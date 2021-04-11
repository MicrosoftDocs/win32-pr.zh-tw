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
# <a name="authentication-protocol-registry-values"></a>驗證通訊協定登錄值

EAP DLL 的安裝軟體可能會在 **&lt; eaptypeid &gt;** 底下建立下列登錄值。 這些登錄值定義于 Raseapif .h 標頭檔中。 需要 **RAS_EAP_VALUENAME_PATH** 和 **RAS_EAP_VALUENAME_FRIENDLY_NAME** 值。 安裝軟體也可以建立其他金鑰和值。 驗證通訊協定本身可以使用這些方法。 如需登錄設定的詳細資訊和範例，請參閱登錄 [值範例](registry-values-example.md)。

[RAS_EAP_VALUENAME_PATH](#ras_eap_valuename_path)

[RAS_EAP_VALUENAME_FRIENDLY_NAME](#ras_eap_valuename_friendly_name)

[RAS_EAP_VALUENAME_CONFIGUI](#ras_eap_valuename_configui)

[RAS_EAP_VALUENAME_DEFAULT_DATA](#ras_eap_valuename_default_data)

[RAS_EAP_VALUENAME_REQUIRE_CONFIGUI](#ras_eap_valuename_require_configui)

[RAS_EAP_VALUENAME_CONFIG_CLSID](#ras_eap_valuename_config_clsid)

[RAS_EAP_VALUENAME_IDENTITY](#ras_eap_valuename_identity)

[RAS_EAP_VALUENAME_INTERACTIVEUI](#ras_eap_valuename_interactiveui)我

[RAS_EAP_VALUENAME_INVOKE_NAMEDLG](#ras_eap_valuename_invoke_namedlg)

[RAS_EAP_VALUENAME_INVOKE_PWDDLG](#ras_eap_valuename_invoke_pwddlg)

[RAS_EAP_VALUENAME_ENCRYPTION](#ras_eap_valuename_encryption)

[RAS_EAP_VALUENAME_STANDALONE_SUPPORTED](#ras_eap_valuename_standalone_supported)

[RAS_EAP_VALUENAME_ROLES_SUPPORTED](#ras_eap_valuename_roles_supported)

[RAS_EAP_VALUENAME_PER_POLICY_CONFIG](#ras_eap_valuename_per_policy_config)

[RAS_EAP_VALUENAME_ISTUNNEL_METHOD](#ras_eap_valuename_istunnel_method)

[RAS_EAP_VALUENAME_FILTER_INNERMETHODS](#ras_eap_valuename_filter_innermethods)

## <a name="ras_eap_valuename_path"></a>RAS_EAP_VALUENAME_PATH

| 常數值 | 路徑                               |
|----------------|------------------------------------|
| 類型           |  REG_EXPAND_SZ                     |
| Description    | 指定 EAP DLL 的路徑。 |

## <a name="ras_eap_valuename_friendly_name"></a>RAS_EAP_VALUENAME_FRIENDLY_NAME

| 常數值 | FriendlyName                                                                                                                                                      |
|----------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 類型           | REG_SZ                                                                                                                                                           |
| Description    | 指定驗證通訊協定的易記名稱。 這個名稱會出現在 EAP 應用程式使用者介面中，以供撥號和無線執行。 |

## <a name="ras_eap_valuename_configui"></a>RAS_EAP_VALUENAME_CONFIGUI

| 常數值 | ConfigUIPath                                                                                                                      |
|----------------|-----------------------------------------------------------------------------------------------------------------------------------|
| 類型           |  REG_EXPAND_SZ                                                                                                                    |
| Description    | 指定在用戶端上執行設定使用者介面之 DLL 的路徑，因為此 UI 僅供用戶端使用。 |

## <a name="ras_eap_valuename_default_data"></a>RAS_EAP_VALUENAME_DEFAULT_DATA

| 常數值 | ConfigData                                                            |
|----------------|-----------------------------------------------------------------------|
| 類型           | REG_BINARY                                                           |
| Description    | 指定驗證通訊協定的預設設定資料。 |

## <a name="ras_eap_valuename_require_configui"></a>RAS_EAP_VALUENAME_REQUIRE_CONFIGUI

| 常數值 | RequireConfigUI                                                                                                                                                                                                                                          |
|----------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 類型           | REG_DWORD                                                                                                                                                                                                                                               |
| Description    | 指定使用者是否必須在 EAP 用戶端應用程式使用者介面中提供設定資料。 如果此值為1，則不允許使用者離開 EAP 用戶端應用程式 UI，而不提供設定資料。 預設值為 0。 |

## <a name="ras_eap_valuename_config_clsid"></a>RAS_EAP_VALUENAME_CONFIG_CLSID

| 常數值 | ConfigCLSID                                                   |
|----------------|---------------------------------------------------------------|
| 類型           | REG_SZ                                                       |
| Description    | 指定伺服器上設定 UI 的類別識別碼。 |

## <a name="ras_eap_valuename_identity"></a>RAS_EAP_VALUENAME_IDENTITY

| 常數值 | IdentityPath                                                                                                                           |
|----------------|----------------------------------------------------------------------------------------------------------------------------------------|
| 類型           |  REG_EXPAND_SZ                                                                                                                         |
| Description    | 指定可在用戶端上執行函式以取得使用者身分識別之 DLL 的路徑，因為此 UI 僅供用戶端使用。 |

## <a name="ras_eap_valuename_interactiveui"></a>RAS_EAP_VALUENAME_INTERACTIVEUI

| 常數值 | InteractiveUIPath                                                                                                               |
|----------------|---------------------------------------------------------------------------------------------------------------------------------|
| 類型           |  REG_EXPAND_SZ                                                                                                                  |
| Description    | 指定在用戶端上執行互動式使用者介面之 DLL 的路徑，因為此 UI 僅供用戶端使用。 |

## <a name="ras_eap_valuename_invoke_namedlg"></a>RAS_EAP_VALUENAME_INVOKE_NAMEDLG

| 常數值 | InvokeUsernameDialog                                                                                                                                                                                   |
|----------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 類型           | REG_DWORD                                                                                                                                                                                             |
| Description    | 指定 RAS 是否應顯示標準的 Windows NT/Windows 2000 使用者名稱對話方塊 (值為 1) 或叫用 [**RasEapGetIdentity**](/previous-versions/windows/desktop/api/Raseapif/nf-raseapif-raseapgetidentity) (值為 0) 。 預設值為 1。 |

## <a name="ras_eap_valuename_invoke_pwddlg"></a>RAS_EAP_VALUENAME_INVOKE_PWDDLG

| 常數值 | InvokePasswordDialog                                                                                                                                                                        |
|----------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 類型           | REG_DWORD                                                                                                                                                                                  |
| Description    | 指定 RAS 是否應顯示標準的 Windows NT/Windows 2000 密碼對話方塊。 如果這個值存在且為0，RAS 將不會顯示密碼對話方塊。 預設值為 1。 |


## <a name="ras_eap_valuename_encryption"></a>RAS_EAP_VALUENAME_ENCRYPTION

| 常數值 | MPPEEncryptionSupported                                                                                                                                                                       |
|----------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 類型           | REG_DWORD                                                                                                                                                                                    |
| Description    | 如果這個值是1，則驗證通訊協定可以產生 Microsoft 點對點加密 (MPPE) 加密樣式的金鑰。 可能的值為0或1。 預設值為 0。 |

## <a name="ras_eap_valuename_standalone_supported"></a>RAS_EAP_VALUENAME_STANDALONE_SUPPORTED

| 常數值 | StandaloneSupported                                                                                                                                                            |
|----------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 類型           | REG_DWORD                                                                                                                                                                     |
| Description    | 指定獨立 Windows 2000 伺服器是否支援此驗證通訊協定。 值為0表示不支援 EAP。 預設值為 1。 |

## <a name="ras_eap_valuename_roles_supported"></a>RAS_EAP_VALUENAME_ROLES_SUPPORTED

| 常數值 | RolesSupported                                                                                                                                                                                                                             |
|----------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 類型           | REG_DWORD                                                                                                                                                                                                                                 |
| Description    | 指定 EAP 支援的各種角色。 這指出是否可在伺服器或用戶端上使用它， (VPN) 或 PEAP 的 RAS 連線是否支援。 預設行為是在 PEAP 和 EAP 中顯示 EAP 方法。 |

## <a name="ras_eap_valuename_per_policy_config"></a>RAS_EAP_VALUENAME_PER_POLICY_CONFIG

| 常數值 | PerPolicyConfig |
|----------------|-----------------|
| 類型           | REG_DWORD      |
| Description    |                 |

## <a name="ras_eap_valuename_istunnel_method"></a>RAS_EAP_VALUENAME_ISTUNNEL_METHOD

此登錄值不在使用中。

## <a name="ras_eap_valuename_filter_innermethods"></a>RAS_EAP_VALUENAME_FILTER_INNERMETHODS

此登錄值不在使用中。

