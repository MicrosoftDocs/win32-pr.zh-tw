---
description: 如果發生錯誤，WMI 會以 HRESULT 值傳回錯誤碼。 腳本、c + + 應用程式或 Wmic 可能會傳回這些程式碼。
ms.assetid: b560f37c-da22-4745-8d1f-b27afdf572ec
ms.tgt_platform: multiple
title: 'WMI 錯誤常數 (WbemCli) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e95db7220bdc9669716dbe19f5bf2f4e139dfe5c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106974377"
---
# <a name="wmi-error-constants"></a>WMI 錯誤常數

如果發生錯誤，WMI 會以 **HRESULT** 值傳回錯誤碼。 腳本、c + + 應用程式或 [**Wmic**](wmic.md)可能會傳回這些程式碼。

> [!Note]
>
> 下列檔的目標是開發人員和 IT 系統管理員。 如果您是遇到關於 WMI 的錯誤訊息的使用者，您應該移至 [Microsoft 支援服務](https://support.microsoft.com/) 並搜尋錯誤訊息上所看到的錯誤碼。 如需有關疑難排解 WMI 腳本和 WMI 服務問題的詳細資訊，請參閱 [Wmi 無法運作！](/previous-versions/tn-archive/ff406382(v=msdn.10))。
>
> 如果 WMI 傳回錯誤訊息，請注意，它們可能不會指出 WMI 服務或 WMI 提供者中的問題。 失敗可能源自于作業系統的其他部分，並透過 WMI 出現錯誤。 在任何情況下，請勿將 WMI 儲存機制刪除為第一個動作，因為刪除存放庫可能會導致系統損毀或已安裝的應用程式。
>
> 若要取得問題來源的詳細資訊，您可以下載並執行 [WMI Diagnosis Utility](https://www.microsoft.com/downloads/en/details.aspx?familyid=d7ba3cd6-18d1-4d05-b11e-4c64192ae97d&displaylang=en) 診斷命令列工具。 這項工具會產生一份報告，通常可以找出問題的來源，並提供如何修正問題的指示。 報表也會協助 Microsoft 支援服務協助您。 您可以在 [這裡](https://www.microsoft.com/downloads/details.aspx?FamilyID=d7ba3cd6-18d1-4d05-b11e-4c64192ae97d)下載 WMI Diagnosis Utility。

 

WMI 類別中的某些方法可以傳回系統和網路錯誤碼 (64，例如) 。 您可以在 [命令提示字元] 視窗中，使用 **net helpmsg** 命令檢查這些類型之錯誤碼的定義。 例如， **net helpmsg 64** 命令會傳回訊息：指定的網路名稱已無法再使用。

下列清單列出一些常見的錯誤範圍。

<dl> <dt>

<span id="0x80041068_-_0x80041099"></span><span id="0X80041068_-_0X80041099"></span>0x80041068 - 0x80041099
</dt> <dd>

源自 WMI 本身的錯誤。

特定 WMI 作業失敗，因為

-   要求中發生錯誤，例如 WQL 查詢失敗或帳戶沒有正確的許可權。
-   WMI 基礎結構問題，例如不正確的 CIM 或 DCOM 註冊。

</dd> <dt>

<span id="0x8007xxxx"></span><span id="0X8007XXXX"></span>0x8007xxxx
</dt> <dd>

源自核心作業系統的錯誤。 WMI 可能會因為外部失敗而傳回此類型的錯誤，例如 DCOM 安全性失敗。

</dd> <dt>

<span id="0x80040xxx"></span><span id="0X80040XXX"></span>0x80040xxx
</dt> <dd>

源自 DCOM 的錯誤。 例如，遠端電腦的作業 DCOM 設定可能不正確。

</dd> <dt>

<span id="0x8005xxxx"></span><span id="0X8005XXXX"></span>0x8005xxxx
</dt> <dd>

源自 ADSI (Active Directory 服務介面的錯誤) 或 LDAP (輕量型目錄存取協定) ，例如，使用 WMI Active Directory 提供者時 Active Directory 存取失敗。

</dd> </dl>

WMI 類別中的某些方法可以傳回系統和網路錯誤碼 (64，例如) 。 您可以在 [命令提示字元] 視窗中，使用 **net helpmsg** 命令檢查這些類型之錯誤碼的定義。 例如， **net helpmsg 64** 命令會傳回訊息：指定的網路名稱已無法再使用。 在 c + + 中，您可以呼叫 [**FormatMessage**](/windows/desktop/api/winbase/nf-winbase-formatmessage) 並指定 **C： \\ Windows \\ System32 \\ wbem \\wmiutils.dll** 作為訊息模組。

<dl> <dt>

<span id="WBEM_E_FAILED"></span><span id="wbem_e_failed"></span>**WBEM \_ E \_ 失敗**
</dt> <dd> <dl> <dt>

2147749889 (0x80041001) 
</dt> <dt>



呼叫失敗。


</dt> </dl> </dd> <dt>

<span id="WBEM_E_NOT_FOUND"></span><span id="wbem_e_not_found"></span>**\_ \_ 找不到 WBEM E \_**
</dt> <dd> <dl> <dt>

2147749890 (0x80041002) 
</dt> <dt>



找不到物件。


</dt> </dl> </dd> <dt>

<span id="WBEM_E_ACCESS_DENIED"></span><span id="wbem_e_access_denied"></span>**WBEM \_ E \_ \_ 拒絕存取**
</dt> <dd> <dl> <dt>

2147749891 (0x80041003) 
</dt> <dt>



目前的使用者沒有執行此動作的許可權。


</dt> </dl> </dd> <dt>

<span id="WBEM_E_PROVIDER_FAILURE"></span><span id="wbem_e_provider_failure"></span>**WBEM \_ E \_ 提供者 \_ 失敗**
</dt> <dd> <dl> <dt>

2147749892 (0x80041004) 
</dt> <dt>



在初始化期間，提供者在某些時間失敗。


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



記憶體不足，無法運作。


</dt> </dl> </dd> <dt>

<span id="WBEM_E_INVALID_CONTEXT"></span><span id="wbem_e_invalid_context"></span>**WBEM \_ E \_ 不正確 \_ 內容**
</dt> <dd> <dl> <dt>

2147749895 (0x80041007) 
</dt> <dt>



[**IWbemCoNtext**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemcontext)物件無效。


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



資源（通常是遠端伺服器）目前無法使用。


</dt> </dl> </dd> <dt>

<span id="WBEM_E_CRITICAL_ERROR"></span><span id="wbem_e_critical_error"></span>**WBEM \_ E \_ 重大 \_ 錯誤**
</dt> <dd> <dl> <dt>

2147749898 (0x8004100A) 
</dt> <dt>



發生內部、重大和非預期的錯誤。 向 Microsoft 技術支援人員回報錯誤。


</dt> </dl> </dd> <dt>

<span id="WBEM_E_INVALID_STREAM"></span><span id="wbem_e_invalid_stream"></span>**WBEM \_ E \_ 不正確 \_ 資料流程**
</dt> <dd> <dl> <dt>

2147749899 (0x8004100B) 
</dt> <dt>



一個或多個網路封包在遠端工作階段 (Session) 期間損毀。


</dt> </dl> </dd> <dt>

<span id="WBEM_E_NOT_SUPPORTED"></span><span id="wbem_e_not_supported"></span>**\_ \_ 不支援 WBEM \_ E**
</dt> <dd> <dl> <dt>

2147749900 (0x8004100C) 
</dt> <dt>



不支援功能或操作。


</dt> </dl> </dd> <dt>

<span id="WBEM_E_INVALID_SUPERCLASS"></span><span id="wbem_e_invalid_superclass"></span>**WBEM \_ E \_ 不正確 \_ 超類**
</dt> <dd> <dl> <dt>

2147749901 (0x8004100D) 
</dt> <dt>



指定的父類別無效。


</dt> </dl> </dd> <dt>

<span id="WBEM_E_INVALID_NAMESPACE"></span><span id="wbem_e_invalid_namespace"></span>**WBEM \_ E \_ 不正確 \_ 命名空間**
</dt> <dd> <dl> <dt>

2147749902 (0x8004100E) 
</dt> <dt>



找不到指定的命名空間。


</dt> </dl> </dd> <dt>

<span id="WBEM_E_INVALID_OBJECT"></span><span id="wbem_e_invalid_object"></span>**WBEM \_ E \_ 不正確 \_ 物件**
</dt> <dd> <dl> <dt>

2147749903 (0x8004100F) 
</dt> <dt>



指定的實例無效。


</dt> </dl> </dd> <dt>

<span id="WBEM_E_INVALID_CLASS"></span><span id="wbem_e_invalid_class"></span>**WBEM \_ E \_ 無效 \_ 類別**
</dt> <dd> <dl> <dt>

2147749904 (0x80041010) 
</dt> <dt>



指定的類別無效。


</dt> </dl> </dd> <dt>

<span id="WBEM_E_PROVIDER_NOT_FOUND"></span><span id="wbem_e_provider_not_found"></span>**\_ \_ \_ 找不到 WBEM E 提供者 \_**
</dt> <dd> <dl> <dt>

2147749905 (0x80041011) 
</dt> <dt>



架構中參考的提供者沒有相對應的註冊。


</dt> </dl> </dd> <dt>

<span id="WBEM_E_INVALID_PROVIDER_REGISTRATION"></span><span id="wbem_e_invalid_provider_registration"></span>**WBEM \_ E \_ 不正確 \_ 提供者 \_ 註冊**
</dt> <dd> <dl> <dt>

2147749906
</dt> <dt>



架構中所參考的提供者的註冊不正確或不完整。

這項錯誤可能是由許多狀況所造成，包括下列各項：

-   在用來註冊提供者的受控物件格式 (MOF) 檔中遺漏[ \# pragma namespace](pragma-namespace.md)命令。 提供者可能會在錯誤的 WMI 命名空間中註冊。
-   無法取出 COM 註冊。
-   裝載模型無效。 如需詳細資訊，請參閱 [提供者裝載和安全性](provider-hosting-and-security.md)。
-   註冊中指定的類別無效。
-   無法建立的實例或繼承自 [**\_ \_ Win32Provider**](--win32provider.md)類別，以便在 MOF 檔案中建立提供者註冊。


</dt> </dl> </dd> <dt>

<span id="WBEM_E_PROVIDER_LOAD_FAILURE"></span><span id="wbem_e_provider_load_failure"></span>**WBEM \_ E \_ 提供者 \_ 載入 \_ 失敗**
</dt> <dd> <dl> <dt>

2147749907 (0x80041013) 
</dt> <dt>



COM 無法找到結構描述中所參考的提供者。

這項錯誤可能是由許多狀況所造成，包括下列各項：

-   提供者使用的 WMI DLL 不符合建立提供者時所使用的 .lib 檔案。
-   提供者的 DLL 或其相依的任何 Dll 已損毀。
-   提供者無法匯出 [**DllRegisterServer**](/windows/win32/api/olectl/nf-olectl-dllregisterserver)。
-   未使用 **regsvr32** 命令註冊同進程提供者。
-   未使用 **/regserver** 參數註冊跨進程提供者。 例如， **myprog.exe/regserver**。


</dt> </dl> </dd> <dt>

<span id="WBEM_E_INITIALIZATION_FAILURE"></span><span id="wbem_e_initialization_failure"></span>**WBEM \_ E \_ 初始化 \_ 失敗**
</dt> <dd> <dl> <dt>

2147749908 (0x80041014) 
</dt> <dt>



元件（例如提供者）因內部原因而無法初始化。


</dt> </dl> </dd> <dt>

<span id="WBEM_E_TRANSPORT_FAILURE"></span><span id="wbem_e_transport_failure"></span>**WBEM \_ E \_ 傳輸 \_ 失敗**
</dt> <dd> <dl> <dt>

2147749909 (0x80041015) 
</dt> <dt>



防止正常操作發生的網路錯誤。


</dt> </dl> </dd> <dt>

<span id="WBEM_E_INVALID_OPERATION"></span><span id="wbem_e_invalid_operation"></span>**WBEM \_ E \_ 不正確作業 \_**
</dt> <dd> <dl> <dt>

2147749910 (0x80041016) 
</dt> <dt>



要求的作業無效。 這個錯誤通常發生於要刪除類別或屬性的無效嘗試。


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



不支援要求的查詢語言。


</dt> </dl> </dd> <dt>

<span id="WBEM_E_ALREADY_EXISTS"></span><span id="wbem_e_already_exists"></span>**WBEM \_ E \_ 已 \_ 存在**
</dt> <dd> <dl> <dt>

2147749913 (0x80041019) 
</dt> <dt>



在 put 作業中，指定了 **wbemChangeFlagCreateOnly** 旗標，但該實例已經存在。


</dt> </dl> </dd> <dt>

<span id="WBEM_E_OVERRIDE_NOT_ALLOWED"></span><span id="wbem_e_override_not_allowed"></span>**\_ \_ \_ 不 \_ 允許使用 WBEM E 覆寫**
</dt> <dd> <dl> <dt>

2147749914 (0x8004101A) 
</dt> <dt>



因為擁有物件不允許覆寫，所以無法對此限定詞執行加入作業。


</dt> </dl> </dd> <dt>

<span id="WBEM_E_PROPAGATED_QUALIFIER"></span><span id="wbem_e_propagated_qualifier"></span>**WBEM \_ E 已 \_ 傳播 \_ 限定詞**
</dt> <dd> <dl> <dt>

2147749915 (0x8004101B) 
</dt> <dt>



使用者嘗試刪除未擁有的辨識符號。 限定詞繼承自父代類別。


</dt> </dl> </dd> <dt>

<span id="WBEM_E_PROPAGATED_PROPERTY"></span><span id="wbem_e_propagated_property"></span>**WBEM \_ E 已 \_ 傳播 \_ 屬性**
</dt> <dd> <dl> <dt>

2147749916 (0x8004101C) 
</dt> <dt>



使用者嘗試刪除未擁有的屬性。 屬性繼承自父代 (Parent) 類別。


</dt> </dl> </dd> <dt>

<span id="WBEM_E_UNEXPECTED"></span><span id="wbem_e_unexpected"></span>**WBEM \_ E 未 \_ 預期**
</dt> <dd> <dl> <dt>

2147749917 (0x8004101D) 
</dt> <dt>



用戶端進行了非預期和不合法的呼叫順序，例如在呼叫 [**BeginEnumeration**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-beginenumeration)之前呼叫 [**EndEnumeration**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-endenumeration) 。


</dt> </dl> </dd> <dt>

<span id="WBEM_E_ILLEGAL_OPERATION"></span><span id="wbem_e_illegal_operation"></span>**WBEM \_ E 不 \_ 合法的 \_ 作業**
</dt> <dd> <dl> <dt>

2147749918 (0x8004101E) 
</dt> <dt>



使用者要求了不合法的操作，例如從實例產生類別。


</dt> </dl> </dd> <dt>

<span id="WBEM_E_CANNOT_BE_KEY"></span><span id="wbem_e_cannot_be_key"></span>**WBEM \_ E \_ 不 \_ 可以是索引 \_ 鍵**
</dt> <dd> <dl> <dt>

2147749919 (0x8004101F) 
</dt> <dt>



在不能是索引鍵的屬性上指定索引鍵限定詞的行為不合法。 索引鍵會在物件的類別定義中指定，並且不能對每個執行個體進行變更。


</dt> </dl> </dd> <dt>

<span id="WBEM_E_INCOMPLETE_CLASS"></span><span id="wbem_e_incomplete_class"></span>**WBEM \_ E \_ 未完成 \_ 類別**
</dt> <dd> <dl> <dt>

2147749920 (0x80041020) 
</dt> <dt>



目前的物件不是有效的類別定義。 可能是未完成，或尚未使用 [**SWbemObject \_**](swbemobject-put-.md)向 WMI 註冊。


</dt> </dl> </dd> <dt>

<span id="WBEM_E_INVALID_SYNTAX"></span><span id="wbem_e_invalid_syntax"></span>**WBEM \_ E \_ 不正確 \_ 語法**
</dt> <dd> <dl> <dt>

2147749921 (0x80041021) 
</dt> <dt>



查詢的語法無效。


</dt> </dl> </dd> <dt>

<span id="WBEM_E_NONDECORATED_OBJECT"></span><span id="wbem_e_nondecorated_object"></span>**WBEM \_ E \_ NONDECORATED \_ 物件**
</dt> <dd> <dl> <dt>

2147749922 (0x80041022) 
</dt> <dt>



保留供未來使用。


</dt> </dl> </dd> <dt>

<span id="WBEM_E_READ_ONLY"></span><span id="wbem_e_read_only"></span>**WBEM \_ E \_ 唯讀 \_**
</dt> <dd> <dl> <dt>

2147749923 (0x80041023) 
</dt> <dt>



已嘗試修改唯讀屬性。


</dt> </dl> </dd> <dt>

<span id="WBEM_E_PROVIDER_NOT_CAPABLE"></span><span id="wbem_e_provider_not_capable"></span>**WBEM \_ E \_ 提供者 \_ 無法 \_ 支援**
</dt> <dd> <dl> <dt>

2147749924 (0x80041024) 
</dt> <dt>



提供者無法執行要求的作業。 這可能包括太複雜的查詢、如何取出實例、建立或更新類別、刪除類別，或列舉類別。


</dt> </dl> </dd> <dt>

<span id="WBEM_E_CLASS_HAS_CHILDREN"></span><span id="wbem_e_class_has_children"></span>**WBEM \_ E \_ 類別 \_ 具有 \_ 子系**
</dt> <dd> <dl> <dt>

2147749925 (0x80041025) 
</dt> <dt>



嘗試進行變更，使子類別失效。


</dt> </dl> </dd> <dt>

<span id="WBEM_E_CLASS_HAS_INSTANCES"></span><span id="wbem_e_class_has_instances"></span>**WBEM \_ E \_ 類別 \_ 具有 \_ 實例**
</dt> <dd> <dl> <dt>

2147749926 (0x80041026) 
</dt> <dt>



嘗試刪除或修改具有實例的類別。


</dt> </dl> </dd> <dt>

<span id="WBEM_E_QUERY_NOT_IMPLEMENTED"></span><span id="wbem_e_query_not_implemented"></span>**\_ \_ \_ 未執行 WBEM E \_ 查詢**
</dt> <dd> <dl> <dt>

2147749927 (0x80041027) 
</dt> <dt>



保留供未來使用。


</dt> </dl> </dd> <dt>

<span id="WBEM_E_ILLEGAL_NULL"></span><span id="wbem_e_illegal_null"></span>**WBEM \_ E 不 \_ 合法的 \_ Null**
</dt> <dd> <dl> <dt>

2147749928 (0x80041028) 
</dt> <dt>



針對必須具有值的屬性指定了 Nothing/**Null** 值，例如由 [**索引**](optional-qualifiers.md)[**鍵**](key-qualifier.md)、索引或 **非 \_ Null** 限定詞標記的屬性。


</dt> </dl> </dd> <dt>

<span id="WBEM_E_INVALID_QUALIFIER_TYPE"></span><span id="wbem_e_invalid_qualifier_type"></span>**WBEM \_ E \_ 不正確辨識 \_ 符號 \_ 類型**
</dt> <dd> <dl> <dt>

2147749929 (0x80041029) 
</dt> <dt>



提供的限定詞變數值不是合法的辨識符號類型。


</dt> </dl> </dd> <dt>

<span id="WBEM_E_INVALID_PROPERTY_TYPE"></span><span id="wbem_e_invalid_property_type"></span>**WBEM \_ E \_ 不正確 \_ 屬性 \_ 類型**
</dt> <dd> <dl> <dt>

2147749930 (0x8004102A) 
</dt> <dt>



為屬性指定的 CIM 類型無效。


</dt> </dl> </dd> <dt>

<span id="WBEM_E_VALUE_OUT_OF_RANGE"></span><span id="wbem_e_value_out_of_range"></span>**WBEM \_ E \_ 值 \_ 超出 \_ \_ 範圍**
</dt> <dd> <dl> <dt>

2147749931 (0x8004102B) 
</dt> <dt>



以超出範圍的值提出要求，或其與類型不相容。


</dt> </dl> </dd> <dt>

<span id="WBEM_E_CANNOT_BE_SINGLETON"></span><span id="wbem_e_cannot_be_singleton"></span>**WBEM \_ E \_ 不 \_ 可以是 \_ 單一**
</dt> <dd> <dl> <dt>

2147749932 (0x8004102C) 
</dt> <dt>



嘗試使類別成為 singleton，例如從非 singleton 類別衍生類別時。


</dt> </dl> </dd> <dt>

<span id="WBEM_E_INVALID_CIM_TYPE"></span><span id="wbem_e_invalid_cim_type"></span>**WBEM \_ E \_ 不正確 \_ CIM \_ 類型**
</dt> <dd> <dl> <dt>

2147749933 (0x8004102D) 
</dt> <dt>



指定的 CIM 類型無效。


</dt> </dl> </dd> <dt>

<span id="WBEM_E_INVALID_METHOD"></span><span id="wbem_e_invalid_method"></span>**WBEM \_ E \_ 無效 \_ 方法**
</dt> <dd> <dl> <dt>

2147749934 (0x8004102E) 
</dt> <dt>



無法使用要求的方法。


</dt> </dl> </dd> <dt>

<span id="WBEM_E_INVALID_METHOD_PARAMETERS"></span><span id="wbem_e_invalid_method_parameters"></span>**WBEM \_ E \_ 不正確 \_ 方法 \_ 參數**
</dt> <dd> <dl> <dt>

2147749935 (0x8004102F) 
</dt> <dt>



為方法提供的參數無效。


</dt> </dl> </dd> <dt>

<span id="WBEM_E_SYSTEM_PROPERTY"></span><span id="wbem_e_system_property"></span>**WBEM \_ E \_ 系統 \_ 屬性**
</dt> <dd> <dl> <dt>

2147749936 (0x80041030) 
</dt> <dt>



嘗試取得系統屬性上的限定詞。


</dt> </dl> </dd> <dt>

<span id="WBEM_E_INVALID_PROPERTY"></span><span id="wbem_e_invalid_property"></span>**WBEM \_ E \_ 不正確 \_ 屬性**
</dt> <dd> <dl> <dt>

2147749937 (0x80041031) 
</dt> <dt>



無法辨識屬性類型。


</dt> </dl> </dd> <dt>

<span id="WBEM_E_CALL_CANCELLED"></span><span id="wbem_e_call_cancelled"></span>**已 \_ 取消 WBEM E \_ 通話 \_**
</dt> <dd> <dl> <dt>

2147749938 (0x80041032) 
</dt> <dt>



非同步處理已在內部或由使用者取消。 請注意，由於非同步作業的時間和本質，此作業可能未真正取消。


</dt> </dl> </dd> <dt>

<span id="WBEM_E_SHUTTING_DOWN"></span><span id="wbem_e_shutting_down"></span>**WBEM \_ E \_ 關機 \_**
</dt> <dd> <dl> <dt>

2147749939 (0x80041033) 
</dt> <dt>



當 WMI 正在關機的過程中，使用者已要求操作。


</dt> </dl> </dd> <dt>

<span id="WBEM_E_PROPAGATED_METHOD"></span><span id="wbem_e_propagated_method"></span>**WBEM \_ E \_ 傳播 \_ 方法**
</dt> <dd> <dl> <dt>

2147749940 (0x80041034) 
</dt> <dt>



嘗試從父類別重複使用現有的方法名稱，但簽章不相符。


</dt> </dl> </dd> <dt>

<span id="WBEM_E_UNSUPPORTED_PARAMETER"></span><span id="wbem_e_unsupported_parameter"></span>**WBEM \_ E \_ 不支援的 \_ 參數**
</dt> <dd> <dl> <dt>

2147749941 (0x80041035) 
</dt> <dt>



一個或多個參數值 (例如查詢文字) 過於複雜或不支援。 因此，會要求 WMI 以較簡單的參數重試此操作。


</dt> </dl> </dd> <dt>

<span id="WBEM_E_MISSING_PARAMETER_ID"></span><span id="wbem_e_missing_parameter_id"></span>**WBEM \_ E \_ 缺少 \_ 參數 \_ 識別碼**
</dt> <dd> <dl> <dt>

2147749942 (0x80041036) 
</dt> <dt>



方法呼叫中遺漏參數。


</dt> </dl> </dd> <dt>

<span id="WBEM_E_INVALID_PARAMETER_ID"></span><span id="wbem_e_invalid_parameter_id"></span>**WBEM \_ E \_ 不正確 \_ 參數 \_ 識別碼**
</dt> <dd> <dl> <dt>

2147749943 (0x80041037) 
</dt> <dt>



方法參數有不正確 [**識別碼**](standard-wmi-qualifiers.md) 限定詞。


</dt> </dl> </dd> <dt>

<span id="WBEM_E_NONCONSECUTIVE_PARAMETER_IDS"></span><span id="wbem_e_nonconsecutive_parameter_ids"></span>**WBEM \_ E 不 \_ 連續的 \_ 參數 \_ 識別碼**
</dt> <dd> <dl> <dt>

2147749944 (0x80041038) 
</dt> <dt>



有一或多個方法參數的 [**識別碼**](standard-wmi-qualifiers.md) 限定詞不是順序。


</dt> </dl> </dd> <dt>

<span id="WBEM_E_PARAMETER_ID_ON_RETVAL"></span><span id="wbem_e_parameter_id_on_retval"></span>**\_ \_ \_ \_ RETVAL 上的 WBEM E 參數識別碼 \_**
</dt> <dd> <dl> <dt>

2147749945 (0x80041039) 
</dt> <dt>



方法的傳回值具有 [**識別碼**](standard-wmi-qualifiers.md) 辨識符號。


</dt> </dl> </dd> <dt>

<span id="WBEM_E_INVALID_OBJECT_PATH"></span><span id="wbem_e_invalid_object_path"></span>**WBEM \_ E \_ 不正確 \_ 物件 \_ 路徑**
</dt> <dd> <dl> <dt>

2147749946 (0x8004103A) 
</dt> <dt>



指定的物件路徑無效。


</dt> </dl> </dd> <dt>

<span id="WBEM_E_OUT_OF_DISK_SPACE"></span><span id="wbem_e_out_of_disk_space"></span>**WBEM \_ E \_ \_ \_ 磁碟空間不足 \_**
</dt> <dd> <dl> <dt>

2147749947 (0x8004103B) 
</dt> <dt>



磁碟空間不足，或已達到 (CIM 存放庫) 大小的 WMI 儲存機制的 4 GB 限制。


</dt> </dl> </dd> <dt>

<span id="WBEM_E_BUFFER_TOO_SMALL"></span><span id="wbem_e_buffer_too_small"></span>**WBEM \_ E \_ 緩衝區 \_ 太 \_ 小**
</dt> <dd> <dl> <dt>

2147749948 (0x8004103C) 
</dt> <dt>



提供的緩衝區太小，無法容納列舉值中的所有物件，或無法讀取字串屬性。


</dt> </dl> </dd> <dt>

<span id="WBEM_E_UNSUPPORTED_PUT_EXTENSION"></span><span id="wbem_e_unsupported_put_extension"></span>**WBEM \_ E \_ 不支援的 \_ PUT \_ 延伸模組**
</dt> <dd> <dl> <dt>

2147749949 (0x8004103D) 
</dt> <dt>



提供者不支援要求的 put 作業。


</dt> </dl> </dd> <dt>

<span id="WBEM_E_UNKNOWN_OBJECT_TYPE"></span><span id="wbem_e_unknown_object_type"></span>**WBEM \_ E \_ 未知的 \_ 物件 \_ 類型**
</dt> <dd> <dl> <dt>

2147749950 (0x8004103E) 
</dt> <dt>



封送處理期間遇到不正確類型或版本的物件。


</dt> </dl> </dd> <dt>

<span id="WBEM_E_UNKNOWN_PACKET_TYPE"></span><span id="wbem_e_unknown_packet_type"></span>**WBEM \_ E \_ 未知的封 \_ 包 \_ 類型**
</dt> <dd> <dl> <dt>

2147749951 (0x8004103F) 
</dt> <dt>



封送處理期間遇到不正確類型或版本的封包。


</dt> </dl> </dd> <dt>

<span id="WBEM_E_MARSHAL_VERSION_MISMATCH"></span><span id="wbem_e_marshal_version_mismatch"></span>**WBEM \_ E \_ 封送處理 \_ 版本 \_ 不符**
</dt> <dd> <dl> <dt>

2147749952 (0x80041040) 
</dt> <dt>



封包有不支援的版本。


</dt> </dl> </dd> <dt>

<span id="WBEM_E_MARSHAL_INVALID_SIGNATURE"></span><span id="wbem_e_marshal_invalid_signature"></span>**WBEM \_ E \_ 封送處理 \_ 無效 \_ 的簽章**
</dt> <dd> <dl> <dt>

2147749953 (0x80041041) 
</dt> <dt>



封包似乎已損毀。


</dt> </dl> </dd> <dt>

<span id="WBEM_E_INVALID_QUALIFIER"></span><span id="wbem_e_invalid_qualifier"></span>**WBEM \_ E \_ 不正確辨識 \_ 符號**
</dt> <dd> <dl> <dt>

2147749954 (0x80041042) 
</dt> <dt>



嘗試不相符的限定詞，例如 \[ 在物件上放置索引鍵， \] 而不是在屬性上進行。


</dt> </dl> </dd> <dt>

<span id="WBEM_E_INVALID_DUPLICATE_PARAMETER"></span><span id="wbem_e_invalid_duplicate_parameter"></span>**WBEM \_ E \_ 不正確 \_ 重複 \_ 參數**
</dt> <dd> <dl> <dt>

2147749955 (0x80041043) 
</dt> <dt>



在 CIM 方法中宣告了重複的參數。


</dt> </dl> </dd> <dt>

<span id="WBEM_E_TOO_MUCH_DATA"></span><span id="wbem_e_too_much_data"></span>**WBEM \_ 電子 \_ \_ 資料太多 \_**
</dt> <dd> <dl> <dt>

2147749956 (0x80041044) 
</dt> <dt>



保留供未來使用。


</dt> </dl> </dd> <dt>

<span id="WBEM_E_SERVER_TOO_BUSY"></span><span id="wbem_e_server_too_busy"></span>**WBEM \_ E \_ SERVER \_ 太 \_ 忙碌**
</dt> <dd> <dl> <dt>

2147749957 (0x80041045) 
</dt> <dt>



[**IWbemObjectSink：：表示**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemobjectsink-indicate)的呼叫失敗。 提供者可以 refire 事件。


</dt> </dl> </dd> <dt>

<span id="WBEM_E_INVALID_FLAVOR"></span><span id="wbem_e_invalid_flavor"></span>**WBEM \_ E \_ 不正確類別 \_**
</dt> <dd> <dl> <dt>

2147749958 (0x80041046) 
</dt> <dt>



指定的限定詞類別無效。


</dt> </dl> </dd> <dt>

<span id="WBEM_E_CIRCULAR_REFERENCE"></span><span id="wbem_e_circular_reference"></span>**WBEM \_ E \_ 迴圈 \_ 參考**
</dt> <dd> <dl> <dt>

2147749959 (0x80041047) 
</dt> <dt>



嘗試建立迴圈 (的參考，例如，衍生類別本身) 。


</dt> </dl> </dd> <dt>

<span id="WBEM_E_UNSUPPORTED_CLASS_UPDATE"></span><span id="wbem_e_unsupported_class_update"></span>**WBEM \_ E \_ 不支援的 \_ 類別 \_ 更新**
</dt> <dd> <dl> <dt>

2147749960 (0x80041048) 
</dt> <dt>



不支援指定的類別。


</dt> </dl> </dd> <dt>

<span id="WBEM_E_CANNOT_CHANGE_KEY_INHERITANCE"></span><span id="wbem_e_cannot_change_key_inheritance"></span>**WBEM \_ E \_ 無法 \_ 變更 \_ 金鑰 \_ 繼承**
</dt> <dd> <dl> <dt>

2147749961 (0x80041049) 
</dt> <dt>



嘗試在實例或子類別已使用金鑰時變更金鑰。


</dt> </dl> </dd> <dt>

<span id="WBEM_E_CANNOT_CHANGE_INDEX_INHERITANCE"></span><span id="wbem_e_cannot_change_index_inheritance"></span>**WBEM \_ E \_ 無法 \_ 變更 \_ 索引 \_ 繼承**
</dt> <dd> <dl> <dt>

2147749968 (0x80041050) 
</dt> <dt>



當實例或子類別已經在使用索引時，嘗試變更索引。


</dt> </dl> </dd> <dt>

<span id="WBEM_E_TOO_MANY_PROPERTIES"></span><span id="wbem_e_too_many_properties"></span>**WBEM \_ E \_ 的 \_ 屬性太多 \_**
</dt> <dd> <dl> <dt>

2147749969 (0x80041051) 
</dt> <dt>



嘗試建立的屬性多於目前版本類別所支援的屬性。


</dt> </dl> </dd> <dt>

<span id="WBEM_E_UPDATE_TYPE_MISMATCH"></span><span id="wbem_e_update_type_mismatch"></span>**WBEM \_ E \_ 更新 \_ 類型 \_ 不符**
</dt> <dd> <dl> <dt>

2147749970 (0x80041052) 
</dt> <dt>



在衍生類別中重新定義了具有衝突類型的屬性。


</dt> </dl> </dd> <dt>

<span id="WBEM_E_UPDATE_OVERRIDE_NOT_ALLOWED"></span><span id="wbem_e_update_override_not_allowed"></span>**\_ \_ \_ \_ 不 \_ 允許使用 WBEM E 更新覆寫**
</dt> <dd> <dl> <dt>

2147749971 (0x80041053) 
</dt> <dt>



嘗試在衍生類別中進行覆寫無法覆寫的辨識符號。


</dt> </dl> </dd> <dt>

<span id="WBEM_E_UPDATE_PROPAGATED_METHOD"></span><span id="wbem_e_update_propagated_method"></span>**WBEM \_ E \_ 更新 \_ 傳播 \_ 方法**
</dt> <dd> <dl> <dt>

2147749972 (0x80041054) 
</dt> <dt>



已使用衍生類別中的衝突簽章重新宣告方法。


</dt> </dl> </dd> <dt>

<span id="WBEM_E_METHOD_NOT_IMPLEMENTED"></span><span id="wbem_e_method_not_implemented"></span>**WBEM \_ E \_ 方法 \_ 未 \_ 執行**
</dt> <dd> <dl> <dt>

2147749973 (0x80041055) 
</dt> <dt>



嘗試執行未標示為 \[ \] 在任何相關類別中執行的方法。


</dt> </dl> </dd> <dt>

<span id="WBEM_E_METHOD_DISABLED"></span><span id="wbem_e_method_disabled"></span>**\_ \_ \_ 已停用 WBEM E 方法**
</dt> <dd> <dl> <dt>


</dt> <dt>



嘗試執行標示為停用的方法 \[ \] 。


</dt> </dl> </dd> <dt>

<span id="WBEM_E_REFRESHER_BUSY"></span><span id="wbem_e_refresher_busy"></span>**WBEM \_ E \_ 複習複習 \_ 忙碌**
</dt> <dd> <dl> <dt>

2147749975 (0x80041057) 
</dt> <dt>



重新整理程式正忙於其他作業。


</dt> </dl> </dd> <dt>

<span id="WBEM_E_UNPARSABLE_QUERY"></span><span id="wbem_e_unparsable_query"></span>**WBEM E 無法剖析的 \_ \_ \_ 查詢**
</dt> <dd> <dl> <dt>

2147749976 (0x80041058) 
</dt> <dt>



篩選查詢的語法無效。


</dt> </dl> </dd> <dt>

<span id="WBEM_E_NOT_EVENT_CLASS"></span><span id="wbem_e_not_event_class"></span>**WBEM \_ E \_ NOT \_ 事件 \_ 類別**
</dt> <dd> <dl> <dt>

2147749977 (0x80041059) 
</dt> <dt>



篩選查詢的 FROM 子句參考的類別不是事件類別， (並非衍生自 [**\_ \_ 事件**](--event.md)) 。


</dt> </dl> </dd> <dt>

<span id="WBEM_E_MISSING_GROUP_WITHIN"></span><span id="wbem_e_missing_group_within"></span>**WBEM \_ E \_ 遺失 \_ 群組 \_**
</dt> <dd> <dl> <dt>

2147749978 (0x8004105A) 
</dt> <dt>



使用 GROUP BY 子句，而不使用對應的 GROUP WITHIN 子句。


</dt> </dl> </dd> <dt>

<span id="WBEM_E_MISSING_AGGREGATION_LIST"></span><span id="wbem_e_missing_aggregation_list"></span>**WBEM \_ E \_ 遺失 \_ 匯總 \_ 清單**
</dt> <dd> <dl> <dt>

2147749979 (0x8004105B) 
</dt> <dt>



使用 GROUP BY 子句。 不支援所有屬性的彙總 (Aggregation)。


</dt> </dl> </dd> <dt>

<span id="WBEM_E_PROPERTY_NOT_AN_OBJECT"></span><span id="wbem_e_property_not_an_object"></span>**WBEM \_ E \_ 屬性 \_ 不 \_ 是 \_ 物件**
</dt> <dd> <dl> <dt>

2147749980 (0x8004105C) 
</dt> <dt>



點標記法使用於不是內嵌物件的屬性上。


</dt> </dl> </dd> <dt>

<span id="WBEM_E_AGGREGATING_BY_OBJECT"></span><span id="wbem_e_aggregating_by_object"></span>**\_ \_ \_ 以物件匯總的 WBEM E \_**
</dt> <dd> <dl> <dt>

2147749981 (0x8004105D) 
</dt> <dt>



GROUP BY 子句不使用點標記法參考做為內嵌物件 (Embedded Object) 的屬性。


</dt> </dl> </dd> <dt>

<span id="WBEM_E_UNINTERPRETABLE_PROVIDER_QUERY"></span><span id="wbem_e_uninterpretable_provider_query"></span>**WBEM \_ E \_ UNINTERPRETABLE \_ 提供者 \_ 查詢**
</dt> <dd> <dl> <dt>

2147749983 (0x8004105F) 
</dt> <dt>



事件提供者註冊查詢 ([**\_ \_ EventProviderRegistration**](--eventproviderregistration.md)) 未指定提供事件的類別。


</dt> </dl> </dd> <dt>

<span id="WBEM_E_BACKUP_RESTORE_WINMGMT_RUNNING"></span><span id="wbem_e_backup_restore_winmgmt_running"></span>**WBEM \_ E \_ 備份 \_ 還原 \_ WINMGMT \_ 正在執行**
</dt> <dd> <dl> <dt>

2147749984 (0x80041060) 
</dt> <dt>



要求在 WinMgmt.exe 或包含 WMI 服務的 SVCHOST 進程使用時，備份或還原存放庫。


</dt> </dl> </dd> <dt>

<span id="WBEM_E_QUEUE_OVERFLOW"></span><span id="wbem_e_queue_overflow"></span>**WBEM \_ E \_ 佇列 \_ 溢位**
</dt> <dd> <dl> <dt>

2147749985 (0x80041061) 
</dt> <dt>



事件取用者的非同步傳遞佇列溢位太慢。


</dt> </dl> </dd> <dt>

<span id="WBEM_E_PRIVILEGE_NOT_HELD"></span><span id="wbem_e_privilege_not_held"></span>**\_ \_ \_ 未保留 WBEM E \_ 許可權**
</dt> <dd> <dl> <dt>

2147749986 (0x80041062) 
</dt> <dt>



因為用戶端沒有必要的安全性許可權，所以操作失敗。


</dt> </dl> </dd> <dt>

<span id="WBEM_E_INVALID_OPERATOR"></span><span id="wbem_e_invalid_operator"></span>**WBEM \_ E \_ 無效 \_ 運算子**
</dt> <dd> <dl> <dt>

2147749987 (0x80041063) 
</dt> <dt>



運算子對此屬性類型無效。


</dt> </dl> </dd> <dt>

<span id="WBEM_E_LOCAL_CREDENTIALS"></span><span id="wbem_e_local_credentials"></span>**WBEM \_ E \_ 本機 \_ 認證**
</dt> <dd> <dl> <dt>

2147749988 (0x80041064) 
</dt> <dt>



使用者在本機連接上指定了使用者名稱/密碼/授權單位。 使用者必須使用空白的使用者名稱/密碼，並且依賴預設安全性。


</dt> </dl> </dd> <dt>

<span id="WBEM_E_CANNOT_BE_ABSTRACT"></span><span id="wbem_e_cannot_be_abstract"></span>**WBEM \_ E \_ 不 \_ 可以是 \_ 抽象的**
</dt> <dd> <dl> <dt>

2147749989 (0x80041065) 
</dt> <dt>



類別在其父類別不是抽象時成為抽象。


</dt> </dl> </dd> <dt>

<span id="WBEM_E_AMENDED_OBJECT"></span><span id="wbem_e_amended_object"></span>**WBEM \_ E \_ 修改過的 \_ 物件**
</dt> <dd> <dl> <dt>

2147749990 (0x80041066) 
</dt> <dt>



未使用 WBEM 旗標來寫入修改過的物件， **\_ 請使用指定的 \_ \_ 修改 \_ 限定詞** 旗標。


</dt> </dl> </dd> <dt>

<span id="WBEM_E_CLIENT_TOO_SLOW"></span><span id="wbem_e_client_too_slow"></span>**WBEM \_ E \_ 用戶端 \_ 太 \_ 慢**
</dt> <dd> <dl> <dt>

2147749991 (0x80041067) 
</dt> <dt>



用戶端無法從列舉快速地取出物件。 當用戶端建立列舉物件時，會傳回此常數，但不會及時從列舉值抓取物件，進而導致列舉值的物件快取進行備份。


</dt> </dl> </dd> <dt>

<span id="WBEM_E_NULL_SECURITY_DESCRIPTOR"></span><span id="wbem_e_null_security_descriptor"></span>**WBEM \_ E \_ Null \_ 安全 \_ 描述項**
</dt> <dd> <dl> <dt>

2147749992 (0x80041068) 
</dt> <dt>



已使用 Null 安全描述項。


</dt> </dl> </dd> <dt>

<span id="WBEM_E_TIMED_OUT"></span><span id="wbem_e_timed_out"></span>**WBEM \_ E \_ 超時 \_**
</dt> <dd> <dl> <dt>

2147749993 (0x80041069) 
</dt> <dt>



作業超時。


</dt> </dl> </dd> <dt>

<span id="WBEM_E_INVALID_ASSOCIATION"></span><span id="wbem_e_invalid_association"></span>**WBEM \_ E \_ 不正確 \_ 關聯**
</dt> <dd> <dl> <dt>

2147749994
</dt> <dt>



關聯無效。


</dt> </dl> </dd> <dt>

<span id="WBEM_E_AMBIGUOUS_OPERATION"></span><span id="wbem_e_ambiguous_operation"></span>**WBEM \_ E 不 \_ 明確的 \_ 運算**
</dt> <dd> <dl> <dt>

2147749995 (0x8004106B) 
</dt> <dt>



運算不明確。


</dt> </dl> </dd> <dt>

<span id="WBEM_E_QUOTA_VIOLATION"></span><span id="wbem_e_quota_violation"></span>**WBEM \_ E \_ 配額 \_ 違規**
</dt> <dd> <dl> <dt>

2147749996 (0x8004106C) 
</dt> <dt>



WMI 佔用太多記憶體。 這可能是因為記憶體可用性不足或 WMI 耗用過多記憶體所致。


</dt> </dl> </dd> <dt>

<span id="WBEM_E_TRANSACTION_CONFLICT"></span><span id="wbem_e_transaction_conflict"></span>**WBEM \_ E \_ 交易 \_ 衝突**
</dt> <dd> <dl> <dt>

2147749997 (0x8004106D) 
</dt> <dt>



作業導致交易衝突。


</dt> </dl> </dd> <dt>

<span id="WBEM_E_FORCED_ROLLBACK"></span><span id="wbem_e_forced_rollback"></span>**WBEM \_ E \_ 強制 \_ 復原**
</dt> <dd> <dl> <dt>

2147749998 (0x8004106E) 
</dt> <dt>



交易強制執行回復。


</dt> </dl> </dd> <dt>

<span id="WBEM_E_UNSUPPORTED_LOCALE"></span><span id="wbem_e_unsupported_locale"></span>**WBEM \_ E \_ 不支援的 \_ 地區設定**
</dt> <dd> <dl> <dt>

2147749999 (0x8004106F) 
</dt> <dt>



不支援在呼叫中使用的地區設定。


</dt> </dl> </dd> <dt>

<span id="WBEM_E_HANDLE_OUT_OF_DATE"></span><span id="wbem_e_handle_out_of_date"></span>**WBEM \_ E \_ 句 \_ 柄 \_ 過期 \_**
</dt> <dd> <dl> <dt>

2147750000 (0x80041070) 
</dt> <dt>



物件控制碼已過期。


</dt> </dl> </dd> <dt>

<span id="WBEM_E_CONNECTION_FAILED"></span><span id="wbem_e_connection_failed"></span>**WBEM \_ E \_ 連接 \_ 失敗**
</dt> <dd> <dl> <dt>

2147750001 (0x80041071) 
</dt> <dt>



連接至 SQL 資料庫失敗。


</dt> </dl> </dd> <dt>

<span id="WBEM_E_INVALID_HANDLE_REQUEST"></span><span id="wbem_e_invalid_handle_request"></span>**WBEM \_ E \_ 不正確 \_ 控制碼 \_ 要求**
</dt> <dd> <dl> <dt>

2147750002 (0x80041072) 
</dt> <dt>



控制碼要求無效。


</dt> </dl> </dd> <dt>

<span id="WBEM_E_PROPERTY_NAME_TOO_WIDE"></span><span id="wbem_e_property_name_too_wide"></span>**WBEM \_ E \_ 屬性 \_ 名稱 \_ 太 \_ 寬**
</dt> <dd> <dl> <dt>

2147750003 (0x80041073) 
</dt> <dt>



屬性名稱包含超過255個字元。


</dt> </dl> </dd> <dt>

<span id="WBEM_E_CLASS_NAME_TOO_WIDE"></span><span id="wbem_e_class_name_too_wide"></span>**WBEM \_ E \_ 類別 \_ 名稱 \_ 太 \_ 寬**
</dt> <dd> <dl> <dt>

2147750004 (0x80041074) 
</dt> <dt>



類別名稱包含超過255個字元。


</dt> </dl> </dd> <dt>

<span id="WBEM_E_METHOD_NAME_TOO_WIDE"></span><span id="wbem_e_method_name_too_wide"></span>**WBEM \_ E \_ 方法 \_ 名稱 \_ 太 \_ 寬**
</dt> <dd> <dl> <dt>

2147750005 (0x80041075) 
</dt> <dt>



方法名稱包含超過255個字元。


</dt> </dl> </dd> <dt>

<span id="WBEM_E_QUALIFIER_NAME_TOO_WIDE"></span><span id="wbem_e_qualifier_name_too_wide"></span>**WBEM \_ E 辨識 \_ 符號 \_ 名稱 \_ 太 \_ 寬**
</dt> <dd> <dl> <dt>

2147750006 (0x80041076) 
</dt> <dt>



限定詞名稱包含超過255個字元。


</dt> </dl> </dd> <dt>

<span id="WBEM_E_RERUN_COMMAND"></span><span id="wbem_e_rerun_command"></span>**WBEM \_ E \_ 重新執行 \_ 命令**
</dt> <dd> <dl> <dt>

2147750007 (0x80041077) 
</dt> <dt>



因為 SQL 中有鎖死，所以必須重新執行 SQL 命令。 只有當資料儲存在 SQL 資料庫中時，才會傳回此項。


</dt> </dl> </dd> <dt>

<span id="WBEM_E_DATABASE_VER_MISMATCH"></span><span id="wbem_e_database_ver_mismatch"></span>**WBEM \_ E \_ 資料庫 \_ VER \_ 不符**
</dt> <dd> <dl> <dt>

2147750008 (0x80041078) 
</dt> <dt>



資料庫版本與存放庫驅動程式所處理的版本不相符。


</dt> </dl> </dd> <dt>

<span id="WBEM_E_VETO_DELETE"></span><span id="wbem_e_veto_delete"></span>**WBEM \_ E \_ 拒絕 \_ 刪除**
</dt> <dd> <dl> <dt>

2147750009 (0x80041079) 
</dt> <dt>



WMI 無法執行刪除作業，因為提供者不允許該操作。


</dt> </dl> </dd> <dt>

<span id="WBEM_E_VETO_PUT"></span><span id="wbem_e_veto_put"></span>**WBEM \_ E \_ 否決 \_ PUT**
</dt> <dd> <dl> <dt>

2147750010 (0x8004107A) 
</dt> <dt>



WMI 無法執行 put 作業，因為提供者不允許此操作。


</dt> </dl> </dd> <dt>

<span id="WBEM_E_INVALID_LOCALE"></span><span id="wbem_e_invalid_locale"></span>**WBEM \_ E \_ 不正確 \_ 地區設定**
</dt> <dd> <dl> <dt>

2147750016 (0x80041080) 
</dt> <dt>



指定的地區設定識別碼對作業無效。


</dt> </dl> </dd> <dt>

<span id="WBEM_E_PROVIDER_SUSPENDED"></span><span id="wbem_e_provider_suspended"></span>**已 \_ 暫停 WBEM E \_ 提供者 \_**
</dt> <dd> <dl> <dt>

2147750017 (0x80041081) 
</dt> <dt>



提供者已暫止。


</dt> </dl> </dd> <dt>

<span id="WBEM_E_SYNCHRONIZATION_REQUIRED"></span><span id="wbem_e_synchronization_required"></span>**\_需要 WBEM E \_ 同步 \_ 處理**
</dt> <dd> <dl> <dt>

2147750018 (0x80041082) 
</dt> <dt>



物件必須寫入至 WMI 儲存機制，並再次抓取，要求的作業才會成功。 當必須認可並抓取物件以查看屬性值時，就會傳回這個常數。


</dt> </dl> </dd> <dt>

<span id="WBEM_E_NO_SCHEMA"></span><span id="wbem_e_no_schema"></span>**WBEM \_ E \_ 沒有 \_ 架構**
</dt> <dd> <dl> <dt>

2147750019 (0x80041083) 
</dt> <dt>



無法完成操作;沒有任何可用的架構。


</dt> </dl> </dd> <dt>

<span id="WBEM_E_PROVIDER_ALREADY_REGISTERED"></span><span id="wbem_e_provider_already_registered"></span>**\_ \_ \_ 已註冊 WBEM E 提供者 \_**
</dt> <dd> <dl> <dt>

02147750020 (0x119FD010) 
</dt> <dt>



因為提供者已經註冊，所以無法註冊。


</dt> </dl> </dd> <dt>

<span id="WBEM_E_PROVIDER_NOT_REGISTERED"></span><span id="wbem_e_provider_not_registered"></span>**WBEM \_ E \_ 提供者 \_ 未 \_ 註冊**
</dt> <dd> <dl> <dt>

2147750021 (0x80041085) 
</dt> <dt>



未註冊提供者。


</dt> </dl> </dd> <dt>

<span id="WBEM_E_FATAL_TRANSPORT_ERROR"></span><span id="wbem_e_fatal_transport_error"></span>**WBEM \_ E \_ 嚴重 \_ 傳輸 \_ 錯誤**
</dt> <dd> <dl> <dt>

2147750022 (0x80041086) 
</dt> <dt>



發生嚴重的傳輸錯誤。


</dt> </dl> </dd> <dt>

<span id="WBEM_E_ENCRYPTED_CONNECTION_REQUIRED"></span><span id="wbem_e_encrypted_connection_required"></span>**\_需要 WBEM E \_ 加密 \_ 連接 \_**
</dt> <dd> <dl> <dt>

2147750023 (0x80041087) 
</dt> <dt>



使用者嘗試設定沒有加密連接的電腦名稱稱或網域。


</dt> </dl> </dd> <dt>

<span id="WBEM_E_PROVIDER_TIMED_OUT"></span><span id="wbem_e_provider_timed_out"></span>**WBEM \_ E \_ 提供者已 \_ 超時 \_**
</dt> <dd> <dl> <dt>

2147750024 (0x80041088) 
</dt> <dt>



提供者無法在指定的超時時間內報告結果。


</dt> </dl> </dd> <dt>

<span id="WBEM_E_NO_KEY"></span><span id="wbem_e_no_key"></span>**WBEM \_ E \_ 無 \_ 按鍵**
</dt> <dd> <dl> <dt>

2147750025 (0x80041089) 
</dt> <dt>



使用者嘗試放置未定義索引鍵的實例。


</dt> </dl> </dd> <dt>

<span id="WBEM_E_PROVIDER_DISABLED"></span><span id="wbem_e_provider_disabled"></span>**\_ \_ 已停用 WBEM E 提供者 \_**
</dt> <dd> <dl> <dt>

2147750026 (0x8004108A) 
</dt> <dt>



使用者嘗試註冊提供者實例，但已卸載提供者實例的 COM 伺服器。


</dt> </dl> </dd> <dt>

<span id="WBEMESS_E_REGISTRATION_TOO_BROAD"></span><span id="wbemess_e_registration_too_broad"></span>**WBEMESS \_ E \_ 註冊 \_ 太 \_ 廣泛**
</dt> <dd> <dl> <dt>

2147753985 (0x80042001) 
</dt> <dt>



提供者註冊與系統事件網域重迭。


</dt> </dl> </dd> <dt>

<span id="WBEMESS_E_REGISTRATION_TOO_PRECISE"></span><span id="wbemess_e_registration_too_precise"></span>**WBEMESS \_ E \_ 註冊 \_ 太 \_ 精確**
</dt> <dd> <dl> <dt>

2147753986 (0x80042002) 
</dt> <dt>



這個查詢中未使用 WITHIN 子句。


</dt> </dl> </dd> <dt>

<span id="WBEMESS_E_AUTHZ_NOT_PRIVILEGED"></span><span id="wbemess_e_authz_not_privileged"></span>**WBEMESS \_ E \_ 授權 \_ 不具特殊 \_ 許可權**
</dt> <dd> <dl> <dt>

2147753987 (0x80042003) 
</dt> <dt>



這部電腦沒有必要的網域許可權，無法支援與所建立訂用帳戶實例相關的安全性功能。 請聯絡網域系統管理員，將此電腦新增至 Windows 授權存取群組。


</dt> </dl> </dd> <dt>

<span id="WBEM_E_RETRY_LATER"></span><span id="wbem_e_retry_later"></span>**WBEM \_ E \_ 稍後重試 \_**
</dt> <dd> <dl> <dt>

2147758081 (0x80043001) 
</dt> <dt>



保留供未來使用。


</dt> </dl> </dd> <dt>

<span id="WBEM_E_RESOURCE_CONTENTION"></span><span id="wbem_e_resource_contention"></span>**WBEM \_ E \_ 資源 \_ 爭用**
</dt> <dd> <dl> <dt>

2147758082 (0x80043002) 
</dt> <dt>



保留供未來使用。


</dt> </dl> </dd> <dt>

<span id="WBEMMOF_E_EXPECTED_QUALIFIER_NAME"></span><span id="wbemmof_e_expected_qualifier_name"></span>**WBEMMOF \_ 電子 \_ 預期的辨識 \_ 符號 \_ 名稱**
</dt> <dd> <dl> <dt>

2147762177 (0x80044001) 
</dt> <dt>



必須是辨識符號名稱。


</dt> </dl> </dd> <dt>

<span id="WBEMMOF_E_EXPECTED_SEMI"></span><span id="wbemmof_e_expected_semi"></span>**WBEMMOF \_ E 必須 \_ 為 \_ 半**
</dt> <dd> <dl> <dt>

2147762178 (0x80044002) 
</dt> <dt>



必須是分號或 ' = '。


</dt> </dl> </dd> <dt>

<span id="WBEMMOF_E_EXPECTED_OPEN_BRACE"></span><span id="wbemmof_e_expected_open_brace"></span>**WBEMMOF \_ 電子 \_ 預期的 \_ 左 \_ 大括弧**
</dt> <dd> <dl> <dt>

2147762179 (0x80044003) 
</dt> <dt>



需要左大括弧。


</dt> </dl> </dd> <dt>

<span id="WBEMMOF_E_EXPECTED_CLOSE_BRACE"></span><span id="wbemmof_e_expected_close_brace"></span>**WBEMMOF \_ E \_ 應有 \_ 右 \_ 大括弧**
</dt> <dd> <dl> <dt>

2147762180 (0x80044004) 
</dt> <dt>



遺漏右大括弧或不合法的陣列元素。


</dt> </dl> </dd> <dt>

<span id="WBEMMOF_E_EXPECTED_CLOSE_BRACKET"></span><span id="wbemmof_e_expected_close_bracket"></span>**WBEMMOF \_ E \_ 應有 \_ 右 \_ 括弧**
</dt> <dd> <dl> <dt>

2147762181 (0x80044005) 
</dt> <dt>



必須是右括弧。


</dt> </dl> </dd> <dt>

<span id="WBEMMOF_E_EXPECTED_CLOSE_PAREN"></span><span id="wbemmof_e_expected_close_paren"></span>**WBEMMOF \_ E \_ 預期 \_ 右 \_ 括弧**
</dt> <dd> <dl> <dt>

2147762182 (0x80044006) 
</dt> <dt>



需要右括弧。


</dt> </dl> </dd> <dt>

<span id="WBEMMOF_E_ILLEGAL_CONSTANT_VALUE"></span><span id="wbemmof_e_illegal_constant_value"></span>**WBEMMOF \_ E 不 \_ 合法的 \_ 常 \_ 數值**
</dt> <dd> <dl> <dt>

2147762183 (0x80044007) 
</dt> <dt>



數值超出範圍或不含引號的字串。


</dt> </dl> </dd> <dt>

<span id="WBEMMOF_E_EXPECTED_TYPE_IDENTIFIER"></span><span id="wbemmof_e_expected_type_identifier"></span>**WBEMMOF \_ E \_ 預期的 \_ 類型 \_ 識別碼**
</dt> <dd> <dl> <dt>

2147762184 (0x80044008) 
</dt> <dt>



必須是類型識別碼。


</dt> </dl> </dd> <dt>

<span id="WBEMMOF_E_EXPECTED_OPEN_PAREN"></span><span id="wbemmof_e_expected_open_paren"></span>**WBEMMOF \_ 電子 \_ 預期的 \_ 左 \_ 括弧**
</dt> <dd> <dl> <dt>

2147762185 (0x80044009) 
</dt> <dt>



應為左括弧。


</dt> </dl> </dd> <dt>

<span id="WBEMMOF_E_UNRECOGNIZED_TOKEN"></span><span id="wbemmof_e_unrecognized_token"></span>**WBEMMOF \_ E \_ 無法辨識的 \_ 權杖**
</dt> <dd> <dl> <dt>

2147762186 (0x8004400A) 
</dt> <dt>



檔案中有未預期的標記。


</dt> </dl> </dd> <dt>

<span id="WBEMMOF_E_UNRECOGNIZED_TYPE"></span><span id="wbemmof_e_unrecognized_type"></span>**WBEMMOF \_ E \_ 無法辨識的 \_ 類型**
</dt> <dd> <dl> <dt>

2147762187 (0x8004400B) 
</dt> <dt>



無法辨識或不支援的類型識別碼。


</dt> </dl> </dd> <dt>

<span id="WBEMMOF_E_EXPECTED_PROPERTY_NAME"></span><span id="wbemmof_e_expected_property_name"></span>**WBEMMOF \_ E \_ 預期的 \_ 屬性 \_ 名稱**
</dt> <dd> <dl> <dt>

2147762187 (0x8004400B) 
</dt> <dt>



預期的屬性或方法名稱。


</dt> </dl> </dd> <dt>

<span id="WBEMMOF_E_TYPEDEF_NOT_SUPPORTED"></span><span id="wbemmof_e_typedef_not_supported"></span>**\_ \_ \_ 不支援 WBEMMOF E \_ TYPEDEF**
</dt> <dd> <dl> <dt>

2147762189 (0x8004400D) 
</dt> <dt>



不支援 typedef 和列舉類型。


</dt> </dl> </dd> <dt>

<span id="WBEMMOF_E_UNEXPECTED_ALIAS"></span><span id="wbemmof_e_unexpected_alias"></span>**WBEMMOF \_ E 未 \_ 預期的 \_ 別名**
</dt> <dd> <dl> <dt>

2147762190 (0x8004400E) 
</dt> <dt>



只有類別物件的參考可以有別名值。


</dt> </dl> </dd> <dt>

<span id="WBEMMOF_E_UNEXPECTED_ARRAY_INIT"></span><span id="wbemmof_e_unexpected_array_init"></span>**WBEMMOF \_ E 未 \_ 預期的 \_ 陣列 \_ 初始化**
</dt> <dd> <dl> <dt>

2147762191 (0x8004400F) 
</dt> <dt>



未預期的陣列初始化。 陣列必須使用宣告 \[ \] 。


</dt> </dl> </dd> <dt>

<span id="WBEMMOF_E_INVALID_AMENDMENT_SYNTAX"></span><span id="wbemmof_e_invalid_amendment_syntax"></span>**WBEMMOF \_ E \_ 不正確 \_ 修訂 \_ 語法**
</dt> <dd> <dl> <dt>

2147762192 (0x80044010) 
</dt> <dt>



命名空間路徑語法無效。


</dt> </dl> </dd> <dt>

<span id="WBEMMOF_E_INVALID_DUPLICATE_AMENDMENT"></span><span id="wbemmof_e_invalid_duplicate_amendment"></span>**WBEMMOF \_ 電子 \_ \_ 重複 \_ 修訂無效**
</dt> <dd> <dl> <dt>

2147762193 (0x80044011) 
</dt> <dt>



重複的修訂規範。


</dt> </dl> </dd> <dt>

<span id="WBEMMOF_E_INVALID_PRAGMA"></span><span id="wbemmof_e_invalid_pragma"></span>**WBEMMOF \_ E \_ 不正確 \_ PRAGMA**
</dt> <dd> <dl> <dt>

2147762194 (0x80044012) 
</dt> <dt>



[ \# pragma](pragma-namespace.md)之後必須接著有效的關鍵字。


</dt> </dl> </dd> <dt>

<span id="WBEMMOF_E_INVALID_NAMESPACE_SYNTAX"></span><span id="wbemmof_e_invalid_namespace_syntax"></span>**WBEMMOF \_ E \_ 不正確 \_ 命名空間 \_ 語法**
</dt> <dd> <dl> <dt>

2147762195 (0x80044013) 
</dt> <dt>



命名空間路徑語法無效。


</dt> </dl> </dd> <dt>

<span id="WBEMMOF_E_EXPECTED_CLASS_NAME"></span><span id="wbemmof_e_expected_class_name"></span>**WBEMMOF \_ E \_ 需要的 \_ 類別 \_ 名稱**
</dt> <dd> <dl> <dt>

2147762196 (0x80044014) 
</dt> <dt>



類別名稱中未預期的字元必須是識別碼。


</dt> </dl> </dd> <dt>

<span id="WBEMMOF_E_TYPE_MISMATCH"></span><span id="wbemmof_e_type_mismatch"></span>**WBEMMOF \_ E \_ 類型 \_ 不符**
</dt> <dd> <dl> <dt>

2147762197 (0x80044015) 
</dt> <dt>



指定的值不能成為適當的類型。


</dt> </dl> </dd> <dt>

<span id="WBEMMOF_E_EXPECTED_ALIAS_NAME"></span><span id="wbemmof_e_expected_alias_name"></span>**WBEMMOF \_ 電子 \_ 預期的 \_ 別名 \_ 名稱**
</dt> <dd> <dl> <dt>

2147762198 (0x80044016) 
</dt> <dt>



貨幣符號後面必須接著別名名稱作為識別碼。


</dt> </dl> </dd> <dt>

<span id="WBEMMOF_E_INVALID_CLASS_DECLARATION"></span><span id="wbemmof_e_invalid_class_declaration"></span>**WBEMMOF \_ E \_ 不正確 \_ 類別 \_ 宣告**
</dt> <dd> <dl> <dt>

2147762199 (0x80044017) 
</dt> <dt>



類別宣告無效。


</dt> </dl> </dd> <dt>

<span id="WBEMMOF_E_INVALID_INSTANCE_DECLARATION"></span><span id="wbemmof_e_invalid_instance_declaration"></span>**WBEMMOF \_ E \_ 不正確 \_ 實例 \_ 宣告**
</dt> <dd> <dl> <dt>

2147762200 (0x80044018) 
</dt> <dt>



實例宣告無效。 它必須以 "instance of" 開頭


</dt> </dl> </dd> <dt>

<span id="WBEMMOF_E_EXPECTED_DOLLAR"></span><span id="wbemmof_e_expected_dollar"></span>**WBEMMOF \_ 電子 \_ 預期的 \_ 貨幣**
</dt> <dd> <dl> <dt>

2147762201 (0x80044019) 
</dt> <dt>



預期的貨幣符號。 格式為 "$name" 的別名必須遵照 "as" 關鍵字。


</dt> </dl> </dd> <dt>

<span id="WBEMMOF_E_CIMTYPE_QUALIFIER"></span><span id="wbemmof_e_cimtype_qualifier"></span>**WBEMMOF \_ E \_ CIMTYPE 辨識 \_ 符號**
</dt> <dd> <dl> <dt>

2147762202 (0x8004401A) 
</dt> <dt>



無法直接在 MOF 檔案中指定 "CIMTYPE" 限定詞。 使用標準類型標記法。


</dt> </dl> </dd> <dt>

<span id="WBEMMOF_E_DUPLICATE_PROPERTY"></span><span id="wbemmof_e_duplicate_property"></span>**WBEMMOF \_ E \_ 重複 \_ 屬性**
</dt> <dd> <dl> <dt>

2147762203 (0x8004401B) 
</dt> <dt>



MOF 中找到重複的屬性名稱。


</dt> </dl> </dd> <dt>

<span id="WBEMMOF_E_INVALID_NAMESPACE_SPECIFICATION"></span><span id="wbemmof_e_invalid_namespace_specification"></span>**WBEMMOF \_ E \_ 不正確 \_ 命名空間 \_ 規格**
</dt> <dd> <dl> <dt>

2147762204 (0x8004401C) 
</dt> <dt>



命名空間語法無效。 不允許對其他伺服器的參考。


</dt> </dl> </dd> <dt>

<span id="WBEMMOF_E_OUT_OF_RANGE"></span><span id="wbemmof_e_out_of_range"></span>**WBEMMOF \_ E \_ 超出 \_ \_ 範圍**
</dt> <dd> <dl> <dt>

2147762205 (0x8004401D) 
</dt> <dt>



值超出範圍。


</dt> </dl> </dd> <dt>

<span id="WBEMMOF_E_INVALID_FILE"></span><span id="wbemmof_e_invalid_file"></span>**WBEMMOF \_ 電子 \_ 不正確檔案 \_**
</dt> <dd> <dl> <dt>

2147762206 (0x8004401E) 
</dt> <dt>



檔案不是有效的文字 MOF 檔案或二進位 MOF 檔案。


</dt> </dl> </dd> <dt>

<span id="WBEMMOF_E_ALIASES_IN_EMBEDDED"></span><span id="wbemmof_e_aliases_in_embedded"></span>**WBEMMOF \_ \_ \_ EMBEDDED 中的 E 別名 \_**
</dt> <dd> <dl> <dt>

2147762207 (0x8004401F) 
</dt> <dt>



内嵌物件不可以是別名。


</dt> </dl> </dd> <dt>

<span id="WBEMMOF_E_NULL_ARRAY_ELEM"></span><span id="wbemmof_e_null_array_elem"></span>**WBEMMOF \_ E \_ Null \_ 陣列 \_ ELEM**
</dt> <dd> <dl> <dt>

2147762208 (0x80044020) 
</dt> <dt>



陣列中的 Null 元素不受支援。


</dt> </dl> </dd> <dt>

<span id="WBEMMOF_E_DUPLICATE_QUALIFIER"></span><span id="wbemmof_e_duplicate_qualifier"></span>**WBEMMOF \_ E \_ 重複辨識 \_ 符號**
</dt> <dd> <dl> <dt>

2147762209 (0x80044021) 
</dt> <dt>



物件上的限定詞使用了一次以上。


</dt> </dl> </dd> <dt>

<span id="WBEMMOF_E_EXPECTED_FLAVOR_TYPE"></span><span id="wbemmof_e_expected_flavor_type"></span>**WBEMMOF \_ E \_ 預期 \_ 的 \_ 類型類型**
</dt> <dd> <dl> <dt>

2147762210 (0x80044022) 
</dt> <dt>



必須是類別類型，例如 **ToInstance**、 **ToSubClass**、 **EnableOverride** 或 **DisableOverride**。


</dt> </dl> </dd> <dt>

<span id="WBEMMOF_E_INCOMPATIBLE_FLAVOR_TYPES"></span><span id="wbemmof_e_incompatible_flavor_types"></span>**WBEMMOF \_ E \_ 不相容的 \_ \_ 種類類型**
</dt> <dd> <dl> <dt>

2147762211 (0x80044023) 
</dt> <dt>



在相同的辨識符號上結合 **EnableOverride** 和 **DisableOverride** 並不合法。


</dt> </dl> </dd> <dt>

<span id="WBEMMOF_E_MULTIPLE_ALIASES"></span><span id="wbemmof_e_multiple_aliases"></span>**WBEMMOF \_ E \_ 多個 \_ 別名**
</dt> <dd> <dl> <dt>

2147762212 (0x80044024) 
</dt> <dt>



別名不可使用兩次。


</dt> </dl> </dd> <dt>

<span id="WBEMMOF_E_INCOMPATIBLE_FLAVOR_TYPES2"></span><span id="wbemmof_e_incompatible_flavor_types2"></span>**WBEMMOF \_ E \_ 不相容的類別 \_ \_ TYPES2**
</dt> <dd> <dl> <dt>

2147762213 (0x80044025) 
</dt> <dt>



組合 **受限** 的、 **ToInstance** 或 **ToSubClass** 並不合法。


</dt> </dl> </dd> <dt>

<span id="WBEMMOF_E_NO_ARRAYS_RETURNED"></span><span id="wbemmof_e_no_arrays_returned"></span>**WBEMMOF \_ E \_ 未 \_ \_ 傳回陣列**
</dt> <dd> <dl> <dt>

2147762214 (0x80044026) 
</dt> <dt>



方法無法傳回陣列值。


</dt> </dl> </dd> <dt>

<span id="WBEMMOF_E_MUST_BE_IN_OR_OUT"></span><span id="wbemmof_e_must_be_in_or_out"></span>**WBEMMOF \_ E \_ 必須 \_ 是 \_ IN \_ 或 \_ OUT**
</dt> <dd> <dl> <dt>

2147762215 (0x80044027) 
</dt> <dt>



引數必須有 **In** 或 **Out** 限定詞。


</dt> </dl> </dd> <dt>

<span id="WBEMMOF_E_INVALID_FLAGS_SYNTAX"></span><span id="wbemmof_e_invalid_flags_syntax"></span>**WBEMMOF \_ E \_ 不正確 \_ 旗標 \_ 語法**
</dt> <dd> <dl> <dt>

2147762216 (0x80044028) 
</dt> <dt>



旗標語法無效。


</dt> </dl> </dd> <dt>

<span id="WBEMMOF_E_EXPECTED_BRACE_OR_BAD_TYPE"></span><span id="wbemmof_e_expected_brace_or_bad_type"></span>**WBEMMOF \_ E 必須是 \_ \_ 大括弧 \_ 或不 \_ 正確的 \_ 類型**
</dt> <dd> <dl> <dt>

2147762217 (0x80044029) 
</dt> <dt>



遺漏了類別的最後大括弧和分號。


</dt> </dl> </dd> <dt>

<span id="WBEMMOF_E_UNSUPPORTED_CIMV22_QUAL_VALUE"></span><span id="wbemmof_e_unsupported_cimv22_qual_value"></span>**WBEMMOF \_ E \_ 不支援的 \_ CIMV22 \_ QUAL \_ 值**
</dt> <dd> <dl> <dt>

2147762218 (0x8004402A) 
</dt> <dt>



限定詞值不支援 CIM 2.2 版的功能。


</dt> </dl> </dd> <dt>

<span id="WBEMMOF_E_UNSUPPORTED_CIMV22_DATA_TYPE"></span><span id="wbemmof_e_unsupported_cimv22_data_type"></span>**WBEMMOF \_ E \_ 不支援的 \_ CIMV22 \_ 資料 \_ 類型**
</dt> <dd> <dl> <dt>

2147762219 (0x8004402B) 
</dt> <dt>



不支援 CIM 版本2.2 資料類型。


</dt> </dl> </dd> <dt>

<span id="WBEMMOF_E_INVALID_DELETEINSTANCE_SYNTAX"></span><span id="wbemmof_e_invalid_deleteinstance_syntax"></span>**WBEMMOF \_ E \_ 不正確 \_ DELETEINSTANCE \_ 語法**
</dt> <dd> <dl> <dt>

2147762220 (0x8004402C) 
</dt> <dt>



刪除實例語法無效。 它應該是 `#pragma DeleteInstance("instancepath", FAIL|NOFAIL)`


</dt> </dl> </dd> <dt>

<span id="WBEMMOF_E_INVALID_QUALIFIER_SYNTAX"></span><span id="wbemmof_e_invalid_qualifier_syntax"></span>**WBEMMOF \_ E \_ 不正確辨識 \_ 符號 \_ 語法**
</dt> <dd> <dl> <dt>

2147762221 (0x8004402D) 
</dt> <dt>



限定詞語法無效。 此屬性應該是 `qualifiername:type=value,scope(class|instance), flavorname`。


</dt> </dl> </dd> <dt>

<span id="WBEMMOF_E_QUALIFIER_USED_OUTSIDE_SCOPE"></span><span id="wbemmof_e_qualifier_used_outside_scope"></span>**\_ \_ \_ \_ 範圍外使用的 WBEMMOF E 限定詞 \_**
</dt> <dd> <dl> <dt>

2147762222 (0x8004402E) 
</dt> <dt>



限定詞會在其範圍之外使用。


</dt> </dl> </dd> <dt>

<span id="WBEMMOF_E_ERROR_CREATING_TEMP_FILE"></span><span id="wbemmof_e_error_creating_temp_file"></span>**\_ \_ \_ 建立 \_ 臨時 \_ 檔時發生 WBEMMOF E 錯誤**
</dt> <dd> <dl> <dt>

2147762223 (0x8004402F) 
</dt> <dt>



建立暫存檔案時發生錯誤。 暫存檔案是 MOF 編譯中的中繼階段。


</dt> </dl> </dd> <dt>

<span id="WBEMMOF_E_ERROR_INVALID_INCLUDE_FILE"></span><span id="wbemmof_e_error_invalid_include_file"></span>**WBEMMOF \_ E \_ ERROR \_ 不正確 \_ INCLUDE \_ 檔案**
</dt> <dd> <dl> <dt>

2147762224 (0x80044030) 
</dt> <dt>



預處理器命令[ \# 包含](-include.md)MOF 中包含的檔案無效。


</dt> </dl> </dd> <dt>

<span id="WBEMMOF_E_INVALID_DELETECLASS_SYNTAX"></span><span id="wbemmof_e_invalid_deleteclass_syntax"></span>**WBEMMOF \_ E \_ 不正確 \_ DELETECLASS \_ 語法**
</dt> <dd> <dl> <dt>

2147762225 (0x80044031) 
</dt> <dt>



預處理器命令[ \# pragma deleteinstance](pragma-deleteinstance.md)或[ \# pragma deleteclass](pragma-deleteclass.md)的語法無效。


</dt> </dl> </dd> </dl>

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|----------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows Vista<br/>                                                               |
| 最低支援的伺服器<br/> | Windows Server 2008<br/>                                                         |
| 標頭<br/>                   | <dl> <dt>WbemCli。h</dt> </dl>   |
| Idl<br/>                      | <dl> <dt>WbemCli .idl</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[WMI 傳回碼](wmi-return-codes.md)
</dt> </dl>

 

