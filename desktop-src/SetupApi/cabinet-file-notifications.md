---
description: 下列通知是由 SetupIterateCabinet 傳送。 如需有關通知格式和使用的詳細資訊，請參閱通知。
ms.assetid: 5a362a93-ebe8-4995-aacc-13ee10d3407a
title: 封包檔通知
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bb3e4eb7645fc3603f026db6bde3ce92f2ed2ce7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106970591"
---
# <a name="cabinet-file-notifications"></a><span data-ttu-id="5f864-104">封包檔通知</span><span class="sxs-lookup"><span data-stu-id="5f864-104">Cabinet File Notifications</span></span>

<span data-ttu-id="5f864-105">下列通知是由 [**SetupIterateCabinet**](/windows/desktop/api/Setupapi/nf-setupapi-setupiteratecabineta)傳送。</span><span class="sxs-lookup"><span data-stu-id="5f864-105">The following notifications are sent by [**SetupIterateCabinet**](/windows/desktop/api/Setupapi/nf-setupapi-setupiteratecabineta).</span></span> <span data-ttu-id="5f864-106">如需有關通知格式和使用的詳細資訊，請參閱 [通知](notifications.md)。</span><span class="sxs-lookup"><span data-stu-id="5f864-106">For more information about the format and use of notifications, see [Notifications](notifications.md).</span></span>



| <span data-ttu-id="5f864-107">通知</span><span class="sxs-lookup"><span data-stu-id="5f864-107">Notification</span></span>                                                        | <span data-ttu-id="5f864-108">Description</span><span class="sxs-lookup"><span data-stu-id="5f864-108">Description</span></span>                                                                    |
|---------------------------------------------------------------------|--------------------------------------------------------------------------------|
| [<span data-ttu-id="5f864-109">**SPFILENOTIFY \_ FILEEXTRACTED**</span><span class="sxs-lookup"><span data-stu-id="5f864-109">**SPFILENOTIFY\_FILEEXTRACTED**</span></span>](spfilenotify-fileextracted.md)   | <span data-ttu-id="5f864-110">已從封包解壓縮檔案。</span><span class="sxs-lookup"><span data-stu-id="5f864-110">The file has been extracted from the cabinet.</span></span>                                  |
| [<span data-ttu-id="5f864-111">**SPFILENOTIFY \_ FILEINCABINET**</span><span class="sxs-lookup"><span data-stu-id="5f864-111">**SPFILENOTIFY\_FILEINCABINET**</span></span>](spfilenotify-fileincabinet.md)   | <span data-ttu-id="5f864-112">在封包中遇到檔案，應用程式是否要將它解壓縮？</span><span class="sxs-lookup"><span data-stu-id="5f864-112">A file is encountered in the cabinet, does the application want to extract it?</span></span> |
| [<span data-ttu-id="5f864-113">**SPFILENOTIFY \_ NEEDNEWCABINET**</span><span class="sxs-lookup"><span data-stu-id="5f864-113">**SPFILENOTIFY\_NEEDNEWCABINET**</span></span>](spfilenotify-neednewcabinet.md) | <span data-ttu-id="5f864-114">目前的檔案會在下一個封包中繼續。</span><span class="sxs-lookup"><span data-stu-id="5f864-114">The current file is continued in the next cabinet.</span></span>                             |



 

 

 



