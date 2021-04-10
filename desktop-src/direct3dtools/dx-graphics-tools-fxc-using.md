---
title: 離線編譯
description: 效果編譯器工具 (fxc.exe) 是針對 HLSL 著色器的離線編譯所設計。
ms.assetid: 56806335-a0c7-4247-b40d-ba93486a88ac
keywords:
- fxc.exe，離線編譯
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8e7c2bf96a24cb586a5d229a395cbf6dc0cb9ee1
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "103683010"
---
# <a name="offline-compiling"></a><span data-ttu-id="0ebb2-104">離線編譯</span><span class="sxs-lookup"><span data-stu-id="0ebb2-104">Offline compiling</span></span>

<span data-ttu-id="0ebb2-105">效果編譯器工具 (fxc.exe) 是針對 HLSL 著色器的離線編譯所設計。</span><span class="sxs-lookup"><span data-stu-id="0ebb2-105">The effect-compiler tool (fxc.exe) is designed for offline compilation of HLSL shaders.</span></span>

## <a name="compiling-with-the-current-compiler"></a><span data-ttu-id="0ebb2-106">使用目前的編譯器編譯</span><span class="sxs-lookup"><span data-stu-id="0ebb2-106">Compiling with the current compiler</span></span>

<span data-ttu-id="0ebb2-107">目前編譯器所支援的著色器模型會顯示在 [設定檔](dx-graphics-tools-fxc-syntax.md)中。</span><span class="sxs-lookup"><span data-stu-id="0ebb2-107">The shader models supported by the current compiler are shown in [Profiles](dx-graphics-tools-fxc-syntax.md).</span></span> <span data-ttu-id="0ebb2-108">此範例會編譯著色器模型5.1 目標的圖元著色器。</span><span class="sxs-lookup"><span data-stu-id="0ebb2-108">This example compiles a pixel shader for the shader model 5.1 target.</span></span>

```
fxc /T ps_5_1 /Fo PixelShader1.fxc PixelShader1.hlsl
```

<span data-ttu-id="0ebb2-109">在此範例中：</span><span class="sxs-lookup"><span data-stu-id="0ebb2-109">In this example:</span></span>

-   <span data-ttu-id="0ebb2-110">ps \_ 5 \_ 1 是目標設定檔。</span><span class="sxs-lookup"><span data-stu-id="0ebb2-110">ps\_5\_1 is the target profile.</span></span>
-   <span data-ttu-id="0ebb2-111">PixelShader1. fxc.exe 是輸出物件檔案，其中包含已編譯的著色器。</span><span class="sxs-lookup"><span data-stu-id="0ebb2-111">PixelShader1.fxc is the output object file containing the compiled shader.</span></span>
-   <span data-ttu-id="0ebb2-112">PixelShader1。 hlsl 是來源。</span><span class="sxs-lookup"><span data-stu-id="0ebb2-112">PixelShader1.hlsl is the source.</span></span>

```
fxc /Od /Zi /T ps_5_1 /Fo PixelShader1.fxc PixelShader1.hlsl
```

<span data-ttu-id="0ebb2-113">偵錯工具選項包含其他選項，可停用編譯器優化 (Od) 並啟用 (Zi) 的 debug 資訊，例如行號和符號。</span><span class="sxs-lookup"><span data-stu-id="0ebb2-113">The debug options include additional options to disable compiler optimizations (Od) and enable debug information (Zi) like line numbers and symbols.</span></span>

<span data-ttu-id="0ebb2-114">如需命令列選項的完整清單，請參閱 [語法](dx-graphics-tools-fxc-syntax.md) 頁面。</span><span class="sxs-lookup"><span data-stu-id="0ebb2-114">For a full listing of the command-line options, see the [Syntax](dx-graphics-tools-fxc-syntax.md) page.</span></span>

## <a name="compiling-with-the-legacy-compiler"></a><span data-ttu-id="0ebb2-115">使用舊版編譯器進行編譯</span><span class="sxs-lookup"><span data-stu-id="0ebb2-115">Compiling with the legacy compiler</span></span>

<span data-ttu-id="0ebb2-116">從 Direct3D 10 開始，已不再支援某些著色器模型。</span><span class="sxs-lookup"><span data-stu-id="0ebb2-116">Beginning with Direct3D 10, some shader models are no longer supported.</span></span> <span data-ttu-id="0ebb2-117">這些包括圖元著色器模型： ps \_ 1 \_ 1、ps \_ 1 \_ 2、ps \_ 1 \_ 3 和 ps \_ 1 \_ 4，支援非常有限的資源且相依于硬體。</span><span class="sxs-lookup"><span data-stu-id="0ebb2-117">These include pixel shader models: ps\_1\_1, ps\_1\_2, ps\_1\_3, and ps\_1\_4 which support very limited resources and are dependent on hardware.</span></span> <span data-ttu-id="0ebb2-118">編譯器已重新設計為著色器模型 2 (或更高的) ，可讓您在編譯時獲得更高的效率。</span><span class="sxs-lookup"><span data-stu-id="0ebb2-118">The compiler has been redesigned with shader model 2 (or greater) which allows for greater efficiencies with compilation.</span></span> <span data-ttu-id="0ebb2-119">這當然會要求您在支援著色器模型2和更新版本的硬體上執行。</span><span class="sxs-lookup"><span data-stu-id="0ebb2-119">This of course will require that you are running on hardware that supports shader models 2 and greater.</span></span>

