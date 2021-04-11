---
description: 編寫完善的元件不會擾亂過程裝載應用程式的環境，也不會流失啟用內容。
ms.assetid: cc3e21fd-5fd3-40b6-9218-cb5f47be3567
title: 隔離元件
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5e201375f50324209380a4ecef5fa762ae70e56d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103847901"
---
# <a name="isolating-components"></a><span data-ttu-id="3edb3-103">隔離元件</span><span class="sxs-lookup"><span data-stu-id="3edb3-103">Isolating Components</span></span>

<span data-ttu-id="3edb3-104">編寫完善的元件不會擾亂過程裝載應用程式的環境，也不會流失啟用內容。</span><span class="sxs-lookup"><span data-stu-id="3edb3-104">Well-authored components do not perturb the environment of the hosting application, nor do they leak activation contexts.</span></span> <span data-ttu-id="3edb3-105">編寫完善的元件會執行自己的內容管理，而不是依賴主控應用程式的環境。</span><span class="sxs-lookup"><span data-stu-id="3edb3-105">Well-authored components perform their own context management rather than relying on the hosting application's environment.</span></span>

<span data-ttu-id="3edb3-106">主控元件的作者是最好的位置，以確切瞭解元件所需的其他元件。</span><span class="sxs-lookup"><span data-stu-id="3edb3-106">The author of the hosted component is in the best position to know exactly which other assemblies the component requires.</span></span> <span data-ttu-id="3edb3-107">依賴主機應用程式，為您的託管元件提供正確的環境，是可能的錯誤來源。</span><span class="sxs-lookup"><span data-stu-id="3edb3-107">Relying on the host application to provide the correct environment for your hosted component is a probable source of errors.</span></span> <span data-ttu-id="3edb3-108">請改為建立裝載元件的資訊清單，以指定其所有相依性，然後使用 \_ 已啟用的隔離感知來進行編譯 \_ 。</span><span class="sxs-lookup"><span data-stu-id="3edb3-108">Instead, create a manifest for your hosted component that specifies all its dependencies, and then compile using ISOLATION\_AWARE\_ENABLED.</span></span> <span data-ttu-id="3edb3-109">這可確保隔離您的元件所進行的外部呼叫，並使用正確的版本。</span><span class="sxs-lookup"><span data-stu-id="3edb3-109">This ensures that outside calls made by your component are isolated and use the correct versions.</span></span> <span data-ttu-id="3edb3-110">由於 \_ 啟用隔離感知的啟用內容 \_ 是針對每個 dll，因此可以安全地在多個 dll 中使用，而每個 dll 都有自己的資訊清單來呼叫相依性。</span><span class="sxs-lookup"><span data-stu-id="3edb3-110">Because the activation context that ISOLATION\_AWARE\_ENABLED uses is per-DLL, it is safe to use in multiple DLLs, each with their own manifest calling out dependencies.</span></span>

<span data-ttu-id="3edb3-111">如果無法在啟用隔離感知的情況下進行編譯 \_ \_ ，請使用類似于 [使用託管元件的回呼](using-callbacks-from-hosted-components.md)所提供的解決方案。</span><span class="sxs-lookup"><span data-stu-id="3edb3-111">If it is not possible to compile with ISOLATION\_AWARE\_ENABLED, then use a solution like the one presented in [Using Callbacks From Hosted Components](using-callbacks-from-hosted-components.md).</span></span>

<span data-ttu-id="3edb3-112">您應該在裝載應用程式可以呼叫的所有進入點中啟用自己的啟用內容，以確保您的託管元件完全以正確的啟用內容執行。</span><span class="sxs-lookup"><span data-stu-id="3edb3-112">You should activate your own activation context in all the entry points that the hosting application can call to ensure that your hosted component runs entirely with the correct activation context.</span></span> <span data-ttu-id="3edb3-113">您可以使用 c + + helper 物件來加速變更所有 e。</span><span class="sxs-lookup"><span data-stu-id="3edb3-113">You can use a C++ helper object to facilitate changing all the entrypoints.</span></span> <span data-ttu-id="3edb3-114">例如，您可以使用 c + + 類別，如下所示：</span><span class="sxs-lookup"><span data-stu-id="3edb3-114">For example, you could use a C++ class such as the following:</span></span>


```C++
#include <windows.h>

class CActivationContext 
{
    HANDLE m_hActivationContext;

public:
    CActivationContext() : m_hActivationContext(INVALID_HANDLE_VALUE) 
    {
    }

    VOID Set(HANDLE hActCtx) 
    {
        if (hActCtx != INVALID_HANDLE_VALUE)
            AddRefActCtx(hActCtx);

        if (m_hActivationContext != INVALID_HANDLE_VALUE)
            ReleaseActCtx(m_hActivationContext);
        m_hActivationContext = hActCtx;
    }

    ~CActivationContext() 
    {
        if (m_hActivationContext != INVALID_HANDLE_VALUE)
            ReleaseActCtx(m_hActivationContext);
    }

    BOOL Activate(ULONG_PTR &ulpCookie) 
    {
        return ActivateActCtx(m_hActivationContext, &ulpCookie);
    }

    BOOL Deactivate(ULONG_PTR ulpCookie) 
    {
        return DeactivateActCtx(0, ulpCookie);
    }
};

class CActCtxActivator 
{
    CActivationContext &m_ActCtx;
    ULONG_PTR m_Cookie;
    bool m_fActivated;

public:
    CActCtxActivator(CActivationContext& src, bool fActivate = true) 
        : m_ActCtx(src), m_Cookie(0), m_fActivated(false) 
    {
        if (fActivate) {
            if (src.Activate(m_Cookie))
                m_fActivated = true;
        }
    }

    ~CActCtxActivator() 
    {
        if (m_fActivated) {
            m_ActCtx.Deactivate(m_Cookie);
            m_fActivated = false;
        }
    }
};

```



<span data-ttu-id="3edb3-115">然後，您可以在元件中使用全域變數來儲存應該在每個進入點上啟用的啟用內容。</span><span class="sxs-lookup"><span data-stu-id="3edb3-115">This can then be used in your component, using a global variable to store the activation context that should be activated on each entry point.</span></span> <span data-ttu-id="3edb3-116">如此一來，您就可以將您的元件與裝載應用程式隔離。</span><span class="sxs-lookup"><span data-stu-id="3edb3-116">In this way, you can isolate your component from your hosting application.</span></span>


```C++
CActivationContext s_GlobalContext;

void MyExportedEntrypoint(void) 
{
    CActCtxActivator ScopedContext(s_GlobalContext);
    // Do whatever work here
    // Destructor automatically deactivates the context
}

void MyInitializerFunction() 
{
    HANDLE hActCtx;
    ACTCTX actctx = {sizeof(actctx)};
    hActCtx = CreateActCtx(&actctx);
    s_GlobalContext.Set(hActCtx);
    ReleaseActCtx(hActCtx);
    // The static destructor for s_GlobalContext destroys the
    // activation context on component unload.
}
```



 

 



