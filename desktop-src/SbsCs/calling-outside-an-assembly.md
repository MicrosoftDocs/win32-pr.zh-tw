---
description: 在元件外部呼叫
ms.assetid: 7a59f707-fb89-4899-891f-4cd556b62b26
title: 在元件外部呼叫
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3ed60536c3daa62957929dd1d3f1a850fd551ae9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106975138"
---
# <a name="calling-outside-an-assembly"></a>在元件外部呼叫

在元件外部呼叫時，裝載的元件應該確保正確的啟用內容為作用中。 呼叫 [**CreateActCtx**](/windows/desktop/api/Winbase/nf-winbase-createactctxa) 然後再呼叫 [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) 或 [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance)來呼叫外部程式碼，則應該以用來尋找它的相同內容呼叫。 呼叫在啟用內容之外找到的程式碼，或呼叫回裝載應用程式的程式碼，應該使用應用程式預設啟用內容來呼叫。

\_ \_ 在託管元件之外呼叫時，使用已定義隔離感知的編譯可能會很有用。 不過，這表示只有 Windows Api 的呼叫會隔離到元件的啟用內容。 這在大多數情況下已足夠，因為呼叫協力廠商函式在呼叫之前未啟用內容。 \_ \_ 如果您的元件搭配各種平臺 api 使用多個啟用內容，則使用已定義的隔離感知來編譯時，不會有説明。

若要執行這項操作，請使用啟用內容啟動程式，例如 [隔離元件](isolating-components.md)中所呈現的範例。 這裡的外部資訊清單是元件建立所在的相依性集合，也許它包含一些擴充的元件清單，這些元件會在執行時間載入和使用。 InternalcoNtext 包含元件在其存留期內確定使用的相依性集合，而且應該在外部的所有 e 中設定。 請注意，此內部內容會在所有 e 中啟動，而內容啟動項會與 c + + 範圍一起使用，以便在呼叫此元件所使用的各種外部程式碼時，設定適當的內容。

``` syntax
CActivationContext s_InternalContext;
CActivationContext s_OutboundContext;
CActivationContext s_ExternalContext;

void MyInitializeFunction() 
{
    HANDLE hActCtx;
    ACTCTX actctx = {sizeof(actctx)};

    s_OutboundContext.Set(NULL);

    actctx.lpSource = TEXT("internalcontext.manifest");
    hActCtx = CreateActCtx(&actctx);
    s_InternalActCtx.Set(hActCtx);
    ReleaseActCtx(hActCtx);

    actctx.lpSource = TEXT("externals.manifest");
    hActCtx = CreateActCtx(&actctx);
    s_ExternalContext.Set(hActCtx);
    ReleaseActCtx(hActCtx);
}

void foo() 
{
    // Some code that makes a few calls
    {
        CActCtxActivator CallUnknown(s_OutboundContext);
        pfnUnknownImplementor(...);
    }
    {
        CActCtxActivator CallDependency(s_ExternalContext);
        KnownExternalDependencyPtr->Call();
    }
}

void WINAPI MyEntrypoint() 
{
    CActCtxActivator ContextFirewall(s_InternalContext);
    // Do some work here
    foo();
    // Some more work here
}
```

 

 
