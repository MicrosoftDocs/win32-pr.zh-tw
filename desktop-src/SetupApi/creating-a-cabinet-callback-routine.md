---
description: 因為安裝程式 API 未提供預設的封包回呼常式，所以您必須提供常式。 SetupIterateCabinet 函式所需的回呼常式必須具有與 FileCallback 所指向的相同形式。
ms.assetid: 45a2690e-1db6-4a09-a141-9e68ebc2a6d8
title: 建立封包回呼常式
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1f25d59515a6afdd68cef4458868fbfb62335aed
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104193080"
---
# <a name="creating-a-cabinet-callback-routine"></a><span data-ttu-id="ce9ad-104">建立封包回呼常式</span><span class="sxs-lookup"><span data-stu-id="ce9ad-104">Creating a Cabinet Callback Routine</span></span>

<span data-ttu-id="ce9ad-105">因為安裝程式 API 未提供預設的封包回呼常式，所以您必須提供常式。</span><span class="sxs-lookup"><span data-stu-id="ce9ad-105">Because the Setup API does not supply a default cabinet callback routine, you need to supply a routine.</span></span> <span data-ttu-id="ce9ad-106">[**SetupIterateCabinet**](/windows/desktop/api/Setupapi/nf-setupapi-setupiteratecabineta)函式所需的回呼常式必須具有與 [FileCallback](/windows/win32/api/setupapi/nc-setupapi-psp_file_callback_a)所指向的相同形式。</span><span class="sxs-lookup"><span data-stu-id="ce9ad-106">The callback routine that the [**SetupIterateCabinet**](/windows/desktop/api/Setupapi/nf-setupapi-setupiteratecabineta) function requires must have the same form as those pointed to by [FileCallback](/windows/win32/api/setupapi/nc-setupapi-psp_file_callback_a).</span></span>

<span data-ttu-id="ce9ad-107">以下是 [**SetupIterateCabinet**](/windows/desktop/api/Setupapi/nf-setupapi-setupiteratecabineta) 用來傳送通知給回呼常式的語法。</span><span class="sxs-lookup"><span data-stu-id="ce9ad-107">Following is the syntax that [**SetupIterateCabinet**](/windows/desktop/api/Setupapi/nf-setupapi-setupiteratecabineta) uses to send a notification to the callback routine.</span></span>

``` syntax
MsgHandler(          //the specified callback routine
    Context,         //context used by the callback routine
    Notification,    //cabinet notification
    Param1,          //additional notification information
    Param2           //additional notification information
);
```

<span data-ttu-id="ce9ad-108">*內容* 參數是內容變數或結構的 void 指標，可供回呼常式用來儲存在後續呼叫回呼常式之間必須保存的資訊。</span><span class="sxs-lookup"><span data-stu-id="ce9ad-108">The *Context* parameter is a void pointer to a context variable or structure that can be used by the callback routine to store information that needs to persist between subsequent calls to the callback routine.</span></span>

<span data-ttu-id="ce9ad-109">此內容的實作為回呼常式的指定，且 [**SetupIterateCabinet**](/windows/desktop/api/Setupapi/nf-setupapi-setupiteratecabineta)絕對不會參考或改變。</span><span class="sxs-lookup"><span data-stu-id="ce9ad-109">This context's implementation is specified by the callback routine, and it is never referenced or altered by [**SetupIterateCabinet**](/windows/desktop/api/Setupapi/nf-setupapi-setupiteratecabineta).</span></span>

<span data-ttu-id="ce9ad-110">*通知* 參數是不帶正負號的整數，而且會是下列其中一個值。</span><span class="sxs-lookup"><span data-stu-id="ce9ad-110">The *Notification* parameter is an unsigned integer and will be one of the following values.</span></span>



