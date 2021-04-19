---
title: Cancel-Session
description: 使用 Cancel-Session 封包來終止與 BITS 伺服器的上傳會話。
ms.assetid: 670d061e-ab73-4aa8-85ba-2c9693794235
keywords:
- Cancel-Session 位
topic_type:
- apiref
api_name:
- Cancel-Session
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 017097bea656309aabf3d773f34152805fd6a579
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/25/2019
ms.locfileid: "106967861"
---
# <a name="cancel-session"></a>Cancel-Session

使用 **取消會話** 封包來終止與 BITS 伺服器的上傳會話。

``` syntax
BITS_POST remote-URL HTTP/1.1
BITS-Packet-Type: Cancel-Session
BITS-Session-Id: {guid}
```

## <a name="headers"></a>標題

<dl> <dt>

<span id="BITS_POST"></span><span id="bits_post"></span>BITS \_ POST
</dt> <dd>

識別此封包到 BITS 伺服器的位特定動詞。

將遠端 URL 取代為絕對或相對 URI。 通常，將遠端 URL 取代為作業的遠端檔案名。 如需網路負載平衡的考慮，請參閱 [**建立會話**](create-session.md) 封包中的 BITS 主機識別碼標頭。

</dd> <dt>

<span id="BITS-Packet-Type"></span><span id="bits-packet-type"></span><span id="BITS-PACKET-TYPE"></span>BITS-封包類型
</dt> <dd>

將此要求封包識別為 Cancel-Session 封包。

</dd> <dt>

<span id="BITS-Session-Id"></span><span id="bits-session-id"></span><span id="BITS-SESSION-ID"></span>位-會話識別碼
</dt> <dd>

識別伺服器會話的字串 GUID。 將 {guid} 取代為伺服器在 [**建立會話**](ack-for-create-session.md) 回應封包的 Ack 中傳回的會話識別碼。

</dd> </dl>

## <a name="remarks"></a>備註

此封包會取消上傳工作（如果在傳送最後一個片段之前傳送）。 Cancel-Session 對於已傳送最後一個片段的檔案沒有任何作用。 當 BITS 伺服器收到最後一個片段時，它會將檔案寫入其最終目的地，而在上傳-回復的情況下，會將檔案張貼至伺服器應用程式。 在上傳-回復案例中，Cancel-Session 封包會取消上傳-回復作業的回復部分。

BITS 伺服器會釋放所有資源，並在接收到此封包時刪除所有暫存檔案。

BITS 用戶端會在使用者取消作業時傳送此封包。

## <a name="see-also"></a>另請參閱

<dl> <dt>

[**Create-Session 的 Ack**](ack-for-create-session.md)
</dt> <dt>

[**關閉會話**](close-session.md)
</dt> </dl>

 

 




