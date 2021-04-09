---
title: 回呼連接
description: RAS 支援在遠端伺服器掛斷的連接，然後回呼用戶端以建立連線。
ms.assetid: 25f0e84d-8900-4efe-b07d-59f25186c976
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9aabe3bf5503f16d7d27e44e02dc19ccb2a6f2e5
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "103682988"
---
# <a name="callback-connections"></a><span data-ttu-id="95773-103">回呼連接</span><span class="sxs-lookup"><span data-stu-id="95773-103">Callback Connections</span></span>

<span data-ttu-id="95773-104">RAS 支援在遠端伺服器掛斷的連接，然後回呼用戶端以建立連線。</span><span class="sxs-lookup"><span data-stu-id="95773-104">RAS supports connections in which the remote server hangs up and then calls back to the client to establish the connection.</span></span>

<span data-ttu-id="95773-105">針對可連接到 RAS 伺服器的每個使用者，伺服器會儲存回呼屬性來控制連接的建立方式。</span><span class="sxs-lookup"><span data-stu-id="95773-105">For each user that can connect to a RAS server, the server stores a callback attribute that controls how the connection is made.</span></span> <span data-ttu-id="95773-106">預設屬性為 [無回呼]，這表示使用者不需要回呼就能連線到 RAS 伺服器。</span><span class="sxs-lookup"><span data-stu-id="95773-106">The default attribute is No Callback, which means that the user can connect to the RAS server without a callback.</span></span> <span data-ttu-id="95773-107">或者，RAS 伺服器的系統管理員可以將預設值或設定為呼叫端回呼屬性指派給使用者。</span><span class="sxs-lookup"><span data-stu-id="95773-107">Alternatively, the administrator of the RAS server can assign to a user either the Preset or Set-By-Caller callback attribute.</span></span>

<span data-ttu-id="95773-108">針對指派預設限制的使用者，系統管理員會指定 RAS 伺服器必須回呼才能建立連線的電話號碼。</span><span class="sxs-lookup"><span data-stu-id="95773-108">For a user assigned the Preset restriction, the administrator specifies a phone number that the RAS server must call back to establish a connection.</span></span> <span data-ttu-id="95773-109">使用者不能指定不同的數位，也無法在沒有回呼的情況下建立連接。</span><span class="sxs-lookup"><span data-stu-id="95773-109">The user cannot specify a different number, and the connection cannot be made without a callback.</span></span>

<span data-ttu-id="95773-110">遠端存取連線管理員和遠端伺服器會自動處理預設回呼作業。</span><span class="sxs-lookup"><span data-stu-id="95773-110">A Preset callback operation is handled automatically by the Remote Access Connection Manager and the remote server.</span></span> <span data-ttu-id="95773-111">RAS 用戶端應用程式不需要執行任何動作，而是在回呼作業的各種狀態期間呼叫通知處理常式時，將意見反應提供給使用者。</span><span class="sxs-lookup"><span data-stu-id="95773-111">The RAS client application does not need to do anything other than provide feedback to the user when the notification handler is called during the various states of the callback operation.</span></span>

<span data-ttu-id="95773-112">指派給 [由呼叫者] 許可權的使用者可以選擇使用或不使用回呼連接。</span><span class="sxs-lookup"><span data-stu-id="95773-112">A user assigned the Set By Caller privilege can choose to connect either with or without a callback.</span></span> <span data-ttu-id="95773-113">[**RasDial**](/windows/desktop/api/Ras/nf-ras-rasdiala)呼叫會使用 [**RASDIALPARAMS**](/previous-versions/windows/desktop/legacy/aa377238(v=vs.85))結構的 **szCallbackNumber** 成員來表示選擇。</span><span class="sxs-lookup"><span data-stu-id="95773-113">The [**RasDial**](/windows/desktop/api/Ras/nf-ras-rasdiala) call uses the **szCallbackNumber** member of the [**RASDIALPARAMS**](/previous-versions/windows/desktop/legacy/aa377238(v=vs.85)) structure to indicate the choice.</span></span>

