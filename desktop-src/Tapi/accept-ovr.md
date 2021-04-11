---
description: 在某些環境中，使用者並不會自動收到供應專案來電的警示，例如透過響鈴或透過其電腦螢幕上的訊息。
ms.assetid: 50684e2a-0799-458b-9402-0958e35026d7
title: 接受
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1dd23d8ca1ed483b23d1b56fe98721b9fc53fb3d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104191252"
---
# <a name="accept"></a><span data-ttu-id="c2719-103">接受</span><span class="sxs-lookup"><span data-stu-id="c2719-103">Accept</span></span>

<span data-ttu-id="c2719-104">在某些環境中，使用者並不會自動收到供應專案來電的警示，例如透過響鈴或透過其電腦螢幕上的訊息。</span><span class="sxs-lookup"><span data-stu-id="c2719-104">In some environments, a user is not automatically alerted to an offering call, such as by ringing or by a message on their computer screen.</span></span> <span data-ttu-id="c2719-105">接受作業會開始發出警示的程式， (通常會響鈴) ，而 [回應](answer-ovr.md) 作業會在之後進行。</span><span class="sxs-lookup"><span data-stu-id="c2719-105">The accept operation starts the process of alerting (usually ringing), and the [answer](answer-ovr.md) operation takes place afterward.</span></span> <span data-ttu-id="c2719-106">應用程式可能會卸載會話 [、將它](drop-ovr.md) 重新 [導向](redirect-ovr.md) 或接受。</span><span class="sxs-lookup"><span data-stu-id="c2719-106">The application may [drop](drop-ovr.md) the session, [redirect](redirect-ovr.md) it, or accept it.</span></span>

<span data-ttu-id="c2719-107">如果目前的服務提供者支援，則應用程式可以選擇在接受時傳送使用者的資訊。</span><span class="sxs-lookup"><span data-stu-id="c2719-107">If the current service provider supports it, the application has the option to send user-user information at the time of the accept.</span></span> <span data-ttu-id="c2719-108">不保證網路會將這項資訊傳遞給呼叫方。</span><span class="sxs-lookup"><span data-stu-id="c2719-108">There is no guarantee that the network will deliver this information to the calling party.</span></span>

<span data-ttu-id="c2719-109">並非所有服務提供者都支援使用這項作業。</span><span class="sxs-lookup"><span data-stu-id="c2719-109">Not all service providers support use of this operation.</span></span>

<span data-ttu-id="c2719-110">**TAPI 2.x：** 請參閱 [**lineAccept**](/windows/win32/api/tapi/nf-tapi-lineaccept)。</span><span class="sxs-lookup"><span data-stu-id="c2719-110">**TAPI 2.x:** See [**lineAccept**](/windows/win32/api/tapi/nf-tapi-lineaccept).</span></span>

 

 
