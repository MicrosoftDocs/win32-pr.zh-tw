---
title: 從 Upload-Reply 作業中取出回復
description: 若要將資料上傳至伺服器應用程式，並將資料傳回給用戶端，請將作業指定為 BG \_ 作業 \_ 類型 \_ 上傳 \_ 回復工作。
ms.assetid: bab28a2c-1e2f-4b76-9dc6-57df26f7efec
ms.topic: article
ms.date: 11/29/2018
ms.openlocfilehash: 582a37a31c13c5cc3e0b44c51a767cfbe465c64c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103931955"
---
# <a name="retrieving-the-reply-from-an-upload-reply-job"></a><span data-ttu-id="676b5-103">從 Upload-Reply 作業中取出回復</span><span class="sxs-lookup"><span data-stu-id="676b5-103">Retrieving the Reply from an Upload-Reply Job</span></span>

<span data-ttu-id="676b5-104">除了將檔案上傳至伺服器之外，BITS Upload-Reply 作業也會檢查隨伺服器回復一起傳送的回復 URL，然後自動遵循回復 URL，然後再從該 URL 下載回應。</span><span class="sxs-lookup"><span data-stu-id="676b5-104">A BITS Upload-Reply job, in addition to uploading a file to a server, will also examine a reply URL sent as part of the server reply and then automatically follow the reply URL and download a response from it.</span></span> <span data-ttu-id="676b5-105">如需有關 BITS-回復 URL 標頭值的詳細資訊，請參閱「通知 [片段](/windows/desktop/Bits/ack-for-fragment) 」檔。</span><span class="sxs-lookup"><span data-stu-id="676b5-105">See the [Ack for Fragment](/windows/desktop/Bits/ack-for-fragment) documentation for more details about the BITS-Reply-URL header value.</span></span>

<span data-ttu-id="676b5-106">將作業類型設定為 BG \_ 作業 \_ 類型 \_ 上傳 \_ 回復，以建立 Upload-Reply 類型的作業。</span><span class="sxs-lookup"><span data-stu-id="676b5-106">Set the job type as BG\_JOB\_TYPE\_UPLOAD\_REPLY to create an Upload-Reply type job.</span></span> <span data-ttu-id="676b5-107">當工作進入「BG 工作狀態」狀態時，用戶端就可以使用回復資料 \_ \_ \_ 。</span><span class="sxs-lookup"><span data-stu-id="676b5-107">The reply data is available to the client after the job enters the BG\_JOB\_STATE\_TRANSFERRED state.</span></span> <span data-ttu-id="676b5-108">若要取得回復，請呼叫下列其中一種方法：</span><span class="sxs-lookup"><span data-stu-id="676b5-108">To retrieve the reply, call one of the following methods:</span></span>

-   [<span data-ttu-id="676b5-109">**IBackgroundCopyJob2::GetReplyData**</span><span class="sxs-lookup"><span data-stu-id="676b5-109">**IBackgroundCopyJob2::GetReplyData**</span></span>](/windows/desktop/api/Bits1_5/nf-bits1_5-ibackgroundcopyjob2-getreplydata)

    <span data-ttu-id="676b5-110">提供回復資料的記憶體中複本。</span><span class="sxs-lookup"><span data-stu-id="676b5-110">Provides an in-memory copy of the reply data.</span></span> <span data-ttu-id="676b5-111">您可以使用這個方法，在呼叫 [**IBackgroundCopyJob：： Complete**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-complete) 方法之前或之後讀取回復資料。</span><span class="sxs-lookup"><span data-stu-id="676b5-111">Use this method to read the reply data before or after calling the [**IBackgroundCopyJob::Complete**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-complete) method.</span></span> <span data-ttu-id="676b5-112">如果回復資料超過 1 MB，則應用程式必須呼叫 [**IBackgroundCopyJob2：： GetReplyFileName**](/windows/desktop/api/Bits1_5/nf-bits1_5-ibackgroundcopyjob2-getreplyfilename) 方法來取出回復檔案的名稱，並直接讀取其內容。</span><span class="sxs-lookup"><span data-stu-id="676b5-112">If the reply data exceeds 1 MB, the application must call the [**IBackgroundCopyJob2::GetReplyFileName**](/windows/desktop/api/Bits1_5/nf-bits1_5-ibackgroundcopyjob2-getreplyfilename) method to retrieve the name of the reply file and read its contents directly.</span></span>

