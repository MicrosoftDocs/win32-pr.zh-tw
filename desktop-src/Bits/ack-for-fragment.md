---
title: 適用于片段的 Ack
description: 使用片段封包的 Ack 來確認用戶端的片段要求。
ms.assetid: f5466489-2d5e-4850-a39c-37bc4923a7ac
keywords:
- 片段位的 Ack
topic_type:
- apiref
api_name:
- Ack for Fragment
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ecd4b8bf5580a5724c689ced1886051006d34cd3c9ba0561d253f36428178c0a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119702118"
---
# <a name="ack-for-fragment"></a>適用于片段的 Ack

使用片段封包的 **Ack** 來確認用戶端的 [**片段**](fragment.md) 要求。

``` syntax
reason-code reason-description
BITS-Packet-Type: Ack
BITS-Session-Id: {guid}
BITS-Received-Content-Range: range
BITS-Reply-URL: url
Content-Length: length
BITS-Error-Code: error-code
BITS-Error-Context: error-context
```

## <a name="headers"></a>標題

<dl> <dt>

<span id="reason-code"></span><span id="REASON-CODE"></span>原因-代碼
</dt> <dd>

以 HTTP 原因代碼取代 reason 碼。 下錶針對 [**片段**](fragment.md) 要求的回應，顯示一般的原因代碼。 如需 HTTP 原因代碼的清單，請參閱 [RFC 2616](https://www.ietf.org/rfc/rfc2616.txt)。



| 原因代碼    | 描述                                                                                                            |
|----------------|------------------------------------------------------------------------------------------------------------------------|
| 200<br/> | 正常。 要求成功。<br/>                                                                             |
| 416<br/> | 範圍-不] 正確。 用戶端傳送的片段的範圍與上一個片段不連續。<br/> |



 

</dd> <dt>

<span id="reason-description"></span><span id="REASON-DESCRIPTION"></span>原因-描述
</dt> <dd>

以與原因代碼相關聯的 HTTP 描述取代 reason 描述。 例如，如果 reason-code 是200，請將 reason 描述設定為 OK。

</dd> <dt>

<span id="BITS-Packet-Type"></span><span id="bits-packet-type"></span><span id="BITS-PACKET-TYPE"></span>BITS-封包類型
</dt> <dd>

將此回應封包識別為 Ack 封包。

</dd> <dt>

<span id="BITS-Received-Content-Range"></span><span id="bits-received-content-range"></span><span id="BITS-RECEIVED-CONTENT-RANGE"></span>位-已接收-內容約制
</dt> <dd>

伺服器預期用戶端傳送的下一個位元組以零為基底的位移。 例如，如果片段包含範圍 128 212，則會將範圍設定為213。

</dd> <dt>

<span id="BITS-Session-Id"></span><span id="bits-session-id"></span><span id="BITS-SESSION-ID"></span>位-會話識別碼
</dt> <dd>

識別用戶端會話的字串 GUID。 將 {guid} 取代為用戶端在 [**片段**](fragment.md) 要求封包中傳送的會話識別碼。 如果您無法辨識會話識別碼，請將位-錯誤碼標頭設定為 [找不到 BG \_ E \_ 會話] \_ \_ 。

</dd> <dt>

<span id="BITS-Reply-URL"></span><span id="bits-reply-url"></span><span id="BITS-REPLY-URL"></span>位-回復-URL
</dt> <dd>

包含上傳-回復作業之回復資料的 URL。 上傳完成之後，在最終片段回應中包含此標頭，而且您會收到來自伺服器應用程式的回應（如果有的話）。

使用片段要求中的內容約制標頭來判斷上傳是否完成。 如果範圍值的結束位移等於總計長度值減一，則上傳已完成。

BITS 伺服器會在判斷上傳完成之後，將上傳檔案張貼至伺服器應用程式。 伺服器應用程式會處理檔案並產生回復。 BITS 伺服器會將位-回復 URL 的值，從伺服器應用程式設定為回復檔案的 URL。

</dd> <dt>

<span id="Content-Length"></span><span id="content-length"></span><span id="CONTENT-LENGTH"></span>內容長度
</dt> <dd>

以回應主體中包含的位元組數目取代長度。 即使回應本文不包含內容，也需要內容長度。

</dd> <dt>

<span id="BITS-Error-Code"></span><span id="bits-error-code"></span><span id="BITS-ERROR-CODE"></span>BITS-Error-Code
</dt> <dd>

以代表與伺服器端錯誤相關之 HRESULT 值的十六進位數位取代錯誤碼。 如果原因-代碼不是200或201，則只包含此標頭。

</dd> <dt>

<span id="BITS-Error-Context"></span><span id="bits-error-context"></span><span id="BITS-ERROR-CONTEXT"></span>BITS-Error-CoNtext
</dt> <dd>

將錯誤內容取代為十六進位數位，代表發生錯誤的內容。 如果伺服器產生錯誤，請指定 [**BG \_ ERROR \_ CONTEXT \_ REMOTE \_ FILE**](/windows/win32/api/bits/ne-bits-bg_error_context) 的十六進位數位 (0x5) 。 否則，請為 **BG \_ 錯誤 \_ 內容 \_ 遠端 \_ 應用程式** 指定十六進位數位 (0x7) 是否由傳遞上傳檔案的應用程式產生錯誤。 只有當原因代碼不是200或201時，才包含此標頭。

</dd> </dl>

## <a name="remarks"></a>備註

如果會話適用于上傳-回復作業，則可能會在用戶端收到片段回應的最終 **認可** 之前發生延遲。 延遲的長度取決於伺服器應用程式 (應用程式用來將上傳檔案張貼) 用來產生回復的時間量。

## <a name="see-also"></a>另請參閱

<dl> <dt>

[**建立-會話**](create-session.md)
</dt> <dt>

[**片段**](fragment.md)
</dt> </dl>

 

 





