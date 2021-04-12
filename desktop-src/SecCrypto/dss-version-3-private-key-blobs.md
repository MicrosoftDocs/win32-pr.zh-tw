---
description: 描述匯出的 DSS 第3版私密金鑰的格式。
ms.assetid: 650532fd-919b-495a-9fb9-981790447d3d
title: DSS 第3版私密金鑰 Blob
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7a6434e411ba3268901176a5c9739ceecfa79689
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104192741"
---
# <a name="dss-version-3-private-key-blobs"></a><span data-ttu-id="3a884-103">DSS 第3版私密金鑰 Blob</span><span class="sxs-lookup"><span data-stu-id="3a884-103">DSS Version 3 Private Key BLOBs</span></span>

<span data-ttu-id="3a884-104">匯出第3版 [*DSS*](../secgloss/d-gly.md) [*私密金鑰*](../secgloss/p-gly.md) 時，其格式如下：</span><span class="sxs-lookup"><span data-stu-id="3a884-104">When a version 3 [*DSS*](../secgloss/d-gly.md) [*private key*](../secgloss/p-gly.md) is exported, it is in a format as follows:</span></span>


```C++
BLOBHEADER        blobheader; 
DSSPRIVKEY_VER3   dssprivkeyver3;
BYTE p[dssprivkeyver3.bitlenP/8]; 
                    // Where P is the prime modulus
BYTE q[dssprivkeyver3.bitlenQ/8]; 
                    // Where Q is a large factor of P-1
BYTE g[dssprivkeyver3.bitlenP/8]; 
                    // Where G is the generator parameter
BYTE j[dssprivkeyver3.bitlenJ/8]; 
                    // Where J is (P-1)/Q
BYTE y[dssprivkeyver3.bitlenP/8]; 
                    // Where Y is (G^X) mod P
BYTE x[dssprivkeyver3.bitlenX/8]; 
                    // Where X is the private exponent
```



<span data-ttu-id="3a884-105">當 [](../secgloss/b-gly.md) CRYPT \_ BLOB \_ VER3 旗標與 [**CryptExportKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptexportkey)搭配使用時，會匯出此 blob 格式。</span><span class="sxs-lookup"><span data-stu-id="3a884-105">This [*BLOB*](../secgloss/b-gly.md) format is exported when the CRYPT\_BLOB\_VER3 flag is used with [**CryptExportKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptexportkey).</span></span> <span data-ttu-id="3a884-106">因為版本是在 BLOB 中，所以將此 BLOB 與 [**CryptImportKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptimportkey)搭配使用時，不需要指定旗標。</span><span class="sxs-lookup"><span data-stu-id="3a884-106">Because the version is in the BLOB, there is no need to specify a flag when using this BLOB with [**CryptImportKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptimportkey).</span></span>

<span data-ttu-id="3a884-107">下表說明 [*金鑰 BLOB*](../secgloss/k-gly.md)的每個元件。</span><span class="sxs-lookup"><span data-stu-id="3a884-107">The following table describes each component of the [*key BLOB*](../secgloss/k-gly.md).</span></span>



