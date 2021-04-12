---
title: 暫停狀態
description: 在連接操作期間，遠端伺服器可能會在沒有本機使用者的其他資訊的情況下繼續進行。
ms.assetid: a1a36b2a-33df-4cba-85a6-f4225779cd63
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 914acb85ccf74c92b4bd4119966a421faddeb011
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104316321"
---
# <a name="paused-states"></a><span data-ttu-id="928fb-103">暫停狀態</span><span class="sxs-lookup"><span data-stu-id="928fb-103">Paused States</span></span>

<span data-ttu-id="928fb-104">在連接操作期間，遠端伺服器可能會在沒有本機使用者的其他資訊的情況下繼續進行。</span><span class="sxs-lookup"><span data-stu-id="928fb-104">During a connection operation, there can be times when the remote server cannot proceed without additional information from the local user.</span></span> <span data-ttu-id="928fb-105">從 Windows NT 3.5 開始， [**RasDial**](/windows/desktop/api/Ras/nf-ras-rasdiala) 函數支援暫停狀態。</span><span class="sxs-lookup"><span data-stu-id="928fb-105">Beginning with Windows NT 3.5, the [**RasDial**](/windows/desktop/api/Ras/nf-ras-rasdiala) function supports paused states.</span></span> <span data-ttu-id="928fb-106">暫停狀態可讓遠端存取連線管理員暫停線上作業，讓 RAS 用戶端應用程式可以從使用者收集資訊。</span><span class="sxs-lookup"><span data-stu-id="928fb-106">A paused state allows the Remote Access Connection Manager to suspend a connection operation so the RAS client application can collect information from the user.</span></span>

<span data-ttu-id="928fb-107">暫停狀態在下列情況下很有用：</span><span class="sxs-lookup"><span data-stu-id="928fb-107">Paused states are useful in the following situations:</span></span>

-   <span data-ttu-id="928fb-108">當使用者需要提供 [回呼](callback-connections.md) 號碼時。</span><span class="sxs-lookup"><span data-stu-id="928fb-108">When the user needs to provide a [callback](callback-connections.md) number.</span></span>
-   <span data-ttu-id="928fb-109">當使用者驗證失敗時，使用者可以輸入不同的使用者名稱和密碼。</span><span class="sxs-lookup"><span data-stu-id="928fb-109">When the user authentication fails, the user can type in a different user name and password.</span></span>
-   <span data-ttu-id="928fb-110">當使用者的密碼過期時，使用者可以提供新的密碼。</span><span class="sxs-lookup"><span data-stu-id="928fb-110">When the user's password has expired, the user can provide a new password.</span></span>

<span data-ttu-id="928fb-111">預設會停用暫停狀態支援。</span><span class="sxs-lookup"><span data-stu-id="928fb-111">By default, paused state support is disabled.</span></span> <span data-ttu-id="928fb-112">想要支援暫停狀態的 RAS 用戶端，必須 \_ 在以參數形式傳遞至 [**RasDial**](/windows/desktop/api/Ras/nf-ras-rasdiala)的 [**RASDIALEXTENSIONS**](/previous-versions/windows/desktop/legacy/aa377029(v=vs.85))結構中，設定 RDEOPTS PausedStates 旗標。</span><span class="sxs-lookup"><span data-stu-id="928fb-112">RAS clients that want to support paused states must set the RDEOPTS\_PausedStates flag in the [**RASDIALEXTENSIONS**](/previous-versions/windows/desktop/legacy/aa377029(v=vs.85)) structure passed as a parameter to [**RasDial**](/windows/desktop/api/Ras/nf-ras-rasdiala).</span></span>

