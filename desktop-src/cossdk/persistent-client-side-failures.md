---
description: 持續性 Client-Side 失敗
ms.assetid: f991db71-8319-414d-8a25-2d02bc7c8b51
title: 持續性 Client-Side 失敗
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 25d303e712257d62e4ae42497cb4463e782cfbb8
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104385948"
---
# <a name="persistent-client-side-failures"></a><span data-ttu-id="5fad0-103">持續性 Client-Side 失敗</span><span class="sxs-lookup"><span data-stu-id="5fad0-103">Persistent Client-Side Failures</span></span>

<span data-ttu-id="5fad0-104">在某些情況下， [訊息佇列](/previous-versions/windows/desktop/legacy/ms711472(v=vs.85)) 可以將訊息移至目的地佇列。</span><span class="sxs-lookup"><span data-stu-id="5fad0-104">In some cases, [Message Queuing](/previous-versions/windows/desktop/legacy/ms711472(v=vs.85)) can move a message to the destination queue.</span></span> <span data-ttu-id="5fad0-105">例如，如果佇列存取控制不允許將訊息從用戶端移至伺服器，則會將違規的訊息移至用戶端無效信件佇列。</span><span class="sxs-lookup"><span data-stu-id="5fad0-105">For example, if the queue access controls do not permit the message to be moved from client to server, the offending message is moved to the client-side dead letter queue.</span></span> <span data-ttu-id="5fad0-106">發生這種情況時，COM + 佇列的元件服務可讓例外狀況類別與元件相關聯。</span><span class="sxs-lookup"><span data-stu-id="5fad0-106">When this occurs, the COM+ queued components service allows an exception class to be associated with a component.</span></span> <span data-ttu-id="5fad0-107">若要將例外狀況類別與元件產生關聯，請在 [元件服務管理工具] 的 [元件屬性] 頁面中，使用 [ **Advanced** ] 索引標籤。</span><span class="sxs-lookup"><span data-stu-id="5fad0-107">To associate the exception class with the component, use the **Advanced** tab in the component properties page of the Component Services administration tool.</span></span> <span data-ttu-id="5fad0-108">您也可以使用 COM + 系統管理函數的 ExceptionClass catalog component 屬性，以程式設計的方式建立例外狀況類別的關聯。</span><span class="sxs-lookup"><span data-stu-id="5fad0-108">You can also associate the exception class programmatically, by using the ExceptionClass catalog component attribute of the COM+ Administrative functions.</span></span>

<span data-ttu-id="5fad0-109">例外狀況類別定義為執行 [**IPlaybackControl**](/windows/desktop/api/ComSvcs/nn-comsvcs-iplaybackcontrol)之元件的 PROGID 或 CLSID。</span><span class="sxs-lookup"><span data-stu-id="5fad0-109">The exception class is defined as either the ProgID or the CLSID of a component implementing [**IPlaybackControl**](/windows/desktop/api/ComSvcs/nn-comsvcs-iplaybackcontrol).</span></span> <span data-ttu-id="5fad0-110">排入佇列的元件服務具有可掃描交易無效信件佇列的無效信件佇列監視器。</span><span class="sxs-lookup"><span data-stu-id="5fad0-110">The queued components service has a dead letter queue monitor that scans the Xact dead letter queue.</span></span> <span data-ttu-id="5fad0-111">如果佇列中有訊息，寄不出的信件佇列監視器會具現化與目標群組件相關聯的例外狀況處理常式，並呼叫 [**IPlaybackControl：： FinalClientRetry**](/windows/desktop/api/ComSvcs/nf-comsvcs-iplaybackcontrol-finalclientretry)，表示有用戶端、無法復原的錯誤。</span><span class="sxs-lookup"><span data-stu-id="5fad0-111">If there is a message on the queue, the dead letter queue monitor instantiates the exception handler associated with the target component and calls [**IPlaybackControl::FinalClientRetry**](/windows/desktop/api/ComSvcs/nf-comsvcs-iplaybackcontrol-finalclientretry), indicating that there has been a client-side, unrecoverable error.</span></span>

