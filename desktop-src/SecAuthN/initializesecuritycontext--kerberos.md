---
description: 使用 Kerberos [*限制委派*](../secgloss/s-gly.md)，從認證控制碼起始用戶端輸出 [*安全性內容*](../secgloss/s-gly.md)。
ms.assetid: b5c968dc-9343-44ed-acbc-a89c58c14e4a
title: 'InitializeSecurityCoNtext (Kerberos) 函數 (Sspi. h) '
ms.topic: reference
ms.date: 07/25/2019
ms.openlocfilehash: 8c558174c168b17b67c9c08b1aee92e6dc10161f
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2021
ms.locfileid: "122470533"
---
# <a name="initializesecuritycontext-kerberos-function"></a>InitializeSecurityCoNtext (Kerberos) 函數

**InitializeSecurityCoNtext (Kerberos)** 函數會從認證控制碼起始用戶端的輸出 [*安全性內容*](../secgloss/s-gly.md)。 函數是用來建立用戶端應用程式和遠端對等之間的 [*安全性內容*](../secgloss/s-gly.md) 。 **InitializeSecurityCoNtext (Kerberos)** 會傳回用戶端必須傳遞給遠端對等的權杖，對等互連接著會透過 [**AcceptSecurityCoNtext (Kerberos)**](acceptsecuritycontext--kerberos.md) 呼叫，提交給本機安全性執行。 所有呼叫端都應該將產生的 token 視為不透明。

一般而言， **InitializeSecurityCoNtext (Kerberos)** 函數會在迴圈中呼叫，直到建立足夠的 [*安全性內容*](../secgloss/s-gly.md) 為止。

## <a name="syntax"></a>語法


