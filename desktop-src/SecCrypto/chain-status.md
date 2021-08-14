---
description: 抓取鏈的有效狀態或鏈中的特定憑證。
title: IChain2：： Status 屬性
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IChain2.Status
- IChain.Status
- Chain.Status
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 5307d03d340a0a960a5d78226d26e7b5553d27af72f255131651690e5b723355
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117769548"
---
# <a name="ichain2status-property"></a>IChain2：： Status 屬性

\[CAPICOM 是僅限32位的元件，可供下列作業系統使用： Windows Server 2008、Windows Vista 和 Windows XP。 請改為使用 [**system.security.cryptography.x509certificates.x509certificate2**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1)命名空間中的 [**X509Chain 類別**](/dotnet/api/system.security.cryptography.x509certificates.x509chain?view=netcore-3.1)。\]

**Status** 屬性會抓取鏈的有效狀態或鏈中的特定憑證。

## <a name="syntax"></a>Syntax


```VB
Chain.Status( _
  ByVal Index _
) As Long
```



## <a name="property-value"></a>屬性值

**LONG** 值，表示鏈或指定憑證的有效狀態指標。 下表顯示可能的值。 如果鏈或指定的憑證有效，則這個屬性會包含零。 否則，此屬性會包含一或多個下列值的組合。

<dt>

<span id="CAPICOM_TRUST_IS_NOT_TIME_VALID"></span><span id="capicom_trust_is_not_time_valid"></span>

<span id="CAPICOM_TRUST_IS_NOT_TIME_VALID"></span><span id="capicom_trust_is_not_time_valid"></span>**CAPICOM \_信任 \_ 不 \_ 是 \_ 時間 \_ 有效** (&H00000001) 


</dt> <dd>

此憑證或憑證鏈中的其中一個憑證的時間無效。

</dd> <dt>

<span id="CAPICOM_TRUST_IS_NOT_TIME_NESTED"></span><span id="capicom_trust_is_not_time_nested"></span>

<span id="CAPICOM_TRUST_IS_NOT_TIME_NESTED"></span><span id="capicom_trust_is_not_time_nested"></span>**CAPICOM \_信任 \_ 不 \_ 是 \_ 時間 \_ 嵌套** (&H00000002) 


</dt> <dd>

鏈中的憑證未正確地進行時間嵌套。

</dd> <dt>

<span id="CAPICOM_TRUST_IS_REVOKED"></span><span id="capicom_trust_is_revoked"></span>

<span id="CAPICOM_TRUST_IS_REVOKED"></span><span id="capicom_trust_is_revoked"></span>**CAPICOM \_ (&\_ H00000004 \_ 撤銷信任**) 


</dt> <dd>

此憑證的信任或憑證鏈中的其中一個憑證已遭撤銷。

</dd> <dt>

<span id="CAPICOM_TRUST_IS_NOT_SIGNATURE_VALID"></span><span id="capicom_trust_is_not_signature_valid"></span>

<span id="CAPICOM_TRUST_IS_NOT_SIGNATURE_VALID"></span><span id="capicom_trust_is_not_signature_valid"></span>**CAPICOM \_信任 \_ 不 \_ 是 \_ 簽名碼 \_ 有效** (&H00000008) 


</dt> <dd>

憑證或憑證鏈中的其中一個憑證沒有有效的簽章。

</dd> <dt>

<span id="CAPICOM_TRUST_IS_NOT_VALID_FOR_USAGE"></span><span id="capicom_trust_is_not_valid_for_usage"></span>

<span id="CAPICOM_TRUST_IS_NOT_VALID_FOR_USAGE"></span><span id="capicom_trust_is_not_valid_for_usage"></span>**CAPICOM \_信任 \_ 對 (&H00000010 \_ \_ \_ 的 \_ 使用** 方式無效) 


</dt> <dd>

憑證或憑證鏈的建議使用方式無效。

</dd> <dt>

<span id="CAPICOM_TRUST_IS_UNTRUSTED_ROOT"></span><span id="capicom_trust_is_untrusted_root"></span>

<span id="CAPICOM_TRUST_IS_UNTRUSTED_ROOT"></span><span id="capicom_trust_is_untrusted_root"></span>**CAPICOM \_信任 \_ 是不 \_ 受信任的 \_ 根** (&H00000020) 


</dt> <dd>

憑證或憑證鏈是以不受信任的根目錄為基礎。

</dd> <dt>

<span id="CAPICOM_TRUST_REVOCATION_STATUS_UNKNOWN"></span><span id="capicom_trust_revocation_status_unknown"></span>

<span id="CAPICOM_TRUST_REVOCATION_STATUS_UNKNOWN"></span><span id="capicom_trust_revocation_status_unknown"></span>**CAPICOM \_信任 \_ 撤銷 \_ 狀態 \_ 不明** (&H00000040) 


</dt> <dd>

