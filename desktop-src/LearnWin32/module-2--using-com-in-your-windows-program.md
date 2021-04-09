---
title: 在您的 Windows 應用程式中使用 COM
description: 本系列的課程模組1顯示如何建立視窗並回應視窗訊息，例如 WM \_ 油漆和 wm \_ CLOSE。 模組2引進元件物件模型 (COM) 。
ms.assetid: 6e867618-4d02-4c17-b7ea-dc7290507689
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c8c03f16937846c4479a70e16141f1b50bde3efc
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2020
ms.locfileid: "103682270"
---
# <a name="module-2-using-com-in-your-windows-based-program"></a><span data-ttu-id="183b0-104">模組2。</span><span class="sxs-lookup"><span data-stu-id="183b0-104">Module 2.</span></span> <span data-ttu-id="183b0-105">在 Windows-Based 程式中使用 COM</span><span class="sxs-lookup"><span data-stu-id="183b0-105">Using COM in Your Windows-Based Program</span></span>

<span data-ttu-id="183b0-106">本系列的 [課程模組 1](your-first-windows-program.md)顯示如何建立視窗並回應視窗訊息，例如 [**Wm \_ 油漆**](/windows/desktop/gdi/wm-paint)和 [**wm \_ CLOSE**](/windows/desktop/winmsg/wm-close)。</span><span class="sxs-lookup"><span data-stu-id="183b0-106">[Module 1](your-first-windows-program.md) of this series showed how to create a window and respond to window messages such as [**WM\_PAINT**](/windows/desktop/gdi/wm-paint) and [**WM\_CLOSE**](/windows/desktop/winmsg/wm-close).</span></span> <span data-ttu-id="183b0-107">模組2引進元件物件模型 (COM) 。</span><span class="sxs-lookup"><span data-stu-id="183b0-107">Module 2 introduces the Component Object Model (COM).</span></span>

<span data-ttu-id="183b0-108">COM 是建立可重複使用的軟體元件的規格。</span><span class="sxs-lookup"><span data-stu-id="183b0-108">COM is a specification for creating reusable software components.</span></span> <span data-ttu-id="183b0-109">您將在新式 Windows 程式中使用的許多功能都依賴 COM，如下所示：</span><span class="sxs-lookup"><span data-stu-id="183b0-109">Many of the features that you will use in a modern Windows-based program rely on COM, such as the following:</span></span>

-   <span data-ttu-id="183b0-110">圖形 (Direct2D) </span><span class="sxs-lookup"><span data-stu-id="183b0-110">Graphics (Direct2D)</span></span>
-   <span data-ttu-id="183b0-111">文字 (DirectWrite) </span><span class="sxs-lookup"><span data-stu-id="183b0-111">Text (DirectWrite)</span></span>
-   <span data-ttu-id="183b0-112">Windows Shell</span><span class="sxs-lookup"><span data-stu-id="183b0-112">The Windows Shell</span></span>
-   <span data-ttu-id="183b0-113">功能區控制項</span><span class="sxs-lookup"><span data-stu-id="183b0-113">The Ribbon control</span></span>
-   <span data-ttu-id="183b0-114">UI 動畫</span><span class="sxs-lookup"><span data-stu-id="183b0-114">UI animation</span></span>

<span data-ttu-id="183b0-115"> (這份清單上的某些技術會使用 COM 的子集，因此不是 "pure" COM。 ) </span><span class="sxs-lookup"><span data-stu-id="183b0-115">(Some technologies on this list use a subset of COM and are therefore not "pure" COM.)</span></span>

<span data-ttu-id="183b0-116">COM 具有難以學習的信譽。</span><span class="sxs-lookup"><span data-stu-id="183b0-116">COM has a reputation for being difficult to learn.</span></span> <span data-ttu-id="183b0-117">撰寫新的軟體模組以支援 COM 是很棘手的。</span><span class="sxs-lookup"><span data-stu-id="183b0-117">And it is true that writing a new software module to support COM can be tricky.</span></span> <span data-ttu-id="183b0-118">但是，如果您的程式完全是 COM 的取用 *者* ，您可能會發現 com 比預期更容易理解。</span><span class="sxs-lookup"><span data-stu-id="183b0-118">But if your program is strictly a *consumer* of COM, you may find that COM is easier to understand than you expect.</span></span>

<span data-ttu-id="183b0-119">此課程模組說明如何在您的程式中呼叫以 COM 為基礎的 Api。</span><span class="sxs-lookup"><span data-stu-id="183b0-119">This module shows how to call COM-based APIs in your program.</span></span> <span data-ttu-id="183b0-120">它也會說明 COM 設計背後的一些原因。</span><span class="sxs-lookup"><span data-stu-id="183b0-120">It also describes some of the reasoning behind the design of COM.</span></span> <span data-ttu-id="183b0-121">如果您瞭解 COM 的設計方式，您可以更有效率地進行程式設計。</span><span class="sxs-lookup"><span data-stu-id="183b0-121">If you understand why COM is designed as it is, you can program with it more effectively.</span></span> <span data-ttu-id="183b0-122">此課程模組的第二個部分描述 COM 的一些建議程式設計作法。</span><span class="sxs-lookup"><span data-stu-id="183b0-122">The second part of the module describes some recommended programming practices for COM.</span></span>

