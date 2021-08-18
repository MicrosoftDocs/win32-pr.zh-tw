---
description: 從認證控制碼起始用戶端輸出安全性內容。
ms.assetid: f3d8c07b-db28-4f26-ba29-8733fc95bdb5
title: InitializeSecurityContext (CredSSP) 函式 (Sspi.h)
ms.topic: reference
ms.date: 07/25/2019
ms.openlocfilehash: 5ba38dd10552f90ecfcc5045b96edc5e62aff1f8a2beec0f2a728fc1f0be8c52
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120015988"
---
# <a name="initializesecuritycontext-credssp-function"></a>InitializeSecurityCoNtext (CredSSP) 函數

**InitializeSecurityCoNtext (CredSSP)** 函數會從認證控制碼起始用戶端的輸出安全性內容。 此函數會在用戶端應用程式和遠端對等之間建立安全性內容。 **InitializeSecurityCoNtext (CredSSP)** 會傳回用戶端必須傳遞給遠端對等的權杖;對等接著會透過 [**AcceptSecurityCoNtext (CredSSP)**](acceptsecuritycontext--credssp.md) 呼叫，將該權杖提交至本機安全性執行。 所有呼叫端都應該將產生的 token 視為不透明。

通常會在迴圈中呼叫 **InitializeSecurityCoNtext (CredSSP)** 函數，直到建立足夠的安全性內容為止。

## <a name="syntax"></a>語法


