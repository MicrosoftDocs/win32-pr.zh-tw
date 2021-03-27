---
description: 同步處理管理員包含使用者介面元件，例如 SyncMgr 服務中的索引標籤式對話方塊、錯誤對話方塊和進度對話方塊。
title: 同步處理管理員架構
ms.topic: article
ms.date: 05/31/2018
ms.assetid: db338835-ca8d-4e9f-973a-8eb081feda2b
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: f178b407c1f7d568c9de2ce7c81d937e7d1cdef4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103695647"
---
# <a name="synchronization-manager-architecture"></a><span data-ttu-id="ba9fd-103">同步處理管理員架構</span><span class="sxs-lookup"><span data-stu-id="ba9fd-103">Synchronization Manager Architecture</span></span>

<span data-ttu-id="ba9fd-104">同步處理管理員包含使用者介面元件，例如 SyncMgr 服務中的索引標籤式對話方塊、錯誤對話方塊和進度對話方塊。</span><span class="sxs-lookup"><span data-stu-id="ba9fd-104">The Synchronization Manager includes user interface components, such as the tabbed dialog boxes in the SyncMgr service, error dialogs, and progress dialogs.</span></span> <span data-ttu-id="ba9fd-105">使用者介面元件可讓使用者排程同步處理的應用程式，並設定自動同步處理，以與指定的系統事件一起發生。</span><span class="sxs-lookup"><span data-stu-id="ba9fd-105">With the user interface components the end user can schedule applications for synchronization and set up automatic synchronization to occur in conjunction with specified system events.</span></span> <span data-ttu-id="ba9fd-106">例如，您可以在使用者登入或系統關機時叫用 SyncMgr。</span><span class="sxs-lookup"><span data-stu-id="ba9fd-106">For example, the SyncMgr can be invoked at user logon or system shutdown.</span></span> <span data-ttu-id="ba9fd-107">使用者也可以叫用手動同步處理。</span><span class="sxs-lookup"><span data-stu-id="ba9fd-107">The user can also invoke a manual synchronization.</span></span>

<span data-ttu-id="ba9fd-108">使用者選取應用程式，並指定要同步處理之應用程式內的專案，並設定觸發程式事件。</span><span class="sxs-lookup"><span data-stu-id="ba9fd-108">The user selects an application and specifies the items within the application to be synchronized and sets a trigger event.</span></span> <span data-ttu-id="ba9fd-109">例如，在電子郵件應用程式中，[收件匣]、[寄件匣] 或其他包含訊息的資料夾可以是應用程式的個別專案。</span><span class="sxs-lookup"><span data-stu-id="ba9fd-109">For example, within an email application, the Inbox, the Outbox, or some other folder containing messages can be a separate item for the application.</span></span>

<span data-ttu-id="ba9fd-110">SyncMgr 也包含程式設計介面，讓應用程式可以註冊以使用同步處理功能、可處理錯誤，以及在同步處理過程中接收進度資訊和通知。</span><span class="sxs-lookup"><span data-stu-id="ba9fd-110">SyncMgr also includes a programming interface so that applications can register to use synchronization features, can process errors, and can receive progress information and notifications during the synchronization process.</span></span>

 

 



