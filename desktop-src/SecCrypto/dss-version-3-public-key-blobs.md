---
description: PUBLICKEYBLOB 類型的 DSS 版本3公開金鑰 Blob 可用來匯出和匯入有關 DH 公開金鑰的資訊。
ms.assetid: 9aac1d61-8b61-4f0f-b037-afe4a60302de
title: DSS 版本3公開金鑰 Blob
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 593ac69025ff046a9a8d014286c2464788c07b02
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "107000242"
---
# <a name="dss-version-3-public-key-blobs"></a><span data-ttu-id="c9f67-103">DSS 版本3公開金鑰 Blob</span><span class="sxs-lookup"><span data-stu-id="c9f67-103">DSS Version 3 Public Key BLOBs</span></span>

<span data-ttu-id="c9f67-104">PUBLICKEYBLOB 類型的 DSS 版本 3 [*公開金鑰 blob*](../secgloss/p-gly.md) 可用來匯出和匯入有關 DH 公開金鑰的資訊。</span><span class="sxs-lookup"><span data-stu-id="c9f67-104">DSS version 3 [*Public Key BLOBs*](../secgloss/p-gly.md) of type PUBLICKEYBLOB are used to export and import information about a DH public key.</span></span> <span data-ttu-id="c9f67-105">它們具有下列格式：</span><span class="sxs-lookup"><span data-stu-id="c9f67-105">They have the following format:</span></span>


```C++
BLOBHEADER blobheader; 
        // As explained under "Data Structures"
DSSPUBKEY_VER3 dsspubkeyver3;
BYTE p[dsspubkeyver3.bitlenP/8]; 
       // Where P is the prime modulus
BYTE q[dsspubkeyver3.bitlenQ/8]; 
       // Where Q is a large factor of P-1
BYTE g[dsspubkeyver3.bitlenP/8]; 
       // Where G is the generator parameter
BYTE j[dsspubkeyver3.bitlenJ/8]; 
       // Where J is (P-1)/Q
BYTE y[dsspubkeyver3.bitlenP/8]; 
       // Where Y is (G^X) mod P
```



<span data-ttu-id="c9f67-106">當 [](../secgloss/b-gly.md) CRYPT \_ BLOB \_ VER3 旗標與 [**CryptExportKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptexportkey)搭配使用時，會匯出此 blob 格式。</span><span class="sxs-lookup"><span data-stu-id="c9f67-106">This [*BLOB*](../secgloss/b-gly.md) format is exported when the CRYPT\_BLOB\_VER3 flag is used with [**CryptExportKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptexportkey).</span></span> <span data-ttu-id="c9f67-107">因為版本是在 BLOB 中，所以將此 BLOB 與 [**CryptImportKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptimportkey)搭配使用時，不需要指定旗標。</span><span class="sxs-lookup"><span data-stu-id="c9f67-107">Because the version is in the BLOB, there is no need to specify a flag when using this BLOB with [**CryptImportKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptimportkey).</span></span>

<span data-ttu-id="c9f67-108">此外，當使用 *dwParam* 值 KP [](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptsetkeyparam) \_ PUB \_ 參數來設定 DSS 金鑰的金鑰參數時，此 BLOB 格式會搭配 CryptSetKeyParam 函式使用。</span><span class="sxs-lookup"><span data-stu-id="c9f67-108">In addition, this BLOB format is used with the [**CryptSetKeyParam**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptsetkeyparam) function when the *dwParam* value KP\_PUB\_PARAMS is used to set key parameters on a DSS key.</span></span> <span data-ttu-id="c9f67-109">這是在 \_ 用來產生金鑰的 CRYPT PREGEN 旗標時完成的。</span><span class="sxs-lookup"><span data-stu-id="c9f67-109">This is done when the CRYPT\_PREGEN flag has been used to generate the key.</span></span> <span data-ttu-id="c9f67-110">在這種情況下，y 值會被忽略，因此不應該包含在 BLOB 中。</span><span class="sxs-lookup"><span data-stu-id="c9f67-110">When used in this situation, the y value is ignored and therefore should not be included in the BLOB.</span></span>

