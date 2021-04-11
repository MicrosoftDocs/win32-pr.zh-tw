---
description: 已提供一組高階函式來簡化及縮短完成一般訊息操作工作所需的程式碼數量。
ms.assetid: 7c1a4d6e-9b9d-43c8-b094-3c98b9a68490
title: 簡化的訊息
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1dbacaac4dd8ef32b7bab1ff4e57ad04aa1263c2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104113544"
---
# <a name="simplified-messages"></a><span data-ttu-id="2253b-103">簡化的訊息</span><span class="sxs-lookup"><span data-stu-id="2253b-103">Simplified Messages</span></span>

<span data-ttu-id="2253b-104">已提供一組高階函式來簡化及縮短完成一般訊息操作工作所需的程式碼數量。</span><span class="sxs-lookup"><span data-stu-id="2253b-104">A group of high-level functions has been provided to simplify and shorten the amount of code necessary to accomplish the usual message manipulation tasks.</span></span> <span data-ttu-id="2253b-105">這些函式稱為「簡化的訊息函數」。</span><span class="sxs-lookup"><span data-stu-id="2253b-105">These functions are called "simplified message functions."</span></span> <span data-ttu-id="2253b-106">所有簡化訊息函數的名稱都包含 "Message" 這個字。</span><span class="sxs-lookup"><span data-stu-id="2253b-106">The names of all simplified message functions contain the word "Message."</span></span>

<span data-ttu-id="2253b-107">[*簡化的訊息*](../secgloss/s-gly.md) 函式比基底加密函式或低層級訊息函式的層級更高。</span><span class="sxs-lookup"><span data-stu-id="2253b-107">[*Simplified message functions*](../secgloss/s-gly.md) are at a higher level than the base cryptographic functions or the low-level message functions.</span></span> <span data-ttu-id="2253b-108">它們會將數個基本密碼編譯、低層級訊息和憑證函式包裝成單一函式，以特定方式執行特定工作，例如加密 PKCS \# 7 訊息或簽署訊息。</span><span class="sxs-lookup"><span data-stu-id="2253b-108">They wrap several of the base cryptographic, low-level message, and certificate functions into a single function that performs a specific task in a specific manner, such as encrypting a PKCS \#7 message or signing a message.</span></span> <span data-ttu-id="2253b-109">簡化的訊息函數可讓您快速開始使用 CryptoAPI，方法是減少完成工作所需的函式呼叫數目。</span><span class="sxs-lookup"><span data-stu-id="2253b-109">Simplified message functions provide a quick way to get started using CryptoAPI by reducing the number of function calls needed to accomplish a task.</span></span>

<span data-ttu-id="2253b-110">下表列出包含詳細程式描述的章節，或使用簡化訊息函式的 C 程式範例。</span><span class="sxs-lookup"><span data-stu-id="2253b-110">The following table list sections that contain detailed procedure descriptions or C program examples of using the simplified message functions.</span></span>



| <span data-ttu-id="2253b-111">區段</span><span class="sxs-lookup"><span data-stu-id="2253b-111">Section</span></span>                                                                                                                                         | <span data-ttu-id="2253b-112">目錄</span><span class="sxs-lookup"><span data-stu-id="2253b-112">Contents</span></span>                                                                                    |
|-------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------|
| [<span data-ttu-id="2253b-113">簡化的訊息函數</span><span class="sxs-lookup"><span data-stu-id="2253b-113">Simplified Message Functions</span></span>](cryptography-functions.md)                                                         | <span data-ttu-id="2253b-114">列出簡化的訊息函數。</span><span class="sxs-lookup"><span data-stu-id="2253b-114">Lists the simplified message functions.</span></span>                                                     |
| [<span data-ttu-id="2253b-115">建立已簽署的訊息</span><span class="sxs-lookup"><span data-stu-id="2253b-115">Creating a Signed Message</span></span>](creating-a-signed-message.md)                                                                                      | <span data-ttu-id="2253b-116">詳細說明建立已簽署訊息的程式。</span><span class="sxs-lookup"><span data-stu-id="2253b-116">Details the process of creating a signed message.</span></span>                                           |
| [<span data-ttu-id="2253b-117">簽署資料的程式</span><span class="sxs-lookup"><span data-stu-id="2253b-117">Procedure for Signing Data</span></span>](procedure-for-signing-data.md)                                                                                    | <span data-ttu-id="2253b-118">提供使用簡化的訊息函式來建立已簽署訊息的程式。</span><span class="sxs-lookup"><span data-stu-id="2253b-118">Provides a procedure for using the simplified message functions to create a signed message.</span></span> |
| [<span data-ttu-id="2253b-119">驗證已簽署的訊息</span><span class="sxs-lookup"><span data-stu-id="2253b-119">Verifying A Signed Message</span></span>](verifying-a-signed-message.md)                                                                                    | <span data-ttu-id="2253b-120">詳細說明在已簽署的訊息上驗證簽章的流程。</span><span class="sxs-lookup"><span data-stu-id="2253b-120">Details a process for verifying the signature on a signed message.</span></span>                          |
| [<span data-ttu-id="2253b-121">加密訊息</span><span class="sxs-lookup"><span data-stu-id="2253b-121">Encrypting a Message</span></span>](../secauthn/encrypting-a-message.md)                                                                                           | <span data-ttu-id="2253b-122">詳述加密和解密訊息所需的工作。</span><span class="sxs-lookup"><span data-stu-id="2253b-122">Details the tasks needed to encrypt and decrypt a message.</span></span>                                  |
| [<span data-ttu-id="2253b-123">解密訊息</span><span class="sxs-lookup"><span data-stu-id="2253b-123">Decrypting a Message</span></span>](../secauthn/decrypting-a-message.md)                                                                                           | <span data-ttu-id="2253b-124">詳細說明解密訊息所需的工作。</span><span class="sxs-lookup"><span data-stu-id="2253b-124">Details the tasks needed to decrypt a message.</span></span>                                              |
| [<span data-ttu-id="2253b-125">範例 C 程式：使用 CryptEncryptMessage 和 CryptDecryptMessage</span><span class="sxs-lookup"><span data-stu-id="2253b-125">Example C Program: Using CryptEncryptMessage and CryptDecryptMessage</span></span>](example-c-program-using-cryptencryptmessage-and-cryptdecryptmessage.md) | <span data-ttu-id="2253b-126">提供用來加密和解密訊息的程式和範例程式碼。</span><span class="sxs-lookup"><span data-stu-id="2253b-126">Provides a procedure and sample code for encrypting and decrypting a message.</span></span>               |



 

 

 
