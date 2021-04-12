---
title: 註冊變更通知
description: 用戶端可以註冊，以接收路由表管理員中儲存之路由資訊變更的通知。 此要求只能在用戶端向路由表管理員註冊之後進行。
ms.assetid: 90dc98eb-0d0b-4450-848b-c7cedab75a52
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9c3a98062fee73c481c1f47c32fa7eeb5465a112
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104300680"
---
# <a name="registering-for-change-notification"></a><span data-ttu-id="05e3d-104">註冊變更通知</span><span class="sxs-lookup"><span data-stu-id="05e3d-104">Registering for Change Notification</span></span>

<span data-ttu-id="05e3d-105">用戶端可以註冊，以接收路由表管理員中儲存之路由資訊變更的通知。</span><span class="sxs-lookup"><span data-stu-id="05e3d-105">A client can register to receive notification of changes to routing information that is stored in the routing table manager.</span></span> <span data-ttu-id="05e3d-106">此要求只能在用戶端向路由表管理員註冊之後進行。</span><span class="sxs-lookup"><span data-stu-id="05e3d-106">This request can only be made after a client has registered with the routing table manager.</span></span>

<span data-ttu-id="05e3d-107">若要註冊變更通知，用戶端必須呼叫 [**RtmRegisterForChangeNotification**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmregisterforchangenotification)，並指定用戶端必須接收通知的變更類型。</span><span class="sxs-lookup"><span data-stu-id="05e3d-107">To register for change notification, a client must call [**RtmRegisterForChangeNotification**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmregisterforchangenotification), specifying the types of changes for which the client must receive notification.</span></span> <span data-ttu-id="05e3d-108">如果用戶端必須在特定目的地發生變更時收到通知，用戶端會針對每個目的地呼叫 [**RtmMarkDestForChangeNotification**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmmarkdestforchangenotification) 一次。</span><span class="sxs-lookup"><span data-stu-id="05e3d-108">If the client must be notified of change to specific destinations, the client calls [**RtmMarkDestForChangeNotification**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmmarkdestforchangenotification) once for each destination.</span></span>

<span data-ttu-id="05e3d-109">用戶端可以藉由呼叫 [**RtmDeregisterFromChangeNotification**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmderegisterfromchangenotification)來停止接收變更通知。</span><span class="sxs-lookup"><span data-stu-id="05e3d-109">The client can stop receiving change notifications by calling [**RtmDeregisterFromChangeNotification**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmderegisterfromchangenotification).</span></span>

<span data-ttu-id="05e3d-110">如需示範如何使用這些函數的範例程式碼，請參閱 [註冊變更通知](register-for-change-notification.md)。</span><span class="sxs-lookup"><span data-stu-id="05e3d-110">For sample code that shows how to use these functions, see [Register For Change Notification](register-for-change-notification.md).</span></span>

 

 




