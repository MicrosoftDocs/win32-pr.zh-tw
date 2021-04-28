---
title: 什麼是視窗
description: 什麼是視窗？
ms.assetid: eef5e139-91f9-4d8b-9153-e178d7416d7e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8494738e3985f78930549f313cb2868b79b34f3b
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/28/2021
ms.locfileid: "108103846"
---
# <a name="what-is-a-window"></a><span data-ttu-id="0edcd-103">什麼是視窗？</span><span class="sxs-lookup"><span data-stu-id="0edcd-103">What Is a Window?</span></span>

## <a name="what-is-a-window"></a><span data-ttu-id="0edcd-104">什麼是視窗？</span><span class="sxs-lookup"><span data-stu-id="0edcd-104">What Is a Window?</span></span>

<span data-ttu-id="0edcd-105">很明顯地，windows 是 Windows 的核心。</span><span class="sxs-lookup"><span data-stu-id="0edcd-105">Obviously, windows are central to Windows.</span></span> <span data-ttu-id="0edcd-106">他們很重要的是，它們會在作業系統之後命名。</span><span class="sxs-lookup"><span data-stu-id="0edcd-106">They are so important that they named the operating system after them.</span></span> <span data-ttu-id="0edcd-107">但什麼是視窗？</span><span class="sxs-lookup"><span data-stu-id="0edcd-107">But what is a window?</span></span> <span data-ttu-id="0edcd-108">當您想像一下某個視窗時，您可能會想一下像這樣的內容：</span><span class="sxs-lookup"><span data-stu-id="0edcd-108">When you think of a window, you probably think of something like this:</span></span>

![應用程式視窗的螢幕擷取畫面](images/window01.png)

<span data-ttu-id="0edcd-110">這種視窗稱為 *應用程式視窗* 或 *主視窗*。</span><span class="sxs-lookup"><span data-stu-id="0edcd-110">This type of window is called an *application window* or *main window*.</span></span> <span data-ttu-id="0edcd-111">它通常會有一個具有標題列的框架、 **最小化** 和 **最大化** 按鈕，以及其他標準 UI 元素。</span><span class="sxs-lookup"><span data-stu-id="0edcd-111">It typically has a frame with a title bar, **Minimize** and **Maximize** buttons, and other standard UI elements.</span></span> <span data-ttu-id="0edcd-112">框架稱為視窗的 *非工作區* ，因此呼叫的原因是作業系統會管理視窗的該部分。</span><span class="sxs-lookup"><span data-stu-id="0edcd-112">The frame is called the *non-client area* of the window, so called because the operating system manages that portion of the window.</span></span> <span data-ttu-id="0edcd-113">框架內的區域是工作 *區*。</span><span class="sxs-lookup"><span data-stu-id="0edcd-113">The area within the frame is the *client area*.</span></span> <span data-ttu-id="0edcd-114">這是您的程式所管理視窗的一部分。</span><span class="sxs-lookup"><span data-stu-id="0edcd-114">This is the part of the window that your program manages.</span></span>

<span data-ttu-id="0edcd-115">以下是另一種視窗：</span><span class="sxs-lookup"><span data-stu-id="0edcd-115">Here is another type of window:</span></span>

![控制項視窗的螢幕擷取畫面](images/window02.png)

<span data-ttu-id="0edcd-117">如果您不熟悉 Windows 程式設計，您可能會驚訝 UI 控制項（例如按鈕和編輯方塊）本身就是 windows。</span><span class="sxs-lookup"><span data-stu-id="0edcd-117">If you are new to Windows programming, it may surprise you that UI controls, such as buttons and edit boxes, are themselves windows.</span></span> <span data-ttu-id="0edcd-118">UI 控制項與應用程式視窗之間的主要差異在於控制項本身不存在。</span><span class="sxs-lookup"><span data-stu-id="0edcd-118">The major difference between a UI control and an application window is that a control does not exist by itself.</span></span> <span data-ttu-id="0edcd-119">相反地，控制項相對於應用程式視窗的位置。</span><span class="sxs-lookup"><span data-stu-id="0edcd-119">Instead, the control is positioned relative to the application window.</span></span> <span data-ttu-id="0edcd-120">當您拖曳應用程式視窗時，控制項會依照您的預期來移動它。</span><span class="sxs-lookup"><span data-stu-id="0edcd-120">When you drag the application window, the control moves with it, as you would expect.</span></span> <span data-ttu-id="0edcd-121">此外，控制項和應用程式視窗也可以彼此通訊。</span><span class="sxs-lookup"><span data-stu-id="0edcd-121">Also, the control and the application window can communicate with each other.</span></span> <span data-ttu-id="0edcd-122"> (例如，應用程式視窗會從按鈕接收按一下通知。 ) </span><span class="sxs-lookup"><span data-stu-id="0edcd-122">(For example, the application window receives click notifications from a button.)</span></span>

