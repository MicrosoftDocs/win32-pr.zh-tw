---
description: 不透明的 Blob （也稱為 OPAQUEKEYBLOBs）是用來將工作階段金鑰儲存為特定廠商的格式，例如 Schannel。
ms.assetid: a0756c03-0c27-41ff-9b74-8af462e09675
title: 不透明的 BLOB 類型
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3e45cf8899d5cc63fb360a6b5e4177733de3880f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104386279"
---
# <a name="opaque-blob-type"></a><span data-ttu-id="c5567-103">不透明的 BLOB 類型</span><span class="sxs-lookup"><span data-stu-id="c5567-103">Opaque BLOB Type</span></span>

<span data-ttu-id="c5567-104">不 [*透明的 blob*](../secgloss/o-gly.md)（也稱為 OPAQUEKEYBLOBs）是用來將 [*工作階段金鑰*](../secgloss/s-gly.md)儲存為特定廠商的格式，例如 [*Schannel*](../secgloss/s-gly.md)。</span><span class="sxs-lookup"><span data-stu-id="c5567-104">[*Opaque BLOBs*](../secgloss/o-gly.md), also known as OPAQUEKEYBLOBs, are used to store [*session keys*](../secgloss/s-gly.md) in a vendor-specific format, such as [*Schannel*](../secgloss/s-gly.md).</span></span> <span data-ttu-id="c5567-105">其中包含基本金鑰材質和所有目前的 [*狀態*](../secgloss/s-gly.md) 資訊。</span><span class="sxs-lookup"><span data-stu-id="c5567-105">They contain the base key material and all current [*state*](../secgloss/s-gly.md) information.</span></span> <span data-ttu-id="c5567-106">這包括 [*salt 值*](../secgloss/s-gly.md)、 [*初始化向量*](../secgloss/i-gly.md)和索引鍵資料表等資訊。</span><span class="sxs-lookup"><span data-stu-id="c5567-106">This includes information such as the [*salt value*](../secgloss/s-gly.md), the [*initialization vector*](../secgloss/i-gly.md), and the key table.</span></span> <span data-ttu-id="c5567-107">不透明 Blob 的格式已解除發佈。</span><span class="sxs-lookup"><span data-stu-id="c5567-107">The format of opaque BLOBs is unpublished.</span></span> <span data-ttu-id="c5567-108">每個 CSP 廠商都會決定自己的 BLOB 格式。</span><span class="sxs-lookup"><span data-stu-id="c5567-108">Each CSP vendor determines its own BLOB format.</span></span>

<span data-ttu-id="c5567-109">因為金鑰會匯出為 CSP 專屬格式的不透明 BLOB，所以只能匯入其原本匯出的 CSP 中。</span><span class="sxs-lookup"><span data-stu-id="c5567-109">Because a key is exported into an opaque BLOB in CSP-specific format, it can only be imported into the CSP from which it was originally exported.</span></span>

<span data-ttu-id="c5567-110">牽涉到兩個進程時，每個 [*進程*](../secgloss/p-gly.md) 都會個別呼叫 [**CryptAcquireCoNtext**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptacquirecontexta) 。</span><span class="sxs-lookup"><span data-stu-id="c5567-110">When two processes are involved, each [*process*](../secgloss/p-gly.md) calls [**CryptAcquireContext**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptacquirecontexta) independently.</span></span> <span data-ttu-id="c5567-111">每個進程都會取得金鑰容器的控制碼。</span><span class="sxs-lookup"><span data-stu-id="c5567-111">Each process gets a handle to a key container.</span></span> <span data-ttu-id="c5567-112">這兩個處理常式都有可能會有相同金鑰容器的控制碼。</span><span class="sxs-lookup"><span data-stu-id="c5567-112">It is possible for both processes to have handles to the same key container.</span></span> <span data-ttu-id="c5567-113">其中一個進程會建立金鑰，並將它們匯出到不透明的 Blob，然後將 Blob 傳遞給第二個進程。</span><span class="sxs-lookup"><span data-stu-id="c5567-113">One process creates the keys and exports them into opaque BLOBs, then passes the BLOBs to the second process.</span></span> <span data-ttu-id="c5567-114">第二個進程會將 BLOB 中的金鑰匯入至其 [*金鑰容器*](../secgloss/k-gly.md)。</span><span class="sxs-lookup"><span data-stu-id="c5567-114">The second process imports the keys from the BLOB into its [*key container*](../secgloss/k-gly.md).</span></span>

<span data-ttu-id="c5567-115">如果硬體 CSP 不支援匯出金鑰，BLOB 可能只會包含金鑰登錄的索引或類似的索引。</span><span class="sxs-lookup"><span data-stu-id="c5567-115">If a hardware CSP does not support exporting keys, the BLOB might only contain the index of a key register, or something similar.</span></span> <span data-ttu-id="c5567-116">在此情況下，會忽略程式的其餘部分。</span><span class="sxs-lookup"><span data-stu-id="c5567-116">In this case, the rest of the procedure is ignored.</span></span>

``` syntax
<secure process>
cbBlob = sizeof(rgbBlob);
CryptExportKey(
          hKey, 
          0, 
          OPAQUEKEYBLOB, 
          0, 
          rgbBlob, 
          &cbBlob);
hKey = 0;

<BLOB is transferred to other process>

<user process>
CryptImportKey(
            hProv, 
            pbBlob, 
            cbBlob, 
            0, 
            0, 
            &hKey);
```

 

 
