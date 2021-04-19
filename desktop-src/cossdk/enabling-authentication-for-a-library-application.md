---
description: 啟用程式庫應用程式的驗證
ms.assetid: 80c80c14-ceef-4a74-810d-6aa3cc320cef
title: 啟用程式庫應用程式的驗證
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 74cfa9f2a6a5e3c1312fa13e0aff1e9f4ea17e4c
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106972142"
---
# <a name="enabling-authentication-for-a-library-application"></a><span data-ttu-id="714c5-103">啟用程式庫應用程式的驗證</span><span class="sxs-lookup"><span data-stu-id="714c5-103">Enabling Authentication for a Library Application</span></span>

<span data-ttu-id="714c5-104">由於 COM + 程式庫應用程式是由其他進程主控，因此其安全性需求可能與伺服器應用程式的需求不同。</span><span class="sxs-lookup"><span data-stu-id="714c5-104">Because COM+ library applications are hosted by other processes, their security requirements may be different from those of server applications.</span></span> <span data-ttu-id="714c5-105">如果程式庫應用程式將由瀏覽器主控，則可能需要接收未經驗證的回呼。</span><span class="sxs-lookup"><span data-stu-id="714c5-105">If the library application will be hosted by a browser, it might need to receive unauthenticated callbacks.</span></span>

<span data-ttu-id="714c5-106">若要解決此需求，您可以停用驗證，讓裝載進程不會針對程式庫應用程式的呼叫端執行安全性檢查。</span><span class="sxs-lookup"><span data-stu-id="714c5-106">To address this need, you can disable authentication so that the hosting process does not perform security checks for callers of the library application.</span></span> <span data-ttu-id="714c5-107">當您停用驗證時，對程式庫應用程式的呼叫會有效地進行未經驗證，而且所有對它的呼叫都會成功。</span><span class="sxs-lookup"><span data-stu-id="714c5-107">When you disable authentication, calls to the library application effectively go unauthenticated—all calls to it will succeed.</span></span> <span data-ttu-id="714c5-108">如需詳細資訊，請參閱連結 [庫應用程式安全性](library-application-security.md)。</span><span class="sxs-lookup"><span data-stu-id="714c5-108">For more information, see [Library Application Security](library-application-security.md).</span></span>

<span data-ttu-id="714c5-109">**啟用 (或停用程式庫應用程式的) 驗證**</span><span class="sxs-lookup"><span data-stu-id="714c5-109">**To enable (or disable) authentication for a library application**</span></span>

1.  <span data-ttu-id="714c5-110">以滑鼠右鍵按一下您要啟用或停用驗證的 COM + 應用程式，然後按一下 [ **屬性**]。</span><span class="sxs-lookup"><span data-stu-id="714c5-110">Right-click the COM+ application for which you are enabling or disabling authentication, and then click **Properties**.</span></span>

2.  <span data-ttu-id="714c5-111">在 [應用程式屬性] 對話方塊中，按一下 [ **安全性** ] 索引標籤。</span><span class="sxs-lookup"><span data-stu-id="714c5-111">In the application properties dialog box, click the **Security** tab.</span></span>

3.  <span data-ttu-id="714c5-112">在 [ **驗證**] 下，選取 [ **啟用驗證** ] 核取方塊以啟用驗證;清除此核取方塊將會停用驗證。</span><span class="sxs-lookup"><span data-stu-id="714c5-112">Under **Authentication**, select the **Enable authentication** check box to enable authentication; clearing the check box will disable authentication.</span></span>

4.  <span data-ttu-id="714c5-113">按一下 [確定]  。</span><span class="sxs-lookup"><span data-stu-id="714c5-113">Click **OK**.</span></span>

## <a name="related-topics"></a><span data-ttu-id="714c5-114">相關主題</span><span class="sxs-lookup"><span data-stu-id="714c5-114">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="714c5-115">設定伺服器應用程式的驗證層級</span><span class="sxs-lookup"><span data-stu-id="714c5-115">Setting an Authentication Level for a Server Application</span></span>](setting-an-authentication-level-for-a-server-application.md)
</dt> </dl>

 

 



