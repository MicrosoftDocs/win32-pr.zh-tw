---
description: 本主題列出撰寫 Direct3D 應用程式時可能遇到的常見問題類別，以及如何防止這些問題。
ms.assetid: 27b87f0f-7118-4252-b6e8-6ea18a9399e4
title: '疑難排解 (Direct3D 9) '
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6726e761dd8c15e2da18e6c370472a73e82cef0b
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "106999827"
---
# <a name="troubleshooting-direct3d-9"></a><span data-ttu-id="a29f3-103">疑難排解 (Direct3D 9) </span><span class="sxs-lookup"><span data-stu-id="a29f3-103">Troubleshooting (Direct3D 9)</span></span>

<span data-ttu-id="a29f3-104">本主題列出撰寫 Direct3D 應用程式時可能遇到的常見問題類別，以及如何防止這些問題。</span><span class="sxs-lookup"><span data-stu-id="a29f3-104">This topic lists common categories of problems that you might encounter when writing Direct3D applications, and how to prevent them.</span></span>

## <a name="device-creation"></a><span data-ttu-id="a29f3-105">裝置建立</span><span class="sxs-lookup"><span data-stu-id="a29f3-105">Device Creation</span></span>

<span data-ttu-id="a29f3-106">如果您的應用程式在裝置建立期間失敗，請檢查是否有下列常見的錯誤。</span><span class="sxs-lookup"><span data-stu-id="a29f3-106">If your application fails during device creation, check for the following common errors.</span></span>

-   <span data-ttu-id="a29f3-107">請務必檢查裝置的功能，特別是轉譯的深度。</span><span class="sxs-lookup"><span data-stu-id="a29f3-107">Make sure you check the device capabilities, particularly the render depths.</span></span>
-   <span data-ttu-id="a29f3-108">檢查錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="a29f3-108">Examine the error code.</span></span> <span data-ttu-id="a29f3-109">\_一律可以 D3DERR OUTOFVIDEOMEMORY。</span><span class="sxs-lookup"><span data-stu-id="a29f3-109">D3DERR\_OUTOFVIDEOMEMORY is always possible.</span></span>
-   <span data-ttu-id="a29f3-110">使用 (Dll) 的偵錯工具 DirectX 動態連結程式庫，並在偵錯工具下查看輸出訊息。</span><span class="sxs-lookup"><span data-stu-id="a29f3-110">Use the debug DirectX dynamic-link libraries (DLLs) and review output messages under the debugger.</span></span>

## <a name="using-lit-vertices"></a><span data-ttu-id="a29f3-111">使用亮頂點</span><span class="sxs-lookup"><span data-stu-id="a29f3-111">Using Lit Vertices</span></span>

<span data-ttu-id="a29f3-112">使用亮頂點的應用程式應該將 D3DRS \_ 光源轉譯狀態設為 **FALSE**，以停用 Direct3D 光源引擎。</span><span class="sxs-lookup"><span data-stu-id="a29f3-112">Applications that use lit vertices should disable the Direct3D lighting engine by setting the D3DRS\_LIGHTING render state to **FALSE**.</span></span> <span data-ttu-id="a29f3-113">根據預設，當啟用光源時，系統會將不含一般向量的任何頂點色彩設定為 0 (黑色) ，即使輸入頂點包含非零的色彩值也是如此。</span><span class="sxs-lookup"><span data-stu-id="a29f3-113">By default, when lighting is enabled, the system sets the color for any vertex that doesn't contain a normal vector to 0 (black), even if the input vertex contained a nonzero color value.</span></span> <span data-ttu-id="a29f3-114">由於頂點的本質不會包含頂點標準，因此，如果已啟用光源引擎，則在轉譯期間傳遞給 Direct3D 的任何色彩資訊都會遺失。</span><span class="sxs-lookup"><span data-stu-id="a29f3-114">Because lit-vertices don't, by their nature, contain a vertex normal, any color information passed to Direct3D is lost during rendering if the lighting engine is enabled.</span></span>

