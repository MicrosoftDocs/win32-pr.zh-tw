---
title: Yield 回呼函數
description: Yield 回呼函數
ms.assetid: 8c9b43ea-fdba-41a2-ba2d-1eaa4516e14f
keywords:
- AVICap 回呼函式，yield
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3666ea24a1d37402ffc13c09ca8ab95fcd19e1f7
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2020
ms.locfileid: "103681996"
---
# <a name="yield-callback-functions"></a><span data-ttu-id="a684a-104">Yield 回呼函數</span><span class="sxs-lookup"><span data-stu-id="a684a-104">Yield Callback Functions</span></span>

<span data-ttu-id="a684a-105">應用程式可以在串流處理期間使用 yield 回呼函數。</span><span class="sxs-lookup"><span data-stu-id="a684a-105">Applications can use yield callback functions during streaming capture.</span></span> <span data-ttu-id="a684a-106"> (yield 回呼函式通常是由呼叫 [PeekMessage](/windows/win32/api/winuser/nf-winuser-peekmessagea)、 [TranslateMessage](/windows/win32/api/winuser/nf-winuser-translatemessage)和 [DispatchMessage](/windows/win32/api/winuser/nf-winuser-dispatchmessage)的訊息迴圈所組成。 ) 捕捉視窗會針對每個已捕捉的影片框架呼叫 yield 回呼函式至少一次，但確切的速率取決於畫面播放速率和捕獲驅動程式和磁片的額外負荷。</span><span class="sxs-lookup"><span data-stu-id="a684a-106">(A yield callback function typically consists of a message loop that calls [PeekMessage](/windows/win32/api/winuser/nf-winuser-peekmessagea), [TranslateMessage](/windows/win32/api/winuser/nf-winuser-translatemessage), and [DispatchMessage](/windows/win32/api/winuser/nf-winuser-dispatchmessage).) The capture window calls the yield callback function at least once for every captured video frame, but the exact rate depends on the frame rate and the overhead of the capture driver and disk.</span></span>

 

 