<span data-ttu-id="5fad0-112">除了 [**IPlaybackControl**](/windows/desktop/api/ComSvcs/nn-comsvcs-iplaybackcontrol)之外，例外狀況處理常式也應該執行與處理例外狀況之伺服器元件相同的介面集。</span><span class="sxs-lookup"><span data-stu-id="5fad0-112">In addition to [**IPlaybackControl**](/windows/desktop/api/ComSvcs/nn-comsvcs-iplaybackcontrol), the exception handler should implement the same set of interfaces as the server component for which it is handling exceptions.</span></span> <span data-ttu-id="5fad0-113">呼叫 [**IPlaybackControl：： FinalClientRetry**](/windows/desktop/api/ComSvcs/nf-comsvcs-iplaybackcontrol-finalclientretry) 時，已排入佇列的元件執行時間會將失敗的訊息播放回例外狀況處理常式。</span><span class="sxs-lookup"><span data-stu-id="5fad0-113">When [**IPlaybackControl::FinalClientRetry**](/windows/desktop/api/ComSvcs/nf-comsvcs-iplaybackcontrol-finalclientretry) is called, the queued components run-time plays back the failing message to the exception handler.</span></span> <span data-ttu-id="5fad0-114">這可讓例外狀況處理常式針對無法移至伺服器的訊息（例如，藉由產生補償交易）來執行替代行為。</span><span class="sxs-lookup"><span data-stu-id="5fad0-114">This allows the exception handler to implement an alternative behavior for messages that cannot be moved to the server—for example, by generating a compensating transaction.</span></span>

<span data-ttu-id="5fad0-115">如果例外狀況處理常式完成所有已播放的方法呼叫，則會從交易寄不出的信件佇列中移除訊息，並加以關閉。</span><span class="sxs-lookup"><span data-stu-id="5fad0-115">If the exception handler completes all the method calls played back, the message is removed from the Xact dead letter queue and is dismissed.</span></span> <span data-ttu-id="5fad0-116">但是，如果例外狀況處理常式藉由傳回其中一個方法呼叫的失敗狀態來中止訊息，則會將訊息傳回給交易無效信件佇列。</span><span class="sxs-lookup"><span data-stu-id="5fad0-116">If, however, the exception handler aborts the message by returning a failure status from one of the method calls, the message is returned to the Xact dead letter queue.</span></span> <span data-ttu-id="5fad0-117">下列事件順序顯示用戶端例外狀況的處理方式：</span><span class="sxs-lookup"><span data-stu-id="5fad0-117">The following sequence of events shows how client-side exceptions are handled:</span></span>

