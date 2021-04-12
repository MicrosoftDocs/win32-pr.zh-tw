---
description: 物件識別碼資料類型會編碼成以0x06 的標記值開頭的 TLV 三個。
ms.assetid: 42c015c8-3de1-4482-bf27-b19c422b8cdb
title: 物件識別碼
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d6cc81169968bfb3be5a49b0f30b8171cd904bf6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104192748"
---
# <a name="object-identifier"></a><span data-ttu-id="832ba-103">物件識別碼</span><span class="sxs-lookup"><span data-stu-id="832ba-103">OBJECT IDENTIFIER</span></span>

<span data-ttu-id="832ba-104">**物件識別碼** 資料類型會編碼成以0X06 的 **標記** 值開頭的 TLV 三個。</span><span class="sxs-lookup"><span data-stu-id="832ba-104">The **OBJECT IDENTIFIER** data type is encoded into a TLV triplet that begins with a **Tag** value of 0x06.</span></span> <span data-ttu-id="832ba-105">點十進位物件識別碼 (OID) 的每個整數都是根據下列規則進行編碼：</span><span class="sxs-lookup"><span data-stu-id="832ba-105">Each integer of a dotted decimal object identifier (OID) is encoded according to the following rules:</span></span>

-   <span data-ttu-id="832ba-106">OID 的前兩個節點會編碼至單一位元組。</span><span class="sxs-lookup"><span data-stu-id="832ba-106">The first two nodes of the OID are encoded onto a single byte.</span></span> <span data-ttu-id="832ba-107">第一個節點乘以小數40，並將結果加入至第二個節點的值。</span><span class="sxs-lookup"><span data-stu-id="832ba-107">The first node is multiplied by the decimal 40 and the result is added to the value of the second node.</span></span>
-   <span data-ttu-id="832ba-108">小於或等於127的節點值會以一個位元組編碼。</span><span class="sxs-lookup"><span data-stu-id="832ba-108">Node values less than or equal to 127 are encoded on one byte.</span></span>
-   <span data-ttu-id="832ba-109">大於或等於128的節點值會以多個位元組編碼。</span><span class="sxs-lookup"><span data-stu-id="832ba-109">Node values greater than or equal to 128 are encoded on multiple bytes.</span></span> <span data-ttu-id="832ba-110">最左邊位元組的位7會設定為1。</span><span class="sxs-lookup"><span data-stu-id="832ba-110">Bit 7 of the leftmost byte is set to one.</span></span> <span data-ttu-id="832ba-111">每個位元組的位0到6包含編碼的值。</span><span class="sxs-lookup"><span data-stu-id="832ba-111">Bits 0 through 6 of each byte contains the encoded value.</span></span>

<span data-ttu-id="832ba-112">下圖顯示這些點。</span><span class="sxs-lookup"><span data-stu-id="832ba-112">These points are shown by the following illustration.</span></span>

![物件識別碼資料類型的 der 編碼](images/der-tlv-oid.png)

<span data-ttu-id="832ba-114">下列範例顯示 **ClientId** 屬性如何在憑證要求中進行編碼。</span><span class="sxs-lookup"><span data-stu-id="832ba-114">The following example shows how the **ClientId** attribute is encoded in a certificate request.</span></span>

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

 

 



