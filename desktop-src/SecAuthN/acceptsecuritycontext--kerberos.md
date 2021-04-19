---
description: 啟用傳輸應用程式的伺服器元件，以便在伺服器與使用 Kerberos 的遠端用戶端之間建立 [*安全性內容*](../secgloss/s-gly.md) 。
ms.assetid: 838eaaa7-6fce-4ed1-bd69-6e76a804c67b
title: 'AcceptSecurityCoNtext (Kerberos) 函數 (Sspi. h) '
ms.topic: reference
ms.date: 07/25/2019
ms.openlocfilehash: 2c379aa0f111e24d534bb14746df4b0e7cbbc9c2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106977369"
---
# <a name="acceptsecuritycontext-kerberos-function"></a>AcceptSecurityCoNtext (Kerberos) 函數

**AcceptSecurityCoNtext (Kerberos)** 函數可讓傳輸應用程式的伺服器元件建立伺服器與遠端用戶端之間的 [*安全性內容*](../secgloss/s-gly.md)。 遠端用戶端會使用 [**InitializeSecurityCoNtext (Kerberos)**](initializesecuritycontext--kerberos.md) 函數來啟動建立 [*安全性內容*](../secgloss/s-gly.md)的程式。 伺服器可能需要來自遠端用戶端的一或多個回復權杖，才能完成 [*安全性內容*](../secgloss/s-gly.md)的建立。

## <a name="syntax"></a>語法