```C++
SECURITY_STATUS SEC_Entry InitializeSecurityContext(
  _In_opt_    PCredHandle    phCredential,
  _In_opt_    PCtxtHandle    phContext,
  _In_        SEC_CHAR       *pszTargetName,
  _In_        ULONG          fContextReq,
  _In_        ULONG          Reserved1,
  _In_        ULONG          TargetDataRep,
  _In_opt_    PSecBufferDesc pInput,
  _In_        ULONG          Reserved2,
  _Inout_opt_ PCtxtHandle    phNewContext,
  _Inout_opt_ PSecBufferDesc pOutput,
  _Out_       PULONG         pfContextAttr,
  _Out_opt_   PTimeStamp     ptsExpiry
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*phCredential* \[在中，選擇性\]
</dt> <dd>

[**AcquireCredentialsHandle (Kerberos)**](acquirecredentialshandle--kerberos.md)所傳回之認證的控制碼。 這個控制碼是用來建立 [*安全性內容*](../secgloss/s-gly.md)。 **InitializeSecurityCoNtext (Kerberos)** 函數至少需要輸出認證。

</dd> <dt>

*phCoNtext* \[在中，選擇性\]
</dt> <dd>

[CtxtHandle](sspi-handles.md)結構的指標。 在第一次呼叫 **InitializeSecurityCoNtext (Kerberos)** 時，此指標為 **Null**。 第二次呼叫時，這個參數是第一個呼叫在 *phNewCoNtext* 參數中傳回之部分格式內容的控制碼指標。

</dd> <dt>

*pszTargetName* \[在\]
</dt> <dd>

以 null 結束的字串指標，指出 (SPN) 的服務主體名稱或目的地伺服器的 [*安全性內容*](../secgloss/s-gly.md) 。

請使用完整的目標名稱，因為跨樹系不支援簡短名稱。

</dd> <dt>

*fCoNtextReq* \[在\]
</dt> <dd>

表示內容要求的位旗標。 並非所有封裝都能支援所有的需求。 用於此參數的旗標前面會加 \_ 上 isc 需求 \_ ，例如，isc 要求 \_ \_ 委派。 這個參數可以是下列其中一個或多個屬性旗標。




| 值 | 意義 | 
|-------|---------|
| <span id="ISC_REQ_ALLOCATE_MEMORY"></span><span id="isc_req_allocate_memory"></span><dl><dt><strong>ISC_REQ_ALLOCATE_MEMORY</strong></dt></dl> | [*安全性套件*](../secgloss/s-gly.md)會為您配置輸出緩衝區。 當您完成使用輸出緩衝區時，請呼叫 [<strong>FreeCoNtextBuffer</strong>](/windows/win32/api/sspi/nf-sspi-freecontextbuffer) 函式釋放它們。<br /> | 
| <span id="ISC_REQ_CONFIDENTIALITY"></span><span id="isc_req_confidentiality"></span><dl><dt><strong>ISC_REQ_CONFIDENTIALITY</strong></dt></dl> | 使用 [<strong>EncryptMessage</strong>](encryptmessage--general.md) 函數來加密訊息。<br /> | 
| <span id="ISC_REQ_CONNECTION"></span><span id="isc_req_connection"></span><dl><dt><strong>ISC_REQ_CONNECTION</strong></dt></dl> | [*安全性內容*](../secgloss/s-gly.md)將不會處理格式化訊息。 此值為預設值。<br /> | 
| <span id="ISC_REQ_DELEGATE"></span><span id="isc_req_delegate"></span><dl><dt><strong>ISC_REQ_DELEGATE</strong></dt></dl> | 伺服器可以使用內容，以用戶端的身分向其他伺服器進行驗證。 必須設定 ISC_REQ_MUTUAL_AUTH 旗標，此旗標才能運作。 適用于 Kerberos。 請忽略此旗標以進行 [*限制委派*](../secgloss/c-gly.md)。<br /> | 
| <span id="ISC_REQ_EXTENDED_ERROR"></span><span id="isc_req_extended_error"></span><dl><dt><strong>ISC_REQ_EXTENDED_ERROR</strong></dt></dl> | 發生錯誤時，將會通知遠端方。<br /> | 
| <span id="ISC_REQ_INTEGRITY"></span><span id="isc_req_integrity"></span><dl><dt><strong>ISC_REQ_INTEGRITY</strong></dt></dl> | 使用 [<strong>EncryptMessage</strong>](encryptmessage--general.md) 和 [<strong>MakeSignature</strong>](makesignature.md) 函數來簽署訊息和驗證簽章。<br /> | 
| <span id="ISC_REQ_MUTUAL_AUTH"></span><span id="isc_req_mutual_auth"></span><dl><dt><strong>ISC_REQ_MUTUAL_AUTH</strong></dt></dl> | 將會滿足服務的相互驗證原則。<br /><blockquote>[!Caution]<br />這並不代表會執行相互驗證，只會滿足服務的驗證原則。 為確保執行相互驗證，請呼叫 [<strong>QueryCoNtextAttributes (Kerberos) </strong>](querycontextattributes--kerberos.md) 函式。</blockquote><br /> | 
| <span id="ISC_REQ_NO_INTEGRITY"></span><span id="isc_req_no_integrity"></span><dl><dt><strong>ISC_REQ_NO_INTEGRITY</strong></dt></dl> | 如果設定此旗標，則會忽略 <strong>ISC_REQ_INTEGRITY</strong> 旗標。<br /> | 
| <span id="ISC_REQ_REPLAY_DETECT"></span><span id="isc_req_replay_detect"></span><dl><dt><strong>ISC_REQ_REPLAY_DETECT</strong></dt></dl> | 偵測使用 [<strong>EncryptMessage</strong>](encryptmessage--general.md) 或 [<strong>MakeSignature</strong>](makesignature.md) 函數編碼的重新執行訊息。<br /> | 
| <span id="ISC_REQ_SEQUENCE_DETECT"></span><span id="isc_req_sequence_detect"></span><dl><dt><strong>ISC_REQ_SEQUENCE_DETECT</strong></dt></dl> | 偵測順序中所接收的訊息。<br /> | 
| <span id="ISC_REQ_STREAM"></span><span id="isc_req_stream"></span><dl><dt><strong>ISC_REQ_STREAM</strong></dt></dl> | 支援資料流程導向連接。<br /> | 
| <span id="ISC_REQ_USE_SESSION_KEY"></span><span id="isc_req_use_session_key"></span><dl><dt><strong>ISC_REQ_USE_SESSION_KEY</strong></dt></dl> | 必須協商新的 [*工作階段金鑰*](../secgloss/s-gly.md) 。<br /> | 




 

用戶端可能不支援要求的屬性。 如需詳細資訊，請參閱 *pfCoNtextAttr* 參數。

如需各種屬性的進一步說明，請參閱 [內容需求](context-requirements.md)。

</dd> <dt>

*Reserved1* \[在\]
</dt> <dd>

此參數是保留的，而且必須設定為零。

</dd> <dt>

*TargetDataRep* \[在\]
</dt> <dd>

目標上的資料標記法，例如位元組順序。 此參數可以是安全性 \_ 原生 \_ DREP 或安全性 \_ 網路 \_ DREP。

</dd> <dt>

*pInput* \[在中，選擇性\]
</dt> <dd>

[**SecBufferDesc**](/windows/win32/api/sspi/ns-sspi-secbufferdesc)結構的指標，其中包含提供給封裝輸入的緩衝區指標。 除非用戶端內容是由伺服器起始，否則這個參數的值在第一次呼叫函式時必須是 **Null** 。 在後續呼叫函式或由伺服器起始用戶端內容時，此參數的值會是配置有足夠記憶體的緩衝區指標，以保存遠端電腦所傳回的權杖。

</dd> <dt>

*Reserved2* \[在\]
</dt> <dd>

此參數是保留的，而且必須設定為零。

</dd> <dt>

*phNewCoNtext* \[in、out、optional\]
</dt> <dd>

[CtxtHandle](sspi-handles.md)結構的指標。 在第一次呼叫 **InitializeSecurityCoNtext (Kerberos)** 時，此指標會收到新的內容控制碼。 第二次呼叫時， *phNewCoNtext* 可以與 *phCoNtext* 參數中指定的控制碼相同。

</dd> <dt>

*pOutput* \[in、out、optional\]
</dt> <dd>

[**SecBufferDesc**](/windows/win32/api/sspi/ns-sspi-secbufferdesc)結構的指標，其中包含接收輸出資料之 [**之 secbuffer**](/windows/win32/api/sspi/ns-sspi-secbuffer)結構的指標。 如果輸入中的緩衝區輸入為 SEC \_ READWRITE，則輸出中會有該緩衝區。 如果要求 (透過 ISC \_ 需求 \_ 配置 \_ 記憶體) ，並在安全性權杖的緩衝區描述項中填入位址，系統將會配置安全性權杖的緩衝區。

</dd> <dt>

*pfCoNtextAttr* \[擴展\]
</dt> <dd>

變數的指標，用來接收一組位旗標，以指出已建立內容的 [*屬性*](../secgloss/a-gly.md#_security_attribute_gly) 。 如需各種屬性的說明，請參閱 [內容需求](context-requirements.md)。

用於此參數的旗標前面會加 \_ 上 isc ret，例如 isc \_ ret \_ 委派。 如需有效值的清單，請參閱 *fCoNtextReq* 參數。

在最後一個函式呼叫成功傳回之前，請勿檢查安全性相關屬性。 與安全性無關的屬性旗標（例如 ASC RET 配置的 \_ \_ \_ 記憶體旗標）可以在最後一次傳回前進行檢查。

> [!Note]  
> 特定內容屬性在與遠端對等的協商期間可能會變更。

 

</dd> <dt>

*ptsExpiry* \[out、optional\]
</dt> <dd>

[**時間戳記**](timestamp.md)結構的指標，此結構會接收內容的到期時間。 我們建議 [*安全性封裝*](../secgloss/s-gly.md) 一律以當地時間傳回此值。 因為此參數是選擇性的，所以應針對短期用戶端傳遞 **Null** 。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果函式成功，函數會傳回下列其中一個成功碼。



| 傳回碼                                                                                                    | Description                                                                                                                                                                                                                                                                                                                                                                                                                 |
|----------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**秒 \_ E \_ 確定**</dt> </dl>                      | 已成功初始化 [*安全性內容*](../secgloss/s-gly.md) 。 [**(Kerberos)**](initializesecuritycontext--kerberos.md)呼叫不需要其他 InitializeSecurityCoNtext。 如果函式傳回輸出 token，也就是，如果 \_ *pOutput* 中的之 secbuffer token 的長度是非零，則該 token 必須傳送至伺服器。<br/> |
| <dl> <dt>**秒 \_ \_ 完成 \_ 並 \_ 繼續**</dt> </dl> | 用戶端必須呼叫 [**CompleteAuthToken**](/windows/win32/api/sspi/nf-sspi-completeauthtoken) ，然後將輸出傳遞至伺服器。 然後，用戶端會等候傳回的權杖，並在另一個呼叫中傳遞它，以 [**InitializeSecurityCoNtext (Kerberos)**](initializesecuritycontext--kerberos.md)。<br/>                                                                                                                                  |
| <dl> <dt>**\_ \_ 需要完成的秒數 \_**</dt> </dl>        | 用戶端必須完成建立訊息，然後呼叫 [**CompleteAuthToken**](/windows/win32/api/sspi/nf-sspi-completeauthtoken) 函數。<br/>                                                                                                                                                                                                                                                                                           |
| <dl> <dt>**每 \_ 秒 \_ 繼續 \_ 需要**</dt> </dl>        | 用戶端必須將輸出 token 傳送至伺服器，並等候傳回權杖。 傳回的權杖接著會在另一個對 [**InitializeSecurityCoNtext (Kerberos)**](initializesecuritycontext--kerberos.md)的呼叫中傳遞。 輸出 token 可以是空的。<br/>                                                                                                                                                       |
| <dl> <dt>**秒 \_ 我 \_ 的 \_ 認證不完整**</dt> </dl> | 使用搭配 Schannel。 伺服器已要求用戶端驗證，而提供的認證不包含憑證或憑證不是由伺服器所信任的憑證授權單位單位 (CA) 。 如需詳細資訊，請參閱＜備註＞。<br/>                                                |



 

如果函式失敗，函數會傳回下列其中一個錯誤碼。



| 傳回碼                                                                                                          | Description                                                                                                                                                                                                                                                                                         |
|----------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**每 \_ 秒 \_ 沒有足夠的 \_ 記憶體**</dt> </dl>          | 沒有足夠的記憶體可完成要求的動作。<br/>                                                                                                                                                                                                                   |
| <dl> <dt>**SEC \_ E \_ 內部 \_ 錯誤**</dt> </dl>               | 發生未對應到 SSPI 錯誤碼的錯誤。<br/>                                                                                                                                                                                                                                |
| <dl> <dt>**SEC \_ E \_ 不正確 \_ 控制碼**</dt> </dl>               | 傳遞給函數的控制碼無效。<br/>                                                                                                                                                                                                                                          |
| <dl> <dt>**SEC \_ E \_ 不正確 \_ 權杖**</dt> </dl>                | 此錯誤是因為輸入標記格式不正確，例如傳輸中損毀、不正確大小的權杖，或傳入錯誤 [*限制委派*](../secgloss/s-gly.md)的權杖。 如果用戶端和伺服器未協調適當的 [*限制委派*](../secgloss/s-gly.md)，就可能會發生將權杖傳遞至錯誤的封裝。<br/> |
| <dl> <dt>**秒 \_ E \_ 登入 \_ 拒絕**</dt> </dl>                 | 登入失敗。<br/>                                                                                                                                                                                                                                                                        |
| <dl> <dt>**SEC \_ E \_ 無 \_ 驗證 \_ 授權單位**</dt> </dl> | 無法連絡任何授權單位進行驗證。 驗證方的功能變數名稱可能錯誤、無法連線到網域，或可能有信任關係失敗。<br/>                                                                                  |
| <dl> <dt>**SEC \_ E \_ 無 \_ 認證**</dt> </dl>               | [*限制委派*](../secgloss/s-gly.md)中不提供任何認證。<br/>                                                                                                                                                  |
| <dl> <dt>**SEC \_ E \_ 目標 \_ 不明**</dt> </dl>               | 無法辨識目標。<br/>                                                                                                                                                                                                                                                           |
| <dl> <dt>**SEC \_ E \_ 不支援的函式 \_**</dt> </dl>         | FCoNtextReq 參數中指定了不正確內容屬性旗標， () 的的 ISC \_ \_ 要求委派或 isc \_ \_ 要求 \_ 的提示 \_ 。 <br/>                                                                                                                                            |
| <dl> <dt>**SEC \_ E \_ 錯誤的 \_ 主體**</dt> </dl>              | 收到驗證要求的主體與傳入 *pszTargetName* 參數的主體不同。 這表示相互驗證失敗。<br/>                                                                                                          |



 

## <a name="remarks"></a>備註

呼叫端負責判斷最終的內容屬性是否足夠。 例如，如果要求了機密性，但無法建立，有些應用程式可能會選擇立即關閉連接。

如果 [*安全性內容*](../secgloss/s-gly.md) 的屬性不足夠，用戶端必須藉由呼叫 [**DeleteSecurityCoNtext**](/windows/win32/api/sspi/nf-sspi-deletesecuritycontext) 函式來釋放部分建立的內容。

用戶端會使用 **InitializeSecurityCoNtext (Kerberos)** 函數來初始化輸出內容。

針對兩階段 [*安全性內容*](../secgloss/s-gly.md)，呼叫順序如下所示：

1.  用戶端會呼叫 *phCoNtext* 設為 **Null** 的函式，並使用輸入訊息填入緩衝區描述項。
2.  [*安全性套件*](../secgloss/s-gly.md)會檢查參數並建立不透明的權杖，並將它放在緩衝區陣列的 token 專案中。 如果 *fCoNtextReq* 參數包含「ISC \_ 需求 \_ 配置記憶體」旗標 \_ ，則 [*安全性封裝*](../secgloss/s-gly.md) 會配置記憶體，並傳回 TOKEN 元素中的指標。
3.  用戶端會將 *pOutput* 緩衝區中傳回的權杖傳送至目標伺服器。 然後，伺服器會在對 [**AcceptSecurityCoNtext (Kerberos)**](acceptsecuritycontext--kerberos.md) 函式的呼叫中，將權杖傳遞為輸入引數。
4.  [**AcceptSecurityCoNtext (Kerberos)**](acceptsecuritycontext--kerberos.md) 可能會傳回權杖，而伺服器會將權杖傳送給用戶端，以進行第二次呼叫 **InitializeSecurityCoNtext (Kerberos)** 如果第一次呼叫傳回時， \_ 我 \_ 需要繼續進行 \_ 。

針對多階段 [*安全性內容*](../secgloss/s-gly.md)，例如相互驗證，呼叫順序如下所示：

1.  用戶端會如先前所述呼叫函式，但封裝會傳回每秒 \_ \_ 繼續 \_ 需要的成功程式碼。
2.  用戶端會將輸出 token 傳送至伺服器，並等候伺服器的回復。
3.  當收到伺服器的回應時，用戶端會再次呼叫 **InitializeSecurityCoNtext (Kerberos)** ，並將 *phCoNtext* 設定為上次呼叫所傳回的控制碼。 從伺服器收到的權杖是在 *pInput* 參數中提供。

如果伺服器已順利回應，則 [*安全性封裝*](../secgloss/s-gly.md) 會傳回 SEC \_ E \_ OK，並且會建立安全會話。

如果函數傳回其中一個錯誤回應，則不接受伺服器的回應，也不會建立會話。

如果函式傳回的秒數 \_ \_ 是我繼續 \_ 需要的，則需要秒完成 \_ \_ \_ ，或每秒 \_ \_ 完成 \_ 並 \_ 繼續進行，步驟2和3會重複執行。

若要初始化 [*安全性內容*](../secgloss/s-gly.md)，根據基礎驗證機制以及 *fCoNtextReq* 參數中指定的選項而定，可能需要對這個函式進行一個以上的呼叫。

*FCoNtextReq* 和 *pfCoNtextAttributes* 參數是代表各種內容屬性的位元遮罩。 如需各種屬性的說明，請參閱 [內容需求](context-requirements.md)。 *PfCoNtextAttributes* 參數在任何成功傳回時都有效，但只有在最後成功傳回時，才應該檢查與內容安全性層面相關的旗標。 例如，中繼傳回可以設定 ISC RET 配置的 \_ \_ \_ 記憶體旗標。

如果 \_ \_ 已設定 ISC 需求使用提供的認證旗標 \_ \_ ，則 [*安全性封裝*](../secgloss/s-gly.md) 必須 \_ \_ 在 *pInput* 輸入緩衝區中尋找之 secbuffer PKG PARAMS 緩衝區類型。 這不是一般的解決方案，但在適當的情況下允許 [*安全套件*](../secgloss/s-gly.md) 和應用程式的強式配對。

如果 \_ \_ 指定了 ISC 要求配置 \_ 記憶體，呼叫端必須藉由呼叫 [**FreeCoNtextBuffer**](/windows/win32/api/sspi/nf-sspi-freecontextbuffer) 函式來釋放記憶體。

例如，輸入權杖可能是 LAN Manager 的挑戰。 在此情況下，輸出權杖會是對挑戰的 NTLM 加密回應。

用戶端所採取的動作取決於此函式的傳回碼。 如果傳回碼為 SEC \_ E \_ OK，將不會有第二個 **InitializeSecurityCoNtext (Kerberos)** 呼叫，且不需要伺服器的回應。 如果傳回碼是每秒 \_ \_ 繼續 \_ 需要的，用戶端就會需要權杖以回應伺服器，並在 **InitializeSecurityCoNtext (Kerberos)** 的第二次呼叫中傳遞權杖。 當 \_ 我 \_ 完成所需的傳回碼時， \_ 會指出用戶端必須完成建立訊息並呼叫 [**CompleteAuthToken**](/windows/win32/api/sspi/nf-sspi-completeauthtoken) 函數。 當 \_ 我 \_ 完成並繼續程式碼時，會 \_ \_ 合併這兩個動作。

如果 **InitializeSecurityCoNtext (Kerberos)** 在第一個 (或只有) 呼叫傳回 success，則呼叫端最後必須在傳回的控制碼上呼叫 [**DeleteSecurityCoNtext**](/windows/win32/api/sspi/nf-sspi-deletesecuritycontext) 函式，即使在驗證交換的後續階段中呼叫失敗也是一樣。

用戶端可能會在 InitializeSecurityCoNtext 成功完成之後，再次呼叫 **(Kerberos)** 。 這會向 [*安全性封裝*](../secgloss/s-gly.md) 指出需要重新驗證。

核心模式呼叫端有下列差異：目標名稱是必須使用 [**VirtualAlloc**](/windows/win32/api/memoryapi/nf-memoryapi-virtualalloc)在虛擬記憶體中配置的 [*Unicode*](../secgloss/u-gly.md)字串;它不得從集區配置。 *PInput* 和 *pOutput* 中傳遞和提供的緩衝區必須在虛擬記憶體中，而不是在集區中。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|--------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows\[僅限 XP desktop 應用程式\]<br/>                                                            |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2003 desktop 應用程式\]<br/>                                                   |
| 標頭<br/>                   | <dl> <dt>Sspi (包含 Security .h) </dt> </dl> |
| 程式庫<br/>                  | <dl> <dt>Secur32 .lib</dt> </dl>                 |
| DLL<br/>                      | <dl> <dt>Secur32.dll</dt> </dl>                 |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[SSPI 函數](authentication-functions.md#sspi-functions)
</dt> <dt>

[**AcceptSecurityCoNtext (Kerberos)**](acceptsecuritycontext--kerberos.md)
</dt> <dt>

[**AcquireCredentialsHandle (Kerberos)**](acquirecredentialshandle--kerberos.md)
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

 

 