<span data-ttu-id="a29f3-115">很明顯地，頂點色彩對執行它自己光源的任何應用程式都很重要。</span><span class="sxs-lookup"><span data-stu-id="a29f3-115">Obviously, vertex color is important to any application that performs its own lighting.</span></span> <span data-ttu-id="a29f3-116">若要防止系統強加預設值，請務必將 D3DRS \_ 光源設定為 **FALSE**。</span><span class="sxs-lookup"><span data-stu-id="a29f3-116">To prevent the system from imposing the default values, make sure you set D3DRS\_LIGHTING to **FALSE**.</span></span>

<span data-ttu-id="a29f3-117">如果您的應用程式執行，但未顯示任何內容，請檢查是否有下列常見的錯誤。</span><span class="sxs-lookup"><span data-stu-id="a29f3-117">If your application runs but nothing is visible, check for the following common errors.</span></span>

-   <span data-ttu-id="a29f3-118">確定您的三角形不是退化的。</span><span class="sxs-lookup"><span data-stu-id="a29f3-118">Ensure that your triangles are not degenerate.</span></span>
-   <span data-ttu-id="a29f3-119">確定您的三角形未挑選。</span><span class="sxs-lookup"><span data-stu-id="a29f3-119">Ensure that your triangles are not being culled.</span></span>
-   <span data-ttu-id="a29f3-120">請確定您的轉換在內部保持一致。</span><span class="sxs-lookup"><span data-stu-id="a29f3-120">Make sure that your transformations are internally consistent.</span></span>
-   <span data-ttu-id="a29f3-121">請檢查 [視口] 設定，以確定可以看見您的三角形。</span><span class="sxs-lookup"><span data-stu-id="a29f3-121">Check the viewport settings to be sure they allow your triangles to be seen.</span></span>

## <a name="debugging"></a><span data-ttu-id="a29f3-122">偵錯</span><span class="sxs-lookup"><span data-stu-id="a29f3-122">Debugging</span></span>

<span data-ttu-id="a29f3-123">對 Direct3D 應用程式進行偵錯工具可能是一項挑戰。</span><span class="sxs-lookup"><span data-stu-id="a29f3-123">Debugging a Direct3D application can be challenging.</span></span> <span data-ttu-id="a29f3-124">除了檢查所有傳回值之外，您還可以嘗試下列技巧，這是 Direct3D 程式設計中特別重要的建議，其相依于非常不同的硬體。</span><span class="sxs-lookup"><span data-stu-id="a29f3-124">Try the following techniques, in addition to checking all the return values - a particularly important piece of advice in Direct3D programming, which is dependent on very different hardware implementations.</span></span>

-   <span data-ttu-id="a29f3-125">切換至 debug Dll。</span><span class="sxs-lookup"><span data-stu-id="a29f3-125">Switch to debug DLLs.</span></span>
-   <span data-ttu-id="a29f3-126">強制軟體專用裝置，即使可用，仍關閉硬體加速。</span><span class="sxs-lookup"><span data-stu-id="a29f3-126">Force a software-only device, turning off hardware acceleration even when it is available.</span></span>
-   <span data-ttu-id="a29f3-127">強制表面進入系統記憶體。</span><span class="sxs-lookup"><span data-stu-id="a29f3-127">Force surfaces into system memory.</span></span>
-   <span data-ttu-id="a29f3-128">建立在視窗中執行的選項，讓您可以使用整合式偵錯工具。</span><span class="sxs-lookup"><span data-stu-id="a29f3-128">Create an option to run in a window, so that you can use an integrated debugger.</span></span>

<span data-ttu-id="a29f3-129">這份清單中的第二個和第三個選項可協助您避免 Win16 鎖定，否則可能會導致偵錯工具停止回應。</span><span class="sxs-lookup"><span data-stu-id="a29f3-129">The second and third options in this list can help you avoid the Win16 lock which can otherwise cause your debugger to hang.</span></span>

