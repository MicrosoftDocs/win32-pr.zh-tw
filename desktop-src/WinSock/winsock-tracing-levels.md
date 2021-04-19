---
description: 深入瞭解： Winsock 追蹤層級
ms.assetid: a92bc4d2-257a-478a-b10d-4fada4323c9b
title: Winsock 追蹤層級
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b225558015fb823cd02028a1ae1433d3d0549896
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106975818"
---
# <a name="winsock-tracing-levels"></a><span data-ttu-id="d4bbb-103">Winsock 追蹤層級</span><span class="sxs-lookup"><span data-stu-id="d4bbb-103">Winsock Tracing Levels</span></span>

## <a name="levels-of-winsock-tracing"></a><span data-ttu-id="d4bbb-104">Winsock 追蹤的層級</span><span class="sxs-lookup"><span data-stu-id="d4bbb-104">Levels of Winsock Tracing</span></span>

<span data-ttu-id="d4bbb-105">Winsock 追蹤有兩種可能的記錄層級：</span><span class="sxs-lookup"><span data-stu-id="d4bbb-105">There are two levels of logging possible in Winsock tracing:</span></span>

-   <span data-ttu-id="d4bbb-106">資訊</span><span class="sxs-lookup"><span data-stu-id="d4bbb-106">Information</span></span>
-   <span data-ttu-id="d4bbb-107">「詳細資訊」</span><span class="sxs-lookup"><span data-stu-id="d4bbb-107">Verbose</span></span>

<span data-ttu-id="d4bbb-108">資訊層級會追蹤通訊端建立和關閉事件，以及任何發生在通訊端上的錯誤。</span><span class="sxs-lookup"><span data-stu-id="d4bbb-108">The information level traces socket create and close events, as well as any errors that occur on the socket.</span></span>

<span data-ttu-id="d4bbb-109">詳細資訊層級包含資訊層級的事件，並新增了傳送和接收事件的額外追蹤。</span><span class="sxs-lookup"><span data-stu-id="d4bbb-109">The verbose level includes the information level events, and adds additional tracing for send and receive events.</span></span> <span data-ttu-id="d4bbb-110">詳細資訊記錄會用來捕捉緩衝區損毀問題以及寫入不良的應用程式。</span><span class="sxs-lookup"><span data-stu-id="d4bbb-110">The verbose logging would be used to catch buffer corruption issues as well as poorly written applications.</span></span>

<span data-ttu-id="d4bbb-111">[資訊] 或 [詳細資訊] 層級可以與 Winsock 網路事件追蹤一起使用。</span><span class="sxs-lookup"><span data-stu-id="d4bbb-111">Either the information or verbose level can be used with the Winsock Network Event tracing.</span></span> <span data-ttu-id="d4bbb-112">Winsock 類別目錄變更追蹤只支援資訊層級。</span><span class="sxs-lookup"><span data-stu-id="d4bbb-112">The Winsock Catalog Change tracing supports only information level.</span></span>

## <a name="information-event-tracing"></a><span data-ttu-id="d4bbb-113">資訊事件追蹤</span><span class="sxs-lookup"><span data-stu-id="d4bbb-113">Information Event Tracing</span></span>

<span data-ttu-id="d4bbb-114">下列清單詳細說明在資訊層級追蹤的 Winsock 網路事件通訊端作業：</span><span class="sxs-lookup"><span data-stu-id="d4bbb-114">The following list details those Winsock network event socket operations that are traced at the information level:</span></span>

-   <span data-ttu-id="d4bbb-115">通訊端建立</span><span class="sxs-lookup"><span data-stu-id="d4bbb-115">Socket creation</span></span>

    <span data-ttu-id="d4bbb-116">系統會在建立通訊端時記錄事件，可用來追蹤通訊端的存留期。</span><span class="sxs-lookup"><span data-stu-id="d4bbb-116">An event is logged on socket creation which can be used to trace the lifetime of a socket.</span></span> <span data-ttu-id="d4bbb-117">這些事件也包含在接聽通訊端上接受連接所建立的通訊端。</span><span class="sxs-lookup"><span data-stu-id="d4bbb-117">These events also includes sockets created by accepting connections on a listening socket.</span></span>

-   <span data-ttu-id="d4bbb-118">繫結</span><span class="sxs-lookup"><span data-stu-id="d4bbb-118">Bind</span></span>

    <span data-ttu-id="d4bbb-119">系統會記錄本機 IP 位址，以協助將 Winsock 追蹤資訊與應用程式的通訊端呼叫產生關聯。</span><span class="sxs-lookup"><span data-stu-id="d4bbb-119">The local IP address is logged to help correlate the Winsock tracing information to an application's socket calls.</span></span>