```C++
SECURITY_STATUS SEC_Entry AcceptSecurityContext(
  _In_opt_    PCredHandle    phCredential,
  _In_opt_    PCtxtHandle    phContext,
  _In_opt_    PSecBufferDesc pInput,
  _In_        ULONG          fContextReq,
  _In_        ULONG          TargetDataRep,
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

伺服器認證的控制碼。 伺服器會使用 SECPKG 的「輸入或 SECPKG 認證」旗標來呼叫 [**AcquireCredentialsHandle (Kerberos)**](acquirecredentialshandle--kerberos.md) 函式， \_ 以抓取 \_ \_ \_ 此控制碼。

</dd> <dt>

*phCoNtext* \[in、out、optional\]
</dt> <dd>

[CtxtHandle](sspi-handles.md)結構的指標。 在第一次呼叫 **AcceptSecurityCoNtext (Kerberos)** 時，此指標為 **Null**。 在後續的呼叫中， *phCoNtext* 是第一次呼叫時， *phNewCoNtext* 參數所傳回之部分格式內容的控制碼。

</dd> <dt>

*pInput* \[在中，選擇性\]
</dt> <dd>

用戶端呼叫所產生之 [**SecBufferDesc**](/windows/win32/api/sspi/ns-sspi-secbufferdesc) 結構的指標， [**InitializeSecurityCoNtext (Kerberos)**](initializesecuritycontext--kerberos.md) ，其中包含輸入緩衝區描述項。

除了 [**InitializeSecurityCoNtext (一般)**](initializesecuritycontext--general.md)函式的呼叫所產生的緩衝區外，也可以藉由傳入 **之 secbuffer \_ \_ 通道** 系結類型的 [**之 secbuffer**](/windows/win32/api/sspi/ns-sspi-secbuffer)結構來指定通道系結資訊。 通道系結緩衝區的通道系結資訊，可以藉由在用戶端用來驗證的 Schannel 內容上呼叫 [**QueryCoNtextAttributes (schannel)**](querycontextattributes--schannel.md) 函式取得。

</dd> <dt>

*fCoNtextReq* \[在\]
</dt> <dd>

位旗標，指定伺服器所需的屬性以建立內容。 您可以使用位 **or** 運算結合位旗標。 這個參數可以是下列一或多個值。



| 值                                                                                                                                                                                         | 意義                                                                                                                                                                                                                    |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="ASC_REQ_CONFIDENTIALITY"></span><span id="asc_req_confidentiality"></span><dl> <dt>**ASC \_ 需求 \_ 機密性**</dt> </dl>  | 加密和解密訊息。<br/>                                                                                                                                                                                   |
| <span id="ASC_REQ_CONNECTION"></span><span id="asc_req_connection"></span><dl> <dt>**ASC \_ 需求 \_ 連接**</dt> </dl>                 | [*安全性內容*](../secgloss/s-gly.md)將不會處理格式化訊息。<br/>                                                                                                                                                       |
| <span id="ASC_REQ_DELEGATE"></span><span id="asc_req_delegate"></span><dl> <dt>**ASC \_ 需求 \_ 委派**</dt> </dl>                       | 允許伺服器模擬用戶端。 適用于 Kerberos。 請忽略此旗標以進行 [*限制委派*](../secgloss/c-gly.md)。<br/> |
| <span id="ASC_REQ_EXTENDED_ERROR"></span><span id="asc_req_extended_error"></span><dl> <dt>**ASC \_ 需求 \_ 擴充 \_ 錯誤**</dt> </dl>    | 發生錯誤時，將會通知遠端方。<br/>                                                                                                                                                           |
| <span id="ASC_REQ_INTEGRITY"></span><span id="asc_req_integrity"></span><dl> <dt>**ASC \_ 需求 \_ 完整性**</dt> </dl>                    | 簽署訊息並驗證簽章。<br/>                                                                                                                                                                            |
| <span id="ASC_REQ_REPLAY_DETECT"></span><span id="asc_req_replay_detect"></span><dl> <dt>**ASC 要求重新執行偵測 \_ \_ \_**</dt> </dl>       | 偵測重新執行的封包。<br/>                                                                                                                                                                                        |
| <span id="ASC_REQ_SEQUENCE_DETECT"></span><span id="asc_req_sequence_detect"></span><dl> <dt>**ASC \_ 需求 \_ 序列 \_ 偵測**</dt> </dl> | 偵測順序中所接收的訊息。<br/>                                                                                                                                                                       |



 

如需可能的屬性旗標及其意義，請參閱 [內容需求](context-requirements.md)。 用於此參數的旗標前面會加上 ASC \_ 需求，例如 asc \_ 要求 \_ 委派。

用戶端可能不支援要求的屬性。 如需詳細資訊，請參閱 *pfCoNtextAttr* 參數。

</dd> <dt>

*TargetDataRep* \[在\]
</dt> <dd>

目標上的資料標記法，例如位元組順序。 此參數可以是安全性 \_ 原生 \_ DREP 或安全性 \_ 網路 \_ DREP。

</dd> <dt>

*phNewCoNtext* \[in、out、optional\]
</dt> <dd>

[CtxtHandle](sspi-handles.md)結構的指標。 在第一次呼叫 **AcceptSecurityCoNtext (Kerberos)** 時，此指標會收到新的內容控制碼。 在後續的呼叫中， *phNewCoNtext* 可以與 *phCoNtext* 參數中指定的控制碼相同。

</dd> <dt>

*pOutput* \[in、out、optional\]
</dt> <dd>

[**SecBufferDesc**](/windows/win32/api/sspi/ns-sspi-secbufferdesc)結構的指標，其中包含輸出緩衝區描述項。 此緩衝區會傳送至用戶端，以輸入 [**InitializeSecurityCoNtext (Kerberos)**](initializesecuritycontext--kerberos.md)的其他呼叫。 即使函數傳回 SEC E OK，也可能產生輸出緩衝區 \_ \_ 。 任何產生的緩衝區都必須傳送回用戶端應用程式。

</dd> <dt>

*pfCoNtextAttr* \[擴展\]
</dt> <dd>

變數的指標，此變數會接收一組位旗標，以指出已建立內容的屬性。 如需各種屬性的說明，請參閱 [內容需求](context-requirements.md)。 用於此參數的旗標前面會加上 ASC \_ ret，例如 asc \_ ret \_ 委派。

在最後一個函式呼叫成功傳回之前，請勿檢查安全性相關屬性。 與安全性無關的屬性旗標（例如 ASC \_ RET 配置 \_ 的 \_ 記憶體旗標）可以在最後一次傳回前進行檢查。

</dd> <dt>

*ptsTimeStamp* \[out、optional\]
</dt> <dd>

[**時間戳記**](timestamp.md)結構的指標，此結構會接收內容的到期時間。 我們建議 [*安全性封裝*](../secgloss/s-gly.md) 一律以當地時間傳回此值。

> [!Note]  
> 在驗證程式的最後一個呼叫之前，內容的到期時間可能會不正確，因為在後續的協商階段中將會提供更多的資訊。 因此，在最後一次呼叫函式之前， *ptsTimeStamp* 必須是 **Null** 。

 

</dd> </dl>

## <a name="return-value"></a>傳回值

此函數會傳回下列其中一個值。



<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><thead><tr class="header"><th>傳回碼/值</th><th>Description</th></tr></thead><tbody><tr class="odd"><td><dl> <dt><strong>SEC_E_INSUFFICIENT_MEMORY</strong></dt> <dt>0x80090300L</dt> </dl></td><td>函數失敗。 沒有足夠的記憶體可完成要求的動作。<br/></td></tr><tr class="even"><td><dl> <dt><strong>SEC_E_INTERNAL_ERROR</strong></dt> <dt>0x80090304L</dt> </dl></td><td>函數失敗。 發生未對應到 SSPI 錯誤碼的錯誤。<br/></td></tr><tr class="odd"><td><dl> <dt><strong>SEC_E_INVALID_HANDLE</strong></dt> <dt>0x80100003L</dt> </dl></td><td>函數失敗。 傳遞給函數的控制碼無效。<br/></td></tr><tr class="even"><td><dl> <dt><strong>SEC_E_INVALID_TOKEN</strong></dt> <dt>0x80090308L</dt> </dl></td><td>函數失敗。 傳遞給函數的 token 無效。<br/></td></tr><tr class="odd"><td><dl> <dt><strong>SEC_E_LOGON_DENIED</strong></dt> <dt>0x8009030CL</dt> </dl></td><td>登入失敗。<br/></td></tr><tr class="even"><td><dl> <dt><strong>SEC_E_NO_AUTHENTICATING_AUTHORITY</strong></dt> <dt>0x80090311L</dt> </dl></td><td>函數失敗。 無法連絡任何授權單位進行驗證。 這可能是因為下列狀況：<br/><ul><li>驗證方的功能變數名稱不正確。</li><li>網域無法使用。</li><li>信任關係失敗。</li></ul></td></tr><tr class="odd"><td><dl> <dt><strong>SEC_E_OK</strong></dt> <dt>0x00000000L</dt> </dl></td><td>此函數已成功。 接受從用戶端接收的 [*安全性內容*](../secgloss/s-gly.md) 。 如果輸出 token 是由函式所產生，則必須將它傳送至用戶端進程。<br/></td></tr><tr class="even"><td><dl> <dt><strong>SEC_E_UNSUPPORTED_FUNCTION</strong></dt> <dt>0x80090302L</dt> </dl></td><td>函數失敗。 在 <em>fCoNtextReq</em> 參數中指定了無效 (ASC_REQ_DELEGATE 或 ASC_REQ_PROMPT_FOR_CREDS) 的內容屬性旗標。 使用 Schannel SSP 時，可以傳回這個值。<br/></td></tr><tr class="odd"><td><dl> <dt><strong>SEC_I_COMPLETE_AND_CONTINUE</strong></dt> <dt>0x00090314L</dt> </dl></td><td>此函數已成功。 伺服器必須呼叫 [<strong>CompleteAuthToken</strong>] (/windows/win32/api/sspi/nf-sspi-completeauthtoken) ，並將輸出 token 傳遞給用戶端。 然後伺服器會等候來自用戶端的傳回權杖，然後對 [<strong>AcceptSecurityCoNtext (Kerberos) </strong>] (acceptsecuritycoNtext--kerberos.md) 進行另一次呼叫。<br/></td></tr><tr class="even"><td><dl> <dt><strong>SEC_I_COMPLETE_NEEDED</strong></dt> <dt>0x00090313L</dt> </dl></td><td>此函數已成功。 伺服器必須完成從用戶端建立訊息，然後呼叫 [<strong>CompleteAuthToken</strong>] (/windows/win32/api/sspi/nf-sspi-completeauthtoken) 函數。<br/></td></tr><tr class="odd"><td><dl> <dt><strong>SEC_I_CONTINUE_NEEDED</strong></dt> <dt>0x00090312L</dt> </dl></td><td>此函數已成功。 伺服器必須將輸出 token 傳送給用戶端，並等候傳回的權杖。 傳回的權杖應該在 <em>pInput</em> 中傳遞給 [<strong>AcceptSecurityCoNtext (Kerberos) </strong>] (acceptsecuritycoNtext--kerberos.md) 的另一個呼叫。<br/></td></tr></tbody></table>



 

## <a name="remarks"></a>備註

**AcceptSecurityCoNtext (kerberos)** 函數是 [**InitializeSecurityCoNtext (Kerberos)**](initializesecuritycontext--kerberos.md)函數的伺服器對應項。

當伺服器收到來自用戶端的要求時，伺服器會使用 *fCoNtextReq* 參數來指定它需要的會話。 如此一來，伺服器可以指定用戶端必須能夠使用機密或 [*完整性*](../secgloss/i-gly.md)檢查的會話，而且它可以拒絕不符合該要求的用戶端。 或者，伺服器可能不需要任何專案，而且用戶端可以提供或需要的任何專案，都會在 *pfCoNtextAttr* 參數中傳回。

針對支援多階段驗證的封裝，例如相互驗證，呼叫順序如下所示：

1.  用戶端會將權杖傳送至伺服器。
2.  伺服器第一次呼叫 **AcceptSecurityCoNtext (Kerberos)** ，它會產生回復權杖，然後傳送至用戶端。
3.  用戶端會接收權杖，並將它傳遞給 [**InitializeSecurityCoNtext (Kerberos)**](initializesecuritycontext--kerberos.md)。 如果 **InitializeSecurityCoNtext (Kerberos)** 會傳回 SEC \_ E \_ OK，相互驗證已完成，而且可以開始安全的會話。 如果 **InitializeSecurityCoNtext (Kerberos)** 傳回錯誤碼，相互驗證協商就會結束。 否則， **InitializeSecurityCoNtext (Kerberos)** 所傳回的安全性權杖會傳送至用戶端，並重複步驟2和3。

*FCoNtextReq* 和 *pfCoNtextAttr* 參數是代表各種內容屬性的位元遮罩。 如需各種屬性的說明，請參閱 [內容需求](context-requirements.md)。

> [!Note]  
> *PfCoNtextAttr* 參數在任何成功傳回時都有效，但只有在最後成功傳回時，才應該檢查與內容安全性層面相關的旗標。 例如，中繼傳回可以設定 ISC RET 配置的 \_ \_ \_ 記憶體旗標。

 

呼叫端負責判斷最終的內容屬性是否足夠。 例如，如果要求加密)  (加密，但無法建立，有些應用程式可能會選擇立即關閉連接。 如果無法建立 [*安全性內容*](../secgloss/s-gly.md) ，伺服器必須藉由呼叫 [**DeleteSecurityCoNtext**](/windows/win32/api/sspi/nf-sspi-deletesecuritycontext) 函式來釋放部分建立的內容。 如需何時呼叫 **DeleteSecurityCoNtext** 函數的詳細資訊，請參閱 **DeleteSecurityCoNtext**。

建立 [*安全性內容*](../secgloss/s-gly.md) 之後，伺服器應用程式可以使用 [**QuerySecurityCoNtextToken**](/windows/win32/api/sspi/nf-sspi-querysecuritycontexttoken) 函式來抓取用戶端憑證所對應之使用者帳戶的控制碼。 此外，伺服器也可以使用 [**ImpersonateSecurityCoNtext**](/windows/win32/api/sspi/nf-sspi-impersonatesecuritycontext) 函數來模擬使用者。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|--------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 WINDOWS XP desktop 應用程式\]<br/>                                                            |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2003 \[ desktop 應用程式\]<br/>                                                   |
| 標頭<br/>                   | <dl> <dt>Sspi (包含 Security .h) </dt> </dl> |
| 程式庫<br/>                  | <dl> <dt>Secur32 .lib</dt> </dl>                 |
| DLL<br/>                      | <dl> <dt>Secur32.dll</dt> </dl>                 |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[SSPI 函數](authentication-functions.md#sspi-functions)
</dt> <dt>

[**DeleteSecurityCoNtext**](/windows/win32/api/sspi/nf-sspi-deletesecuritycontext)
</dt> <dt>

[**InitializeSecurityCoNtext (Kerberos)**](initializesecuritycontext--kerberos.md)
</dt> </dl>

 

 
