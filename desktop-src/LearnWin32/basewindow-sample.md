---
title: BaseWindow 範例
description: 這個範例應用程式說明如何在 WM NCCREATE 訊息中傳遞應用程式狀態資料 \_ 。
ms.assetid: 5be8a5ef-8a63-43e7-b2a5-a4fff63c7ce3
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 304a29b3f194e9ec8f530d1a5bb360d2d98add51
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2020
ms.locfileid: "104092733"
---
# <a name="basewindow-sample"></a><span data-ttu-id="93e52-103">BaseWindow 範例</span><span class="sxs-lookup"><span data-stu-id="93e52-103">BaseWindow Sample</span></span>

<span data-ttu-id="93e52-104">這個範例應用程式說明如何在 [**WM \_ NCCREATE**](/windows/desktop/winmsg/wm-nccreate) 訊息中傳遞應用程式狀態資料。</span><span class="sxs-lookup"><span data-stu-id="93e52-104">This sample application shows how to pass application state data in the [**WM\_NCCREATE**](/windows/desktop/winmsg/wm-nccreate) message.</span></span>

## <a name="description"></a><span data-ttu-id="93e52-105">Description</span><span class="sxs-lookup"><span data-stu-id="93e52-105">Description</span></span>

<span data-ttu-id="93e52-106">BaseWindow 範例應用程式是 [Windows Hello 世界範例](windows-hello-world-sample.md)的變化。</span><span class="sxs-lookup"><span data-stu-id="93e52-106">The BaseWindow sample application is a variation on the [Windows Hello World Sample](windows-hello-world-sample.md).</span></span> <span data-ttu-id="93e52-107">它會使用 [**WM \_ NCCREATE**](/windows/desktop/winmsg/wm-nccreate) 訊息將應用程式資料傳遞給視窗程式。</span><span class="sxs-lookup"><span data-stu-id="93e52-107">It uses the [**WM\_NCCREATE**](/windows/desktop/winmsg/wm-nccreate) message to pass application data to the window procedure.</span></span> <span data-ttu-id="93e52-108">此範例會在 [管理應用程式狀態](managing-application-state-.md)的主題中討論。</span><span class="sxs-lookup"><span data-stu-id="93e52-108">This sample is discussed in the topic [Managing Application State](managing-application-state-.md).</span></span>

## <a name="downloading-the-sample"></a><span data-ttu-id="93e52-109">下載範例</span><span class="sxs-lookup"><span data-stu-id="93e52-109">Downloading the Sample</span></span>

<span data-ttu-id="93e52-110">此範例可在 [這裡](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/begin/LearnWin32/BaseWindow)取得。</span><span class="sxs-lookup"><span data-stu-id="93e52-110">This sample is available [here](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/begin/LearnWin32/BaseWindow).</span></span>

## <a name="related-topics"></a><span data-ttu-id="93e52-111">相關主題</span><span class="sxs-lookup"><span data-stu-id="93e52-111">Related topics</span></span>

* [<span data-ttu-id="93e52-112">學習如何撰寫 Windows 程式：範例程式碼</span><span class="sxs-lookup"><span data-stu-id="93e52-112">Learn to Program for Windows: Sample Code</span></span>](learn-to-program-for-windows--sample-code.md)
* [<span data-ttu-id="93e52-113">管理應用程式狀態</span><span class="sxs-lookup"><span data-stu-id="93e52-113">Managing Application State</span></span>](managing-application-state-.md)
* [<span data-ttu-id="93e52-114">模組1。您的第一個 Windows 程式</span><span class="sxs-lookup"><span data-stu-id="93e52-114">Module 1. Your First Windows Program</span></span>](your-first-windows-program.md)