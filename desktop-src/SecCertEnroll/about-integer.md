---
description: 整數值會編碼成以0x02 的標記值開頭的 TLV 三個。
ms.assetid: a6fed62f-af59-488c-a690-be8c3413086f
title: '整數 (憑證註冊 API) '
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1f0e8ed162d4cf4b2ac4909baf1cd7b5e94ddea6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104319151"
---
# <a name="integer-certificate-enrollment-api"></a>整數 (憑證註冊 API) 

整數值會編碼成以0x02 的 **標記** 值開頭的 TLV 三個。 如果是正數，則會包含編碼的整數 **值** 欄位，如果是負數，則會包含其二的補數。 如果整數是正數，但高序位位設為1，則會將前置0x00 新增至內容，以指出該數位不是負數。 例如，0x8F (10001111) 的高序位位元組為1。 因此，會將前置零位元組新增至內容，如下圖所示。

![以 der 編碼的 boolean 資料類型](images/der-tlv-integer.png)

如果整數包含少於128個位元組，則 [ *長度* ] 欄位只需要一個位元組來指定內容長度。 如果整數超過127個位元組，則 [ *長度* ] 欄位中的位7設定為1，而位6至0則指定用來識別內容長度的其他位元組數目。 如需詳細資訊，請參閱 [編碼的長度和值位元組](about-encoded-length-and-value-bytes.md)。

下列範例（來自 [PKCS \# 10 編碼](pkcs--10-encoded-asn-1.md)的 asn.1）會顯示128位元組公開金鑰的編碼方式。 第一個位元組包含 **整數** 資料類型的 **標記** 值，0x02。 第二個和第三個位元組包含 **長度** 值。 第二個位元組的位7設定為1，因為內容超過127個位元組。 第二個位元組的位0到6會指定所需的尾端位元組數（在此案例中為1），以精確指定內容長度。 第三個位元組會指定 content bytes （0x81）的數目。 第四個位元組0x00 會新增至內容中，以指出即使前置內容位元組 (0x8F) 的正負號設定為1，整數確實是正值。

``` syntax
02 81 81          ; INTEGER (81 Bytes)
|  00
|  8f e2 41 2a 08 e8 51 a8  8c b3 e8 53 e7 d5 49 50
|  b3 27 8a 2b cb ea b5 42  73 ea 02 57 cc 65 33 ee
|  88 20 61 a1 17 56 c1 24  18 e3 a8 08 d3 be d9 31
|  f3 37 0b 94 b8 cc 43 08  0b 70 24 f7 9c b1 8d 5d
|  d6 6d 82 d0 54 09 84 f8  9f 97 01 75 05 9c 89 d4
|  d5 c9 1e c9 13 d7 2a 6b  30 91 19 d6 d4 42 e0 c4
|  9d 7c 92 71 e1 b2 2f 5c  8d ee f0 f1 17 1e d2 5f
|  31 5b b1 9c bc 20 55 bf  3a 37 42 45 75 dc 90 65
```

下列範例顯示如何編碼整數值0x03。 **標記** 位元組包含0x02，而 **長度** 位元組則指定一個位元組的內容。

``` syntax
02 01             ; INTEGER (1 Bytes)
|  03
```

## <a name="related-topics"></a>相關主題

<dl> <dt>

[ASN. 1 類型系統](about-asn-1-type-system.md)
</dt> <dt>

[以 DER 編碼的 ASN. 1 類型](about-der-encoding-of-asn-1-types.md)
</dt> </dl>

 

 