| <span data-ttu-id="3a884-108">欄位</span><span class="sxs-lookup"><span data-stu-id="3a884-108">Field</span></span>          | <span data-ttu-id="3a884-109">描述</span><span class="sxs-lookup"><span data-stu-id="3a884-109">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                     |
|----------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3a884-110">Blobheader</span><span class="sxs-lookup"><span data-stu-id="3a884-110">Blobheader</span></span>     | <span data-ttu-id="3a884-111">[**BLOBHEADER**](/windows/desktop/api/Wincrypt/ns-wincrypt-publickeystruc)結構。</span><span class="sxs-lookup"><span data-stu-id="3a884-111">A [**BLOBHEADER**](/windows/desktop/api/Wincrypt/ns-wincrypt-publickeystruc) structure.</span></span> <span data-ttu-id="3a884-112">**BType** 成員的值必須是 PUBLICKEYBLOB。</span><span class="sxs-lookup"><span data-stu-id="3a884-112">The **bType** member must have a value of PUBLICKEYBLOB.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                      |
| <span data-ttu-id="3a884-113">Dssprivkeyver3</span><span class="sxs-lookup"><span data-stu-id="3a884-113">Dssprivkeyver3</span></span> | <span data-ttu-id="3a884-114">**DSSPRIVKEY \_ VER3** 結構。</span><span class="sxs-lookup"><span data-stu-id="3a884-114">A **DSSPRIVKEY\_VER3** structure.</span></span> <span data-ttu-id="3a884-115">**魔術** 成員應設定為 "DSS4"， (0x34535344) 做為私用金鑰。</span><span class="sxs-lookup"><span data-stu-id="3a884-115">The **magic** member should be set to "DSS4" (0x34535344) for private keys.</span></span> <span data-ttu-id="3a884-116">請注意，十六進位值只是 "DSS4" 的 [*ASCII*](../secgloss/a-gly.md) 編碼。</span><span class="sxs-lookup"><span data-stu-id="3a884-116">Notice that the hexadecimal value is just an [*ASCII*](../secgloss/a-gly.md) encoding of "DSS4."</span></span><br/>                                                                                                                                                                                                                                                                     |
| <span data-ttu-id="3a884-117">P</span><span class="sxs-lookup"><span data-stu-id="3a884-117">P</span></span>              | <span data-ttu-id="3a884-118">P 值是位於 **DSSPRIVKEY \_ VER3** 結構的正後方，而且應該一律是 **DSSPRIVKEY \_ VER3 bitlenP** 欄位的長度（以位元組為單位）， (位長度的 p) 除以八 ([*位元組由小到小*](../secgloss/l-gly.md) 的格式) 。</span><span class="sxs-lookup"><span data-stu-id="3a884-118">The P value is located directly after the **DSSPRIVKEY\_VER3** structure, and should always be the length, in bytes, of the **DSSPRIVKEY\_VER3 bitlenP** field (bit length of P) divided by eight ([*little-endian*](../secgloss/l-gly.md) format).</span></span>                                                                                                                                                                                                                           |
| <span data-ttu-id="3a884-119">Q</span><span class="sxs-lookup"><span data-stu-id="3a884-119">Q</span></span>              | <span data-ttu-id="3a884-120">Q 值位於 P 值的正後方，而且應該一律是 **DSSPRIVKEY \_ VER3 bitlenQ** 欄位的長度（以位元組為單位），並以 8 (位元組由大到 [*小*](../secgloss/l-gly.md) 的格式) 。</span><span class="sxs-lookup"><span data-stu-id="3a884-120">The Q value is located directly after the P value and should always be the length, in bytes, of the **DSSPRIVKEY\_VER3 bitlenQ** field divided by eight ([*little-endian*](../secgloss/l-gly.md) format).</span></span>                                                                                                                                                                                                                                                                     |
| <span data-ttu-id="3a884-121">G</span><span class="sxs-lookup"><span data-stu-id="3a884-121">G</span></span>              | <span data-ttu-id="3a884-122">G 值位於 Q 值的正後方，而且應該一律是 **DSSPRIVKEY \_ VER3 bitlenP** 欄位的長度（以位元組為單位）， (位長度的 P) 除以八。</span><span class="sxs-lookup"><span data-stu-id="3a884-122">The G value is located directly after the Q value and should always be the length, in bytes, of the **DSSPRIVKEY\_VER3 bitlenP** field (bit length of P) divided by eight.</span></span> <span data-ttu-id="3a884-123">如果資料的長度是一或多個小於 P 的位元組除以8，則必須以零值的必要位元組填補資料， (零值) 讓資料變成所需的長度 (以 [*位元組*](../secgloss/l-gly.md) 由小到大格式) 。</span><span class="sxs-lookup"><span data-stu-id="3a884-123">If the length of the data is one or more bytes shorter than P divided by 8, the data must be padded with the necessary bytes (of zero value) to make the data the desired length ([*little-endian*](../secgloss/l-gly.md) format).</span></span>                                                                 |
| <span data-ttu-id="3a884-124">J</span><span class="sxs-lookup"><span data-stu-id="3a884-124">J</span></span>              | <span data-ttu-id="3a884-125">J 值會緊接在 G 值之後，且應一律為 **DSSPRIVKEY \_ VER3 bitlenJ** 欄位的長度（以位元組為單位），並以 8 (位元組由大到 [*小*](../secgloss/l-gly.md) 的格式) 。</span><span class="sxs-lookup"><span data-stu-id="3a884-125">The J value is located directly after the G value and should always be the length, in bytes, of the **DSSPRIVKEY\_VER3 bitlenJ** field divided by eight ([*little-endian*](../secgloss/l-gly.md) format).</span></span> <span data-ttu-id="3a884-126">如果 bitlenJ 值為0，則不會從 BLOB 中遺漏值。</span><span class="sxs-lookup"><span data-stu-id="3a884-126">If the bitlenJ value is 0 then the value is absent from the BLOB.</span></span>                                                                                                                                                                                                   |
| <span data-ttu-id="3a884-127">Y</span><span class="sxs-lookup"><span data-stu-id="3a884-127">Y</span></span>              | <span data-ttu-id="3a884-128">Y 值（ (G ^ X) mod P）位在 J 值的正後方，而且應該一律是 **DSSPRIVKEY \_ VER3 bitlenP** 欄位的長度（以位元組為單位）， (位長度 P) 除以八。</span><span class="sxs-lookup"><span data-stu-id="3a884-128">The Y value, (G^X) mod P, is located directly after the J value, and should always be the length, in bytes, of the **DSSPRIVKEY\_VER3 bitlenP** field (bit length of P) divided by eight.</span></span> <span data-ttu-id="3a884-129">如果 (G ^ X) mod P 的計算所產生的資料長度是一個或多個小於 P 除以8的位元組，則資料必須以零值 (的必要位元組填補，) 才能讓資料變成所需的長度 (位元組由小到 [*小*](../secgloss/l-gly.md) 的格式) 。</span><span class="sxs-lookup"><span data-stu-id="3a884-129">If the length of the data that results from the calculation of (G^X) mod P is one or more bytes shorter than P divided by 8, the data must be padded with the necessary bytes (of zero value) to make the data the desired length ([*little-endian*](../secgloss/l-gly.md) format).</span></span> |
| <span data-ttu-id="3a884-130">X</span><span class="sxs-lookup"><span data-stu-id="3a884-130">X</span></span>              | <span data-ttu-id="3a884-131">X 值是隨機的大型整數，因此 DH 金鑰組（Y）的公開部分等於： Y = (G ^ X) mod P</span><span class="sxs-lookup"><span data-stu-id="3a884-131">The X value is a random large integer such that the public portion of the DH key pair, Y, is equal to: Y = (G^X) mod P</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                               |



 

