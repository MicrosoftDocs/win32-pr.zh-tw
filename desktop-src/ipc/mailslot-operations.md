---
description: 使用 mailslots、用戶端和伺服器時所要使用之函式的描述。
ms.assetid: 40758d5e-8538-47d9-b8ca-8de5b053ee8b
title: 郵筒作業
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0055ad434971659dc2cfd058146029bb63023654
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106977951"
---
# <a name="mailslot-operations"></a><span data-ttu-id="75fe3-103">郵筒作業</span><span class="sxs-lookup"><span data-stu-id="75fe3-103">Mailslot Operations</span></span>

<span data-ttu-id="75fe3-104">使用 mailslots 時，用戶端和伺服器只應使用下表中所討論的函式。</span><span class="sxs-lookup"><span data-stu-id="75fe3-104">When working with mailslots, clients and servers should use only the functions discussed in the following tables.</span></span> <span data-ttu-id="75fe3-105">請勿使用其他函式，即使它們接受檔案控制代碼或檔案名作為參數，因為它們不是設計來與 mailslots 搭配使用。</span><span class="sxs-lookup"><span data-stu-id="75fe3-105">Do not use other functions, even if they accept file handles or file names as parameters, as they are not designed to work with mailslots.</span></span>

## <a name="mailslot-server-functions"></a><span data-ttu-id="75fe3-106">郵筒伺服器函數</span><span class="sxs-lookup"><span data-stu-id="75fe3-106">Mailslot Server Functions</span></span>

<span data-ttu-id="75fe3-107">郵筒伺服器獨佔使用三個功能，如下表所示。</span><span class="sxs-lookup"><span data-stu-id="75fe3-107">Mailslot servers have exclusive use of three functions, as shown in the following table.</span></span>



| <span data-ttu-id="75fe3-108">函式</span><span class="sxs-lookup"><span data-stu-id="75fe3-108">Function</span></span>                                   | <span data-ttu-id="75fe3-109">描述</span><span class="sxs-lookup"><span data-stu-id="75fe3-109">Description</span></span>                                                                                                                                                                                                  |
|--------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="75fe3-110">**CreateMailslot**</span><span class="sxs-lookup"><span data-stu-id="75fe3-110">**CreateMailslot**</span></span>](/windows/desktop/api/Winbase/nf-winbase-createmailslota)   | <span data-ttu-id="75fe3-111">建立信箱並傳回郵筒控制碼。</span><span class="sxs-lookup"><span data-stu-id="75fe3-111">Creates a mailslot and returns a mailslot handle.</span></span>                                                                                                                                                            |
| [<span data-ttu-id="75fe3-112">**GetMailslotInfo**</span><span class="sxs-lookup"><span data-stu-id="75fe3-112">**GetMailslotInfo**</span></span>](/windows/desktop/api/Winbase/nf-winbase-getmailslotinfo) | <span data-ttu-id="75fe3-113">抓取訊息大小上限、信箱大小、郵件中下一則訊息的大小、郵筒中的訊息數目，以及讀取作業可等候訊息的時間量。</span><span class="sxs-lookup"><span data-stu-id="75fe3-113">Retrieves the maximum message size, the mailslot size, the size of the next message in the mailslot, the number of messages in the mailslot, and the amount of time a read operation can wait for a message.</span></span> |
| [<span data-ttu-id="75fe3-114">**SetMailslotInfo**</span><span class="sxs-lookup"><span data-stu-id="75fe3-114">**SetMailslotInfo**</span></span>](/windows/desktop/api/Winbase/nf-winbase-setmailslotinfo) | <span data-ttu-id="75fe3-115">變更郵筒的讀取超時時間。</span><span class="sxs-lookup"><span data-stu-id="75fe3-115">Changes the read time-out for a mailslot.</span></span>                                                                                                                                                                    |



 

<span data-ttu-id="75fe3-116">郵筒伺服器也會使用下列函數。</span><span class="sxs-lookup"><span data-stu-id="75fe3-116">The following functions are also used by mailslot servers.</span></span>



