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
ms.openlocfilehash: e7672df5eee1634c41ff153435edcbecc58c2595
ms.sourcegitcommit: 476861130ea63675206d1f06e517059705b930ed
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 11/06/2019
ms.locfileid: "103678868"
---
# <a name="delete-sslcert"></a>delete sslcert

刪除 IP 位址和埠的 SSL 伺服器憑證系結和對應的用戶端憑證原則。

``` syntax
delete sslcert [ipport=]IP Address:port
 
```

## <a name="parameters"></a>參數

<dl> <dt>

<span id="_ipport__IP_Address_port"></span><span id="_ipport__ip_address_port"></span><span id="_IPPORT__IP_ADDRESS_PORT"></span>**\[ipport = \] * * * IP 位址：埠*
</dt> <dd>

指定將刪除 SSL 憑證系結的 IPv4 或 IPv6 位址和埠。

</dd> </dl>

## <a name="examples"></a>範例

**delete sslcert ipport=1.1.1.1:443**

**delete sslcert ipport=0.0.0.0:443**

**delete sslcert ipport = \[ ：： \] ：443**

 

 




