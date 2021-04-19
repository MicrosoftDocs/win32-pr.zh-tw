---
description: TLV 內建的長度欄位會識別值欄位中編碼的位元組數目。
ms.assetid: d72371f9-fe55-468d-b15b-0f8948674619
title: 編碼的長度和值位元組
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b45eaec36875446d7493f37fc150f7b5f9d1a59c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "107001361"
---
# <a name="encoded-length-and-value-bytes"></a><span data-ttu-id="c8f2a-103">編碼的長度和值位元組</span><span class="sxs-lookup"><span data-stu-id="c8f2a-103">Encoded Length and Value Bytes</span></span>

<span data-ttu-id="c8f2a-104">TLV 內建的 *長度* 欄位會識別 *值* 欄位中編碼的位元組數目。</span><span class="sxs-lookup"><span data-stu-id="c8f2a-104">The *Length* field in a TLV triplet identifies the number of bytes encoded in the *Value* field.</span></span> <span data-ttu-id="c8f2a-105">*值* 欄位包含在電腦之間傳送的內容。</span><span class="sxs-lookup"><span data-stu-id="c8f2a-105">The *Value* field contains the content being sent between computers.</span></span> <span data-ttu-id="c8f2a-106">如果 [ *值* ] 欄位包含少於128個位元組，則 [ *長度* ] 欄位只需要一個位元組。</span><span class="sxs-lookup"><span data-stu-id="c8f2a-106">If the *Value* field contains fewer than 128 bytes, the *Length* field requires only one byte.</span></span> <span data-ttu-id="c8f2a-107">*長度* 欄位的位7是零 (0) 而其餘的位會識別要傳送之內容的位元組數目。</span><span class="sxs-lookup"><span data-stu-id="c8f2a-107">Bit 7 of the *Length* field is zero (0) and the remaining bits identify the number of bytes of content being sent.</span></span> <span data-ttu-id="c8f2a-108">如果 [ *值* ] 欄位包含超過127個位元組，則 [ *長度* ] 欄位中的位7是一個 (1) 而其餘的位會識別包含長度所需的位元組數目。</span><span class="sxs-lookup"><span data-stu-id="c8f2a-108">If the *Value* field contains more than 127 bytes, bit 7 of the *Length* field is one (1) and the remaining bits identify the number of bytes needed to contain the length.</span></span> <span data-ttu-id="c8f2a-109">下圖顯示範例。</span><span class="sxs-lookup"><span data-stu-id="c8f2a-109">Examples are shown in the following illustration.</span></span>

![der tlv 長度位元組](images/der-tlv-lengthbyte.png)

## <a name="related-topics"></a><span data-ttu-id="c8f2a-111">相關主題</span><span class="sxs-lookup"><span data-stu-id="c8f2a-111">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c8f2a-112">DER 傳送語法</span><span class="sxs-lookup"><span data-stu-id="c8f2a-112">DER Transfer Syntax</span></span>](about-der-transfer-syntax.md)
</dt> <dt>

[<span data-ttu-id="c8f2a-113">編碼的標記位元組</span><span class="sxs-lookup"><span data-stu-id="c8f2a-113">Encoded Tag Bytes</span></span>](about-encoded-tag-bytes.md)
</dt> </dl>

 

 



