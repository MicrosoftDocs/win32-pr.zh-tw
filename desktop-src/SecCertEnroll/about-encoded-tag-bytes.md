---
description: TLV 中的標記欄位會識別在電腦之間傳送的資料結構類型。
ms.assetid: 4723cc02-8c48-488e-95b8-c646a99b6aab
title: 編碼的標記位元組
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5a5994f7beea0aba6896e94cb992a1e72eb70914
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104559451"
---
# <a name="encoded-tag-bytes"></a>編碼的標記位元組

TLV 中的 *標記* 欄位會識別在電腦之間傳送的資料結構類型。 例如，整數的標記為0x02，而物件識別碼的標記為0x06。 雖然允許多個位元組，但憑證註冊 API 所使用的資料類型都不需要一個以上的資料類型。 下圖顯示 *標記* 值的明細。 位7和6識別 asn.1 標記類別。 有四個可用的類別，但憑證註冊 API 使用屬於通用類別的資料類型。 Bit 5 會識別編碼形式為基本或已建立。 基本和字串類型是使用基本形式的編碼，並使用結構化的表單來進行編碼。 如需詳細資訊，請參閱 [ASN. 1 類型系統](about-asn-1-type-system.md)。 位4至0包含標記編號。

![der tlv 標記位元組](images/der-tlv-tagbyte.png)

下表列出憑證註冊 API 所支援的資料類型、使用的編碼形式，以及標記值。

| 類型              | ASN. 1 類別 | 編碼形式 | 標籤值                             |
|-------------------|-------------|---------------|---------------------------------------|
| 位字串        | 普遍   | Primitive     | 00000011<br/>  (0x03) <br/> |
| BOOLEAN           | 普遍   | Primitive     | 00000001<br/>  (0x01) <br/> |
| INTEGER           | 普遍   | Primitive     | 00000010<br/>  (0x02) <br/> |
| NULL              | 普遍   | Primitive     | 00000101<br/>  (0x05) <br/> |
| 物件識別碼 | 普遍   | Primitive     | 00000110<br/>  (0x06) <br/> |
| 八位字串      | 普遍   | Primitive     | 00000100<br/>  (0x04) <br/> |
| BMPString         | 普遍   | Primitive     | 00011110<br/>  (0x1E) <br/> |
| IA5String         | 普遍   | Primitive     | 00010110<br/>  (0x16) <br/> |
| PrintableString   | 普遍   | Primitive     | 00010011<br/>  (0x13) <br/> |
| TeletexString     | 普遍   | Primitive     | 00010100<br/>  (0x14) <br/> |
| UTF8String        | 普遍   | Primitive     | 00001100<br/>  (0x0C) <br/> |
| SEQUENCE          | 普遍   | 構建   | 00110000<br/>  (0x30<) <br/> |
| 順序       | 普遍   | 構建   | 00110000<br/>  (0x30<) <br/> |
| SET               | 普遍   | 構建   | 00110001<br/>  (0x31) <br/> |
| 的集合            | 普遍   | 構建   | 00110001<br/>  (0x31) <br/> |



 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[DER 傳送語法](about-der-transfer-syntax.md)
</dt> <dt>

[編碼的長度和值位元組](about-encoded-length-and-value-bytes.md)
</dt> </dl>

 

 