<span data-ttu-id="0edcd-123">因此，當您考慮到 *視窗* 時，請不要只考慮 *應用程式視窗*。</span><span class="sxs-lookup"><span data-stu-id="0edcd-123">Therefore, when you think *window*, do not simply think *application window*.</span></span> <span data-ttu-id="0edcd-124">相反地，請將視窗視為程式設計結構，如下所示：</span><span class="sxs-lookup"><span data-stu-id="0edcd-124">Instead, think of a window as a programming construct that:</span></span>

-   <span data-ttu-id="0edcd-125">佔用畫面的特定部分。</span><span class="sxs-lookup"><span data-stu-id="0edcd-125">Occupies a certain portion of the screen.</span></span>
-   <span data-ttu-id="0edcd-126">在指定的時刻，可能或可能不會顯示。</span><span class="sxs-lookup"><span data-stu-id="0edcd-126">May or may not be visible at a given moment.</span></span>
-   <span data-ttu-id="0edcd-127">知道如何自行繪製。</span><span class="sxs-lookup"><span data-stu-id="0edcd-127">Knows how to draw itself.</span></span>
-   <span data-ttu-id="0edcd-128">回應來自使用者或作業系統的事件。</span><span class="sxs-lookup"><span data-stu-id="0edcd-128">Responds to events from the user or the operating system.</span></span>

## <a name="parent-windows-and-owner-windows"></a><span data-ttu-id="0edcd-129">父視窗和擁有者視窗</span><span class="sxs-lookup"><span data-stu-id="0edcd-129">Parent Windows and Owner Windows</span></span>

<span data-ttu-id="0edcd-130">在 UI 控制項的案例中，控制項視窗稱為應用程式視窗的 *子* 系。</span><span class="sxs-lookup"><span data-stu-id="0edcd-130">In the case of a UI control, the control window is said to be the *child* of the application window.</span></span> <span data-ttu-id="0edcd-131">應用程式視窗是控制項視窗的 *父系* 。</span><span class="sxs-lookup"><span data-stu-id="0edcd-131">The application window is the *parent* of the control window.</span></span> <span data-ttu-id="0edcd-132">父視窗提供用來放置子視窗的座標系統。</span><span class="sxs-lookup"><span data-stu-id="0edcd-132">The parent window provides the coordinate system used for positioning a child window.</span></span> <span data-ttu-id="0edcd-133">擁有父視窗會影響視窗外觀的各個層面;例如，會裁剪子視窗，讓子視窗的任何部分不能出現在其父視窗的框線之外。</span><span class="sxs-lookup"><span data-stu-id="0edcd-133">Having a parent window affects aspects of a window's appearance; for example, a child window is clipped so that no part of the child window can appear outside the borders of its parent window.</span></span>

