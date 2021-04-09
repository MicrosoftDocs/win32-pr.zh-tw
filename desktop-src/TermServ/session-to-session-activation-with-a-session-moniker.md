---
title: 使用會話標記的會話對會話啟用
description: 會話對會話啟用 (也稱為跨會話啟用) 可讓用戶端進程啟動 (在指定的會話) 本機伺服器處理常式。
ms.assetid: d405c276-040b-4cde-aeb2-482a25e2867f
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2714f3dbe7b23c8b7f04d4271018891960b87f76
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "103682937"
---
# <a name="session-to-session-activation-with-a-session-moniker"></a><span data-ttu-id="49ed4-103">使用會話標記的會話對會話啟用</span><span class="sxs-lookup"><span data-stu-id="49ed4-103">Session-to-Session Activation with a Session Moniker</span></span>

<span data-ttu-id="49ed4-104">會話對會話啟用 (也稱為跨會話啟用) 可讓用戶端進程啟動 (在指定的會話) 本機伺服器處理常式。</span><span class="sxs-lookup"><span data-stu-id="49ed4-104">Session-to-session activation (also called cross-session activation) allows a client process to start (activate) a local server process on a specified session.</span></span> <span data-ttu-id="49ed4-105">這項功能適用于設定為在互動式使用者的安全性內容中執行的應用程式，也稱為「RunAs 互動式使用者」物件啟用模式。</span><span class="sxs-lookup"><span data-stu-id="49ed4-105">This feature is available for applications that are configured to run in the security context of the interactive user, also known as the "RunAs Interactive User" object activation mode.</span></span> <span data-ttu-id="49ed4-106">如需安全性環境的詳細資訊，請參閱 [用戶端的安全性內容](/windows/desktop/SecAuthZ/the-client-security-context)。</span><span class="sxs-lookup"><span data-stu-id="49ed4-106">For more information about security contexts, see [The Client's Security Context](/windows/desktop/SecAuthZ/the-client-security-context).</span></span>

<span data-ttu-id="49ed4-107">分散式 COM (DCOM) 使用系統提供的 [會話標記](session-monikers.md)，啟用每個會話的物件啟用。</span><span class="sxs-lookup"><span data-stu-id="49ed4-107">Distributed COM (DCOM) enables object activation on a per-session basis by using a system-supplied [Session Moniker](session-monikers.md).</span></span> <span data-ttu-id="49ed4-108">其他系統提供的標記包括檔案的 [名字](../com/file-monikers.md)、 [專案的名字](../com/item-monikers.md)、泛型 [複合](../com/composite-monikers.md)標記、 [反](../com/anti-monikers.md)標記、 [指標](../com/pointer-monikers.md)標記以及 [URL 的名字](../com/url-monikers.md)。</span><span class="sxs-lookup"><span data-stu-id="49ed4-108">Other system-supplied monikers include [file monikers](../com/file-monikers.md), [item monikers](../com/item-monikers.md), generic [composite monikers](../com/composite-monikers.md), [anti-monikers](../com/anti-monikers.md), [pointer monikers](../com/pointer-monikers.md), and [URL monikers](../com/url-monikers.md).</span></span>

<span data-ttu-id="49ed4-109">若要能夠使用會話的標記，必須將 DCOM 應用程式設定為以互動式使用者的形式執行。</span><span class="sxs-lookup"><span data-stu-id="49ed4-109">To be able to use the session moniker, the DCOM application must be set to run as the interactive user.</span></span> <span data-ttu-id="49ed4-110">您可以使用 [元件服務] 系統管理工具、查看 DCOM 應用程式的內容，然後在 [身分 **識別**] 索引標籤上選取 **互動式使用者**，來設定此選項。如需有關將 DCOM 應用程式設定為在遠端桌面服務環境中以互動式使用者身分執行的可能安全性風險的詳細資訊，請參閱平臺軟體發展工具組 (SDK) 之 COM 檔的「應用程式識別 (COM) 」一節。</span><span class="sxs-lookup"><span data-stu-id="49ed4-110">This can be set by using the Component Services Administrative tool, viewing the Properties of the DCOM application, and selecting **The interactive user** on the **Identity** tab. For more information about the possible security risks associated with setting a DCOM application to run as the interactive user in a Remote Desktop Services environment, see the "Application Identity (COM)" section of the COM documentation in the Platform Software Development Kit (SDK).</span></span>

<span data-ttu-id="49ed4-111">如果選取任何其他類型的使用者來執行應用程式，應用程式將會忽略會話的標記。</span><span class="sxs-lookup"><span data-stu-id="49ed4-111">If any other type of user is selected to run the application, the session moniker will be ignored by the application.</span></span> <span data-ttu-id="49ed4-112">COM + 伺服器應用程式也會忽略會話的標記。</span><span class="sxs-lookup"><span data-stu-id="49ed4-112">The session moniker is also ignored by COM+ server applications.</span></span> <span data-ttu-id="49ed4-113">如需有關選取要執行應用程式之使用者類型之其他方法的詳細資訊，請參閱 Platform SDK 中的 COM 檔。</span><span class="sxs-lookup"><span data-stu-id="49ed4-113">For more information about other methods for selecting the type of user to run the application, see the COM documentation in the Platform SDK.</span></span>

<span data-ttu-id="49ed4-114">若要建立會話的標記，您必須使用指定進程伺服器類別識別碼的類別指定識別碼，撰寫遠端桌面服務會話的會話識別碼。</span><span class="sxs-lookup"><span data-stu-id="49ed4-114">To create a session moniker, you must compose the session ID of the Remote Desktop Services session with a class moniker that specifies the process server's class ID.</span></span>

<span data-ttu-id="49ed4-115">**若要建立會話的標記**</span><span class="sxs-lookup"><span data-stu-id="49ed4-115">**To create a session moniker**</span></span>

1.  <span data-ttu-id="49ed4-116">使用下列語法，將類別名字標記的顯示名稱加上前置詞，並將其顯示為會話的名字：</span><span class="sxs-lookup"><span data-stu-id="49ed4-116">Prefix the display name of the class moniker with the display name of the session moniker by using the following syntax:</span></span>

    ``` syntax
    "Session:[digits]!clsid:[class id]"
    ```

    <span data-ttu-id="49ed4-117">其中 *數位* 代表將啟動伺服器進程之會話的會話識別碼，而 *類別識別碼* 代表伺服器的類別識別碼。</span><span class="sxs-lookup"><span data-stu-id="49ed4-117">where *digits* represents the session ID of the session on which the server process will be started, and where *class id* represents the class ID of the server.</span></span> <span data-ttu-id="49ed4-118">請注意，會話識別碼是以10為底數的數位。</span><span class="sxs-lookup"><span data-stu-id="49ed4-118">Note that the session ID is a base-10 number.</span></span>

    <span data-ttu-id="49ed4-119">若為執行 Windows XP 或更新版本的電腦，使用下列語法將會導致 COM 將啟用傳送至目前作用中的實體主控台會話（不論其會話識別碼為何）：</span><span class="sxs-lookup"><span data-stu-id="49ed4-119">For computers that are running Windows XP or later, using the following syntax will result in COM sending the activation to the currently active physical console session, whatever its session ID is:</span></span>

    ``` syntax
    "Session:Console!clsid:[class id]"
    ```

2.  <span data-ttu-id="49ed4-120">建立會話的標記之後，您可以將結果傳遞給 [**MkParseDisplayName**](/windows/desktop/api/objbase/nf-objbase-mkparsedisplayname) 函數或 [MkParseDisplayNameEx](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms775113(v=vs.85)) 函數。</span><span class="sxs-lookup"><span data-stu-id="49ed4-120">After you have created the session moniker, you can pass the result to either the [**MkParseDisplayName**](/windows/desktop/api/objbase/nf-objbase-mkparsedisplayname) function or the [MkParseDisplayNameEx](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms775113(v=vs.85)) function.</span></span>

<span data-ttu-id="49ed4-121">您可以使用會話的標記，就像使用任何其他的標記一樣。</span><span class="sxs-lookup"><span data-stu-id="49ed4-121">You can use a session moniker in the same way as you would use any other moniker.</span></span>

<span data-ttu-id="49ed4-122">如需示範如何在指定的會話上啟動本機伺服器進程的程式碼範例，請參閱 [使用會話的標記](using-a-session-moniker.md)。</span><span class="sxs-lookup"><span data-stu-id="49ed4-122">For a code sample that demonstrates how to activate a local server process on a specified session, see [Using a Session Moniker](using-a-session-moniker.md).</span></span>

<span data-ttu-id="49ed4-123">如需物件啟用、系統提供的名字和類別標記的詳細資訊，請參閱 Platform SDK 中的 COM 檔。</span><span class="sxs-lookup"><span data-stu-id="49ed4-123">For more information about object activation, system-supplied monikers and class monikers, see the COM documentation in the Platform SDK.</span></span>

> [!Note]  
> <span data-ttu-id="49ed4-124">跨會話建立的進程具有環境區塊大小的上限。</span><span class="sxs-lookup"><span data-stu-id="49ed4-124">Processes that are created across sessions have an upper limit on the size of the environment block.</span></span> <span data-ttu-id="49ed4-125">這項限制約為 4 KB，但可能較大或較小，這取決於建立程式所需的其他資訊 (例如) 的新進程的檔案名、目錄和參數。</span><span class="sxs-lookup"><span data-stu-id="49ed4-125">This limit is around 4 KB, but it can be larger or smaller depending on what other information is needed to create the process (for example file names, directories, and parameters for the new process).</span></span>

 

 

 