憑證或憑證鏈中的其中一個憑證的撤銷狀態不明。

</dd> <dt>

<span id="CAPICOM_TRUST_IS_CYCLIC"></span><span id="capicom_trust_is_cyclic"></span>

<span id="CAPICOM_TRUST_IS_CYCLIC"></span><span id="capicom_trust_is_cyclic"></span>**CAPICOM \_信任 \_ 是 \_ 迴圈** (&H00000080) 


</dt> <dd>

鏈中的其中一個憑證是由原始憑證已認證的 [*憑證授權單位*](../secgloss/c-gly.md) 單位所發出。

</dd> <dt>

<span id="CAPICOM_TRUST_INVALID_EXTENSION"></span><span id="capicom_trust_invalid_extension"></span>

<span id="CAPICOM_TRUST_INVALID_EXTENSION"></span><span id="capicom_trust_invalid_extension"></span>**CAPICOM \_信任 \_ 不正確 \_ 延伸** 模組 (&H00000100) 


</dt> <dd>

其中一個憑證具有不正確延伸模組。

</dd> <dt>

<span id="CAPICOM_TRUST_INVALID_POLICY_CONSTRAINTS"></span><span id="capicom_trust_invalid_policy_constraints"></span>

<span id="CAPICOM_TRUST_INVALID_POLICY_CONSTRAINTS"></span><span id="capicom_trust_invalid_policy_constraints"></span>**CAPICOM \_ (&H00000200) 信任 \_ 不正確 \_ 原則 \_ 條件約束**


</dt> <dd>

憑證或憑證鏈中的其中一個憑證具有原則條件約束延伸，而其中一個已發行的憑證有不允許的原則對應延伸，或沒有必要的發佈原則延伸。

</dd> <dt>

<span id="CAPICOM_TRUST_INVALID_BASIC_CONSTRAINTS"></span><span id="capicom_trust_invalid_basic_constraints"></span>

<span id="CAPICOM_TRUST_INVALID_BASIC_CONSTRAINTS"></span><span id="capicom_trust_invalid_basic_constraints"></span>**CAPICOM \_信任 \_ 不正確 \_ 基本 \_ 條件約束** (&H00000400) 


</dt> <dd>

憑證或憑證鏈中的其中一個憑證具有基本的限制延伸，而憑證無法用來發行其他憑證，或已超過鏈路徑長度。

</dd> <dt>

<span id="CAPICOM_TRUST_INVALID_NAME_CONSTRAINTS"></span><span id="capicom_trust_invalid_name_constraints"></span>

<span id="CAPICOM_TRUST_INVALID_NAME_CONSTRAINTS"></span><span id="capicom_trust_invalid_name_constraints"></span>**CAPICOM \_信任 \_ 不正確 \_ 名稱 \_ 條件約束** (&H00000800) 


</dt> <dd>

憑證或憑證鏈中的其中一個憑證具有不正確名稱限制延伸。

</dd> <dt>

<span id="CAPICOM_TRUST_HAS_NOT_SUPPORTED_NAME_CONSTRAINT"></span><span id="capicom_trust_has_not_supported_name_constraint"></span>

<span id="CAPICOM_TRUST_HAS_NOT_SUPPORTED_NAME_CONSTRAINT"></span><span id="capicom_trust_has_not_supported_name_constraint"></span>**CAPICOM \_信任 \_ 不支援 (&H00001000) 的 \_ \_ \_ 名稱 \_ 條件約束**


</dt> <dd>

憑證或憑證鏈中的其中一個憑證具有名稱限制延伸，其包含不受支援的欄位。 不支援最小和最大欄位。 因此，最小值必須一律為零，且最大值必須一律不存在。 僅支援其他名稱的 UPN。 不支援下列替代名稱選擇：

-   X400 位址
-   EDI 合作物件名稱
-   註冊的識別碼

</dd> <dt>

<span id="CAPICOM_TRUST_HAS_NOT_DEFINED_NAME_CONSTRAINT"></span><span id="capicom_trust_has_not_defined_name_constraint"></span>

<span id="CAPICOM_TRUST_HAS_NOT_DEFINED_NAME_CONSTRAINT"></span><span id="capicom_trust_has_not_defined_name_constraint"></span>**CAPICOM \_信任 \_ \_ 未 \_ 定義 \_ 名稱 \_ 條件約束** (&H00002000) 


</dt> <dd>

憑證或憑證鏈中的其中一個憑證具有名稱限制延伸，而且在終端憑證中的其中一個名稱選擇缺少名稱條件約束。

</dd> <dt>

<span id="CAPICOM_TRUST_HAS_NOT_PERMITTED_NAME_CONSTRAINT"></span><span id="capicom_trust_has_not_permitted_name_constraint"></span>

<span id="CAPICOM_TRUST_HAS_NOT_PERMITTED_NAME_CONSTRAINT"></span><span id="capicom_trust_has_not_permitted_name_constraint"></span>**CAPICOM \_信任在 H00004000 中 \_ \_ 不 \_ 允許 \_ 名稱 \_ 條件約束** (&) 


