---
description: 有些應用程式需要在事件發生之前，或在事件發生時，或兩者都收到連接事件的通知。 您可以建立 DLL，以接收連接事件的前進和事後通知。
ms.assetid: 692eb8f2-1c53-4535-b44d-babb30eecd9c
title: 接收連接通知
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c054d4f7bb78f610afe6c1cbdf028416de7b5596
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104510887"
---
# <a name="receiving-connection-notifications"></a><span data-ttu-id="b723f-104">接收連接通知</span><span class="sxs-lookup"><span data-stu-id="b723f-104">Receiving Connection Notifications</span></span>

<span data-ttu-id="b723f-105">有些應用程式需要在事件發生之前，或在事件發生時，或兩者都收到連接事件的通知。</span><span class="sxs-lookup"><span data-stu-id="b723f-105">Some applications need to receive notification of connection events, either before the event, just after it occurs, or both.</span></span> <span data-ttu-id="b723f-106">您可以建立 DLL，以接收連接事件的前進和事後通知。</span><span class="sxs-lookup"><span data-stu-id="b723f-106">You can create a DLL to receive advance and after-the-fact notification of connection events.</span></span>

<span data-ttu-id="b723f-107">遠端存取服務 (RAS) ，是需要接收連接事件之提前通知的應用程式範例。</span><span class="sxs-lookup"><span data-stu-id="b723f-107">An example of an application that needs to receive advance notification of a connection event is the Remote Access Service (RAS).</span></span> <span data-ttu-id="b723f-108">必須先通知 RAS，才能進行連線，因為可能需要先建立數據機連線，才能進行網路連線。</span><span class="sxs-lookup"><span data-stu-id="b723f-108">RAS needs to be informed before a connection is made because it may be necessary to establish a modem connection before making the network connection.</span></span>

<span data-ttu-id="b723f-109">同樣地，在建立連線之後，應用程式可能需要清除資源，因此需要連接後通知。</span><span class="sxs-lookup"><span data-stu-id="b723f-109">Similarly, applications may need to clean up resources after the connection is made, therefore requiring a post-connection notification.</span></span>

<span data-ttu-id="b723f-110">有興趣接收「前進」和「事後」連接事件通知的應用程式，必須提供可匯出兩個函式（ [**AddConnectNotify**](/windows/desktop/api/Npapi/nf-npapi-addconnectnotify) 和 [**CANCELCONNECTNOTIFY**](/windows/desktop/api/Npapi/nf-npapi-cancelconnectnotify)）的 DLL。</span><span class="sxs-lookup"><span data-stu-id="b723f-110">Applications interested in receiving advance and after-the-fact notification of connection events must supply a DLL that exports two functions, [**AddConnectNotify**](/windows/desktop/api/Npapi/nf-npapi-addconnectnotify) and [**CancelConnectNotify**](/windows/desktop/api/Npapi/nf-npapi-cancelconnectnotify).</span></span>

<span data-ttu-id="b723f-111">在您執行這些函式之後，您必須依照 [註冊接收連接通知](registering-to-receive-connection-notifications.md)中所述的方式註冊 DLL。</span><span class="sxs-lookup"><span data-stu-id="b723f-111">After you implement these functions, you must register your DLL as described in [Registering to Receive Connection Notifications](registering-to-receive-connection-notifications.md).</span></span>

 

 



