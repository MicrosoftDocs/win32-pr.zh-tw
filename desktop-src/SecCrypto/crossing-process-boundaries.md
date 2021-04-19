---
description: 安全通道通訊協定引擎會在安全的程式中，以及在應用程式進程中傳遞大量加密/訊息的方式，執行信號交換和驗證。
ms.assetid: bcd49aaf-b0e3-4c31-be95-986b8ad843a8
title: 跨越進程界限
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 046bc6f53d609ec22ed37edd08d6967cc4ae73e6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106970589"
---
# <a name="crossing-process-boundaries"></a><span data-ttu-id="340e6-103">跨越進程界限</span><span class="sxs-lookup"><span data-stu-id="340e6-103">Crossing Process Boundaries</span></span>

<span data-ttu-id="340e6-104">安全 [*通道通訊協定*](../secgloss/s-gly.md) 引擎會在安全的程式中，以及在應用程式進程中傳遞大量加密/訊息的 [*方式，執行*](../secgloss/p-gly.md) 信號交換和驗證。</span><span class="sxs-lookup"><span data-stu-id="340e6-104">The [*Schannel*](../secgloss/s-gly.md) protocol engine performs the handshaking and authentication in a secure [*process*](../secgloss/p-gly.md) and the bulk encryption/message passing in the application process.</span></span> <span data-ttu-id="340e6-105">這表示 [*大量加密金鑰*](../secgloss/b-gly.md) 和 [*MAC*](../secgloss/m-gly.md) 金鑰必須從一個進程複製到另一個進程。</span><span class="sxs-lookup"><span data-stu-id="340e6-105">This means that the [*bulk encryption keys*](../secgloss/b-gly.md) and [*MAC*](../secgloss/m-gly.md) keys must be copied from one process to another.</span></span> <span data-ttu-id="340e6-106">若要將金鑰從某個進程複製到另一個進程，請使用 [**CryptExportKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptexportkey) 和 [**CryptImportKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptimportkey) 功能，如下所示：</span><span class="sxs-lookup"><span data-stu-id="340e6-106">To copy the keys from one process to another, use the [**CryptExportKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptexportkey) and [**CryptImportKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptimportkey) functions as follows:</span></span>

1.  <span data-ttu-id="340e6-107">安全進程會使用 [**CryptExportKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptexportkey)將每個金鑰匯出到 [*OPAQUEKEYBLOB*](../secgloss/o-gly.md) ，然後使用 [**CryptDestroyKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptdestroykey)來終結金鑰。</span><span class="sxs-lookup"><span data-stu-id="340e6-107">The secure process exports each key into an [*OPAQUEKEYBLOB*](../secgloss/o-gly.md) using [**CryptExportKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptexportkey), then destroys the key using [**CryptDestroyKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptdestroykey).</span></span> <span data-ttu-id="340e6-108">請注意，如果金鑰儲存在硬體中，則 CSP 必須辨識這一點，且不能嘗試終結金鑰。</span><span class="sxs-lookup"><span data-stu-id="340e6-108">Note that if the key is stored in hardware, the CSP must recognize this and must not attempt to destroy the key.</span></span>
2.  <span data-ttu-id="340e6-109">安全進程會以超出本檔範圍的方式，將 OPAQUEKEYBLOBs 傳遞至應用程式進程。</span><span class="sxs-lookup"><span data-stu-id="340e6-109">The secure process passes the OPAQUEKEYBLOBs to the application process in a manner beyond the scope of this document.</span></span>
3.  <span data-ttu-id="340e6-110">應用程式進程會使用 [**CryptImportKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptimportkey)，將每個 OPAQUEKEYBLOB 匯入回 CSP。</span><span class="sxs-lookup"><span data-stu-id="340e6-110">The application process imports each OPAQUEKEYBLOB back into the CSP using [**CryptImportKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptimportkey).</span></span> <span data-ttu-id="340e6-111">此時，金鑰必須與匯出時的 [*狀態*](../secgloss/s-gly.md) 完全相同。</span><span class="sxs-lookup"><span data-stu-id="340e6-111">At this point, the key must be in exactly the same [*state*](../secgloss/s-gly.md) as when it was exported.</span></span>

 

 