<span data-ttu-id="95773-114">**SzCallbackNumber** 成員可以直接指定回呼號碼;或者，若要建立沒有回呼的連接， **szCallbackNumber** 可以指向空字串 ""。</span><span class="sxs-lookup"><span data-stu-id="95773-114">The **szCallbackNumber** member can simply specify the callback number; or, to establish the connection without a callback, **szCallbackNumber** can point to an empty string, "".</span></span> <span data-ttu-id="95773-115">在上述任何一種情況下，「遠端存取」連線管理員會自動處理連接操作。</span><span class="sxs-lookup"><span data-stu-id="95773-115">In either of these cases, the Remote Access Connection Manager handles the connection operation automatically.</span></span> <span data-ttu-id="95773-116">如同使用預設回呼作業，RAS 用戶端不需要執行任何動作，就能將意見反應提供給使用者。</span><span class="sxs-lookup"><span data-stu-id="95773-116">As with a Preset callback operation, the RAS client does not need to perform any action other than to provide feedback to the user.</span></span>

<span data-ttu-id="95773-117">如果 [**RasDial**](/windows/desktop/api/Ras/nf-ras-rasdiala) 呼叫啟用 [暫停狀態](paused-states.md)， **szCallbackNumber** 可指向星號字串 " \* "，以表示連接作業應進入暫停狀態，以允許使用者輸入回呼號碼。</span><span class="sxs-lookup"><span data-stu-id="95773-117">If the [**RasDial**](/windows/desktop/api/Ras/nf-ras-rasdiala) call enables [paused states](paused-states.md), **szCallbackNumber** can point to an asterisk string, "\*", to indicate that the connection operation should enter a paused state to allow the user to type in the callback number.</span></span> <span data-ttu-id="95773-118">在此情況下，由呼叫者使用者設定的連接作業，會在遠端伺服器驗證使用者之後進入暫停狀態。</span><span class="sxs-lookup"><span data-stu-id="95773-118">In this case, the connection operation for a Set By Caller user enters a paused state after the remote server has authenticated the user.</span></span> <span data-ttu-id="95773-119">在暫停狀態期間，RAS 用戶端會取得使用者的回呼號碼輸入。</span><span class="sxs-lookup"><span data-stu-id="95773-119">During the paused state, the RAS client gets the callback number input from the user.</span></span> <span data-ttu-id="95773-120">然後，用戶端會藉由進行第二個 **RasDial** 呼叫（其中 **szCallbackNumber** 指定使用者提供的數位）來繼續連接作業。</span><span class="sxs-lookup"><span data-stu-id="95773-120">The client then resumes the connection operation by making a second **RasDial** call in which **szCallbackNumber** specifies the number supplied by the user.</span></span>

> [!Note]  
> <span data-ttu-id="95773-121">如果未啟用暫停狀態，則當 **szCallbackNumber** 指向星號字串 "" 時，會有不同的意義 \* 。</span><span class="sxs-lookup"><span data-stu-id="95773-121">If paused states are not enabled there is a different meaning when **szCallbackNumber** points to an asterisk string, "\*".</span></span> <span data-ttu-id="95773-122">在此情況下，星號表示回呼號碼會儲存在 [**RasDial**](/windows/desktop/api/Ras/nf-ras-rasdiala) 呼叫所指定的電話簿檔案中。</span><span class="sxs-lookup"><span data-stu-id="95773-122">In this case, the asterisk indicates that the callback number is stored in the phone-book file specified by the [**RasDial**](/windows/desktop/api/Ras/nf-ras-rasdiala) call.</span></span>

 

<span data-ttu-id="95773-123">在回呼的事件中， [**RasDial**](/windows/desktop/api/Ras/nf-ras-rasdiala) 的呼叫會等到伺服器回呼用戶端之後才會返回。</span><span class="sxs-lookup"><span data-stu-id="95773-123">In the event of a callback, the call to [**RasDial**](/windows/desktop/api/Ras/nf-ras-rasdiala) does not return until after the server has called back the client.</span></span>

 

 