---
description: 啟用內容是參考計數的物件。 您的應用程式必須具有啟用內容的參考，才能使用它。
ms.assetid: 2dc8ffc5-0a65-4227-b93a-30c3cf0d3c2d
title: 參考計數啟用內容
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a62f7806a452dc8b98f824069be0cd584c39f45ad9807a97a11f6f3d7c4929f9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119141931"
---
# <a name="reference-counting-activation-contexts"></a>參考計數啟用內容

啟用內容是參考計數的物件。 您的應用程式必須具有啟用內容的參考，才能使用它。 採用啟用內容之啟用內容 API 的函式可以執行自己的參考計數。 例如， [**ActivateActCtx**](/windows/desktop/api/Winbase/nf-winbase-activateactctx) 會增加，而且 [**DeactivateActCtx**](/windows/desktop/api/Winbase/nf-winbase-deactivateactctx) 會減少參考計數。 但是，如果您的應用程式未使用這些函式就傳遞啟用內容，則應用程式應該提供自己的參考計數方法。

當應用程式呼叫 [**CreateActCtx**](/windows/desktop/api/Winbase/nf-winbase-createactctxa)時，傳回的控制碼會有一個的參考計數。 當應用程式使用啟動內容完成之後，應該釋放控制碼，並藉由呼叫 [**ReleaseActCtx**](/windows/desktop/api/Winbase/nf-winbase-releaseactctx)減少參考計數。 請勿在啟用內容控制碼上嘗試使用 [**>localfree**](/windows/desktop/api/winbase/nf-winbase-localfree)、 [**HeapFree**](/windows/desktop/api/heapapi/nf-heapapi-heapfree)或任何其他記憶體管理函數。

下列範例顯示在啟用內容的存留期處理參考計數的方法。 函式 Funct 會建立啟用內容，然後將其傳遞至物件目標，以將參考計數遞增為2。 然後，Funct 會釋出其在啟用內容上的參考，並將參考計數減少回1。 當再次呼叫 SetActCtx 或終結物件時，目標就會擁有釋放自己的參考。


```C++
#include <windows.h>

class CMyObject 
{
private:
    HANDLE m_hActCtx;
public:
    CMyObject() : m_hActCtx(INVALID_HANDLE_VALUE) { }
    ~CMyObject() 
    { 
        if (m_hActCtx != INVALID_HANDLE_VALUE) 
        {
            ReleaseActCtx(m_hActCtx);
            m_hActCtx = INVALID_HANDLE_VALUE;
        }
    }
    void SetActCtx(HANDLE hActCtx) 
    {
        if (m_hActCtx != INVALID_HANDLE_VALUE) 
        {
            ReleaseActCtx(m_hActCtx);
        }
        m_hActCtx = hActCtx;
        if (m_hActCtx != INVALID_HANDLE_VALUE) 
        {
            AddRefActCtx(m_hActCtx);
        }
    }
    void DoWorkWithActCtx();
};

void Funct(CMyObject &Target) 
{
    HANDLE hActCtx;
    ACTCTX actctx = { sizeof(ACTCTX) };
    hActCtx = CreateActCtx(&actctx);  //create activation context  
    Target.SetActCtx(hActCtx);    //pass activation context to Target; 
    // actctx now has 1 more reference
    ReleaseActCtx(hActCtx);
}
```



 

 
