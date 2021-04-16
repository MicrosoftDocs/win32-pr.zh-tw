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
# <a name="bit-string"></a><span data-ttu-id="4a31e-103">位字串</span><span class="sxs-lookup"><span data-stu-id="4a31e-103">BIT STRING</span></span>

<span data-ttu-id="4a31e-104">**位字串** 資料類型會編碼成以0X03 的 **標記** 位元組開頭的 TLV 三位元組。</span><span class="sxs-lookup"><span data-stu-id="4a31e-104">The **BIT STRING** data type is encoded into a TLV triplet that begins with a **Tag** byte of 0x03.</span></span> <span data-ttu-id="4a31e-105">多型的 [ **值** ] 欄位包含前置位元組，可指定最後一個位元組內容中未使用的位數。</span><span class="sxs-lookup"><span data-stu-id="4a31e-105">The **Value** field of the TLV triplet contains a leading byte that specifies the number of bits left unused in the final byte of content.</span></span> <span data-ttu-id="4a31e-106">在下列範例中，[ **長度** ] 欄位設定為 [0x03]，因為接下來有三個內容位元組，而 [ **值** ] 欄位的前置位元組會設定為 [0x04]，因為最後一個內容位元組中有四個未使用的位。</span><span class="sxs-lookup"><span data-stu-id="4a31e-106">In the following example, the **Length** field is set to 0x03 because three content bytes follow, and the leading byte of the **Value** field is set to 0x04 because there are four unused bits in the last content byte.</span></span> <span data-ttu-id="4a31e-107">每個未使用的位都會以字母 x 表示。</span><span class="sxs-lookup"><span data-stu-id="4a31e-107">Each unused bit is denoted by the letter x.</span></span>

![位字串資料類型的 der 編碼](images/der-tlv-bitstring.png)

<span data-ttu-id="4a31e-109">下列範例（取自 [pkcs \# 10 編碼](pkcs--10-encoded-asn-1.md) 的 asn.1 主題）會顯示範例 PKCS \# 10 憑證要求的編碼簽章。</span><span class="sxs-lookup"><span data-stu-id="4a31e-109">The following example, adapted from the [PKCS \#10 Encoded ASN.1](pkcs--10-encoded-asn-1.md) topic, shows the encoded signature of a sample PKCS \#10 certificate request.</span></span> <span data-ttu-id="4a31e-110">第一個位元組包含 **位字串** 資料類型（0x03）的 **標記** 值。</span><span class="sxs-lookup"><span data-stu-id="4a31e-110">The first byte contains the **Tag** value for the **BIT STRING** data type, 0x03.</span></span> <span data-ttu-id="4a31e-111">第二個和第三個位元組包含位元組陣列的長度。</span><span class="sxs-lookup"><span data-stu-id="4a31e-111">The second and third bytes contain the length of the byte array.</span></span> <span data-ttu-id="4a31e-112">第二個位元組的位7設定為1，因為內容超過127個位元組。</span><span class="sxs-lookup"><span data-stu-id="4a31e-112">Bit 7 of the second byte is set to 1 because there are more than 127 bytes of content.</span></span> <span data-ttu-id="4a31e-113">第二個位元組的位0到6指定尾端 **長度** 的位元組數，在此案例中為1。</span><span class="sxs-lookup"><span data-stu-id="4a31e-113">Bits 0 through 6 of the second byte specify the number of trailing **Length** bytes, in this case one.</span></span> <span data-ttu-id="4a31e-114">第三個位元組會指定 content bytes （0x81）的數目。</span><span class="sxs-lookup"><span data-stu-id="4a31e-114">The third byte specifies the number of content bytes, 0x81.</span></span> <span data-ttu-id="4a31e-115">第四個位元組0x00 指定存在於最後一個內容位元組中的未使用位數目。</span><span class="sxs-lookup"><span data-stu-id="4a31e-115">The fourth byte, 0x00, specifies the number of unused bits that exist in the last content byte.</span></span> <span data-ttu-id="4a31e-116">請注意，簽章會以位元組由大到小的順序進行編碼。</span><span class="sxs-lookup"><span data-stu-id="4a31e-116">Note that the signature is encoded in big-endian byte order.</span></span>

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

## <a name="related-topics"></a><span data-ttu-id="4a31e-117">相關主題</span><span class="sxs-lookup"><span data-stu-id="4a31e-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4a31e-118">ASN. 1 類型系統</span><span class="sxs-lookup"><span data-stu-id="4a31e-118">ASN.1 Type System</span></span>](about-asn-1-type-system.md)
</dt> <dt>

[<span data-ttu-id="4a31e-119">以 DER 編碼的 ASN. 1 類型</span><span class="sxs-lookup"><span data-stu-id="4a31e-119">DER Encoding of ASN.1 Types</span></span>](about-der-encoding-of-asn-1-types.md)
</dt> <dt>

[<span data-ttu-id="4a31e-120">編碼的長度和值位元組</span><span class="sxs-lookup"><span data-stu-id="4a31e-120">Encoded Length and Value Bytes</span></span>](about-encoded-length-and-value-bytes.md)
</dt> </dl>

 

 



