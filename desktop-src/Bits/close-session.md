---
title: Close-Session
description: 使用 Close-Session 封包來告訴 BITS 伺服器檔案上傳已完成，並結束會話。
ms.assetid: 9d4b658a-8b41-4678-b996-f2174784cdd6
keywords:
- Close-Session 位
topic_type:
- apiref
api_name:
- Close-Session
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b1ae1318a99e690b13f4f0cad03624fb351c359efbcb1be9e105076ce53ceba2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119021196"
---
# <a name="close-session"></a>Close-Session

使用「 **關閉會話** 」封包，告訴 BITS 伺服器檔案上傳已完成，並結束會話。

``` syntax
BITS_POST remote-URL HTTP/1.1
BITS-Packet-Type: Close-Session
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

將此要求封包識別為 Close-Session 封包。

</dd> <dt>

<span id="BITS-Session-Id"></span><span id="bits-session-id"></span><span id="BITS-SESSION-ID"></span>位-會話識別碼
</dt> <dd>

識別伺服器會話的字串 GUID。 將 {guid} 取代為伺服器在 [**建立會話**](ack-for-create-session.md) 回應封包的 Ack 中傳回的會話識別碼。

</dd> </dl>

## <a name="remarks"></a>備註

BITS 伺服器會釋放所有資源，並在接收到此封包時刪除所有暫存檔案。

針對上傳-回復作業，您必須先下載回復，再傳送 **關閉會話**。 否則，回復會遺失。

如果您在上傳所有片段之前傳送此封包，則會刪除上傳檔案;您無法上傳部分檔案。

## <a name="see-also"></a>另請參閱

<dl> <dt>

[**確認是否已關閉會話**](ack-for-close-session.md)
</dt> <dt>

[**取消-會話**](cancel-session.md)
</dt> <dt>

[**建立-會話**](create-session.md)
</dt> </dl>

 

 




