---
description: 有五種類型的事件可以記錄。 這些都有定義完善的一般資料，並可選擇性地包含事件特定的資料。
ms.assetid: 4ab4a284-a4cd-4cf7-a9d2-e4a75fce01b9
title: 事件類型
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3832f90ccdb8dafc676c139f92665efde732533c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103848854"
---
# <a name="event-types"></a><span data-ttu-id="871a9-104">事件類型</span><span class="sxs-lookup"><span data-stu-id="871a9-104">Event Types</span></span>

<span data-ttu-id="871a9-105">有五種類型的事件可以記錄。</span><span class="sxs-lookup"><span data-stu-id="871a9-105">There are five types of events that can be logged.</span></span> <span data-ttu-id="871a9-106">這些都有定義完善的一般資料，並可選擇性地包含事件特定的資料。</span><span class="sxs-lookup"><span data-stu-id="871a9-106">All of these have well-defined common data and can optionally include event-specific data.</span></span>

<span data-ttu-id="871a9-107">應用程式會在報告事件時指出事件種類。</span><span class="sxs-lookup"><span data-stu-id="871a9-107">The application indicates the event type when it reports an event.</span></span> <span data-ttu-id="871a9-108">每個事件都必須是單一類型。</span><span class="sxs-lookup"><span data-stu-id="871a9-108">Each event must be of a single type.</span></span> <span data-ttu-id="871a9-109">事件檢視器會在事件記錄檔的清單查看中，針對每個類型顯示不同的圖示。</span><span class="sxs-lookup"><span data-stu-id="871a9-109">The Event Viewer displays a different icon for each type in the list view of the event log.</span></span>

<span data-ttu-id="871a9-110">下表描述事件記錄中使用的五種事件種類。</span><span class="sxs-lookup"><span data-stu-id="871a9-110">The following table describes the five event types used in event logging.</span></span>



| <span data-ttu-id="871a9-111">事件類型</span><span class="sxs-lookup"><span data-stu-id="871a9-111">Event type</span></span>        | <span data-ttu-id="871a9-112">描述</span><span class="sxs-lookup"><span data-stu-id="871a9-112">Description</span></span>                                                                                                                                                                                                                                                                                              |
|-------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="871a9-113">**錯誤**</span><span class="sxs-lookup"><span data-stu-id="871a9-113">**Error**</span></span>         | <span data-ttu-id="871a9-114">表示重大問題的事件，例如資料遺失或功能遺失。</span><span class="sxs-lookup"><span data-stu-id="871a9-114">An event that indicates a significant problem such as loss of data or loss of functionality.</span></span> <span data-ttu-id="871a9-115">例如，如果服務無法在啟動時載入，就會記錄錯誤事件。</span><span class="sxs-lookup"><span data-stu-id="871a9-115">For example, if a service fails to load during startup, an Error event is logged.</span></span>                                                                                                                           |
| <span data-ttu-id="871a9-116">**警告**</span><span class="sxs-lookup"><span data-stu-id="871a9-116">**Warning**</span></span>       | <span data-ttu-id="871a9-117">不一定很重要，但可能表示未來可能發生問題的事件。</span><span class="sxs-lookup"><span data-stu-id="871a9-117">An event that is not necessarily significant, but may indicate a possible future problem.</span></span> <span data-ttu-id="871a9-118">例如，當磁碟空間不足時，就會記錄警告事件。</span><span class="sxs-lookup"><span data-stu-id="871a9-118">For example, when disk space is low, a Warning event is logged.</span></span> <span data-ttu-id="871a9-119">如果應用程式可以從沒有遺失功能或資料的事件中復原，通常可以將事件分類為警告事件。</span><span class="sxs-lookup"><span data-stu-id="871a9-119">If an application can recover from an event without loss of functionality or data, it can generally classify the event as a Warning event.</span></span>     |
| <span data-ttu-id="871a9-120">**資訊**</span><span class="sxs-lookup"><span data-stu-id="871a9-120">**Information**</span></span>   | <span data-ttu-id="871a9-121">描述應用程式、驅動程式或服務之成功操作的事件。</span><span class="sxs-lookup"><span data-stu-id="871a9-121">An event that describes the successful operation of an application, driver, or service.</span></span> <span data-ttu-id="871a9-122">例如，當網路驅動程式成功載入時，可能會需要記錄資訊事件。</span><span class="sxs-lookup"><span data-stu-id="871a9-122">For example, when a network driver loads successfully, it may be appropriate to log an Information event.</span></span> <span data-ttu-id="871a9-123">請注意，在每次啟動時，桌面應用程式都不適合用來記錄事件。</span><span class="sxs-lookup"><span data-stu-id="871a9-123">Note that it is generally inappropriate for a desktop application to log an event each time it starts.</span></span> |
| <span data-ttu-id="871a9-124">**稽核成功**</span><span class="sxs-lookup"><span data-stu-id="871a9-124">**Success Audit**</span></span> | <span data-ttu-id="871a9-125">此事件會記錄成功的已審核安全性存取嘗試。</span><span class="sxs-lookup"><span data-stu-id="871a9-125">An event that records an audited security access attempt that is successful.</span></span> <span data-ttu-id="871a9-126">例如，使用者成功登入系統的嘗試會記錄為成功審核事件。</span><span class="sxs-lookup"><span data-stu-id="871a9-126">For example, a user's successful attempt to log on to the system is logged as a Success Audit event.</span></span>                                                                                                                        |
| <span data-ttu-id="871a9-127">**稽核失敗**</span><span class="sxs-lookup"><span data-stu-id="871a9-127">**Failure Audit**</span></span> | <span data-ttu-id="871a9-128">此事件會記錄失敗的已審核安全性存取嘗試。</span><span class="sxs-lookup"><span data-stu-id="871a9-128">An event that records an audited security access attempt that fails.</span></span> <span data-ttu-id="871a9-129">例如，如果使用者嘗試存取網路磁碟機機而失敗，則會將嘗試記錄為「失敗審核」事件。</span><span class="sxs-lookup"><span data-stu-id="871a9-129">For example, if a user tries to access a network drive and fails, the attempt is logged as a Failure Audit event.</span></span>                                                                                                                   |



 

<span data-ttu-id="871a9-130">您可以透過審核安全性事件，然後將專案放在電腦的安全性記錄檔中，來追蹤使用者的選取活動。</span><span class="sxs-lookup"><span data-stu-id="871a9-130">Selected activities of users can be tracked by auditing security events and then placing entries in a computer's security log.</span></span>

 

 



