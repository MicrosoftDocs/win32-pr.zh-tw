---
description: UTF8String 資料類型會編碼成以0x0C 的標記位元組開頭的 TLV 三位元組。
ms.assetid: e30737d3-8294-48d8-9e42-f21918acc73c
title: UTF8String
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 26048a46689d27b68e8cacfa4af13b37cde4d613
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103849242"
---
# <a name="utf8string"></a>UTF8String

**UTF8String** 資料類型會編碼成以0X0C 的 **標記** 位元組開頭的 TLV 三位元組。 下列範例（來自 [CMC 編碼](cmc-encoded-asn-1.md) 的 asn.1 主題）會顯示 **ClientId** 屬性如何編碼為整數和三個 **UTF8String** 類型。 屬性的物件識別碼是1.3.6.1.4.1.311.21.20。 您可以使用 [**IX509AttributeClientId**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509attributeclientid) 介面指定的資訊包括用戶端識別碼、網域名稱系統 (DNS) 電腦名稱稱、安全性帳戶管理員 (SAM) 使用者名稱，以及建立憑證要求的應用程式名稱。

``` syntax
06 09                                ; OBJECT_ID (9 Bytes)
|  2b 06 01 04 01 82 37 15  14       ;   1.3.6.1.4.1.311.21.20 
31 4a                                ; SET (4a Bytes)
   30 48                             ; SEQUENCE (48 Bytes)
      02 01                          ; INTEGER (1 Bytes)
      |  09
      0c 23                          ; UTF8_STRING (23 Bytes)
      |  76 69 63 68 33 64 2e 6a     ;   vich3d.j
      |  64 6f 6d 63 73 63 2e 6e     ;   domcsc.n
      |  74 74 65 73 74 2e 6d 69     ;   ttest.mi
      |  63 72 6f 73 6f 66 74 2e     ;   crosoft.
      |  63 6f 6d                    ;   com
      0c 15                          ; UTF8_STRING (15 Bytes)
      |  4a 44 4f 4d 43 53 43 5c     ;   JDOMCSC\
      |  61 64 6d 69 6e 69 73 74     ;   administ
      |  72 61 74 6f 72              ;   rator
      0c 07                          ; UTF8_STRING (7 Bytes)
         63 65 72 74 72 65 71        ;   certreq
```

如果字串包含少於128個位元組，則多位元組的 **長度** 欄位只需要一個位元組來指定內容長度。 如果字串超過127個位元組，則 [ **長度** ] 欄位中的位7會設定為1，而位6至0則指定用來識別內容長度的其他位元組數目。 如需詳細資訊，請參閱 [編碼的長度和值位元組](about-encoded-length-and-value-bytes.md)。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[ASN. 1 類型系統](about-asn-1-type-system.md)
</dt> <dt>

[以 DER 編碼的 ASN. 1 類型](about-der-encoding-of-asn-1-types.md)
</dt> </dl>

 

 



