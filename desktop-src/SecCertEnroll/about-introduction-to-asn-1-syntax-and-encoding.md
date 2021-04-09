---
description: 憑證註冊 API 使用抽象語法標記法 (一)  (asn.1) 來定義、編碼和解碼在用戶端電腦和憑證授權單位單位之間傳輸的憑證要求和憑證。
ms.assetid: 970a246f-a4c3-489b-b6a4-7d3103f388cf
title: ASN. 1 語法和編碼簡介
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a4fe15d2fb8fba4af25b9da7c249fec3a92630e6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103849247"
---
# <a name="introduction-to-asn1-syntax-and-encoding"></a>ASN. 1 語法和編碼簡介

憑證註冊 API 使用抽象語法標記法 (一)  (asn.1) 來定義、編碼和解碼在用戶端電腦和憑證授權單位單位之間傳輸的憑證要求和憑證。 Asn.1 可以概念分為一組語法規則和一組編碼規則，如下列範例所示。

## <a name="asn1-syntax-example"></a>ASN. 1 語法範例

憑證要求包含了提出要求之實體的名稱，或提出要求的機構名稱。 名稱是 X. 500 相對辨別名稱 (RDNs) 的序列。 順序中的每個 RDN 都包含物件識別碼 (OID) 和值。 下列範例顯示的是主體名稱的 asn.1 語法。

``` syntax
---------------------------------------------------------------------
-- Subject name
---------------------------------------------------------------------
Name ::= SEQUENCE OF RelativeDistinguishedName

RelativeDistinguishedName ::= SET OF AttributeTypeValue

AttributeTypeValue ::= SEQUENCE 
{
   type               OBJECT IDENTIFIER,
   value              ANY 
}
```

## <a name="asn1-encoding-example"></a>ASN. 1 編碼範例

憑證註冊 API 會使用 [*可辨別編碼規則*](/windows/desktop/SecGloss/d-gly) (DER) 來編碼先前的主體名稱。 DER 要求名稱中的每個專案都是以每個的 TLV 表示，其中 T 包含 asn.1 類型的標記編號、L 包含長度，而 V 則包含相關聯的值。 下列範例顯示如何編碼主體名稱 TestCN. TestOrg。

``` syntax
1.     30 23            ; SEQUENCE (23 Bytes)
2.     |  |  31 0f            ; SET (f Bytes)
3.     |  |  |  30 0d            ; SEQUENCE (d Bytes)
4.     |  |  |     06 03         ; OBJECT_ID (3 Bytes)
5.     |  |  |     |  55 04 03
6.     |  |  |     |     ; 2.5.4.3 Common Name (CN)
7.     |  |  |     13 06         ; PRINTABLE_STRING (6 Bytes)
8.     |  |  |        54 65 73 74 43 4e                    ; TestCN
9.     |  |  |           ; "TestCN"
10.    |  |  31 10            ; SET (10 Bytes)
11.    |  |     30 0e            ; SEQUENCE (e Bytes)
12.    |  |        06 03         ; OBJECT_ID (3 Bytes)
13.    |  |        |  55 04 0a
14.    |  |        |     ; 2.5.4.10 Organization (O)
15.    |  |        13 07         ; PRINTABLE_STRING (7 Bytes)
16.    |  |           54 65 73 74 4f 72 67                 ; TestOrg
17.    |  |              ; "TestOrg"
```

請注意下列幾點：

-   第1行：<dl> 名稱是一系列的相對辨別名稱。  
    **序列** 類型的標記編號為0x30<。  
    TestCN 的主體名稱 TestOrg 需要 35 (0x23) 個位元組。  
    </dl>
-   Line 2:<dl> 一般名稱 TestCN 是一組 **AttributeTypeValue** 結構。  
    **集合** 的標記編號為0x31。  
    </dl>
-   第3行：<dl> **AttributeTypeValue** 結構是一種序列。  
    **序列** 類型的標記編號為0x30<。  
    結構需要 13 (0xD) 個位元組。  
    </dl>
-   第4到6行：<dl> 一般名稱 (OID) 的物件識別碼是2.5.4.3。  
    OID 是三個位元組的 **物件 \_ 識別碼** 型別。  
    **物件 \_ 識別碼** 類型的標記編號為0x06。  
    </dl>
-   第7到第9行：<dl> 一般名稱 TestCN 是一個字串值。  
    字串是6個位元組的 **可列印 \_ 字串** 類型。  
    **可列印 \_ 字串** 類型的標記編號為0x13。  
    </dl>

## <a name="related-topics"></a>相關主題

<dl> <dt>

[ASN. 1 類型系統](about-asn-1-type-system.md)
</dt> <dt>

[憑證要求編碼](about-certificate-request-encoding.md)
</dt> <dt>

[以 DER 編碼的 ASN. 1 類型](about-der-encoding-of-asn-1-types.md)
</dt> <dt>

[可辨別編碼規則](distinguished-encoding-rules.md)
</dt> </dl>

 

 
