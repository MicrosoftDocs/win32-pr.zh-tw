---
title: 與 MCI 裝置通訊
description: 與 MCI 裝置通訊
ms.assetid: 2408f8e4-d040-40f5-a880-1ecb8025656c
keywords:
- MCIWndSendString 宏
- mciSendString 函式
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8f7f5458cff0ef4c5c5f84e565fae06ade8796c4
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2020
ms.locfileid: "106969511"
---
# <a name="communicating-with-mci-devices"></a><span data-ttu-id="97f06-105">與 MCI 裝置通訊</span><span class="sxs-lookup"><span data-stu-id="97f06-105">Communicating with MCI Devices</span></span>

<span data-ttu-id="97f06-106">每個 MCI 裝置的驅動程式都會維護其目前設定和功能的清單，讓它可以在查詢資訊時發出精確的回應。</span><span class="sxs-lookup"><span data-stu-id="97f06-106">The driver of each MCI device maintains a list of its current settings and capabilities, so it can issue an accurate response when it is queried for information.</span></span>

<span data-ttu-id="97f06-107">當您想要與 MCI 裝置通訊時，可以使用 MCIWnd 宏和函式。</span><span class="sxs-lookup"><span data-stu-id="97f06-107">When you want to communicate with an MCI device, you can use MCIWnd macros and functions.</span></span> <span data-ttu-id="97f06-108">許多最常見的 MCI 命令和查詢都會定義為宏。</span><span class="sxs-lookup"><span data-stu-id="97f06-108">Many of the most common MCI commands and queries are defined as macros.</span></span> <span data-ttu-id="97f06-109">但是，如果您要執行的工作無法作為函式或宏使用，您可以使用 [**MCIWndSendString**](/windows/desktop/api/Vfw/nf-vfw-mciwndsendstring) 宏或使用 MCI 命令的訊息表單或字串格式，將 mci 命令直接傳送到設備磁碟機。</span><span class="sxs-lookup"><span data-stu-id="97f06-109">However, if the task you want to perform is unavailable as a function or macro, you can send MCI commands directly to the device driver by using the [**MCIWndSendString**](/windows/desktop/api/Vfw/nf-vfw-mciwndsendstring) macro or by using either the message form or string form of the MCI commands.</span></span> <span data-ttu-id="97f06-110">使用 **MCIWndSendString** 宏相當於使用 [**mciSendString**](/previous-versions//dd757161(v=vs.85)) 函數，如下所示：</span><span class="sxs-lookup"><span data-stu-id="97f06-110">Using the **MCIWndSendString** macro is equivalent to using the [**mciSendString**](/previous-versions//dd757161(v=vs.85)) function as follows:</span></span>


```C++
mciSendString(sz, Null, 0, Null) 
```



<span data-ttu-id="97f06-111">[**MCIWndSendString**](/windows/desktop/api/Vfw/nf-vfw-mciwndsendstring)的參數只會包含視窗控制碼和命令的字串形式。</span><span class="sxs-lookup"><span data-stu-id="97f06-111">The parameters of [**MCIWndSendString**](/windows/desktop/api/Vfw/nf-vfw-mciwndsendstring) include only the window handle and the string form of the command.</span></span> <span data-ttu-id="97f06-112">若要取出字串命令所傳回的資訊，請使用 [**MCIWndReturnString**](/windows/desktop/api/Vfw/nf-vfw-mciwndreturnstring) 宏。</span><span class="sxs-lookup"><span data-stu-id="97f06-112">To retrieve the information returned by a string command, use the [**MCIWndReturnString**](/windows/desktop/api/Vfw/nf-vfw-mciwndreturnstring) macro.</span></span>

<span data-ttu-id="97f06-113">如需 MCI 的詳細資訊，請參閱 [mci](mci.md)。</span><span class="sxs-lookup"><span data-stu-id="97f06-113">For more information about MCI, see [MCI](mci.md).</span></span>

> [!Note]  
> <span data-ttu-id="97f06-114">當您使用 **MCIWndSendString** 時，必須從 MCI 命令排除裝置別名。</span><span class="sxs-lookup"><span data-stu-id="97f06-114">You must exclude the device alias from the MCI command when you use **MCIWndSendString**.</span></span> <span data-ttu-id="97f06-115">MCIWnd 程式庫會在將命令傳送至 MCI 裝置時，新增此別名。</span><span class="sxs-lookup"><span data-stu-id="97f06-115">The MCIWnd library adds this alias when it sends the command to the MCI device.</span></span>

 

 

 