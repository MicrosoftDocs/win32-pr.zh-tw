---
description: PrintableString 資料類型會編碼成以0x13 的標記位元組開頭的 TLV 三位元組。
ms.assetid: 998fef66-7a24-462f-96f2-92c739bbefa2
title: PrintableString
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 72ebc95f1a58e8d7beb4a1d3bbb037788252349a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103849244"
---
# <a name="printablestring"></a>PrintableString

**PrintableString** 資料類型會編碼成以0X13 的 **標記** 位元組開頭的 TLV 三位元組。 下列範例從 [PKCS \# 10 編碼的 ASN. 1](pkcs--10-encoded-asn-1.md) 主題，顯示如何將 TestCN 的使用者一般名稱編碼為 **PrintableString** 類型。 一般名稱的物件識別碼是2.5.4.3。

``` syntax
06 03                   ; OBJECT_ID (3 Bytes)
|  55 04 03             ;   2.5.4.3 Common Name (CN)
13 06                   ; PRINTABLE_STRING (6 Bytes)
   54 65 73 74 43 4e    ;   TestCN
```

如果字串包含少於128個位元組，則多位元組的 **長度** 欄位只需要一個位元組來指定內容長度。 如果字串超過127個位元組，則 [ **長度** ] 欄位中的位7會設定為1，而位6至0則指定用來識別內容長度的其他位元組數目。 如需詳細資訊，請參閱 [編碼的長度和值位元組](about-encoded-length-and-value-bytes.md)。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[ASN. 1 類型系統](about-asn-1-type-system.md)
</dt> <dt>

[以 DER 編碼的 ASN. 1 類型](about-der-encoding-of-asn-1-types.md)
</dt> </dl>

 

 



