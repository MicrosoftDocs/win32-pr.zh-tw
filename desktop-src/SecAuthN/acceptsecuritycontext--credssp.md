---
description: 讓傳輸應用程式的伺服器元件建立伺服器與遠端用戶端之間的安全性內容。
ms.assetid: a53f733e-b646-4431-b021-a2c446308849
title: AcceptSecurityCoNtext (CredSSP) 函數
ms.topic: article
ms.date: 07/25/2019
ms.openlocfilehash: 681e03ea15729cc8726d63551e8b7b0a2b39ecac
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106983519"
---
# <a name="acceptsecuritycontext-credssp-function"></a>AcceptSecurityCoNtext (CredSSP) 函數

**AcceptSecurityCoNtext (CredSSP)** 函數可讓傳輸應用程式的伺服器元件建立伺服器與遠端用戶端之間的安全性內容。 遠端用戶端會呼叫 [**InitializeSecurityCoNtext (CredSSP)**](initializesecuritycontext--credssp.md) 函數來啟動建立安全性內容的程式。 伺服器可能需要來自遠端用戶端的一或多個回復權杖，才能完成安全性內容的建立。

## <a name="syntax"></a>語法

```C++
SECURITY_STATUS SEC_ENTRY AcceptSecurityContext(
  _In_opt_    PCredHandle    phCredential,
  _In_opt_    PCtxtHandle    phContext,
  _In_opt_    PSecBufferDesc pInput,
  _In_        unsigned long  fContextReq,
  _In_        unsigned long  TargetDataRep,
  _Inout_opt_ PCtxtHandle    phNewContext,
  _Inout_opt_ PSecBufferDesc pOutput,
  _Out_       unsigned long  *pfContextAttr,
  _Out_opt_   PTimeStamp     ptsExpiry
);
```

## <a name="parameters"></a>參數

*phCredential* \[在中，選擇性\]

伺服器認證的控制碼。 為了取得此控制碼，伺服器會呼叫 [**AcquireCredentialsHandle (CredSSP)**](acquirecredentialshandle--credssp.md) 函式，並同時設定 SECPKG 的認證 \_ \_ 輸入或 SECPKG 認證 \_ \_ 兩個旗標。

*phCoNtext* \[在中，選擇性\]

[CtxtHandle](sspi-handles.md)結構的指標。 在第一次呼叫 **AcceptSecurityCoNtext (CredSSP)** 時，此指標為 **Null**。 在後續的呼叫中， *phCoNtext* 會指定第一次呼叫時，在 *phNewCoNtext* 參數中傳回的部分格式內容。

*pInput* \[在中，選擇性\]

用戶端呼叫所產生之 [**SecBufferDesc**](/windows/win32/api/sspi/ns-sspi-secbufferdesc) 結構的指標， [**InitializeSecurityCoNtext (CredSSP)**](initializesecuritycontext--credssp.md)。 結構包含輸入緩衝區描述項。

第一個緩衝區的型別必須是 **之 secbuffer \_ TOKEN** ，並且包含從用戶端收到的安全性權杖。 第二個緩衝區的類型應該是 **之 secbuffer \_ EMPTY**。

*fCoNtextReq* \[在\]

-位旗標，指定伺服器所需的屬性以建立內容。 您可以使用位 **or** 運算結合位旗標。 這個參數可以是下列一或多個值。

| 值                          | 意義                                                                                                                                                                                                        |
|--------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **ASC \_ 需求 \_ 配置 \_ 記憶體** | 認證安全性支援提供者 (CredSSP) 將會配置輸出緩衝區。 當您完成使用輸出緩衝區時，請呼叫 [**FreeCoNtextBuffer**](/windows/win32/api/sspi/nf-sspi-freecontextbuffer) 函式釋放它們。 |
| **ASC \_ 需求 \_ 連接**       | 安全性內容將不會處理格式化訊息。                                                                                                                                                      |
| **ASC \_ 需求 \_ 委派**         | 允許伺服器模擬用戶端。 請忽略此旗標以進行限制委派。                                                         |
| **ASC \_ 需求 \_ 擴充 \_ 錯誤**  | 發生錯誤時，將會通知遠端方。                                                                                                                                                          |
| **ASC 要求重新執行偵測 \_ \_ \_**   | 偵測重新執行的封包。                                                                                                                                                                                       |
| **ASC \_ 需求 \_ 序列 \_ 偵測** | 偵測順序中所接收的訊息。                                                                                                                                                                      |
| **ASC \_ 需求 \_ 資料流程**           | 支援資料流程導向連接。                                                                                                                                                                          |