| <span data-ttu-id="ce9ad-111">通知</span><span class="sxs-lookup"><span data-stu-id="ce9ad-111">Notification</span></span>                                                        | <span data-ttu-id="ce9ad-112">Description</span><span class="sxs-lookup"><span data-stu-id="ce9ad-112">Description</span></span>                                        |
|---------------------------------------------------------------------|----------------------------------------------------|
| [<span data-ttu-id="ce9ad-113">**SPFILENOTIFY \_ FILEEXTRACTED**</span><span class="sxs-lookup"><span data-stu-id="ce9ad-113">**SPFILENOTIFY\_FILEEXTRACTED**</span></span>](spfilenotify-fileextracted.md)   | <span data-ttu-id="ce9ad-114">已從封包解壓縮檔案。</span><span class="sxs-lookup"><span data-stu-id="ce9ad-114">The file has been extracted from the cabinet.</span></span>      |
| [<span data-ttu-id="ce9ad-115">**SPFILENOTIFY \_ FILEINCABINET**</span><span class="sxs-lookup"><span data-stu-id="ce9ad-115">**SPFILENOTIFY\_FILEINCABINET**</span></span>](spfilenotify-fileincabinet.md)   | <span data-ttu-id="ce9ad-116">在封包中發現檔案。</span><span class="sxs-lookup"><span data-stu-id="ce9ad-116">A file is encountered in the cabinet.</span></span>              |
| [<span data-ttu-id="ce9ad-117">**SPFILENOTIFY \_ NEEDNEWCABINET**</span><span class="sxs-lookup"><span data-stu-id="ce9ad-117">**SPFILENOTIFY\_NEEDNEWCABINET**</span></span>](spfilenotify-neednewcabinet.md) | <span data-ttu-id="ce9ad-118">目前的檔案會在下一個封包中繼續。</span><span class="sxs-lookup"><span data-stu-id="ce9ad-118">The current file is continued in the next cabinet.</span></span> |



 

<span data-ttu-id="ce9ad-119">最後兩個參數 *Param1* 和 *Param2* 也是不帶正負號的整數，並包含與通知相關的其他資訊。</span><span class="sxs-lookup"><span data-stu-id="ce9ad-119">The final two parameters, *Param1* and *Param2*, are also unsigned integers and contain additional information relevant to the notification.</span></span> <span data-ttu-id="ce9ad-120">如需 [**SetupIterateCabinet**](/windows/desktop/api/Setupapi/nf-setupapi-setupiteratecabineta)所傳送通知的詳細資訊，請參閱封 [包檔通知](cabinet-file-notifications.md)。</span><span class="sxs-lookup"><span data-stu-id="ce9ad-120">For more information about the notifications sent by [**SetupIterateCabinet**](/windows/desktop/api/Setupapi/nf-setupapi-setupiteratecabineta), see [Cabinet File Notifications](cabinet-file-notifications.md).</span></span>

<span data-ttu-id="ce9ad-121">SP 檔案 \_ \_ 通知 \_ 回呼常式傳回不帶正負號的整數。</span><span class="sxs-lookup"><span data-stu-id="ce9ad-121">A SP\_FILE\_NOTIFY\_CALLBACK routine returns an unsigned integer.</span></span> <span data-ttu-id="ce9ad-122">根據通知，封包回呼常式應該會傳回下列其中一個值。</span><span class="sxs-lookup"><span data-stu-id="ce9ad-122">The cabinet callback routine should return one of the following values depending on the notification.</span></span>

<span data-ttu-id="ce9ad-123">針對 SPFILENOTIFY \_ FILEINCABINET 通知， [**SetupIterateCabinet**](/windows/desktop/api/Setupapi/nf-setupapi-setupiteratecabineta) 預期回呼常式會傳回下列其中一個值。</span><span class="sxs-lookup"><span data-stu-id="ce9ad-123">For the SPFILENOTIFY\_FILEINCABINET notification, [**SetupIterateCabinet**](/windows/desktop/api/Setupapi/nf-setupapi-setupiteratecabineta) expects one of the following values to be returned by the callback routine.</span></span>



