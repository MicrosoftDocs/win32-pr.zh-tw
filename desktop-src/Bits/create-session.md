---
title: Create-Session
description: 使用 Create-Session 封包向 BITS 伺服器要求上傳會話。
ms.assetid: eeb8ff83-2a7f-4fef-9df7-8c12febfcf36
keywords:
- Create-Session 位
topic_type:
- apiref
api_name:
- Create-Session
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 639db08c5a29b09f5c32d7b0243de66f2c4dced001a1ff2afa7e74837c8d67e4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119021186"
---
# <a name="create-session"></a>Create-Session

使用 **Create-Session** 封包要求 BITS 伺服器的上傳會話。

``` syntax
BITS_POST remote-URL HTTP/1.1
BITS-Packet-Type: Create-Session
BITS-Supported-Protocols: {guid1} ... {guidN}
```

## <a name="headers"></a>標題

<dl> <dt>

<span id="BITS_POST"></span><span id="bits_post"></span>BITS \_ POST
</dt> <dd>

識別此封包到 BITS 伺服器的位特定動詞。

將遠端 URL 取代為絕對或相對 URI。 通常，將遠端 URL 取代為作業的遠端檔案名。 如需網路負載平衡的考慮，請參閱 BITS-主機-識別碼標頭。

</dd> <dt>

<span id="BITS-Packet-Type"></span><span id="bits-packet-type"></span><span id="BITS-PACKET-TYPE"></span>BITS-封包類型
</dt> <dd>

將此要求封包識別為 Create-Session 封包。

</dd> <dt>

<span id="BITS-Supported-Protocols"></span><span id="bits-supported-protocols"></span><span id="BITS-SUPPORTED-PROTOCOLS"></span>BITS-支援的通訊協定
</dt> <dd>

用戶端支援的通訊協定清單（以空格分隔）。 使用字串 Guid 來識別通訊協定。 依喜好設定順序指定清單，從最高到最低。 下表列出 BITS 用戶端支援的通訊協定。 取代 {guid1} .。。具有清單中一或多個字串 Guid 的 {guidN}。



| 通訊協定                                          | 描述                         |
|---------------------------------------------------|-------------------------------------|
| {7df0354d-249b-430f-820d-3d2a9bef4931}<br/> | BITS 1.5 Upload 通訊協定<br/> |



 

</dd> </dl>

## <a name="remarks"></a>備註

傳送 Create-Session 封包之前，您應該先傳送 [**Ping**](ping.md) 封包來建立 HTTP 連線。 Create-Session 封包也可以建立連接;不過，Create-Session 封包的效率較低。

伺服器會從用戶端在 BITS 支援的通訊協定標頭中提供的清單中選取想要使用的通訊協定。 伺服器會在 [**Create-Session**](ack-for-create-session.md) response 封包的 Ack BITS-Protocol 標頭中傳回選取的通訊協定。

用戶端預期伺服器會傳回 [**Create Session**](ack-for-create-session.md) response 封包的 Ack。 如果伺服器可以建立會話，用戶端會使用 [**片段**](fragment.md) 要求封包，將檔案範圍傳送至伺服器。

## <a name="see-also"></a>另請參閱

<dl> <dt>

[**Create-Session 的 Ack**](ack-for-create-session.md)
</dt> <dt>

[**片段**](fragment.md)
</dt> <dt>

[**坪**](ping.md)
</dt> </dl>

 

 