| <span data-ttu-id="75fe3-117">函式</span><span class="sxs-lookup"><span data-stu-id="75fe3-117">Function</span></span>                                                         | <span data-ttu-id="75fe3-118">描述</span><span class="sxs-lookup"><span data-stu-id="75fe3-118">Description</span></span>                                         |
|------------------------------------------------------------------|-----------------------------------------------------|
| [<span data-ttu-id="75fe3-119">**DuplicateHandle**</span><span class="sxs-lookup"><span data-stu-id="75fe3-119">**DuplicateHandle**</span></span>](/windows/desktop/api/handleapi/nf-handleapi-duplicatehandle)                      | <span data-ttu-id="75fe3-120">複製郵筒控制碼。</span><span class="sxs-lookup"><span data-stu-id="75fe3-120">Duplicates the mailslot handle.</span></span>                     |
| <span data-ttu-id="75fe3-121">[**ReadFile**](/windows/desktop/api/fileapi/nf-fileapi-readfile)、 [ **ReadFileEx**](/windows/desktop/api/fileapi/nf-fileapi-readfileex)</span><span class="sxs-lookup"><span data-stu-id="75fe3-121">[**ReadFile**](/windows/desktop/api/fileapi/nf-fileapi-readfile), [**ReadFileEx**](/windows/desktop/api/fileapi/nf-fileapi-readfileex)</span></span> | <span data-ttu-id="75fe3-122">從郵筒抓取訊息。</span><span class="sxs-lookup"><span data-stu-id="75fe3-122">Retrieves messages from a mailslot.</span></span>                 |
| [<span data-ttu-id="75fe3-123">**GetFileTime**</span><span class="sxs-lookup"><span data-stu-id="75fe3-123">**GetFileTime**</span></span>](/windows/desktop/api/fileapi/nf-fileapi-getfiletime)                              | <span data-ttu-id="75fe3-124">捕獲建立郵筒的日期和時間。</span><span class="sxs-lookup"><span data-stu-id="75fe3-124">Retrieves the date and time a mailslot was created.</span></span> |
| [<span data-ttu-id="75fe3-125">**SetFileTime**</span><span class="sxs-lookup"><span data-stu-id="75fe3-125">**SetFileTime**</span></span>](/windows/desktop/api/fileapi/nf-fileapi-setfiletime)                              | <span data-ttu-id="75fe3-126">設定建立郵筒的日期和時間。</span><span class="sxs-lookup"><span data-stu-id="75fe3-126">Sets the date and time a mailslot was created.</span></span>      |
| [<span data-ttu-id="75fe3-127">**GetHandleInformation**</span><span class="sxs-lookup"><span data-stu-id="75fe3-127">**GetHandleInformation**</span></span>](/windows/desktop/api/handleapi/nf-handleapi-gethandleinformation)            | <span data-ttu-id="75fe3-128">抓取郵筒控點的屬性。</span><span class="sxs-lookup"><span data-stu-id="75fe3-128">Retrieves properties of the mailslot handle.</span></span>        |
| [<span data-ttu-id="75fe3-129">**SetHandleInformation**</span><span class="sxs-lookup"><span data-stu-id="75fe3-129">**SetHandleInformation**</span></span>](/windows/desktop/api/handleapi/nf-handleapi-sethandleinformation)            | <span data-ttu-id="75fe3-130">設定信箱控點的屬性。</span><span class="sxs-lookup"><span data-stu-id="75fe3-130">Sets properties of the mailslot handle.</span></span>             |



 

## <a name="mailslot-client-functions"></a><span data-ttu-id="75fe3-131">郵筒用戶端函式</span><span class="sxs-lookup"><span data-stu-id="75fe3-131">Mailslot Client Functions</span></span>

<span data-ttu-id="75fe3-132">在與信箱互動時，用戶端進程會使用下列功能。</span><span class="sxs-lookup"><span data-stu-id="75fe3-132">A client process uses the following functions when interacting with a mailslot.</span></span>



| <span data-ttu-id="75fe3-133">函式</span><span class="sxs-lookup"><span data-stu-id="75fe3-133">Function</span></span>                                                             | <span data-ttu-id="75fe3-134">描述</span><span class="sxs-lookup"><span data-stu-id="75fe3-134">Description</span></span>                                     |
|----------------------------------------------------------------------|-------------------------------------------------|
| [<span data-ttu-id="75fe3-135">**CloseHandle**</span><span class="sxs-lookup"><span data-stu-id="75fe3-135">**CloseHandle**</span></span>](/windows/desktop/api/handleapi/nf-handleapi-closehandle)                                  | <span data-ttu-id="75fe3-136">關閉用戶端進程的信箱控制碼。</span><span class="sxs-lookup"><span data-stu-id="75fe3-136">Closes a mailslot handle for a client process.</span></span>  |
| [<span data-ttu-id="75fe3-137">**CreateFile**</span><span class="sxs-lookup"><span data-stu-id="75fe3-137">**CreateFile**</span></span>](/windows/desktop/api/fileapi/nf-fileapi-createfilea)                                    | <span data-ttu-id="75fe3-138">建立用戶端進程的郵筒控制碼。</span><span class="sxs-lookup"><span data-stu-id="75fe3-138">Creates a mailslot handle for a client process.</span></span> |
| [<span data-ttu-id="75fe3-139">**DuplicateHandle**</span><span class="sxs-lookup"><span data-stu-id="75fe3-139">**DuplicateHandle**</span></span>](/windows/desktop/api/handleapi/nf-handleapi-duplicatehandle)                          | <span data-ttu-id="75fe3-140">複製郵筒控制碼。</span><span class="sxs-lookup"><span data-stu-id="75fe3-140">Duplicates a mailslot handle.</span></span>                   |
| <span data-ttu-id="75fe3-141">[**WriteFile**](/windows/desktop/api/fileapi/nf-fileapi-writefile)、 [ **WriteFileEx**](/windows/desktop/api/fileapi/nf-fileapi-writefileex)</span><span class="sxs-lookup"><span data-stu-id="75fe3-141">[**WriteFile**](/windows/desktop/api/fileapi/nf-fileapi-writefile), [**WriteFileEx**](/windows/desktop/api/fileapi/nf-fileapi-writefileex)</span></span> | <span data-ttu-id="75fe3-142">將資料寫入郵筒。</span><span class="sxs-lookup"><span data-stu-id="75fe3-142">Writes data to a mailslot.</span></span>                      |



 

 

 
