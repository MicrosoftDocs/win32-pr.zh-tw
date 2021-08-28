---
title: delete sslcert
description: 刪除 IP 位址和埠的 SSL 伺服器憑證系結和對應的用戶端憑證原則。
ms.assetid: 2adea7a8-f31f-4c02-8279-7d452e36cd9b
keywords:
- 刪除 sslcert HTTP
topic_type:
- apiref
api_name:
- delete sslcert
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a45d811bedfa1d2a228cd29decf2272d85b8ca6de5c1d27656b3e37b8d6b4d4e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119870538"
---
# <a name="delete-sslcert"></a>delete sslcert

刪除 IP 位址和埠的 SSL 伺服器憑證系結和對應的用戶端憑證原則。

``` syntax
delete sslcert [ipport=]IP Address:port
 
```

## <a name="parameters"></a>參數

<dl> <dt>

<span id="_ipport__IP_Address_port"></span><span id="_ipport__ip_address_port"></span><span id="_IPPORT__IP_ADDRESS_PORT"></span>**\[ ipport = \]** _IP 位址：埠_
</dt> <dd>

指定將刪除 SSL 憑證系結的 IPv4 或 IPv6 位址和埠。

</dd> </dl>

## <a name="examples"></a>範例

**delete sslcert ipport=1.1.1.1:443**

**delete sslcert ipport=0.0.0.0:443**

**delete sslcert ipport = \[ ：： \] ：443**

 

 