<span data-ttu-id="183b0-123">COM 是在1993中引進，以支援 OLE) 2.0 (的物件連結和內嵌。</span><span class="sxs-lookup"><span data-stu-id="183b0-123">COM was introduced in 1993 to support Object Linking and Embedding (OLE) 2.0.</span></span> <span data-ttu-id="183b0-124">有時候，人們認為 COM 和 OLE 是一樣的。</span><span class="sxs-lookup"><span data-stu-id="183b0-124">People sometimes think that COM and OLE are the same thing.</span></span> <span data-ttu-id="183b0-125">這可能是您認為 COM 難以學習的另一個原因。</span><span class="sxs-lookup"><span data-stu-id="183b0-125">This may be another reason for the perception that COM is difficult to learn.</span></span> <span data-ttu-id="183b0-126">OLE 2.0 是以 COM 為基礎，但您不需要知道 OLE 就能瞭解 COM。</span><span class="sxs-lookup"><span data-stu-id="183b0-126">OLE 2.0 is built on COM, but you do not have to know OLE to understand COM.</span></span>

<span data-ttu-id="183b0-127">COM 是 *二進位標準*，不是語言標準：它會定義應用程式與軟體元件之間的二進位介面。</span><span class="sxs-lookup"><span data-stu-id="183b0-127">COM is a *binary standard*, not a language standard: It defines the binary interface between an application and a software component.</span></span> <span data-ttu-id="183b0-128">以二進位標準而言，COM 會與語言無關，雖然它會自然地對應到某些 c + + 結構。</span><span class="sxs-lookup"><span data-stu-id="183b0-128">As a binary standard, COM is language-neutral, although it maps naturally to certain C++ constructs.</span></span> <span data-ttu-id="183b0-129">此課程模組將著重于 COM 的三個主要目標：</span><span class="sxs-lookup"><span data-stu-id="183b0-129">This module will focus on three major goals of COM:</span></span>

-   <span data-ttu-id="183b0-130">將物件的執行與其介面分開。</span><span class="sxs-lookup"><span data-stu-id="183b0-130">Separating the implementation of an object from its interface.</span></span>
-   <span data-ttu-id="183b0-131">管理物件的存留期。</span><span class="sxs-lookup"><span data-stu-id="183b0-131">Managing the lifetime of an object.</span></span>
-   <span data-ttu-id="183b0-132">在執行時間探索物件的功能。</span><span class="sxs-lookup"><span data-stu-id="183b0-132">Discovering the capabilities of an object at run time.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="183b0-133">本節內容</span><span class="sxs-lookup"><span data-stu-id="183b0-133">In this section</span></span>

-   [<span data-ttu-id="183b0-134">什麼是 COM 介面？</span><span class="sxs-lookup"><span data-stu-id="183b0-134">What Is a COM Interface?</span></span>](what-is-a-com-interface-.md)
-   [<span data-ttu-id="183b0-135">初始化 COM 程式庫</span><span class="sxs-lookup"><span data-stu-id="183b0-135">Initializing the COM Library</span></span>](initializing-the-com-library.md)
-   [<span data-ttu-id="183b0-136">COM 中的錯誤碼</span><span class="sxs-lookup"><span data-stu-id="183b0-136">Error Codes in COM</span></span>](error-codes-in-com.md)
-   [<span data-ttu-id="183b0-137">在 COM 中建立物件</span><span class="sxs-lookup"><span data-stu-id="183b0-137">Creating an Object in COM</span></span>](creating-an-object-in-com.md)
-   [<span data-ttu-id="183b0-138">範例：開啟對話方塊</span><span class="sxs-lookup"><span data-stu-id="183b0-138">Example: The Open Dialog Box</span></span>](example--the-open-dialog-box.md)
-   [<span data-ttu-id="183b0-139">管理物件的存留期</span><span class="sxs-lookup"><span data-stu-id="183b0-139">Managing the Lifetime of an Object</span></span>](managing-the-lifetime-of-an-object.md)
-   [<span data-ttu-id="183b0-140">要求物件提供介面</span><span class="sxs-lookup"><span data-stu-id="183b0-140">Asking an Object for an Interface</span></span>](asking-an-object-for-an-interface.md)
-   [<span data-ttu-id="183b0-141">COM 中的記憶體配置</span><span class="sxs-lookup"><span data-stu-id="183b0-141">Memory Allocation in COM</span></span>](memory-allocation-in-com.md)
-   [<span data-ttu-id="183b0-142">COM 編碼作法</span><span class="sxs-lookup"><span data-stu-id="183b0-142">COM Coding Practices</span></span>](com-coding-practices.md)
-   [<span data-ttu-id="183b0-143">COM 中的錯誤處理</span><span class="sxs-lookup"><span data-stu-id="183b0-143">Error Handling in COM</span></span>](error-handling-in-com.md)

## <a name="related-topics"></a><span data-ttu-id="183b0-144">相關主題</span><span class="sxs-lookup"><span data-stu-id="183b0-144">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="183b0-145">學習如何以 c + + 撰寫 Windows 程式</span><span class="sxs-lookup"><span data-stu-id="183b0-145">Learn to Program for Windows in C++</span></span>](learn-to-program-for-windows.md)
</dt> </dl>

 

 