-   <span data-ttu-id="d4bbb-120">連線</span><span class="sxs-lookup"><span data-stu-id="d4bbb-120">Connect</span></span>

    <span data-ttu-id="d4bbb-121">系統會記錄已連接通訊端的遠端 IP 位址，以協助將 Winsock 追蹤資訊與應用程式的通訊端呼叫產生關聯。</span><span class="sxs-lookup"><span data-stu-id="d4bbb-121">The remote IP address of the connected socket is logged to help correlate the Winsock tracing information to an application's socket calls.</span></span>

-   <span data-ttu-id="d4bbb-122">Winsock 起始的中止和取消</span><span class="sxs-lookup"><span data-stu-id="d4bbb-122">Winsock-initiated aborts and cancels</span></span>

    <span data-ttu-id="d4bbb-123">每當 Winsock 主動中止或取消要求時，就會記錄事件。</span><span class="sxs-lookup"><span data-stu-id="d4bbb-123">Anytime Winsock actively aborts or cancels a request, the event is logged.</span></span>

-   <span data-ttu-id="d4bbb-124">傳輸起始的重設</span><span class="sxs-lookup"><span data-stu-id="d4bbb-124">Transport initiated resets</span></span>

    <span data-ttu-id="d4bbb-125">當基礎傳輸表示連接已重設時，會記錄事件。</span><span class="sxs-lookup"><span data-stu-id="d4bbb-125">Anytime the underlying transport indicates a connection has been reset, the event is logged.</span></span>

-   <span data-ttu-id="d4bbb-126">傳送和接收錯誤</span><span class="sxs-lookup"><span data-stu-id="d4bbb-126">Send and receive errors</span></span>

    <span data-ttu-id="d4bbb-127">每當基礎傳輸的傳送或接收呼叫失敗時，就會記錄事件。</span><span class="sxs-lookup"><span data-stu-id="d4bbb-127">Whenever a send or receive call to the underlying transport fails, the event is logged.</span></span>

-   <span data-ttu-id="d4bbb-128">通訊端中斷連線和關閉</span><span class="sxs-lookup"><span data-stu-id="d4bbb-128">Socket disconnect and close</span></span>

    <span data-ttu-id="d4bbb-129">當通訊端控制碼關閉時，就會記錄事件。</span><span class="sxs-lookup"><span data-stu-id="d4bbb-129">An event is logged when a socket handle is closed.</span></span>

## <a name="verbose-event-tracing"></a><span data-ttu-id="d4bbb-130">詳細資訊事件追蹤</span><span class="sxs-lookup"><span data-stu-id="d4bbb-130">Verbose Event Tracing</span></span>

<span data-ttu-id="d4bbb-131">所有資訊事件都是在詳細資訊層級進行追蹤。</span><span class="sxs-lookup"><span data-stu-id="d4bbb-131">All of the information events are traced at the verbose level.</span></span> <span data-ttu-id="d4bbb-132">下列清單詳細說明在詳細資訊層級追蹤的額外 Winsock 網路事件通訊端作業：</span><span class="sxs-lookup"><span data-stu-id="d4bbb-132">The following list details those additional Winsock network event socket operations that are traced at the verbose level:</span></span>

-   <span data-ttu-id="d4bbb-133">傳送和接收緩衝區</span><span class="sxs-lookup"><span data-stu-id="d4bbb-133">Send and receive buffers</span></span>

    <span data-ttu-id="d4bbb-134">當傳送和接收呼叫張貼到 Winsock，以及完成這些呼叫時，會記錄使用者緩衝區位址和長度的事件。</span><span class="sxs-lookup"><span data-stu-id="d4bbb-134">Events are logged of user buffer addresses and lengths when send and receive calls are posted to Winsock, as well as upon completion of these calls.</span></span> <span data-ttu-id="d4bbb-135">這對於診斷緩衝區重複使用問題以及無效率的緩衝區使用來說很有用。</span><span class="sxs-lookup"><span data-stu-id="d4bbb-135">This is useful for diagnosing buffer re-use issues as well as inefficient use of buffers.</span></span>