<span data-ttu-id="928fb-113">當暫停狀態發生時，遠端存取連線管理員會叫用用戶端的通知處理常式。</span><span class="sxs-lookup"><span data-stu-id="928fb-113">When a paused state occurs, the Remote Access Connection Manager invokes the client's notification handler.</span></span> <span data-ttu-id="928fb-114">如果停用暫停狀態支援，則通知訊息會指出錯誤，且連接作業會失敗。</span><span class="sxs-lookup"><span data-stu-id="928fb-114">If paused state support is disabled, the notification message indicates an error, and the connection operation fails.</span></span> <span data-ttu-id="928fb-115">若已啟用，連線管理員會暫停連線作業以等候 RAS 用戶端的回應。</span><span class="sxs-lookup"><span data-stu-id="928fb-115">If it is enabled, the Connection Manager pauses the connection operation to wait for the RAS client's response.</span></span> <span data-ttu-id="928fb-116">RAS 用戶端可以透過第二個 [**RasDial**](/windows/desktop/api/Ras/nf-ras-rasdiala) 呼叫來繼續連線作業，或呼叫 [**RasHangUp**](/windows/desktop/api/Ras/nf-ras-rashangupa) 函式將它終止。</span><span class="sxs-lookup"><span data-stu-id="928fb-116">The RAS client can resume the connection operation by a second [**RasDial**](/windows/desktop/api/Ras/nf-ras-rasdiala) call, or terminate it by calling the [**RasHangUp**](/windows/desktop/api/Ras/nf-ras-rashangupa) function.</span></span>

<span data-ttu-id="928fb-117">取得使用者的輸入之後，RAS 用戶端會重新開機連接作業，方法是再次呼叫 [**RasDial**](/windows/desktop/api/Ras/nf-ras-rasdiala) 。</span><span class="sxs-lookup"><span data-stu-id="928fb-117">After getting the user's input, the RAS client restarts the connection operation by calling [**RasDial**](/windows/desktop/api/Ras/nf-ras-rasdiala) again.</span></span> <span data-ttu-id="928fb-118">第二個 **RasDial** 呼叫必須指定下列資訊：</span><span class="sxs-lookup"><span data-stu-id="928fb-118">This second **RasDial** call must specify the following information:</span></span>

-   <span data-ttu-id="928fb-119">原始 [**RasDial**](/windows/desktop/api/Ras/nf-ras-rasdiala) 呼叫所傳回的連接控制碼。</span><span class="sxs-lookup"><span data-stu-id="928fb-119">The connection handle that was returned by the original [**RasDial**](/windows/desktop/api/Ras/nf-ras-rasdiala) call.</span></span>
-   <span data-ttu-id="928fb-120">與原始 [**RasDial**](/windows/desktop/api/Ras/nf-ras-rasdiala) 呼叫相同的通知處理常式。</span><span class="sxs-lookup"><span data-stu-id="928fb-120">The same notification handler as the original [**RasDial**](/windows/desktop/api/Ras/nf-ras-rasdiala) call.</span></span>
-   <span data-ttu-id="928fb-121">使用者在 [**RASDIALPARAMS**](/previous-versions/windows/desktop/legacy/aa377238(v=vs.85)) 結構中適當的成員輸入。</span><span class="sxs-lookup"><span data-stu-id="928fb-121">The user's input in the appropriate members of the [**RASDIALPARAMS**](/previous-versions/windows/desktop/legacy/aa377238(v=vs.85)) structure.</span></span> <span data-ttu-id="928fb-122">**RASDIALPARAMS** 結構的其他成員應具有與原始 [**RasDial**](/windows/desktop/api/Ras/nf-ras-rasdiala)呼叫中所指定的相同資訊。</span><span class="sxs-lookup"><span data-stu-id="928fb-122">Other members of the **RASDIALPARAMS** structure should have the same information as specified in the original [**RasDial**](/windows/desktop/api/Ras/nf-ras-rasdiala) call.</span></span>

<span data-ttu-id="928fb-123">無法從通知處理常式內進行第二個 [**RasDial**](/windows/desktop/api/Ras/nf-ras-rasdiala) 呼叫。</span><span class="sxs-lookup"><span data-stu-id="928fb-123">The second [**RasDial**](/windows/desktop/api/Ras/nf-ras-rasdiala) call cannot be made from within the notification handler.</span></span>

 

 