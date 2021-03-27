---
description: 當使用者按一下 [視窗] 功能表中的 [最小化]，或應用程式呼叫 ShowWindow 函式並指定值（例如 SW 最小化）時，系統會將應用程式的主視窗減少 (重迭樣式) 至最小化的視窗 \_ 。
ms.assetid: a52dba49-e4ec-45e2-a00f-211a58e28773
title: 最小化視窗
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c792a90dba2526b6d09fabf8281fc74ebfe96667
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103691867"
---
# <a name="minimized-windows"></a><span data-ttu-id="c96fc-103">最小化視窗</span><span class="sxs-lookup"><span data-stu-id="c96fc-103">Minimized Windows</span></span>

<span data-ttu-id="c96fc-104">當使用者按一下 [視窗] 功能表中的 [最小化]，或應用程式呼叫 [**ShowWindow**](/windows/win32/api/winuser/nf-winuser-showwindow) 函式並指定值（例如 SW \_ 最小化）時，系統會將應用程式的主視窗減少 (重迭樣式) 至最小化的視窗。</span><span class="sxs-lookup"><span data-stu-id="c96fc-104">The system reduces an application's main window (overlapping style) to a minimized window when the user clicks Minimize from the window menu or the application calls the [**ShowWindow**](/windows/win32/api/winuser/nf-winuser-showwindow) function and specifies a value such as SW\_MINIMIZE.</span></span> <span data-ttu-id="c96fc-105">將視窗最小化可減少應用程式在更新主視窗時必須執行的工作量，以加速系統效能。</span><span class="sxs-lookup"><span data-stu-id="c96fc-105">Minimizing a window speeds up system performance by reducing the amount of work an application must do when updating its main window.</span></span>

<span data-ttu-id="c96fc-106">若為一般應用程式，系統會在視窗最小化時，繪製稱為類別圖示的圖示，並以視窗的名稱標記圖示。</span><span class="sxs-lookup"><span data-stu-id="c96fc-106">For a typical application, the system draws an icon, called the class icon, when the window is minimized, labeling the icon with the name of the window.</span></span> <span data-ttu-id="c96fc-107">類別圖示（代表應用程式的靜態影像）是由應用程式在註冊視窗類別時所指定。</span><span class="sxs-lookup"><span data-stu-id="c96fc-107">The class icon, a static image that represents the application, is specified by the application when it registers the window class.</span></span> <span data-ttu-id="c96fc-108">應用程式會在呼叫 [**RegisterClass**](/windows/win32/api/winuser/nf-winuser-registerclassa)之前，將控制碼指派給 [**WNDCLASS**](/windows/win32/api/winuser/ns-winuser-wndclassa)的 **hIcon** 成員。</span><span class="sxs-lookup"><span data-stu-id="c96fc-108">The application assigns a handle to the class icon to the **hIcon** member of [**WNDCLASS**](/windows/win32/api/winuser/ns-winuser-wndclassa) before calling [**RegisterClass**](/windows/win32/api/winuser/nf-winuser-registerclassa).</span></span> <span data-ttu-id="c96fc-109">應用程式可以使用 [**LoadIcon**](/windows/win32/api/winuser/nf-winuser-loadicona) 函式來取出圖示控制碼。</span><span class="sxs-lookup"><span data-stu-id="c96fc-109">The application can use the [**LoadIcon**](/windows/win32/api/winuser/nf-winuser-loadicona) function to retrieve the icon handle.</span></span>

 

 
