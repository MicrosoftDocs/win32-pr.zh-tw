---
description: 啟用傳輸應用程式的伺服器元件，以在使用 Schannel 的伺服器與遠端用戶端之間建立 [*安全性內容*](../secgloss/s-gly.md) 。
ms.assetid: 03fd5272-8476-4c93-8590-0d00acf6a130
title: 'AcceptSecurityCoNtext (Schannel) 函數 (Sspi. h) '
ms.topic: reference
ms.date: 07/25/2019
ms.openlocfilehash: 2700704c9fc1c40fc2d5648306147c5091a318e5c8bd4383bb32bc5416c8d069
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119141641"
---
# <a name="acceptsecuritycontext-schannel-function"></a>AcceptSecurityCoNtext (Schannel) 函數

**AcceptSecurityCoNtext (Schannel)** 函數可讓傳輸應用程式的伺服器元件建立伺服器與遠端用戶端之間的 [*安全性內容*](../secgloss/s-gly.md)。 遠端用戶端會使用 [**InitializeSecurityCoNtext (Schannel)**](initializesecuritycontext--schannel.md) 函數來啟動建立 [*安全性內容*](../secgloss/s-gly.md)的程式。 伺服器可能需要來自遠端用戶端的一或多個回復權杖，才能完成 [*安全性內容*](../secgloss/s-gly.md)的建立。

## <a name="syntax"></a>語法


