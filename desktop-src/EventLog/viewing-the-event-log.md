---
description: 當使用者啟動事件檢視器來查看事件記錄檔專案時，它會呼叫 ReadEventLog 函式來取得 EVENTLOGRECORD 結構。
ms.assetid: 1d5b62cb-cf5b-4f4c-8521-1c783ae3afc7
title: 查看事件記錄檔
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 58c566fef29cfb110883741ddc0e6c298d6a1255
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104192313"
---
# <a name="viewing-the-event-log"></a><span data-ttu-id="16b28-103">查看事件記錄檔</span><span class="sxs-lookup"><span data-stu-id="16b28-103">Viewing the Event Log</span></span>

<span data-ttu-id="16b28-104">當使用者啟動事件檢視器來查看事件記錄檔專案時，它會呼叫 [**ReadEventLog**](/windows/desktop/api/Winbase/nf-winbase-readeventloga) 函式來取得 [**EVENTLOGRECORD**](/windows/desktop/api/Winnt/ns-winnt-eventlogrecord) 結構。</span><span class="sxs-lookup"><span data-stu-id="16b28-104">When the user starts Event Viewer to view the event log entries, it calls the [**ReadEventLog**](/windows/desktop/api/Winbase/nf-winbase-readeventloga) function to obtain the [**EVENTLOGRECORD**](/windows/desktop/api/Winnt/ns-winnt-eventlogrecord) structures.</span></span> <span data-ttu-id="16b28-105">事件檢視器使用事件來源和事件識別碼，從已註冊的訊息檔案中取得每個事件的郵件內文， (由來源) 的 **EventMessageFile** 登錄值指出。</span><span class="sxs-lookup"><span data-stu-id="16b28-105">The Event Viewer uses the event source and event identifier to get message text for each event from the registered message file (indicated by the **EventMessageFile** registry value for the source).</span></span> <span data-ttu-id="16b28-106">事件檢視器使用 [**LoadLibraryEx**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibraryexa) 函式來載入訊息檔。</span><span class="sxs-lookup"><span data-stu-id="16b28-106">The Event Viewer uses the [**LoadLibraryEx**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibraryexa) function to load the message file.</span></span> <span data-ttu-id="16b28-107">事件檢視器接著會使用 [**FormatMessage**](/windows/desktop/api/winbase/nf-winbase-formatmessage) 函式，從載入的模組中取出基底描述字串。</span><span class="sxs-lookup"><span data-stu-id="16b28-107">The Event Viewer then uses the [**FormatMessage**](/windows/desktop/api/winbase/nf-winbase-formatmessage) function to retrieve the base description string from the loaded module.</span></span> <span data-ttu-id="16b28-108">最後，事件檢視器取代基底描述字串中的插入參數，以產生最後的訊息字串。</span><span class="sxs-lookup"><span data-stu-id="16b28-108">Finally, the Event Viewer replaces the insertion parameters in the base description string to yield the final message string.</span></span>

 

 
