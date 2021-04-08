---
description: 當伺服器收到來自用戶端的挑戰回應時，就會進行初始驗證。
ms.assetid: 8a5cf26b-0b2a-4f19-807b-9ec4d533cdd4
title: 使用 Microsoft Digest 的初始驗證
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8ed4960d947bbc60df962e6a9b71be755e158c8e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103851744"
---
# <a name="initial-authentication-using-microsoft-digest"></a><span data-ttu-id="51bac-103">使用 Microsoft Digest 的初始驗證</span><span class="sxs-lookup"><span data-stu-id="51bac-103">Initial Authentication Using Microsoft Digest</span></span>

<span data-ttu-id="51bac-104">當伺服器收到來自用戶端的挑戰回應時，就會進行初始驗證。</span><span class="sxs-lookup"><span data-stu-id="51bac-104">The initial authentication takes place when the server receives a challenge response from a client.</span></span> <span data-ttu-id="51bac-105">驗證挑戰回應通常牽涉到至少兩部伺服器：</span><span class="sxs-lookup"><span data-stu-id="51bac-105">Authenticating a challenge response typically involves a minimum of two servers:</span></span>

-   <span data-ttu-id="51bac-106">源伺服器-接收來自用戶端的要求併發出挑戰，然後從必須驗證的用戶端收到挑戰回應。</span><span class="sxs-lookup"><span data-stu-id="51bac-106">The originating server—receives the request from the client and issues a challenge, and then receives the challenge response from the client which must be authenticated.</span></span>
-   <span data-ttu-id="51bac-107">驗證服務器-接收來自源伺服器的授權資訊，並執行驗證。</span><span class="sxs-lookup"><span data-stu-id="51bac-107">The authenticating server—receives authorization information from the originating server, and performs the authentication.</span></span> <span data-ttu-id="51bac-108">此伺服器通常是支援多個來源伺服器的網域控制站。</span><span class="sxs-lookup"><span data-stu-id="51bac-108">This server is typically a domain controller that supports multiple originating servers.</span></span>

<span data-ttu-id="51bac-109">當源伺服器收到包含摘要挑戰回應的授權標頭要求時，驗證會依照下列方式繼續進行：</span><span class="sxs-lookup"><span data-stu-id="51bac-109">When the originating server receives a request with an Authorization header containing a Digest challenge response, the authentication proceeds as follows:</span></span>

-   <span data-ttu-id="51bac-110">源伺服器的身分識別是針對挑戰的 nonce 所編碼的伺服器進行檢查。</span><span class="sxs-lookup"><span data-stu-id="51bac-110">The identity of the originating server is checked against the server encoded in the challenge's nonce.</span></span>
-   <span data-ttu-id="51bac-111">已檢查 nonce 中編碼的時間戳記。</span><span class="sxs-lookup"><span data-stu-id="51bac-111">The time stamp encoded in the nonce is checked.</span></span> <span data-ttu-id="51bac-112">如果 nonce 已過期，且使用者名稱/密碼資訊有效，則原始伺服器會發出新的摘要挑戰，並將過時的指示詞設為 "true"，藉此結束驗證。</span><span class="sxs-lookup"><span data-stu-id="51bac-112">If the nonce has expired and the user name/password information is valid, the originating server ends the authentication by issuing a new Digest challenge with the stale directive set to "true".</span></span> <span data-ttu-id="51bac-113">這表示只有 nonce 「過時」，且用戶端可以使用先前回應中使用的密碼來回應新的挑戰。</span><span class="sxs-lookup"><span data-stu-id="51bac-113">This indicates that only the nonce was "stale" and the client can respond to the new challenge using the password it used in the previous response.</span></span> <span data-ttu-id="51bac-114">如果用戶端在傳送過時挑戰的挑戰回應之後收到新的挑戰，用戶端就必須產生新的挑戰回應。</span><span class="sxs-lookup"><span data-stu-id="51bac-114">If the client receives a new challenge after sending the challenge response for the stale challenge, the client must generate a new challenge response.</span></span>
-   <span data-ttu-id="51bac-115">如果強制執行重新執行偵測，則會根據伺服器維護的 nonce 會話資料庫來檢查 nc 指示詞 (nonce 計數) 。</span><span class="sxs-lookup"><span data-stu-id="51bac-115">If replay detection is enforced, the nc directive (nonce count) is checked against the nonce session database maintained by the server.</span></span>
-   <span data-ttu-id="51bac-116">驗證服務器會識別並傳送用戶端的授權資訊。</span><span class="sxs-lookup"><span data-stu-id="51bac-116">The authenticating server is identified and sent the client's authorization information.</span></span>
-   <span data-ttu-id="51bac-117">驗證服務器會根據源伺服器的身分識別，檢查在 nonce 中編碼之伺服器的身分識別。</span><span class="sxs-lookup"><span data-stu-id="51bac-117">The authenticating server checks the identity of the server encoded in the nonce against the identity of the originating server.</span></span>
-   <span data-ttu-id="51bac-118">驗證服務器是網域控制站，可抓取使用者的密碼。</span><span class="sxs-lookup"><span data-stu-id="51bac-118">The authenticating server, which is a domain controller, retrieves the user's password.</span></span>
-   <span data-ttu-id="51bac-119">驗證服務器會使用授權資訊、密碼和源伺服器識別，來計算用戶端應該在挑戰回應的回應指示詞中提供的值。</span><span class="sxs-lookup"><span data-stu-id="51bac-119">Using the authorization information, password, and originating server identification, the authenticating server computes the value that the client should have supplied in the challenge response's response directive.</span></span> <span data-ttu-id="51bac-120">驗證服務器會將計算的值與用戶端的回應進行比較，以判斷驗證是否成功或失敗。</span><span class="sxs-lookup"><span data-stu-id="51bac-120">The authenticating server compares the computed value to the client's response to determine the success or failure of the authentication.</span></span>

<span data-ttu-id="51bac-121">如果驗證成功，就會將使用者的 [*安全性內容*](../secgloss/s-gly.md) 和摘要 [*工作階段金鑰*](../secgloss/s-gly.md) 傳回給源伺服器。</span><span class="sxs-lookup"><span data-stu-id="51bac-121">If authentication is successful, the user's [*security context*](../secgloss/s-gly.md) and a Digest [*session key*](../secgloss/s-gly.md) are returned to the originating server.</span></span> <span data-ttu-id="51bac-122">如果驗證失敗，則源伺服器必須產生錯誤回應。</span><span class="sxs-lookup"><span data-stu-id="51bac-122">If authentication fails, the originating server must generate an error response.</span></span> <span data-ttu-id="51bac-123">成功驗證之後，源伺服器會將要求的資源傳回給用戶端。</span><span class="sxs-lookup"><span data-stu-id="51bac-123">After a successful authentication the originating server returns the requested resource to the client.</span></span>

<span data-ttu-id="51bac-124">驗證服務器所傳回的摘要工作階段金鑰會由源伺服器快取，以便用於驗證未來的要求。</span><span class="sxs-lookup"><span data-stu-id="51bac-124">The Digest session key returned by the authenticating server is cached by the originating server for use in authenticating future requests.</span></span> <span data-ttu-id="51bac-125">如需詳細資訊，請參閱 [使用 Microsoft Digest 驗證後續要求](authenticating-subsequent-requests-using-microsoft-digest.md)。</span><span class="sxs-lookup"><span data-stu-id="51bac-125">For more information, see [Authenticating Subsequent Requests using Microsoft Digest](authenticating-subsequent-requests-using-microsoft-digest.md).</span></span>

 

 