-   <span data-ttu-id="d4bbb-136">通訊端選項</span><span class="sxs-lookup"><span data-stu-id="d4bbb-136">Socket options</span></span>

    <span data-ttu-id="d4bbb-137">當應用程式變更特定通訊端選項值時，就會記錄事件。</span><span class="sxs-lookup"><span data-stu-id="d4bbb-137">An event is logged when an application changes certain socket option values.</span></span> <span data-ttu-id="d4bbb-138">記錄的部分選項包含 \_ SNDBUF，因此 \_ RCVBUF、SIO \_ 啟用 \_ 迴圈 \_ 佇列和 FIONBIO。</span><span class="sxs-lookup"><span data-stu-id="d4bbb-138">Some of the options logged include SO\_SNDBUF, SO\_RCVBUF, SIO\_ENABLE\_CIRCULAR\_QUEUEING, and FIONBIO.</span></span>

-   <span data-ttu-id="d4bbb-139">WSAPoll 並選取</span><span class="sxs-lookup"><span data-stu-id="d4bbb-139">WSAPoll and select</span></span>

    <span data-ttu-id="d4bbb-140">系統會記錄應用程式使用 [**WSAPoll**](/windows/win32/api/winsock2/nf-winsock2-wsapoll) 的事件，並 [**選取**](/windows/desktop/api/Winsock2/nf-winsock2-select) 可用於尋找效能瓶頸的呼叫。</span><span class="sxs-lookup"><span data-stu-id="d4bbb-140">An event is logged of an application's usage of [**WSAPoll**](/windows/win32/api/winsock2/nf-winsock2-wsapoll) and [**select**](/windows/desktop/api/Winsock2/nf-winsock2-select) calls which can be used to find performance bottlenecks.</span></span>

-   <span data-ttu-id="d4bbb-141">Winsock 起始的中止和取消</span><span class="sxs-lookup"><span data-stu-id="d4bbb-141">Winsock-initiated aborts and cancels</span></span>

    <span data-ttu-id="d4bbb-142">每當 Winsock 主動中止或取消要求時，就會記錄事件。</span><span class="sxs-lookup"><span data-stu-id="d4bbb-142">Anytime Winsock actively aborts or cancels a request, the event is logged.</span></span>

-   <span data-ttu-id="d4bbb-143">事件遮罩</span><span class="sxs-lookup"><span data-stu-id="d4bbb-143">Event mask</span></span>

    <span data-ttu-id="d4bbb-144">事件是由應用程式註冊以使用 [**WSAEventSelect**](/windows/desktop/api/Winsock2/nf-winsock2-wsaeventselect) 函式的事件遮罩來記錄。</span><span class="sxs-lookup"><span data-stu-id="d4bbb-144">An event is logged of the event mask an application registers for using the [**WSAEventSelect**](/windows/desktop/api/Winsock2/nf-winsock2-wsaeventselect) function.</span></span>

-   <span data-ttu-id="d4bbb-145">資料包</span><span class="sxs-lookup"><span data-stu-id="d4bbb-145">Datagram</span></span>

    <span data-ttu-id="d4bbb-146">每當資料包抵達且沒有可複製的緩衝區空間時，就會記錄事件。</span><span class="sxs-lookup"><span data-stu-id="d4bbb-146">An event is logged whenever a datagram arrives and there is no buffer space in which to copy it.</span></span>

## <a name="related-topics"></a><span data-ttu-id="d4bbb-147">相關主題</span><span class="sxs-lookup"><span data-stu-id="d4bbb-147">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d4bbb-148">Winsock 追蹤的控制權</span><span class="sxs-lookup"><span data-stu-id="d4bbb-148">Control of Winsock Tracing</span></span>](control-of-winsock-tracing.md)
</dt> <dt>

[<span data-ttu-id="d4bbb-149">Winsock 追蹤</span><span class="sxs-lookup"><span data-stu-id="d4bbb-149">Winsock Tracing</span></span>](winsock-tracing.md)
</dt> <dt>

[<span data-ttu-id="d4bbb-150">Winsock 目錄變更追蹤詳細資料</span><span class="sxs-lookup"><span data-stu-id="d4bbb-150">Winsock Catalog Change Tracing Details</span></span>](winsock-layered-service-provider-tracing-event-details.md)
</dt> <dt>

[<span data-ttu-id="d4bbb-151">Winsock 網路事件追蹤詳細資料</span><span class="sxs-lookup"><span data-stu-id="d4bbb-151">Winsock Network Event Tracing Details</span></span>](winsock-tracing-event-details.md)
</dt> </dl>

 

 