</dt> <dd>

憑證或憑證鏈中的其中一個憑證具有名稱限制延伸，而且在終端憑證中的其中一個名稱選擇不會有允許的名稱限制。

</dd> <dt>

<span id="CAPICOM_TRUST_HAS_EXCLUDED_NAME_CONSTRAINT"></span><span id="capicom_trust_has_excluded_name_constraint"></span>

<span id="CAPICOM_TRUST_HAS_EXCLUDED_NAME_CONSTRAINT"></span><span id="capicom_trust_has_excluded_name_constraint"></span>**CAPICOM \_信任 \_ 已 \_ 排除 \_ 名稱 \_ 條件約束** (&H00008000) 


</dt> <dd>

憑證或憑證鏈中的其中一個憑證具有名稱限制延伸，而且會明確排除終端憑證中的其中一個名稱選擇。

</dd> <dt>

<span id="CAPICOM_TRUST_IS_OFFLINE_REVOCATION"></span><span id="capicom_trust_is_offline_revocation"></span>

<span id="CAPICOM_TRUST_IS_OFFLINE_REVOCATION"></span><span id="capicom_trust_is_offline_revocation"></span>**CAPICOM \_信任 \_ \_ 離線 \_ 撤銷** (&H01000000) 


</dt> <dd>

憑證的撤銷狀態，或憑證鏈中的其中一個憑證已離線或過時。

</dd> <dt>

<span id="CAPICOM_TRUST_NO_ISSUANCE_CHAIN_POLICY"></span><span id="capicom_trust_no_issuance_chain_policy"></span>

<span id="CAPICOM_TRUST_NO_ISSUANCE_CHAIN_POLICY"></span><span id="capicom_trust_no_issuance_chain_policy"></span>**CAPICOM \_ (&H02000000) 信任 \_ 無 \_ 發佈 \_ 鏈 \_ 原則**


</dt> <dd>

終端憑證沒有任何產生的發佈原則，而且其中一個發行 CA 憑證有需要的原則限制延伸。

</dd> <dt>

<span id="CAPICOM_TRUST_IS_PARTIAL_CHAIN"></span><span id="capicom_trust_is_partial_chain"></span>

<span id="CAPICOM_TRUST_IS_PARTIAL_CHAIN"></span><span id="capicom_trust_is_partial_chain"></span>**CAPICOM \_信任 \_ 是 (&H00010000 的 \_ 部分 \_ 鏈**) 


</dt> <dd>

憑證鏈不會競爭。

</dd> <dt>

<span id="CAPICOM_TRUST_CTL_IS_NOT_TIME_VALID"></span><span id="capicom_trust_ctl_is_not_time_valid"></span>

<span id="CAPICOM_TRUST_CTL_IS_NOT_TIME_VALID"></span><span id="capicom_trust_ctl_is_not_time_valid"></span>**CAPICOM \_信任 \_ CTL \_ \_ 不是 \_ 時間 \_ 有效** (&H00020000) 


</dt> <dd>

用來建立此鏈的 CTL 沒有時間有效。

</dd> <dt>

<span id="CAPICOM_TRUST_CTL_IS_NOT_SIGNATURE_VALID"></span><span id="capicom_trust_ctl_is_not_signature_valid"></span>

<span id="CAPICOM_TRUST_CTL_IS_NOT_SIGNATURE_VALID"></span><span id="capicom_trust_ctl_is_not_signature_valid"></span>**CAPICOM \_信任 \_ CTL \_ \_ 不是 \_ \_** 簽章有效 (&H00040000) 


</dt> <dd>

用來建立此鏈的 CTL 沒有有效的簽章。

</dd> <dt>

<span id="CAPICOM_TRUST_CTL_IS_NOT_VALID_FOR_USAGE"></span><span id="capicom_trust_ctl_is_not_valid_for_usage"></span>

<span id="CAPICOM_TRUST_CTL_IS_NOT_VALID_FOR_USAGE"></span><span id="capicom_trust_ctl_is_not_valid_for_usage"></span>**CAPICOM \_信賴 \_ CTL \_ 對 (&H00080000 \_ \_ \_ 的 \_ 使用** 方式無效) 


</dt> <dd>

用來建立此鏈的 CTL 對此使用方式無效。

</dd> </dl>

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|----------------------------------|----------------------------------------------------------------------------------------|
| 用戶端支援結束<br/> | Windows Vista<br/>                                                               |
| 伺服器支援結束<br/> | Windows Server 2008<br/>                                                         |
| 可轉散發套件<br/>       | Windows Server 2003 和 Windows XP 上的 CAPICOM 2.0 或更新版本<br/>                  |
| DLL<br/>                   | <dl> <dt>Capicom.dll</dt> </dl> |



 

 