| <span data-ttu-id="ce9ad-124">值</span><span class="sxs-lookup"><span data-stu-id="ce9ad-124">Value</span></span>         | <span data-ttu-id="ce9ad-125">意義</span><span class="sxs-lookup"><span data-stu-id="ce9ad-125">Meaning</span></span>                   |
|---------------|---------------------------|
| <span data-ttu-id="ce9ad-126">FILEOP \_ 中止</span><span class="sxs-lookup"><span data-stu-id="ce9ad-126">FILEOP\_ABORT</span></span> | <span data-ttu-id="ce9ad-127">中止封包處理。</span><span class="sxs-lookup"><span data-stu-id="ce9ad-127">Abort cabinet processing.</span></span> |
| <span data-ttu-id="ce9ad-128">FILEOP \_ DOIT R</span><span class="sxs-lookup"><span data-stu-id="ce9ad-128">FILEOP\_DOIT</span></span>  | <span data-ttu-id="ce9ad-129">將目前的檔案解壓縮。</span><span class="sxs-lookup"><span data-stu-id="ce9ad-129">Extract the current file.</span></span> |
| <span data-ttu-id="ce9ad-130">FILEOP \_ SKIP</span><span class="sxs-lookup"><span data-stu-id="ce9ad-130">FILEOP\_SKIP</span></span>  | <span data-ttu-id="ce9ad-131">略過目前的檔案。</span><span class="sxs-lookup"><span data-stu-id="ce9ad-131">Skip the current file.</span></span>    |



 

<span data-ttu-id="ce9ad-132">針對 SPFILENOTIFY \_ NEEDNEWCABINET 和 SPFILENOTIFY \_ FILEEXTRACTED 通知， **SetupIterateCabinet** 預期回呼常式會傳回下列其中一個值。</span><span class="sxs-lookup"><span data-stu-id="ce9ad-132">For SPFILENOTIFY\_NEEDNEWCABINET and SPFILENOTIFY\_FILEEXTRACTED notifications, **SetupIterateCabinet** expects one of the following values to be returned by the callback routine.</span></span>



| <span data-ttu-id="ce9ad-133">值</span><span class="sxs-lookup"><span data-stu-id="ce9ad-133">Value</span></span>      | <span data-ttu-id="ce9ad-134">意義</span><span class="sxs-lookup"><span data-stu-id="ce9ad-134">Meaning</span></span>                                                                                                                                                                                                                           |
|------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ce9ad-135">沒有 \_ 錯誤</span><span class="sxs-lookup"><span data-stu-id="ce9ad-135">NO\_ERROR</span></span>  | <span data-ttu-id="ce9ad-136">未發生任何錯誤，請繼續處理封包。</span><span class="sxs-lookup"><span data-stu-id="ce9ad-136">No error was encountered, continue processing the cabinet.</span></span>                                                                                                                                                                        |
| <span data-ttu-id="ce9ad-137">錯誤 \_ XXX</span><span class="sxs-lookup"><span data-stu-id="ce9ad-137">ERROR\_XXX</span></span> | <span data-ttu-id="ce9ad-138">發生指定的類型時發生錯誤。</span><span class="sxs-lookup"><span data-stu-id="ce9ad-138">An error of the specified type occurred.</span></span> <span data-ttu-id="ce9ad-139">[**SetupIterateCabinet**](/windows/desktop/api/Setupapi/nf-setupapi-setupiteratecabineta)函式會傳回 **FALSE**，而指定的錯誤碼會由對 [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror)的呼叫傳回。</span><span class="sxs-lookup"><span data-stu-id="ce9ad-139">The [**SetupIterateCabinet**](/windows/desktop/api/Setupapi/nf-setupapi-setupiteratecabineta) function will return **FALSE**, and the specified error code will be returned by a call to [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror).</span></span> |



 

<span data-ttu-id="ce9ad-140">如果回呼常式傳回 FILEOP \_ doit r，則常式也必須提供完整的目標路徑。</span><span class="sxs-lookup"><span data-stu-id="ce9ad-140">If the callback routine returns FILEOP\_DOIT, the routine must also provide a full target path.</span></span> <span data-ttu-id="ce9ad-141">如需詳細資訊，請參閱 [**SPFILENOTIFY \_ FILEINCABINET**](spfilenotify-fileincabinet.md)。</span><span class="sxs-lookup"><span data-stu-id="ce9ad-141">For more information see [**SPFILENOTIFY\_FILEINCABINET**](spfilenotify-fileincabinet.md).</span></span>

 

 
