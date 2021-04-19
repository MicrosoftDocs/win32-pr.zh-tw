---
description: 說明如何使用 CryptMsgVerifyCountersignatureEncoded 來驗證副署。
ms.assetid: b7be0d4c-338f-4319-bd82-5cf3d158d6fe
title: 驗證副署
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 711e15388144fbf674cbb0c42ff41883edbb5af0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "107001683"
---
# <a name="verifying-a-countersignature"></a><span data-ttu-id="da220-103">驗證副署</span><span class="sxs-lookup"><span data-stu-id="da220-103">Verifying a Countersignature</span></span>

<span data-ttu-id="da220-104">**驗證副署**</span><span class="sxs-lookup"><span data-stu-id="da220-104">**To verify a countersignature**</span></span>

1.  <span data-ttu-id="da220-105">呼叫 [**CryptMsgOpenToDecode**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsgopentodecode) 以取得已簽署訊息的控制碼。</span><span class="sxs-lookup"><span data-stu-id="da220-105">Call [**CryptMsgOpenToDecode**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsgopentodecode) to get a handle to the signed message.</span></span>
2.  <span data-ttu-id="da220-106">取得 countersigner 憑證 ( [**CERT \_ 資訊**](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_info)) 的指標。</span><span class="sxs-lookup"><span data-stu-id="da220-106">Get a pointer to the countersigner's certificate ( [**CERT\_INFO**](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_info)).</span></span>
3.  <span data-ttu-id="da220-107">呼叫 [**CryptMsgGetParam**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsggetparam) 以從訊息中取出簽署者資訊。</span><span class="sxs-lookup"><span data-stu-id="da220-107">Call [**CryptMsgGetParam**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsggetparam) to retrieve the signer information from the message.</span></span>
4.  <span data-ttu-id="da220-108">呼叫 [**CryptMsgGetParam**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsggetparam) 以從訊息中取出 [*副署*](../secgloss/c-gly.md) 。</span><span class="sxs-lookup"><span data-stu-id="da220-108">Call [**CryptMsgGetParam**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsggetparam) to retrieve the [*countersignature*](../secgloss/c-gly.md) from the message.</span></span>
5.  <span data-ttu-id="da220-109">呼叫 [**CryptMsgVerifyCountersignatureEncoded**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsgverifycountersignatureencoded) 來驗證副署。</span><span class="sxs-lookup"><span data-stu-id="da220-109">Call [**CryptMsgVerifyCountersignatureEncoded**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsgverifycountersignatureencoded) to verify the countersignature.</span></span>

<span data-ttu-id="da220-110">如果 [**CryptMsgVerifyCountersignatureEncoded**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsgverifycountersignatureencoded) 函式呼叫成功，則會驗證 [*副署*](../secgloss/c-gly.md) 。</span><span class="sxs-lookup"><span data-stu-id="da220-110">If the [**CryptMsgVerifyCountersignatureEncoded**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsgverifycountersignatureencoded) function call succeeds, the [*countersignature*](../secgloss/c-gly.md) is verified.</span></span>

 

 
