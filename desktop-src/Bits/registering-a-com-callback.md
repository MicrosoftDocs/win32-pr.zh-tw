---
title: 註冊 COM 回呼
description: 您可以註冊以在作業的狀態變更時接收通知，而不是輪詢作業狀態中的變更。
ms.assetid: 29350ea4-f7a9-4a42-a531-2cf623fe247b
keywords:
- 傳送工作 BITS，事件通知
- 註冊事件通知位
- 事件通知位
- 事件通知位，回呼
- 通知事件位
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cdcc52c772656c2168af9c10724ee43fac25aa80
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104315694"
---
# <a name="registering-a-com-callback"></a>註冊 COM 回呼

您可以註冊以在作業的狀態變更時接收通知，而不是 [輪詢](polling-for-the-status-of-the-job.md) 作業狀態中的變更。 若要接收通知，您必須執行 [**IBackgroundCopyCallback2**](/windows/desktop/api/Bits3_0/nn-bits3_0-ibackgroundcopycallback2) 介面。 介面會根據您的註冊，包含下列各位呼叫的方法：

-   [**JobTransferred**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopycallback-jobtransferred)
-   [**JobError**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopycallback-joberror)
-   [**JobModification**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopycallback-jobmodification)
-   [**FileTransferred**](/windows/desktop/api/Bits3_0/nf-bits3_0-ibackgroundcopycallback2-filetransferred)

如需執行 [**IBackgroundCopyCallback2**](/windows/desktop/api/Bits3_0/nn-bits3_0-ibackgroundcopycallback2) 介面的範例，請參閱 [**IBackgroundCopyCallback**](/windows/desktop/api/Bits/nn-bits-ibackgroundcopycallback) 介面主題中的範例程式碼。

[**IBackgroundCopyCallback2**](/windows/desktop/api/Bits3_0/nn-bits3_0-ibackgroundcopycallback2)介面會在檔案傳送時提供通知。 一般而言，您會使用此方法來驗證檔案，以便讓對等檔可以進行下載;否則，在您呼叫 [**IBackgroundCopyJob：： Complete**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-complete) 方法之前，將無法使用該檔案。 若要驗證檔案，請呼叫 [**IBackgroundCopyFile3：： SetValidationState**](/windows/desktop/api/Bits3_0/nf-bits3_0-ibackgroundcopyfile3-setvalidationstate) 方法。

註冊 COM 回呼的方法有兩種：註冊回呼物件或註冊回呼類別識別碼。 使用回呼物件較為簡單且較低的額外負荷;使用回呼 CLSID 更可靠，但更複雜。 您可以註冊、兩者或兩者皆會使用回呼物件（如果有的話），而且仍可呼叫，並且會根據提供的類別識別碼（如果失敗）切換回具現化新的物件。

### <a name="registering-a-callback-object"></a>註冊回呼物件

若要向 BITS 註冊您的執行，請呼叫 [**IBackgroundCopyJob：： SetNotifyInterface**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-setnotifyinterface) 方法。 若要指定 BITS 呼叫的方法，請呼叫 [**IBackgroundCopyJob：： SetNotifyFlags**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-setnotifyflags)方法。

當您的應用程式終止時，通知介面會變成無效;BITS 不會保存通知介面。 因此，您應用程式的初始化程式應該註冊您要接收通知的現有工作。 如果您需要捕獲自上一次執行應用程式之後發生的狀態和進度資訊，請在應用程式初始化期間輪詢狀態和進度資訊。

在結束之前，您的應用程式應該清除回呼介面指標 (**SetNotifyInterface (Null)**) 。 更有效率的方式是清除回呼指標，而不是讓 BITS 發現它不再有效。

請注意，如果有一個以上的應用程式呼叫 [**SetNotifyInterface**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-setnotifyinterface) 方法來設定作業的通知介面，則呼叫 **SetNotifyInterface** 方法的最後一個應用程式就是要接收通知的應用程式，其他應用程式不會收到通知。

下列範例顯示如何註冊通知。 此範例假設 [**IBackgroundCopyJob**](/windows/desktop/api/Bits/nn-bits-ibackgroundcopyjob) 介面指標有效。 如需在下列範例中使用的 CNotifyInterface 範例類別的詳細資訊，請參閱 [**IBackgroundCopyCallback**](/windows/desktop/api/Bits/nn-bits-ibackgroundcopycallback) 介面。


