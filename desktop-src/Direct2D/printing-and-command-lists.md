---
title: 列印和命令清單
description: Direct2D \ 32; 列印控制項是 Windows 8 之 Direct2D 模組中的新元件。
ms.assetid: C51ACCDE-B205-4F79-A2FD-D112BAAD1616
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7b6beb16a24c972016686e2dffe915a947128a63
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104375561"
---
# <a name="printing-and-command-lists"></a><span data-ttu-id="3beb0-103">列印和命令清單</span><span class="sxs-lookup"><span data-stu-id="3beb0-103">Printing and command lists</span></span>

<span data-ttu-id="3beb0-104">[Direct2D](./direct2d-portal.md) [**列印控制項**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1printcontrol)是 Windows 8 之 Direct2D 模組中的新元件。</span><span class="sxs-lookup"><span data-stu-id="3beb0-104">The [Direct2D](./direct2d-portal.md) [**print control**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1printcontrol) is a new component in the Direct2D module in Windows 8.</span></span> <span data-ttu-id="3beb0-105">此元件可讓 Direct2D apps 重複使用其 Direct2D 繪圖呼叫 (的狀態變更和轉譯基本) ，以提供類似您在螢幕上所看到的列印結果。</span><span class="sxs-lookup"><span data-stu-id="3beb0-105">This component lets Direct2D apps reuse their Direct2D drawing calls (in terms of state changes and rending primitives) to deliver printing results that are similar to what you see on the screen.</span></span>

<span data-ttu-id="3beb0-106">[**ID2D1PrintControl**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1printcontrol)介面代表虛擬列印工作：您可以建立 [Direct2D](./direct2d-portal.md)列印控制項來起始新的列印工作、針對您要列印的每個頁面傳入 Direct2D 內容，然後關閉列印控制項來完成列印工作。</span><span class="sxs-lookup"><span data-stu-id="3beb0-106">The [**ID2D1PrintControl**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1printcontrol) interface represents a virtual print job: you can create a [Direct2D](./direct2d-portal.md) print control to initiate a new print job, pass in Direct2D contents for each page you want to print, then close the print control to complete a print job.</span></span>

> [!Note]  
> <span data-ttu-id="3beb0-107">列印控制項只會對應到一項列印工作，您也無法重複使用它。</span><span class="sxs-lookup"><span data-stu-id="3beb0-107">A print control maps to one and exactly one print job, and you can't reuse it.</span></span>

<span data-ttu-id="3beb0-108">[Direct2D](./direct2d-portal.md)列印控制項會轉換和優化針對列印子系統所傳入的 Direct2D 內容，這可與真實的印表機搭配使用，以提供實際的列印結果。</span><span class="sxs-lookup"><span data-stu-id="3beb0-108">The [Direct2D](./direct2d-portal.md) print control converts and optimizes the passed in Direct2D contents for the print sub-system, which works with the real printers to deliver the actual printout.</span></span> <span data-ttu-id="3beb0-109">Direct2D apps 不會隱藏所有列印特定的詳細資料，這表示 Direct2D apps 可以列印，而不需要知道其繪製的裝置，或如何將繪圖轉譯成列印。</span><span class="sxs-lookup"><span data-stu-id="3beb0-109">All print-specific details are hidden from Direct2D apps, which means Direct2D apps can print without knowing what devices they are drawing to, or how the drawings are translated to printing.</span></span>

<span data-ttu-id="3beb0-110">若要使用 [Direct2D](./direct2d-portal.md)進行列印，您需要為您想要列印的每個頁面準備一個 Direct2D 命令清單，然後將該命令清單傳遞給 Direct2D 列印控制項。</span><span class="sxs-lookup"><span data-stu-id="3beb0-110">To print with [Direct2D](./direct2d-portal.md), you need to prepare one Direct2D command list for each page you want to print, then pass that command list to the Direct2D print control.</span></span> <span data-ttu-id="3beb0-111">若要準備該 Direct2D 命令清單，您只需建立命令清單，並將其設定為目前裝置內容的繪製目標，然後繪製至該裝置內容，就像您繪製到點陣圖目標以供顯示一樣。</span><span class="sxs-lookup"><span data-stu-id="3beb0-111">To prepare that Direct2D command list, you simply create and set a command list as the drawing target of the current device context, and then draw to that device context, exactly as if you are drawing to a bitmap target for display.</span></span> <span data-ttu-id="3beb0-112">如需裝置和目標的詳細資訊，請參閱 [裝置和裝置](devices-and-device-contexts.md) 內容。</span><span class="sxs-lookup"><span data-stu-id="3beb0-112">See [Devices and Device Contexts](devices-and-device-contexts.md) for more info on devices and targets.</span></span>

