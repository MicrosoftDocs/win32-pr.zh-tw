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
# <a name="printablestring"></a><span data-ttu-id="45e9a-103">PrintableString</span><span class="sxs-lookup"><span data-stu-id="45e9a-103">PrintableString</span></span>

<span data-ttu-id="45e9a-104">**PrintableString** 資料類型會編碼成以0X13 的 **標記** 位元組開頭的 TLV 三位元組。</span><span class="sxs-lookup"><span data-stu-id="45e9a-104">The ASN.1 **PrintableString** data type is encoded into a TLV triplet that begins with a **Tag** byte of 0x13.</span></span> <span data-ttu-id="45e9a-105">下列範例從 [PKCS \# 10 編碼的 ASN. 1](pkcs--10-encoded-asn-1.md) 主題，顯示如何將 TestCN 的使用者一般名稱編碼為 **PrintableString** 類型。</span><span class="sxs-lookup"><span data-stu-id="45e9a-105">The following example, from the [PKCS \#10 Encoded ASN.1](pkcs--10-encoded-asn-1.md) topic, shows how a user common name of TestCN is encoded as a **PrintableString** type.</span></span> <span data-ttu-id="45e9a-106">一般名稱的物件識別碼是2.5.4.3。</span><span class="sxs-lookup"><span data-stu-id="45e9a-106">The object identifier for a common name is 2.5.4.3.</span></span>

``` syntax
06 03                   ; OBJECT_ID (3 Bytes)
|  55 04 03             ;   2.5.4.3 Common Name (CN)
13 06                   ; PRINTABLE_STRING (6 Bytes)
   54 65 73 74 43 4e    ;   TestCN
```

<span data-ttu-id="45e9a-107">如果字串包含少於128個位元組，則多位元組的 **長度** 欄位只需要一個位元組來指定內容長度。</span><span class="sxs-lookup"><span data-stu-id="45e9a-107">If the string contains fewer than 128 bytes, the **Length** field of the TLV triplet requires only one byte to specify the content length.</span></span> <span data-ttu-id="45e9a-108">如果字串超過127個位元組，則 [ **長度** ] 欄位中的位7會設定為1，而位6至0則指定用來識別內容長度的其他位元組數目。</span><span class="sxs-lookup"><span data-stu-id="45e9a-108">If the string is more than 127 bytes, bit 7 of the **Length** field is set to 1 and bits 6 through 0 specify the number of additional bytes used to identify the content length.</span></span> <span data-ttu-id="45e9a-109">如需詳細資訊，請參閱 [編碼的長度和值位元組](about-encoded-length-and-value-bytes.md)。</span><span class="sxs-lookup"><span data-stu-id="45e9a-109">For more information, see [Encoded Length and Value Bytes](about-encoded-length-and-value-bytes.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="45e9a-110">相關主題</span><span class="sxs-lookup"><span data-stu-id="45e9a-110">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="45e9a-111">ASN. 1 類型系統</span><span class="sxs-lookup"><span data-stu-id="45e9a-111">ASN.1 Type System</span></span>](about-asn-1-type-system.md)
</dt> <dt>

[<span data-ttu-id="45e9a-112">以 DER 編碼的 ASN. 1 類型</span><span class="sxs-lookup"><span data-stu-id="45e9a-112">DER Encoding of ASN.1 Types</span></span>](about-der-encoding-of-asn-1-types.md)
</dt> </dl>

 

 



