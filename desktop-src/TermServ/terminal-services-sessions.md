---
title: 遠端桌面會話
description: 因為每次登入遠端桌面連線 (RDC) 用戶端會收到個別的會話識別碼，所以使用者體驗類似于同時登入多部電腦;例如，辦公室電腦和家用電腦。
ms.assetid: 09a990cd-7590-4d73-b1f5-8736f0b4f17e
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6bb99f9745e382bdff1099eabae9a8e8ef0b8333
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "106966250"
---
# <a name="remote-desktop-sessions"></a><span data-ttu-id="689ff-103">遠端桌面會話</span><span class="sxs-lookup"><span data-stu-id="689ff-103">Remote Desktop Sessions</span></span>

<span data-ttu-id="689ff-104">當使用者登入已啟用遠端桌面服務的電腦時，就會啟動使用者的會話。</span><span class="sxs-lookup"><span data-stu-id="689ff-104">When a user logs on to a Remote Desktop Services–enabled computer, a session is started for the user.</span></span> <span data-ttu-id="689ff-105">每個會話都是由唯一的會話識別碼所識別。</span><span class="sxs-lookup"><span data-stu-id="689ff-105">Each session is identified by a unique session ID.</span></span> <span data-ttu-id="689ff-106">因為每次登入遠端桌面連線 (RDC) 用戶端會收到個別的會話識別碼，所以使用者體驗類似于同時登入多部電腦;例如，辦公室電腦和家用電腦。</span><span class="sxs-lookup"><span data-stu-id="689ff-106">Because each logon to a Remote Desktop Connection (RDC) client receives a separate session ID, the user-experience is similar to being logged on to multiple computers at the same time; for example, an office computer and a home computer.</span></span>

<span data-ttu-id="689ff-107">每個遠端桌面會話都與互動式視窗工作站相關聯。</span><span class="sxs-lookup"><span data-stu-id="689ff-107">Each remote desktop session is associated with an interactive window station.</span></span> <span data-ttu-id="689ff-108">互動式視窗工作站唯一支援的 windows 工作站名稱為 "WinSta0";因此，每個會話都會與它自己的「WinSta0」視窗站產生關聯。</span><span class="sxs-lookup"><span data-stu-id="689ff-108">The only supported window station name for an interactive window station is "WinSta0"; therefore each session is associated with its own "WinSta0" window station.</span></span> <span data-ttu-id="689ff-109">每個視窗工作站都有三個標準桌面： Winlogon desktop、螢幕保護裝置桌面和互動式桌面。</span><span class="sxs-lookup"><span data-stu-id="689ff-109">There are three standard desktops for each window station: the Winlogon desktop, the screen saver desktop, and the interactive desktop.</span></span>

<span data-ttu-id="689ff-110">與會話的互動式視窗工作站相關聯的使用者，就是所謂的 *互動式使用者*。</span><span class="sxs-lookup"><span data-stu-id="689ff-110">The user associated with the interactive window station for a session is known as the *interactive user*.</span></span> <span data-ttu-id="689ff-111">在遠端桌面連線 (RDC) 用戶端上，除了遠端桌面服務主控台的互動式使用者之外，也可以有多個互動式使用者。</span><span class="sxs-lookup"><span data-stu-id="689ff-111">On a Remote Desktop Connection (RDC) client there can be multiple interactive users in addition to the interactive user on the Remote Desktop Services console.</span></span> <span data-ttu-id="689ff-112">若要取得目前附加至主控台之會話的識別碼，請使用 [**WTSGetActiveConsoleSessionId**](/windows/desktop/api/Winbase/nf-winbase-wtsgetactiveconsolesessionid) 函式。</span><span class="sxs-lookup"><span data-stu-id="689ff-112">To retrieve the identifier of the session currently attached to the console, use the [**WTSGetActiveConsoleSessionId**](/windows/desktop/api/Winbase/nf-winbase-wtsgetactiveconsolesessionid) function.</span></span>

<span data-ttu-id="689ff-113">當使用者登出遠端桌面連線 (RDC) 用戶端時，系統會刪除用戶端在遠端桌面工作階段主機 (RD 工作階段主機)  (伺服器上的會話，) 先前稱為終端機伺服器，並移除與該會話相關聯的視窗和桌面。</span><span class="sxs-lookup"><span data-stu-id="689ff-113">When a user logs off from a Remote Desktop Connection (RDC) client, the session that the client has on the Remote Desktop Session Host (RD Session Host) server (formerly known as a terminal server) is deleted and the window stations and desktops associated with that session are removed.</span></span> <span data-ttu-id="689ff-114">不過，由於不會刪除遠端桌面服務主控台會話，因此不會刪除與主控台會話相關聯的視窗工作站。</span><span class="sxs-lookup"><span data-stu-id="689ff-114">However, because the Remote Desktop Services console session is never deleted, the window stations associated with the console session are not deleted.</span></span> <span data-ttu-id="689ff-115">這會影響當應用程式設定為在互動式使用者的安全性內容（也稱為「RunAs 互動式使用者」物件啟用模式）中執行時，在遠端桌面服務環境中的行為。</span><span class="sxs-lookup"><span data-stu-id="689ff-115">This affects how applications behave in a Remote Desktop Services environment when they are configured to run in the security context of the interactive user, also known as the "RunAs Interactive User" object activation mode.</span></span>

<span data-ttu-id="689ff-116">如需有關在指定的會話上啟動本機伺服器進程的詳細資訊，請參閱 [使用會話標記的會話對會話啟用](session-to-session-activation-with-a-session-moniker.md) 和 [使用會話的標記](using-a-session-moniker.md)。</span><span class="sxs-lookup"><span data-stu-id="689ff-116">For more information about starting a local server process on a specified session, see [Session-to-Session Activation with a Session Moniker](session-to-session-activation-with-a-session-moniker.md) and [Using a Session Moniker](using-a-session-moniker.md).</span></span> <span data-ttu-id="689ff-117">如需安全性環境的詳細資訊，請參閱 [用戶端的安全性內容](/windows/desktop/SecAuthZ/the-client-security-context)。</span><span class="sxs-lookup"><span data-stu-id="689ff-117">For more information about security contexts, see [The Client's Security Context](/windows/desktop/SecAuthZ/the-client-security-context).</span></span>

## <a name="related-topics"></a><span data-ttu-id="689ff-118">相關主題</span><span class="sxs-lookup"><span data-stu-id="689ff-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="689ff-119">子會話</span><span class="sxs-lookup"><span data-stu-id="689ff-119">Child Sessions</span></span>](child-sessions.md)
</dt> </dl>

 

 