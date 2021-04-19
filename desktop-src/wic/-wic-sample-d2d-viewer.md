---
description: 這個範例示範如何使用 Windows 影像處理元件 (WIC) 來解碼影像檔案，以及 Direct2D 將影像轉譯至螢幕。
ms.assetid: 4f989ff6-b513-4354-a1bb-8d9521f693a2
title: 使用 Direct2D 範例的 WIC 影像檢視器
ms.topic: article
ms.date: 03/19/2021
ms.custom: project-verbatim
ms.openlocfilehash: a18bf17e7f43d3c4ad935bae9f8ed42e7b48db01
ms.sourcegitcommit: af120ad5c30da2fc5eb717ca2a1c4c45878efd71
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/20/2021
ms.locfileid: "106999063"
---
# <a name="wic-image-viewer-using-direct2d-sample"></a><span data-ttu-id="a7445-103">使用 Direct2D 範例的 WIC 影像檢視器</span><span class="sxs-lookup"><span data-stu-id="a7445-103">WIC image viewer using Direct2D sample</span></span>

<span data-ttu-id="a7445-104">此範例示範如何使用 Windows 影像處理元件 (WIC) 來解碼影像檔案，並 Direct2D 以將影像轉譯至螢幕。</span><span class="sxs-lookup"><span data-stu-id="a7445-104">This sample demonstrates the use of Windows Imaging Component (WIC) to decode an image file and Direct2D to render the image to the screen.</span></span>

## <a name="requirements"></a><span data-ttu-id="a7445-105">規格需求</span><span class="sxs-lookup"><span data-stu-id="a7445-105">Requirements</span></span>

<span data-ttu-id="a7445-106">此範例具有下列需求。</span><span class="sxs-lookup"><span data-stu-id="a7445-106">This sample has the following requirements.</span></span>

| <span data-ttu-id="a7445-107">需求</span><span class="sxs-lookup"><span data-stu-id="a7445-107">Requirement</span></span> | <span data-ttu-id="a7445-108">值</span><span class="sxs-lookup"><span data-stu-id="a7445-108">Value</span></span> |
|-|-|
| <span data-ttu-id="a7445-109">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="a7445-109">Minimum supported client</span></span> | <span data-ttu-id="a7445-110">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="a7445-110">Windows Vista</span></span> |
| <span data-ttu-id="a7445-111">最小 Windows SDK</span><span class="sxs-lookup"><span data-stu-id="a7445-111">Minimum Windows SDK</span></span> | <span data-ttu-id="a7445-112">適用于 Windows 7 的[Windows 軟體開發套件 (SDK) ](https://msdn.microsoft.com/windowsvista/bb980924.aspx)</span><span class="sxs-lookup"><span data-stu-id="a7445-112">[Windows Software Development Kit (SDK)](https://msdn.microsoft.com/windowsvista/bb980924.aspx) for Windows 7</span></span> |

## <a name="downloading-the-sample"></a><span data-ttu-id="a7445-113">下載範例</span><span class="sxs-lookup"><span data-stu-id="a7445-113">Downloading the sample</span></span>

<span data-ttu-id="a7445-114">您可以在 [WIC 檢視器 D2D](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/multimedia/wic/wicviewerd2d)取得此範例。</span><span class="sxs-lookup"><span data-stu-id="a7445-114">This sample is available at [WIC Viewer D2D](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/multimedia/wic/wicviewerd2d).</span></span>

## <a name="building-the-sample"></a><span data-ttu-id="a7445-115">建置範例</span><span class="sxs-lookup"><span data-stu-id="a7445-115">Building the sample</span></span>

### <a name="using-visual-studio-preferred-method"></a><span data-ttu-id="a7445-116">使用 Visual Studio (慣用方法) </span><span class="sxs-lookup"><span data-stu-id="a7445-116">Using Visual Studio (preferred method)</span></span>

1. <span data-ttu-id="a7445-117">開啟 Windows 檔案總管，巡覽至目錄。</span><span class="sxs-lookup"><span data-stu-id="a7445-117">Open Windows Explorer and navigate to the directory.</span></span>
2. <span data-ttu-id="a7445-118">按兩下 .sln (方案的圖示) 檔案，在 Visual Studio 中開啟檔案。</span><span class="sxs-lookup"><span data-stu-id="a7445-118">Double-click the icon for the .sln (solution) file to open the file in Visual Studio.</span></span>
3. <span data-ttu-id="a7445-119">在 [建置] 功能表中，選取 [建置方案]。</span><span class="sxs-lookup"><span data-stu-id="a7445-119">In the **Build** menu, select **Build Solution**.</span></span> <span data-ttu-id="a7445-120">應用程式將會建立在預設的 \\ Debug 或 \\ Release 目錄中。</span><span class="sxs-lookup"><span data-stu-id="a7445-120">The application will be built in the default \\Debug or \\Release directory.</span></span>

### <a name="using-the-command-prompt"></a><span data-ttu-id="a7445-121">使用命令提示字元</span><span class="sxs-lookup"><span data-stu-id="a7445-121">Using the command prompt</span></span>

<span data-ttu-id="a7445-122">若要使用命令提示字元建立範例：</span><span class="sxs-lookup"><span data-stu-id="a7445-122">To build the sample by using a command prompt:</span></span>

1. <span data-ttu-id="a7445-123">開啟 [命令提示字元] 視窗，並流覽至範例目錄。</span><span class="sxs-lookup"><span data-stu-id="a7445-123">Open a command prompt window and navigate to the sample directory.</span></span>
2. <span data-ttu-id="a7445-124">輸入 `msbuild WICViewerD2D.sln`</span><span class="sxs-lookup"><span data-stu-id="a7445-124">Type `msbuild WICViewerD2D.sln`</span></span>

## <a name="running-the-sample"></a><span data-ttu-id="a7445-125">執行範例</span><span class="sxs-lookup"><span data-stu-id="a7445-125">Running the sample</span></span>

<span data-ttu-id="a7445-126">當您啟動應用程式之後，請使用 [檔案 **] 功能表的 [** **開啟**] 命令載入影像檔案。</span><span class="sxs-lookup"><span data-stu-id="a7445-126">After you start the application, load an image file by using the **Open** command of the **File** menu.</span></span>

## <a name="see-also"></a><span data-ttu-id="a7445-127">另請參閱</span><span class="sxs-lookup"><span data-stu-id="a7445-127">See also</span></span>

[<span data-ttu-id="a7445-128">Microsoft Windows Imaging 編解碼器</span><span class="sxs-lookup"><span data-stu-id="a7445-128">Microsoft Windows Imaging Codec</span></span>](-wic-lh.md)

[<span data-ttu-id="a7445-129">程式設計手冊</span><span class="sxs-lookup"><span data-stu-id="a7445-129">Programming guide</span></span>](-wic-programming-guide.md)

[<span data-ttu-id="a7445-130">參考</span><span class="sxs-lookup"><span data-stu-id="a7445-130">Reference</span></span>](-wic-codec-reference.md)

[<span data-ttu-id="a7445-131">Direct2D</span><span class="sxs-lookup"><span data-stu-id="a7445-131">Direct2D</span></span>](../direct2d/direct2d-portal.md)

[<span data-ttu-id="a7445-132">範例和程式碼範例</span><span class="sxs-lookup"><span data-stu-id="a7445-132">Samples and code examples</span></span>](-wic-samples.md)
