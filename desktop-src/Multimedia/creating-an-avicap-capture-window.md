---
title: 建立 AVICap Capture 視窗
description: 建立 AVICap Capture 視窗
ms.assetid: a1418e98-f16d-401a-94a7-64fb272a39e2
keywords:
- capCreateCaptureWindow 函式
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 084d035d44b8d0b46df31afa5c3235e59286121c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104300520"
---
# <a name="creating-an-avicap-capture-window"></a><span data-ttu-id="ce7ee-104">建立 AVICap Capture 視窗</span><span class="sxs-lookup"><span data-stu-id="ce7ee-104">Creating an AVICap Capture Window</span></span>

<span data-ttu-id="ce7ee-105">您可以使用 [**capCreateCaptureWindow**](/windows/desktop/api/Vfw/nf-vfw-capcreatecapturewindowa) 函數來建立 AVICap 視窗類別的捕獲視窗。</span><span class="sxs-lookup"><span data-stu-id="ce7ee-105">You can create a capture window of the AVICap window class by using the [**capCreateCaptureWindow**](/windows/desktop/api/Vfw/nf-vfw-capcreatecapturewindowa) function.</span></span> <span data-ttu-id="ce7ee-106">此函式會傳回一個視窗控制碼，此控制碼會識別「捕獲」視窗，並由應用程式用來將後續訊息傳送至視窗。</span><span class="sxs-lookup"><span data-stu-id="ce7ee-106">This function returns a window handle that identifies the capture window and is used by an application to send subsequent messages to the window.</span></span>

<span data-ttu-id="ce7ee-107">您可以在應用程式中建立一或多個捕獲視窗，並將每個捕獲視窗連接至不同的捕獲裝置。</span><span class="sxs-lookup"><span data-stu-id="ce7ee-107">You can create one or more capture windows in an application and connect each capture window to a different capture device.</span></span>

 

 




