---
description: 接收事件的其中一個最常見的方法是透過執行中的應用程式，例如，可收集並向使用者顯示事件的管理應用程式。
ms.assetid: 380ac556-ba0a-4fae-8b76-0645d99e8583
ms.tgt_platform: multiple
title: 在您的應用程式期間接收事件
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3fd6b9731dd662a92296a86910a6cf8cb231cca1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104026494"
---
# <a name="receiving-events-for-the-duration-of-your-application"></a><span data-ttu-id="2ea78-103">在您的應用程式期間接收事件</span><span class="sxs-lookup"><span data-stu-id="2ea78-103">Receiving Events for the Duration of Your Application</span></span>

<span data-ttu-id="2ea78-104">接收事件的其中一個最常見的方法是透過執行中的應用程式，例如，可收集並向使用者顯示事件的管理應用程式。</span><span class="sxs-lookup"><span data-stu-id="2ea78-104">One of the most common ways to receive an event is through a running application, such as a management application that collects and displays events to a user.</span></span> <span data-ttu-id="2ea78-105">這類應用程式稱為「暫時性」，因為暫時性取用者不會在關閉時收到事件通知。</span><span class="sxs-lookup"><span data-stu-id="2ea78-105">Such applications are called "temporary" because a temporary consumer does not receive event notifications when shut down.</span></span>

<span data-ttu-id="2ea78-106">暫時性取用者會呼叫腳本中的 [**SWbemServices.ExecNotificationQuery**](swbemservices-execnotificationquery.md) ，或在 c + + 中 [**IWbemServices.ExecNotificationQuery**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execnotificationquery) ，以訂閱命名空間中的事件。</span><span class="sxs-lookup"><span data-stu-id="2ea78-106">A temporary consumer calls [**SWbemServices.ExecNotificationQuery**](swbemservices-execnotificationquery.md) in script or [**IWbemServices.ExecNotificationQuery**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execnotificationquery) in C++ to subscribe to events in a namespace.</span></span> <span data-ttu-id="2ea78-107">與此訂用帳戶相關聯的身分識別是呼叫者。</span><span class="sxs-lookup"><span data-stu-id="2ea78-107">The identity associated with this subscription is the caller.</span></span>

<span data-ttu-id="2ea78-108">暫存事件取用者可以在腳本和 c + + 中非同步或半同步方式接收通知。</span><span class="sxs-lookup"><span data-stu-id="2ea78-108">A temporary event consumer can receive notifications either asynchronously or semisynchronously in both scripts and C++.</span></span>

> [!Note]  
> <span data-ttu-id="2ea78-109">基於安全性理由，請務必注意，不建議使用非同步事件通知。</span><span class="sxs-lookup"><span data-stu-id="2ea78-109">For security reasons, it is important to note that asynchronous event notifications are not recommended.</span></span> <span data-ttu-id="2ea78-110">如需詳細資訊，請參閱 [在非同步呼叫上設定安全性](setting-security-on-an-asynchronous-call.md)。</span><span class="sxs-lookup"><span data-stu-id="2ea78-110">For more information, see [Setting Security on an Asynchronous Call](setting-security-on-an-asynchronous-call.md).</span></span> <span data-ttu-id="2ea78-111">事件取用者具有特殊的安全性考慮。</span><span class="sxs-lookup"><span data-stu-id="2ea78-111">Event consumers have special security concerns.</span></span> <span data-ttu-id="2ea78-112">如需詳細資訊，請參閱 [保護 WMI 事件](securing-wmi-events.md)。</span><span class="sxs-lookup"><span data-stu-id="2ea78-112">For more information, see [Securing WMI Events](securing-wmi-events.md).</span></span>

 

<span data-ttu-id="2ea78-113">如需接收非同步事件和同步事件通知的詳細資訊，請參閱 [接收非同步事件通知](receiving-asynchronous-event-notifications.md) 和 [接收半同步事件通知](receiving-synchronous-and-semisynchronous-event-notifications.md)。</span><span class="sxs-lookup"><span data-stu-id="2ea78-113">For more information about receiving asynchronous and semisynchronous event notifications, see [Receiving Asynchronous Event Notifications](receiving-asynchronous-event-notifications.md) and [Receiving Semisynchronous Event Notifications](receiving-synchronous-and-semisynchronous-event-notifications.md).</span></span>

 

 



