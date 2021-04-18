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
ms.openlocfilehash: 84704e59ed43466c47435f4804cb4dedc9c3a92d
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/21/2020
ms.locfileid: "104382830"
---
# <a name="eaphost-constants"></a><span data-ttu-id="78282-103">EAPHost 常數</span><span class="sxs-lookup"><span data-stu-id="78282-103">EAPHost Constants</span></span>

<span data-ttu-id="78282-104">EAPHost 方法所使用的常數。</span><span class="sxs-lookup"><span data-stu-id="78282-104">The constants used by EAPHost methods.</span></span>

<dl> <dt>

<span data-ttu-id="78282-105"><span id="EAP_INTERACTIVE_UI_DATA_VERSION"></span><span id="eap_interactive_ui_data_version"></span>**EAP \_ 互動式 \_ UI \_ 資料 \_ 版本**</span><span class="sxs-lookup"><span data-stu-id="78282-105"><span id="EAP_INTERACTIVE_UI_DATA_VERSION"></span><span id="eap_interactive_ui_data_version"></span>**EAP\_INTERACTIVE\_UI\_DATA\_VERSION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="78282-106">0</span><span class="sxs-lookup"><span data-stu-id="78282-106">0</span></span>
</dt> <dt>



<span data-ttu-id="78282-107">EAP 互動式 UI 資料的版本。</span><span class="sxs-lookup"><span data-stu-id="78282-107">The version of the EAP interactive UI data.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="78282-108"><span id="EAP_CREDENTIAL_VERSION"></span><span id="eap_credential_version"></span>**EAP \_ 認證 \_ 版本**</span><span class="sxs-lookup"><span data-stu-id="78282-108"><span id="EAP_CREDENTIAL_VERSION"></span><span id="eap_credential_version"></span>**EAP\_CREDENTIAL\_VERSION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="78282-109">1</span><span class="sxs-lookup"><span data-stu-id="78282-109">1</span></span>
</dt> <dt>



<span data-ttu-id="78282-110">使用者所提供之 EAP 認證的版本。</span><span class="sxs-lookup"><span data-stu-id="78282-110">The version of the EAP credentials supplied by the user.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="78282-111"><span id="EAPHOST_PEER_API_VERSION"></span><span id="eaphost_peer_api_version"></span>**EAPHOST \_ 對等 \_ API \_ 版本**</span><span class="sxs-lookup"><span data-stu-id="78282-111"><span id="EAPHOST_PEER_API_VERSION"></span><span id="eaphost_peer_api_version"></span>**EAPHOST\_PEER\_API\_VERSION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="78282-112">1</span><span class="sxs-lookup"><span data-stu-id="78282-112">1</span></span>
</dt> <dt>



<span data-ttu-id="78282-113">EAPHost 對等 API 的版本。</span><span class="sxs-lookup"><span data-stu-id="78282-113">The version of the EAPHost peer API.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="78282-114"><span id="CERTIFICATE_HASH_LENGTH"></span><span id="certificate_hash_length"></span>**憑證 \_ 雜湊 \_ 長度**</span><span class="sxs-lookup"><span data-stu-id="78282-114"><span id="CERTIFICATE_HASH_LENGTH"></span><span id="certificate_hash_length"></span>**CERTIFICATE\_HASH\_LENGTH**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="78282-115">20</span><span class="sxs-lookup"><span data-stu-id="78282-115">20</span></span>
</dt> <dt>



<span data-ttu-id="78282-116">憑證的 SHA1 雜湊長度。</span><span class="sxs-lookup"><span data-stu-id="78282-116">Length of the SHA1 hash of the certificate.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="78282-117"><span id="MAX_EAP_CONFIG_INPUT_FIELD_LENGTH"></span><span id="max_eap_config_input_field_length"></span>**最大 \_ EAP 設定 \_ \_ 輸入 \_ 欄位 \_ 長度**</span><span class="sxs-lookup"><span data-stu-id="78282-117"><span id="MAX_EAP_CONFIG_INPUT_FIELD_LENGTH"></span><span id="max_eap_config_input_field_length"></span>**MAX\_EAP\_CONFIG\_INPUT\_FIELD\_LENGTH**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="78282-118">256</span><span class="sxs-lookup"><span data-stu-id="78282-118">256</span></span>
</dt> <dt>



