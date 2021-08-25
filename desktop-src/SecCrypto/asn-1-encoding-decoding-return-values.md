---
description: 下表包含執行抽象語法標記法 (一)  (asn.1) 編碼或解碼的函式可能會傳回的傳回值。
ms.assetid: cb1f34dd-dab4-4ffb-a73b-79a214290509
title: ASN. 1 編碼/解碼傳回值
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 61c48bc5bc122f322650c7913ea9d1978d5113da31fa650a23e8f439555d7ed0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119880098"
---
# <a name="asn1-encodingdecoding-return-values"></a>ASN. 1 編碼/解碼傳回值

下表包含執行 [*抽象語法標記法 (一)*](../secgloss/a-gly.md) (asn.1) 編碼或解碼的函式可能會傳回的傳回值。



| 定義的常數           | 簡訊                                      | 十六進位值 |
|----------------------------|---------------------------------------------------|-------------------|
| CRYPT \_ E \_ ASN1 \_ 錯誤      | ASN. 1 憑證編碼/解碼傳回值基底 | 0x80093100        |
| CRYPT \_ E \_ ASN1 \_ INTERNAL   | ASN. 1 內部編碼或解碼錯誤             | 0x80093101        |
| CRYPT \_ E \_ ASN1 \_ EOD        | ASN. 1 非預期的資料結尾                      | 0x80093102        |
| CRYPT \_ E \_ ASN1 \_ 已損毀    | ASN. 1 損毀的資料                              | 0x80093103        |
| CRYPT \_ E \_ ASN1 \_ 大型      | ASN. 1 值太大                             | 0x80093104        |
| CRYPT \_ E \_ ASN1 \_ 條件約束 | 違反了 asn.1 條件約束                         | 0x80093105        |
| CRYPT \_ E \_ ASN1 \_ MEMORY     | ASN. 1 記憶體不足                               | 0x80093106        |
| CRYPT \_ E \_ ASN1 \_ 溢位   | Asn.1 緩衝區溢位                             | 0x80093107        |
| CRYPT \_ E \_ ASN1 \_ BADPDU     | 此 PDU 不支援 asn.1 函數         | 0x80093108        |
| CRYPT \_ E \_ ASN1 \_ BADARGS    | Asn.1 錯誤引數給函式呼叫              | 0x80093109        |
| CRYPT \_ E \_ ASN1 \_ BADREAL    | Asn.1 不正確的實值                              | 0x8009310A        |
| CRYPT \_ E \_ ASN1 \_ BADTAG     | Asn.1 符合錯誤的標記值                           | 0x8009310B        |
| CRYPT \_ E \_ ASN1 \_ CHOICE     | ASN. 1 不正確的選擇值                            | 0x8009310C        |
| CRYPT \_ E \_ ASN1 \_ RULE       | ASN. 1 錯誤編碼規則                           | 0x8009310D        |
| CRYPT \_ E \_ ASN1 \_ UTF8       | Asn.1 不正確的 Unicode (UTF8)                           | 0x8009310E        |
| CRYPT \_ E \_ ASN1 \_ PDU \_ 類型  | Asn.1 錯誤的 PDU 類型                                | 0x80093133        |
| CRYPT \_ E \_ ASN1 \_ NYI        | Asn.1 尚未實行                         | 0x80093134        |
| CRYPT \_ E \_ ASN1 \_ EXTENDED   | ASN. 1 略過未知的延伸模組                  | 0x80093201        |
| CRYPT \_ E \_ ASN1 \_ NOEOD      | 需要 asn.1 資料結尾                        | 0x80093202        |



 

 

 
