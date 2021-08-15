---
title: Ping
description: 使用 Ping 封包來建立連接，並與伺服器協商安全性。
ms.assetid: 10b01fe8-d1a3-4a3b-ac35-e3557d3ef4ee
keywords:
- Ping 位
topic_type:
- apiref
api_name:
- Ping
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 479e03e6e18c0ec7421bd225744c5181029fc2b2e220f35c7bae7a3b02d42b07
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120004888"
---
# <a name="ping"></a>Ping

使用 **Ping** 封包來建立連接，並與伺服器協商安全性。

``` syntax
BITS_POST remote-URL HTTP/1.1
BITS-Packet-Type: Ping
```

## <a name="headers"></a>標題

<dl> <dt>

<span id="BITS_POST"></span><span id="bits_post"></span>BITS \_ POST
</dt> <dd>

識別此封包到 BITS 伺服器的位特定動詞。

將遠端 URL 取代為絕對或相對 URI。 通常，將遠端 URL 取代為作業的遠端檔案名。

</dd> <dt>

<span id="BITS-Packet-Type"></span><span id="bits-packet-type"></span><span id="BITS-PACKET-TYPE"></span>BITS-封包類型
</dt> <dd>

將此要求封包識別為 Ping 封包。

</dd> </dl>

## <a name="remarks"></a>備註

**Ping** 封包是選擇性的。 您可以使用建立 [**會話**](create-session.md)封包來建立連線和協商安全性，而不是傳送 **Ping** 封包。 不過，針對此目的使用 **Ping** 封包較有效率。

## <a name="see-also"></a>另請參閱

<dl> <dt>

[**Ping 的 Ack**](ack-for-ping.md)
</dt> <dt>

[**建立-會話**](create-session.md)
</dt> </dl>

 

 




