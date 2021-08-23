---
description: PUBLICKEYBLOB 類型的 DSS 版本3公開金鑰 Blob 可用來匯出和匯入有關 DH 公開金鑰的資訊。
ms.assetid: 9aac1d61-8b61-4f0f-b037-afe4a60302de
title: DSS 版本3公開金鑰 Blob
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f5cc4894000f284dfd5d1b1dd9e9a7353e4eee0b09a42edc63de76e8eaa93184
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119875258"
---
# <a name="dss-version-3-public-key-blobs"></a>DSS 版本3公開金鑰 Blob

PUBLICKEYBLOB 類型的 DSS 版本 3 [*公開金鑰 blob*](../secgloss/p-gly.md) 可用來匯出和匯入有關 DH 公開金鑰的資訊。 它們具有下列格式：


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



當 [](../secgloss/b-gly.md) CRYPT \_ BLOB \_ VER3 旗標與 [**CryptExportKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptexportkey)搭配使用時，會匯出此 blob 格式。 因為版本是在 BLOB 中，所以將此 BLOB 與 [**CryptImportKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptimportkey)搭配使用時，不需要指定旗標。

此外，當使用 *dwParam* 值 KP [](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptsetkeyparam) \_ PUB \_ 參數來設定 DSS 金鑰的金鑰參數時，此 BLOB 格式會搭配 CryptSetKeyParam 函式使用。 這是在 \_ 用來產生金鑰的 CRYPT PREGEN 旗標時完成的。 在這種情況下，y 值會被忽略，因此不應該包含在 BLOB 中。

下表說明金鑰 BLOB 的每個元件。



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>欄位</th>
<th>描述</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Blobheader</td>
<td><a href="/windows/desktop/api/Wincrypt/ns-wincrypt-publickeystruc"><strong>BLOBHEADER</strong></a>結構。 <strong>BType</strong>成員的值必須是 PUBLICKEYBLOB。</td>
</tr>
<tr class="even">
<td>Dsspubkeyver3</td>
<td><a href="/previous-versions/windows/desktop/legacy/aa381983(v=vs.85)"><strong>DSSPUBKEY_VER3</strong></a>結構。 <strong>魔術</strong>成員應設定為 &quot; DSS3 &quot; (0x33535344) 的公開金鑰。 請注意，十六進位值只是 DSS3 的 <a href="/windows/desktop/SecGloss/a-gly"><em>ASCII</em></a> 編碼 &quot; 。&quot;<br/></td>
</tr>
<tr class="odd">
<td>P</td>
<td>P 值位於 <a href="/previous-versions/windows/desktop/legacy/aa381983(v=vs.85)"><strong>DSSPUBKEY_VER3</strong></a> 結構的正後方，而且應該一律是 DSSPUBKEY_VER3 <strong>bitlenP</strong> (欄位的長度（以位元組為單位）) 除以八 (<a href="/windows/desktop/SecGloss/l-gly"><em>位元組由小到小</em></a> 的格式) 。</td>
</tr>
<tr class="even">
<td>Q</td>
<td>Q 值位於 P 值的正後方，而且應該一律是 <a href="/previous-versions/windows/desktop/legacy/aa381983(v=vs.85)"><strong>DSSPUBKEY_VER3</strong></a><strong>bitlenQ</strong> 成員的長度（以位元組為單位），並以八 (位元組由大 <a href="/windows/desktop/SecGloss/l-gly"><em>到小</em></a> 的格式) 。</td>
</tr>
<tr class="odd">
<td>G</td>
<td>G 值是在 Q 值的正後方，而且應該一律是 DSSPUBKEY_VER3 的長度（以位元組為單位），而 P) 的<a href="/previous-versions/windows/desktop/legacy/aa381983(v=vs.85)"><strong></strong></a><strong>bitlenP</strong>成員 (位長度除以八。 如果資料的長度是一或多個小於 P 的位元組除以8，則必須以零值的必要位元組填補資料， (零值) 讓資料變成所需的長度 (以 <a href="/windows/desktop/SecGloss/l-gly"><em>位元組</em></a> 由小到大格式) 。</td>
</tr>
<tr class="even">
<td>J</td>
<td>J 值會緊接在 G 值之後，且應該一律是 <a href="/previous-versions/windows/desktop/legacy/aa381983(v=vs.85)"><strong>DSSPUBKEY_VER3</strong></a><strong>bitlenJ</strong> 成員的長度（以位元組為單位），並以八 (位元組由大 <a href="/windows/desktop/SecGloss/l-gly"><em>到小</em></a> 的格式) 。 如果 bitlenQ 值為0，則不會從 BLOB 中遺漏值。</td>
</tr>
<tr class="odd">
<td>Y</td>
<td>Y 值（ (G ^ X) mod P）位在 J 值的正後方，而且應該一律是以位元組為單位的 <a href="/previous-versions/windows/desktop/legacy/aa381983(v=vs.85)"><strong>DSSPUBKEY_VER3</strong></a><strong>bitlenP</strong> 成員 (位長度的 P) 除以八。 如果 (G ^ X) mod P 的計算所產生的資料長度是一個或多個小於 P 除以8的位元組，則資料必須以零值 (的必要位元組填補，) 才能讓資料變成所需的長度 (位元組由小到 <a href="/windows/desktop/SecGloss/l-gly"><em>小</em></a> 的格式) 。
<blockquote>
[!Note]<br />
當此結構搭配 <a href="/windows/desktop/api/Wincrypt/nf-wincrypt-cryptsetkeyparam"><strong>CryptSetKeyParam</strong></a> 使用 <em>dwParam</em> 值 KP_PUB_PARAMS 時，BLOB 中不會包含此值。
</blockquote>
<br/> <br/></td>
</tr>
</tbody>
</table>



 

> [!Note]  
> 公開金鑰 Blob 未加密，但包含純文字格式的公開金鑰。

 

 

 