<span data-ttu-id="0ebb2-120">另請注意，您應該查閱與您的 FXC.EXE 編譯器版本相關聯的 SDK 版本資訊，以瞭解受/Gec 參數影響的行為。</span><span class="sxs-lookup"><span data-stu-id="0ebb2-120">Also note that you should consult the SDK release notes associated with your version of the FXC compiler for behavior affected by the /Gec switch.</span></span>

## <a name="using-the-effect-compiler-tool-in-a-subprocess"></a><span data-ttu-id="0ebb2-121">在子流程中使用效果編譯器工具</span><span class="sxs-lookup"><span data-stu-id="0ebb2-121">Using the effect-compiler tool in a subprocess</span></span>

<span data-ttu-id="0ebb2-122">如果應用程式以子流程的形式產生 fxc.exe，請務必確保應用程式會檢查並讀取傳遞至 CreateProcess 函數的輸出或錯誤管道中的任何資料。</span><span class="sxs-lookup"><span data-stu-id="0ebb2-122">If fxc.exe is spawned as a subprocess by an application it is important to ensure that the application checks for and reads any data in output or error pipes passed to the CreateProcess function.</span></span> <span data-ttu-id="0ebb2-123">如果應用程式只會等待子流程完成，而且其中一個管道已滿，則子流程永遠不會完成。</span><span class="sxs-lookup"><span data-stu-id="0ebb2-123">If the application only waits for the subprocess to finish and one of the pipes becomes full the subprocess will never finish.</span></span>

<span data-ttu-id="0ebb2-124">下列範例程式碼說明如何等候子流程，以及讀取附加至子流程的輸出和錯誤管道。</span><span class="sxs-lookup"><span data-stu-id="0ebb2-124">The following example code illustrates waiting on a subprocess and reading the output and error pipes attached to the subprocess.</span></span> <span data-ttu-id="0ebb2-125">陣列的內容 `WaitHandles` 對應至子流程的控制碼、stdout 的管道和 stderr 的管道。</span><span class="sxs-lookup"><span data-stu-id="0ebb2-125">The contents of the `WaitHandles` array correspond to handles for the subprocess, the pipe for stdout and the pipe for stderr.</span></span>

```cpp
HANDLE WaitHandles[] = {
  piProcInfo.hProcess, hReadOutPipe, hReadErrorPipe
};

const DWORD BUFSIZE = 4096;
BYTE buff[BUFSIZE];

while (1)
{
    DWORD dwBytesRead, dwBytesAvailable;

    dwWaitResult = WaitForMultipleObjects(3, WaitHandles, FALSE, 60000L);

    // Read from the pipes...
    while (PeekNamedPipe(hReadOutPipe, NULL, 0, NULL, &dwBytesAvailable, NULL) && dwBytesAvailable)
    {
        ReadFile(hReadOutPipe, buff, BUFSIZE - 1, &dwBytesRead, 0);
        streamOut << std::string((char*)buff, (size_t)dwBytesRead);
    }
    while (PeekNamedPipe(hReadErrorPipe, NULL, 0, NULL, &dwBytesAvailable, NULL) && dwBytesAvailable)
    {
        ReadFile(hReadErrorPipe, buff, BUFSIZE - 1, &dwBytesRead, 0);
        streamError << std::string((char*)buff, (size_t)dwBytesRead);
    }

    // Process is done, or we timed out:
    if (dwWaitResult == WAIT_OBJECT_0 || dwWaitResult == WAIT_TIMEOUT)
        break;
}
```

<span data-ttu-id="0ebb2-126">如需有關產生進程的詳細資訊，請參閱 [**CreateProcess**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-createprocessa)的參考頁面。</span><span class="sxs-lookup"><span data-stu-id="0ebb2-126">For additional information on spawning a process see the reference page for [**CreateProcess**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-createprocessa).</span></span>

## <a name="related-topics"></a><span data-ttu-id="0ebb2-127">相關主題</span><span class="sxs-lookup"><span data-stu-id="0ebb2-127">Related topics</span></span>

* [<span data-ttu-id="0ebb2-128">效果-編譯器工具</span><span class="sxs-lookup"><span data-stu-id="0ebb2-128">Effect-Compiler Tool</span></span>](fxc.md)