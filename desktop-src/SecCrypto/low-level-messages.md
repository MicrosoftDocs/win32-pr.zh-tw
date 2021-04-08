---
description: 低層級訊息函式會針對已接收的傳輸和解碼資料來編碼資料。 低層級訊息函式也會解密並驗證已接收訊息的簽章。
ms.assetid: 42c19920-c7f7-4a4d-9de3-3de9a34fbe0c
title: 低層級訊息函數
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 22654f19dfe5178dfb98006c17c2d0536f78cd46
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103690743"
---
# <a name="low-level-message-functions"></a><span data-ttu-id="20580-104">低層級訊息函數</span><span class="sxs-lookup"><span data-stu-id="20580-104">Low-level Message Functions</span></span>

<span data-ttu-id="20580-105">[*低層級訊息函式*](../secgloss/l-gly.md)會針對已接收的傳輸和解碼資料來編碼資料。</span><span class="sxs-lookup"><span data-stu-id="20580-105">The [*low-level message functions*](../secgloss/l-gly.md) encode data for transmission and decode data that has been received.</span></span> <span data-ttu-id="20580-106">低層級訊息函式也會解密並驗證已接收訊息的簽章。</span><span class="sxs-lookup"><span data-stu-id="20580-106">Low-level message functions also decrypt and verify the signatures of received messages.</span></span>

<span data-ttu-id="20580-107">使用低層級的訊息開啟函式開啟訊息時，它會保持開啟且可用 (維護其 [*狀態*](../secgloss/s-gly.md)) 直到關閉為止。</span><span class="sxs-lookup"><span data-stu-id="20580-107">When a message is opened using a low-level message open function, it remains open and available (maintains its [*state*](../secgloss/s-gly.md)) until it is closed.</span></span> <span data-ttu-id="20580-108">這可讓您使用多個呼叫 [**CryptMsgUpdate**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsgupdate) 函式來分次訊息。</span><span class="sxs-lookup"><span data-stu-id="20580-108">This allows a message to be constructed piecemeal using multiple calls to the [**CryptMsgUpdate**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsgupdate) function.</span></span>

<span data-ttu-id="20580-109">使用低層級的訊息函式需要比使用簡化的訊息函式更多的函式呼叫 (請參閱) 的 [簡化訊息](simplified-messages.md) 。</span><span class="sxs-lookup"><span data-stu-id="20580-109">Using low-level message functions requires more function calls than using simplified message functions (see [Simplified Messages](simplified-messages.md)).</span></span> <span data-ttu-id="20580-110">如果使用簡化的訊息函式，則會在 API 的函式內執行更多工作。</span><span class="sxs-lookup"><span data-stu-id="20580-110">If the simplified message functions are used, more of the work is done inside the functions of the API.</span></span>

<span data-ttu-id="20580-111">使用低層級訊息函式牽涉到額外的工作，以呼叫其他憑證或密碼編譯功能。</span><span class="sxs-lookup"><span data-stu-id="20580-111">Using low-level message functions involves the additional work of making calls to other certificate or cryptographic functions.</span></span> <span data-ttu-id="20580-112">例如，可能需要呼叫憑證函式的資料，才能初始化這些低層級訊息函式所使用的結構。</span><span class="sxs-lookup"><span data-stu-id="20580-112">For example, data from calls to certificate functions may be needed to initialize structures used by these low-level message functions.</span></span> <span data-ttu-id="20580-113">簡化的訊息函數會在內部初始化許多這些結構。</span><span class="sxs-lookup"><span data-stu-id="20580-113">Simplified message functions initialize many of these structures internally.</span></span>

<span data-ttu-id="20580-114">下表列出具有程式描述的區段，以及使用低層級訊息函式的 C 程式碼範例。</span><span class="sxs-lookup"><span data-stu-id="20580-114">The following table lists sections with procedure descriptions and C code examples of using the low-level message functions.</span></span>



| <span data-ttu-id="20580-115">區段</span><span class="sxs-lookup"><span data-stu-id="20580-115">Section</span></span>                                                                               | <span data-ttu-id="20580-116">目錄</span><span class="sxs-lookup"><span data-stu-id="20580-116">Contents</span></span>                                           |
|---------------------------------------------------------------------------------------|----------------------------------------------------|
| [<span data-ttu-id="20580-117">低層級訊息函數</span><span class="sxs-lookup"><span data-stu-id="20580-117">Low-level Message Functions</span></span>](cryptography-functions.md) | <span data-ttu-id="20580-118">列出低層級的訊息函數。</span><span class="sxs-lookup"><span data-stu-id="20580-118">Lists the low-level message functions.</span></span>             |
| [<span data-ttu-id="20580-119">簽署資料</span><span class="sxs-lookup"><span data-stu-id="20580-119">Signing Data</span></span>](signing-data.md)                                                      | <span data-ttu-id="20580-120">詳述簽署資料所需的工作。</span><span class="sxs-lookup"><span data-stu-id="20580-120">Details the tasks needed to sign data.</span></span>             |
| [<span data-ttu-id="20580-121">編碼封包資料</span><span class="sxs-lookup"><span data-stu-id="20580-121">Encoding Enveloped Data</span></span>](encoding-enveloped-data.md)                                | <span data-ttu-id="20580-122">詳細說明編碼封包資料所需的工作。</span><span class="sxs-lookup"><span data-stu-id="20580-122">Details the tasks needed to encode enveloped data.</span></span> |
| [<span data-ttu-id="20580-123">解碼封包資料</span><span class="sxs-lookup"><span data-stu-id="20580-123">Decoding Enveloped Data</span></span>](decoding-enveloped-data.md)                                | <span data-ttu-id="20580-124">詳細說明解碼封包資料所需的工作。</span><span class="sxs-lookup"><span data-stu-id="20580-124">Details the tasks needed to decode enveloped data.</span></span> |



 

 

 
