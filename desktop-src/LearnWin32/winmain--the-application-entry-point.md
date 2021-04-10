---
title: WinMain 應用程式進入點
description: .
ms.assetid: 389da5d4-d0f9-4339-be6c-0f4fecc59316
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bef44c4d31aa53dfd60f579b68c438a539058b85
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2020
ms.locfileid: "104185633"
---
# <a name="winmain-the-application-entry-point"></a><span data-ttu-id="46303-103">WinMain：應用程式進入點</span><span class="sxs-lookup"><span data-stu-id="46303-103">WinMain: The Application Entry Point</span></span>

<span data-ttu-id="46303-104">每個 Windows 程式都包含一個名為 **WinMain** 或 **wWinMain** 的進入點函數。</span><span class="sxs-lookup"><span data-stu-id="46303-104">Every Windows program includes an entry-point function that is named either **WinMain** or **wWinMain**.</span></span> <span data-ttu-id="46303-105">以下是 **wWinMain** 的簽章。</span><span class="sxs-lookup"><span data-stu-id="46303-105">Here is the signature for **wWinMain**.</span></span>


```C++
int WINAPI wWinMain(HINSTANCE hInstance, HINSTANCE hPrevInstance, PWSTR pCmdLine, int nCmdShow);
```



<span data-ttu-id="46303-106">這四個參數為：</span><span class="sxs-lookup"><span data-stu-id="46303-106">The four parameters are:</span></span>

-   <span data-ttu-id="46303-107">*hInstance* 稱為「實例的控制碼」或「模組的控制碼」。</span><span class="sxs-lookup"><span data-stu-id="46303-107">*hInstance* is something called a "handle to an instance" or "handle to a module."</span></span> <span data-ttu-id="46303-108">作業系統會在載入記憶體時，使用這個值來識別可執行檔 (EXE) 。</span><span class="sxs-lookup"><span data-stu-id="46303-108">The operating system uses this value to identify the executable (EXE) when it is loaded in memory.</span></span> <span data-ttu-id="46303-109">某些 Windows 函式需要實例控制碼，例如載入圖示或點陣圖。</span><span class="sxs-lookup"><span data-stu-id="46303-109">The instance handle is needed for certain Windows functions—for example, to load icons or bitmaps.</span></span>
-   <span data-ttu-id="46303-110">*hPrevInstance* 沒有任何意義。</span><span class="sxs-lookup"><span data-stu-id="46303-110">*hPrevInstance* has no meaning.</span></span> <span data-ttu-id="46303-111">它是在16位 Windows 中使用，但現在一律為零。</span><span class="sxs-lookup"><span data-stu-id="46303-111">It was used in 16-bit Windows, but is now always zero.</span></span>
-   <span data-ttu-id="46303-112">*pCmdLine* 包含命令列引數做為 Unicode 字串。</span><span class="sxs-lookup"><span data-stu-id="46303-112">*pCmdLine* contains the command-line arguments as a Unicode string.</span></span>
-   <span data-ttu-id="46303-113">*nCmdShow* 是一個旗標，指出主要應用程式視窗將會最小化、最大化，或正常顯示。</span><span class="sxs-lookup"><span data-stu-id="46303-113">*nCmdShow* is a flag that says whether the main application window will be minimized, maximized, or shown normally.</span></span>

<span data-ttu-id="46303-114">函數會傳回 **int** 值。</span><span class="sxs-lookup"><span data-stu-id="46303-114">The function returns an **int** value.</span></span> <span data-ttu-id="46303-115">作業系統不會使用傳回值，但您可以使用傳回值來將狀態碼傳達給您所撰寫的其他程式。</span><span class="sxs-lookup"><span data-stu-id="46303-115">The return value is not used by the operating system, but you can use the return value to convey a status code to some other program that you write.</span></span>

<span data-ttu-id="46303-116">**WINAPI** 是呼叫慣例。</span><span class="sxs-lookup"><span data-stu-id="46303-116">**WINAPI** is the calling convention.</span></span> <span data-ttu-id="46303-117">*呼叫慣例* 會定義函數如何從呼叫端接收參數。</span><span class="sxs-lookup"><span data-stu-id="46303-117">A *calling convention* defines how a function receives parameters from the caller.</span></span> <span data-ttu-id="46303-118">例如，它會定義參數出現在堆疊上的順序。</span><span class="sxs-lookup"><span data-stu-id="46303-118">For example, it defines the order that parameters appear on the stack.</span></span> <span data-ttu-id="46303-119">請務必宣告您的 **wWinMain** 函式，如下所示。</span><span class="sxs-lookup"><span data-stu-id="46303-119">Just make sure to declare your **wWinMain** function as shown.</span></span>

