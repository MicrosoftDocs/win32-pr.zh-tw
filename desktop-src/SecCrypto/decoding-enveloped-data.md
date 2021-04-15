---
description: 解碼封包訊息所需的一般工作。
ms.assetid: cb71ea3a-0edd-4d46-8088-a395fab89d2b
title: 解碼封包資料
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dc1a0ba12e967f5a0cd56347c0839ce9fca40f02
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104561057"
---
# <a name="decoding-enveloped-data"></a><span data-ttu-id="2b638-103">解碼封包資料</span><span class="sxs-lookup"><span data-stu-id="2b638-103">Decoding Enveloped Data</span></span>

<span data-ttu-id="2b638-104">下圖說明解碼封包訊息所需的一般工作，並在後面的清單中加以說明。</span><span class="sxs-lookup"><span data-stu-id="2b638-104">The general tasks required to decode an enveloped message are depicted in the following illustration and described in the list that follows it.</span></span>

![解碼封包資料](images/decemsg.png)

<span data-ttu-id="2b638-106">使用金鑰傳輸金鑰管理來解碼封包資料的事件順序（如上圖所示）如下所示：</span><span class="sxs-lookup"><span data-stu-id="2b638-106">The sequence of events for decoding enveloped data using key transport key management, as depicted in the previous illustration, is as follows:</span></span>

-   <span data-ttu-id="2b638-107">已抓取 [*數位封包*](../secgloss/d-gly.md) 訊息的指標。</span><span class="sxs-lookup"><span data-stu-id="2b638-107">A pointer to the [*digitally enveloped*](../secgloss/d-gly.md) message is retrieved.</span></span>
-   <span data-ttu-id="2b638-108">即會開啟 [*憑證存放區*](../secgloss/c-gly.md) 。</span><span class="sxs-lookup"><span data-stu-id="2b638-108">A [*certificate store*](../secgloss/c-gly.md) is opened.</span></span>
-   <span data-ttu-id="2b638-109">從訊息中，會抓取收件者識別碼 (我的識別碼) 。</span><span class="sxs-lookup"><span data-stu-id="2b638-109">From the message, the recipient ID (My ID) is retrieved.</span></span>
-   <span data-ttu-id="2b638-110">收件者識別碼用來取得憑證。</span><span class="sxs-lookup"><span data-stu-id="2b638-110">The recipient ID is used to retrieve the certificate.</span></span>
-   <span data-ttu-id="2b638-111">已抓取與該憑證相關聯的 [*私密金鑰*](../secgloss/p-gly.md) 。</span><span class="sxs-lookup"><span data-stu-id="2b638-111">The [*private key*](../secgloss/p-gly.md) associated with that certificate is retrieved.</span></span>
-   <span data-ttu-id="2b638-112">私密金鑰用來將 [*對稱*](../secgloss/s-gly.md) 式 ([*會話*](../secgloss/s-gly.md)) 機碼解密。</span><span class="sxs-lookup"><span data-stu-id="2b638-112">The private key is used to decrypt the [*symmetric*](../secgloss/s-gly.md) ([*session*](../secgloss/s-gly.md)) key.</span></span>
-   <span data-ttu-id="2b638-113">從訊息中取出加密演算法。</span><span class="sxs-lookup"><span data-stu-id="2b638-113">The encryption algorithm is retrieved from the message.</span></span>
-   <span data-ttu-id="2b638-114">使用私密金鑰和加密演算法可解密資料。</span><span class="sxs-lookup"><span data-stu-id="2b638-114">Using the private key and encryption algorithm, the data is decrypted.</span></span>

<span data-ttu-id="2b638-115">下列程式使用低層級的訊息函式來完成剛剛列出的工作。</span><span class="sxs-lookup"><span data-stu-id="2b638-115">The following procedure uses low-level message functions to accomplish the tasks just listed.</span></span>

<span data-ttu-id="2b638-116">**解碼封包訊息**</span><span class="sxs-lookup"><span data-stu-id="2b638-116">**To decode an enveloped message**</span></span>