<span data-ttu-id="78282-119">指定輸入欄位支援的最大長度。</span><span class="sxs-lookup"><span data-stu-id="78282-119">Specifies the maximum supported length of an input field.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="78282-120"><span id="MAX_EAP_CONFIG_INPUT_FIELD_VALUE_LENGTH"></span><span id="max_eap_config_input_field_value_length"></span>**最大 \_ EAP 設定 \_ \_ 輸入 \_ 域 \_ 值 \_ 長度**</span><span class="sxs-lookup"><span data-stu-id="78282-120"><span id="MAX_EAP_CONFIG_INPUT_FIELD_VALUE_LENGTH"></span><span id="max_eap_config_input_field_value_length"></span>**MAX\_EAP\_CONFIG\_INPUT\_FIELD\_VALUE\_LENGTH**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="78282-121">1024</span><span class="sxs-lookup"><span data-stu-id="78282-121">1024</span></span>
</dt> <dt>



<span data-ttu-id="78282-122">指定輸入欄位支援的最大長度。</span><span class="sxs-lookup"><span data-stu-id="78282-122">Specifies the maximum supported length of an input field.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="78282-123"><span id="EAP_UI_INPUT_FIELD_PROPS_DEFAULT"></span><span id="eap_ui_input_field_props_default"></span>**EAP \_ UI \_ 輸入 \_ 欄位 \_ .PROPS \_ 預設值**</span><span class="sxs-lookup"><span data-stu-id="78282-123"><span id="EAP_UI_INPUT_FIELD_PROPS_DEFAULT"></span><span id="eap_ui_input_field_props_default"></span>**EAP\_UI\_INPUT\_FIELD\_PROPS\_DEFAULT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="78282-124">0X00000000</span><span class="sxs-lookup"><span data-stu-id="78282-124">0X00000000</span></span> 
</dt> <dt>



<span data-ttu-id="78282-125">Windows Vista SP1 或更新版本：代表 UI 中顯示之輸入欄位專案的預設屬性值。</span><span class="sxs-lookup"><span data-stu-id="78282-125">Windows Vista with SP1 or later: Represents the default property value for input field entries displayed in the UI.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="78282-126"><span id="EAP_CONFIG_INPUT_FIELD_PROPS_DEFAULT"></span><span id="eap_config_input_field_props_default"></span>**EAP \_ 設定 \_ 輸入 \_ 欄位 \_ .PROPS \_ 預設值**</span><span class="sxs-lookup"><span data-stu-id="78282-126"><span id="EAP_CONFIG_INPUT_FIELD_PROPS_DEFAULT"></span><span id="eap_config_input_field_props_default"></span>**EAP\_CONFIG\_INPUT\_FIELD\_PROPS\_DEFAULT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="78282-127">0X00000000</span><span class="sxs-lookup"><span data-stu-id="78282-127">0X00000000</span></span> 
</dt> <dt>



<span data-ttu-id="78282-128">代表 UI 中顯示之設定輸入欄位專案的預設屬性值。</span><span class="sxs-lookup"><span data-stu-id="78282-128">Represents the default property value for configuration input field entries displayed in the UI.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="78282-129"><span id="EAP_UI_INPUT_FIELD_PROPS_NON_DISPLAYABLE"></span><span id="eap_ui_input_field_props_non_displayable"></span>**EAP \_ UI \_ 輸入 \_ 欄位 \_ .PROPS \_ 不可 \_ 顯示**</span><span class="sxs-lookup"><span data-stu-id="78282-129"><span id="EAP_UI_INPUT_FIELD_PROPS_NON_DISPLAYABLE"></span><span id="eap_ui_input_field_props_non_displayable"></span>**EAP\_UI\_INPUT\_FIELD\_PROPS\_NON\_DISPLAYABLE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="78282-130">0X00000001</span><span class="sxs-lookup"><span data-stu-id="78282-130">0X00000001</span></span> 
</dt> <dt>



