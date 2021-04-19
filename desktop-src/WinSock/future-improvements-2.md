---
description: 範例 Winsock 應用程式程式碼的未來改進。
ms.assetid: 317baa53-6bc8-42bd-8f56-480cab29ae6b
title: 未來的改進
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 938f38334a4bbe392e83efc0be12905fb7ae66a8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106972631"
---
# <a name="future-improvements"></a><span data-ttu-id="79c52-103">未來的改進</span><span class="sxs-lookup"><span data-stu-id="79c52-103">Future Improvements</span></span>

<span data-ttu-id="79c52-104">您可以對這個應用程式進行幾項改進，例如：</span><span class="sxs-lookup"><span data-stu-id="79c52-104">There are several improvements that can be made to this application, such as:</span></span>

-   <span data-ttu-id="79c52-105">應用程式可能會建立單一的持續性連接。</span><span class="sxs-lookup"><span data-stu-id="79c52-105">A single, persistent connection could be created by the application.</span></span> <span data-ttu-id="79c52-106">必須新增適當的錯誤處理。</span><span class="sxs-lookup"><span data-stu-id="79c52-106">Appropriate error handling would have to be added.</span></span> <span data-ttu-id="79c52-107">這會降低與連線啟動和卸載相關的額外負荷。</span><span class="sxs-lookup"><span data-stu-id="79c52-107">This would reduce the overhead associated with connection startup and teardown.</span></span>
-   <span data-ttu-id="79c52-108">您可以將伺服器上的回復碼優化以合併回復，減少從伺服器傳送的封包數目。</span><span class="sxs-lookup"><span data-stu-id="79c52-108">The reply code on the server could be optimized to consolidate replies, reducing the number of packets sent from the server.</span></span>
-   <span data-ttu-id="79c52-109">您可以對通訊協定進行改善。</span><span class="sxs-lookup"><span data-stu-id="79c52-109">Improvements in the protocol could be made.</span></span> <span data-ttu-id="79c52-110">例如，「更新位元遮罩」可用來表示要更新的資料格，以及只有傳送的資料格。</span><span class="sxs-lookup"><span data-stu-id="79c52-110">For example, an update bitmask could be used to signify which cells are to be updated, and only that cell data sent.</span></span>
-   <span data-ttu-id="79c52-111">您可以使用不同的執行緒來重迭更新，如此一來，當 **ComputeNext** 函式正在執行時，就不會讓網路處於閒置狀態。</span><span class="sxs-lookup"><span data-stu-id="79c52-111">Updates could be overlapped using different threads, so that the network is not idle while the **ComputeNext** function is running.</span></span>

## <a name="related-topics"></a><span data-ttu-id="79c52-112">相關主題</span><span class="sxs-lookup"><span data-stu-id="79c52-112">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="79c52-113">改善應用程式緩慢</span><span class="sxs-lookup"><span data-stu-id="79c52-113">Improving a Slow Application</span></span>](improving-a-slow-application-2.md)
</dt> <dt>

[<span data-ttu-id="79c52-114">基準版本：執行效能不佳的應用程式</span><span class="sxs-lookup"><span data-stu-id="79c52-114">The Baseline Version: A Very Poor Performing Application</span></span>](the-baseline-version-a-very-poor-performing-application-2.md)
</dt> <dt>

[<span data-ttu-id="79c52-115">修訂1：清除明顯的</span><span class="sxs-lookup"><span data-stu-id="79c52-115">Revision 1: Cleaning up the Obvious</span></span>](revision-1-cleaning-up-the-obvious-2.md)
</dt> <dt>

[<span data-ttu-id="79c52-116">修訂2：重新設計較少的連接</span><span class="sxs-lookup"><span data-stu-id="79c52-116">Revision 2: Redesigning for Fewer Connects</span></span>](revision-2-redesigning-for-fewer-connects-2.md)
</dt> <dt>

[<span data-ttu-id="79c52-117">修訂3：壓縮的區區塊轉送</span><span class="sxs-lookup"><span data-stu-id="79c52-117">Revision 3: Compressed Block Send</span></span>](revision-3-compressed-block-send-2.md)
</dt> </dl>

 

 



