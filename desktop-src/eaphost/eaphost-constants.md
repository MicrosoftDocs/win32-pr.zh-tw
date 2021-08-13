---
title: 'EAPHost 常數 (Eaptypes) '
description: 查看 EAPHost 方法所使用) EAPHost 常數 (Eaptypes 的清單，並查看其使用需求。
ms.assetid: 56338B98-06E3-4CD3-B1CA-F8F45AA39566
topic_type:
- apiref
api_name:
- EAP_INTERACTIVE_UI_DATA_VERSION
- EAP_CREDENTIAL_VERSION
- EAPHOST_PEER_API_VERSION
- CERTIFICATE_HASH_LENGTH
- MAX_EAP_CONFIG_INPUT_FIELD_LENGTH
- MAX_EAP_CONFIG_INPUT_FIELD_VALUE_LENGTH
- EAP_UI_INPUT_FIELD_PROPS_DEFAULT
- EAP_CONFIG_INPUT_FIELD_PROPS_DEFAULT
- EAP_UI_INPUT_FIELD_PROPS_NON_DISPLAYABLE
- EAP_CONFIG_INPUT_FIELD_PROPS_NON_DISPLAYABLE
- EAP_UI_INPUT_FIELD_PROPS_NON_PERSIST
- EAP_UI_INPUT_FIELD_PROPS_READ_ONLY
api_location:
- eaptypes.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ab336b147557722f1bec72bfe662b12599a64ee1622b31bdad6a92a05af6d92e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119483008"
---
# <a name="eaphost-constants"></a>EAPHost 常數

EAPHost 方法所使用的常數。

<dl> <dt>

<span id="EAP_INTERACTIVE_UI_DATA_VERSION"></span><span id="eap_interactive_ui_data_version"></span>**EAP \_ 互動式 \_ UI \_ 資料 \_ 版本**
</dt> <dd> <dl> <dt>

0
</dt> <dt>



EAP 互動式 UI 資料的版本。


</dt> </dl> </dd> <dt>

<span id="EAP_CREDENTIAL_VERSION"></span><span id="eap_credential_version"></span>**EAP \_ 認證 \_ 版本**
</dt> <dd> <dl> <dt>

1
</dt> <dt>



使用者所提供之 EAP 認證的版本。


</dt> </dl> </dd> <dt>

<span id="EAPHOST_PEER_API_VERSION"></span><span id="eaphost_peer_api_version"></span>**EAPHOST \_ 對等 \_ API \_ 版本**
</dt> <dd> <dl> <dt>

1
</dt> <dt>



EAPHost 對等 API 的版本。


</dt> </dl> </dd> <dt>

<span id="CERTIFICATE_HASH_LENGTH"></span><span id="certificate_hash_length"></span>**憑證 \_ 雜湊 \_ 長度**
</dt> <dd> <dl> <dt>

20
</dt> <dt>



憑證的 SHA1 雜湊長度。


</dt> </dl> </dd> <dt>

<span id="MAX_EAP_CONFIG_INPUT_FIELD_LENGTH"></span><span id="max_eap_config_input_field_length"></span>**最大 \_ EAP 設定 \_ \_ 輸入 \_ 欄位 \_ 長度**
</dt> <dd> <dl> <dt>

256
</dt> <dt>



指定輸入欄位支援的最大長度。


</dt> </dl> </dd> <dt>

<span id="MAX_EAP_CONFIG_INPUT_FIELD_VALUE_LENGTH"></span><span id="max_eap_config_input_field_value_length"></span>**最大 \_ EAP 設定 \_ \_ 輸入 \_ 域 \_ 值 \_ 長度**
</dt> <dd> <dl> <dt>

1024
</dt> <dt>



指定輸入欄位支援的最大長度。


</dt> </dl> </dd> <dt>

<span id="EAP_UI_INPUT_FIELD_PROPS_DEFAULT"></span><span id="eap_ui_input_field_props_default"></span>**EAP \_ UI \_ 輸入 \_ 欄位 \_ .PROPS \_ 預設值**
</dt> <dd> <dl> <dt>

0X00000000 
</dt> <dt>



WindowsVista SP1 或更新版本：代表 UI 中顯示之輸入欄位專案的預設屬性值。


</dt> </dl> </dd> <dt>

<span id="EAP_CONFIG_INPUT_FIELD_PROPS_DEFAULT"></span><span id="eap_config_input_field_props_default"></span>**EAP \_ 設定 \_ 輸入 \_ 欄位 \_ .PROPS \_ 預設值**
</dt> <dd> <dl> <dt>

0X00000000 
</dt> <dt>



代表 UI 中顯示之設定輸入欄位專案的預設屬性值。


</dt> </dl> </dd> <dt>

<span id="EAP_UI_INPUT_FIELD_PROPS_NON_DISPLAYABLE"></span><span id="eap_ui_input_field_props_non_displayable"></span>**EAP \_ UI \_ 輸入 \_ 欄位 \_ .PROPS \_ 不可 \_ 顯示**
</dt> <dd> <dl> <dt>

0X00000001 
</dt> <dt>



WindowsVista SP1 或更新版本：指定輸入欄位專案將不會顯示在 UI 中 (密碼或 PIN 碼，例如) 。


</dt> </dl> </dd> <dt>

<span id="EAP_CONFIG_INPUT_FIELD_PROPS_NON_DISPLAYABLE"></span><span id="eap_config_input_field_props_non_displayable"></span>**EAP \_ 設定 \_ 輸入 \_ 欄位 \_ .PROPS \_ 不可 \_ 顯示**
</dt> <dd> <dl> <dt>

0X00000001 
</dt> <dt>



指定設定輸入欄位專案將不會顯示在 UI 中 (密碼或 PIN 碼，例如) 。


</dt> </dl> </dd> <dt>

<span id="EAP_UI_INPUT_FIELD_PROPS_NON_PERSIST"></span><span id="eap_ui_input_field_props_non_persist"></span>**EAP \_ UI \_ 輸入 \_ 欄位 \_ .PROPS \_ 非 \_ 保存**
</dt> <dd> <dl> <dt>

0X00000002 
</dt> <dt>



WindowsVista SP1 或更新版本：表示 EAP 方法不會快取欄位資料;要求者必須快取欄位資料以進行漫遊。


</dt> </dl> </dd> <dt>

<span id="EAP_UI_INPUT_FIELD_PROPS_READ_ONLY"></span><span id="eap_ui_input_field_props_read_only"></span>**EAP \_ UI \_ 輸入 \_ 欄位 \_ .PROPS \_ 唯讀 \_**
</dt> <dd> <dl> <dt>

0x00000004
</dt> <dt>



WindowsVista SP1 或更新版本：表示輸入欄位是唯讀的，而且無法編輯。


</dt> </dl> </dd> </dl>

## <a name="requirements"></a>規格需求



| 角色 | 最低支援作業系統版本 |
|------|------------------------------|
| 用戶端<br/> | Windows 8 \[僅限桌面應用程式\]<br/> |
| 伺服器<br/> | Windows Server 2012 \[僅限桌面應用程式\]<br/> |



 

 





