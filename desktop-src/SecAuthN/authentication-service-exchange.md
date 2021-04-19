---
description: 使用者可以輸入登入名稱和密碼來開始登入網路。 使用者工作站上的 Kerberos 用戶端會將密碼轉換為加密金鑰，並將結果儲存在程式變數中。
ms.assetid: fcb3b601-9953-474c-9a08-1fa25706f3d7
title: 驗證服務交換
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c14121ed33ae0ac169c590b03dfb0b395306d11f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106987636"
---
# <a name="authentication-service-exchange"></a><span data-ttu-id="0b831-104">驗證服務交換</span><span class="sxs-lookup"><span data-stu-id="0b831-104">Authentication Service Exchange</span></span>

<span data-ttu-id="0b831-105">使用者可以輸入登入名稱和密碼來開始登入網路。</span><span class="sxs-lookup"><span data-stu-id="0b831-105">The user begins logging on to the network by typing a logon name and password.</span></span> <span data-ttu-id="0b831-106">使用者工作站上的 [*Kerberos*](/windows/desktop/SecGloss/k-gly) 用戶端會將密碼轉換為加密金鑰，並將結果儲存在程式變數中。</span><span class="sxs-lookup"><span data-stu-id="0b831-106">The [*Kerberos*](/windows/desktop/SecGloss/k-gly) client on the user's workstation converts the password to an encryption key and saves the result in a program variable.</span></span>

<span data-ttu-id="0b831-107">接著，用戶端[](/windows/desktop/SecGloss/c-gly)會透過將 KRB 型別為「 [](/windows/desktop/SecGloss/k-gly) \_ \_ 要求) Kerberos 驗證服務要求 (」的訊息傳送給 kdc 的驗證服務，以要求金鑰發佈中心 (KDC) 的 (TGS) 的票證授與服務的認證。</span><span class="sxs-lookup"><span data-stu-id="0b831-107">The client then requests [*credentials*](/windows/desktop/SecGloss/c-gly) for the ticket-granting service (TGS) of the [*Key Distribution Center*](/windows/desktop/SecGloss/k-gly) (KDC) by sending the KDC's authentication service a message of type KRB\_AS\_REQ (Kerberos Authentication Service Request).</span></span> <span data-ttu-id="0b831-108">此訊息的第一個部分會識別所要求的使用者和 TGS 服務。</span><span class="sxs-lookup"><span data-stu-id="0b831-108">The first part of this message identifies the user and the TGS service being requested.</span></span> <span data-ttu-id="0b831-109">此訊息的第二個部分包含預先驗證的資料，目的在於證明使用者知道密碼。</span><span class="sxs-lookup"><span data-stu-id="0b831-109">The second part of this message contains preauthentication data intended to prove that the user knows the password.</span></span> <span data-ttu-id="0b831-110">這只是使用衍生自使用者登入密碼的 [*主要金鑰*](/windows/desktop/SecGloss/m-gly) 加密的驗證器訊息。</span><span class="sxs-lookup"><span data-stu-id="0b831-110">This is simply an authenticator message that is encrypted with the [*master key*](/windows/desktop/SecGloss/m-gly) derived from the user's logon password.</span></span>

<span data-ttu-id="0b831-111">當 KDC 以要求的形式接收 KRB 時， \_ \_ 它會在其資料庫中尋找使用者、取得相關聯使用者的主要金鑰、解密預先驗證資料，並評估內的時間戳記。</span><span class="sxs-lookup"><span data-stu-id="0b831-111">When the KDC receives KRB\_AS\_REQ, it looks up the user in its database, gets the associated user's master key, decrypts the preauthentication data, and evaluates the time stamp inside.</span></span> <span data-ttu-id="0b831-112">如果時間戳記有效，KDC 可以確保預先驗證資料是以使用者的主要金鑰加密，因此用戶端為正版。</span><span class="sxs-lookup"><span data-stu-id="0b831-112">If the time stamp is valid, the KDC can be assured that the preauthentication data was encrypted with the user's master key and thus that the client is genuine.</span></span>

<span data-ttu-id="0b831-113">在 KDC 驗證使用者的身分識別之後，它會建立用戶端可以出示給 TGS 的認證，如下所示：</span><span class="sxs-lookup"><span data-stu-id="0b831-113">After the KDC has verified the user's identity, it creates credentials that the client can present to the TGS, as follows:</span></span>

1.  <span data-ttu-id="0b831-114">KDC 會 invents 登入 [*工作階段金鑰*](/windows/desktop/SecGloss/s-gly) ，並使用使用者的主要金鑰來加密複本。</span><span class="sxs-lookup"><span data-stu-id="0b831-114">The KDC invents a logon [*session key*](/windows/desktop/SecGloss/s-gly) and encrypts a copy with the user's master key.</span></span>
2.  <span data-ttu-id="0b831-115">KDC 會將登入工作階段金鑰的另一份複本和使用者的授權資料內嵌在票證授與票證 (TGT) ，並使用 KDC 本身的主要金鑰來加密 TGT。</span><span class="sxs-lookup"><span data-stu-id="0b831-115">The KDC embeds another copy of the logon session key and the user's authorization data in a ticket-granting ticket (TGT), and encrypts the TGT with the KDC's own master key.</span></span>
3.  <span data-ttu-id="0b831-116">KDC 會以 KRB 類型的訊息來回複，將這些認證傳送回用戶端 \_ ， \_ (Kerberos 驗證服務回復) 。</span><span class="sxs-lookup"><span data-stu-id="0b831-116">The KDC sends these credentials back to the client by replying with a message of type KRB\_AS\_REP (Kerberos Authentication Service Reply).</span></span>
4.  <span data-ttu-id="0b831-117">當用戶端收到回復時，會使用從使用者的密碼衍生的金鑰來解密新的登入工作階段金鑰。</span><span class="sxs-lookup"><span data-stu-id="0b831-117">When the client receives the reply, it uses the key derived from the user's password to decrypt the new logon session key.</span></span>
5.  <span data-ttu-id="0b831-118">用戶端會將新的金鑰儲存在其票證快取中。</span><span class="sxs-lookup"><span data-stu-id="0b831-118">The client stores the new key in its ticket cache.</span></span>
6.  <span data-ttu-id="0b831-119">用戶端也會從訊息中解壓縮 TGT，並將其儲存在其票證快取中。</span><span class="sxs-lookup"><span data-stu-id="0b831-119">The client extracts the TGT from the message and stores that in its ticket cache as well.</span></span>

 

 
