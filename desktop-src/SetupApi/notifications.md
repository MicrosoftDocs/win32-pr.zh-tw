---
description: 通知是安裝函數傳送給回呼常式以指定狀態或事件的值。 Param1 和 Param2 這兩個參數會隨著通知一起傳送，並且包含與通知相關的其他資訊。
ms.assetid: 93434558-ae83-4ea2-9324-659e5873a8c3
title: " (設定 API) 的通知"
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 096d4261a99e0a837a90aa5c965a3b676843945d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106979262"
---
# <a name="notifications-setup-api"></a><span data-ttu-id="96d00-104"> (設定 API) 的通知</span><span class="sxs-lookup"><span data-stu-id="96d00-104">Notifications (Setup API)</span></span>

<span data-ttu-id="96d00-105">通知是安裝函數傳送給回呼常式以指定狀態或事件的值。</span><span class="sxs-lookup"><span data-stu-id="96d00-105">Notifications are values that a setup function sends to a callback routine to specify a state or event.</span></span> <span data-ttu-id="96d00-106">*Param1* 和 *Param2* 這兩個參數會隨著通知一起傳送，並且包含與通知相關的其他資訊。</span><span class="sxs-lookup"><span data-stu-id="96d00-106">Two parameters, *Param1* and *Param2*, are sent with the notification, and contain additional information relevant to the notification.</span></span>

<span data-ttu-id="96d00-107">回呼常式會處理通知，並將不帶正負號的整數傳回至安裝函式。</span><span class="sxs-lookup"><span data-stu-id="96d00-107">The callback routine processes the notification and returns an unsigned integer to the setup function.</span></span> <span data-ttu-id="96d00-108">根據安裝函式而定，您可以使用這個值來指定作業或使用者選擇，也可以忽略它。</span><span class="sxs-lookup"><span data-stu-id="96d00-108">Depending on the setup function, you can use this value to specify an operation or user selection, or you may ignore it.</span></span>

<span data-ttu-id="96d00-109">安裝函式會使用下列語法，將通知傳送給回呼常式。</span><span class="sxs-lookup"><span data-stu-id="96d00-109">The setup functions send notifications to callback routines using the following syntax.</span></span>

``` syntax
MsgHandler(          //the specified callback routine
    Context,         //context used by the callback routine
    Notification,    //notification code
    Param1,          //additional notification information
    Param2           //additional notification information
);
```

<span data-ttu-id="96d00-110">*內容* 參數是內容變數或結構的 void 指標，回呼常式可以用它來儲存必須在回呼常式後續呼叫之間保存的資訊。</span><span class="sxs-lookup"><span data-stu-id="96d00-110">The *Context* parameter is a void pointer to a context variable or structure that the callback routine can use to store information that must persist between subsequent calls to the callback routine.</span></span>

<span data-ttu-id="96d00-111">由於回呼常式會指定內容的執行，而且它永遠不會由安裝函式參考或改變，因此內容不會記載在後續通知訊息的參考資料中。</span><span class="sxs-lookup"><span data-stu-id="96d00-111">Because the callback routine specifies the context's implementation, and it is never referenced or altered by the setup functions, the context is not documented in the reference material for the notification messages that follow.</span></span>

<span data-ttu-id="96d00-112">*通知* 參數會針對事件或狀態指定不帶正負號的整數值，使設定函數呼叫回呼常式。</span><span class="sxs-lookup"><span data-stu-id="96d00-112">The *Notification* parameter specifies an unsigned integer value for an event or state that causes the setup function to call the callback routine.</span></span>

<span data-ttu-id="96d00-113">*Param1* 和 *Param2* 是選擇性參數，可包含與通知相關的其他資訊。</span><span class="sxs-lookup"><span data-stu-id="96d00-113">*Param1* and *Param2* are optional parameters that can contain additional information relevant to the notification.</span></span> <span data-ttu-id="96d00-114">這些參數是不帶正負號的整數。</span><span class="sxs-lookup"><span data-stu-id="96d00-114">These parameters are unsigned integers.</span></span> <span data-ttu-id="96d00-115">如果 *Param1* 或 *Param2* 傳回的資訊不是不帶正負號的整數，則會轉換成不帶正負號的整數，而且必須先重新轉換成其原始資料類型，才能讓回呼常式使用它。</span><span class="sxs-lookup"><span data-stu-id="96d00-115">If *Param1* or *Param2* return information that is not an unsigned integer, it is cast to an unsigned integer and must be recast to its original data type before it can be used by the callback routine.</span></span>

