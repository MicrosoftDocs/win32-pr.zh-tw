---
title: 開始使用 Win32 和 C++
description: 本開始系列旨在告訴您如何在 c + + 中使用 Win32 和 COM Api 撰寫桌上型電腦程式。
ms.assetid: a9470cb9-a1e7-4d6d-a4be-61b81d209ada
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f5b1ad80530877e9502d158a16295013e3f4a05e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103675631"
---
# <a name="get-started-with-win32-and-c"></a><span data-ttu-id="0962e-103">開始使用 Win32 和 C++</span><span class="sxs-lookup"><span data-stu-id="0962e-103">Get Started with Win32 and C++</span></span>

<span data-ttu-id="0962e-104">本開始系列旨在告訴您如何在 c + + 中使用 Win32 和 COM Api 撰寫桌上型電腦程式。</span><span class="sxs-lookup"><span data-stu-id="0962e-104">The aim of this Get Started series is to teach you how to write a desktop program in C++ using Win32 and COM APIs.</span></span>

<span data-ttu-id="0962e-105">在第一個課程模組中，您將學習如何建立及顯示視窗的逐步解說。</span><span class="sxs-lookup"><span data-stu-id="0962e-105">In the first module, you'll learn step-by-step how to create and show a window.</span></span> <span data-ttu-id="0962e-106">稍後的課程模組會介紹元件物件模型 (COM) 、圖形和文字，以及使用者輸入。</span><span class="sxs-lookup"><span data-stu-id="0962e-106">Later modules will introduce the Component Object Model (COM), graphics and text, and user input.</span></span>

<span data-ttu-id="0962e-107">在本系列中，我們假設您對 c + + 程式設計有良好的使用知識。</span><span class="sxs-lookup"><span data-stu-id="0962e-107">For this series, it is assumed that you have a good working knowledge of C++ programming.</span></span> <span data-ttu-id="0962e-108">未採用任何先前的 Windows 程式設計經驗。</span><span class="sxs-lookup"><span data-stu-id="0962e-108">No previous experience with Windows programming is assumed.</span></span> <span data-ttu-id="0962e-109">如果您不熟悉 c + +，您可以在 [Visual C++ 開發人員中心](https://msdn.microsoft.com/vstudio//default.aspx)找到學習教材。</span><span class="sxs-lookup"><span data-stu-id="0962e-109">If you are new to C++, you can find learning material at the [Visual C++ Developer Center](https://msdn.microsoft.com/vstudio//default.aspx).</span></span> <span data-ttu-id="0962e-110"> (此資源可能無法在某些語言及國家/地區使用。 ) </span><span class="sxs-lookup"><span data-stu-id="0962e-110">(This resource may not be available in some languages and countries.)</span></span>

## <a name="in-this-section"></a><span data-ttu-id="0962e-111">本節內容</span><span class="sxs-lookup"><span data-stu-id="0962e-111">In this section</span></span>



| <span data-ttu-id="0962e-112">主題</span><span class="sxs-lookup"><span data-stu-id="0962e-112">Topic</span></span>                                                                                                     | <span data-ttu-id="0962e-113">描述</span><span class="sxs-lookup"><span data-stu-id="0962e-113">Description</span></span>                                                                                                          |
|-----------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="0962e-114">C + + 中的 Windows 程式設計簡介</span><span class="sxs-lookup"><span data-stu-id="0962e-114">Introduction to Windows Programming in C++</span></span>](introduction-to-windows-programming-in-c--.md)<br/>   | <span data-ttu-id="0962e-115">本節說明 Windows 程式設計中所使用的一些基本術語和程式碼撰寫慣例。</span><span class="sxs-lookup"><span data-stu-id="0962e-115">This section describes some of the basic terminology and coding conventions used in Windows programming.</span></span><br/>  |
| [<span data-ttu-id="0962e-116">模組1。您的第一個 Windows 程式</span><span class="sxs-lookup"><span data-stu-id="0962e-116">Module 1. Your First Windows Program</span></span>](your-first-windows-program.md)<br/>                         | <span data-ttu-id="0962e-117">在本課程模組中，您將建立簡單的 Windows 程式，以顯示空白視窗。</span><span class="sxs-lookup"><span data-stu-id="0962e-117">In this module, you will create a simple Windows program that shows a blank window.</span></span><br/>                       |
| [<span data-ttu-id="0962e-118">模組2。在您的 Windows 程式中使用 COM</span><span class="sxs-lookup"><span data-stu-id="0962e-118">Module 2. Using COM in Your Windows Program</span></span>](module-2--using-com-in-your-windows-program.md)<br/> | <span data-ttu-id="0962e-119">此課程模組介紹元件物件模型 (COM) ，其基礎為許多新式 Windows Api。</span><span class="sxs-lookup"><span data-stu-id="0962e-119">This module introduces the Component Object Model (COM), which underlies many of the modern Windows APIs.</span></span><br/> |
| [<span data-ttu-id="0962e-120">模組3。Windows 圖形</span><span class="sxs-lookup"><span data-stu-id="0962e-120">Module 3. Windows Graphics</span></span>](module-3---windows-graphics.md)<br/>                                  | <span data-ttu-id="0962e-121">此課程模組介紹 Windows 圖形架構，並著重于 Direct2D。</span><span class="sxs-lookup"><span data-stu-id="0962e-121">This module introduces the Windows graphics architecture, with a focus on Direct2D.</span></span><br/>                       |
| [<span data-ttu-id="0962e-122">模組4：使用者輸入</span><span class="sxs-lookup"><span data-stu-id="0962e-122">Module 4. User Input</span></span>](module-4--user-input.md)<br/>                                               | <span data-ttu-id="0962e-123">此課程模組說明滑鼠和鍵盤輸入。</span><span class="sxs-lookup"><span data-stu-id="0962e-123">This module describes mouse and keyboard input.</span></span><br/>                                                           |
| [<span data-ttu-id="0962e-124">範例程式碼</span><span class="sxs-lookup"><span data-stu-id="0962e-124">Sample Code</span></span>](learn-to-program-for-windows--sample-code.md)<br/>                                   | <span data-ttu-id="0962e-125">包含下載此系列之範例程式碼的連結。</span><span class="sxs-lookup"><span data-stu-id="0962e-125">Contains links to download the sample code for this series.</span></span><br/>                                               |



 

 

 