-   [<span data-ttu-id="676b5-113">**IBackgroundCopyJob2::GetReplyFileName**</span><span class="sxs-lookup"><span data-stu-id="676b5-113">**IBackgroundCopyJob2::GetReplyFileName**</span></span>](/windows/desktop/api/Bits1_5/nf-bits1_5-ibackgroundcopyjob2-getreplyfilename)

    <span data-ttu-id="676b5-114">提供包含回復的檔案名。</span><span class="sxs-lookup"><span data-stu-id="676b5-114">Provides the name of the file that contains the reply.</span></span> <span data-ttu-id="676b5-115">開啟和讀取回復檔案之前，您必須先呼叫 **IBackgroundCopyJob：： Complete** 方法;除非您呼叫 **Complete** 方法，否則無法將回復檔案提供給用戶端。</span><span class="sxs-lookup"><span data-stu-id="676b5-115">You must call the **IBackgroundCopyJob::Complete** method before opening and reading the reply file; the reply file is not available to the client until you call the **Complete** method.</span></span>

<span data-ttu-id="676b5-116">只有當回復很小，而且可以快速處理，以便不封鎖回呼執行緒時，才在 [**IBackgroundCopyCallback：： JobTransferred**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopycallback-jobtransferred) 方法中呼叫這些方法。</span><span class="sxs-lookup"><span data-stu-id="676b5-116">Call these methods in your [**IBackgroundCopyCallback::JobTransferred**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopycallback-jobtransferred) method only if the reply is small and can be processed quickly so as to not block the callback thread.</span></span> <span data-ttu-id="676b5-117">如果您使用 [**命令列通知**](/windows/desktop/api/Bits1_5/nf-bits1_5-ibackgroundcopyjob2-setnotifycmdline) 而不是回呼，請將作業識別碼傳遞給可執行檔。</span><span class="sxs-lookup"><span data-stu-id="676b5-117">If you use [**command line notification**](/windows/desktop/api/Bits1_5/nf-bits1_5-ibackgroundcopyjob2-setnotifycmdline) instead of the callback, pass the job identifier to the executable file.</span></span> <span data-ttu-id="676b5-118">可執行檔會使用作業識別碼來呼叫 **Complete** 方法，讓回復檔案可供使用。</span><span class="sxs-lookup"><span data-stu-id="676b5-118">The executable file uses the job identifier to call the **Complete** method to make the reply file available.</span></span>

<span data-ttu-id="676b5-119">下列範例示範如何使用每個方法來取得回復資料。</span><span class="sxs-lookup"><span data-stu-id="676b5-119">The following examples show how to use each method to retrieve the reply data.</span></span>

