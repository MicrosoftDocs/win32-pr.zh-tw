---
title: 代理共用
description: 如果 DLL 伺服器具有相符的安全性識別，且共用相同的 AppID 值，就會共用代理。
ms.assetid: 88544be1-4716-47b6-9c08-2b5b2b178e1f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6f6a934f03d42113cf73df4f059ac108801d21ea
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103672483"
---
# <a name="surrogate-sharing"></a><span data-ttu-id="670af-103">代理共用</span><span class="sxs-lookup"><span data-stu-id="670af-103">Surrogate Sharing</span></span>

<span data-ttu-id="670af-104">如果 DLL 伺服器具有相符的安全性識別，且共用相同的 AppID 值，就會共用代理。</span><span class="sxs-lookup"><span data-stu-id="670af-104">DLL servers will share a surrogate if they have matching security identities and share the same AppID value.</span></span>

<span data-ttu-id="670af-105">預設會將 DLL 伺服器載入至自己的代理進程。</span><span class="sxs-lookup"><span data-stu-id="670af-105">DLL servers are loaded, by default, into their own surrogate process.</span></span> <span data-ttu-id="670af-106">若要將其他 DLL 伺服器載入至現有的代理，讓它支援一部以上的 DLL 伺服器，有兩個需求：</span><span class="sxs-lookup"><span data-stu-id="670af-106">To load other DLL servers into an existing surrogate so that it supports more than one DLL server, there are two requirements:</span></span>

-   <span data-ttu-id="670af-107">DLL 伺服器必須具有相同的 AppID 值。</span><span class="sxs-lookup"><span data-stu-id="670af-107">The DLL servers must have the same AppID value.</span></span>
-   <span data-ttu-id="670af-108">DLL 伺服器的安全性內容必須相同。</span><span class="sxs-lookup"><span data-stu-id="670af-108">The security context of the DLL servers must be the same.</span></span>

<span data-ttu-id="670af-109">如果要在不同的安全性身分識別下啟動兩個 DLL 伺服器，它們必須位於不同的代理中，不論其 Appid 是否相符。</span><span class="sxs-lookup"><span data-stu-id="670af-109">If two DLL servers are to be launched under different security identities, they must be in different surrogates, whether their AppIDs match.</span></span>

<span data-ttu-id="670af-110">以下是使用 Appid 管理代理共用的範例：</span><span class="sxs-lookup"><span data-stu-id="670af-110">Following is an example of administering surrogate sharing with AppIDs:</span></span>

``` syntax
    AppID
        {12345678-0000-0000-0000-abcdabcdabcd}
            @DllSurrogate    REG_SZ
    CLSID
        {12345678-0000-0000-0000-000000000001}
            @AppId    REG_SZ    {12345678-0000-0000-0000-abcdabcdabcd}
            InProcServer32
    @    REG_SZ    c:\myapp\comp1.dll
        {12345678-0000-0000-0000-000000000002}
            @AppId    REG_SZ    {12345678-0000-0000-0000-abcdabcdabcd}
            InProcServer32
    @    REG_SZ    c:\myapp\comp2.dll
 
```

<span data-ttu-id="670af-111">comp1.dll 和 comp2.dll 的 DLL 元件的兩個 Clsid 已設定為共用 AppID。</span><span class="sxs-lookup"><span data-stu-id="670af-111">The two CLSIDs for DLL components comp1.dll and comp2.dll have been configured to share an AppID.</span></span> <span data-ttu-id="670af-112">[AppID](appid-key.md)索引鍵會指定[DllSurrogate](dllsurrogate.md)值，以指定可在代理中載入 DLL 伺服器。</span><span class="sxs-lookup"><span data-stu-id="670af-112">The [AppID](appid-key.md) key specifies that the DLL server can be loaded in a surrogate by specifying the [DllSurrogate](dllsurrogate.md) value.</span></span> <span data-ttu-id="670af-113">在此範例中， **DllSurrogate** 值為空字串，表示應該使用 DLL 代理的預設系統執行。</span><span class="sxs-lookup"><span data-stu-id="670af-113">In this example, the **DllSurrogate** value is an empty string, indicating that the default system implementation of the DLL surrogate should be used.</span></span>

## <a name="related-topics"></a><span data-ttu-id="670af-114">相關主題</span><span class="sxs-lookup"><span data-stu-id="670af-114">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="670af-115">DLL 伺服器需求</span><span class="sxs-lookup"><span data-stu-id="670af-115">DLL Server Requirements</span></span>](dll-server-requirements.md)
</dt> <dt>

[<span data-ttu-id="670af-116">註冊 DLL 伺服器以進行代理程式啟用</span><span class="sxs-lookup"><span data-stu-id="670af-116">Registering the DLL Server for Surrogate Activation</span></span>](registering-the-dll-server-for-surrogate-activation.md)
</dt> </dl>

 

 




