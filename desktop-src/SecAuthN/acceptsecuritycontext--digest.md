---
description: 啟用傳輸應用程式的伺服器元件，以便在伺服器與使用摘要的遠端用戶端之間建立安全性內容。
ms.assetid: 017683e3-b21a-4e97-9232-582ac7dbd5b2
title: 'AcceptSecurityCoNtext (Digest) 函數 (Sspi. h) '
ms.topic: article
ms.date: 07/25/2019
ms.openlocfilehash: 11ffa801612f14f5b9aaf61e7d48b61377bc9e56
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/05/2021
ms.locfileid: "104035230"
---
# <a name="acceptsecuritycontext-digest-function"></a>AcceptSecurityCoNtext (Digest) 函數

**AcceptSecurityCoNtext (Digest)** 函數可讓傳輸應用程式的伺服器元件建立伺服器與遠端用戶端之間的 [*安全性內容*](../secgloss/s-gly.md)。 遠端用戶端會使用 [**InitializeSecurityCoNtext (Digest)**](initializesecuritycontext--digest.md) 函數來啟動建立安全性內容的程式。 伺服器可能需要來自遠端用戶端的一或多個回復權杖，才能完成安全性內容的建立。

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
  _Out_opt_   PTimeStamp     ptsExpiry
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*phCredential* \[在中，選擇性\]
</dt> <dd>

伺服器認證的控制碼。 伺服器會呼叫 [**AcquireCredentialsHandle (Digest)**](acquirecredentialshandle--digest.md) 函式，並將 \_ \_ \_ \_ 兩個旗標設定為取得此控制碼。

</dd> <dt>

*phCoNtext* \[in、out、optional\]
</dt> <dd>

[CtxtHandle](sspi-handles.md)結構的指標。 在第一次呼叫 **AcceptSecurityCoNtext (Digest)** 時，此指標為 **Null**。 在後續的呼叫中， *phCoNtext* 是第一次呼叫時， *phNewCoNtext* 參數所傳回之部分格式內容的控制碼。

</dd> <dt>

*pInput* \[在中，選擇性\]
</dt> <dd>

用戶端呼叫所產生之 [**SecBufferDesc**](/windows/win32/api/sspi/ns-sspi-secbufferdesc) 結構的指標， [**InitializeSecurityCoNtext (摘要)**](initializesecuritycontext--digest.md) ，其中包含輸入緩衝區描述項。

下表顯示摘要式 HTTP 的緩衝區設定。 第一個緩衝區的型別必須是 **之 secbuffer \_ TOKEN**，而其餘的必須是 **之 secbuffer \_ PKG \_ PARAMS** 型別。 SASL 只需要緩衝區零。



| 緩衝區 \# /buffer 類型                                                                                                                                                                                                 | 意義                                                                                                                                                                  |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="0"></span><dl> <dt>**0**</dt> <dt>**之 secbuffer \_ 權杖**</dt> </dl>                                        | 第一個呼叫會是空的，而第二個呼叫則是從用戶端收到的挑戰回應。<br/>                                                             |
| <span id="1"></span><dl> <dt>**1**</dt> <dt>**之 secbuffer \_ PKG \_ PARAMS**</dt> </dl>                                  | 方法。 字元是來自要求行的有線格式。 US ASCII 單一位元組字元。<br/>                                                                |
| <span id="2"></span><dl> <dt>**2**</dt> <dt>**之 secbuffer \_ PKG \_ PARAMS**</dt> </dl>                                  | 保留的。<br/>                                                                                                                                                     |
| <span id="3"></span><dl> <dt>**3**</dt> <dt>**之 secbuffer \_ PKG \_ PARAMS**</dt> </dl>                                  | HEntity. H (實體主體) 的十六進位標記法。 US ASCII 單一位元組字元。<br/>                                                                       |
| <span id="4"></span><dl> <dt>**4**</dt> <dt>**之 secbuffer \_ PKG \_ PARAMS**</dt> </dl>                                  | 領域。 挑戰的領域字串。 必須在 US ASCII 中表示的 Unicode 字串。<br/>                                                                 |
| <span id="5"></span><dl> <dt>**5**</dt> <dt>**之 secbuffer \_ 通道 \_** 系結 \| **之 secbuffer \_ READONLY**</dt> </dl> | 包含通道系結 token 值。<br/> **Windows server 2008、Windows Vista、Windows server 2003 和 WINDOWS XP：** 不支援這個值。<br/> |



 

</dd> <dt>

*fCoNtextReq* \[在\]
</dt> <dd>

位旗標，指定伺服器所需的屬性以建立內容。 您可以使用位 **or** 運算結合位旗標。 這個參數可以是下列一或多個值。