如需可能的屬性旗標及其意義，請參閱 [內容需求](context-requirements.md)。 用於此參數的旗標前面會加上 ASC \_ 需求，例如 asc \_ 要求 \_ 委派。

用戶端可能不支援要求的屬性。 如需詳細資訊，請參閱 *pfCoNtextAttr* 參數。

*TargetDataRep* \[在\]

目標上的資料標記法，例如位元組順序。 此參數可以是 **安全性 \_ 原生 \_ DREP** 或 **安全性 \_ 網路 \_ DREP**。

*phNewCoNtext* \[in、out、optional\]

[CtxtHandle](sspi-handles.md)結構的指標。 在第一次呼叫 **AcceptSecurityCoNtext (CredSSP)** 時，此指標會收到新的內容控制碼。 在後續的呼叫中， *phNewCoNtext* 可以與 *phCoNtext* 參數中指定的控制碼相同。

*pOutput* \[in、out、optional\]

[**SecBufferDesc**](/windows/win32/api/sspi/ns-sspi-secbufferdesc)結構的指標，其中包含輸出緩衝區描述項。 此緩衝區會傳送至用戶端，以輸入至 [**InitializeSecurityCoNtext (CredSSP)**](initializesecuritycontext--credssp.md)的其他呼叫。 即使函數傳回 SEC E OK，也可能產生輸出緩衝區 \_ \_ 。 任何產生的緩衝區都必須傳送回用戶端應用程式。

在輸出時，此緩衝區會接收資訊安全內容的權杖。 權杖必須傳送至用戶端。 函數也可以傳回之 SECBUFFER 額外的緩衝區 \_ 。

*pfCoNtextAttr* \[擴展\]

一組位旗標的指標，指出已建立內容的屬性。 如需各種屬性的說明，請參閱 [內容需求](context-requirements.md)。 用於此參數的旗標前面會加上 ASC \_ ret，例如 asc \_ ret \_ 委派。

在最後一個函式呼叫成功傳回之前，請勿檢查安全性相關屬性。 與安全性無關的屬性旗標（例如 ASC \_ RET 配置 \_ 的 \_ 記憶體旗標）可以在最後一次傳回前進行檢查。

*ptsExpiry* \[out、optional\]

[**時間戳記**](timestamp.md)結構的指標，此結構會接收內容的到期時間。 我們建議安全性封裝一律以當地時間傳回此值。

> [!Note]  
> 在驗證程式的最後一個呼叫之前，內容的到期時間可能會不正確，因為在後續的協商階段中將會提供更多的資訊。 因此，在最後一次呼叫函式之前， *ptsTimeStamp* 必須是 **Null** 。

## <a name="return-value"></a>傳回值

此函數會傳回下列其中一個值。

| 傳回碼/值                                   | Description                                                                                                                                                                 |
|-----------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| SEC_E_INCOMPLETE_MESSAGE <br/> 0x80090318L          | 此函數已成功。 輸入緩衝區中的資料不完整。 應用程式必須從用戶端讀取其他資料，並再次呼叫 [<strong>AcceptSecurityCoNtext (CredSSP) </strong>](acceptsecuritycontext--credssp.md) 。 |
| SEC_E_INSUFFICIENT_MEMORY <br/> 0x80090300L         | 函數失敗。 沒有足夠的記憶體可完成要求的動作。                                                                                 |
| SEC_E_INTERNAL_ERROR <br/> 0x80090304L              | 函數失敗。 發生未對應到 SSPI 錯誤碼的錯誤。                                                                                              |
| SEC_E_INVALID_HANDLE <br/> 0x80100003L              | 函數失敗。 傳遞給函數的控制碼無效。                                                                                                        |
| SEC_E_INVALID_TOKEN <br/> 0x80090308L               | 函數失敗。 傳遞給函數的 token 無效。                                                                                                         |
| SEC_E_LOGON_DENIED <br/> 0x8009030CL                | 登入失敗。                                                                                                                                                           |
| SEC_E_NO_AUTHENTICATING_AUTHORITY <br/> 0x80090311L | 函數失敗。 無法連絡任何授權單位進行驗證。 這可能是因為下列狀況：<br/><ul><li>驗證方的功能變數名稱不正確。</li><li>網域無法使用。</li><li>信任關係失敗。 |
| SEC_E_NO_CREDENTIALS <br/>0x8009030EL               | 函數失敗。 *PhCredential* 參數中指定的認證控制碼無效。                            |
| SEC_E_OK <br/> 0x00000000L                          | 此函數已成功。 接受從用戶端接收的安全性內容。 如果函式產生輸出 token，則必須將標記傳送至用戶端進程。 |
| SEC_E_UNSUPPORTED_FUNCTION <br/> 0x80090302L        | 函數失敗。 *FCoNtextReq* 參數指定了內容屬性旗標 (ASC_REQ_DELEGATE 或 ASC_REQ_PROMPT_FOR_CREDS) 無效。                       |
| SEC_I_COMPLETE_AND_CONTINUE <br/> 0x00090314L       | 此函數已成功。 伺服器必須呼叫 [**CompleteAuthToken**](/windows/win32/api/sspi/nf-sspi-completeauthtoken) ，並將輸出 token 傳遞給用戶端。 然後，伺服器必須等待用戶端的傳回權杖，再對 [**AcceptSecurityCoNtext (CredSSP)**](acceptsecuritycontext--credssp.md)進行另一個呼叫。 |
| SEC_I_COMPLETE_NEEDED <br/> 0x00090313L             | 此函數已成功。 伺服器必須先完成從用戶端建立訊息，然後再呼叫 [ **CompleteAuthToken**](/windows/win32/api/sspi/nf-sspi-completeauthtoken)                             |
| SEC_I_CONTINUE_NEEDED <br/> 0x00090312L             | 此函數已成功。 伺服器必須將輸出 token 傳送給用戶端，並等候傳回的權杖。 針對 [**AcceptSecurityCoNtext (CredSSP)**](acceptsecuritycontext--credssp.md)的另一次呼叫，應該在 *pInput* 中傳遞傳回的權杖。