> [!Note]  
> <span data-ttu-id="96d00-116">下列通知代表安裝函數所使用的每個通知。</span><span class="sxs-lookup"><span data-stu-id="96d00-116">The following notifications represent every notification used by the setup functions.</span></span> <span data-ttu-id="96d00-117">個別函式會使用這些通知的子集。</span><span class="sxs-lookup"><span data-stu-id="96d00-117">Individual functions use a subset of these notifications.</span></span> <span data-ttu-id="96d00-118">換句話說，並非每個函數都使用每個通知。</span><span class="sxs-lookup"><span data-stu-id="96d00-118">In other words, not every notification is used by every function.</span></span>

 

<span data-ttu-id="96d00-119">安裝函數會使用下列通知。</span><span class="sxs-lookup"><span data-stu-id="96d00-119">The following notifications are used by the setup functions.</span></span>



| <span data-ttu-id="96d00-120">通知</span><span class="sxs-lookup"><span data-stu-id="96d00-120">Notification</span></span>                                                                     | <span data-ttu-id="96d00-121">Description</span><span class="sxs-lookup"><span data-stu-id="96d00-121">Description</span></span>                                                                                   |
|----------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------|
| [<span data-ttu-id="96d00-122">**SPFILENOTIFY \_ COPYERROR**</span><span class="sxs-lookup"><span data-stu-id="96d00-122">**SPFILENOTIFY\_COPYERROR**</span></span>](spfilenotify-copyerror.md)                        | <span data-ttu-id="96d00-123">檔案複製作業期間發生錯誤。</span><span class="sxs-lookup"><span data-stu-id="96d00-123">An error occurred during a file copy operation.</span></span>                                               |
| [<span data-ttu-id="96d00-124">**SPFILENOTIFY \_ DELETEERROR**</span><span class="sxs-lookup"><span data-stu-id="96d00-124">**SPFILENOTIFY\_DELETEERROR**</span></span>](spfilenotify-deleteerror.md)                    | <span data-ttu-id="96d00-125">檔案刪除作業期間發生錯誤。</span><span class="sxs-lookup"><span data-stu-id="96d00-125">An error occurred during a file deletion operation.</span></span>                                           |
| [<span data-ttu-id="96d00-126">**SPFILENOTIFY \_ ENDCOPY**</span><span class="sxs-lookup"><span data-stu-id="96d00-126">**SPFILENOTIFY\_ENDCOPY**</span></span>](spfilenotify-endcopy.md)                            | <span data-ttu-id="96d00-127">檔案複製作業已結束。</span><span class="sxs-lookup"><span data-stu-id="96d00-127">A file copy operation has ended.</span></span>                                                              |
| [<span data-ttu-id="96d00-128">**SPFILENOTIFY \_ ENDDELETE**</span><span class="sxs-lookup"><span data-stu-id="96d00-128">**SPFILENOTIFY\_ENDDELETE**</span></span>](spfilenotify-enddelete.md)                        | <span data-ttu-id="96d00-129">檔案刪除操作已結束。</span><span class="sxs-lookup"><span data-stu-id="96d00-129">A file deletion operation has ended.</span></span>                                                          |
| [<span data-ttu-id="96d00-130">**SPFILENOTIFY \_ ENDQUEUE**</span><span class="sxs-lookup"><span data-stu-id="96d00-130">**SPFILENOTIFY\_ENDQUEUE**</span></span>](spfilenotify-endqueue.md)                          | <span data-ttu-id="96d00-131">佇列已完成認可。</span><span class="sxs-lookup"><span data-stu-id="96d00-131">The queue has finished committing.</span></span>                                                            |
| [<span data-ttu-id="96d00-132">**SPFILENOTIFY \_ ENDREGISTRATION**</span><span class="sxs-lookup"><span data-stu-id="96d00-132">**SPFILENOTIFY\_ENDREGISTRATION**</span></span>](spfilenotify-endregistration.md)            | <span data-ttu-id="96d00-133">檔案的註冊或取消註冊已完成。</span><span class="sxs-lookup"><span data-stu-id="96d00-133">The registration or unregistration of the file has finished.</span></span>                                  |
| [<span data-ttu-id="96d00-134">**SPFILENOTIFY \_ ENDRENAME**</span><span class="sxs-lookup"><span data-stu-id="96d00-134">**SPFILENOTIFY\_ENDRENAME**</span></span>](spfilenotify-endrename.md)                        | <span data-ttu-id="96d00-135">檔案重新命名作業已結束。</span><span class="sxs-lookup"><span data-stu-id="96d00-135">A file rename operation has ended.</span></span>                                                            |
| [<span data-ttu-id="96d00-136">**SPFILENOTIFY \_ ENDSUBQUEUE**</span><span class="sxs-lookup"><span data-stu-id="96d00-136">**SPFILENOTIFY\_ENDSUBQUEUE**</span></span>](spfilenotify-endsubqueue.md)                    | <span data-ttu-id="96d00-137">子佇列 (複製、重新命名或刪除) 已結束。</span><span class="sxs-lookup"><span data-stu-id="96d00-137">A subqueue (either copy, rename or delete) has ended.</span></span>                                         |
| [<span data-ttu-id="96d00-138">**SPFILENOTIFY \_ FILEEXTRACTED**</span><span class="sxs-lookup"><span data-stu-id="96d00-138">**SPFILENOTIFY\_FILEEXTRACTED**</span></span>](spfilenotify-fileextracted.md)                | <span data-ttu-id="96d00-139">已從封包解壓縮檔案。</span><span class="sxs-lookup"><span data-stu-id="96d00-139">The file has been extracted from the cabinet.</span></span>                                                 |
| [<span data-ttu-id="96d00-140">**SPFILENOTIFY \_ FILEINCABINET**</span><span class="sxs-lookup"><span data-stu-id="96d00-140">**SPFILENOTIFY\_FILEINCABINET**</span></span>](spfilenotify-fileincabinet.md)                | <span data-ttu-id="96d00-141">在封包中發現檔案。</span><span class="sxs-lookup"><span data-stu-id="96d00-141">A file is encountered in the cabinet.</span></span>                                                         |
| [<span data-ttu-id="96d00-142">**SPFILENOTIFY \_ FILEOPDELAYED**</span><span class="sxs-lookup"><span data-stu-id="96d00-142">**SPFILENOTIFY\_FILEOPDELAYED**</span></span>](spfilenotify-fileopdelayed.md)                | <span data-ttu-id="96d00-143">檔案已在使用中，而且目前的操作已延遲，直到系統重新開機為止。</span><span class="sxs-lookup"><span data-stu-id="96d00-143">The file was in use, and the current operation has been delayed until the system is rebooted.</span></span> |
| [<span data-ttu-id="96d00-144">**SPFILENOTIFY \_ LANGMISMATCH**</span><span class="sxs-lookup"><span data-stu-id="96d00-144">**SPFILENOTIFY\_LANGMISMATCH**</span></span>](spfilenotify-langmismatch.md)                  | <span data-ttu-id="96d00-145">目前操作的語言與系統語言不符。</span><span class="sxs-lookup"><span data-stu-id="96d00-145">The language of the current operation does not match the system language.</span></span>                     |
| [<span data-ttu-id="96d00-146">**SPFILENOTIFY \_ NEEDMEDIA**</span><span class="sxs-lookup"><span data-stu-id="96d00-146">**SPFILENOTIFY\_NEEDMEDIA**</span></span>](spfilenotify-needmedia.md)                        | <span data-ttu-id="96d00-147">需要新的來源媒體。</span><span class="sxs-lookup"><span data-stu-id="96d00-147">New source media is required.</span></span>                                                                 |
| [<span data-ttu-id="96d00-148">**SPFILENOTIFY \_ NEEDNEWCABINET**</span><span class="sxs-lookup"><span data-stu-id="96d00-148">**SPFILENOTIFY\_NEEDNEWCABINET**</span></span>](spfilenotify-neednewcabinet.md)              | <span data-ttu-id="96d00-149">目前的檔案會在下一個封包中繼續。</span><span class="sxs-lookup"><span data-stu-id="96d00-149">The current file is continued in the next cabinet.</span></span>                                            |
| [<span data-ttu-id="96d00-150">**SPFILENOTIFY \_ QUEUESCAN**</span><span class="sxs-lookup"><span data-stu-id="96d00-150">**SPFILENOTIFY\_QUEUESCAN**</span></span>](spfilenotify-queuescan.md)                        | <span data-ttu-id="96d00-151">已掃描檔案佇列中的節點。</span><span class="sxs-lookup"><span data-stu-id="96d00-151">A node in the file queue has been scanned.</span></span>                                                    |
| [<span data-ttu-id="96d00-152">**SPFILENOTIFY \_ QUEUESCAN \_ EX**</span><span class="sxs-lookup"><span data-stu-id="96d00-152">**SPFILENOTIFY\_QUEUESCAN\_EX**</span></span>](spfilenotify-queuescan-ex.md)                 | <span data-ttu-id="96d00-153">已掃描檔案佇列中的節點。</span><span class="sxs-lookup"><span data-stu-id="96d00-153">A node in the file queue has been scanned.</span></span>                                                    |
| [<span data-ttu-id="96d00-154">**SPFILENOTIFY \_ QUEUESCAN \_ SIGNERINFO**</span><span class="sxs-lookup"><span data-stu-id="96d00-154">**SPFILENOTIFY\_QUEUESCAN\_SIGNERINFO**</span></span>](spfilenotify-queuescan-signerinfo.md) | <span data-ttu-id="96d00-155">已掃描檔案佇列中的節點。</span><span class="sxs-lookup"><span data-stu-id="96d00-155">A node in the file queue has been scanned.</span></span>                                                    |
| [<span data-ttu-id="96d00-156">**SPFILENOTIFY \_ RENAMEERROR**</span><span class="sxs-lookup"><span data-stu-id="96d00-156">**SPFILENOTIFY\_RENAMEERROR**</span></span>](spfilenotify-renameerror.md)                    | <span data-ttu-id="96d00-157">檔案重新命名作業期間發生錯誤。</span><span class="sxs-lookup"><span data-stu-id="96d00-157">An error occurred during a file rename operation.</span></span>                                             |
| [<span data-ttu-id="96d00-158">**SPFILENOTIFY \_ STARTCOPY**</span><span class="sxs-lookup"><span data-stu-id="96d00-158">**SPFILENOTIFY\_STARTCOPY**</span></span>](spfilenotify-startcopy.md)                        | <span data-ttu-id="96d00-159">檔案複製作業已啟動。</span><span class="sxs-lookup"><span data-stu-id="96d00-159">A file copy operation has started.</span></span>                                                            |
| [<span data-ttu-id="96d00-160">**SPFILENOTIFY \_ STARTDELETE**</span><span class="sxs-lookup"><span data-stu-id="96d00-160">**SPFILENOTIFY\_STARTDELETE**</span></span>](spfilenotify-startdelete.md)                    | <span data-ttu-id="96d00-161">檔案刪除作業已啟動。</span><span class="sxs-lookup"><span data-stu-id="96d00-161">A file delete operation has started.</span></span>                                                          |
| [<span data-ttu-id="96d00-162">**SPFILENOTIFY \_ STARTQUEUE**</span><span class="sxs-lookup"><span data-stu-id="96d00-162">**SPFILENOTIFY\_STARTQUEUE**</span></span>](spfilenotify-startqueue.md)                      | <span data-ttu-id="96d00-163">佇列已開始認可。</span><span class="sxs-lookup"><span data-stu-id="96d00-163">The queue has started to commit.</span></span>                                                              |
| [<span data-ttu-id="96d00-164">**SPFILENOTIFY \_ STARTREGISTRATION**</span><span class="sxs-lookup"><span data-stu-id="96d00-164">**SPFILENOTIFY\_STARTREGISTRATION**</span></span>](spfilenotify-startregistration.md)        | <span data-ttu-id="96d00-165">檔案的註冊或取消註冊已開始。</span><span class="sxs-lookup"><span data-stu-id="96d00-165">The registration or unregistration of the file has started.</span></span>                                   |
| [<span data-ttu-id="96d00-166">**SPFILENOTIFY \_ STARTRENAME**</span><span class="sxs-lookup"><span data-stu-id="96d00-166">**SPFILENOTIFY\_STARTRENAME**</span></span>](spfilenotify-startrename.md)                    | <span data-ttu-id="96d00-167">檔案重新命名作業已啟動。</span><span class="sxs-lookup"><span data-stu-id="96d00-167">A file rename operation has started.</span></span>                                                          |
| [<span data-ttu-id="96d00-168">**SPFILENOTIFY \_ STARTSUBQUEUE**</span><span class="sxs-lookup"><span data-stu-id="96d00-168">**SPFILENOTIFY\_STARTSUBQUEUE**</span></span>](spfilenotify-startsubqueue.md)                | <span data-ttu-id="96d00-169">子佇列 (複製、重新命名或刪除) 已開始。</span><span class="sxs-lookup"><span data-stu-id="96d00-169">A subqueue (either copy, rename or delete) has started.</span></span>                                       |
| [<span data-ttu-id="96d00-170">**SPFILENOTIFY \_ TARGETEXISTS**</span><span class="sxs-lookup"><span data-stu-id="96d00-170">**SPFILENOTIFY\_TARGETEXISTS**</span></span>](spfilenotify-targetexists.md)                  | <span data-ttu-id="96d00-171">目標上已有指定檔案的複本。</span><span class="sxs-lookup"><span data-stu-id="96d00-171">A copy of the specified file already exists on the target.</span></span>                                    |
| [<span data-ttu-id="96d00-172">**SPFILENOTIFY \_ TARGETNEWER**</span><span class="sxs-lookup"><span data-stu-id="96d00-172">**SPFILENOTIFY\_TARGETNEWER**</span></span>](spfilenotify-targetnewer.md)                    | <span data-ttu-id="96d00-173">目標上有較新版本的指定檔案。</span><span class="sxs-lookup"><span data-stu-id="96d00-173">A newer version of the specified file exists on the target.</span></span>                                   |



 

 

 



