---
description: 網路 DDE 使用受信任的共用和安全描述項來控制對共用的存取。
ms.assetid: a22d9fc6-a0c9-442f-b278-1271cfbc636b
title: 受信任的共用和安全性
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 899be51745b2b27c22212c3ceeaceea016fa8d4b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106998443"
---
# <a name="trusted-shares-and-security"></a><span data-ttu-id="79b48-103">受信任的共用和安全性</span><span class="sxs-lookup"><span data-stu-id="79b48-103">Trusted Shares and Security</span></span>

<span data-ttu-id="79b48-104">\[不再支援網路 DDE。</span><span class="sxs-lookup"><span data-stu-id="79b48-104">\[Network DDE is no longer supported.</span></span> <span data-ttu-id="79b48-105">Windows Vista 上有 Nddeapi.dll，但是所有的函式呼叫都會傳回 NDDE \_ 未 \_ 執行。\]</span><span class="sxs-lookup"><span data-stu-id="79b48-105">Nddeapi.dll is present on Windows Vista, but all function calls return NDDE\_NOT\_IMPLEMENTED.\]</span></span>

<span data-ttu-id="79b48-106">網路 DDE 使用受信任的共用和安全描述項來控制對共用的存取。</span><span class="sxs-lookup"><span data-stu-id="79b48-106">Network DDE uses trusted shares and security descriptors to control access to shares.</span></span>

## <a name="trusted-shares"></a><span data-ttu-id="79b48-107">信任的共用</span><span class="sxs-lookup"><span data-stu-id="79b48-107">Trusted Shares</span></span>

<span data-ttu-id="79b48-108">當用戶端使用者從遠端電腦連接到 DDE 共用時，只有在下列陳述成立時，網路 DDE 才會接受要求：</span><span class="sxs-lookup"><span data-stu-id="79b48-108">When a client user connects to a DDE share from a remote computer, network DDE accepts the request only if the following statements are true:</span></span>

-   <span data-ttu-id="79b48-109">建立共用的使用者已透過呼叫 [**NDdeSetTrustedShare**](nddesettrustedshare.md)，將信任的狀態授與共享。</span><span class="sxs-lookup"><span data-stu-id="79b48-109">The user who created the share has granted trusted status to the share by calling [**NDdeSetTrustedShare**](nddesettrustedshare.md).</span></span> <span data-ttu-id="79b48-110">只有共用的建立者可以將信任狀態授與共享。</span><span class="sxs-lookup"><span data-stu-id="79b48-110">Only the creator of the share can grant trusted status to the share.</span></span> <span data-ttu-id="79b48-111">系統管理員甚至不能將受信任的狀態授與給不同使用者所建立的 DDE 共用。</span><span class="sxs-lookup"><span data-stu-id="79b48-111">Not even an administrator can grant trusted status to a DDE share that was created by a different user.</span></span>
-   <span data-ttu-id="79b48-112">建立共用的使用者目前已登入伺服器電腦。</span><span class="sxs-lookup"><span data-stu-id="79b48-112">The user who created the share is currently logged on to the server computer.</span></span>

<span data-ttu-id="79b48-113">將信任狀態授與共享的程式，會將共用新增至 DSDM 中已登入使用者的受信任共用清單。</span><span class="sxs-lookup"><span data-stu-id="79b48-113">The process of granting trusted status to a share adds the share to the logged-on user's trusted shares list in the DSDM.</span></span> <span data-ttu-id="79b48-114">這會在伺服器及其用戶端之間建立信任關係。</span><span class="sxs-lookup"><span data-stu-id="79b48-114">This creates a trust relationship between the server and its clients.</span></span> <span data-ttu-id="79b48-115">當 DDE 共用有受信任狀態時，只要建立共用的使用者登入，用戶端就可以連線到該狀態。</span><span class="sxs-lookup"><span data-stu-id="79b48-115">Once a DDE share has trusted status, clients can connect to it as long as the user that created the share is logged on.</span></span> <span data-ttu-id="79b48-116">當用戶端從遠端電腦連接到共用時，只有在 DSDM 中已登入使用者的受信任共用清單中列出共用時，網路 DDE 才會接受要求。</span><span class="sxs-lookup"><span data-stu-id="79b48-116">When the client connects to the share from a remote computer, network DDE accepts the request only if the share is listed in the logged-on user's trusted shares list in the DSDM.</span></span>

## <a name="security"></a><span data-ttu-id="79b48-117">安全性</span><span class="sxs-lookup"><span data-stu-id="79b48-117">Security</span></span>

<span data-ttu-id="79b48-118">當用戶端要求資料或連結時，網路 DDE 會執行額外的安全性檢查。</span><span class="sxs-lookup"><span data-stu-id="79b48-118">Network DDE performs an additional security check when the client requests data or a link.</span></span> <span data-ttu-id="79b48-119">它會檢查伺服器是否已為遠端使用者授與操作的必要許可權。</span><span class="sxs-lookup"><span data-stu-id="79b48-119">It checks that the server has granted the remote user the necessary permission for the operation.</span></span> <span data-ttu-id="79b48-120">伺服器會透過 [**NDdeShareAdd**](nddeshareadd.md)函數的 *pSD* 參數，控制對共用的存取。</span><span class="sxs-lookup"><span data-stu-id="79b48-120">The server controls access to the share through the *pSD* parameter of the [**NDdeShareAdd**](nddeshareadd.md) function.</span></span> <span data-ttu-id="79b48-121">此參數會指定安全描述項。</span><span class="sxs-lookup"><span data-stu-id="79b48-121">This parameter specifies the security descriptor.</span></span> <span data-ttu-id="79b48-122">如果此參數為 **Null**，此函式會建立預設安全描述項，以授與共享建立者的完整存取權，並將讀取和連結許可權授與所有其他使用者。</span><span class="sxs-lookup"><span data-stu-id="79b48-122">If this parameter is **NULL**, the function creates a default security descriptor that grants full access to the creator of the share and grants read and link permission to all other users.</span></span> <span data-ttu-id="79b48-123">若要授與或拒絕個別使用者或使用者群組的其他許可權，請建立並使用安全描述項。</span><span class="sxs-lookup"><span data-stu-id="79b48-123">To grant or deny additional permissions to individual users or groups of users, create and use a security descriptor.</span></span> <span data-ttu-id="79b48-124">如需安全描述項的詳細資訊，請參閱 [**存取控制**](/windows/desktop/SecAuthZ/access-control)。</span><span class="sxs-lookup"><span data-stu-id="79b48-124">For more information on security descriptors, see [**Access Control**](/windows/desktop/SecAuthZ/access-control).</span></span>

<span data-ttu-id="79b48-125">若要取得現有 DDE 共用的安全描述項，請呼叫 [**NDdeGetShareSecurity**](nddegetsharesecurity.md) 函數。</span><span class="sxs-lookup"><span data-stu-id="79b48-125">To obtain the security descriptor for an existing DDE share, call the [**NDdeGetShareSecurity**](nddegetsharesecurity.md) function.</span></span> <span data-ttu-id="79b48-126">您可以編輯資訊，然後使用 [**NDdeSetShareSecurity**](nddesetsharesecurity.md) 函數來更新共用的安全描述項。</span><span class="sxs-lookup"><span data-stu-id="79b48-126">You can edit the information and then update the security descriptor for the share by using the [**NDdeSetShareSecurity**](nddesetsharesecurity.md) function.</span></span>

 

 