-   [<span data-ttu-id="676b5-120">使用 GetReplyData</span><span class="sxs-lookup"><span data-stu-id="676b5-120">Using GetReplyData</span></span>](#using-getreplydata)
-   [<span data-ttu-id="676b5-121">使用 GetReplyFileName</span><span class="sxs-lookup"><span data-stu-id="676b5-121">Using GetReplyFileName</span></span>](#using-getreplyfilename)

## <a name="using-getreplydata"></a><span data-ttu-id="676b5-122">使用 GetReplyData</span><span class="sxs-lookup"><span data-stu-id="676b5-122">Using GetReplyData</span></span>

<span data-ttu-id="676b5-123">下列範例示範如何使用 [**IBackgroundCopyJob2：： GetReplyData**](/windows/desktop/api/Bits1_5/nf-bits1_5-ibackgroundcopyjob2-getreplydata) 方法來取得回復資料。</span><span class="sxs-lookup"><span data-stu-id="676b5-123">The following example shows how to retrieve the reply data using the [**IBackgroundCopyJob2::GetReplyData**](/windows/desktop/api/Bits1_5/nf-bits1_5-ibackgroundcopyjob2-getreplydata) method.</span></span> <span data-ttu-id="676b5-124">此範例假設 [**IBackgroundCopyJob**](/windows/desktop/api/Bits/nn-bits-ibackgroundcopyjob) 介面指標有效、工作的類型為上傳-回復，且工作的狀態為已傳輸的 BG \_ 工作 \_ 狀態 \_ 。</span><span class="sxs-lookup"><span data-stu-id="676b5-124">The example assumes the [**IBackgroundCopyJob**](/windows/desktop/api/Bits/nn-bits-ibackgroundcopyjob) interface pointer is valid, the type of the job is upload-reply, and the state of the job is BG\_JOB\_STATE\_TRANSFERRED.</span></span>


```C++
HRESULT hr;
IBackgroundCopyJob* pJob;
IBackgroundCopyJob2* pJob2 = NULL;
BYTE* pReply = NULL;
UINT64 ReplySize;

//Need to query the IBackgroundCopyJob interface for an IBackgroundCopyJob2
//interface pointer. The IBackgroundCopyJob2 interface contains the GetReplyData method.
hr = pJob->QueryInterface(__uuidof(IBackgroundCopyJob2), (void**)&pJob2);
if (SUCCEEDED(hr))
{
    hr = pJob2->GetReplyData(&pReply, &ReplySize);
    if (S_OK == hr))
    {
        if (pReply)
        {
            //Do something with the data.
            CoTaskMemFree(pReply);
        }
        else
        {
            //The server application did not return a reply.
        }
    }
    else if (BG_E_TOO_LARGE == hr)
    {
        //The reply exceeds 1 MB. To retrieve the reply, get the reply file name,
        //complete the job, open the reply file, and read the reply.
    }
    else
    {
        //Handle the error
    }

    pJob2->Release(); //When done, release the interface.
}
else
{
    //Handle error. QueryInterface will return E_NOINTERFACE if the version of BITS
    //running on the computer is less than BITS 1.5.
}
```



## <a name="using-getreplyfilename"></a><span data-ttu-id="676b5-125">使用 GetReplyFileName</span><span class="sxs-lookup"><span data-stu-id="676b5-125">Using GetReplyFileName</span></span>

<span data-ttu-id="676b5-126">下列範例示範如何使用 [**IBackgroundCopyJob2：： GetReplyFileName**](/windows/desktop/api/Bits1_5/nf-bits1_5-ibackgroundcopyjob2-getreplyfilename) 方法來取得回復資料。</span><span class="sxs-lookup"><span data-stu-id="676b5-126">The following example shows how to retrieve the reply data using the [**IBackgroundCopyJob2::GetReplyFileName**](/windows/desktop/api/Bits1_5/nf-bits1_5-ibackgroundcopyjob2-getreplyfilename) method.</span></span> <span data-ttu-id="676b5-127">此範例假設 [**IBackgroundCopyJob**](/windows/desktop/api/Bits/nn-bits-ibackgroundcopyjob) 介面指標有效、工作的類型為上傳-回復，且作業的狀態為「BG \_ 作業狀態已傳輸 \_ 」 \_ 。</span><span class="sxs-lookup"><span data-stu-id="676b5-127">The example assumes the [**IBackgroundCopyJob**](/windows/desktop/api/Bits/nn-bits-ibackgroundcopyjob) interface pointer is valid, the type of job is upload-reply, and the state of the job is BG\_JOB\_STATE\_TRANSFERRED.</span></span>


```C++
HRESULT hr;
IBackgroundCopyJob* pJob;
IBackgroundCopyJob2* pJob2 = NULL;
WCHAR* pszFileName = NULL;

//Need to query the IBackgroundCopyJob interface for an IBackgroundCopyJob2
//interface pointer. The IBackgroundCopyJob2 interface contains the GetReplyFileName method.
hr = pJob->QueryInterface(__uuidof(IBackgroundCopyJob2), (void**)&pJob2);
if (SUCCEEDED(hr))
{
    hr = pJob2->GetReplyFileName(&pszFileName);
    if (SUCCEEDED(hr))
    {
        //Calling the Complete method removes the job from the queue, 
        //so make sure you maintain an interface pointer to this job 
        //or retrieve any job related information that you require 
        //when processing the reply.
        hr = pJob->Complete();

        //Open, read the file, and do something with the data.
        CoTaskMemFree(pszFileName);
    }

    pJob2->Release(); //When done, release the interface.
}
else
{
    //Handle error. QueryInterface will return E_NOINTERFACE if the version of BITS
    //running on the computer is less than BITS 1.5.
}
```



 

 




