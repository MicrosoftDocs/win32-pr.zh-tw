---
title: 完成通知
description: 在完成連接作業之前，遠端存取連線管理員會繼續進度通知。
ms.assetid: 2c3b0d03-1cb7-4fa4-a7fa-bcfe623b791f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b4b949eb7dcc0f09d05d2fb272f4f3d36da40fac
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104021489"
---
# <a name="completion-notifications"></a><span data-ttu-id="91d59-103">完成通知</span><span class="sxs-lookup"><span data-stu-id="91d59-103">Completion Notifications</span></span>

<span data-ttu-id="91d59-104">在完成連接作業之前，遠端存取連線管理員會繼續進度通知。</span><span class="sxs-lookup"><span data-stu-id="91d59-104">The Remote Access Connection Manager continues progress notifications until the connection operation has been completed.</span></span> <span data-ttu-id="91d59-105">這會發生在下列情況：</span><span class="sxs-lookup"><span data-stu-id="91d59-105">This occurs in the following situations:</span></span>

-   <span data-ttu-id="91d59-106">處理常式會收到 RASCS \_ 連接，或 RASCS \_ 中斷連線的通知。</span><span class="sxs-lookup"><span data-stu-id="91d59-106">The handler receives a RASCS\_Connected, or RASCS\_Disconnected notification.</span></span> <span data-ttu-id="91d59-107">RAS 用戶端應用程式可以結束，而不會中斷任何已建立的連接。</span><span class="sxs-lookup"><span data-stu-id="91d59-107">The RAS client application can exit without breaking any established connection.</span></span>
-   <span data-ttu-id="91d59-108">發生錯誤。</span><span class="sxs-lookup"><span data-stu-id="91d59-108">An error occurs.</span></span> <span data-ttu-id="91d59-109">處理常式會收到通知，指出發生錯誤時的錯誤和連接狀態。</span><span class="sxs-lookup"><span data-stu-id="91d59-109">The handler receives a notification indicating the error and the connection state when the error occurred.</span></span> <span data-ttu-id="91d59-110">RAS 用戶端應用程式可能會結束。</span><span class="sxs-lookup"><span data-stu-id="91d59-110">The RAS client application can exit.</span></span>

<span data-ttu-id="91d59-111">在呼叫 [**RasHangUp**](/windows/desktop/api/Ras/nf-ras-rashangupa)之後，RAS 用戶端應用程式不應假設連接作業已完成。</span><span class="sxs-lookup"><span data-stu-id="91d59-111">The RAS client application should not assume the connection operation is complete after calling [**RasHangUp**](/windows/desktop/api/Ras/nf-ras-rashangupa).</span></span> <span data-ttu-id="91d59-112">在結束之前，它應該等待上述其中一個條件。</span><span class="sxs-lookup"><span data-stu-id="91d59-112">It should wait for one of the preceding conditions before exiting.</span></span>

 

 