<span data-ttu-id="3a884-132">呼叫 [**CryptExportKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptexportkey)時，開發人員可以選擇是否要加密金鑰。</span><span class="sxs-lookup"><span data-stu-id="3a884-132">When calling [**CryptExportKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptexportkey), the developer can choose whether to encrypt the key.</span></span> <span data-ttu-id="3a884-133">如果 *hExpKey* 參數包含工作階段金鑰的有效控制碼，就會將金鑰加密。</span><span class="sxs-lookup"><span data-stu-id="3a884-133">The key is encrypted if the *hExpKey* parameter contains a valid handle to a session key.</span></span> <span data-ttu-id="3a884-134">但 BLOB 的 [**BLOBHEADER**](/windows/desktop/api/Wincrypt/ns-wincrypt-publickeystruc) 部分都會加密。</span><span class="sxs-lookup"><span data-stu-id="3a884-134">Everything but the [**BLOBHEADER**](/windows/desktop/api/Wincrypt/ns-wincrypt-publickeystruc) portion of the BLOB is encrypted.</span></span> <span data-ttu-id="3a884-135">請注意，加密演算法和加密金鑰參數不會與 [*私密金鑰 BLOB*](../secgloss/p-gly.md)一起儲存。</span><span class="sxs-lookup"><span data-stu-id="3a884-135">Note that the encryption algorithm and encryption key parameters are not stored along with the [*private key BLOB*](../secgloss/p-gly.md).</span></span> <span data-ttu-id="3a884-136">應用程式必須管理和儲存此資訊。</span><span class="sxs-lookup"><span data-stu-id="3a884-136">The application must manage and store this information.</span></span> <span data-ttu-id="3a884-137">如果傳遞給 *hExpKey* 的值為零，將會匯出私密金鑰而不加密。</span><span class="sxs-lookup"><span data-stu-id="3a884-137">If zero is passed for *hExpKey*, the private key will be exported without encryption.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="3a884-138">匯出私密金鑰而不加密是很危險的，因為這些金鑰接著很容易被未經授權的實體攔截及使用。</span><span class="sxs-lookup"><span data-stu-id="3a884-138">It is dangerous to export private keys without encryption because they are then vulnerable to interception and use by unauthorized entities.</span></span>

 

 

 
