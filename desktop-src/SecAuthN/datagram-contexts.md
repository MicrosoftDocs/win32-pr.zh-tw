---
description: 資料包的語義或不需連線的內容，與連接導向內容的內容稍有不同。
ms.assetid: f312796c-cbe6-4be9-9886-52fdb34ced6b
title: 資料包內容
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8d233a0ba397e67a13b1c25588cf81b6f12c31d1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104113812"
---
# <a name="datagram-contexts"></a><span data-ttu-id="76dbc-103">資料包內容</span><span class="sxs-lookup"><span data-stu-id="76dbc-103">Datagram Contexts</span></span>

<span data-ttu-id="76dbc-104">[*資料包*](/windows/desktop/SecGloss/d-gly)的語義或不需連線的內容，與連接導向內容的內容稍有不同。</span><span class="sxs-lookup"><span data-stu-id="76dbc-104">The semantics for [*datagram*](/windows/desktop/SecGloss/d-gly), or connectionless, contexts differ slightly from those for connection-oriented contexts.</span></span> <span data-ttu-id="76dbc-105">在資料包的無連接 [*內容*](/windows/desktop/SecGloss/c-gly)中，伺服器無法判斷用戶端何時關閉或終止連接。</span><span class="sxs-lookup"><span data-stu-id="76dbc-105">In a datagram's connectionless [*context*](/windows/desktop/SecGloss/c-gly), a server cannot determine when the client has shut down or otherwise terminated the connection.</span></span> <span data-ttu-id="76dbc-106">換句話說，在連接導向的內容中，不會將任何終止通知從傳輸應用程式傳遞到伺服器。</span><span class="sxs-lookup"><span data-stu-id="76dbc-106">In other words, no termination notice is passed from the transport application to the server as would occur in a connection-oriented context.</span></span>

<span data-ttu-id="76dbc-107">若要使用資料包內容，用戶端會 \_ 在對 \_ [**InitializeSecurityCoNtext (一般)**](/windows/win32/api/sspi/nf-sspi-initializesecuritycontexta) 函式的呼叫中，設定 ISC 需求資料包旗標。</span><span class="sxs-lookup"><span data-stu-id="76dbc-107">To use a datagram context, a client sets the ISC\_REQ\_DATAGRAM flag in its call to the [**InitializeSecurityContext (General)**](/windows/win32/api/sspi/nf-sspi-initializesecuritycontexta) function.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="76dbc-108">[Microsoft Kerberos](microsoft-kerberos.md)套件不支援使用者到使用者模式中的資料包內容。</span><span class="sxs-lookup"><span data-stu-id="76dbc-108">The [Microsoft Kerberos](microsoft-kerberos.md) package does not support datagram contexts in user-to-user mode.</span></span>

 

<span data-ttu-id="76dbc-109">若要更妥善地支援某些模型（特別是 DCE 樣式 RPC），當用戶端使用資料包內容時，會套用下列規則：</span><span class="sxs-lookup"><span data-stu-id="76dbc-109">To better support some models, particularly DCE-style RPC, the following rules apply when the client uses a datagram context:</span></span>

-   <span data-ttu-id="76dbc-110">在第一次呼叫 [**InitializeSecurityCoNtext (一般)**](/windows/win32/api/sspi/nf-sspi-initializesecuritycontexta)時，[*安全性套件*](/windows/desktop/SecGloss/s-gly)不會產生驗證 [*BLOB*](/windows/desktop/SecGloss/b-gly) (二進位大型物件) 。</span><span class="sxs-lookup"><span data-stu-id="76dbc-110">The [*security package*](/windows/desktop/SecGloss/s-gly) does not produce an authentication [*BLOB*](/windows/desktop/SecGloss/b-gly) (binary large object) on the first call to [**InitializeSecurityContext (General)**](/windows/win32/api/sspi/nf-sspi-initializesecuritycontexta).</span></span> <span data-ttu-id="76dbc-111">不過，用戶端可以在呼叫 [**MakeSignature**](/windows/desktop/api/Sspi/nf-sspi-makesignature) 函式時使用傳回的安全性內容，以產生訊息的簽章。</span><span class="sxs-lookup"><span data-stu-id="76dbc-111">However, the client can use the returned security context in a call to the [**MakeSignature**](/windows/desktop/api/Sspi/nf-sspi-makesignature) function to generate a signature for a message.</span></span>
-   <span data-ttu-id="76dbc-112">安全性封裝必須允許重新建立內容多次，以允許伺服器在不另行通知的情況下卸載連接。</span><span class="sxs-lookup"><span data-stu-id="76dbc-112">The security package must allow for the context to be re-established multiple times to allow the server to drop the connection without notice.</span></span> <span data-ttu-id="76dbc-113">這表示 [**MakeSignature**](/windows/desktop/api/Sspi/nf-sspi-makesignature) 和 [**VerifySignature**](/windows/desktop/api/Sspi/nf-sspi-verifysignature) 函式中使用的任何金鑰都可以重設為一致的 [*狀態*](/windows/desktop/SecGloss/s-gly)。</span><span class="sxs-lookup"><span data-stu-id="76dbc-113">This implies that any keys used in the [**MakeSignature**](/windows/desktop/api/Sspi/nf-sspi-makesignature) and [**VerifySignature**](/windows/desktop/api/Sspi/nf-sspi-verifysignature) functions can be reset to a consistent [*state*](/windows/desktop/SecGloss/s-gly).</span></span>
-   <span data-ttu-id="76dbc-114">安全性封裝可讓呼叫者指定順序資訊，並在接收者端提供該順序資訊。</span><span class="sxs-lookup"><span data-stu-id="76dbc-114">The security package allows the caller to specify sequence information, and provides that sequence information at the receiver side.</span></span> <span data-ttu-id="76dbc-115">這是封裝所維護的任何順序資訊以外的資訊。</span><span class="sxs-lookup"><span data-stu-id="76dbc-115">This is in addition to any sequence information maintained by the package.</span></span>

<span data-ttu-id="76dbc-116">安全性套件會設定 SECPKG \_ 旗 \_ 標資料包旗標，表示它支援資料包語義。</span><span class="sxs-lookup"><span data-stu-id="76dbc-116">A security package sets the SECPKG\_FLAG\_DATAGRAM flag to indicate that it supports datagram semantics.</span></span>

 

 
