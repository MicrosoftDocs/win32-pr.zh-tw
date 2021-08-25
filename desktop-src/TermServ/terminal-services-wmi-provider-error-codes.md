---
title: '遠端桌面服務 WMI 提供者錯誤碼 (Wbemcli) '
description: 遠端桌面服務 WMI 提供者所傳回的錯誤。 如需其他 WMI 錯誤的清單，請參閱 WMI 錯誤常數。
ms.assetid: 1e68c41d-f321-4bc5-ba30-b69f5ba741eb
ms.tgt_platform: multiple
topic_type:
- apiref
api_name:
- WBEM_E_FAILED
- WBEM_E_NOT_FOUND
- WBEM_E_PROVIDER_FAILURE
- WBEM_E_TYPE_MISMATCH
- WBEM_E_OUT_OF_MEMORY
- WBEM_E_INVALID_PARAMETER
- WBEM_E_NOT_AVAILABLE
- WBEM_E_NOT_SUPPORTED
- WBEM_E_INVALID_NAMESPACE
- WBEM_E_INVALID_OBJECT
- WBEM_E_INITIALIZATION_FAILURE
- WBEM_E_INVALID_OPERATION
- WBEM_E_INVALID_QUERY
- WBEM_E_INVALID_QUERY_TYPE
- WBEM_E_ALREADY_EXISTS
- WBEM_E_INVALID_SYNTAX
- WBEM_E_READ_ONLY
- WBEM_E_PROVIDER_NOT_CAPABLE
- WBEM_E_ILLEGAL_NULL
- WBEM_E_VALUE_OUT_OF_RANGE
- WBEM_E_INVALID_METHOD
- WBEM_E_INVALID_METHOD_PARAMETERS
- WBEM_E_INVALID_OBJECT_PATH
api_location:
- Wbemcli.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f02b2c1cc07bbe9431f2d0e64252258d76de9e6f06c0d7b756b3a5af4e42bff2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119869668"
---
# <a name="remote-desktop-services-wmi-provider-error-codes"></a>遠端桌面服務 WMI 提供者錯誤碼

下列清單列出遠端桌面服務 WMI 提供者所傳回的 WMI 錯誤。 如需其他 WMI 錯誤的清單，請參閱 [**Wmi 錯誤常數**](/windows/desktop/WmiSdk/wmi-error-constants)。

<dl> <dt>

<span id="WBEM_E_FAILED"></span><span id="wbem_e_failed"></span>**WBEM \_ E \_ 失敗**
</dt> <dd> <dl> <dt>

2147749889 (0x80041001) 
</dt> <dt>



方法呼叫失敗。


</dt> </dl> </dd> <dt>

<span id="WBEM_E_NOT_FOUND"></span><span id="wbem_e_not_found"></span>**\_ \_ 找不到 WBEM E \_**
</dt> <dd> <dl> <dt>

2147749890 (0x80041002) 
</dt> <dt>



找不到物件。


</dt> </dl> </dd> <dt>

<span id="WBEM_E_PROVIDER_FAILURE"></span><span id="wbem_e_provider_failure"></span>**WBEM \_ E \_ 提供者 \_ 失敗**
</dt> <dd> <dl> <dt>

2147749892 (0x80041004) 
</dt> <dt>



在初始化期間，提供者在某個時間失敗。


</dt> </dl> </dd> <dt>

<span id="WBEM_E_TYPE_MISMATCH"></span><span id="wbem_e_type_mismatch"></span>**WBEM \_ E \_ 類型 \_ 不符**
</dt> <dd> <dl> <dt>

2147749893 (0x80041005) 
</dt> <dt>



發生類型不符的情況。


</dt> </dl> </dd> <dt>

<span id="WBEM_E_OUT_OF_MEMORY"></span><span id="wbem_e_out_of_memory"></span>**WBEM \_ E \_ \_ 記憶體不足 \_**
</dt> <dd> <dl> <dt>

2147749894 (0x80041006) 
</dt> <dt>



沒有足夠的記憶體可以進行作業。


</dt> </dl> </dd> <dt>

<span id="WBEM_E_INVALID_PARAMETER"></span><span id="wbem_e_invalid_parameter"></span>**WBEM \_ E \_ 不正確 \_ 參數**
</dt> <dd> <dl> <dt>

2147749896 (0x80041008) 
</dt> <dt>



呼叫的其中一個參數不正確。


</dt> </dl> </dd> <dt>

<span id="WBEM_E_NOT_AVAILABLE"></span><span id="wbem_e_not_available"></span>**WBEM \_ E \_ 無法 \_ 使用**
</dt> <dd> <dl> <dt>

2147749897 (0x80041009) 
</dt> <dt>



資源 (通常是遠端伺服器) 目前不可使用。


</dt> </dl> </dd> <dt>

<span id="WBEM_E_NOT_SUPPORTED"></span><span id="wbem_e_not_supported"></span>**\_ \_ 不支援 WBEM \_ E**
</dt> <dd> <dl> <dt>

2147749900 (0x8004100C) 
</dt> <dt>



功能或作業不支援。


</dt> </dl> </dd> <dt>

<span id="WBEM_E_INVALID_NAMESPACE"></span><span id="wbem_e_invalid_namespace"></span>**WBEM \_ E \_ 不正確 \_ 命名空間**
</dt> <dd> <dl> <dt>

2147749902 (0x8004100E) 
</dt> <dt>



找不到所指定的命名空間。


</dt> </dl> </dd> <dt>

<span id="WBEM_E_INVALID_OBJECT"></span><span id="wbem_e_invalid_object"></span>**WBEM \_ E \_ 不正確 \_ 物件**
</dt> <dd> <dl> <dt>

2147749903 (0x8004100F) 
</dt> <dt>



