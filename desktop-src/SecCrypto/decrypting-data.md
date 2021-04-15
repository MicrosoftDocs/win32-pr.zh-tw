---
description: 提供解密加密訊息的步驟。
ms.assetid: 6af7dd28-325e-431a-9cdb-109d93af6302
title: 解密資料
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 970f16862bb8c6693b2ff11f519af3f7c412024b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104321039"
---
# <a name="decrypting-data"></a><span data-ttu-id="67840-103">解密資料</span><span class="sxs-lookup"><span data-stu-id="67840-103">Decrypting Data</span></span>

<span data-ttu-id="67840-104">本節提供解密加密訊息的步驟。</span><span class="sxs-lookup"><span data-stu-id="67840-104">This section presents the steps to decrypt an encrypted message.</span></span>

<span data-ttu-id="67840-105">**解密加密的訊息**</span><span class="sxs-lookup"><span data-stu-id="67840-105">**To decrypt an encrypted message**</span></span>

1.  <span data-ttu-id="67840-106">取得數位封包訊息的指標。</span><span class="sxs-lookup"><span data-stu-id="67840-106">Get a pointer to the digitally enveloped message.</span></span>
2.  <span data-ttu-id="67840-107">開啟憑證存放區。</span><span class="sxs-lookup"><span data-stu-id="67840-107">Open a certificate store.</span></span>
3.  <span data-ttu-id="67840-108">從訊息中，取出 (My ID) 的收件者識別碼。</span><span class="sxs-lookup"><span data-stu-id="67840-108">From the message, retrieve the recipient identifier (My ID).</span></span>
4.  <span data-ttu-id="67840-109">使用收件者識別碼來取得憑證。</span><span class="sxs-lookup"><span data-stu-id="67840-109">Use the recipient identifier to retrieve the certificate.</span></span>
5.  <span data-ttu-id="67840-110">取得憑證的私密金鑰。</span><span class="sxs-lookup"><span data-stu-id="67840-110">Get the private key for the certificate.</span></span>
6.  <span data-ttu-id="67840-111">使用私密金鑰來解密對稱式 (會話) 金鑰。</span><span class="sxs-lookup"><span data-stu-id="67840-111">Use the private key to decrypt the symmetric (session) key.</span></span>
7.  <span data-ttu-id="67840-112">從訊息中取出加密演算法。</span><span class="sxs-lookup"><span data-stu-id="67840-112">Retrieve the encryption algorithm from the message.</span></span>
8.  <span data-ttu-id="67840-113">使用解密的工作階段金鑰和加密演算法，解密資料。</span><span class="sxs-lookup"><span data-stu-id="67840-113">Using the decrypted session key and the encryption algorithm, decrypt the data.</span></span>

<span data-ttu-id="67840-114">[**CryptDecryptMessage**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptdecryptmessage) 會進行解密訊息的所有工作;不過，仍需要初始化結構和其他資料。</span><span class="sxs-lookup"><span data-stu-id="67840-114">[**CryptDecryptMessage**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptdecryptmessage) does all of the tasks for decrypting a message; however, initialization of structures and other data is still necessary.</span></span>

<span data-ttu-id="67840-115">**使用 CryptDecryptMessage 解密資料**</span><span class="sxs-lookup"><span data-stu-id="67840-115">**To decrypt data using CryptDecryptMessage**</span></span>

1.  <span data-ttu-id="67840-116">取得加密 BLOB 的指標。</span><span class="sxs-lookup"><span data-stu-id="67840-116">Get a pointer to the encrypted BLOB.</span></span>
2.  <span data-ttu-id="67840-117">開啟憑證存放區。</span><span class="sxs-lookup"><span data-stu-id="67840-117">Open a certificate store.</span></span>
3.  <span data-ttu-id="67840-118">建立憑證存放區陣列。</span><span class="sxs-lookup"><span data-stu-id="67840-118">Create a certificate store array.</span></span>
4.  <span data-ttu-id="67840-119">將 [**CRYPT \_ 解密訊息 \_ 的 \_ 段落**](/windows/desktop/api/Wincrypt/ns-wincrypt-crypt_decrypt_message_para) 結構初始化。</span><span class="sxs-lookup"><span data-stu-id="67840-119">Initialize the [**CRYPT\_DECRYPT\_MESSAGE\_PARA**](/windows/desktop/api/Wincrypt/ns-wincrypt-crypt_decrypt_message_para) structure.</span></span>
5.  <span data-ttu-id="67840-120">呼叫 [**CryptDecryptMessage**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptdecryptmessage) 來解密訊息中包含的資料。</span><span class="sxs-lookup"><span data-stu-id="67840-120">Call [**CryptDecryptMessage**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptdecryptmessage) to decrypt the data contained in the message.</span></span>

<span data-ttu-id="67840-121">[範例 C 程式：使用 CryptEncryptMessage 和 CryptDecryptMessage 會執行](example-c-program-using-cryptencryptmessage-and-cryptdecryptmessage.md) 剛剛呈現的程式。</span><span class="sxs-lookup"><span data-stu-id="67840-121">[Example C Program: Using CryptEncryptMessage and CryptDecryptMessage](example-c-program-using-cryptencryptmessage-and-cryptdecryptmessage.md) implements the procedure just presented.</span></span> <span data-ttu-id="67840-122">批註會顯示哪些程式碼元素完成程式中的每個步驟。</span><span class="sxs-lookup"><span data-stu-id="67840-122">Comments show which code elements accomplish each step in the procedure.</span></span> <span data-ttu-id="67840-123">如需有關函數的詳細資訊，請參閱 [**CryptDecryptMessage**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptdecryptmessage)，如需有關資料結構的詳細資訊，請參閱 [**CRYPT \_ 解密 \_ 訊息 \_ 段落**](/windows/desktop/api/Wincrypt/ns-wincrypt-crypt_decrypt_message_para)。</span><span class="sxs-lookup"><span data-stu-id="67840-123">For details about the function, see [**CryptDecryptMessage**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptdecryptmessage), and for details about the data structure, see [**CRYPT\_DECRYPT\_MESSAGE\_PARA**](/windows/desktop/api/Wincrypt/ns-wincrypt-crypt_decrypt_message_para).</span></span>

 

 



