---
title: 效能指導方針
description: 開發在遠端桌面服務環境中順利執行之應用程式的指導方針。
ms.assetid: 50f0c1f6-8046-4ceb-b2c4-6fc1ae86fd73
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3ea7ada6ee2b51943d47f39446d0b1bb3b7d6718
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104372608"
---
# <a name="performance-guidelines"></a><span data-ttu-id="b9992-103">效能指導方針</span><span class="sxs-lookup"><span data-stu-id="b9992-103">Performance guidelines</span></span>

<span data-ttu-id="b9992-104">下列各節提供在遠端桌面服務環境中開發順利執行應用程式的指導方針。</span><span class="sxs-lookup"><span data-stu-id="b9992-104">The following sections provide guidelines for developing applications that perform well in a Remote Desktop Services environment.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="b9992-105">本節內容</span><span class="sxs-lookup"><span data-stu-id="b9992-105">In this section</span></span>

<dl> <dt>

[<span data-ttu-id="b9992-106">圖形效果</span><span class="sxs-lookup"><span data-stu-id="b9992-106">Graphic effects</span></span>](graphic-effects.md)
</dt> <dd>

<span data-ttu-id="b9992-107">在遠端桌面服務環境中做為遠端會話執行時，應該停用的功能清單。</span><span class="sxs-lookup"><span data-stu-id="b9992-107">A list of features that should be disabled when running as a remote session in a Remote Desktop Services environment.</span></span>

</dd> <dt>

[<span data-ttu-id="b9992-108">遠端桌面服務中背景工作的指導方針</span><span class="sxs-lookup"><span data-stu-id="b9992-108">Guidelines for background tasks in Remote Desktop Services</span></span>](background-tasks.md)
</dt> <dd>

<span data-ttu-id="b9992-109">若要讓所有使用者都能發揮最大的 CPU 可用性，請在遠端桌面服務環境中執行時停用背景工作，或建立不需耗用大量資源的有效率背景工作。</span><span class="sxs-lookup"><span data-stu-id="b9992-109">To maximize CPU availability for all users, either disable background tasks when running in a Remote Desktop Services environment or create efficient background tasks that are not resource-intensive.</span></span>

</dd> <dt>

[<span data-ttu-id="b9992-110">執行緒使用方式</span><span class="sxs-lookup"><span data-stu-id="b9992-110">Thread usage</span></span>](thread-usage.md)
</dt> <dd>

<span data-ttu-id="b9992-111">您應該針對多使用者、多處理器遠端桌面服務環境，調整應用程式執行緒的使用方式並進行平衡。</span><span class="sxs-lookup"><span data-stu-id="b9992-111">You should tune and balance application thread usage for a multiuser, multiprocessor Remote Desktop Services environment.</span></span>

</dd> <dt>

[<span data-ttu-id="b9992-112">偵測遠端桌面服務環境</span><span class="sxs-lookup"><span data-stu-id="b9992-112">Detecting the Remote Desktop Services environment</span></span>](detecting-the-terminal-services-environment.md)
</dt> <dd>

<span data-ttu-id="b9992-113">為了將效能優化，應用程式可以偵測它們是否在遠端桌面服務用戶端會話中執行，是很好的作法。</span><span class="sxs-lookup"><span data-stu-id="b9992-113">To optimize performance, it is good practice for applications to detect whether they are running in a Remote Desktop Services client session.</span></span>

</dd> </dl>

<span data-ttu-id="b9992-114">檢查您的應用程式是否發生記憶體流失問題，並解決任何問題。</span><span class="sxs-lookup"><span data-stu-id="b9992-114">Check your application for memory leaks and resolve any problems.</span></span> <span data-ttu-id="b9992-115">當然，對於任何應用程式來說，這是很好的建議，但是在遠端桌面服務環境中，多個使用者可以多次執行應用程式，因此可快速放大記憶體流失的影響。</span><span class="sxs-lookup"><span data-stu-id="b9992-115">Of course this is good advice for any application, but in a Remote Desktop Services environment, an application can be run multiple times by multiple users, thus rapidly magnifying the effect of a memory leak.</span></span>

<span data-ttu-id="b9992-116">動畫、大型影像、音訊和其他頻寬密集型服務都必須可設定。</span><span class="sxs-lookup"><span data-stu-id="b9992-116">Animations, large images, audio, and other bandwidth-intensive services must be configurable.</span></span> <span data-ttu-id="b9992-117">當這些服務不是主要功能時，它們預設可以針對遠端會話關閉，但在會話執行于本機或透過高頻寬連接時啟用。</span><span class="sxs-lookup"><span data-stu-id="b9992-117">When these services are not the primary function, they can be off by default for remote sessions, but enabled when a session is running locally or over a high bandwidth connection.</span></span> <span data-ttu-id="b9992-118">如果應用程式的目的是要提供高頻寬的服務，例如串流影片廣播，則服務預設不需要關閉。</span><span class="sxs-lookup"><span data-stu-id="b9992-118">If the purpose of an application is to provide high bandwidth services, such as streaming video broadcasts, the service does not have to be off by default.</span></span>

 

 




