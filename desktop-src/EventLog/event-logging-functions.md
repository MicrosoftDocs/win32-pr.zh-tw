---
description: 下列函式可用於事件記錄。
ms.assetid: fd5c12ec-3a3d-4b75-a573-0b27ae7a890b
title: 事件記錄功能
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 437899684861c5fc7ddbfe98c2499dc07bd9da8a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106998281"
---
# <a name="event-logging-functions"></a><span data-ttu-id="eb590-103">事件記錄功能</span><span class="sxs-lookup"><span data-stu-id="eb590-103">Event Logging Functions</span></span>

<span data-ttu-id="eb590-104">下列函式可用於事件記錄。</span><span class="sxs-lookup"><span data-stu-id="eb590-104">The following functions are used with event logging.</span></span>



| <span data-ttu-id="eb590-105">函式</span><span class="sxs-lookup"><span data-stu-id="eb590-105">Function</span></span>                                                         | <span data-ttu-id="eb590-106">描述</span><span class="sxs-lookup"><span data-stu-id="eb590-106">Description</span></span>                                                                                         |
|------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="eb590-107">**BackupEventLog**</span><span class="sxs-lookup"><span data-stu-id="eb590-107">**BackupEventLog**</span></span>](/windows/desktop/api/Winbase/nf-winbase-backupeventloga)                         | <span data-ttu-id="eb590-108">將指定的事件記錄檔儲存至備份檔案。</span><span class="sxs-lookup"><span data-stu-id="eb590-108">Saves the specified event log to a backup file.</span></span>                                                     |
| [<span data-ttu-id="eb590-109">**ClearEventLog**</span><span class="sxs-lookup"><span data-stu-id="eb590-109">**ClearEventLog**</span></span>](/windows/desktop/api/Winbase/nf-winbase-cleareventloga)                           | <span data-ttu-id="eb590-110">清除指定的事件記錄檔，並選擇性地將記錄檔的目前副本儲存至備份檔案。</span><span class="sxs-lookup"><span data-stu-id="eb590-110">Clears the specified event log, and optionally saves the current copy of the log to a backup file.</span></span>  |
| [<span data-ttu-id="eb590-111">**CloseEventLog**</span><span class="sxs-lookup"><span data-stu-id="eb590-111">**CloseEventLog**</span></span>](/windows/desktop/api/Winbase/nf-winbase-closeeventlog)                           | <span data-ttu-id="eb590-112">關閉指定之事件記錄檔的讀取控制碼。</span><span class="sxs-lookup"><span data-stu-id="eb590-112">Closes a read handle to the specified event log.</span></span>                                                    |
| [<span data-ttu-id="eb590-113">**DeregisterEventSource**</span><span class="sxs-lookup"><span data-stu-id="eb590-113">**DeregisterEventSource**</span></span>](/windows/desktop/api/Winbase/nf-winbase-deregistereventsource)           | <span data-ttu-id="eb590-114">關閉指定之事件記錄檔的寫入控制碼。</span><span class="sxs-lookup"><span data-stu-id="eb590-114">Closes a write handle to the specified event log.</span></span>                                                   |
| [<span data-ttu-id="eb590-115">**GetEventLogInformation**</span><span class="sxs-lookup"><span data-stu-id="eb590-115">**GetEventLogInformation**</span></span>](/windows/desktop/api/Winbase/nf-winbase-geteventloginformation)         | <span data-ttu-id="eb590-116">抓取指定之事件記錄檔的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="eb590-116">Retrieves information about the specified event log.</span></span>                                                |
| [<span data-ttu-id="eb590-117">**GetNumberOfEventLogRecords**</span><span class="sxs-lookup"><span data-stu-id="eb590-117">**GetNumberOfEventLogRecords**</span></span>](/windows/desktop/api/Winbase/nf-winbase-getnumberofeventlogrecords) | <span data-ttu-id="eb590-118">捕獲指定事件記錄檔中的記錄數目。</span><span class="sxs-lookup"><span data-stu-id="eb590-118">Retrieves the number of records in the specified event log.</span></span>                                         |
| [<span data-ttu-id="eb590-119">**GetOldestEventLogRecord**</span><span class="sxs-lookup"><span data-stu-id="eb590-119">**GetOldestEventLogRecord**</span></span>](/windows/desktop/api/Winbase/nf-winbase-getoldesteventlogrecord)       | <span data-ttu-id="eb590-120">抓取指定之事件記錄檔中最舊記錄的絕對記錄號碼。</span><span class="sxs-lookup"><span data-stu-id="eb590-120">Retrieves the absolute record number of the oldest record in the specified event log.</span></span>               |
| [<span data-ttu-id="eb590-121">**NotifyChangeEventLog**</span><span class="sxs-lookup"><span data-stu-id="eb590-121">**NotifyChangeEventLog**</span></span>](/windows/desktop/api/Winbase/nf-winbase-notifychangeeventlog)             | <span data-ttu-id="eb590-122">讓應用程式在事件寫入至指定的事件記錄檔時接收通知。</span><span class="sxs-lookup"><span data-stu-id="eb590-122">Enables an application to receive notification when an event is written to the specified event log.</span></span> |
| [<span data-ttu-id="eb590-123">**OpenBackupEventLog**</span><span class="sxs-lookup"><span data-stu-id="eb590-123">**OpenBackupEventLog**</span></span>](/windows/desktop/api/Winbase/nf-winbase-openbackupeventloga)                 | <span data-ttu-id="eb590-124">開啟備份事件記錄檔的控制碼。</span><span class="sxs-lookup"><span data-stu-id="eb590-124">Opens a handle to a backup event log.</span></span>                                                               |
| [<span data-ttu-id="eb590-125">**OpenEventLog**</span><span class="sxs-lookup"><span data-stu-id="eb590-125">**OpenEventLog**</span></span>](/windows/desktop/api/Winbase/nf-winbase-openeventloga)                             | <span data-ttu-id="eb590-126">開啟指定之事件記錄檔的控制碼。</span><span class="sxs-lookup"><span data-stu-id="eb590-126">Opens a handle to the specified event log.</span></span>                                                          |
| [<span data-ttu-id="eb590-127">**ReadEventLog**</span><span class="sxs-lookup"><span data-stu-id="eb590-127">**ReadEventLog**</span></span>](/windows/desktop/api/Winbase/nf-winbase-readeventloga)                             | <span data-ttu-id="eb590-128">從指定的事件記錄檔讀取大量的專案。</span><span class="sxs-lookup"><span data-stu-id="eb590-128">Reads a whole number of entries from the specified event log.</span></span>                                       |
| [<span data-ttu-id="eb590-129">**RegisterEventSource**</span><span class="sxs-lookup"><span data-stu-id="eb590-129">**RegisterEventSource**</span></span>](/windows/desktop/api/Winbase/nf-winbase-registereventsourcea)               | <span data-ttu-id="eb590-130">抓取指定之事件記錄檔的已註冊控制碼。</span><span class="sxs-lookup"><span data-stu-id="eb590-130">Retrieves a registered handle to the specified event log.</span></span>                                           |
| [<span data-ttu-id="eb590-131">**ReportEvent**</span><span class="sxs-lookup"><span data-stu-id="eb590-131">**ReportEvent**</span></span>](/windows/desktop/api/Winbase/nf-winbase-reporteventa)                               | <span data-ttu-id="eb590-132">在指定事件記錄檔的結尾寫入專案。</span><span class="sxs-lookup"><span data-stu-id="eb590-132">Writes an entry at the end of the specified event log.</span></span>                                              |



 

 

 



