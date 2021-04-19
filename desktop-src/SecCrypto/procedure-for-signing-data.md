---
description: 顯示這些函式參數之間的關聯性，這些參數會指向結構或陣列與其初始化的資料。
ms.assetid: 89caf4d3-727f-472b-9a09-e81b4ff4d127
title: 簽署資料的程式
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ba289928ab39c690e1c44bdbf65c77c18b7edab3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "107001722"
---
# <a name="procedure-for-signing-data"></a><span data-ttu-id="067f2-103">簽署資料的程式</span><span class="sxs-lookup"><span data-stu-id="067f2-103">Procedure for Signing Data</span></span>

<span data-ttu-id="067f2-104">單一函式 [**CryptSignMessage**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptsignmessage)會執行 [建立簽署訊息](creating-a-signed-message.md)中列出的所有工作。</span><span class="sxs-lookup"><span data-stu-id="067f2-104">A single function, [**CryptSignMessage**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptsignmessage), performs all of the tasks listed in [Creating a Signed Message](creating-a-signed-message.md).</span></span> <span data-ttu-id="067f2-105">不過，仍需要初始化結構和其他資料。</span><span class="sxs-lookup"><span data-stu-id="067f2-105">However, initialization of structures and other data is still necessary.</span></span> <span data-ttu-id="067f2-106">下圖顯示這些函式參數之間的關聯性，這些參數會指向結構或陣列與其初始化的資料。</span><span class="sxs-lookup"><span data-stu-id="067f2-106">The following illustration shows the relationship between those function parameters that point to structures or arrays and their initialized data.</span></span> <span data-ttu-id="067f2-107">下圖只會顯示衍生自其他結構或函數的函式參數和結構成員。</span><span class="sxs-lookup"><span data-stu-id="067f2-107">The illustration shows only the function parameters and structure members that are derived from other structures or functions.</span></span> <span data-ttu-id="067f2-108">其餘的參數都是直接初始化。</span><span class="sxs-lookup"><span data-stu-id="067f2-108">The rest of the parameters are straightforward initializations.</span></span>

![呼叫 cryptsignmessage 的初始化對應](images/crypsign.png)

<span data-ttu-id="067f2-110">**使用 CryptSignMessage 簽署資料**</span><span class="sxs-lookup"><span data-stu-id="067f2-110">**To sign data using CryptSignMessage**</span></span>

1.  <span data-ttu-id="067f2-111">取得要簽署之資料的指標。</span><span class="sxs-lookup"><span data-stu-id="067f2-111">Get a pointer to the data that is to be signed.</span></span>
2.  <span data-ttu-id="067f2-112">將資料指標指派給「要簽署的資料」陣列中的索引零。</span><span class="sxs-lookup"><span data-stu-id="067f2-112">Assign the pointer to the data to index zero of a "data to be signed" array.</span></span>
3.  <span data-ttu-id="067f2-113">取得密碼編譯提供者的控制碼。</span><span class="sxs-lookup"><span data-stu-id="067f2-113">Get a handle to the cryptographic provider.</span></span>
4.  <span data-ttu-id="067f2-114">開啟包含簽署者憑證的 [*憑證存放區*](../secgloss/c-gly.md) 。</span><span class="sxs-lookup"><span data-stu-id="067f2-114">Open a [*certificate store*](../secgloss/c-gly.md) that contains the signer's certificate.</span></span>
5.  <span data-ttu-id="067f2-115">取得簽署者憑證的位址。</span><span class="sxs-lookup"><span data-stu-id="067f2-115">Get an address to the signer's certificate.</span></span>
6.  <span data-ttu-id="067f2-116">將憑證的位址指派給 *MsgCert* 陣列的零索引。</span><span class="sxs-lookup"><span data-stu-id="067f2-116">Assign the address of the certificate to the zero index of the *MsgCert* array.</span></span>
7.  <span data-ttu-id="067f2-117">指派要包含在 *MsgCert* 陣列中之訊息的任何其他憑證位址。</span><span class="sxs-lookup"><span data-stu-id="067f2-117">Assign the addresses of any other certificates to be included with the message to the *MsgCert* array.</span></span>
8.  <span data-ttu-id="067f2-118">初始化 [**CRYPT \_ 演算法 \_ 識別碼**](/windows/desktop/api/Wincrypt/ns-wincrypt-crypt_algorithm_identifier) 結構，並適當地將 **pszObjId** 成員初始化為所需的雜湊演算法和其他成員。</span><span class="sxs-lookup"><span data-stu-id="067f2-118">Initialize the [**CRYPT\_ALGORITHM\_IDENTIFIER**](/windows/desktop/api/Wincrypt/ns-wincrypt-crypt_algorithm_identifier) structure, initializing the **pszObjId** member to the desired hash algorithm and the other members as appropriate.</span></span>
9.  <span data-ttu-id="067f2-119">初始化 [**CRYPT \_ 簽署訊息 \_ 的 \_ 段落**](/windows/desktop/api/Wincrypt/ns-wincrypt-crypt_sign_message_para)結構、將 pSigningCert 成員初始化為簽署人的憑證位址 **、將** 成員初始化為簽署人的憑證、其他憑證的位址、 **HashAlgorithm** 成員與 [**CRYPT \_ 演算法 \_ 識別碼**](/windows/desktop/api/Wincrypt/ns-wincrypt-crypt_algorithm_identifier)結構的位址，以及其他成員適當的成員。</span><span class="sxs-lookup"><span data-stu-id="067f2-119">Initialize the [**CRYPT\_SIGN\_MESSAGE\_PARA**](/windows/desktop/api/Wincrypt/ns-wincrypt-crypt_sign_message_para) structure, initializing the **pSigningCert** member to the address of the signer's certificate, the **MsgCert** array member to the address of the signer's and other's certificates, the **HashAlgorithm** member to the address of the [**CRYPT\_ALGORITHM\_IDENTIFIER**](/windows/desktop/api/Wincrypt/ns-wincrypt-crypt_algorithm_identifier) structure, and the other members as appropriate.</span></span>
10. <span data-ttu-id="067f2-120">呼叫 [**CryptSignMessage**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptsignmessage)函式，傳遞 *PSignPara* 參數的 [**CRYPT \_ 簽署 \_ 訊息 \_ 段落**](/windows/desktop/api/Wincrypt/ns-wincrypt-crypt_sign_message_para)結構、 *rgpbToBeSigned* 參數的「要簽署的資料」陣列位址、 *pbSignedBlob* 輸出參數的位址，以及適用于其他參數的值。</span><span class="sxs-lookup"><span data-stu-id="067f2-120">Call the [**CryptSignMessage**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptsignmessage) function, passing the [**CRYPT\_SIGN\_MESSAGE\_PARA**](/windows/desktop/api/Wincrypt/ns-wincrypt-crypt_sign_message_para) structure for the *pSignPara* parameter, the address of the "data to be signed" array for the *rgpbToBeSigned* parameter, an address for the *pbSignedBlob* output parameter, and values for the other parameters as appropriate.</span></span>

 

 
