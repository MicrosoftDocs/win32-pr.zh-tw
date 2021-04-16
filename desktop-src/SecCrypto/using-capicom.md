---
description: 本章節包含使用 CAPICOM 程式的案例。
ms.assetid: f886e04a-4ea7-4d24-a05f-3e08742fe134
title: 使用 CAPICOM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 46f81b1a346b6186ead6544b7194259cc52ae2be
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104512409"
---
# <a name="using-capicom"></a><span data-ttu-id="785a2-103">使用 CAPICOM</span><span class="sxs-lookup"><span data-stu-id="785a2-103">Using CAPICOM</span></span>

<span data-ttu-id="785a2-104">\[CAPICOM 是僅限32位的元件，可用於下列作業系統： Windows Server 2008、Windows Vista 和 Windows XP。</span><span class="sxs-lookup"><span data-stu-id="785a2-104">\[CAPICOM is a 32-bit only component that is available for use in the following operating systems: Windows Server 2008, Windows Vista, and Windows XP.</span></span> <span data-ttu-id="785a2-105">相反地，請使用 .NET Framework 來執行安全性功能。</span><span class="sxs-lookup"><span data-stu-id="785a2-105">Instead, use the .NET Framework to implement security features.</span></span> <span data-ttu-id="785a2-106">如需詳細資訊，請參閱 [使用 CAPICOM 的替代方案](alternatives-to-using-capicom.md)。\]</span><span class="sxs-lookup"><span data-stu-id="785a2-106">For more information, see [Alternatives to Using CAPICOM](alternatives-to-using-capicom.md).\]</span></span>

<span data-ttu-id="785a2-107">本章節包含使用 CAPICOM 程式的案例。</span><span class="sxs-lookup"><span data-stu-id="785a2-107">This section includes scenarios that use CAPICOM procedures.</span></span>

> [!Note]  
> <span data-ttu-id="785a2-108">使用 CAPICOM 建立 [*數位簽章*](../secgloss/d-gly.md) 和取消封套的訊息是使用公開金鑰基礎結構 (PKI) 密碼編譯來完成，而且只有在簽署封包訊息的簽署者或使用者具有可用、相關聯之私密金鑰的憑證存取權時才能完成。</span><span class="sxs-lookup"><span data-stu-id="785a2-108">Creating [*digital signatures*](../secgloss/d-gly.md) and un-enveloping messages with CAPICOM is done using Public Key Infrastructure (PKI) cryptography and can only be done if the signer or user decrypting an enveloped message has access to a certificate with an available, associated private key.</span></span> <span data-ttu-id="785a2-109">若要解密封裝的訊息，具有私密金鑰存取權的憑證必須在「我的存放區」中。</span><span class="sxs-lookup"><span data-stu-id="785a2-109">To decrypt an enveloped message, a certificate with access to the private key must be in the MY store.</span></span>

 

<span data-ttu-id="785a2-110">以工作為基礎的案例討論和範例分成下列各節：</span><span class="sxs-lookup"><span data-stu-id="785a2-110">Task-based scenarios discussions and examples have been separated into the following sections:</span></span>

-   [<span data-ttu-id="785a2-111">使用 CAPICOM 的替代方案</span><span class="sxs-lookup"><span data-stu-id="785a2-111">Alternatives to Using CAPICOM</span></span>](alternatives-to-using-capicom.md)
-   [<span data-ttu-id="785a2-112">準備開始使用 CAPICOM</span><span class="sxs-lookup"><span data-stu-id="785a2-112">Getting Ready to Use CAPICOM</span></span>](getting-ready-to-use-capicom.md)
-   [<span data-ttu-id="785a2-113">加密和解密資料</span><span class="sxs-lookup"><span data-stu-id="785a2-113">Encrypting and Decrypting Data</span></span>](encrypting-and-decrypting-data.md)
-   [<span data-ttu-id="785a2-114">簽署資料和驗證數位簽章</span><span class="sxs-lookup"><span data-stu-id="785a2-114">Signing Data and Verifying Digital Signatures</span></span>](signing-data-and-verifying-digital-signatures.md)
-   [<span data-ttu-id="785a2-115">使用憑證存放區</span><span class="sxs-lookup"><span data-stu-id="785a2-115">Using Certificate Stores</span></span>](using-certificate-stores.md)
-   [<span data-ttu-id="785a2-116">建立和接收封包的資料訊息</span><span class="sxs-lookup"><span data-stu-id="785a2-116">Creating and Receiving Enveloped Data Messages</span></span>](creating-and-receiving-enveloped-data-messages-in-capicom.md)

 

 
