---
description: 說明如何使用 CryptMsgCountersign 來對訊息進行副署。
ms.assetid: e1969b43-f50e-4c7d-a7e5-b22db4e05be2
title: Countersigning 訊息
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 02091d25e7ee22f986a26b8f07abff68ebb8c11c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106980520"
---
# <a name="countersigning-a-message"></a><span data-ttu-id="31d30-103">Countersigning 訊息</span><span class="sxs-lookup"><span data-stu-id="31d30-103">Countersigning a Message</span></span>

<span data-ttu-id="31d30-104">**若要使用 CryptMsgCountersign 來副署已簽署的訊息**</span><span class="sxs-lookup"><span data-stu-id="31d30-104">**To countersign a signed message by using CryptMsgCountersign**</span></span>

1.  <span data-ttu-id="31d30-105">呼叫 [**CryptMsgOpenToDecode**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsgopentodecode) 以取得已簽署訊息的控制碼。</span><span class="sxs-lookup"><span data-stu-id="31d30-105">Call [**CryptMsgOpenToDecode**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsgopentodecode) to get a handle to the signed message.</span></span>
2.  <span data-ttu-id="31d30-106">初始化 countersigner 的 [**CMSG \_ 簽署者 \_ 編碼 \_ 資訊**](/windows/desktop/api/Wincrypt/ns-wincrypt-cmsg_signer_encode_info) 結構。</span><span class="sxs-lookup"><span data-stu-id="31d30-106">Initialize a [**CMSG\_SIGNER\_ENCODE\_INFO**](/windows/desktop/api/Wincrypt/ns-wincrypt-cmsg_signer_encode_info) structure for the countersigner.</span></span>
3.  <span data-ttu-id="31d30-107">將 [**CMSG \_ 簽署者 \_ 編碼 \_ 資訊**](/windows/desktop/api/Wincrypt/ns-wincrypt-cmsg_signer_encode_info) 結構新增至 countersigners 的陣列 () 目前只支援一個 countersigner。</span><span class="sxs-lookup"><span data-stu-id="31d30-107">Add the [**CMSG\_SIGNER\_ENCODE\_INFO**](/windows/desktop/api/Wincrypt/ns-wincrypt-cmsg_signer_encode_info) structure to an array of countersigners (only one countersigner is currently supported).</span></span>
4.  <span data-ttu-id="31d30-108">呼叫 [**CryptMsgCountersign**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsgcountersign) 以新增副署或副署。</span><span class="sxs-lookup"><span data-stu-id="31d30-108">Call [**CryptMsgCountersign**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsgcountersign) to add the countersignature or countersignatures.</span></span>

<span data-ttu-id="31d30-109">如果所有的函式呼叫都成功，則原始訊息現在會以未驗證的屬性包含 [*副署*](../secgloss/c-gly.md) 。</span><span class="sxs-lookup"><span data-stu-id="31d30-109">If all of the function calls succeed, the original message now has a [*countersignature*](../secgloss/c-gly.md) included as an unauthenticated attribute.</span></span>

<span data-ttu-id="31d30-110">**若要使用 CryptMsgCountersignEncoded 來副署已簽署的訊息**</span><span class="sxs-lookup"><span data-stu-id="31d30-110">**To countersign a signed message by using CryptMsgCountersignEncoded**</span></span>

1.  <span data-ttu-id="31d30-111">呼叫 [**CryptMsgOpenToDecode**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsgopentodecode) 以取得已簽署訊息的控制碼。</span><span class="sxs-lookup"><span data-stu-id="31d30-111">Call [**CryptMsgOpenToDecode**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsgopentodecode) to get a handle to the signed message.</span></span>
2.  <span data-ttu-id="31d30-112">呼叫 [**CryptMsgGetParam**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsggetparam) 以取得已簽署訊息的編碼簽署者資訊。</span><span class="sxs-lookup"><span data-stu-id="31d30-112">Call [**CryptMsgGetParam**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsggetparam) to retrieve the encoded signer information of the signed message.</span></span>
3.  <span data-ttu-id="31d30-113">初始化 countersigner 的 [**CMSG \_ 簽署者 \_ 編碼 \_ 資訊**](/windows/desktop/api/Wincrypt/ns-wincrypt-cmsg_signer_encode_info) 結構。</span><span class="sxs-lookup"><span data-stu-id="31d30-113">Initialize a [**CMSG\_SIGNER\_ENCODE\_INFO**](/windows/desktop/api/Wincrypt/ns-wincrypt-cmsg_signer_encode_info) structure for the countersigner.</span></span>
4.  <span data-ttu-id="31d30-114">將 [**CMSG \_ 簽署者 \_ 編碼 \_ 資訊**](/windows/desktop/api/Wincrypt/ns-wincrypt-cmsg_signer_encode_info) 結構新增至 countersigners 的陣列 () 目前只支援一個 countersigner。</span><span class="sxs-lookup"><span data-stu-id="31d30-114">Add the [**CMSG\_SIGNER\_ENCODE\_INFO**](/windows/desktop/api/Wincrypt/ns-wincrypt-cmsg_signer_encode_info) structure to an array of countersigners (only one countersigner is currently supported).</span></span>
5.  <span data-ttu-id="31d30-115">呼叫 [**CryptMsgCountersignEncoded**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsgcountersignencoded) 來建立編碼的副署屬性。</span><span class="sxs-lookup"><span data-stu-id="31d30-115">Call [**CryptMsgCountersignEncoded**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsgcountersignencoded) to create the encoded countersignature attribute.</span></span>
6.  <span data-ttu-id="31d30-116">呼叫 [**CryptMsgControl**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsgcontrol) 將副署屬性新增至原始訊息作為未驗證的屬性。</span><span class="sxs-lookup"><span data-stu-id="31d30-116">Call [**CryptMsgControl**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsgcontrol) to add the countersignature attribute to the original message as an unauthenticated attribute.</span></span>

<span data-ttu-id="31d30-117">如果所有函式呼叫都成功，則會將 [*副署*](../secgloss/c-gly.md) 屬性新增至原始訊息。</span><span class="sxs-lookup"><span data-stu-id="31d30-117">If all of the function calls succeed, a [*countersignature*](../secgloss/c-gly.md) attribute is added to the original message.</span></span>

 

 
