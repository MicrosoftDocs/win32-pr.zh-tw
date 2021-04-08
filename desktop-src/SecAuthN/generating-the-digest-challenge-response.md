---
description: 從伺服器收到挑戰之後，用戶端會藉由呼叫 InitializeSecurityCoNtext (Digest) 函數來建立摘要挑戰回應。
ms.assetid: b26b5676-a614-4017-a4e5-a5395292a667
title: 產生摘要挑戰回應
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8b577334348745425db23d3de41431ba4e37b7af
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103851760"
---
# <a name="generating-the-digest-challenge-response"></a>產生摘要挑戰回應

從伺服器收到挑戰之後，用戶端會藉由呼叫 [**InitializeSecurityCoNtext (digest)**](/windows/win32/api/sspi/nf-sspi-initializesecuritycontexta) 函數來建立摘要挑戰回應。 此函式會使用來自挑戰的要求資源和資料的相關資訊來產生 MD5 [*雜湊*](/windows/desktop/SecGloss/h-gly) 指紋，並輸出代表部分 [*安全性內容*](/windows/desktop/SecGloss/s-gly)的安全性權杖。 若要完成驗證，用戶端必須將權杖傳回到發出挑戰的伺服器。

下表描述 [**InitializeSecurityCoNtext (Digest)**](/windows/win32/api/sspi/nf-sspi-initializesecuritycontexta) [*函數*](/windows/desktop/SecGloss/c-gly)的參數，以及在建立摘要挑戰回應時要提供的值。



| 參數                  | Description                                                                                                                                                                                               |
|----------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| *fCoNtextReq*<br/>   | 用戶端要求的安全性內容屬性。 如需詳細資訊，請參閱摘要挑戰回應內容需求。<br/>                                                             |
| *pszTargetName*<br/> | HTTP：以 Null 終止的字串，指定目標 URL。<br/> SASL：指定 DNS/SPN 目標的以 Null 結束的字串。<br/>                                                         |
| *pInput*<br/>        | 包含摘要 SSP 所需資訊的緩衝區。 如需詳細資訊，請參閱 [摘要挑戰回應的輸入緩衝區](input-buffers-for-the-digest-challenge-response.md)。<br/> |
| *pfCoNtextAttr*<br/> | 接收傳回的安全性內容所支援的屬性。 如需詳細資訊，請參閱摘要挑戰回應內容需求。<br/>                                                  |
| *pOutput*<br/>       | \_接收要傳回給伺服器之安全性權杖的之 secbuffer TOKEN 類型緩衝區位址。<br/>                                                                                           |



 

## <a name="digest-challenge-response-context-requirements"></a>摘要挑戰回應內容需求

內容需求是決定下列事項的旗標：

-   Microsoft Digest 是否做為 SASL 機制或 HTTP 驗證通訊協定。
-   用戶端和伺服器所共用的 [*安全性內容*](/windows/desktop/SecGloss/s-gly) 所支援的保護品質。

根據預設，Microsoft Digest 會作為 SASL 機制。

內容需求會指定為傳遞給 [**InitializeSecurityCoNtext**](/windows/win32/api/sspi/nf-sspi-initializesecuritycontexta)函數之 *fCoNtextReq* 參數的旗標。 旗標會藉由控制挑戰回應中的 qop 指示詞，來影響安全性內容的保護品質。

根據預設，qop 指示詞會設定為 "auth"。 若要產生將 qop 設定為 "auth-int" 的挑戰回應，必須執行下列動作：

1.  摘要挑戰必須將 qop 指示詞設為 "auth-int"。
2.  用戶端必須指定下列一或多個旗標：

    -   ISC \_ 需求 \_ 完整性
    -   ISC 要求重新執行偵測 \_ \_ \_
    -   會偵測 \_ 到 ISC 需求 \_ 順序 \_

僅限 SASL：藉由指定 ISC 要求機密性旗標，以將 qop 指示詞設定為 "auth" 來產生挑戰回應 \_ \_ 。 因為此旗標對 HTTP 驗證無效，所以無法與 ISC 要求 HTTP 旗標一起使用 \_ \_ 。

## <a name="verifying-the-quality-of-protection"></a>確認保護品質

用戶端必須檢查 [**InitializeSecurityCoNtext**](/windows/win32/api/sspi/nf-sspi-initializesecuritycontexta) 函式的 *pfCoNtextAttr* 參數中所傳回的安全性內容屬性旗標。 只有當旗標所指出的保護品質足以滿足其用途時，用戶端才應該將挑戰回應傳送至伺服器。 相關的旗標可以是下列各項的任意組合：

-   ISC \_ RET \_ 完整性
-   ISC RET 重新執行偵測 \_ \_ \_
-   ISC \_ RET \_ 序列 \_ 偵測
-   ISC \_ RET \_ 機密性僅 (SASL 內容) 

如需 qop 指示詞的詳細資訊，請參閱 [保護品質和密碼](quality-of-protection-and-ciphers.md)。

如需挑戰回應指示詞的詳細資訊，請參閱 [摘要挑戰回應的內容](contents-of-a-digest-challenge-response.md)。

 

