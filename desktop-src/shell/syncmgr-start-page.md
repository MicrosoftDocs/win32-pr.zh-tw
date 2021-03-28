---
description: 同步處理管理員提供集中式的標準技術，可在行動電腦或連接到區域網路的電腦上同步處理檔案，以供離線使用。
title: 同步處理管理員
ms.topic: article
ms.date: 05/31/2018
ms.assetid: 6cdac7e5-8985-407a-98bb-936bb20ed069
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbOrient
ms.openlocfilehash: 2fc56b2afec4fdedf98fe213437a27f2592ce72b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104991615"
---
# <a name="synchronization-manager"></a><span data-ttu-id="ca231-103">同步處理管理員</span><span class="sxs-lookup"><span data-stu-id="ca231-103">Synchronization Manager</span></span>

## <a name="purpose"></a><span data-ttu-id="ca231-104">目的</span><span class="sxs-lookup"><span data-stu-id="ca231-104">Purpose</span></span>

<span data-ttu-id="ca231-105">同步處理管理員提供集中式的標準技術，可在行動電腦或連接到區域網路的電腦上同步處理檔案，以供離線使用。</span><span class="sxs-lookup"><span data-stu-id="ca231-105">The Synchronization Manager provides a centralized, standard technology for synchronizing files for offline use on a mobile computer or a computer connected to a local area network.</span></span> <span data-ttu-id="ca231-106">與連線功能、通知 (系統事件通知服務) 和用戶端快取，同步處理管理員會提供基礎結構來支援行動計算。</span><span class="sxs-lookup"><span data-stu-id="ca231-106">Together with the connectivity functions, notifications (System Event Notification Service), and client side caching, the Synchronization Manager provides an infrastructure to support mobile computing.</span></span> <span data-ttu-id="ca231-107">作業系統會提供所有應用程式可使用的整合式模型，而不是每個應用程式執行自己的技術來快取和同步處理網路資源以供本機使用。</span><span class="sxs-lookup"><span data-stu-id="ca231-107">Instead of each application implementing its own technology to cache and synchronize network resources for local use, the operating system provides an integrated model that all applications can use.</span></span> <span data-ttu-id="ca231-108">與通訊協定無關的檔案會進行同步處理。</span><span class="sxs-lookup"><span data-stu-id="ca231-108">Files are synchronized independent of the protocol.</span></span> <span data-ttu-id="ca231-109">例如，電子郵件程式可以使用 SMTP、NMTP 或 POP3 傳送訊息，而瀏覽器可以使用 HTTP，而資料庫可以使用遠端程序呼叫， (RPC)  (RPC) 。</span><span class="sxs-lookup"><span data-stu-id="ca231-109">For example, an email program can transfer its messages using SMTP, NMTP, or POP3, while a browser can use HTTP, and a database can use remote procedure call (RPC) (RPC).</span></span> <span data-ttu-id="ca231-110">開發人員可以在其應用程式中使用同步處理管理員的通用介面，在使用者的本機電腦和網路存放裝置之間同步處理檔案。</span><span class="sxs-lookup"><span data-stu-id="ca231-110">Developers can use the common interface to the Synchronization Manager in their applications to synchronize files between the user's local computer and network storage.</span></span>

## <a name="where-applicable"></a><span data-ttu-id="ca231-111">適用時</span><span class="sxs-lookup"><span data-stu-id="ca231-111">Where applicable</span></span>

<span data-ttu-id="ca231-112">同步處理管理員適用于主要在行動電腦上執行的應用程式。</span><span class="sxs-lookup"><span data-stu-id="ca231-112">The Synchronization Manager is intended for applications that run primarily on mobile computers.</span></span> <span data-ttu-id="ca231-113">在連接到高延遲區域網路的電腦上執行的應用程式，也可能會因為使用同步處理管理員而受益。</span><span class="sxs-lookup"><span data-stu-id="ca231-113">Applications that run on computers connected to high latency local area networks may also benefit from using the Synchronization Manager.</span></span>

## <a name="developer-audience"></a><span data-ttu-id="ca231-114">開發人員對象</span><span class="sxs-lookup"><span data-stu-id="ca231-114">Developer audience</span></span>

<span data-ttu-id="ca231-115">本檔適用于開發行動電腦運算和高延遲區域網路應用程式的軟體發展人員。</span><span class="sxs-lookup"><span data-stu-id="ca231-115">This document is intended for software developers who develop applications for mobile computing and high latency local area networks.</span></span> <span data-ttu-id="ca231-116">本檔提供同步處理管理員所有部分的完整參考，包括同步處理管理員的方法和介面。</span><span class="sxs-lookup"><span data-stu-id="ca231-116">This document provides a complete reference of all parts of the Synchronization Manager including the methods and interfaces to the Synchronization Manager.</span></span>

