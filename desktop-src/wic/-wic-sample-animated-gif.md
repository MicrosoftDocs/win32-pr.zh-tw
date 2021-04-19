---
description: 這個範例會示範如何解碼 GIF 檔案中的各種框架、為每個框架讀取適當的中繼資料、撰寫框架，以及使用 Direct2D 呈現動畫。
ms.assetid: d71c66b5-d37c-4c8a-bfd7-b97c69c3b8e9
title: WIC 動畫 Gif 範例
ms.topic: article
ms.date: 03/19/2021
ms.custom: project-verbatim
ms.openlocfilehash: afb0c1368e2c66d40d1be4095ec56d5daeb5ab53
ms.sourcegitcommit: af120ad5c30da2fc5eb717ca2a1c4c45878efd71
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/20/2021
ms.locfileid: "107000646"
---
# <a name="wic-animated-gif-sample"></a><span data-ttu-id="955f0-103">WIC 動畫 GIF 範例</span><span class="sxs-lookup"><span data-stu-id="955f0-103">WIC animated GIF sample</span></span>

<span data-ttu-id="955f0-104">這個範例會示範如何解碼 GIF 檔案中的各種框架、為每個框架讀取適當的中繼資料、撰寫框架，以及使用 Direct2D 呈現動畫。</span><span class="sxs-lookup"><span data-stu-id="955f0-104">This sample demonstrates decoding various frames in a GIF file, reading appropriate metadata for each frame, composing frames, and rendering the animation with Direct2D.</span></span>

## <a name="requirements"></a><span data-ttu-id="955f0-105">規格需求</span><span class="sxs-lookup"><span data-stu-id="955f0-105">Requirements</span></span>

<span data-ttu-id="955f0-106">此範例具有下列需求。</span><span class="sxs-lookup"><span data-stu-id="955f0-106">This sample has the following requirements.</span></span>

| <span data-ttu-id="955f0-107">需求</span><span class="sxs-lookup"><span data-stu-id="955f0-107">Requirement</span></span> | <span data-ttu-id="955f0-108">值</span><span class="sxs-lookup"><span data-stu-id="955f0-108">Value</span></span> |
|-|-|
| <span data-ttu-id="955f0-109">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="955f0-109">Minimum supported client</span></span> | <span data-ttu-id="955f0-110">Windows 7</span><span class="sxs-lookup"><span data-stu-id="955f0-110">Windows 7</span></span> |
| <span data-ttu-id="955f0-111">最小 Windows SDK</span><span class="sxs-lookup"><span data-stu-id="955f0-111">Minimum Windows SDK</span></span> | <span data-ttu-id="955f0-112">適用于 Windows 7 的[Windows 軟體開發套件 (SDK) ](https://msdn.microsoft.com/windowsvista/bb980924.aspx)</span><span class="sxs-lookup"><span data-stu-id="955f0-112">[Windows Software Development Kit (SDK)](https://msdn.microsoft.com/windowsvista/bb980924.aspx) for Windows 7</span></span> |

## <a name="downloading-the-sample"></a><span data-ttu-id="955f0-113">下載範例</span><span class="sxs-lookup"><span data-stu-id="955f0-113">Downloading the sample</span></span>

<span data-ttu-id="955f0-114">此範例可在 [WIC 動畫 GIF](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/multimedia/wic/wicanimatedgif)中取得。</span><span class="sxs-lookup"><span data-stu-id="955f0-114">This sample is available at [WIC animated GIF](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/multimedia/wic/wicanimatedgif).</span></span>

## <a name="building-the-sample"></a><span data-ttu-id="955f0-115">建置範例</span><span class="sxs-lookup"><span data-stu-id="955f0-115">Building the sample</span></span>

### <a name="using-visual-studio-preferred-method"></a><span data-ttu-id="955f0-116">使用 Visual Studio (慣用方法) </span><span class="sxs-lookup"><span data-stu-id="955f0-116">Using Visual Studio (preferred method)</span></span>

1. <span data-ttu-id="955f0-117">開啟 Windows 檔案總管，巡覽至目錄。</span><span class="sxs-lookup"><span data-stu-id="955f0-117">Open Windows Explorer and navigate to the directory.</span></span>
2. <span data-ttu-id="955f0-118">按兩下 .sln (方案的圖示) 檔案，在 Visual Studio 中開啟檔案。</span><span class="sxs-lookup"><span data-stu-id="955f0-118">Double-click the icon for the .sln (solution) file to open the file in Visual Studio.</span></span>
3. <span data-ttu-id="955f0-119">在 [建置] 功能表中，選取 [建置方案]。</span><span class="sxs-lookup"><span data-stu-id="955f0-119">In the **Build** menu, select **Build Solution**.</span></span> <span data-ttu-id="955f0-120">應用程式將會建立在預設的 \\ Debug 或 \\ Release 目錄中。</span><span class="sxs-lookup"><span data-stu-id="955f0-120">The application will be built in the default \\Debug or \\Release directory.</span></span>

### <a name="using-the-command-prompt"></a><span data-ttu-id="955f0-121">使用命令提示字元</span><span class="sxs-lookup"><span data-stu-id="955f0-121">Using the command prompt</span></span>

<span data-ttu-id="955f0-122">使用命令提示字元建立範例。</span><span class="sxs-lookup"><span data-stu-id="955f0-122">To build the sample by using a command prompt.</span></span>

1. <span data-ttu-id="955f0-123">開啟命令提示字元，然後流覽至範例目錄。</span><span class="sxs-lookup"><span data-stu-id="955f0-123">Open the command prompt and navigate to the sample directory.</span></span>
2. <span data-ttu-id="955f0-124">輸入 `msbuild WICAnimatedGif.sln`</span><span class="sxs-lookup"><span data-stu-id="955f0-124">Type `msbuild WICAnimatedGif.sln`</span></span>

## <a name="running-the-sample"></a><span data-ttu-id="955f0-125">執行範例</span><span class="sxs-lookup"><span data-stu-id="955f0-125">Running the sample</span></span>

<span data-ttu-id="955f0-126">應用程式啟動之後，使用 [檔案 **] 功能表的 [** **開啟**] 命令載入影像檔案。</span><span class="sxs-lookup"><span data-stu-id="955f0-126">After the application is launched, load an image file by using the **Open** command of the **File** menu.</span></span> <span data-ttu-id="955f0-127">支援視窗調整大小。</span><span class="sxs-lookup"><span data-stu-id="955f0-127">Window resizing is supported.</span></span>

## <a name="see-also"></a><span data-ttu-id="955f0-128">另請參閱</span><span class="sxs-lookup"><span data-stu-id="955f0-128">See also</span></span>

[<span data-ttu-id="955f0-129">Microsoft Windows Imaging 編解碼器</span><span class="sxs-lookup"><span data-stu-id="955f0-129">Microsoft Windows Imaging Codec</span></span>](-wic-lh.md)

[<span data-ttu-id="955f0-130">程式設計手冊</span><span class="sxs-lookup"><span data-stu-id="955f0-130">Programming guide</span></span>](-wic-programming-guide.md)

[<span data-ttu-id="955f0-131">參考</span><span class="sxs-lookup"><span data-stu-id="955f0-131">Reference</span></span>](-wic-codec-reference.md)

[<span data-ttu-id="955f0-132">Direct2D</span><span class="sxs-lookup"><span data-stu-id="955f0-132">Direct2D</span></span>](../direct2d/direct2d-portal.md)

[<span data-ttu-id="955f0-133">範例和程式碼範例</span><span class="sxs-lookup"><span data-stu-id="955f0-133">Samples and code examples</span></span>](-wic-samples.md)
