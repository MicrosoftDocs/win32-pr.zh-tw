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
# <a name="delete-sslcert"></a><span data-ttu-id="4f018-104">delete sslcert</span><span class="sxs-lookup"><span data-stu-id="4f018-104">delete sslcert</span></span>

<span data-ttu-id="4f018-105">刪除 IP 位址和埠的 SSL 伺服器憑證系結和對應的用戶端憑證原則。</span><span class="sxs-lookup"><span data-stu-id="4f018-105">Deletes SSL server certificate bindings and the corresponding client certificate policies for an IP address and port.</span></span>

``` syntax
delete sslcert [ipport=]IP Address:port
 
```

## <a name="parameters"></a><span data-ttu-id="4f018-106">參數</span><span class="sxs-lookup"><span data-stu-id="4f018-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4f018-107"><span id="_ipport__IP_Address_port"></span><span id="_ipport__ip_address_port"></span><span id="_IPPORT__IP_ADDRESS_PORT"></span>\**\[ipport = \] \* \* \* IP 位址：埠*</span><span class="sxs-lookup"><span data-stu-id="4f018-107"><span id="_ipport__IP_Address_port"></span><span id="_ipport__ip_address_port"></span><span id="_IPPORT__IP_ADDRESS_PORT"></span>\**\[ipport=\]\*\*\*IP Address:port*</span></span>
</dt> <dd>

<span data-ttu-id="4f018-108">指定將刪除 SSL 憑證系結的 IPv4 或 IPv6 位址和埠。</span><span class="sxs-lookup"><span data-stu-id="4f018-108">Specifies the IPv4 or IPv6 address and port for which the SSL certificate bindings will be deleted.</span></span>

</dd> </dl>

## <a name="examples"></a><span data-ttu-id="4f018-109">範例</span><span class="sxs-lookup"><span data-stu-id="4f018-109">Examples</span></span>

<span data-ttu-id="4f018-110">**delete sslcert ipport=1.1.1.1:443**</span><span class="sxs-lookup"><span data-stu-id="4f018-110">**delete sslcert ipport=1.1.1.1:443**</span></span>

<span data-ttu-id="4f018-111">**delete sslcert ipport=0.0.0.0:443**</span><span class="sxs-lookup"><span data-stu-id="4f018-111">**delete sslcert ipport=0.0.0.0:443**</span></span>

<span data-ttu-id="4f018-112">**delete sslcert ipport = \[ ：： \] ：443**</span><span class="sxs-lookup"><span data-stu-id="4f018-112">**delete sslcert ipport=\[::\]:443**</span></span>

 

 




