---
description: BMPString 資料類型稱為「 \_ 憑證註冊 API」中的 UNICODE 字串，它會編碼成以0x1E 的標記位元組開頭的 TLV 三位元組。
ms.assetid: 66e4a6d8-2401-4346-9361-e145735cbe19
title: BMPString
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8c911218d852b792a333f015c825a7e4d1486b62
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104192751"
---
# <a name="bmpstring"></a><span data-ttu-id="ba2c4-103">BMPString</span><span class="sxs-lookup"><span data-stu-id="ba2c4-103">BMPString</span></span>

<span data-ttu-id="ba2c4-104">**BMPString** 資料類型稱為「憑證註冊 API」中的 **UNICODE \_ 字串**，它會編碼成以0x1E 的 **標記** 位元組開頭的 TLV 三位元組。</span><span class="sxs-lookup"><span data-stu-id="ba2c4-104">The ASN.1 **BMPString** data type, called a **UNICODE\_STRING** in the Certificate Enrollment API, is encoded into a TLV triplet that begins with a **Tag** byte of 0x1E.</span></span> <span data-ttu-id="ba2c4-105">下列範例是從 [CMC 編碼](cmc-encoded-asn-1.md) 的 asn.1 主題進行調整，以顯示 **TemplateName** 延伸模組的編碼方式。</span><span class="sxs-lookup"><span data-stu-id="ba2c4-105">The following example, adapted from the [CMC Encoded ASN.1](cmc-encoded-asn-1.md) topic, shows the encoding for a **TemplateName** extension.</span></span> <span data-ttu-id="ba2c4-106">您可以使用 [**IX509ExtensionTemplateName**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extensiontemplatename) 介面來指定名稱。</span><span class="sxs-lookup"><span data-stu-id="ba2c4-106">The name can be specified by using the [**IX509ExtensionTemplateName**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extensiontemplatename) interface.</span></span> <span data-ttu-id="ba2c4-107">延伸模組的物件識別碼是1.3.6.1.4.1.311.13.2.1。</span><span class="sxs-lookup"><span data-stu-id="ba2c4-107">The object identifier for the extension is 1.3.6.1.4.1.311.13.2.1.</span></span>

``` syntax
06 0a                              ; OBJECT_ID (a Bytes)
|  2b 06 01 04 01 82 37 0d  02 01  ;   1.3.6.1.4.1.311.13.2.1 
31 34                              ; SET (34 Bytes)
   30 32                           ; SEQUENCE (32 Bytes)
      1e 26                        ; UNICODE_STRING (26 Bytes)
      |  00 43 00 65 00 72 00 74   ;   .C.e.r.t
      |  00 69 00 66 00 69 00 63   ;   .i.f.i.c
      |  00 61 00 74 00 65 00 54   ;   .a.t.e.T
      |  00 65 00 6d 00 70 00 6c   ;   .e.m.p.l
      |  00 61 00 74 00 65         ;   .a.t.e
      1e 08                        ; UNICODE_STRING (8 Bytes)
         00 55 00 73 00 65 00 72   ;   .U.s.e.r
```

<span data-ttu-id="ba2c4-108">如果字串包含少於128個位元組，則多位元組的 **長度** 欄位只需要一個位元組來指定內容長度。</span><span class="sxs-lookup"><span data-stu-id="ba2c4-108">If the string contains fewer than 128 bytes, the **Length** field of the TLV triplet requires only one byte to specify the content length.</span></span> <span data-ttu-id="ba2c4-109">如果字串超過127個位元組，則 [ **長度** ] 欄位中的位7會設定為1，而位6至0則指定用來識別內容長度的其他位元組數目。</span><span class="sxs-lookup"><span data-stu-id="ba2c4-109">If the string is more than 127 bytes, bit 7 of the **Length** field is set to 1 and bits 6 through 0 specify the number of additional bytes used to identify the content length.</span></span> <span data-ttu-id="ba2c4-110">如需詳細資訊，請參閱 [編碼的長度和值位元組](about-encoded-length-and-value-bytes.md)。</span><span class="sxs-lookup"><span data-stu-id="ba2c4-110">For more information, see [Encoded Length and Value Bytes](about-encoded-length-and-value-bytes.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="ba2c4-111">相關主題</span><span class="sxs-lookup"><span data-stu-id="ba2c4-111">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ba2c4-112">ASN. 1 類型系統</span><span class="sxs-lookup"><span data-stu-id="ba2c4-112">ASN.1 Type System</span></span>](about-asn-1-type-system.md)
</dt> <dt>

[<span data-ttu-id="ba2c4-113">以 DER 編碼的 ASN. 1 類型</span><span class="sxs-lookup"><span data-stu-id="ba2c4-113">DER Encoding of ASN.1 Types</span></span>](about-der-encoding-of-asn-1-types.md)
</dt> </dl>

 

 



