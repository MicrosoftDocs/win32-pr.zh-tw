---
description: 預設佇列回呼常式會以一般方式處理 SetupCommitFileQueue 所傳送的通知。
ms.assetid: 6f2b3b9f-86e5-42af-8adc-29a1c768d106
title: 關於預設佇列回呼常式
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 57dfd22a9fa260aa1e98a2085e0cb925ed1f3438
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103847921"
---
# <a name="about-the-default-queue-callback-routine"></a><span data-ttu-id="356cb-103">關於預設佇列回呼常式</span><span class="sxs-lookup"><span data-stu-id="356cb-103">About the Default Queue Callback Routine</span></span>

<span data-ttu-id="356cb-104">預設佇列回呼常式會以一般方式處理 [**SetupCommitFileQueue**](/windows/desktop/api/Setupapi/nf-setupapi-setupcommitfilequeuea) 所傳送的通知。</span><span class="sxs-lookup"><span data-stu-id="356cb-104">The default queue callback routine handles notifications sent by [**SetupCommitFileQueue**](/windows/desktop/api/Setupapi/nf-setupapi-setupcommitfilequeuea) in a generic manner.</span></span> <span data-ttu-id="356cb-105">您可以使用預設常式取得現成的使用者介面，以建立一般安裝程式對話方塊。</span><span class="sxs-lookup"><span data-stu-id="356cb-105">By using the default routine, you get a ready-made user interface to create common setup dialog boxes.</span></span> <span data-ttu-id="356cb-106">建議您使用預設佇列回呼常式（兩者都可方便使用），並確保在安裝期間所產生之對話方塊的外觀和行為都一致。</span><span class="sxs-lookup"><span data-stu-id="356cb-106">It is recommended that you use the default queue callback routine, both for ease of use, and to ensure a consistent appearance and behavior of dialog boxes generated during the installation.</span></span>

<span data-ttu-id="356cb-107">預設回呼常式需要內部記錄保留的內容結構。</span><span class="sxs-lookup"><span data-stu-id="356cb-107">The default callback routine requires a context structure for internal record keeping.</span></span> <span data-ttu-id="356cb-108">此外，佇列會在一組參數（ *Param1* 和 *Param2*）中傳遞與目前通知相關的其他資訊。</span><span class="sxs-lookup"><span data-stu-id="356cb-108">In addition, the queue passes additional information relevant to the current notification in a set of parameters, *Param1* and *Param2*.</span></span>

<span data-ttu-id="356cb-109">例如，如果佇列將 SPFILENOTIFY \_ NEEDMEDIA 通知傳送至預設回呼常式，則 *Param1* 會指向 [**來源 \_ 媒體**](/windows/desktop/api/Setupapi/ns-setupapi-source_media_a) 結構，其中包含所需媒體的相關資訊， *Param2* 指向可以接收使用者新路徑資訊的字元陣列。</span><span class="sxs-lookup"><span data-stu-id="356cb-109">For example, if the queue sends an SPFILENOTIFY\_NEEDMEDIA notification to the default callback routine, *Param1* points to a [**SOURCE\_MEDIA**](/windows/desktop/api/Setupapi/ns-setupapi-source_media_a) structure that contains information about the media needed, and *Param2* points to a character array that can receive new path information from the user.</span></span>

<span data-ttu-id="356cb-110">預設回呼常式會使用這項資訊來提示使用者插入所需的來源媒體、指定新路徑、略過複製目前的檔案，或取消目前的操作。</span><span class="sxs-lookup"><span data-stu-id="356cb-110">The default callback routine uses this information to prompt the user to either insert the needed source media, specify a new path, skip copying the current file, or cancel the current operation.</span></span> <span data-ttu-id="356cb-111">根據使用者採取的動作而定，預設佇列回呼常式會傳回 FILEOP \_ NEWPATH、FILEOP \_ DOIT R、FILEOP \_ SKIP 或 FILEOP \_ ABORT 給佇列。</span><span class="sxs-lookup"><span data-stu-id="356cb-111">The default queue callback routine returns FILEOP\_NEWPATH, FILEOP\_DOIT , FILEOP\_SKIP, or FILEOP\_ABORT to the queue, depending on which action the user took.</span></span>

<span data-ttu-id="356cb-112">如需預設佇列回呼常式如何處理每個佇列通知的詳細資訊，請參閱檔案 [佇列通知](file-queue-notifications.md)。</span><span class="sxs-lookup"><span data-stu-id="356cb-112">For information on how the default queue callback routine handles each queue notification, see [File Queue Notifications](file-queue-notifications.md).</span></span>

<span data-ttu-id="356cb-113">如需自訂佇列回呼常式的詳細資訊，請參閱 [建立自訂佇列回呼常式](creating-a-custom-queue-callback-routine.md)。</span><span class="sxs-lookup"><span data-stu-id="356cb-113">For information on custom queue callback routines, see [Creating a Custom Queue Callback Routine](creating-a-custom-queue-callback-routine.md).</span></span>

 

 