```C++
HRESULT hr;
IBackgroundCopyJob* pJob;
CNotifyInterface *pNotify = new CNotifyInterface();

if (pNotify)
{
    hr = pJob->SetNotifyInterface(pNotify);
    if (SUCCEEDED(hr))
    {
        hr = pJob->SetNotifyFlags(BG_NOTIFY_JOB_TRANSFERRED | 
                                  BG_NOTIFY_JOB_ERROR );
    }
    pNotify->Release();
    pNotify = NULL;

    if (FAILED(hr))
    {
        //Handle error - unable to register callbacks.
    }
}
```



### <a name="registering-a-callback-clsid"></a>註冊回呼 CLSID

若要向 BITS 註冊回呼 CLSID，請使用 **bits \_ 作業 \_ 屬性 \_ 通知 \_ CLSID** PropertyId 呼叫 [**IBackgroundCopyJob5：： SetProperty**](/windows/desktop/api/Bits5_0/nf-bits5_0-ibackgroundcopyjob5-setproperty)方法。 若要指定 BITS 呼叫的方法，請呼叫 [**IBackgroundCopyJob：： SetNotifyFlags**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-setnotifyflags) 方法。

您必須先確定通知 CLSID 已註冊到跨進程 COM 伺服器，然後再向 BITS 工作註冊 CLSID。 相較于定義和傳遞回呼物件，相較于定義和傳遞回呼物件，相較于定義和傳遞 [COM 伺服器](/windows/desktop/com/com-server-responsibilities) ，有許多重要的優點 COM 伺服器可讓 BITS 在系統重新開機期間，以及針對大型或長期的作業，維護 BITS 作業與應用程式程式碼之間的關聯。 COM 伺服器也可讓您的應用程式完全關閉，而 BITS 會繼續在背景執行傳輸，進而改善系統的電池、CPU 和記憶體使用量。

為了提供您已註冊要接收的通知，BITS 會先嘗試呼叫您可能已附加之任何現有回呼物件的對應方法。 如果沒有任何現有的物件，或現有的物件已中斷連線 (通常是因為您的應用程式終止) ，BITS 會使用通知 CLSID 來呼叫 CoCreateInstance 以具現化新的回呼物件，並將該物件用於任何進一步的回呼，直到它中斷連接，或由新的 [**IBackgroundCopyJob：： SetNotifyInterface**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-setnotifyinterface)呼叫取代。

與回呼物件不同的是，如果 BITS 服務或系統已關閉並重新啟動，回呼 CLSID 將會連同對應的 BITS 作業 (的) 保存在一起。 您的應用程式可能會在結束 (之前清除任何先前設定的通知 CLSID，或在任何其他時間透過傳遞 GUID Null 的新通知 CLSID 來) \_ ，但如果您的應用程式已註冊，而您的應用程式已註冊，而您的應用程式已註冊為回應 clsid 要求，則您的應用程式可能會想要讓註冊通知 clsid 請注意，如果有一個以上的應用程式設定，則會呼叫 **bits \_ 作業 \_ 屬性 \_ 通知 \_ CLSID** 屬性，最後要設定的 CLSID 就是用來具現化回呼物件的最新 clsid –將不會具現化其他的 clsid。 同樣地，如果有一個應用程式註冊 CLSID，另一個註冊回呼物件，則會優先使用回呼物件的一般規則，而且除非已清除或中斷回呼物件，否則不會使用 CLSID。

下列範例顯示如何註冊 CLSID 通知。 此範例假設 [**IBackgroundCopyJob5**](/windows/desktop/api/Bits5_0/nn-bits5_0-ibackgroundcopyjob5) 介面指標有效，且您的應用程式已註冊為執行 CNotifyInterface 類別的跨進程 COM 伺服器。 如需在下列範例中使用的 CNotifyInterface 範例類別的詳細資訊，請參閱 [**IBackgroundCopyCallback**](/windows/desktop/api/Bits/nn-bits-ibackgroundcopycallback) 介面。


```C++
HRESULT hr; 
IBackgroundCopyJob5* job; 
BITS_JOB_PROPERTY_VALUE propertyValue; 
propertyValue.ClsID = __uuidof(CNotifyInterface); 

hr = job->SetProperty(BITS_JOB_PROPERTY_NOTIFICATION_CLSID, propertyValue); 
if (SUCCEEDED(hr)) 
{ 
    hr = job->SetNotifyFlags(BG_NOTIFY_JOB_TRANSFERRED |  
                             BG_NOTIFY_JOB_ERROR); 
} 

if (FAILED(hr)) 
{ 
    // Handle error - unable to register callbacks. 
} 
```



 

 