所指定的執行個體無效。


</dt> </dl> </dd> <dt>

<span id="WBEM_E_INITIALIZATION_FAILURE"></span><span id="wbem_e_initialization_failure"></span>**WBEM \_ E \_ 初始化 \_ 失敗**
</dt> <dd> <dl> <dt>

2147749908 (0x80041014) 
</dt> <dt>



模組（例如提供者）因內部原因而無法初始化。


</dt> </dl> </dd> <dt>

<span id="WBEM_E_INVALID_OPERATION"></span><span id="wbem_e_invalid_operation"></span>**WBEM \_ E \_ 不正確作業 \_**
</dt> <dd> <dl> <dt>

2147749910 (0x80041016) 
</dt> <dt>



所要求的作業無效。 這個錯誤通常發生於要刪除類別或屬性的無效嘗試。 嘗試透過群組原則控制來修改伺服器覆寫內容時，會傳回此錯誤。


</dt> </dl> </dd> <dt>

<span id="WBEM_E_INVALID_QUERY"></span><span id="wbem_e_invalid_query"></span>**WBEM \_ E \_ 不正確 \_ 查詢**
</dt> <dd> <dl> <dt>

2147749911 (0x80041017) 
</dt> <dt>



查詢的語法無效。


</dt> </dl> </dd> <dt>

<span id="WBEM_E_INVALID_QUERY_TYPE"></span><span id="wbem_e_invalid_query_type"></span>**WBEM \_ E \_ 不正確 \_ 查詢 \_ 類型**
</dt> <dd> <dl> <dt>

2147749912 (0x80041018) 
</dt> <dt>



所要求的查詢語言不支援。


</dt> </dl> </dd> <dt>

<span id="WBEM_E_ALREADY_EXISTS"></span><span id="wbem_e_already_exists"></span>**WBEM \_ E \_ 已 \_ 存在**
</dt> <dd> <dl> <dt>

2147749913 (0x80041019) 
</dt> <dt>



在 put 作業中，指定了 **wbemChangeFlagCreateOnly** 旗標，但該實例已經存在。


</dt> </dl> </dd> <dt>

<span id="WBEM_E_INVALID_SYNTAX"></span><span id="wbem_e_invalid_syntax"></span>**WBEM \_ E \_ 不正確 \_ 語法**
</dt> <dd> <dl> <dt>

2147749921 (0x80041021) 
</dt> <dt>



查詢的語法無效。


</dt> </dl> </dd> <dt>

<span id="WBEM_E_READ_ONLY"></span><span id="wbem_e_read_only"></span>**WBEM \_ E \_ 唯讀 \_**
</dt> <dd> <dl> <dt>

2147749923 (0x80041023) 
</dt> <dt>



您嘗試修改的屬性是唯讀的。


</dt> </dl> </dd> <dt>

<span id="WBEM_E_PROVIDER_NOT_CAPABLE"></span><span id="wbem_e_provider_not_capable"></span>**WBEM \_ E \_ 提供者 \_ 無法 \_ 支援**
</dt> <dd> <dl> <dt>

2147749924 (0x80041024) 
</dt> <dt>



提供者無法執行要求的作業。 作業可能包括太複雜的查詢、正在抓取實例、建立類別、更新類別、刪除類別，或列舉類別。


</dt> </dl> </dd> <dt>

<span id="WBEM_E_ILLEGAL_NULL"></span><span id="wbem_e_illegal_null"></span>**WBEM \_ E 不 \_ 合法的 \_ Null**
</dt> <dd> <dl> <dt>

2147749928 (0x80041028) 
</dt> <dt>



 / 針對不能為 null 的屬性指定的值不能是null / ****，例如由 [**索引**](/windows/desktop/WmiSdk/optional-qualifiers)[**鍵**](/windows/desktop/WmiSdk/key-qualifier)、索引或 [**非 \_ null**](/windows/desktop/WmiSdk/optional-qualifiers)限定詞標記的屬性。


</dt> </dl> </dd> <dt>

<span id="WBEM_E_VALUE_OUT_OF_RANGE"></span><span id="wbem_e_value_out_of_range"></span>**WBEM \_ E \_ 值 \_ 超出 \_ \_ 範圍**
</dt> <dd> <dl> <dt>

2147749931 (0x8004102B) 
</dt> <dt>



所提出的要求具有超出範圍的值或與型別不相容。


</dt> </dl> </dd> <dt>

<span id="WBEM_E_INVALID_METHOD"></span><span id="wbem_e_invalid_method"></span>**WBEM \_ E \_ 無效 \_ 方法**
</dt> <dd> <dl> <dt>

2147749934 (0x8004102E) 
</dt> <dt>



所要求的方法無法使用。


</dt> </dl> </dd> <dt>

<span id="WBEM_E_INVALID_METHOD_PARAMETERS"></span><span id="wbem_e_invalid_method_parameters"></span>**WBEM \_ E \_ 不正確 \_ 方法 \_ 參數**
</dt> <dd> <dl> <dt>

2147749935 (0x8004102F) 
</dt> <dt>



提供給方法的參數無效。


</dt> </dl> </dd> <dt>

<span id="WBEM_E_INVALID_OBJECT_PATH"></span><span id="wbem_e_invalid_object_path"></span>**WBEM \_ E \_ 不正確 \_ 物件 \_ 路徑**
</dt> <dd> <dl> <dt>

2147749946 (0x8004103A) 
</dt> <dt>



指定的物件路徑無效。


</dt> </dl> </dd> </dl>

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|--------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows Vista<br/>                                                             |
| 最低支援的伺服器<br/> | Windows Server 2008<br/>                                                       |
| 標頭<br/>                   | <dl> <dt>Wbemcli。h</dt> </dl> |



 

