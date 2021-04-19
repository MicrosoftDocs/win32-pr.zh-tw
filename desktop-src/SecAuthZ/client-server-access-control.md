---
description: 伺服器應用程式會為用戶端提供服務。
ms.assetid: 8301ed4f-9458-410b-af19-4f055656005a
title: 用戶端/伺服器存取控制
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 92b1d349abb2d55f00b9801c9bb493437fa858eb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106974335"
---
# <a name="clientserver-access-control"></a><span data-ttu-id="56aef-103">用戶端/伺服器存取控制</span><span class="sxs-lookup"><span data-stu-id="56aef-103">Client/Server Access Control</span></span>

<span data-ttu-id="56aef-104">伺服器應用程式會為用戶端提供服務。</span><span class="sxs-lookup"><span data-stu-id="56aef-104">A server application provides services to clients.</span></span> <span data-ttu-id="56aef-105">例如，伺服器可以代表用戶端執行下列服務：</span><span class="sxs-lookup"><span data-stu-id="56aef-105">For example, a server could perform the following services on behalf of a client:</span></span>

-   <span data-ttu-id="56aef-106">從私用資料庫儲存和取出資訊</span><span class="sxs-lookup"><span data-stu-id="56aef-106">Save and retrieve information from a private database</span></span>
-   <span data-ttu-id="56aef-107">存取網路資源</span><span class="sxs-lookup"><span data-stu-id="56aef-107">Access network resources</span></span>
-   <span data-ttu-id="56aef-108">在伺服器電腦上的用戶端 [*安全性內容*](/windows/desktop/SecGloss/s-gly)中啟動 [*處理*](/windows/desktop/SecGloss/p-gly)程式</span><span class="sxs-lookup"><span data-stu-id="56aef-108">Start [*processes*](/windows/desktop/SecGloss/p-gly) in the client's [*security context*](/windows/desktop/SecGloss/s-gly) on the server's computer</span></span>

<span data-ttu-id="56aef-109">受保護的伺服器可控制其服務的存取權。</span><span class="sxs-lookup"><span data-stu-id="56aef-109">A protected server controls access to its services.</span></span> <span data-ttu-id="56aef-110">Windows 提供安全性支援，可讓伺服器執行下列動作：</span><span class="sxs-lookup"><span data-stu-id="56aef-110">Windows provides security support that enables a server to do the following:</span></span>

-   <span data-ttu-id="56aef-111">模擬用戶端的 [*安全性內容*](/windows/desktop/SecGloss/s-gly)，這會導致系統對用戶端的 [*存取權杖*](/windows/desktop/SecGloss/a-gly)執行大部分的存取和 [*許可權*](/windows/desktop/SecGloss/p-gly)檢查，而不是伺服器的</span><span class="sxs-lookup"><span data-stu-id="56aef-111">Impersonate a client's [*security context*](/windows/desktop/SecGloss/s-gly), which causes the system to perform most access and [*privilege*](/windows/desktop/SecGloss/p-gly) checks against the client's [*access token*](/windows/desktop/SecGloss/a-gly) rather than the server's</span></span>
-   <span data-ttu-id="56aef-112">將用戶端登入伺服器的電腦</span><span class="sxs-lookup"><span data-stu-id="56aef-112">Log a client on to the server's computer</span></span>
-   <span data-ttu-id="56aef-113">使用用戶端的安全性內容連接到網路資源</span><span class="sxs-lookup"><span data-stu-id="56aef-113">Connect to network resources using the client's security context</span></span>
-   <span data-ttu-id="56aef-114">建立 [*安全描述項*](/windows/desktop/SecGloss/s-gly) 以保護私用物件</span><span class="sxs-lookup"><span data-stu-id="56aef-114">Create [*security descriptors*](/windows/desktop/SecGloss/s-gly) to protect private objects</span></span>
-   <span data-ttu-id="56aef-115">判斷安全描述項是否允許存取用戶端</span><span class="sxs-lookup"><span data-stu-id="56aef-115">Determine whether a security descriptor allows access to a client</span></span>
-   <span data-ttu-id="56aef-116">判斷是否已在用戶端的權杖中啟用一組許可權</span><span class="sxs-lookup"><span data-stu-id="56aef-116">Determine whether a set of privileges are enabled in a client's token</span></span>
-   <span data-ttu-id="56aef-117">在安全性事件記錄檔中產生審核訊息，以記錄用戶端存取物件或使用許可權的嘗試</span><span class="sxs-lookup"><span data-stu-id="56aef-117">Generate audit messages in the security event log to record attempts by a client to access objects or use privileges</span></span>

 

 