## <a name="remarks"></a>備註

**AcceptSecurityCoNtext (credssp)** 函數是 [**InitializeSecurityCoNtext (CredSSP)**](initializesecuritycontext--credssp.md)函數的伺服器對應項。

當伺服器收到來自用戶端的要求時，它會使用 *fCoNtextReq* 參數來指定它需要的會話。 如此一來，伺服器就可以要求用戶端能夠使用機密或 [*完整性*](../secgloss/i-gly.md)檢查的會話;它可以拒絕不符合該要求的用戶端。 或者，伺服器也不需要任何東西;無論用戶端需要或可提供的內容，都會在 *pfCoNtextAttr* 參數中傳回。

*FCoNtextReq* 和 *pfCoNtextAttr* 參數是代表各種內容屬性的位元遮罩。 如需各種屬性的說明，請參閱 [內容需求](context-requirements.md)。

> [!Note]  
> 雖然 *pfCoNtextAttr* 參數在任何成功傳回時都有效，但您應該只在最終成功傳回時，檢查有關內容安全性層面的旗標。 例如，中繼傳回可以設定 ISC RET 配置的 \_ \_ \_ 記憶體旗標。

呼叫端負責判斷最終的內容屬性是否足夠。 例如，如果要求加密)  (加密，但無法建立，有些應用程式可能會選擇立即關閉連接。 如果無法建立安全性內容，伺服器必須藉由呼叫 [**DeleteSecurityCoNtext**](/windows/win32/api/sspi/nf-sspi-deletesecuritycontext) 函式來釋放部分建立的內容。 如需何時呼叫 **DeleteSecurityCoNtext** 函數的詳細資訊，請參閱 **DeleteSecurityCoNtext**。

建立安全性內容之後，伺服器應用程式可以使用 [**QuerySecurityCoNtextToken**](/windows/win32/api/sspi/nf-sspi-querysecuritycontexttoken) 函式來抓取用戶端憑證所對應之使用者帳戶的控制碼。 此外，伺服器也可以使用 [**ImpersonateSecurityCoNtext**](/windows/win32/api/sspi/nf-sspi-impersonatesecuritycontext) 函數來模擬使用者。

## <a name="requirements"></a>規格需求

| 需求 | 值 |
|--------------------------|-------------------------------------------|
| 最低支援的用戶端 | \[僅限 Windows Vista 桌面應用程式\]       |
| 最低支援的伺服器 | 僅限 Windows Server 2008 \[ desktop 應用程式\] |
| 標頭                   | Sspi (包含 Security .h)                |
| 程式庫                  | Secur32 .lib                               |
| DLL                      | Secur32.dll                               |

## <a name="see-also"></a>另請參閱

- [SSPI 函數](authentication-functions.md#sspi-functions)
- [**DeleteSecurityCoNtext**](/windows/win32/api/sspi/nf-sspi-deletesecuritycontext)
- [**InitializeSecurityCoNtext (CredSSP)**](initializesecuritycontext--credssp.md)