<span data-ttu-id="46303-120">**WinMain** 函式與 **wWinMain** 相同，不同之處在于命令列引數會做為 ANSI 字串傳遞。</span><span class="sxs-lookup"><span data-stu-id="46303-120">The **WinMain** function is identical to **wWinMain**, except the command-line arguments are passed as an ANSI string.</span></span> <span data-ttu-id="46303-121">慣用的 Unicode 版本。</span><span class="sxs-lookup"><span data-stu-id="46303-121">The Unicode version is preferred.</span></span> <span data-ttu-id="46303-122">即使您將程式編譯成 Unicode，也可以使用 ANSI **WinMain** 函數。</span><span class="sxs-lookup"><span data-stu-id="46303-122">You can use the ANSI **WinMain** function even if you compile your program as Unicode.</span></span> <span data-ttu-id="46303-123">若要取得命令列引數的 Unicode 複本，請呼叫 [**GetCommandLine**](/windows/desktop/api/processenv/nf-processenv-getcommandlinea) 函數。</span><span class="sxs-lookup"><span data-stu-id="46303-123">To get a Unicode copy of the command-line arguments, call the [**GetCommandLine**](/windows/desktop/api/processenv/nf-processenv-getcommandlinea) function.</span></span> <span data-ttu-id="46303-124">此函數會傳回單一字串中的所有引數。</span><span class="sxs-lookup"><span data-stu-id="46303-124">This function returns all of the arguments in a single string.</span></span> <span data-ttu-id="46303-125">如果您想要引數做為 *argv* 樣式陣列，請將此字串傳遞給 [**CommandLineToArgvW**](/windows/desktop/api/shellapi/nf-shellapi-commandlinetoargvw)。</span><span class="sxs-lookup"><span data-stu-id="46303-125">If you want the arguments as an *argv*-style array, pass this string to [**CommandLineToArgvW**](/windows/desktop/api/shellapi/nf-shellapi-commandlinetoargvw).</span></span>

<span data-ttu-id="46303-126">編譯器如何知道要叫用 **wWinMain** ，而不是標準 **main** 函數？</span><span class="sxs-lookup"><span data-stu-id="46303-126">How does the compiler know to invoke **wWinMain** instead of the standard **main** function?</span></span> <span data-ttu-id="46303-127">實際的情況是，Microsoft C 執行時間程式庫 (CRT) 提供可呼叫 **WinMain** 或 **wWinMain** 的 **main** 的實。</span><span class="sxs-lookup"><span data-stu-id="46303-127">What actually happens is that the Microsoft C runtime library (CRT) provides an implementation of **main** that calls either **WinMain** or **wWinMain**.</span></span>

> [!Note]  
> <span data-ttu-id="46303-128">CRT 會在 **main** 內執行一些額外的工作。</span><span class="sxs-lookup"><span data-stu-id="46303-128">The CRT does some additional work inside **main**.</span></span> <span data-ttu-id="46303-129">例如，在 **wWinMain** 之前，會呼叫任何靜態初始化運算式。</span><span class="sxs-lookup"><span data-stu-id="46303-129">For example, any static initializers are called before **wWinMain**.</span></span> <span data-ttu-id="46303-130">雖然您可以指示連結器使用不同的進入點函式，但如果您連結至 CRT，則使用預設值。</span><span class="sxs-lookup"><span data-stu-id="46303-130">Although you can tell the linker to use a different entry-point function, use the default if you link to the CRT.</span></span> <span data-ttu-id="46303-131">否則，將會略過 CRT 初始化程式碼，並產生無法預測的結果。</span><span class="sxs-lookup"><span data-stu-id="46303-131">Otherwise, the CRT initialization code will be skipped, with unpredictable results.</span></span> <span data-ttu-id="46303-132"> (例如，全域物件將無法正確初始化。 ) </span><span class="sxs-lookup"><span data-stu-id="46303-132">(For example, global objects will not be initialized correctly.)</span></span>

 

<span data-ttu-id="46303-133">以下是空的 **WinMain** 函數。</span><span class="sxs-lookup"><span data-stu-id="46303-133">Here is an empty **WinMain** function.</span></span>


```C++
INT WinMain(HINSTANCE hInstance, HINSTANCE hPrevInstance,
    PSTR lpCmdLine, INT nCmdShow)
{
    return 0;
}
```



<span data-ttu-id="46303-134">既然您已經有進入點，並且瞭解一些基本的術語和程式碼撰寫慣例，就可以開始建立完整的視窗程式。</span><span class="sxs-lookup"><span data-stu-id="46303-134">Now that you have the entry point and understand some of the basic terminology and coding conventions, you are ready to create a complete Window program.</span></span>

## <a name="next"></a><span data-ttu-id="46303-135">下一個</span><span class="sxs-lookup"><span data-stu-id="46303-135">Next</span></span>

<span data-ttu-id="46303-136">[模組1。您的第一個 Windows 程式](your-first-windows-program.md)。</span><span class="sxs-lookup"><span data-stu-id="46303-136">[Module 1. Your First Windows Program](your-first-windows-program.md).</span></span>

 

 