1.  <span data-ttu-id="2b638-117">取得編碼 BLOB 的指標。</span><span class="sxs-lookup"><span data-stu-id="2b638-117">Get a pointer to the encoded BLOB.</span></span>
2.  <span data-ttu-id="2b638-118">呼叫 [**CryptMsgOpenToDecode**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsgopentodecode)，傳遞必要的引數。</span><span class="sxs-lookup"><span data-stu-id="2b638-118">Call [**CryptMsgOpenToDecode**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsgopentodecode), passing the necessary arguments.</span></span>
3.  <span data-ttu-id="2b638-119">呼叫 [**CryptMsgUpdate**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsgupdate) 一次，並傳入步驟2中抓取的控制碼，以及要解碼之資料的指標。</span><span class="sxs-lookup"><span data-stu-id="2b638-119">Call [**CryptMsgUpdate**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsgupdate) once, passing in the handle retrieved in step 2 and a pointer to the data that is to be decoded.</span></span> <span data-ttu-id="2b638-120">這會根據訊息類型，對訊息採取適當的動作。</span><span class="sxs-lookup"><span data-stu-id="2b638-120">This causes the appropriate actions to be taken on the message, depending on the message type.</span></span>
4.  <span data-ttu-id="2b638-121">呼叫 [**CryptMsgGetParam**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsggetparam)，傳入在步驟2和 CMSG 類型參數中抓取的控制碼， \_ \_ 以驗證訊息是否為封包資料類型。</span><span class="sxs-lookup"><span data-stu-id="2b638-121">Call [**CryptMsgGetParam**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsggetparam), passing in the handle retrieved in step 2 and CMSG\_TYPE\_PARAM to verify that the message is of the enveloped data type.</span></span>
5.  <span data-ttu-id="2b638-122">再次呼叫 [**CryptMsgGetParam**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsggetparam)，傳入 CMSG \_ 內部 \_ 內容 \_ 類型參數， \_ 以取得 [*內部內容*](../secgloss/i-gly.md)的資料類型。</span><span class="sxs-lookup"><span data-stu-id="2b638-122">Again call [**CryptMsgGetParam**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsggetparam), passing in CMSG\_INNER\_CONTENT\_TYPE\_PARAM to get the data type of the [*inner content*](../secgloss/i-gly.md).</span></span>
6.  <span data-ttu-id="2b638-123">如果內部內容資料類型是 **資料**，請繼續解密並解碼內容。</span><span class="sxs-lookup"><span data-stu-id="2b638-123">If the inner content data type is **data**, proceed to decrypt and decode the content.</span></span> <span data-ttu-id="2b638-124">否則，請執行適用于內容資料類型的解碼程式。</span><span class="sxs-lookup"><span data-stu-id="2b638-124">Otherwise, run a decoding procedure appropriate for the content data type.</span></span>
7.  <span data-ttu-id="2b638-125">假設內部內容類型是 "data"，請將 [**CMSG \_ ctrl \_ 解密 \_ 段落**](/windows/desktop/api/Wincrypt/ns-wincrypt-cmsg_ctrl_decrypt_para) 資料結構和呼叫 [**CryptMsgControl**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsgcontrol)，並傳入 CMSG \_ ctrl \_ 解密和結構位址。</span><span class="sxs-lookup"><span data-stu-id="2b638-125">Assuming the inner content type is "data", initialize the [**CMSG\_CTRL\_DECRYPT\_PARA**](/windows/desktop/api/Wincrypt/ns-wincrypt-cmsg_ctrl_decrypt_para) data structure, and call [**CryptMsgControl**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsgcontrol), passing in CMSG\_CTRL\_DECRYPT and the address of the structure.</span></span> <span data-ttu-id="2b638-126">將會解密內容。</span><span class="sxs-lookup"><span data-stu-id="2b638-126">The content will be decrypted.</span></span>
8.  <span data-ttu-id="2b638-127">呼叫 [**CryptMsgGetParam**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsggetparam)，傳入 CMSG \_ content \_ PARAM 以取得已解碼內容資料 BLOB 的指標， (**位元組** 字串) 。</span><span class="sxs-lookup"><span data-stu-id="2b638-127">Call [**CryptMsgGetParam**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsggetparam), passing in CMSG\_CONTENT\_PARAM to get a pointer to the decoded content data BLOB (**BYTE** string).</span></span>
9.  <span data-ttu-id="2b638-128">呼叫 [**CryptMsgClose**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsgclose) 以關閉訊息。</span><span class="sxs-lookup"><span data-stu-id="2b638-128">Call [**CryptMsgClose**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsgclose) to close the message.</span></span>

<span data-ttu-id="2b638-129">此程式的結果是會將訊息解碼和解密，並將指標取出至內容資料 BLOB。</span><span class="sxs-lookup"><span data-stu-id="2b638-129">The result of this procedure is that the message is decoded and decrypted and a pointer is retrieved to the content data BLOB.</span></span>

## <a name="related-topics"></a><span data-ttu-id="2b638-130">相關主題</span><span class="sxs-lookup"><span data-stu-id="2b638-130">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2b638-131">範例 C 程式：編碼封包、簽署的訊息</span><span class="sxs-lookup"><span data-stu-id="2b638-131">Example C Program: Encoding an Enveloped, Signed Message</span></span>](example-c-program-encoding-an-enveloped-signed-message.md)
</dt> </dl>

 

 