<span data-ttu-id="0edcd-134">另一個關聯性是應用程式視窗和強制回應對話方塊視窗之間的關聯性。</span><span class="sxs-lookup"><span data-stu-id="0edcd-134">Another relationship is the relation between an application window and a modal dialog window.</span></span> <span data-ttu-id="0edcd-135">當應用程式顯示模式對話方塊時，應用程式視窗會是擁有 *者視窗，* 而對話方塊則是 *擁有* 的視窗。</span><span class="sxs-lookup"><span data-stu-id="0edcd-135">When an application displays a modal dialog, the application window is the *owner* window, and the dialog is an *owned* window.</span></span> <span data-ttu-id="0edcd-136">擁有的視窗一律會出現在其擁有者視窗前方。</span><span class="sxs-lookup"><span data-stu-id="0edcd-136">An owned window always appears in front of its owner window.</span></span> <span data-ttu-id="0edcd-137">當擁有者最小化時，它會被隱藏，而且會與擁有者同時終結。</span><span class="sxs-lookup"><span data-stu-id="0edcd-137">It is hidden when the owner is minimized, and is destroyed at the same time as the owner.</span></span>

<span data-ttu-id="0edcd-138">下圖顯示的應用程式會顯示具有兩個按鈕的對話方塊：</span><span class="sxs-lookup"><span data-stu-id="0edcd-138">The following image shows an application that displays a dialog box with two buttons:</span></span>

![具有對話方塊的應用程式螢幕擷取畫面](images/window03.png)

<span data-ttu-id="0edcd-140">應用程式視窗擁有對話方塊視窗，而對話方塊視窗則是這兩個按鈕視窗的父視窗。</span><span class="sxs-lookup"><span data-stu-id="0edcd-140">The application window owns the dialog window, and the dialog window is the parent of both button windows.</span></span> <span data-ttu-id="0edcd-141">下圖顯示這些關係：</span><span class="sxs-lookup"><span data-stu-id="0edcd-141">The following diagram shows these relations:</span></span>

![顯示父/子系和擁有者/擁有關系的圖例](images/window04.png)

## <a name="window-handles"></a><span data-ttu-id="0edcd-143">視窗控制碼</span><span class="sxs-lookup"><span data-stu-id="0edcd-143">Window Handles</span></span>