<span data-ttu-id="78282-131">Windows Vista SP1 或更新版本：指定輸入欄位專案將不會顯示在 UI 中 (密碼或 PIN 碼，例如) 。</span><span class="sxs-lookup"><span data-stu-id="78282-131">Windows Vista with SP1 or later: Specifies that input field entries will not be displayed in the UI (a password or PIN number, for example).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="78282-132"><span id="EAP_CONFIG_INPUT_FIELD_PROPS_NON_DISPLAYABLE"></span><span id="eap_config_input_field_props_non_displayable"></span>**EAP \_ 設定 \_ 輸入 \_ 欄位 \_ .PROPS \_ 不可 \_ 顯示**</span><span class="sxs-lookup"><span data-stu-id="78282-132"><span id="EAP_CONFIG_INPUT_FIELD_PROPS_NON_DISPLAYABLE"></span><span id="eap_config_input_field_props_non_displayable"></span>**EAP\_CONFIG\_INPUT\_FIELD\_PROPS\_NON\_DISPLAYABLE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="78282-133">0X00000001</span><span class="sxs-lookup"><span data-stu-id="78282-133">0X00000001</span></span> 
</dt> <dt>



<span data-ttu-id="78282-134">指定設定輸入欄位專案將不會顯示在 UI 中 (密碼或 PIN 碼，例如) 。</span><span class="sxs-lookup"><span data-stu-id="78282-134">Specifies that configuration input field entries will not be displayed in the UI (a password or PIN number, for example).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="78282-135"><span id="EAP_UI_INPUT_FIELD_PROPS_NON_PERSIST"></span><span id="eap_ui_input_field_props_non_persist"></span>**EAP \_ UI \_ 輸入 \_ 欄位 \_ .PROPS \_ 非 \_ 保存**</span><span class="sxs-lookup"><span data-stu-id="78282-135"><span id="EAP_UI_INPUT_FIELD_PROPS_NON_PERSIST"></span><span id="eap_ui_input_field_props_non_persist"></span>**EAP\_UI\_INPUT\_FIELD\_PROPS\_NON\_PERSIST**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="78282-136">0X00000002</span><span class="sxs-lookup"><span data-stu-id="78282-136">0X00000002</span></span> 
</dt> <dt>



<span data-ttu-id="78282-137">Windows Vista （含 SP1 或更新版本）：表示 EAP 方法不會快取欄位資料;要求者必須快取欄位資料以進行漫遊。</span><span class="sxs-lookup"><span data-stu-id="78282-137">Windows Vista with SP1 or later: Indicates that the EAP method will not cache the field data; the supplicant must cache the field data for roaming.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="78282-138"><span id="EAP_UI_INPUT_FIELD_PROPS_READ_ONLY"></span><span id="eap_ui_input_field_props_read_only"></span>**EAP \_ UI \_ 輸入 \_ 欄位 \_ .PROPS \_ 唯讀 \_**</span><span class="sxs-lookup"><span data-stu-id="78282-138"><span id="EAP_UI_INPUT_FIELD_PROPS_READ_ONLY"></span><span id="eap_ui_input_field_props_read_only"></span>**EAP\_UI\_INPUT\_FIELD\_PROPS\_READ\_ONLY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="78282-139">0x00000004</span><span class="sxs-lookup"><span data-stu-id="78282-139">0x00000004</span></span>
</dt> <dt>



<span data-ttu-id="78282-140">Windows Vista （含 SP1 或更新版本）：表示輸入欄位是唯讀的，而且無法編輯。</span><span class="sxs-lookup"><span data-stu-id="78282-140">Windows Vista with SP1 or later: Indicates that the input field is read-only and cannot be edited.</span></span>


</dt> </dl> </dd> </dl>

## <a name="requirements"></a><span data-ttu-id="78282-141">規格需求</span><span class="sxs-lookup"><span data-stu-id="78282-141">Requirements</span></span>



| <span data-ttu-id="78282-142">角色</span><span class="sxs-lookup"><span data-stu-id="78282-142">Role</span></span> | <span data-ttu-id="78282-143">最低支援作業系統版本</span><span class="sxs-lookup"><span data-stu-id="78282-143">Minimum supported OS version</span></span> |
|------|------------------------------|
| <span data-ttu-id="78282-144">用戶端</span><span class="sxs-lookup"><span data-stu-id="78282-144">Client</span></span><br/> | <span data-ttu-id="78282-145">\[僅 Windows 8 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="78282-145">Windows 8 \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="78282-146">伺服器</span><span class="sxs-lookup"><span data-stu-id="78282-146">Server</span></span><br/> | <span data-ttu-id="78282-147">僅限 Windows Server 2012 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="78282-147">Windows Server 2012 \[desktop apps only\]</span></span><br/> |



 

 