1.  <span data-ttu-id="5fad0-118">訊息佇列無法將訊息傳遞至伺服器，並將訊息放到交易的無效信件佇列。</span><span class="sxs-lookup"><span data-stu-id="5fad0-118">Message Queuing fails to deliver a message to the server and puts the message onto the Xact dead letter queue.</span></span>
2.  <span data-ttu-id="5fad0-119">寄不出的信件佇列接聽程式 (DLQL) 在交易無效信件佇列中尋找訊息。</span><span class="sxs-lookup"><span data-stu-id="5fad0-119">The dead letter queue listener (DLQL) finds a message on the Xact dead letter queue.</span></span>
3.  <span data-ttu-id="5fad0-120">DLQL 會從訊息中抓取目標群組件 CLSID，並檢查是否有例外狀況類別。</span><span class="sxs-lookup"><span data-stu-id="5fad0-120">The DLQL retrieves the target component CLSID from the message and checks for an exception class.</span></span>
4.  <span data-ttu-id="5fad0-121">DLQL 會具現化例外狀況類別。</span><span class="sxs-lookup"><span data-stu-id="5fad0-121">The DLQL instantiates the exception class.</span></span>
5.  <span data-ttu-id="5fad0-122">DLQL 會查詢例外狀況類別的 [**IPlaybackControl**](/windows/desktop/api/ComSvcs/nn-comsvcs-iplaybackcontrol) 。</span><span class="sxs-lookup"><span data-stu-id="5fad0-122">The DLQL queries for [**IPlaybackControl**](/windows/desktop/api/ComSvcs/nn-comsvcs-iplaybackcontrol) for the exception class.</span></span>
6.  <span data-ttu-id="5fad0-123">DLQL 會在例外狀況類別中呼叫 [**IPlaybackControl：： FinalClientRetry**](/windows/desktop/api/ComSvcs/nf-comsvcs-iplaybackcontrol-finalclientretry) 方法。</span><span class="sxs-lookup"><span data-stu-id="5fad0-123">The DLQL calls the [**IPlaybackControl::FinalClientRetry**](/windows/desktop/api/ComSvcs/nf-comsvcs-iplaybackcontrol-finalclientretry) method in the exception class.</span></span>
7.  <span data-ttu-id="5fad0-124">DLQL 會將訊息中的所有屬性和方法呼叫播放到例外狀況類別。</span><span class="sxs-lookup"><span data-stu-id="5fad0-124">The DLQL plays back all property and method calls from the message to the exception class.</span></span>
8.  <span data-ttu-id="5fad0-125">如果例外狀況處理常式成功完成交易，則 DLQL 會刪除訊息。</span><span class="sxs-lookup"><span data-stu-id="5fad0-125">The DLQL deletes the message if the exception handler completes the transaction successfully.</span></span> <span data-ttu-id="5fad0-126">例外狀況處理常式可能會發出 [**IObjectCoNtext：： SetAbort**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontext-setabort)，且訊息會保留在寄不出的信件佇列中。</span><span class="sxs-lookup"><span data-stu-id="5fad0-126">The exception handler may issue [**IObjectContext::SetAbort**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontext-setabort), and the message will remain on the dead letter queue.</span></span>

<span data-ttu-id="5fad0-127">如果上述任何一個步驟失敗，訊息就會保留在交易無效信件佇列中。</span><span class="sxs-lookup"><span data-stu-id="5fad0-127">If any of the preceding steps fail, the message is left on the Xact dead letter queue.</span></span>

<span data-ttu-id="5fad0-128">啟動時，DLQL 會讀取訊息佇列交易式寄不出的信件佇列上的每個訊息，並為每個已佇列的元件訊息具現化例外狀況類別。</span><span class="sxs-lookup"><span data-stu-id="5fad0-128">When started, the DLQL reads each message on the Message Queuing transactional dead letter queue and instantiates the exception class for each queued components message.</span></span> <span data-ttu-id="5fad0-129">一旦通過佇列，它就會等待新的訊息。</span><span class="sxs-lookup"><span data-stu-id="5fad0-129">After one pass through the queue, it waits for new messages.</span></span> <span data-ttu-id="5fad0-130">然後，它會在每個新的寄不出的信件佇列訊息抵達時進行處理。</span><span class="sxs-lookup"><span data-stu-id="5fad0-130">It then processes each new dead letter queue message as it arrives.</span></span>

<span data-ttu-id="5fad0-131">如果您需要介入此處所述的程式，或如果您需要將有害訊息移出其最終的靜止佇列，請使用訊息移動器公用程式。</span><span class="sxs-lookup"><span data-stu-id="5fad0-131">If you need to intervene in the process described here or if you need to move a poison message out of its final resting queue, use the message mover utility.</span></span> <span data-ttu-id="5fad0-132">如需訊息移動器公用程式的詳細資訊，請參閱 [處理錯誤](handling-errors-in-queued-components.md)。</span><span class="sxs-lookup"><span data-stu-id="5fad0-132">For more information on the message mover utility, see [Handling Errors](handling-errors-in-queued-components.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="5fad0-133">相關主題</span><span class="sxs-lookup"><span data-stu-id="5fad0-133">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5fad0-134">用戶端錯誤</span><span class="sxs-lookup"><span data-stu-id="5fad0-134">Client-Side Errors</span></span>](client-side-errors.md)
</dt> <dt>

[<span data-ttu-id="5fad0-135">伺服器端錯誤</span><span class="sxs-lookup"><span data-stu-id="5fad0-135">Server-Side Errors</span></span>](server-side-errors.md)
</dt> </dl>

 

 



