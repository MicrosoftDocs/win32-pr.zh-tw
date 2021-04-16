---
description: 位字串資料類型會編碼成以0x03 的標記位元組開頭的 TLV 三位元組。
ms.assetid: 7464dd20-5e79-4ca1-a6ae-9b706e9cb925
title: 位字串
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 115ead46663b94d6db2d089f1fae2fd8c40a2ac7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104563155"
---
# <a name="bit-string"></a>位字串

**位字串** 資料類型會編碼成以0X03 的 **標記** 位元組開頭的 TLV 三位元組。 多型的 [ **值** ] 欄位包含前置位元組，可指定最後一個位元組內容中未使用的位數。 在下列範例中，[ **長度** ] 欄位設定為 [0x03]，因為接下來有三個內容位元組，而 [ **值** ] 欄位的前置位元組會設定為 [0x04]，因為最後一個內容位元組中有四個未使用的位。 每個未使用的位都會以字母 x 表示。

![位字串資料類型的 der 編碼](images/der-tlv-bitstring.png)

下列範例（取自 [pkcs \# 10 編碼](pkcs--10-encoded-asn-1.md) 的 asn.1 主題）會顯示範例 PKCS \# 10 憑證要求的編碼簽章。 第一個位元組包含 **位字串** 資料類型（0x03）的 **標記** 值。 第二個和第三個位元組包含位元組陣列的長度。 第二個位元組的位7設定為1，因為內容超過127個位元組。 第二個位元組的位0到6指定尾端 **長度** 的位元組數，在此案例中為1。 第三個位元組會指定 content bytes （0x81）的數目。 第四個位元組0x00 指定存在於最後一個內容位元組中的未使用位數目。 請注意，簽章會以位元組由大到小的順序進行編碼。

``` syntax
0299:    03 81 81           ; BIT_STRING (81 Bytes)
029c:       00
029d:       47 eb 99 5a df 9e 70 0d  fb a7 31 32 c1 5f 5c 24
02ad:       c2 e0 bf c6 24 af 15 66  0e b8 6a 2e ab 2b c4 97
02bd:       1f e3 cb dc 63 a5 25 ec  c7 b4 28 61 66 36 a1 31
02cd:       1b bf dd d0 fc bf 17 94  90 1d e5 5e c7 11 5e c9
02dd:       55 9f eb a3 3e 14 c7 99  a6 cb ba a1 46 0f 39 d4
02ed:       44 c4 c8 4b 76 0e 20 5d  6d a9 34 9e d4 d5 87 42
02fd:       eb 24 26 51 14 90 b4 0f  06 5e 52 88 32 7a 95 20
030d:       a0 fd f7 e5 7d 60 dd 72  68 9b f5 7b 05 8f 6d 1e
```

## <a name="related-topics"></a>相關主題

<dl> <dt>

[ASN. 1 類型系統](about-asn-1-type-system.md)
</dt> <dt>

[以 DER 編碼的 ASN. 1 類型](about-der-encoding-of-asn-1-types.md)
</dt> <dt>

[編碼的長度和值位元組](about-encoded-length-and-value-bytes.md)
</dt> </dl>

 

 



