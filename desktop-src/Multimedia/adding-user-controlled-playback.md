---
title: 新增 User-Controlled 播放
description: 新增 User-Controlled 播放
ms.assetid: c865bbc1-f78a-4d88-ab60-fba76818d175
keywords:
- MCIWndCreate 函式
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 198ae0bb72a5da82042b5448d2a9213358f0174d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "106999574"
---
# <a name="adding-user-controlled-playback"></a><span data-ttu-id="828a6-104">新增 User-Controlled 播放</span><span class="sxs-lookup"><span data-stu-id="828a6-104">Adding User-Controlled Playback</span></span>

<span data-ttu-id="828a6-105">您可以藉由呼叫 [**MCIWndCreate**](/windows/desktop/api/Vfw/nf-vfw-mciwndcreatea) 函式，將使用者控制的播放新增至現有的應用程式，如下所示：</span><span class="sxs-lookup"><span data-stu-id="828a6-105">You can add user-controlled playback to an existing application by calling the [**MCIWndCreate**](/windows/desktop/api/Vfw/nf-vfw-mciwndcreatea) function as follows:</span></span>


```C++
MCIWndCreate(hwndParent, hInstModule, NULL, "filename.typ"); 
```



<span data-ttu-id="828a6-106">[**MCIWndCreate**](/windows/desktop/api/Vfw/nf-vfw-mciwndcreatea)參數會識別父視窗的控制碼，以及與 MCIWnd 視窗相關聯的模組實例。</span><span class="sxs-lookup"><span data-stu-id="828a6-106">The [**MCIWndCreate**](/windows/desktop/api/Vfw/nf-vfw-mciwndcreatea) parameters identify handles to the parent window and to the module instance associated with the MCIWnd window.</span></span> <span data-ttu-id="828a6-107">它們也會指定視窗樣式和檔案名 (或裝置名稱，) 要與 MCIWnd 視窗相關聯。</span><span class="sxs-lookup"><span data-stu-id="828a6-107">They also specify window styles and the filename (or device name) to associate with the MCIWnd window.</span></span>

<span data-ttu-id="828a6-108">**MCIWndCreate** 會自動執行下列步驟，針對其他視窗類別，您可以自行在程式碼中執行：</span><span class="sxs-lookup"><span data-stu-id="828a6-108">**MCIWndCreate** automatically performs the following steps that, for other window classes, you would implement in your code yourself:</span></span>

1.  <span data-ttu-id="828a6-109">註冊 MCIWnd 視窗類別。</span><span class="sxs-lookup"><span data-stu-id="828a6-109">Register the MCIWnd window class.</span></span>
2.  <span data-ttu-id="828a6-110">建立 MCIWnd 視窗。</span><span class="sxs-lookup"><span data-stu-id="828a6-110">Create the MCIWnd window.</span></span>
3.  <span data-ttu-id="828a6-111">載入指定的內容。</span><span class="sxs-lookup"><span data-stu-id="828a6-111">Load the specified content.</span></span>
4.  <span data-ttu-id="828a6-112">在內容的開頭建立目前的播放位置。</span><span class="sxs-lookup"><span data-stu-id="828a6-112">Establish the current playback position at the beginning of the content.</span></span>
5.  <span data-ttu-id="828a6-113">顯示裝置控制項。</span><span class="sxs-lookup"><span data-stu-id="828a6-113">Display the device control.</span></span>
6.  <span data-ttu-id="828a6-114">如有需要，顯示視窗的播放區域。</span><span class="sxs-lookup"><span data-stu-id="828a6-114">Display the playback area of the window, if needed.</span></span>

 

 




