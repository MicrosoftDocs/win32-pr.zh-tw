---
description: 解碼已簽署資料的進程。
ms.assetid: 803220d0-7963-4fc4-8451-a979e54a9cc3
title: 解碼簽署的資料
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fdfd327746c5d0ba8e7089e1c273817b76c16370
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106981134"
---
# <a name="decoding-signed-data"></a><span data-ttu-id="ffd9a-103">解碼簽署的資料</span><span class="sxs-lookup"><span data-stu-id="ffd9a-103">Decoding Signed Data</span></span>

<span data-ttu-id="ffd9a-104">下列一般處理常式會將 [*已簽署的資料*](../secgloss/s-gly.md) 型別解碼。</span><span class="sxs-lookup"><span data-stu-id="ffd9a-104">The following general process decodes a [*signed data*](../secgloss/s-gly.md) type.</span></span>

<span data-ttu-id="ffd9a-105">**解碼已簽署的訊息**</span><span class="sxs-lookup"><span data-stu-id="ffd9a-105">**To decode a signed message**</span></span>

1.  <span data-ttu-id="ffd9a-106">取得編碼 BLOB 的指標。</span><span class="sxs-lookup"><span data-stu-id="ffd9a-106">Get a pointer to the encoded BLOB.</span></span>
2.  <span data-ttu-id="ffd9a-107">呼叫 [**CryptMsgOpenToDecode**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsgopentodecode)，傳遞必要的引數。</span><span class="sxs-lookup"><span data-stu-id="ffd9a-107">Call [**CryptMsgOpenToDecode**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsgopentodecode), passing the necessary arguments.</span></span>
3.  <span data-ttu-id="ffd9a-108">呼叫 [**CryptMsgUpdate**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsgupdate) 一次，並傳入步驟2中抓取的控制碼，以及要解碼之資料的指標。</span><span class="sxs-lookup"><span data-stu-id="ffd9a-108">Call [**CryptMsgUpdate**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsgupdate) once, passing in the handle retrieved in step 2 and a pointer to the data that is to be decoded.</span></span> <span data-ttu-id="ffd9a-109">這會根據訊息類型，對訊息採取適當的動作。</span><span class="sxs-lookup"><span data-stu-id="ffd9a-109">This causes the appropriate actions to be taken on the message, depending on the message type.</span></span>
4.  <span data-ttu-id="ffd9a-110">呼叫 [**CryptMsgGetParam**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsggetparam)，傳入步驟2中抓取的控制碼和適當的參數類型，以存取已解碼的資料。</span><span class="sxs-lookup"><span data-stu-id="ffd9a-110">Call [**CryptMsgGetParam**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsggetparam), passing in the handle retrieved in step 2 and the appropriate parameter types to access the decoded data.</span></span> <span data-ttu-id="ffd9a-111">例如，傳入 CMSG \_ content \_ PARAM 以取得已解碼內容的指標。</span><span class="sxs-lookup"><span data-stu-id="ffd9a-111">For example, pass in CMSG\_CONTENT\_PARAM to get a pointer to the decoded content.</span></span>

<span data-ttu-id="ffd9a-112">下列一般程式會驗證已解碼、已簽署訊息的簽章。</span><span class="sxs-lookup"><span data-stu-id="ffd9a-112">The following general process verifies the signature of a decoded, signed message.</span></span>

<span data-ttu-id="ffd9a-113">**驗證已解碼、已簽署訊息的簽章**</span><span class="sxs-lookup"><span data-stu-id="ffd9a-113">**To verify the signature of a decoded, signed message**</span></span>

1.  <span data-ttu-id="ffd9a-114">呼叫 [**CryptMsgGetParam**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsggetparam)，傳入訊息控制碼和 CMSG \_ 簽署者 \_ cert \_ info \_ 參數，以從訊息取得簽署者的憑證 [**\_ 資訊**](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_info) 。</span><span class="sxs-lookup"><span data-stu-id="ffd9a-114">Call [**CryptMsgGetParam**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsggetparam), passing in the message handle and CMSG\_SIGNER\_CERT\_INFO\_PARAM to get the signer's [**CERT\_INFO**](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_info) from the message.</span></span>
2.  <span data-ttu-id="ffd9a-115">呼叫 [**CertOpenStore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certopenstore) 以開啟使用訊息中的憑證初始化的暫存存放區。</span><span class="sxs-lookup"><span data-stu-id="ffd9a-115">Call [**CertOpenStore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certopenstore) to open a temporary store that is initialized with the certificates from the message.</span></span>
3.  <span data-ttu-id="ffd9a-116">呼叫 [**CertGetSubjectCertificateFromStore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certgetsubjectcertificatefromstore) ，以從訊息中包含的憑證取得簽署者的憑證 [**\_ 資訊**](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_info) 。</span><span class="sxs-lookup"><span data-stu-id="ffd9a-116">Call [**CertGetSubjectCertificateFromStore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certgetsubjectcertificatefromstore) to get the signer's [**CERT\_INFO**](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_info) from the certificates included in the message.</span></span>
4.  <span data-ttu-id="ffd9a-117">呼叫 [**CryptMsgControl**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsgcontrol)，傳入 CMSG \_ CTRL 驗證簽章 \_ \_ 來驗證簽章。</span><span class="sxs-lookup"><span data-stu-id="ffd9a-117">Call [**CryptMsgControl**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsgcontrol), passing in CMSG\_CTRL\_VERIFY\_SIGNATURE to verify the signatures.</span></span>
5.  <span data-ttu-id="ffd9a-118">呼叫 [**CryptMsgClose**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsgclose) 以關閉訊息。</span><span class="sxs-lookup"><span data-stu-id="ffd9a-118">Call [**CryptMsgClose**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsgclose) to close the message.</span></span>

<span data-ttu-id="ffd9a-119">這些程式的結果是簽章經過驗證，而且會將指標抓取至在程式的步驟4中取得的解碼訊息內容，以解碼已簽署的訊息。</span><span class="sxs-lookup"><span data-stu-id="ffd9a-119">The result of these procedures is that the signature is verified and a pointer is retrieved to the decoded message content obtained in step 4 of the procedure for decoding a signed message.</span></span>

<span data-ttu-id="ffd9a-120">如需 C 編碼的詳細資料，請參閱 [c 程式範例：簽署、編碼、解碼和驗證訊息](example-c-program-signing-encoding-decoding-and-verifying-a-message.md)。</span><span class="sxs-lookup"><span data-stu-id="ffd9a-120">For C coding details, see [Example C Program: Signing, Encoding, Decoding, and Verifying a Message](example-c-program-signing-encoding-decoding-and-verifying-a-message.md).</span></span>

 

 
