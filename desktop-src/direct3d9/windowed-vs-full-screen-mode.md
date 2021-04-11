---
description: Direct3D 應用程式可在兩種模式中執行：全螢幕或視窗化。
ms.assetid: 6ec30c6e-93d1-4b77-9638-86308bbf8f3c
title: " (Direct3D 9) 的視窗型 vs Full-Screen 模式"
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bf51c641446d3f54ceb37c9cc1ac629604f68400
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "104108733"
---
# <a name="windowed-vs-full-screen-mode-direct3d-9"></a><span data-ttu-id="e5ed2-103"> (Direct3D 9) 的視窗型 vs Full-Screen 模式</span><span class="sxs-lookup"><span data-stu-id="e5ed2-103">Windowed vs Full-Screen Mode (Direct3D 9)</span></span>

<span data-ttu-id="e5ed2-104">Direct3D 應用程式可在兩種模式中執行：全螢幕或視窗化。</span><span class="sxs-lookup"><span data-stu-id="e5ed2-104">Direct3D applications can run in either of two modes: full-screen or windowed.</span></span>

<span data-ttu-id="e5ed2-105">全螢幕模式表示應用程式執行所在的視窗涵蓋整個桌面，隱藏所有正在執行的應用程式， (包括您的開發環境) 。</span><span class="sxs-lookup"><span data-stu-id="e5ed2-105">Full-screen mode means the window that the application runs in covers the entire desktop, hiding all running applications (including your development environment).</span></span> <span data-ttu-id="e5ed2-106">通常遊戲預設為全螢幕模式，隱藏執行的所有應用程式，為使用者提供身歷其境的遊戲體驗。</span><span class="sxs-lookup"><span data-stu-id="e5ed2-106">Games typically default to full-screen mode to fully immerse the user in the game by hiding all running applications.</span></span> <span data-ttu-id="e5ed2-107">在視窗模式中執行的應用程式，會與所有正在執行的應用程式共用桌面。</span><span class="sxs-lookup"><span data-stu-id="e5ed2-107">An application running in windowed-mode shares the desktop with all running applications.</span></span> <span data-ttu-id="e5ed2-108">全螢幕模式和視窗模式之間的程式碼差異很小。</span><span class="sxs-lookup"><span data-stu-id="e5ed2-108">Code differences between full-screen mode and windowed mode are very small.</span></span>

<span data-ttu-id="e5ed2-109">由於以全螢幕模式執行的應用程式會接管螢幕，偵錯應用程式需要其他監視器或使用遠端的偵錯工具。</span><span class="sxs-lookup"><span data-stu-id="e5ed2-109">Because an application running in full-screen mode takes over the screen, debugging the application requires either a separate monitor or the use of a remote debugger.</span></span> <span data-ttu-id="e5ed2-110">使用 [DirectX 主控台工具](https://msdn.microsoft.com/library/Ee416791(v=VS.85).aspx) 來啟用多重監視器的調試。</span><span class="sxs-lookup"><span data-stu-id="e5ed2-110">Use the [DirectX Control Panel Tool](https://msdn.microsoft.com/library/Ee416791(v=VS.85).aspx) to enable multiple-monitor debugging.</span></span> <span data-ttu-id="e5ed2-111">視窗模式應用程式的其中一個優點是，您可以在偵錯工具中逐步執行程式碼，不需要多個監視器或遠端偵錯工具。</span><span class="sxs-lookup"><span data-stu-id="e5ed2-111">One advantage of a windowed-mode application is that you can step through the code in a debugger without multiple monitors or a remote debugger.</span></span>

## <a name="related-topics"></a><span data-ttu-id="e5ed2-112">相關主題</span><span class="sxs-lookup"><span data-stu-id="e5ed2-112">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e5ed2-113">Direct3D 裝置</span><span class="sxs-lookup"><span data-stu-id="e5ed2-113">Direct3D Devices</span></span>](direct3d-devices.md)
</dt> </dl>

 

 