<span data-ttu-id="0edcd-144">Windows 是物件—它們都有程式碼和資料，但它們不是 c + + 類別。</span><span class="sxs-lookup"><span data-stu-id="0edcd-144">Windows are objects—they have both code and data—but they are not C++ classes.</span></span> <span data-ttu-id="0edcd-145">相反地，程式會使用稱為 *控制碼* 的值來參考視窗。</span><span class="sxs-lookup"><span data-stu-id="0edcd-145">Instead, a program references a window by using a value called a *handle*.</span></span> <span data-ttu-id="0edcd-146">控制碼是不透明的型別。</span><span class="sxs-lookup"><span data-stu-id="0edcd-146">A handle is an opaque type.</span></span> <span data-ttu-id="0edcd-147">基本上，它只是作業系統用來識別物件的數位。</span><span class="sxs-lookup"><span data-stu-id="0edcd-147">Essentially, it is just a number that the operating system uses to identify an object.</span></span> <span data-ttu-id="0edcd-148">您可以將視窗畫為具有所有已建立視窗的大型表格。</span><span class="sxs-lookup"><span data-stu-id="0edcd-148">You can picture Windows as having a big table of all the windows that have been created.</span></span> <span data-ttu-id="0edcd-149">它會使用此資料表，依據其控點來查閱視窗。</span><span class="sxs-lookup"><span data-stu-id="0edcd-149">It uses this table to look up windows by their handles.</span></span> <span data-ttu-id="0edcd-150"> (它在內部的運作方式並不重要。 ) 視窗控制碼的資料型別是 **HWND**，通常是「aitch-風」。</span><span class="sxs-lookup"><span data-stu-id="0edcd-150">(Whether that's exactly how it works internally is not important.) The data type for window handles is **HWND**, which is usually pronounced "aitch-wind."</span></span> <span data-ttu-id="0edcd-151">建立 windows： [**CreateWindow**](/windows/desktop/DirectShow/cbasewindow-docreatewindow) 和 [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa)的函式會傳回視窗控制碼。</span><span class="sxs-lookup"><span data-stu-id="0edcd-151">Window handles are returned by the functions that create windows: [**CreateWindow**](/windows/desktop/DirectShow/cbasewindow-docreatewindow) and [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa).</span></span>

<span data-ttu-id="0edcd-152">若要在視窗上執行作業，您通常會呼叫一些接受 **HWND** 值作為參數的函式。</span><span class="sxs-lookup"><span data-stu-id="0edcd-152">To perform an operation on a window, you will typically call some function that takes an **HWND** value as a parameter.</span></span> <span data-ttu-id="0edcd-153">例如，若要在螢幕上重新調整視窗的位置，請呼叫 [**MoveWindow**](/windows/desktop/api/winuser/nf-winuser-movewindow) 函式：</span><span class="sxs-lookup"><span data-stu-id="0edcd-153">For example, to reposition a window on the screen, call the [**MoveWindow**](/windows/desktop/api/winuser/nf-winuser-movewindow) function:</span></span>


```C++
BOOL MoveWindow(HWND hWnd, int X, int Y, int nWidth, int nHeight, BOOL bRepaint);
```



<span data-ttu-id="0edcd-154">第一個參數是您想要移動的視窗控制碼。</span><span class="sxs-lookup"><span data-stu-id="0edcd-154">The first parameter is the handle to the window that you want to move.</span></span> <span data-ttu-id="0edcd-155">其他參數則指定視窗的新位置，以及是否應該重新繪製視窗。</span><span class="sxs-lookup"><span data-stu-id="0edcd-155">The other parameters specify the new location of the window and whether the window should be redrawn.</span></span>

<span data-ttu-id="0edcd-156">請記住，控制碼不是指標。</span><span class="sxs-lookup"><span data-stu-id="0edcd-156">Keep in mind that handles are not pointers.</span></span> <span data-ttu-id="0edcd-157">如果 *hwnd* 是包含控制碼的變數，嘗試透過寫入來將控制碼取值 `*hwnd` 是錯誤。</span><span class="sxs-lookup"><span data-stu-id="0edcd-157">If *hwnd* is a variable that contains a handle, attempting to dereference the handle by writing `*hwnd` is an error.</span></span>

## <a name="screen-and-window-coordinates"></a><span data-ttu-id="0edcd-158">螢幕和視窗座標</span><span class="sxs-lookup"><span data-stu-id="0edcd-158">Screen and Window Coordinates</span></span>

<span data-ttu-id="0edcd-159">座標是以與裝置無關的圖元來測量。</span><span class="sxs-lookup"><span data-stu-id="0edcd-159">Coordinates are measured in device-independent pixels.</span></span> <span data-ttu-id="0edcd-160">當我們討論圖形時，我們將更瞭解與裝置無關的 *圖元* 相關的 *裝置* 部分。</span><span class="sxs-lookup"><span data-stu-id="0edcd-160">We'll have more to say about the *device independent* part of *device-independent pixels* when we discuss graphics.</span></span>

<span data-ttu-id="0edcd-161">視您的工作而定，您可能會測量相對於畫面的座標（相對於視窗 (，包括畫面格) 或相對於視窗的工作區）。</span><span class="sxs-lookup"><span data-stu-id="0edcd-161">Depending on your task, you might measure coordinates relative to the screen, relative to a window (including the frame), or relative to the client area of a window.</span></span> <span data-ttu-id="0edcd-162">例如，您會使用螢幕座標將視窗放置在螢幕上，但您會在使用用戶端座標的視窗內繪製。</span><span class="sxs-lookup"><span data-stu-id="0edcd-162">For example, you would position a window on the screen using screen coordinates, but you would draw inside a window using client coordinates.</span></span> <span data-ttu-id="0edcd-163">在每個案例中，原點 (0，0) 一律是區域的左上角。</span><span class="sxs-lookup"><span data-stu-id="0edcd-163">In each case, the origin (0, 0) is always the top-left corner of the region.</span></span>

![顯示幕幕、視窗和工作區座標的圖例](images/coordinates01.png)

## <a name="next"></a><span data-ttu-id="0edcd-165">下一個</span><span class="sxs-lookup"><span data-stu-id="0edcd-165">Next</span></span>

[<span data-ttu-id="0edcd-166">WinMain：應用程式進入點</span><span class="sxs-lookup"><span data-stu-id="0edcd-166">WinMain: The Application Entry Point</span></span>](winmain--the-application-entry-point.md)

 

 
