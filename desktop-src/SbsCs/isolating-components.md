---
description: 編寫完善的元件不會擾亂過程裝載應用程式的環境，也不會流失啟用內容。
ms.assetid: cc3e21fd-5fd3-40b6-9218-cb5f47be3567
title: 隔離元件
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 411d5e90114b7509dff2e5e48a4770841774df52fce804895155d2bd4d43e514
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119885188"
---
# <a name="isolating-components"></a>隔離元件

編寫完善的元件不會擾亂過程裝載應用程式的環境，也不會流失啟用內容。 編寫完善的元件會執行自己的內容管理，而不是依賴主控應用程式的環境。

主控元件的作者是最好的位置，以確切瞭解元件所需的其他元件。 依賴主機應用程式，為您的託管元件提供正確的環境，是可能的錯誤來源。 請改為建立裝載元件的資訊清單，以指定其所有相依性，然後使用 \_ 已啟用的隔離感知來進行編譯 \_ 。 這可確保隔離您的元件所進行的外部呼叫，並使用正確的版本。 由於 \_ 啟用隔離感知的啟用內容 \_ 是針對每個 dll，因此可以安全地在多個 dll 中使用，而每個 dll 都有自己的資訊清單來呼叫相依性。

如果無法在啟用隔離感知的情況下進行編譯 \_ \_ ，請使用類似于 [使用託管元件的回呼](using-callbacks-from-hosted-components.md)所提供的解決方案。

您應該在裝載應用程式可以呼叫的所有進入點中啟用自己的啟用內容，以確保您的託管元件完全以正確的啟用內容執行。 您可以使用 c + + helper 物件來加速變更所有 e。 例如，您可以使用 c + + 類別，如下所示：


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



然後，您可以在元件中使用全域變數來儲存應該在每個進入點上啟用的啟用內容。 如此一來，您就可以將您的元件與裝載應用程式隔離。


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



 

 



