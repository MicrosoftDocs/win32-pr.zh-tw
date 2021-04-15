---
description: Asn.1 八進位字串資料類型會編碼成以0x04 標記位元組開頭的 TLV。
ms.assetid: 9d07a6c8-a15f-4030-838c-3063e315684f
title: 八位字串
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ed2a042312a4415ea9554b7519404097287244f5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104469296"
---
# <a name="octet-string"></a><span data-ttu-id="b2d41-103">八位字串</span><span class="sxs-lookup"><span data-stu-id="b2d41-103">OCTET STRING</span></span>

<span data-ttu-id="b2d41-104">Asn.1 **八進位字串** 資料類型會編碼成以 0x04 **標記** 位元組開頭的 TLV。</span><span class="sxs-lookup"><span data-stu-id="b2d41-104">The ASN.1 **OCTET STRING** data type is encoded into a TLV triplet that begins with a **Tag** byte of 0x04.</span></span> <span data-ttu-id="b2d41-105">**八進位字串** 和 [位字串](about-bit-string.md)資料類型非常類似。</span><span class="sxs-lookup"><span data-stu-id="b2d41-105">The **OCTET STRING** and [BIT STRING](about-bit-string.md) data types are very similar.</span></span> <span data-ttu-id="b2d41-106">因此，這兩種類型會以類似的方式進行編碼，但因為 **八位字串** 的尾端位元組不能有未使用的位，所以不能將任何前置位元組新增至內容中。</span><span class="sxs-lookup"><span data-stu-id="b2d41-106">Thus, the two types are encoded in a similar manner except that, because the trailing byte of an **OCTET STRING** cannot have unused bits, no leading bytes must be added to the content.</span></span> <span data-ttu-id="b2d41-107">下列範例是從 [CMC 編碼](cmc-encoded-asn-1.md) 的 asn.1 主題進行調整，顯示憑證範本的名稱如何編碼為位元組陣列。</span><span class="sxs-lookup"><span data-stu-id="b2d41-107">The following example, adapted from the [CMC Encoded ASN.1](cmc-encoded-asn-1.md) topic, shows how the name of a certificate template is encoded as a byte array.</span></span>

``` syntax
30 17                                 ; SEQUENCE (17 Bytes)
|  06 09                              ; OBJECT_ID (9 Bytes)
|  |  2b 06 01 04 01 82 37 14  02     ;   1.3.6.1.4.1.311.20.2
|  04 0a                              ; OCTET_STRING (a Bytes)
|     1e 08 00 55 00 73 00 65  00 72  ;   ...U.s.e.r
```

<span data-ttu-id="b2d41-108">如果位元組陣列包含少於128個位元組，則多位元組的 **長度** 欄位只需要一個位元組來指定內容長度。</span><span class="sxs-lookup"><span data-stu-id="b2d41-108">If the byte array contains fewer than 128 bytes, the **Length** field of the TLV triplet requires only one byte to specify the content length.</span></span> <span data-ttu-id="b2d41-109">如果超過127個位元組，則 [ **長度** ] 欄位中的位7會設定為1，而位6至0則指定用來識別內容長度的其他位元組數目。</span><span class="sxs-lookup"><span data-stu-id="b2d41-109">If it is more than 127 bytes, bit 7 of the **Length** field is set to 1 and bits 6 through 0 specify the number of additional bytes used to identify the content length.</span></span> <span data-ttu-id="b2d41-110">這會顯示在下列範例中，第一行的第二個位元組的高序位位設為1，而位元組表示有尾端 **長度** 的位元組。</span><span class="sxs-lookup"><span data-stu-id="b2d41-110">This is shown in the following example where the high order bit of the second byte on the first line is set to 1 and the byte indicates that there is a trailing **Length** byte.</span></span> <span data-ttu-id="b2d41-111">因此，第三個位元組會指定內容為0x80 位元組的長度。</span><span class="sxs-lookup"><span data-stu-id="b2d41-111">The third byte therefore specifies that the content is 0x80 bytes long.</span></span>

``` syntax
04 81 80                       ; OCTET_STRING (80 Bytes)
   38 10 60 e2 70 69 91 4a     ;   8.`.pi.J
   8b b5 22 57 2a 62 ef de     ;   .."W*b..
   15 7d 59 d6 4e 20 9a 45     ;   .}Y.N .E
   2b e3 fd fc 68 ba af bf     ;   +...h...
   9c 17 b0 8e 6d c4 29 1e     ;   ....m.).
   e3 21 ac bb 5a 8a c9 67     ;   .!..Z..g
   0a d4 45 93 10 c0 26 eb     ;   ..E...&.
   0a 83 c2 b1 40 87 36 f7     ;   ....@.6.
   a0 26 da b9 bb 46 73 88     ;   .&...Fs.
   7a 67 b9 e6 b3 6f ea 59     ;   zg...o.Y
   28 8a d3 92 72 f6 7b 89     ;   (...r.{.
   a0 d8 2d 9e 40 eb 1e bb     ;   ..-.@...
   6e ae f0 5a ed 16 c9 e3     ;   n..Z....
   27 59 37 8f f3 4a 98 60     ;   'Y7..J.`
   f8 fb a7 0a ee 1b 6e 91     ;   ......n.
   95 96 cf 0d 56 ac ab 35     ;   ....V..5
```

## <a name="related-topics"></a><span data-ttu-id="b2d41-112">相關主題</span><span class="sxs-lookup"><span data-stu-id="b2d41-112">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b2d41-113">ASN. 1 類型系統</span><span class="sxs-lookup"><span data-stu-id="b2d41-113">ASN.1 Type System</span></span>](about-asn-1-type-system.md)
</dt> <dt>

[<span data-ttu-id="b2d41-114">以 DER 編碼的 ASN. 1 類型</span><span class="sxs-lookup"><span data-stu-id="b2d41-114">DER Encoding of ASN.1 Types</span></span>](about-der-encoding-of-asn-1-types.md)
</dt> </dl>

 

 



