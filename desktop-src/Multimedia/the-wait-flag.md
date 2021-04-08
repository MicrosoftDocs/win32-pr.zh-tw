---
title: 等候旗標
description: 等候旗標
ms.assetid: b971ccd4-0507-4f05-adb3-d4930496034d
keywords:
- MCI_WAIT 旗標
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e552650aca9cf104d2c87d7faddd0b6c85b5a6b8
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104022106"
---
# <a name="the-wait-flag"></a><span data-ttu-id="03155-104">等候旗標</span><span class="sxs-lookup"><span data-stu-id="03155-104">The Wait Flag</span></span>

<span data-ttu-id="03155-105">MCI 命令通常會立即傳回給使用者，即使需要幾分鐘的時間才能完成命令所起始的動作。</span><span class="sxs-lookup"><span data-stu-id="03155-105">MCI commands usually return to the user immediately, even if it takes several minutes to complete the action initiated by the command.</span></span> <span data-ttu-id="03155-106">您可以使用「等待」 (MCI \_ wait) 旗標，指示裝置等待直到要求的動作完成後，再將控制權傳回給應用程式。</span><span class="sxs-lookup"><span data-stu-id="03155-106">You can use the "wait" (MCI\_WAIT) flag to direct the device to wait until the requested action is completed before returning control to the application.</span></span>

<span data-ttu-id="03155-107">例如，下列 [**play**](play.md) 命令不會將控制權傳回給應用程式，直到播放完成為止：</span><span class="sxs-lookup"><span data-stu-id="03155-107">For example, the following [**play**](play.md) command will not return control to the application until the playback completes:</span></span>


```C++
mciSendString("play mydevice from 0 to 100 wait", 
    lpszReturnString, lstrlen(lpszReturnString), NULL);
```



> [!Note]  
> <span data-ttu-id="03155-108">使用者可以藉由按下 break 鍵來取消等候作業。</span><span class="sxs-lookup"><span data-stu-id="03155-108">The user can cancel a wait operation by pressing a break key.</span></span> <span data-ttu-id="03155-109">依預設，此索引鍵是 CTRL + BREAK。</span><span class="sxs-lookup"><span data-stu-id="03155-109">By default, this key is CTRL+BREAK.</span></span> <span data-ttu-id="03155-110">應用程式可以使用 [**break**](break.md) ([**MCI \_ break**](mci-break.md)) 命令來重新定義此機碼。</span><span class="sxs-lookup"><span data-stu-id="03155-110">Applications can redefine this key by using the [**break**](break.md) ([**MCI\_BREAK**](mci-break.md)) command.</span></span> <span data-ttu-id="03155-111"> (**mci \_ break** 會使用 [**MCI \_ break \_ PARMS**](mci-break-parms.md) 結構。 ) 等候作業取消時，MCI 會嘗試將控制權傳回給應用程式，而不會中斷與「等候」旗標相關聯的命令。</span><span class="sxs-lookup"><span data-stu-id="03155-111">(**MCI\_BREAK** uses the [**MCI\_BREAK\_PARMS**](mci-break-parms.md) structure.) When a wait operation is canceled, MCI attempts to return control to the application without interrupting the command associated with the "wait" flag.</span></span>

 

 

 