<span data-ttu-id="a29f3-130">此外，請嘗試新增下列專案以 Win.ini。</span><span class="sxs-lookup"><span data-stu-id="a29f3-130">Also, try adding the following entries to Win.ini.</span></span>


```
[Direct3D] 
debug=3 
[DirectDraw] 
debug=3 
```



## <a name="borland-floating-point-initialization"></a><span data-ttu-id="a29f3-131">Borland Floating-Point 初始化</span><span class="sxs-lookup"><span data-stu-id="a29f3-131">Borland Floating-Point Initialization</span></span>

<span data-ttu-id="a29f3-132">Borland 的編譯器會以與 Direct3D 不相容的方式來報告浮點例外狀況。</span><span class="sxs-lookup"><span data-stu-id="a29f3-132">Compilers from Borland report floating-point exceptions in a manner that is incompatible with Direct3D.</span></span> <span data-ttu-id="a29f3-133">若要解決這個問題，請包含 \_ matherr 例外狀況處理常式，如下所示：</span><span class="sxs-lookup"><span data-stu-id="a29f3-133">To solve this problem, include a \_matherr exception handler like the following:</span></span>


```
// Borland floating point initialization 
#include <math.h>
#include <float.h>

void initfp(void)
{
    // Disable floating point exceptions
    _control87(MCW_EM,MCW_EM);
}

int _matherr(struct _exception  *e)
{
    e;               // Dummy reference to catch the warning
    return 1;        // Error has been handled
}
```



## <a name="parameter-validation"></a><span data-ttu-id="a29f3-134">參數驗證</span><span class="sxs-lookup"><span data-stu-id="a29f3-134">Parameter Validation</span></span>

<span data-ttu-id="a29f3-135">基於效能的考慮，Direct3D 立即模式執行時間的 debug 版會執行比零售版本更多的參數驗證，這有時不會執行任何驗證。</span><span class="sxs-lookup"><span data-stu-id="a29f3-135">For performance reasons, the debug version of the Direct3D Immediate Mode run time performs more parameter validation than the retail version, which sometimes performs no validation at all.</span></span> <span data-ttu-id="a29f3-136">這可讓應用程式使用較慢的偵錯工具執行時間元件來執行健全的偵錯工具，然後再使用更快速的零售版本來微調效能和最終發行版本。</span><span class="sxs-lookup"><span data-stu-id="a29f3-136">This enables applications to perform robust debugging with the slower debug run-time component before using the faster retail version for performance tuning and final release.</span></span>

