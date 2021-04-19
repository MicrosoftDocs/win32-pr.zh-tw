---
title: Create-Session 的 Ack
description: 使用 Create-Session 封包的 Ack 來確認用戶端的 Create-Session 要求。
ms.assetid: eeb8ff83-2a7f-4fef-9df7-8c12febfcf36
keywords:
- Create-Session BITS 的 Ack
topic_type:
- apiref
api_name:
- Ack for Create-Session
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2d978ec4c5693a5087734975c412b999ed7d5890
ms.sourcegitcommit: 73417d55867c804274a55abe5ca71bcba7006119
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/20/2020
ms.locfileid: "106967933"
---
# <a name="ack-for-create-session"></a>Create-Session 的 Ack

使用 **建立會話** 封包的 Ack 來確認用戶端的 [**建立會話**](create-session.md) 要求。

``` syntax
reason-code reason-description
BITS-Packet-Type: Ack
BITS-Protocol: {guid}
BITS-Session-Id: {guid}
BITS-Host-Id: PublicHostName
BITS-Host-Id-Fallback-Timeout: Timeout
Accept-Encoding: Identity
Content-Length: length
BITS-Error-Code: error-code
BITS-Error-Context: error-context
```

## <a name="headers"></a>標題

<dl> <dt>

<span id="reason-code"></span><span id="REASON-CODE"></span>原因-代碼
</dt> <dd>

以 HTTP 原因代碼取代 reason 碼。 下表顯示回應 [**建立會話**](create-session.md) 要求的一般原因代碼。 如需 HTTP 原因代碼的清單，請參閱 [RFC 2616](https://www.ietf.org/rfc/rfc2616.txt)。



| 原因代碼    | 描述                                                                         |
|----------------|-------------------------------------------------------------------------------------|
| 200<br/> | 正常。 要求成功。<br/>                                          |
| 201<br/> | 已建立。 已建立會話。<br/>                                        |
| 403<br/> | 禁止。 不允許使用者將檔案上傳至指定的 URL。<br/> |
| 404<br/> | 找不到。 指定的 URL 不存在。<br/>                             |
| 409<br/> | 衝突。 檔案存在於伺服器上，無法覆寫。<br/>       |



 

</dd> <dt>

<span id="reason-description"></span><span id="REASON-DESCRIPTION"></span>原因-描述
</dt> <dd>

以與原因代碼相關聯的 HTTP 描述取代 reason 描述。 例如，如果 reason-code 是200，請將 reason 描述設定為 OK。

</dd> <dt>

<span id="BITS-Packet-Type"></span><span id="bits-packet-type"></span><span id="BITS-PACKET-TYPE"></span>BITS-封包類型
</dt> <dd>

將此回應封包識別為 Ack 封包。

</dd> <dt>

<span id="BITS-Protocol"></span><span id="bits-protocol"></span><span id="BITS-PROTOCOL"></span>BITS-通訊協定
</dt> <dd>

字串 GUID，可識別伺服器要用於此會話的通訊協定。 將 {guid} 取代為用戶端在 [**建立會話**](create-session.md) 要求中包含的通訊協定清單中的通訊協定識別碼;支援 BITS 的通訊協定標頭包含清單。 只有當原因代碼為200或201時，才包含此標頭。

</dd> <dt>

<span id="BITS-Session-Id"></span><span id="bits-session-id"></span><span id="BITS-SESSION-ID"></span>位-會話識別碼
</dt> <dd>

識別此會話給用戶端的字串 GUID。 將 {guid} 取代為用戶端在所有後續要求封包中傳送的會話識別碼。

BITS 使用 GUID 來識別會話，但您可以使用最多100個字元的任何 HTTP 合法字串。

</dd> <dt>

<span id="BITS-Host-Id"></span><span id="bits-host-id"></span><span id="BITS-HOST-ID"></span>BITS-主機-識別碼
</dt> <dd>

選擇性。 只有在設定 [BITS IIS 延伸模組屬性](bits-iis-extension-properties.md)BITSHostId 時，才包含此標頭。 將 PublicHostName 取代為 BITSHostId 屬性中的伺服器名稱或 IP 位址。

用戶端必須在所有後續的封包上取代遠端 URL 的伺服器部分。 如果用戶端未在後續的封包上指定此主機名稱，則該作業可能會在伺服器陣列中的另一部伺服器上再次開始，而在先前的伺服器上留下部分上傳檔案。

</dd> <dt>

<span id="BITS-Host-Id-Fallback-Timeout"></span><span id="bits-host-id-fallback-timeout"></span><span id="BITS-HOST-ID-FALLBACK-TIMEOUT"></span>BITS-主機-識別碼-回溯-Timeout
</dt> <dd>

選擇性。 只有在指定 BITS-主機識別碼標頭時，才包含此標頭。 將 Timeout 取代為 BITSHostIdFallbackTimeout 屬性的超時值。 BITSHostIdFallbackTimeout 屬性是其中一個 [BITS IIS 延伸模組屬性](bits-iis-extension-properties.md)。

用戶端會使用超時時間來判斷在還原為作業的遠端檔案名中指定的主機名稱之前，嘗試重新連線到位主機識別碼標頭中所指定伺服器名稱的時間長度。 當 BITS 無法連線到 BITS 主機識別碼伺服器時，就會開始計時器。 當還原伺服器的連接時，就會重設計時器。 如果未指定超時期間，用戶端永遠不會還原為遠端檔案名中指定的主機名稱。

</dd> <dt>

<span id="Accept-Encoding"></span><span id="accept-encoding"></span><span id="ACCEPT-ENCODING"></span>接受編碼
</dt> <dd>

識別要在傳送至伺服器的片段上使用的編碼配置。 片段封包會在封包主體中包含編碼的片段。 BITS 伺服器需要 (純文字) 的身分識別編碼。 只有當原因代碼為200或201時，才包含此標頭。

</dd> <dt>

<span id="Content-Length"></span><span id="content-length"></span><span id="CONTENT-LENGTH"></span>內容長度
</dt> <dd>

以回應主體中包含的位元組數目取代長度。 即使回應本文不包含內容，也是必要項。

</dd> <dt>

<span id="BITS-Error-Code"></span><span id="bits-error-code"></span><span id="BITS-ERROR-CODE"></span>BITS-Error-Code
</dt> <dd>

以代表與伺服器端錯誤相關之 HRESULT 值的十六進位數位取代錯誤碼。 只有在原因-程式碼不是200或201時，才包含此標頭。

</dd> <dt>

<span id="BITS-Error-Context"></span><span id="bits-error-context"></span><span id="BITS-ERROR-CONTEXT"></span>BITS-Error-CoNtext
</dt> <dd>

將錯誤內容取代為十六進位數位，代表發生錯誤的內容。 如果伺服器產生錯誤，請指定 [**BG \_ ERROR \_ CONTEXT \_ REMOTE \_ FILE**](/windows/win32/api/bits/ne-bits-bg_error_context) 的十六進位數位 (0x5) 。 否則，請為 **BG \_ 錯誤 \_ 內容 \_ 遠端 \_ 應用程式** 指定十六進位數位 (0x7) 是否由傳遞上傳檔案的應用程式產生錯誤。 只有當原因代碼不是200或201時，才包含此標頭。

</dd> </dl>

## <a name="see-also"></a>另請參閱

<dl> <dt>

[**建立-會話**](create-session.md)
</dt> </dl>

 

 





