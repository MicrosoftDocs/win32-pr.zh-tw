---
description: IA5tring 資料類型會編碼成以0x16 的標記位元組開頭的 TLV 三位元組。
ms.assetid: c1268524-4304-4c21-8f7d-f0a2826cd74e
title: IA5String
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7562fab655462455b03d35041bdb8f572b064cac
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104192752"
---
# <a name="ia5string"></a><span data-ttu-id="e8eb2-103">IA5String</span><span class="sxs-lookup"><span data-stu-id="e8eb2-103">IA5String</span></span>

<span data-ttu-id="e8eb2-104">**IA5tring** 資料類型會編碼成以0X16 的 **標記** 位元組開頭的 TLV 三位元組。</span><span class="sxs-lookup"><span data-stu-id="e8eb2-104">The ASN.1 **IA5tring** data type is encoded into a TLV triplet that begins with a **Tag** byte of 0x16.</span></span> <span data-ttu-id="e8eb2-105">下列範例是從 [CMC 編碼的 ASN. 1](cmc-encoded-asn-1.md) 主題進行調整，顯示 **OSVersion** 屬性如何編碼為 **IA5tring** 類型。</span><span class="sxs-lookup"><span data-stu-id="e8eb2-105">The following example, adapted from the [CMC Encoded ASN.1](cmc-encoded-asn-1.md) topic, shows how the **OSVersion** attribute is encoded as an **IA5tring** type.</span></span> <span data-ttu-id="e8eb2-106">您可以使用 [**IX509AttributeOSVersion**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509attributeosversion) 介面來指定版本號碼。</span><span class="sxs-lookup"><span data-stu-id="e8eb2-106">The version number can be specified by using the [**IX509AttributeOSVersion**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509attributeosversion) interface.</span></span> <span data-ttu-id="e8eb2-107">屬性的物件識別碼是1.3.6.1.4.1.311.13.2.3。</span><span class="sxs-lookup"><span data-stu-id="e8eb2-107">The object identifier for the attribute is 1.3.6.1.4.1.311.13.2.3.</span></span>

``` syntax
06 0a                                   ; OBJECT_ID (a Bytes)
|  2b 06 01 04 01 82 37 0d  02 03       ;   1.3.6.1.4.1.311.13.2.3 
31 0c                                   ; SET (c Bytes)
   16 0a                                ; IA5_STRING (a Bytes)
      36 2e 30 2e 35 33 36 31  2e 32    ;   6.0.5361.2
```

<span data-ttu-id="e8eb2-108">如果字串包含少於128個位元組，則多位元組的 **長度** 欄位只需要一個位元組來指定內容長度。</span><span class="sxs-lookup"><span data-stu-id="e8eb2-108">If the string contains fewer than 128 bytes, the **Length** field of the TLV triplet requires only one byte to specify the content length.</span></span> <span data-ttu-id="e8eb2-109">如果字串超過127個位元組，則 [ **長度** ] 欄位中的位7會設定為1，而位6至0則指定用來識別內容長度的其他位元組數目。</span><span class="sxs-lookup"><span data-stu-id="e8eb2-109">If the string is more than 127 bytes, bit 7 of the **Length** field is set to 1 and bits 6 through 0 specify the number of additional bytes used to identify the content length.</span></span> <span data-ttu-id="e8eb2-110">如需詳細資訊，請參閱 [編碼的長度和值位元組](about-encoded-length-and-value-bytes.md)。</span><span class="sxs-lookup"><span data-stu-id="e8eb2-110">For more information, see [Encoded Length and Value Bytes](about-encoded-length-and-value-bytes.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="e8eb2-111">相關主題</span><span class="sxs-lookup"><span data-stu-id="e8eb2-111">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e8eb2-112">ASN. 1 類型系統</span><span class="sxs-lookup"><span data-stu-id="e8eb2-112">ASN.1 Type System</span></span>](about-asn-1-type-system.md)
</dt> <dt>

[<span data-ttu-id="e8eb2-113">以 DER 編碼的 ASN. 1 類型</span><span class="sxs-lookup"><span data-stu-id="e8eb2-113">DER Encoding of ASN.1 Types</span></span>](about-der-encoding-of-asn-1-types.md)
</dt> </dl>

 

 



