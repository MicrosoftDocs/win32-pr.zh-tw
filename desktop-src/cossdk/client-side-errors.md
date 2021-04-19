---
description: Client-Side 錯誤
ms.assetid: 95fb2ef1-eec2-4c74-891a-617450098160
title: Client-Side 錯誤
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ef309858d1527fdcabe0f487de87df19d20635c0
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106970717"
---
# <a name="client-side-errors"></a><span data-ttu-id="e5d79-103">Client-Side 錯誤</span><span class="sxs-lookup"><span data-stu-id="e5d79-103">Client-Side Errors</span></span>

<span data-ttu-id="e5d79-104">用戶端的失敗會以類似伺服器端失敗的方式處理。</span><span class="sxs-lookup"><span data-stu-id="e5d79-104">Client-side failures are handled in a way that is similar to server-side failures.</span></span> <span data-ttu-id="e5d79-105">例如，如果訊息無法從用戶端移至伺服器，[訊息佇列](/previous-versions/windows/desktop/legacy/ms711472(v=vs.85))就可以將訊息移至其目的地佇列。</span><span class="sxs-lookup"><span data-stu-id="e5d79-105">[Message Queuing](/previous-versions/windows/desktop/legacy/ms711472(v=vs.85)) can move a message to its destination queue if, for example, the message cannot be moved from client to server.</span></span> <span data-ttu-id="e5d79-106">在此情況下，訊息會移至用戶端無效信件佇列。</span><span class="sxs-lookup"><span data-stu-id="e5d79-106">In this case, the message is moved to the client-side dead letter queue.</span></span>

<span data-ttu-id="e5d79-107">COM + 佇列元件服務會監視無效信件佇列。</span><span class="sxs-lookup"><span data-stu-id="e5d79-107">The COM+ queued components service monitors the dead letter queue.</span></span> <span data-ttu-id="e5d79-108">如果訊息已移動，佇列的元件服務會建立例外狀況類別的實例，並呼叫 [**QueryInterface**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) 來要求 [**IPlaybackControl**](/windows/desktop/api/ComSvcs/nn-comsvcs-iplaybackcontrol)。</span><span class="sxs-lookup"><span data-stu-id="e5d79-108">If messages have been moved, the queued components service creates an instance of the exception class and calls [**QueryInterface**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) to request [**IPlaybackControl**](/windows/desktop/api/ComSvcs/nn-comsvcs-iplaybackcontrol).</span></span> <span data-ttu-id="e5d79-109">如果成功，無效信件佇列監視器會叫用 [**IPlaybackControl：： FinalClientRetry**](/windows/desktop/api/ComSvcs/nf-comsvcs-iplaybackcontrol-finalclientretry)。</span><span class="sxs-lookup"><span data-stu-id="e5d79-109">If this is successful, the dead letter queue monitor invokes [**IPlaybackControl::FinalClientRetry**](/windows/desktop/api/ComSvcs/nf-comsvcs-iplaybackcontrol-finalclientretry).</span></span>

<span data-ttu-id="e5d79-110">物件可以採取一些動作來反轉先前交易的效果。</span><span class="sxs-lookup"><span data-stu-id="e5d79-110">The object can take some action to reverse the effect of a prior transaction.</span></span> <span data-ttu-id="e5d79-111">如果播放認可，則會從交易無效信件佇列中移除訊息。</span><span class="sxs-lookup"><span data-stu-id="e5d79-111">If the playback commits, the message is removed from the Xact dead letter queue.</span></span> <span data-ttu-id="e5d79-112">如果播放失敗或必要的 CLSID 和介面無法使用，則訊息會保留在交易無效信件佇列中。</span><span class="sxs-lookup"><span data-stu-id="e5d79-112">If the playback fails or the required CLSID and interface are not available, the message remains on the Xact dead letter queue.</span></span>

<span data-ttu-id="e5d79-113">如果您需要介入以上所述的程式，或如果您需要將有害訊息移出其最終的靜止佇列，請使用訊息移動器公用程式。</span><span class="sxs-lookup"><span data-stu-id="e5d79-113">If you need to intervene in the process described above or if you need to move a poison message out of its final resting queue, use the message mover utility.</span></span> <span data-ttu-id="e5d79-114">如需訊息移動器公用程式的詳細資訊，請參閱 [處理錯誤](handling-errors-in-queued-components.md)。</span><span class="sxs-lookup"><span data-stu-id="e5d79-114">For more information on the message mover utility, see [Handling Errors](handling-errors-in-queued-components.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="e5d79-115">相關主題</span><span class="sxs-lookup"><span data-stu-id="e5d79-115">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e5d79-116">持續性 Client-Side 失敗</span><span class="sxs-lookup"><span data-stu-id="e5d79-116">Persistent Client-Side Failures</span></span>](persistent-client-side-failures.md)
</dt> <dt>

[<span data-ttu-id="e5d79-117">伺服器端錯誤</span><span class="sxs-lookup"><span data-stu-id="e5d79-117">Server-Side Errors</span></span>](server-side-errors.md)
</dt> </dl>

 

 