<span data-ttu-id="3beb0-113">下圖說明應用程式、裝置內容、點陣圖目標、命令清單目標和列印控制項之間的互動。</span><span class="sxs-lookup"><span data-stu-id="3beb0-113">The diagram here illustrates the interaction between the app, device context, bitmap target, command list target, and the print control.</span></span>

> [!Note]  
> <span data-ttu-id="3beb0-114">Windows 列印 Sub-System 和印表機元件都是灰色，因為它們完全隱藏在 [Direct2D](./direct2d-portal.md) apps 中。</span><span class="sxs-lookup"><span data-stu-id="3beb0-114">The Windows Print Sub-System and Printer components are in gray because they are completely hidden from [Direct2D](./direct2d-portal.md) apps.</span></span>

![顯示 commandlist 和列印如何與應用程式和 direct2d 互動的圖表。](images/d2dprintcontroldiagram.png)

## <a name="example"></a><span data-ttu-id="3beb0-116">範例</span><span class="sxs-lookup"><span data-stu-id="3beb0-116">Example</span></span>

<span data-ttu-id="3beb0-117">列印 Direct2D 內容的完整流程包含下列步驟。</span><span class="sxs-lookup"><span data-stu-id="3beb0-117">The complete process of printing Direct2D content includes the following steps.</span></span>

1.  <span data-ttu-id="3beb0-118">建立列印控制項來起始列印工作。</span><span class="sxs-lookup"><span data-stu-id="3beb0-118">Create a print control to initiate a print job.</span></span>
2.  <span data-ttu-id="3beb0-119">藉由傳入命令清單，將頁面加入至列印控制項。</span><span class="sxs-lookup"><span data-stu-id="3beb0-119">Add a page to the print control by passing in a command list.</span></span>
3.  <span data-ttu-id="3beb0-120">針對檔其餘部分中的每個頁面重複步驟2</span><span class="sxs-lookup"><span data-stu-id="3beb0-120">Repeat step 2 for each page in the rest of the document</span></span>
4.  <span data-ttu-id="3beb0-121">關閉列印控制項以完成列印工作。</span><span class="sxs-lookup"><span data-stu-id="3beb0-121">Close the print control to complete the print job.</span></span>

<span data-ttu-id="3beb0-122">以下是顯示進程的程式碼範例。</span><span class="sxs-lookup"><span data-stu-id="3beb0-122">Here is a code example showing the process.</span></span>

```cpp
ID2D1CommandList* commandList;
// Skip command list creation and drawing for simplicity.

// Set print control properties.
D2D1_PRINT_CONTROL_PROPERTIES printControlProperties;
printControlProperties.rasterDPI = 150.0f; // Use the default rasterization DPI for all unsupported Direct2D commands 
                                                                                                                                                                            //  or options.
printControlProperties.fontSubset = D2D1_PRINT_FONT_SUBSET_MODE_DEFAULT; // Using the default font subset strategy.
printControlProperties.colorSpace = D2D1_COLOR_SPACE_SRGB; // Color space for vector graphics in Direct2D print control.

// Create a Direct2D Print Control to initiate a print job.
ID2D1PrintControl* d2dPrintControl;
d2dDevice->CreatePrintControl(
    wicFactory,
    documentTarget,
    printControlProperties,
    &d2dPrintControl
    );

// Add Direct2D drawing commands encapsulated in a command list.
// You can add in more pages by calling this API multiple times.
d2dPrintControl->AddPage(commandList);

// Close the print control to complete a print job.
d2dPrintControl->Close();
```

## <a name="related-topics"></a><span data-ttu-id="3beb0-123">相關主題</span><span class="sxs-lookup"><span data-stu-id="3beb0-123">Related topics</span></span>

[<span data-ttu-id="3beb0-124">**ID2D1CommandList**</span><span class="sxs-lookup"><span data-stu-id="3beb0-124">**ID2D1CommandList**</span></span>](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1commandlist)

[<span data-ttu-id="3beb0-125">**ID2D1PrintControl**</span><span class="sxs-lookup"><span data-stu-id="3beb0-125">**ID2D1PrintControl**</span></span>](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1printcontrol)

[<span data-ttu-id="3beb0-126">改善 Direct2D 應用程式和列印的效能</span><span class="sxs-lookup"><span data-stu-id="3beb0-126">Improving the Performance of Direct2D Applications and Printing</span></span>](improving-direct2d-performance.md)