```C++
SECURITY_STATUS SEC_Entry AcceptSecurityContext(
  _In_opt_    PCredHandle    phCredential,
  _Inout_opt_ PCtxtHandle    phContext,
  _In_opt_    PSecBufferDesc pInput,
  _In_        ULONG          fContextReq,
  _In_        ULONG          TargetDataRep,
  _Inout_opt_ PCtxtHandle    phNewContext,
  _Inout_opt_ PSecBufferDesc pOutput,
  _Out_       PULONG         pfContextAttr,
  _Out_opt_   PTimeStamp     ptsTimeStamp
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*phCredential* \[在中，選擇性\]
</dt> <dd>

伺服器認證的控制碼。 伺服器會呼叫 [**AcquireCredentialsHandle (Schannel)**](acquirecredentialshandle--schannel.md) 函式，並將 \_ \_ \_ \_ 兩個旗標設定為取得此控制碼。

</dd> <dt>

*phCoNtext* \[in、out、optional\]
</dt> <dd>

[CtxtHandle](sspi-handles.md)結構的指標。 在第一次呼叫 **AcceptSecurityCoNtext (Schannel)** 時，此指標為 **Null**。 在後續的呼叫中， *phCoNtext* 是第一次呼叫時， *phNewCoNtext* 參數所傳回之部分格式內容的控制碼。

</dd> <dt>

*pInput* \[在中，選擇性\]
</dt> <dd>

用戶端呼叫所產生之 [**SecBufferDesc**](/windows/win32/api/sspi/ns-sspi-secbufferdesc) 結構的指標， [**InitializeSecurityCoNtext (Schannel)**](initializesecuritycontext--schannel.md) ，其中包含輸入緩衝區描述項。

使用 [*安全通道安全性支援提供者*](../secgloss/s-gly.md) (SSP) 時，第一個緩衝區必須是類型之 secbuffer \_ 權杖，並且包含從用戶端收到的安全性權杖。 第二個緩衝區的類型應該是之 SECBUFFER \_ EMPTY。

</dd> <dt>

*fCoNtextReq* \[在\]
</dt> <dd>

位旗標，指定伺服器所需的屬性以建立內容。 您可以使用位 **or** 運算結合位旗標。 這個參數可以是下列一或多個值。



| 值                                                                                                                                                                                         | 意義                                                                                                                                                                                                 |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="ASC_REQ_ALLOCATE_MEMORY"></span><span id="asc_req_allocate_memory"></span><dl> <dt>**ASC \_ 需求 \_ 配置 \_ 記憶體**</dt> </dl> | 摘要式和 Schannel 將為您配置輸出緩衝區。 當您完成使用輸出緩衝區時，請呼叫 [**FreeCoNtextBuffer**](/windows/win32/api/sspi/nf-sspi-freecontextbuffer) 函式釋放它們。<br/> |
| <span id="ASC_REQ_CONFIDENTIALITY"></span><span id="asc_req_confidentiality"></span><dl> <dt>**ASC \_ 需求 \_ 機密性**</dt> </dl>  | 加密和解密訊息。<br/> 摘要 SSP 僅支援 SASL 的此旗標。<br/>                                                                                                    |
| <span id="ASC_REQ_CONNECTION"></span><span id="asc_req_connection"></span><dl> <dt>**ASC \_ 需求 \_ 連接**</dt> </dl>                 | [*安全性內容*](../secgloss/s-gly.md)將不會處理格式化訊息。<br/>                                                                                                                                    |
| <span id="ASC_REQ_EXTENDED_ERROR"></span><span id="asc_req_extended_error"></span><dl> <dt>**ASC \_ 需求 \_ 擴充 \_ 錯誤**</dt> </dl>    | 發生錯誤時，將會通知遠端方。<br/>                                                                                                                                        |
| <span id="ASC_REQ_MUTUAL_AUTH"></span><span id="asc_req_mutual_auth"></span><dl> <dt>**ASC \_ 要求 \_ 相互 \_ 驗證**</dt> </dl>             | 用戶端必須提供要用於用戶端驗證的憑證。<br/>                                                                                                         |
| <span id="ASC_REQ_REPLAY_DETECT"></span><span id="asc_req_replay_detect"></span><dl> <dt>**ASC 要求重新執行偵測 \_ \_ \_**</dt> </dl>       | 偵測重新執行的封包。<br/>                                                                                                                                                                     |
| <span id="ASC_REQ_SEQUENCE_DETECT"></span><span id="asc_req_sequence_detect"></span><dl> <dt>**ASC \_ 需求 \_ 序列 \_ 偵測**</dt> </dl> | 偵測順序中所接收的訊息。<br/>                                                                                                                                                    |
| <span id="ASC_REQ_STREAM"></span><span id="asc_req_stream"></span><dl> <dt>**ASC \_ 需求 \_ 資料流程**</dt> </dl>                             | 支援資料流程導向連接。<br/> 只有 Schannel 才支援此旗標。<br/>                                                                                                    |



 

如需可能的屬性旗標及其意義，請參閱 [內容需求](context-requirements.md)。 用於此參數的旗標前面會加上 ASC \_ 需求，例如 asc \_ 要求 \_ 委派。

用戶端可能不支援要求的屬性。 如需詳細資訊，請參閱 *pfCoNtextAttr* 參數。

</dd> <dt>

*TargetDataRep* \[在\]
</dt> <dd>

此參數不適用於 Schannel。 請為此參數指定零。

</dd> <dt>

*phNewCoNtext* \[in、out、optional\]
</dt> <dd>

[CtxtHandle](sspi-handles.md)結構的指標。 在第一次呼叫 **AcceptSecurityCoNtext (Schannel)** 時，此指標會收到新的內容控制碼。 在後續的呼叫中， *phNewCoNtext* 可以與 *phCoNtext* 參數中指定的控制碼相同。

</dd> <dt>

*pOutput* \[in、out、optional\]
</dt> <dd>

[**SecBufferDesc**](/windows/win32/api/sspi/ns-sspi-secbufferdesc)結構的指標，其中包含輸出緩衝區描述項。 此緩衝區會傳送至用戶端，以輸入 [**InitializeSecurityCoNtext (Schannel)**](initializesecuritycontext--schannel.md)的其他呼叫。 即使函數傳回 SEC E OK，也可能產生輸出緩衝區 \_ \_ 。 任何產生的緩衝區都必須傳送回用戶端應用程式。

在輸出時，此緩衝區會接收資訊 [*安全內容*](../secgloss/s-gly.md)的權杖。 權杖必須傳送至用戶端。 函數也可以傳回之 SECBUFFER 額外的緩衝區 \_ 。 此外，呼叫端必須傳入 **之 secbuffer \_ 警示** 類型的緩衝區。 在輸出時，如果產生警示，此緩衝區就會包含該警示的相關資訊，而且該函式會失敗。

</dd> <dt>

*pfCoNtextAttr* \[擴展\]
</dt> <dd>

變數的指標，此變數會接收一組位旗標，以指出已建立內容的屬性。 如需各種屬性的說明，請參閱 [內容需求](context-requirements.md)。 用於此參數的旗標前面會加上 ASC \_ ret，例如 asc \_ ret \_ 委派。

在最後一個函式呼叫成功傳回之前，請勿檢查安全性相關屬性。 與安全性無關的屬性旗標（例如 ASC \_ RET 配置 \_ 的 \_ 記憶體旗標）可以在最後一次傳回前進行檢查。

</dd> <dt>

*ptsTimeStamp* \[out、optional\]
</dt> <dd>

[**時間戳記**](timestamp.md)結構的指標，此結構會接收內容的到期時間。 我們建議 [*安全性封裝*](../secgloss/s-gly.md) 一律以當地時間傳回此值。

這在使用 Schannel SSP 時是選擇性的。 當遠端物件提供要用於驗證的憑證時，此參數會收到該憑證的到期時間。 如果未提供任何憑證，則會傳回最大時間值。

> [!Note]  
> 在驗證程式的最後一個呼叫之前，內容的到期時間可能會不正確，因為在後續的協商階段中將會提供更多的資訊。 因此，在最後一次呼叫函式之前， *ptsTimeStamp* 必須是 **Null** 。

 

</dd> </dl>

## <a name="return-value"></a>傳回值

此函數會傳回下列其中一個值。



<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><thead><tr class="header"><th>傳回碼/值</th><th>描述</th></tr></thead><tbody><tr class="odd"><td><dl> <dt><strong>SEC_E_INCOMPLETE_MESSAGE</strong></dt> <dt>0x80090318L</dt> </dl></td><td>此函數已成功。 輸入緩衝區中的資料不完整。 應用程式必須從用戶端讀取其他資料，並再次呼叫 [<strong>AcceptSecurityCoNtext (Schannel) </strong>] (acceptsecuritycoNtext--schannel.md) 。<br/> 傳回這個值時， <em>pInput</em>緩衝區就會包含 [<strong>之 secbuffer</strong>] (/windows/win32/api/sspi/ns-sspi-secbuffer) 結構，其中含有<strong>SECBUFFER_MISSING</strong>的<strong>BufferType</strong>成員。 <strong>之 secbuffer</strong>的<strong>cbBuffer</strong>成員包含一個值，這個值表示函式在此函式成功之前，必須從用戶端讀取的額外位元組數目。 雖然此數目不一定是精確的，但使用它可以避免多次呼叫此函式來協助效能。<br/></td></tr><tr class="even"><td><dl> <dt><strong>SEC_E_INSUFFICIENT_MEMORY</strong></dt> <dt>0x80090300L</dt> </dl></td><td>函數失敗。 沒有足夠的記憶體可完成要求的動作。<br/></td></tr><tr class="odd"><td><dl> <dt><strong>SEC_E_INTERNAL_ERROR</strong></dt> <dt>0x80090304L</dt> </dl></td><td>函數失敗。 發生未對應到 SSPI 錯誤碼的錯誤。<br/></td></tr><tr class="even"><td><dl> <dt><strong>SEC_E_INVALID_HANDLE</strong></dt> <dt>0x80100003L</dt> </dl></td><td>函數失敗。 傳遞給函數的控制碼無效。<br/></td></tr><tr class="odd"><td><dl> <dt><strong>SEC_E_INVALID_TOKEN</strong></dt> <dt>0x80090308L</dt> </dl></td><td>函數失敗。 傳遞給函數的 token 無效。<br/></td></tr><tr class="even"><td><dl> <dt><strong>SEC_E_LOGON_DENIED</strong></dt> <dt>0x8009030CL</dt> </dl></td><td>登入失敗。<br/></td></tr><tr class="odd"><td><dl> <dt><strong>SEC_E_NO_AUTHENTICATING_AUTHORITY</strong></dt> <dt>0x80090311L</dt> </dl></td><td>函數失敗。 無法連絡任何授權單位進行驗證。 這可能是因為下列狀況：<br/><ul><li>驗證方的功能變數名稱不正確。</li><li>網域無法使用。</li><li>信任關係失敗。</li></ul></td></tr><tr class="even"><td><dl> <dt><strong>SEC_E_NO_CREDENTIALS</strong></dt> <dt>0x8009030EL</dt> </dl></td><td>函數失敗。 <em>PhCredential</em>參數中指定的認證控制碼無效。 使用 Digest 或 Schannel SSP 時，可以傳回這個值。<br/></td></tr><tr class="odd"><td><dl> <dt><strong>SEC_E_OK</strong></dt> <dt>0x00000000L</dt> </dl></td><td>此函數已成功。 接受從用戶端接收的 [*安全性內容*](../secgloss/s-gly.md) 。 如果輸出 token 是由函式所產生，則必須將它傳送至用戶端進程。<br/></td></tr><tr class="even"><td><dl> <dt><strong>SEC_E_UNSUPPORTED_FUNCTION</strong></dt> <dt>0x80090302L</dt> </dl></td><td>函數失敗。 在 <em>fCoNtextReq</em> 參數中指定了無效 (ASC_REQ_DELEGATE 或 ASC_REQ_PROMPT_FOR_CREDS) 的內容屬性旗標。<br/></td></tr><tr class="odd"><td><dl> <dt><strong>SEC_E_APPLICATION_PROTOCOL_MISMATCH</strong></dt> <dt>0x80090367L</dt> </dl></td><td>用戶端與伺服器之間不存在一般的應用程式協定。<br/></td></tr><tr class="even"><td><dl> <dt><strong>SEC_I_COMPLETE_AND_CONTINUE</strong></dt> <dt>0x00090314L</dt> </dl></td><td>此函數已成功。 伺服器必須呼叫 [<strong>CompleteAuthToken</strong>] (/windows/win32/api/sspi/nf-sspi-completeauthtoken) ，並將輸出 token 傳遞給用戶端。 然後伺服器會等候來自用戶端的傳回權杖，然後對 [<strong>AcceptSecurityCoNtext (Schannel) </strong>] (acceptsecuritycoNtext--schannel.md) 進行另一次呼叫。 <br/></td></tr><tr class="odd"><td><dl> <dt><strong>SEC_I_COMPLETE_NEEDED</strong></dt> <dt>0x00090313L</dt> </dl></td><td>此函數已成功。 伺服器必須完成從用戶端建立訊息，然後呼叫 [<strong>CompleteAuthToken</strong>] (/windows/win32/api/sspi/nf-sspi-completeauthtoken) 函數。<br/></td></tr><tr class="even"><td><dl> <dt><strong>SEC_I_CONTINUE_NEEDED</strong></dt> <dt>0x00090312L</dt> </dl></td><td>此函數已成功。 伺服器必須將輸出 token 傳送給用戶端，並等候傳回的權杖。 傳回的權杖應該在 <em>pInput</em> 中傳遞給 [<strong>AcceptSecurityCoNtext (Schannel) </strong>] (acceptsecuritycoNtext--schannel.md) 的另一個呼叫。<br/></td></tr><tr class="odd"><td><dl> <dt><strong>STATUS_LOGON_FAILURE</strong></dt> <dt>0xC000006DL</dt> </dl></td><td>函數失敗。 建立指定的內容之後，會呼叫 [<strong>AcceptSecurityCoNtext (Schannel) </strong>] (acceptsecuritycoNtext--schannel.md) 函數。 使用摘要 SSP 時，可以傳回這個值。<br/></td></tr></tbody></table>



 

## <a name="remarks"></a>備註

**AcceptSecurityCoNtext (schannel)** 函數是 [**InitializeSecurityCoNtext (Schannel)**](initializesecuritycontext--schannel.md)函式的伺服器對應項。

當伺服器收到來自用戶端的要求時，伺服器會使用 *fCoNtextReq* 參數來指定它需要的會話。 如此一來，伺服器可以指定用戶端必須能夠使用機密或 [*完整性*](../secgloss/i-gly.md)檢查的會話，而且它可以拒絕不符合該要求的用戶端。 或者，伺服器可能不需要任何專案，而且用戶端可以提供或需要的任何專案，都會在 *pfCoNtextAttr* 參數中傳回。

針對支援多階段驗證的封裝，例如相互驗證，呼叫順序如下所示：

1.  用戶端會將權杖傳送至伺服器。
2.  伺服器第一次呼叫 **AcceptSecurityCoNtext (Schannel)** ，它會產生回復權杖，然後傳送至用戶端。
3.  用戶端會接收權杖，並將它傳遞給 [**InitializeSecurityCoNtext (Schannel)**](initializesecuritycontext--schannel.md)。 如果 **InitializeSecurityCoNtext (Schannel)** 會傳回 SEC \_ E \_ OK，相互驗證已完成，而且可以開始安全的會話。 如果 **InitializeSecurityCoNtext (Schannel)** 傳回錯誤碼，相互驗證協商就會結束。 否則， **InitializeSecurityCoNtext (Schannel)** 所傳回的安全性權杖會傳送至用戶端，並重複步驟2和3。

*FCoNtextReq* 和 *pfCoNtextAttr* 參數是代表各種內容屬性的位元遮罩。 如需各種屬性的說明，請參閱 [內容需求](context-requirements.md)。

> [!Note]  
> *PfCoNtextAttr* 參數在任何成功傳回時都有效，但只有在最後成功傳回時，才應該檢查與內容安全性層面相關的旗標。 例如，中繼傳回可以設定 ISC RET 配置的 \_ \_ \_ 記憶體旗標。

 

呼叫端負責判斷最終的內容屬性是否足夠。 例如，如果要求加密)  (加密，但無法建立，有些應用程式可能會選擇立即關閉連接。 如果無法建立 [*安全性內容*](../secgloss/s-gly.md) ，伺服器必須藉由呼叫 [**DeleteSecurityCoNtext**](/windows/win32/api/sspi/nf-sspi-deletesecuritycontext) 函式來釋放部分建立的內容。 如需何時呼叫 **DeleteSecurityCoNtext** 函數的詳細資訊，請參閱 **DeleteSecurityCoNtext**。

建立 [*安全性內容*](../secgloss/s-gly.md) 之後，伺服器應用程式可以使用 [**QuerySecurityCoNtextToken**](/windows/win32/api/sspi/nf-sspi-querysecuritycontexttoken) 函式來抓取用戶端憑證所對應之使用者帳戶的控制碼。 此外，伺服器也可以使用 [**ImpersonateSecurityCoNtext**](/windows/win32/api/sspi/nf-sspi-impersonatesecuritycontext) 函數來模擬使用者。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|--------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 8.1 \[僅限桌面應用程式\]<br/>                                                           |
| 最低支援的伺服器<br/> | Windows Server 2012\[僅限 R2 desktop 應用程式\]<br/>                                                |
| 標頭<br/>                   | <dl> <dt>Sspi (包含 Security .h) </dt> </dl> |
| 程式庫<br/>                  | <dl> <dt>Secur32 .lib</dt> </dl>                 |
| DLL<br/>                      | <dl> <dt>Secur32.dll</dt> </dl>                 |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[SSPI 函數](authentication-functions.md#sspi-functions)
</dt> <dt>

[**DeleteSecurityCoNtext**](/windows/win32/api/sspi/nf-sspi-deletesecuritycontext)
</dt> <dt>

[**InitializeSecurityCoNtext (Schannel)**](initializesecuritycontext--schannel.md)
</dt> </dl>

 

 