| 值                                                                                                                                                                                                                                          | 意義                                                                                                                                                                                                                                                                                                                                                                                                                     |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="ASC_REQ_ALLOCATE_MEMORY"></span><span id="asc_req_allocate_memory"></span><dl> <dt>**ASC \_ 需求 \_ 配置 \_ 記憶體**</dt> </dl>                                                  | 摘要會為您配置輸出緩衝區。 當您完成使用輸出緩衝區時，請呼叫 [**FreeCoNtextBuffer**](/windows/win32/api/sspi/nf-sspi-freecontextbuffer) 函式釋放它們。<br/>                                                                                                                                                                                                                                      |
| <span id="ASC_REQ_ALLOW_MISSING_BINDINGS"></span><span id="asc_req_allow_missing_bindings"></span><dl> <dt>**ASC \_ 需求 \_ 允許 \_ 遺漏 \_ 系結**</dt> </dl>                            | 表示摘要不需要內部和外部通道的通道系結。 當端點通道系結的支援未知時，此值會用於回溯相容性。<br/> 此值與 **ASC \_ 需求 \_ PROXY \_** 系結互斥。<br/> **Windows server 2008、Windows Vista、Windows server 2003 和 WINDOWS XP：** 不支援這個值。<br/> <br/> |
| <span id="ASC_REQ_CONFIDENTIALITY"></span><span id="asc_req_confidentiality"></span><dl> <dt>**ASC \_ 需求 \_ 機密性**</dt> </dl>                                                   | 加密和解密訊息。 <br/> 摘要 SSP 僅支援 SASL 的此旗標。<br/>                                                                                                                                                                                                                                                                                                                       |
| <span id="ASC_REQ_PROXY_BINDINGS"></span><span id="asc_req_proxy_bindings"></span><dl> <dt>**ASC \_ 需求 \_ PROXY 系結 \_**</dt> </dl>                                                     | 表示摘要需要通道系結。<br/> 此值與 **ASC 要求 \_ \_ 允許 \_ 遺漏 \_** 系結互斥。<br/> **Windows server 2008、Windows Vista、Windows server 2003 和 WINDOWS XP：** 不支援這個值。<br/> <br/>                                                                                                                                         |
| <span id="ASC_REQ_CONNECTION"></span><span id="asc_req_connection"></span><dl> <dt>**ASC \_ 需求 \_ 連接**</dt> </dl>                                                                  | [*安全性內容*](../secgloss/s-gly.md)將不會處理格式化訊息。<br/>                                                                                                                                                                                                                                                                                                                                                        |
| <span id="ASC_REQ_EXTENDED_ERROR"></span><span id="asc_req_extended_error"></span><dl> <dt>**ASC \_ 需求 \_ 擴充 \_ 錯誤**</dt> </dl>                                                     | 發生錯誤時，將會通知遠端方。<br/>                                                                                                                                                                                                                                                                                                                                                            |
| <span id="ASC_REQ_HTTP__0x10000000_"></span><span id="asc_req_http__0x10000000_"></span><span id="ASC_REQ_HTTP__0X10000000_"></span><dl> <dt>**ASC \_ 需求 \_ HTTP (0x10000000)**</dt> </dl> | 針對 HTTP 使用 Digest。 省略此旗標以使用摘要做為 SASL 機制。<br/>                                                                                                                                                                                                                                                                                                                                          |
| <span id="ASC_REQ_INTEGRITY"></span><span id="asc_req_integrity"></span><dl> <dt>**ASC \_ 需求 \_ 完整性**</dt> </dl>                                                                     | 簽署訊息並驗證簽章。<br/>                                                                                                                                                                                                                                                                                                                                                                             |
| <span id="ASC_REQ_REPLAY_DETECT"></span><span id="asc_req_replay_detect"></span><dl> <dt>**ASC 要求重新執行偵測 \_ \_ \_**</dt> </dl>                                                        | 偵測重新執行的封包。<br/>                                                                                                                                                                                                                                                                                                                                                                                         |
| <span id="ASC_REQ_SEQUENCE_DETECT"></span><span id="asc_req_sequence_detect"></span><dl> <dt>**ASC \_ 需求 \_ 序列 \_ 偵測**</dt> </dl>                                                  | 偵測順序中所接收的訊息。<br/>                                                                                                                                                                                                                                                                                                                                                                        |



 

如需可能的屬性旗標及其意義，請參閱 [內容需求](context-requirements.md)。 用於此參數的旗標前面會加上 ASC \_ 需求，例如 asc \_ 要求 \_ 委派。

用戶端可能不支援要求的屬性。 如需詳細資訊，請參閱 *pfCoNtextAttr* 參數。