```C++
SECURITY_STATUS SEC_ENTRY InitializeSecurityContext(
  _In_opt_    PCredHandle    phCredential,
  _In_opt_    PCtxtHandle    phContext,
  _In_opt_    SEC_CHAR       *pszTargetName,
  _In_        unsigned long  fContextReq,
  _Reserved_  unsigned long  Reserved1,
  _In_        unsigned long  TargetDataRep,
  _Inout_opt_ PSecBufferDesc pInput,
  _In_        unsigned long  Reserved2,
  _Inout_opt_ PCtxtHandle    phNewContext,
  _Out_opt_   PSecBufferDesc pOutput,
  _Out_       unsigned long  *pfContextAttr,
  _Out_opt_   PTimeStamp     ptsExpiry
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*phCredential* \[在中，選擇性\]
</dt> <dd>

[**AcquireCredentialsHandle (CredSSP)**](acquirecredentialshandle--credssp.md)所傳回之認證的控制碼。 這個控制碼是用來建立安全性內容。 **InitializeSecurityCoNtext (CredSSP)** 函數至少需要輸出認證。

</dd> <dt>

*phCoNtext* \[在中，選擇性\]
</dt> <dd>

[CtxtHandle](sspi-handles.md)結構的指標。 在第一次呼叫 **InitializeSecurityCoNtext (CredSSP)** 時，此指標為 **Null**。 第二次呼叫時，這個參數是第一個呼叫在 *phNewCoNtext* 參數中傳回之部分格式內容的控制碼指標。

在第一次呼叫 **InitializeSecurityCoNtext (CredSSP)** 時，請指定 **Null**。 在未來的呼叫中，請在第一次呼叫此函式之後，指定在 *phNewCoNtext* 參數中收到的權杖。

</dd> <dt>

*pTargetName* \[在中，選擇性\]
</dt> <dd>

以 null 結束的字串指標，可唯一識別目標伺服器。 Schannel 會使用這個值來驗證伺服器憑證。 當重新建立連接時，Schannel 也會使用此值來找出會話快取中的會話。 只有在符合下列所有條件時，才會使用快取會話：

-   目標名稱相同。
-   快取專案尚未過期。
-   呼叫函數的應用程式進程相同。
-   登入會話相同。
-   認證控制碼相同。

</dd> <dt>

*fCoNtextReq* \[在\]
</dt> <dd>

表示內容要求的位旗標。 並非所有封裝都能支援所有的需求。 用於此參數的旗標前面會加 \_ 上 isc 需求 \_ ，例如，isc 要求 \_ \_ 委派。

這個參數可以是下列其中一個或多個屬性旗標。



| 值                                                                                                                                                                                                                                                                            | 意義                                                                                                                                                                                                                                                            |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="ISC_REQ_ALLOCATE_MEMORY"></span><span id="isc_req_allocate_memory"></span><dl> <dt>**ISC \_需求 \_ 配置 \_ 記憶體**</dt> <dt>0x100</dt> </dl>                         | 安全性封裝會配置呼叫端的輸出緩衝區。 當您完成使用輸出緩衝區時，請呼叫 [**FreeCoNtextBuffer**](/windows/win32/api/sspi/nf-sspi-freecontextbuffer) 函式釋放它們。<br/>                                                        |
| <span id="ISC_REQ_CONNECTION"></span><span id="isc_req_connection"></span><dl> <dt>**ISC \_需求 \_ 連接**</dt> <dt>0x800</dt> </dl>                                         | 安全性內容將不會處理格式化訊息。<br/>                                                                                                                                                                                               |
| <span id="ISC_REQ_EXTENDED_ERROR"></span><span id="isc_req_extended_error"></span><dl> <dt>**ISC \_需求 \_ 擴充 \_ 錯誤**</dt> <dt>0x4000</dt> </dl>                           | 發生錯誤時，將會通知遠端方。<br/>                                                                                                                                                                                                   |
| <span id="ISC_REQ_MANUAL_CRED_VALIDATION"></span><span id="isc_req_manual_cred_validation"></span><dl> <dt>**ISC \_要求 \_ 手動 \_ \_ 認證驗證**</dt> <dt>0x80000</dt> </dl> |  (CredSSP) 的認證安全性支援提供者不能自動驗證服務器。 使用 CredSSP 時，一律會設定這個旗標。<br/>                                                                                                              |
| <span id="ISC_REQ_SEQUENCE_DETECT"></span><span id="isc_req_sequence_detect"></span><dl> <dt>**ISC \_要求 \_ 順序 \_**</dt>偵測 <dt>0x8</dt> </dl>                           | 偵測順序中所接收的訊息。<br/>                                                                                                                                                                                                               |
| <span id="ISC_REQ_STREAM"></span><span id="isc_req_stream"></span><dl> <dt>**ISC \_需求 \_ 資料流程**</dt> <dt>0x8000</dt> </dl>                                                    | 支援資料流程導向連接。<br/>                                                                                                                                                                                                                   |
| <span id="ISC_REQ_USE_SUPPLIED_CREDS"></span><span id="isc_req_use_supplied_creds"></span><dl> <dt>**ISC \_需求 \_ 使用 \_ 提供 \_**</dt>的認證 <dt>0x80</dt> </dl>                | CredSSP 不得嘗試自動提供用戶端的認證。<br/>                                                                                                                                                                            |
| <span id="ISC_REQ_DELEGATE"></span><span id="isc_req_delegate"></span><dl> <dt>**ISC \_要求 \_ 委派**</dt> <dt>0x1</dt> </dl>                                                 | 表示要將使用者的認證委派給伺服器。<br/> 如果未指定此旗標，則會將一組空的認證委派給伺服器。<br/> **Windows Server 2008 和 Windows Vista：** 此為必要旗標。<br/> |
| <span id="ISC_REQ_MUTUAL_AUTH"></span><span id="isc_req_mutual_auth"></span><dl> <dt>**ISC \_要求 \_ 相互 \_ 驗證**</dt> <dt>0x2</dt> </dl>                                       | 表示不需要伺服器驗證。 如果未指定此旗標，仍會強制執行委派原則。<br/> **Windows Server 2008 和 Windows Vista：** 此旗標會被忽略。<br/>                                                 |



 

用戶端可能不支援要求的屬性。 如需詳細資訊，請參閱 *pfCoNtextAttr* 參數。

如需各種屬性的進一步說明，請參閱 [內容需求](context-requirements.md)。

</dd> <dt>

*Reserved1* \[在\]
</dt> <dd>

保留的。 此參數必須設定為零。

</dd> <dt>

*TargetDataRep* \[在\]
</dt> <dd>

目標上的資料標記法，例如位元組順序。 此參數可以是 **安全性 \_ 原生 \_ DREP** 或 **安全性 \_ 網路 \_ DREP**。

</dd> <dt>

*pInput* \[in、out、optional\]
</dt> <dd>

[**SecBufferDesc**](/windows/win32/api/sspi/ns-sspi-secbufferdesc)結構的指標，其中包含提供給封裝輸入的緩衝區指標。 除非用戶端內容是由伺服器起始，否則這個參數的值在第一次呼叫函式時必須是 **Null** 。 在後續呼叫函式或由伺服器起始用戶端內容時，此參數的值會是配置有足夠記憶體的緩衝區指標，以保存遠端電腦所傳回的權杖。

在初始呼叫之後呼叫此函數時，必須有兩個緩衝區。 第一個類型的類型為之 secbuffer，並且包含從伺服器接收的權杖。 **\_** 第二個緩衝區的類型為 **之 secbuffer \_ EMPTY**，將 **pvBuffer** 和 **cbBuffer** 成員設定為零。

</dd> <dt>

*Reserved2* \[在\]
</dt> <dd>

保留的。 此參數必須設定為零。

</dd> <dt>

*phNewCoNtext* \[in、out、optional\]
</dt> <dd>

[CtxtHandle](sspi-handles.md)結構的指標。 在第一次呼叫 **InitializeSecurityCoNtext (CredSSP)** 時，此指標會收到新的內容控制碼。 第二次呼叫時， *phNewCoNtext* 可以與 *phCoNtext* 參數中指定的控制碼相同。

在第一次呼叫後的呼叫中，將此處傳回的控制碼傳遞為 *phCoNtext* 參數，並為 *phNewCoNtext* 指定 **Null** 。

</dd> <dt>

*pOutput* \[out、optional\]
</dt> <dd>

[**SecBufferDesc**](/windows/win32/api/sspi/ns-sspi-secbufferdesc)結構的指標。 此結構接著會包含接收輸出資料之 [**之 secbuffer**](/windows/win32/api/sspi/ns-sspi-secbuffer) 結構的指標。 如果輸入中的緩衝區輸入為 **SEC \_ READWRITE** ，則輸出中會有該緩衝區。 如果要求 (透過 **ISC \_ 需求 \_ 配置 \_ 記憶體**) ，並在安全性權杖的緩衝區描述項中填入位址，系統將會配置安全性權杖的緩衝區。

如果指定了 **ISC \_ 需求 \_ 配置 \_ 記憶體** 旗標，CredSSP 將會為緩衝區配置記憶體，並將適當的資訊放在 [**SecBufferDesc**](/windows/win32/api/sspi/ns-sspi-secbufferdesc)中。

</dd> <dt>

*pfCoNtextAttr* \[擴展\]
</dt> <dd>

一組位旗標的指標，指出已建立內容的 [*屬性*](../secgloss/a-gly.md#_security_attribute_gly) 。 如需各種屬性的說明，請參閱 [內容需求](context-requirements.md)。

用於此參數的旗標前面會加 \_ 上 isc ret，例如 **isc \_ ret \_ 委派**。 如需有效值的清單，請參閱 *fCoNtextReq* 參數。

在最後一個函式呼叫成功傳回之前，請勿檢查安全性相關屬性。 與安全性無關的屬性旗標（例如 **ASC RET 配置的 \_ \_ \_ 記憶體** 旗標）可以在最後一次傳回前進行檢查。

> [!Note]  
> 特定內容屬性在與遠端對等的協商期間可能會變更。

 

</dd> <dt>

*ptsExpiry* \[out、optional\]
</dt> <dd>

[**時間戳記**](timestamp.md)結構的指標，此結構會接收內容的到期時間。 建議安全套件在本地時間一律會傳回此值。 這個參數是選擇性的，且應該傳遞給短期用戶端的 **Null** 。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果函式成功，它會傳回下列其中一個成功碼。



| 傳回碼                                                                                                    | 描述                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
|----------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**SEC \_ E \_ 未完成 \_ 訊息**</dt> </dl>     | 無法從網路讀取整個訊息的資料。<br/> 當傳回這個值時， *pInput* 緩衝區就會包含 [**之 secbuffer**](/windows/win32/api/sspi/ns-sspi-secbuffer) 結構，其中 **遺漏 BufferType** 成員 **之 secbuffer \_**。 **之 secbuffer** 的 **cbBuffer** 成員會指定函式在此函數成功之前，必須從用戶端讀取的額外位元組數目。 雖然此數目不一定是精確的，但使用它有助於藉由避免多次呼叫此函式來改善效能。<br/> |
| <dl> <dt>**秒 \_ E \_ 確定**</dt> </dl>                      | 已成功初始化安全性內容。 不需要另一個 [**InitializeSecurityCoNtext (CredSSP)**](initializesecuritycontext--credssp.md) 呼叫。 如果函式傳回輸出 token，也就是，如果 *pOutput* 中的 **之 secbuffer \_ token** 為非零長度，則該 token 必須傳送至伺服器。<br/>                                                                                                   |
| <dl> <dt>**秒 \_ \_ 完成 \_ 並 \_ 繼續**</dt> </dl> | 用戶端必須呼叫 [**CompleteAuthToken**](/windows/win32/api/sspi/nf-sspi-completeauthtoken) ，然後將輸出傳遞至伺服器。 然後，用戶端會等候傳回的權杖，並在另一個呼叫中傳遞它，以 [**InitializeSecurityCoNtext (CredSSP)**](initializesecuritycontext--credssp.md)。<br/>                                                                                                                                                                                                                                            |
| <dl> <dt>**\_ \_ 需要完成的秒數 \_**</dt> </dl>        | 用戶端必須完成建立訊息，然後呼叫 [**CompleteAuthToken**](/windows/win32/api/sspi/nf-sspi-completeauthtoken) 函數。<br/>                                                                                                                                                                                                                                                                                                                                                                                                   |
| <dl> <dt>**每 \_ 秒 \_ 繼續 \_ 需要**</dt> </dl>        | 用戶端必須將輸出 token 傳送至伺服器，並等候傳回權杖。 用戶端會在對 [**InitializeSecurityCoNtext (CredSSP)**](initializesecuritycontext--credssp.md)的另一個呼叫中傳遞傳回的權杖。 輸出 token 可以是空的。<br/>                                                                                                                                                                                                                                                              |
| <dl> <dt>**秒 \_ 我 \_ 的 \_ 認證不完整**</dt> </dl> | 伺服器已要求用戶端驗證，但提供的認證未包含憑證，或憑證不是由伺服器所信任的憑證授權單位單位所發行。 如需詳細資訊，請參閱＜備註＞。<br/>                                                                                                                                                                              |



 

如果函式失敗，函數會傳回下列其中一個錯誤碼。



| 傳回碼                                                                                                          | 描述                                                                                                                                                                                                                                                                           |
|----------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**每 \_ 秒 \_ 沒有足夠的 \_ 記憶體**</dt> </dl>          | 沒有足夠的記憶體可完成要求的動作。<br/>                                                                                                                                                                                                     |
| <dl> <dt>**SEC \_ E \_ 內部 \_ 錯誤**</dt> </dl>               | 發生未對應到 SSPI 錯誤碼的錯誤。<br/>                                                                                                                                                                                                                  |
| <dl> <dt>**SEC \_ E \_ 不正確 \_ 控制碼**</dt> </dl>               | 傳遞給函數的控制碼無效。<br/>                                                                                                                                                                                                                            |
| <dl> <dt>**SEC \_ E \_ 不正確 \_ 權杖**</dt> </dl>                | 輸入 token 的格式不正確。 可能的原因包括傳輸中的權杖損毀、不正確大小的權杖，以及傳遞到錯誤安全性套件的權杖。 如果用戶端和伺服器未協調適當的安全性套件，則會發生最後一個狀況。<br/> |
| <dl> <dt>**秒 \_ E \_ 登入 \_ 拒絕**</dt> </dl>                 | 登入失敗。<br/>                                                                                                                                                                                                                                                          |
| <dl> <dt>**SEC \_ E \_ 無 \_ 驗證 \_ 授權單位**</dt> </dl> | 無法連絡任何授權單位進行驗證。 驗證方的功能變數名稱可能錯誤、無法連線到網域，或可能有信任關係失敗。<br/>                                                                    |
| <dl> <dt>**SEC \_ E \_ 無 \_ 認證**</dt> </dl>               | 安全性套件中沒有任何可用的認證。<br/>                                                                                                                                    |
| <dl> <dt>**SEC \_ E \_ 目標 \_ 不明**</dt> </dl>               | 無法辨識目標。<br/>                                                                                                                                                                                                                                             |
| <dl> <dt>**SEC \_ E \_ 不支援的函式 \_**</dt> </dl>         | *FCoNtextReq* 參數的值無效。 未指定必要的旗標，或指定了 CredSSP 不支援的旗標。<br/>                                                                                                                 |
| <dl> <dt>**SEC \_ E \_ 錯誤的 \_ 主體**</dt> </dl>              | 收到驗證要求的主體與傳入 *pszTargetName* 參數的主體不同。 此錯誤表示相互驗證失敗。<br/>                                                                                      |
| <dl> <dt>**SEC \_ E \_ 委派 \_ 原則**</dt> </dl>            | 原則不支援將認證委派給目標伺服器。<br/>                                                                                                                                                                                                |
| <dl> <dt>**\_僅限 SEC E \_ 原則 \_ NLTM \_**</dt> </dl>            | 當無法進行相互驗證時，不允許將認證委派給目標伺服器。<br/>                                                                                                                                                                  |
| <dl> <dt>**SEC \_ E \_ 相互 \_ 驗證 \_ 失敗**</dt> </dl>          | 在 \_ \_ \_ *fCoNtextReq* 參數中指定了 ISC 要求相互驗證旗標時，伺服器驗證失敗。<br/>                                                                                                                                                             |



 

## <a name="remarks"></a>備註

呼叫端負責判斷最終的內容屬性是否足夠。 例如，如果要求了機密性，但無法建立，有些應用程式可能會選擇立即關閉連接。

如果安全性內容的屬性不足夠，用戶端必須藉由呼叫 [**DeleteSecurityCoNtext**](/windows/win32/api/sspi/nf-sspi-deletesecuritycontext) 函式來釋放部分建立的內容。

用戶端會呼叫 **InitializeSecurityCoNtext (CredSSP)** 函數來初始化輸出內容。

針對兩階段安全性內容，呼叫順序如下所示：

1.  用戶端會呼叫 *phCoNtext* 設為 **Null** 的函式，並使用輸入訊息填入緩衝區描述項。
2.  安全性套件會檢查參數並建立不透明的權杖，並將它放在緩衝區陣列的 TOKEN 專案中。 如果 *fCoNtextReq* 參數包含「 **ISC \_ 需求 \_ 配置 \_ 記憶體** 」旗標，則安全性封裝會配置記憶體，並傳回 TOKEN 元素中的指標。
3.  用戶端會將 *pOutput* 緩衝區中傳回的權杖傳送至目標伺服器。 然後，伺服器會在對 [**AcceptSecurityCoNtext (CredSSP)**](acceptsecuritycontext--credssp.md) 函式的呼叫中，將權杖傳遞為輸入引數。
4.  [**AcceptSecurityCoNtext (CredSSP)**](acceptsecuritycontext--credssp.md) 可能會傳回權杖。 伺服器會透過第二個 InitializeSecurityCoNtext 將此權杖傳送給用戶端 **(CredSSP)** 呼叫是否會在第一次呼叫傳回時 **\_ \_ 繼續 \_ 需要**。

如果伺服器已順利回應，則安全性封裝會傳回 **SEC \_ E \_ OK** ，並且會建立安全會話。

如果函數傳回其中一個錯誤回應，則不接受伺服器的回應，也不會建立會話。

如果函式傳回的秒數是 **\_ 我 \_ 繼續 \_ 需要** 的，則 **\_ \_ \_ 需要秒** 完成，或 **每秒 \_ \_ 完成 \_ 並 \_ 繼續** 進行，步驟2和3會重複執行。

根據基礎驗證機制以及在 *fCoNtextReq* 參數中指定的選項，安全性內容初始化可能需要對這個函式進行一個以上的呼叫。

*FCoNtextReq* 和 *pfCoNtextAttributes* 參數是代表各種內容屬性的位元遮罩。 如需各種屬性的說明，請參閱 [內容需求](context-requirements.md)。 雖然 *pfCoNtextAttributes* 參數在任何成功傳回時都有效，但您應該只在最終成功傳回時，檢查與內容安全性層面相關的旗標。 例如，中繼傳回可以設定 **ISC RET 配置的 \_ \_ \_ 記憶體** 旗標。

如果已設定 **ISC \_ 需求 \_ 使用 \_ 提供 \_** 的認證旗標，則安全性封裝必須在 *pInput* 輸入緩衝區中尋找 **之 secbuffer \_ PKG \_ PARAMS** 緩衝區類型。 雖然這不是一般解決方案，但在適當的情況下允許安全套件和應用程式的強式配對。

如果指定了 **ISC 要求 \_ \_ 配置 \_ 記憶體** ，呼叫端必須藉由呼叫 [**FreeCoNtextBuffer**](/windows/win32/api/sspi/nf-sspi-freecontextbuffer) 函式來釋放記憶體。

例如，輸入權杖可能是 LAN Manager 的挑戰。 在此情況下，輸出權杖會是對挑戰的 NTLM 加密回應。

用戶端所採取的動作取決於此函式的傳回碼。 如果傳回碼為 **SEC \_ E \_ OK**，將不會有第二個 **InitializeSecurityCoNtext (CredSSP)** 呼叫，且不會預期伺服器的回應。 如果傳回碼是 **每秒 \_ \_ 繼續 \_ 需要** 的，則用戶端會預期權杖以回應伺服器，並在第二次呼叫中傳遞給 **InitializeSecurityCoNtext (CredSSP)**。 當 **\_ 我 \_ 完成 \_ 所需** 的傳回碼時，會指出用戶端必須完成建立訊息並呼叫 [**CompleteAuthToken**](/windows/win32/api/sspi/nf-sspi-completeauthtoken) 函數。 當 **\_ 我 \_ 完成 \_ 並 \_ 繼續** 程式碼時，會合並這兩個動作。

如果 **InitializeSecurityCoNtext (CredSSP)** 在第一個 (或只有) 呼叫傳回 success，呼叫端最後必須在傳回的控制碼上呼叫 [**DeleteSecurityCoNtext**](/windows/win32/api/sspi/nf-sspi-deletesecuritycontext) 函式，即使在驗證交換的後續階段中呼叫失敗也是一樣。

用戶端可能會在成功完成之後，再次呼叫 **InitializeSecurityCoNtext (CredSSP)** 。 這會向安全性封裝指出需要重新驗證。

核心模式呼叫端有下列差異：目標名稱是必須使用 [**VirtualAlloc**](/windows/win32/api/memoryapi/nf-memoryapi-virtualalloc)在虛擬記憶體中配置的 [*Unicode*](../secgloss/u-gly.md#_security_unicode_gly)字串;它不得從集區配置。 *PInput* 和 *pOutput* 中傳遞和提供的緩衝區必須在虛擬記憶體中，而不是在集區中。

如果函式傳回的 **秒數 \_ \_ 不完整的 \_ 認證**，請檢查傳遞給 [**AcquireCredentialsHandle (CredSSP)**](acquirecredentialshandle--credssp.md) 函數是否已指定有效且受信任的憑證，憑證必須是伺服器所信任之憑證授權單位單位所發行的用戶端驗證憑證。 若要取得伺服器所信任的 Ca 清單，請使用 **SECPKG \_ ATTR \_ 簽發者 \_ 清單 \_ EX** 屬性來呼叫 [**QueryCoNtextAttributes (CredSSP)**](querycontextattributes--credssp.md)函數。

從伺服器所信任的憑證授權單位單位收到驗證憑證之後，用戶端應用程式會建立新的認證。 其運作方式是呼叫 [**AcquireCredentialsHandle (credssp)**](acquirecredentialshandle--credssp.md) 函式，然後再次呼叫 **InitializeSecurityCoNtext (CredSSP)** ，在 *phCredential* 參數中指定新的認證。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|--------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows\[僅限 Vista desktop 應用程式\]<br/>                                                         |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2008 desktop 應用程式\]<br/>                                                   |
| 標頭<br/>                   | <dl> <dt>Sspi (包含 Security .h) </dt> </dl> |
| 程式庫<br/>                  | <dl> <dt>Secur32 .lib</dt> </dl>                 |
| DLL<br/>                      | <dl> <dt>Secur32.dll</dt> </dl>                 |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[SSPI 函數](authentication-functions.md#sspi-functions)
</dt> <dt>

[**AcceptSecurityCoNtext (CredSSP)**](acceptsecuritycontext--credssp.md)
</dt> <dt>

[**AcquireCredentialsHandle (CredSSP)**](acquirecredentialshandle--credssp.md)
</dt> <dt>

[**CompleteAuthToken**](/windows/win32/api/sspi/nf-sspi-completeauthtoken)
</dt> <dt>

[**DeleteSecurityCoNtext**](/windows/win32/api/sspi/nf-sspi-deletesecuritycontext)
</dt> <dt>

[**FreeCoNtextBuffer**](/windows/win32/api/sspi/nf-sspi-freecontextbuffer)
</dt> <dt>

[**之 secbuffer**](/windows/win32/api/sspi/ns-sspi-secbuffer)
</dt> <dt>

[**SecBufferDesc**](/windows/win32/api/sspi/ns-sspi-secbufferdesc)
</dt> </dl>

 

 