## <a name="run-time-requirements"></a><span data-ttu-id="ca231-117">執行階段需求求</span><span class="sxs-lookup"><span data-stu-id="ca231-117">Run-time requirements</span></span>

<span data-ttu-id="ca231-118">需要 Windows Server 2003、Windows XP、Windows 2000 或 Windows Millennium Edition (Windows Me) 。</span><span class="sxs-lookup"><span data-stu-id="ca231-118">Requires Windows Server 2003, Windows XP, Windows 2000, or Windows Millennium Edition (Windows Me).</span></span> <span data-ttu-id="ca231-119">也可用於 Microsoft Windows NT 4.0、Windows 98 和 Windows 95 的可轉散發套件。</span><span class="sxs-lookup"><span data-stu-id="ca231-119">Also available as a redistributable for Microsoft Windows NT 4.0, Windows 98, and Windows 95.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="ca231-120">本節內容</span><span class="sxs-lookup"><span data-stu-id="ca231-120">In this section</span></span>



| <span data-ttu-id="ca231-121">主題</span><span class="sxs-lookup"><span data-stu-id="ca231-121">Topic</span></span>                                                                                       | <span data-ttu-id="ca231-122">描述</span><span class="sxs-lookup"><span data-stu-id="ca231-122">Description</span></span>                                                                                                                                         |
|---------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="ca231-123">關於同步處理管理員</span><span class="sxs-lookup"><span data-stu-id="ca231-123">About Synchronization Manager</span></span>](syncmgr-about.md)<br/>                               | <span data-ttu-id="ca231-124">同步處理管理員提供集中式的標準技術，可同步處理檔案以在本機電腦上離線使用。</span><span class="sxs-lookup"><span data-stu-id="ca231-124">The Synchronization Manager provides a centralized, standard technology for synchronizing files for offline use on a local computer.</span></span><br/>     |
| [<span data-ttu-id="ca231-125">行動計算設定</span><span class="sxs-lookup"><span data-stu-id="ca231-125">Mobile Computing Configurations</span></span>](syncmgr-mobile-computing-configs.md)<br/>          | <span data-ttu-id="ca231-126">應用程式可以使用同步處理管理員，讓檔案和資源在本機快取，並在行動和桌上型電腦上同步處理。</span><span class="sxs-lookup"><span data-stu-id="ca231-126">Applications can use Sychronization Manager to keep files and resources cached locally and synchronized on mobile and desktop computers.</span></span><br/> |
| [<span data-ttu-id="ca231-127">應用程式案例</span><span class="sxs-lookup"><span data-stu-id="ca231-127">Application Scenarios</span></span>](syncmgr-app-scenarios.md)<br/>                               | <span data-ttu-id="ca231-128">可以使用同步處理管理員的應用程式和服務。</span><span class="sxs-lookup"><span data-stu-id="ca231-128">Applications and services that can use Synchronization Manager.</span></span><br/>                                                                          |
| [<span data-ttu-id="ca231-129">同步處理管理員架構</span><span class="sxs-lookup"><span data-stu-id="ca231-129">Synchronization Manager Architecture</span></span>](syncmgr-architecture.md)<br/>                 |                                                                                                                                                     |
| [<span data-ttu-id="ca231-130">從程式使用同步處理管理員</span><span class="sxs-lookup"><span data-stu-id="ca231-130">Using Synchronization Manager from a Program</span></span>](syncmgr-using-from-a-program.md)<br/> |                                                                                                                                                     |
| [<span data-ttu-id="ca231-131">同步處理管理員參考</span><span class="sxs-lookup"><span data-stu-id="ca231-131">Synchronization Manager Reference</span></span>](syncmgr-reference.md)<br/>                       | <span data-ttu-id="ca231-132">下列程式設計項目組成同步處理管理員的 API。</span><span class="sxs-lookup"><span data-stu-id="ca231-132">The following programming elements make up the API for Synchronization Manager.</span></span><br/>                                                          |



 

## <a name="related-topics"></a><span data-ttu-id="ca231-133">相關主題</span><span class="sxs-lookup"><span data-stu-id="ca231-133">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ca231-134">關於系統事件通知服務</span><span class="sxs-lookup"><span data-stu-id="ca231-134">About System Event Notification Service</span></span>](../sens/about-system-event-notification-service.md)
</dt> </dl>

 

 
