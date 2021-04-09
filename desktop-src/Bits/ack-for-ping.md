---
title: Ping 的 Ack
description: 使用 Ping 封包的 Ack 來確認用戶端的 Ping 要求。
ms.assetid: 2e288564-d06f-4b45-b0c0-7aab1897da40
keywords:
- Ping 位的 Ack
topic_type:
- apiref
api_name:
- Ack for Ping
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f5a3ca765c8bd7758f19abe396ad0449a5895d8e
ms.sourcegitcommit: 73417d55867c804274a55abe5ca71bcba7006119
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/20/2020
ms.locfileid: "103933704"
---
# <a name="ack-for-ping"></a>Ping 的 Ack

使用 Ping 封包的 **Ack** 來確認用戶端的 [**ping**](ping.md) 要求。

``` syntax
reason-code reason-description
BITS-Packet-Type: Ack
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

[**坪**](ping.md)
</dt> </dl>

 

 