<span data-ttu-id="c9f67-111">下表說明金鑰 BLOB 的每個元件。</span><span class="sxs-lookup"><span data-stu-id="c9f67-111">The following table describes each component of the key BLOB.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="c9f67-112">欄位</span><span class="sxs-lookup"><span data-stu-id="c9f67-112">Field</span></span></th>
<th><span data-ttu-id="c9f67-113">描述</span><span class="sxs-lookup"><span data-stu-id="c9f67-113">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="c9f67-114">Blobheader</span><span class="sxs-lookup"><span data-stu-id="c9f67-114">Blobheader</span></span></td>
<td><span data-ttu-id="c9f67-115"><a href="/windows/desktop/api/Wincrypt/ns-wincrypt-publickeystruc"><strong>BLOBHEADER</strong></a>結構。</span><span class="sxs-lookup"><span data-stu-id="c9f67-115">A <a href="/windows/desktop/api/Wincrypt/ns-wincrypt-publickeystruc"><strong>BLOBHEADER</strong></a> structure.</span></span> <span data-ttu-id="c9f67-116"><strong>BType</strong>成員的值必須是 PUBLICKEYBLOB。</span><span class="sxs-lookup"><span data-stu-id="c9f67-116">The <strong>bType</strong> member must have a value of PUBLICKEYBLOB.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="c9f67-117">Dsspubkeyver3</span><span class="sxs-lookup"><span data-stu-id="c9f67-117">Dsspubkeyver3</span></span></td>
<td><span data-ttu-id="c9f67-118"><a href="/previous-versions/windows/desktop/legacy/aa381983(v=vs.85)"><strong>DSSPUBKEY_VER3</strong></a>結構。</span><span class="sxs-lookup"><span data-stu-id="c9f67-118">A <a href="/previous-versions/windows/desktop/legacy/aa381983(v=vs.85)"><strong>DSSPUBKEY_VER3</strong></a> structure.</span></span> <span data-ttu-id="c9f67-119"><strong>魔術</strong>成員應設定為 &quot; DSS3 &quot; (0x33535344) 的公開金鑰。</span><span class="sxs-lookup"><span data-stu-id="c9f67-119">The <strong>magic</strong> member should be set to &quot;DSS3&quot; (0x33535344) for public keys.</span></span> <span data-ttu-id="c9f67-120">請注意，十六進位值只是 DSS3 的 <a href="/windows/desktop/SecGloss/a-gly"><em>ASCII</em></a> 編碼 &quot; 。&quot;</span><span class="sxs-lookup"><span data-stu-id="c9f67-120">Notice that the hexadecimal value is just an <a href="/windows/desktop/SecGloss/a-gly"><em>ASCII</em></a> encoding of &quot;DSS3.&quot;</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="c9f67-121">P</span><span class="sxs-lookup"><span data-stu-id="c9f67-121">P</span></span></td>
<td><span data-ttu-id="c9f67-122">P 值位於 <a href="/previous-versions/windows/desktop/legacy/aa381983(v=vs.85)"><strong>DSSPUBKEY_VER3</strong></a> 結構的正後方，而且應該一律是 DSSPUBKEY_VER3 <strong>bitlenP</strong> (欄位的長度（以位元組為單位）) 除以八 (<a href="/windows/desktop/SecGloss/l-gly"><em>位元組由小到小</em></a> 的格式) 。</span><span class="sxs-lookup"><span data-stu-id="c9f67-122">The P value is located directly after the <a href="/previous-versions/windows/desktop/legacy/aa381983(v=vs.85)"><strong>DSSPUBKEY_VER3</strong></a> structure, and should always be the length, in bytes, of the DSSPUBKEY_VER3 <strong>bitlenP</strong> field (bit length of P) divided by eight (<a href="/windows/desktop/SecGloss/l-gly"><em>little-endian</em></a> format).</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="c9f67-123">Q</span><span class="sxs-lookup"><span data-stu-id="c9f67-123">Q</span></span></td>
<td><span data-ttu-id="c9f67-124">Q 值位於 P 值的正後方，而且應該一律是 <a href="/previous-versions/windows/desktop/legacy/aa381983(v=vs.85)"><strong>DSSPUBKEY_VER3</strong></a><strong>bitlenQ</strong> 成員的長度（以位元組為單位），並以八 (位元組由大 <a href="/windows/desktop/SecGloss/l-gly"><em>到小</em></a> 的格式) 。</span><span class="sxs-lookup"><span data-stu-id="c9f67-124">The Q value is located directly after the P value and should always be the length in bytes of the <a href="/previous-versions/windows/desktop/legacy/aa381983(v=vs.85)"><strong>DSSPUBKEY_VER3</strong></a><strong>bitlenQ</strong> member divided by eight (<a href="/windows/desktop/SecGloss/l-gly"><em>little-endian</em></a> format).</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="c9f67-125">G</span><span class="sxs-lookup"><span data-stu-id="c9f67-125">G</span></span></td>
<td><span data-ttu-id="c9f67-126">G 值是在 Q 值的正後方，而且應該一律是 DSSPUBKEY_VER3 的長度（以位元組為單位），而 P) 的<a href="/previous-versions/windows/desktop/legacy/aa381983(v=vs.85)"><strong></strong></a><strong>bitlenP</strong>成員 (位長度除以八。</span><span class="sxs-lookup"><span data-stu-id="c9f67-126">The G value is located directly after the Q value and should always be the length, in bytes, of the <a href="/previous-versions/windows/desktop/legacy/aa381983(v=vs.85)"><strong>DSSPUBKEY_VER3</strong></a><strong>bitlenP</strong> member (bit length of P) divided by eight.</span></span> <span data-ttu-id="c9f67-127">如果資料的長度是一或多個小於 P 的位元組除以8，則必須以零值的必要位元組填補資料， (零值) 讓資料變成所需的長度 (以 <a href="/windows/desktop/SecGloss/l-gly"><em>位元組</em></a> 由小到大格式) 。</span><span class="sxs-lookup"><span data-stu-id="c9f67-127">If the length of the data is one or more bytes shorter than P divided by 8, the data must be padded with the necessary bytes (of zero value) to make the data the desired length (<a href="/windows/desktop/SecGloss/l-gly"><em>little-endian</em></a> format).</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="c9f67-128">J</span><span class="sxs-lookup"><span data-stu-id="c9f67-128">J</span></span></td>
<td><span data-ttu-id="c9f67-129">J 值會緊接在 G 值之後，且應該一律是 <a href="/previous-versions/windows/desktop/legacy/aa381983(v=vs.85)"><strong>DSSPUBKEY_VER3</strong></a><strong>bitlenJ</strong> 成員的長度（以位元組為單位），並以八 (位元組由大 <a href="/windows/desktop/SecGloss/l-gly"><em>到小</em></a> 的格式) 。</span><span class="sxs-lookup"><span data-stu-id="c9f67-129">The J value is located directly after the G value and should always be the length in bytes of the <a href="/previous-versions/windows/desktop/legacy/aa381983(v=vs.85)"><strong>DSSPUBKEY_VER3</strong></a><strong>bitlenJ</strong> member divided by eight (<a href="/windows/desktop/SecGloss/l-gly"><em>little-endian</em></a> format).</span></span> <span data-ttu-id="c9f67-130">如果 bitlenQ 值為0，則不會從 BLOB 中遺漏值。</span><span class="sxs-lookup"><span data-stu-id="c9f67-130">If the bitlenQ value is 0, then the value is absent from the BLOB.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="c9f67-131">Y</span><span class="sxs-lookup"><span data-stu-id="c9f67-131">Y</span></span></td>
<td><span data-ttu-id="c9f67-132">Y 值（ (G ^ X) mod P）位在 J 值的正後方，而且應該一律是以位元組為單位的 <a href="/previous-versions/windows/desktop/legacy/aa381983(v=vs.85)"><strong>DSSPUBKEY_VER3</strong></a><strong>bitlenP</strong> 成員 (位長度的 P) 除以八。</span><span class="sxs-lookup"><span data-stu-id="c9f67-132">The Y value, (G^X) mod P, is located directly after the J value, and should always be the length, in bytes, of the <a href="/previous-versions/windows/desktop/legacy/aa381983(v=vs.85)"><strong>DSSPUBKEY_VER3</strong></a><strong>bitlenP</strong> member (bit length of P) divided by eight.</span></span> <span data-ttu-id="c9f67-133">如果 (G ^ X) mod P 的計算所產生的資料長度是一個或多個小於 P 除以8的位元組，則資料必須以零值 (的必要位元組填補，) 才能讓資料變成所需的長度 (位元組由小到 <a href="/windows/desktop/SecGloss/l-gly"><em>小</em></a> 的格式) 。</span><span class="sxs-lookup"><span data-stu-id="c9f67-133">If the length of the data that results from the calculation of (G^X) mod P is one or more bytes shorter than P divided by 8, the data must be padded with the necessary bytes (of zero value) to make the data the desired length (<a href="/windows/desktop/SecGloss/l-gly"><em>little-endian</em></a> format).</span></span>
<blockquote>
[!Note]<br />
<span data-ttu-id="c9f67-134">當此結構搭配 <a href="/windows/desktop/api/Wincrypt/nf-wincrypt-cryptsetkeyparam"><strong>CryptSetKeyParam</strong></a> 使用 <em>dwParam</em> 值 KP_PUB_PARAMS 時，BLOB 中不會包含此值。</span><span class="sxs-lookup"><span data-stu-id="c9f67-134">When this structure is used with <a href="/windows/desktop/api/Wincrypt/nf-wincrypt-cryptsetkeyparam"><strong>CryptSetKeyParam</strong></a> with the <em>dwParam</em> value KP_PUB_PARAMS, then this value is not included in the BLOB.</span></span>
</blockquote>
<br/> <br/></td>
</tr>
</tbody>
</table>



 

> [!Note]  
> <span data-ttu-id="c9f67-135">公開金鑰 Blob 未加密，但包含純文字格式的公開金鑰。</span><span class="sxs-lookup"><span data-stu-id="c9f67-135">Public key BLOBs are not encrypted, but contain public keys in plaintext form.</span></span>

 

 

 