</dd> <dt>

*TargetDataRep* \[在\]
</dt> <dd>

目標上的資料標記法，例如位元組順序。 此參數可以是安全性 \_ 原生 \_ DREP 或安全性 \_ 網路 \_ DREP。

此參數不會與摘要 SSP 一起使用。 當您使用摘要 SSP 時，請為此參數指定零。

</dd> <dt>

*phNewCoNtext* \[in、out、optional\]
</dt> <dd>

[CtxtHandle](sspi-handles.md)結構的指標。 在第一次呼叫 **AcceptSecurityCoNtext (Digest)** 時，此指標會收到新的內容控制碼。 在後續的呼叫中， *phNewCoNtext* 可以與 *phCoNtext* 參數中指定的控制碼相同。

</dd> <dt>

*pOutput* \[in、out、optional\]
</dt> <dd>

[**SecBufferDesc**](/windows/win32/api/sspi/ns-sspi-secbufferdesc)結構的指標，其中包含輸出緩衝區描述項。 此緩衝區會傳送至用戶端，以輸入 [**InitializeSecurityCoNtext (Digest)**](initializesecuritycontext--digest.md)的其他呼叫。 即使函數傳回 SEC E OK，也可能產生輸出緩衝區 \_ \_ 。 任何產生的緩衝區都必須傳送回用戶端應用程式。

</dd> <dt>

*pfCoNtextAttr* \[擴展\]
</dt> <dd>

變數的指標，此變數會接收一組位旗標，以指出已建立內容的屬性。 如需各種屬性的說明，請參閱 [內容需求](context-requirements.md)。 用於此參數的旗標前面會加上 ASC \_ ret，例如 asc \_ ret \_ 委派。

在最後一個函式呼叫成功傳回之前，請勿檢查安全性相關屬性。 與安全性無關的屬性旗標（例如 ASC \_ RET 配置 \_ 的 \_ 記憶體旗標）可以在最後一次傳回前進行檢查。

</dd> <dt>

*ptsTimeStamp* \[out、optional\]
</dt> <dd>

[**時間戳記**](timestamp.md)結構的指標，此結構會接收內容的到期時間。 我們建議 [*安全性封裝*](../secgloss/s-gly.md) 一律以當地時間傳回此值。

此參數會設定為常數的最長時間。 摘要式 [*安全性內容*](../secgloss/s-gly.md)或認證或使用摘要 SSP 時，沒有到期時間。

> [!Note]  
> 在驗證程式的最後一個呼叫之前，內容的到期時間可能會不正確，因為在後續的協商階段中將會提供更多的資訊。 因此，在最後一次呼叫函式之前， *ptsTimeStamp* 必須是 **Null** 。

 

</dd> </dl>

## <a name="return-value"></a>傳回值

此函數會傳回下列其中一個值。



