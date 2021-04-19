---
description: 啟用內容是參考計數的物件。 您的應用程式必須具有啟用內容的參考，才能使用它。
ms.assetid: 2dc8ffc5-0a65-4227-b93a-30c3cf0d3c2d
title: 參考計數啟用內容
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1ff00afa0dd3a347e14ff9723c06d54af4520ce4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106992084"
---
# <a name="reference-counting-activation-contexts"></a><span data-ttu-id="387d1-104">參考計數啟用內容</span><span class="sxs-lookup"><span data-stu-id="387d1-104">Reference Counting Activation Contexts</span></span>

<span data-ttu-id="387d1-105">啟用內容是參考計數的物件。</span><span class="sxs-lookup"><span data-stu-id="387d1-105">Activation contexts are reference-counted objects.</span></span> <span data-ttu-id="387d1-106">您的應用程式必須具有啟用內容的參考，才能使用它。</span><span class="sxs-lookup"><span data-stu-id="387d1-106">Your application must have a reference on an activation context in order to use it.</span></span> <span data-ttu-id="387d1-107">採用啟用內容之啟用內容 API 的函式可以執行自己的參考計數。</span><span class="sxs-lookup"><span data-stu-id="387d1-107">The functions of the Activation Context API that take an activation context can perform their own reference counting.</span></span> <span data-ttu-id="387d1-108">例如， [**ActivateActCtx**](/windows/desktop/api/Winbase/nf-winbase-activateactctx) 會增加，而且 [**DeactivateActCtx**](/windows/desktop/api/Winbase/nf-winbase-deactivateactctx) 會減少參考計數。</span><span class="sxs-lookup"><span data-stu-id="387d1-108">For example, [**ActivateActCtx**](/windows/desktop/api/Winbase/nf-winbase-activateactctx) increases and [**DeactivateActCtx**](/windows/desktop/api/Winbase/nf-winbase-deactivateactctx) decreases the reference count.</span></span> <span data-ttu-id="387d1-109">但是，如果您的應用程式未使用這些函式就傳遞啟用內容，則應用程式應該提供自己的參考計數方法。</span><span class="sxs-lookup"><span data-stu-id="387d1-109">If however your application passes an activation context without using these functions, the application should provide its own method of reference counting.</span></span>

<span data-ttu-id="387d1-110">當應用程式呼叫 [**CreateActCtx**](/windows/desktop/api/Winbase/nf-winbase-createactctxa)時，傳回的控制碼會有一個的參考計數。</span><span class="sxs-lookup"><span data-stu-id="387d1-110">When an application calls [**CreateActCtx**](/windows/desktop/api/Winbase/nf-winbase-createactctxa), the handle returned will have a reference count of one.</span></span> <span data-ttu-id="387d1-111">當應用程式使用啟動內容完成之後，應該釋放控制碼，並藉由呼叫 [**ReleaseActCtx**](/windows/desktop/api/Winbase/nf-winbase-releaseactctx)減少參考計數。</span><span class="sxs-lookup"><span data-stu-id="387d1-111">After the application finishes with the activation context, the handle should be released and the reference count decreased by calling [**ReleaseActCtx**](/windows/desktop/api/Winbase/nf-winbase-releaseactctx).</span></span> <span data-ttu-id="387d1-112">請勿在啟用內容控制碼上嘗試使用 [**>localfree**](/windows/desktop/api/winbase/nf-winbase-localfree)、 [**HeapFree**](/windows/desktop/api/heapapi/nf-heapapi-heapfree)或任何其他記憶體管理函數。</span><span class="sxs-lookup"><span data-stu-id="387d1-112">Do not attempt to use [**LocalFree**](/windows/desktop/api/winbase/nf-winbase-localfree), [**HeapFree**](/windows/desktop/api/heapapi/nf-heapapi-heapfree), or any other memory-management functions on the activation context handle.</span></span>

<span data-ttu-id="387d1-113">下列範例顯示在啟用內容的存留期處理參考計數的方法。</span><span class="sxs-lookup"><span data-stu-id="387d1-113">The following example shows a method for handling reference counting over the lifetime of an activation context.</span></span> <span data-ttu-id="387d1-114">函式 Funct 會建立啟用內容，然後將其傳遞至物件目標，以將參考計數遞增為2。</span><span class="sxs-lookup"><span data-stu-id="387d1-114">The function Funct creates an activation context, which it then passes to the object Target, which increments the reference count to 2.</span></span> <span data-ttu-id="387d1-115">然後，Funct 會釋出其在啟用內容上的參考，並將參考計數減少回1。</span><span class="sxs-lookup"><span data-stu-id="387d1-115">Funct then releases its reference on the activation context and decreases the reference count back to 1.</span></span> <span data-ttu-id="387d1-116">當再次呼叫 SetActCtx 或終結物件時，目標就會擁有釋放自己的參考。</span><span class="sxs-lookup"><span data-stu-id="387d1-116">Target then owns releasing its own reference when SetActCtx is called again or when the object is destroyed.</span></span>


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



 

 