<span data-ttu-id="a29f3-137">雖然有幾個 Direct3D 立即模式方法會限制它們可接受的值，但通常只會檢查並強制執行 Direct3D 立即模式執行時間的偵錯工具版本的限制。</span><span class="sxs-lookup"><span data-stu-id="a29f3-137">Although several Direct3D Immediate Mode methods impose limits on the values that they can accept, these limits are often only checked and enforced by the debug version of the Direct3D Immediate Mode run time.</span></span> <span data-ttu-id="a29f3-138">應用程式必須符合這些限制，在零售版 Direct3D 上執行時可能會發生無法預期且不想要的結果。</span><span class="sxs-lookup"><span data-stu-id="a29f3-138">Applications must conform to these limits, or unpredictable and undesirable results can occur when running on the retail version of Direct3D.</span></span> <span data-ttu-id="a29f3-139">例如， [**IDirect3DDevice9：:D rawprimitive**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawprimitive) 方法可接受參數 (PrimitiveCount) ，指出方法將會轉譯的基本專案數目。</span><span class="sxs-lookup"><span data-stu-id="a29f3-139">For example, the [**IDirect3DDevice9::DrawPrimitive**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawprimitive) method accepts a parameter (PrimitiveCount) that indicates the number of primitives that the method will render.</span></span> <span data-ttu-id="a29f3-140">方法只能接受0到 D3DMAXNUMPRIMITIVES 之間的值。</span><span class="sxs-lookup"><span data-stu-id="a29f3-140">The method can only accept values between 0 and D3DMAXNUMPRIMITIVES.</span></span> <span data-ttu-id="a29f3-141">在 Direct3D 的 debug 版中，如果您傳遞超過 D3DMAXNUMPRIMITIVES 的基本專案，方法會正常失敗、將錯誤訊息列印到錯誤記錄檔，並將錯誤值傳回給您的應用程式。</span><span class="sxs-lookup"><span data-stu-id="a29f3-141">In the debug version of Direct3D, if you pass more than D3DMAXNUMPRIMITIVES primitives, the method fails gracefully, printing an error message to the error log, and returning an error value to your application.</span></span> <span data-ttu-id="a29f3-142">相反地，如果您的應用程式在執行時間的零售版本上執行時，會產生相同的錯誤，則行為會是未定義的。</span><span class="sxs-lookup"><span data-stu-id="a29f3-142">Conversely, if your application makes the same error when it is running with the retail version of the run time, behavior is undefined.</span></span> <span data-ttu-id="a29f3-143">基於效能的考慮，方法不會驗證參數，因而導致無法預期的行為，而且在不正確情況下，會產生完全的狀況。</span><span class="sxs-lookup"><span data-stu-id="a29f3-143">For performance reasons, the method does not validate the parameters, resulting in unpredictable and completely situational behavior when they are not valid.</span></span> <span data-ttu-id="a29f3-144">在某些情況下，呼叫可能會運作，而在其他情況下，可能會導致 Direct3D 中的記憶體錯誤。</span><span class="sxs-lookup"><span data-stu-id="a29f3-144">In some cases the call might work, and in other cases it might cause a memory fault in Direct3D.</span></span> <span data-ttu-id="a29f3-145">如果不正確呼叫一致地使用特定的硬體設定和 DirectX 版本，則不保證它會繼續在其他硬體上運作，或使用較新的 DirectX 版本。</span><span class="sxs-lookup"><span data-stu-id="a29f3-145">If an invalid call consistently works with a particular hardware configuration and DirectX version, there is no guarantee that it will continue to function on other hardware or with later releases of DirectX.</span></span>

<span data-ttu-id="a29f3-146">如果您的應用程式在執行零售 Direct3D 執行時間檔案時遇到未相關的失敗，請針對偵錯工具版本進行測試，並仔細查看您的應用程式傳遞無效參數的案例。</span><span class="sxs-lookup"><span data-stu-id="a29f3-146">If your application encounters unexplained failures when running with the retail Direct3D run-time file, test against the debug version and look closely for cases where your application passes invalid parameters.</span></span> <span data-ttu-id="a29f3-147">使用 DirectX 控制台小程式，視需要切換至偵錯工具執行時間，然後選取 [在 D3DError 時中斷] 選項。</span><span class="sxs-lookup"><span data-stu-id="a29f3-147">Use the DirectX control panel applet, switch to the debug runtime if necessary, and check the "Break on D3DError" option.</span></span> <span data-ttu-id="a29f3-148">此選項會強制執行時間使用 Windows DebugBreak 方法，以強制應用程式在偵測到應用程式錯誤時停止。</span><span class="sxs-lookup"><span data-stu-id="a29f3-148">This option will force the runtime to use the Windows DebugBreak method in order to force the application to stop when an application bug is detected.</span></span>

## <a name="related-topics"></a><span data-ttu-id="a29f3-149">相關主題</span><span class="sxs-lookup"><span data-stu-id="a29f3-149">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a29f3-150">程式設計秘訣</span><span class="sxs-lookup"><span data-stu-id="a29f3-150">Programming Tips</span></span>](programming-tips.md)
</dt> </dl>

 

 