<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><thead><tr class="header"><th>傳回碼/值</th><th>Description</th></tr></thead><tbody><tr class="odd"><td><dl> <dt><strong>SEC_E_INSUFFICIENT_MEMORY</strong></dt> <dt>0x80090300L</dt> </dl></td><td>函數失敗。 沒有足夠的記憶體可完成要求的動作。<br/></td></tr><tr class="even"><td><dl> <dt><strong>SEC_E_INTERNAL_ERROR</strong></dt> <dt>0x80090304L</dt> </dl></td><td>函數失敗。 發生未對應到 SSPI 錯誤碼的錯誤。<br/></td></tr><tr class="odd"><td><dl> <dt><strong>SEC_E_INVALID_HANDLE</strong></dt> <dt>0x80100003L</dt> </dl></td><td>函數失敗。 傳遞給函數的控制碼無效。<br/></td></tr><tr class="even"><td><dl> <dt><strong>SEC_E_INVALID_TOKEN</strong></dt> <dt>0x80090308L</dt> </dl></td><td>函數失敗。 傳遞給函數的 token 無效。<br/></td></tr><tr class="odd"><td><dl> <dt><strong>SEC_E_LOGON_DENIED</strong></dt> <dt>0x8009030CL</dt> </dl></td><td>登入失敗。<br/></td></tr><tr class="even"><td><dl> <dt><strong>SEC_E_NO_AUTHENTICATING_AUTHORITY</strong></dt> <dt>0x80090311L</dt> </dl></td><td>函數失敗。 無法連絡任何授權單位進行驗證。 這可能是因為下列狀況：<br/><ul><li>驗證方的功能變數名稱不正確。</li><li>網域無法使用。</li><li>信任關係失敗。</li></ul></td></tr><tr class="odd"><td><dl> <dt><strong>SEC_E_NO_CREDENTIALS</strong></dt> <dt>0x8009030EL</dt> </dl></td><td>函數失敗。 <em>PhCredential</em>參數中指定的認證控制碼無效。<br/></td></tr><tr class="even"><td><dl> <dt><strong>SEC_E_OK</strong></dt> <dt>0x00000000L</dt> </dl></td><td>此函數已成功。 接受從用戶端接收的 [*安全性內容*](../secgloss/s-gly.md) 。 如果輸出 token 是由函式所產生，則必須將它傳送至用戶端進程。<br/></td></tr><tr class="odd"><td><dl> <dt><strong>SEC_E_SECURITY_QOS_FAILED</strong></dt> <dt>0x80090332L</dt> </dl></td><td>函數失敗。 在 <em>fCoNtextReq</em> 參數中指定了不正確內容屬性旗標。<br/></td></tr><tr class="even"><td><dl> <dt><strong>SEC_I_COMPLETE_AND_CONTINUE</strong></dt> <dt>0x00090314L</dt> </dl></td><td>此函數已成功。 伺服器必須呼叫 [<strong>CompleteAuthToken</strong>] (/windows/win32/api/sspi/nf-sspi-completeauthtoken) ，並將輸出 token 傳遞給用戶端。 然後伺服器會等候來自用戶端的傳回權杖，然後對 [<strong>AcceptSecurityCoNtext (Digest) </strong>] (acceptsecuritycoNtext--digest.md) 進行另一個呼叫。<br/></td></tr><tr class="odd"><td><dl> <dt><strong>SEC_I_COMPLETE_NEEDED</strong></dt> <dt>0x00090313L</dt> </dl></td><td>此函數已成功。 伺服器必須完成從用戶端建立訊息，然後呼叫 [<strong>CompleteAuthToken</strong>] (/windows/win32/api/sspi/nf-sspi-completeauthtoken) 函數。<br/></td></tr><tr class="even"><td><dl> <dt><strong>SEC_I_CONTINUE_NEEDED</strong></dt> <dt>0x00090312L</dt> </dl></td><td>此函數已成功。 伺服器必須將輸出 token 傳送給用戶端，並等候傳回的權杖。 傳回的權杖應該在 <em>pInput</em> 中傳遞給 [<strong>AcceptSecurityCoNtext (Digest) </strong>] (acceptsecuritycoNtext--digest.md) 的另一個呼叫。<br/></td></tr><tr class="odd"><td><dl> <dt><strong>STATUS_LOGON_FAILURE</strong></dt> <dt>0xC000006DL</dt> </dl></td><td>函數失敗。 建立指定的內容之後，會呼叫 [<strong>AcceptSecurityCoNtext (Digest) </strong>] (acceptsecuritycoNtext--digest.md) 函數。<br/></td></tr><tr class="even"><td><dl> <dt><strong>SEC_E_BAD_BINDINGS</strong></dt> <dt>0x80090346L</dt> </dl></td><td>函數失敗。 未滿足通道系結原則。<br/></td></tr></tbody></table>



 

## <a name="remarks"></a>備註

**AcceptSecurityCoNtext (digest)** 函數是 [**InitializeSecurityCoNtext (Digest)**](initializesecuritycontext--digest.md)函數的伺服器對應項。

當伺服器收到來自用戶端的要求時，伺服器會使用 *fCoNtextReq* 參數來指定它需要的會話。 如此一來，伺服器可以指定用戶端必須能夠使用機密或 [*完整性*](../secgloss/i-gly.md)檢查的會話，而且它可以拒絕不符合該要求的用戶端。 或者，伺服器可能不需要任何專案，而且用戶端可以提供或需要的任何專案，都會在 *pfCoNtextAttr* 參數中傳回。

針對支援多階段驗證的封裝，例如相互驗證，呼叫順序如下所示：

1.  用戶端會將權杖傳送至伺服器。
2.  伺服器第一次呼叫 **AcceptSecurityCoNtext (Digest)** ，它會產生回復權杖，然後傳送至用戶端。
3.  用戶端會接收權杖，並將它傳遞給 [**InitializeSecurityCoNtext (摘要)**](initializesecuritycontext--digest.md)。 如果 **InitializeSecurityCoNtext (Digest)** 會傳回 SEC \_ E \_ OK，相互驗證已完成，而且可以開始安全的會話。 如果 **InitializeSecurityCoNtext (Digest)** 傳回錯誤碼，相互驗證協商就會結束。 否則， **InitializeSecurityCoNtext (Digest)** 所傳回的安全性權杖會傳送至用戶端，並重複步驟2和3。

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

[**InitializeSecurityCoNtext (摘要)**](initializesecuritycontext--digest.md)
</dt> </dl>

 

 
