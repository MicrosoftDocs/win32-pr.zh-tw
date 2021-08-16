---
title: Close-Session 的 Ack
description: 使用 Close-Session 封包的 Ack 來確認用戶端的 Close-Session 要求。 伺服器會在釋放與上傳會話相關聯的所有資源之後傳送通知。
ms.assetid: 9d4b658a-8b41-4678-b996-f2174784cdd6
keywords:
- Close-Session BITS 的 Ack
topic_type:
- apiref
api_name:
- Ack for Close-Session
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 289f2cfc2ca9f1e879e0aa592af28d86ae433f6e06d007aa71e00581baba2af5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117835411"
---
# <a name="ack-for-close-session"></a>Close-Session 的 Ack

使用「通知」來確認用戶端的「[**關閉會話**](close-session.md)」要求，以 **取得接近會話** 封包。 伺服器會在釋放與上傳會話相關聯的所有資源之後傳送通知。

``` syntax
reason-code reason-description
BITS-Packet-Type: Ack
BITS-Session-Id: {guid}
Content-Length: length
BITS-Error-Code: error-code
BITS-Error-Context: error-context
```

## <a name="headers"></a>標題

<dl> <dt>

<span id="reason-code"></span><span id="REASON-CODE"></span>原因-代碼
</dt> <dd>

以 HTTP 原因代碼取代 reason 碼。 例如，如果成功，請將 reason 碼設定為200。 如需 HTTP 原因代碼的清單，請參閱 [RFC 2616](https://www.ietf.org/rfc/rfc2616.txt)。

</dd> <dt>

<span id="reason-description"></span><span id="REASON-DESCRIPTION"></span>原因-描述
</dt> <dd>

以與原因代碼相關聯的 HTTP 描述取代 reason 描述。 例如，如果 reason-code 是200，請將 reason 描述設定為 OK。

</dd> <dt>

<span id="BITS-Packet-Type"></span><span id="bits-packet-type"></span><span id="BITS-PACKET-TYPE"></span>BITS-封包類型
</dt> <dd>

將此回應封包識別為 Ack 封包。

</dd> <dt>

<span id="BITS-Session-Id"></span><span id="bits-session-id"></span><span id="BITS-SESSION-ID"></span>位-會話識別碼
</dt> <dd>

識別用戶端會話的字串 GUID。 將 {guid} 取代為用戶端在「 [**關閉會話**](close-session.md) 」要求封包中傳送的會話識別碼。 如果您無法辨識會話識別碼，請將位-錯誤碼標頭設定為 [找不到 BG \_ E \_ 會話] \_ \_ 。

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

如果原因代碼是在500到599的範圍內，則 BITS 用戶端會重新傳送 [**關閉會話**](close-session.md) 封包，除非找不到 BITS-錯誤碼標頭，且值為 BG \_ E \_ 會話找不到 \_ \_ 。 用戶端不會重試，原因代碼為100到499。

## <a name="see-also"></a>另請參閱

<dl> <dt>

[**Ack 以進行取消-會話**](ack-for-cancel-session.md)
</dt> <dt>

[**關閉會話**](close-session.md)
</dt> </dl>

 

 




