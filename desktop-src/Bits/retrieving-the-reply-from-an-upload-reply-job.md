---
title: 從 Upload-Reply 作業中取出回復
description: 若要將資料上傳至伺服器應用程式，並將資料傳回給用戶端，請將作業指定為 BG \_ 作業 \_ 類型 \_ 上傳 \_ 回復工作。
ms.assetid: bab28a2c-1e2f-4b76-9dc6-57df26f7efec
ms.topic: article
ms.date: 11/29/2018
ms.openlocfilehash: 79ca145a3ed243209fc0059b20823e32da3cf3974850a6bc3e872f43dbd40aa1
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120004878"
---
# <a name="retrieving-the-reply-from-an-upload-reply-job"></a>從 Upload-Reply 作業中取出回復

除了將檔案上傳至伺服器之外，BITS Upload-Reply 作業也會檢查隨伺服器回復一起傳送的回復 URL，然後自動遵循回復 URL，然後再從該 URL 下載回應。 如需有關 BITS-回復 URL 標頭值的詳細資訊，請參閱「通知 [片段](/windows/desktop/Bits/ack-for-fragment) 」檔。

將作業類型設定為 BG \_ 作業 \_ 類型 \_ 上傳 \_ 回復，以建立 Upload-Reply 類型的作業。 當工作進入「BG 工作狀態」狀態時，用戶端就可以使用回復資料 \_ \_ \_ 。 若要取得回復，請呼叫下列其中一種方法：

-   [**IBackgroundCopyJob2::GetReplyData**](/windows/desktop/api/Bits1_5/nf-bits1_5-ibackgroundcopyjob2-getreplydata)

    提供回復資料的記憶體中複本。 您可以使用這個方法，在呼叫 [**IBackgroundCopyJob：： Complete**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-complete) 方法之前或之後讀取回復資料。 如果回復資料超過 1 MB，則應用程式必須呼叫 [**IBackgroundCopyJob2：： GetReplyFileName**](/windows/desktop/api/Bits1_5/nf-bits1_5-ibackgroundcopyjob2-getreplyfilename) 方法來取出回復檔案的名稱，並直接讀取其內容。

-   [**IBackgroundCopyJob2::GetReplyFileName**](/windows/desktop/api/Bits1_5/nf-bits1_5-ibackgroundcopyjob2-getreplyfilename)

    提供包含回復的檔案名。 開啟和讀取回復檔案之前，您必須先呼叫 **IBackgroundCopyJob：： Complete** 方法;除非您呼叫 **Complete** 方法，否則無法將回復檔案提供給用戶端。

只有當回復很小，而且可以快速處理，以便不封鎖回呼執行緒時，才在 [**IBackgroundCopyCallback：： JobTransferred**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopycallback-jobtransferred) 方法中呼叫這些方法。 如果您使用 [**命令列通知**](/windows/desktop/api/Bits1_5/nf-bits1_5-ibackgroundcopyjob2-setnotifycmdline) 而不是回呼，請將作業識別碼傳遞給可執行檔。 可執行檔會使用作業識別碼來呼叫 **Complete** 方法，讓回復檔案可供使用。

下列範例示範如何使用每個方法來取得回復資料。

-   [使用 GetReplyData](#using-getreplydata)
-   [使用 GetReplyFileName](#using-getreplyfilename)

## <a name="using-getreplydata"></a>使用 GetReplyData

下列範例示範如何使用 [**IBackgroundCopyJob2：： GetReplyData**](/windows/desktop/api/Bits1_5/nf-bits1_5-ibackgroundcopyjob2-getreplydata) 方法來取得回復資料。 此範例假設 [**IBackgroundCopyJob**](/windows/desktop/api/Bits/nn-bits-ibackgroundcopyjob) 介面指標有效、工作的類型為上傳-回復，且工作的狀態為已傳輸的 BG \_ 工作 \_ 狀態 \_ 。


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



## <a name="using-getreplyfilename"></a>使用 GetReplyFileName

下列範例示範如何使用 [**IBackgroundCopyJob2：： GetReplyFileName**](/windows/desktop/api/Bits1_5/nf-bits1_5-ibackgroundcopyjob2-getreplyfilename) 方法來取得回復資料。 此範例假設 [**IBackgroundCopyJob**](/windows/desktop/api/Bits/nn-bits-ibackgroundcopyjob) 介面指標有效、工作的類型為上傳-回復，且作業的狀態為「BG \_ 作業狀態已傳輸 \_ 」 \_ 。


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



 

 




