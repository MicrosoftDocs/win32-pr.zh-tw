---
description: 這個範例示範如何使用 Windows 影像處理元件 (WIC) 來解碼以漸進式層級編碼的影像。
ms.assetid: 14018dce-26f0-4e1e-9d19-c5b42dd2cdab
title: WIC 漸進解碼範例
ms.topic: article
ms.date: 03/19/2021
ms.custom: project-verbatim
ms.openlocfilehash: 2e4b1fc560af0ee8c817208fec628ddb068676bb
ms.sourcegitcommit: af120ad5c30da2fc5eb717ca2a1c4c45878efd71
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/20/2021
ms.locfileid: "106997436"
---
# <a name="wic-progressive-decoding-sample"></a><span data-ttu-id="0fbb8-103">WIC 漸進解碼範例</span><span class="sxs-lookup"><span data-stu-id="0fbb8-103">WIC progressive decoding sample</span></span>

<span data-ttu-id="0fbb8-104">這個範例示範如何使用 Windows 影像處理元件 (WIC) 來解碼以漸進式層級編碼的影像。</span><span class="sxs-lookup"><span data-stu-id="0fbb8-104">This sample demonstrates the use of Windows Imaging Component (WIC) to decode an image that is encoded with progressive levels.</span></span> <span data-ttu-id="0fbb8-105">這個範例會使用 Direct2D，將不同的漸進層級轉譯至螢幕。</span><span class="sxs-lookup"><span data-stu-id="0fbb8-105">This sample uses Direct2D to render the different progressive levels to the screen.</span></span>

## <a name="requirements"></a><span data-ttu-id="0fbb8-106">規格需求</span><span class="sxs-lookup"><span data-stu-id="0fbb8-106">Requirements</span></span>

<span data-ttu-id="0fbb8-107">此範例具有下列需求。</span><span class="sxs-lookup"><span data-stu-id="0fbb8-107">This sample has the following requirements.</span></span>

| <span data-ttu-id="0fbb8-108">需求</span><span class="sxs-lookup"><span data-stu-id="0fbb8-108">Requirement</span></span> | <span data-ttu-id="0fbb8-109">值</span><span class="sxs-lookup"><span data-stu-id="0fbb8-109">Value</span></span> |
|-|
| <span data-ttu-id="0fbb8-110">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="0fbb8-110">Minimum supported client</span></span> | <span data-ttu-id="0fbb8-111">Windows 7</span><span class="sxs-lookup"><span data-stu-id="0fbb8-111">Windows 7</span></span> |
| <span data-ttu-id="0fbb8-112">最小 Windows SDK</span><span class="sxs-lookup"><span data-stu-id="0fbb8-112">Minimum Windows SDK</span></span> | <span data-ttu-id="0fbb8-113">適用于 Windows 7 的[Windows 軟體開發套件 (SDK) ](https://msdn.microsoft.com/windowsvista/bb980924.aspx)</span><span class="sxs-lookup"><span data-stu-id="0fbb8-113">[Windows Software Development Kit (SDK)](https://msdn.microsoft.com/windowsvista/bb980924.aspx) for Windows 7</span></span> |

## <a name="downloading-the-sample"></a><span data-ttu-id="0fbb8-114">下載範例</span><span class="sxs-lookup"><span data-stu-id="0fbb8-114">Downloading the sample</span></span>

<span data-ttu-id="0fbb8-115">此範例可在 [WIC 漸進編碼](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/multimedia/wic/progressivedecoding)中取得。</span><span class="sxs-lookup"><span data-stu-id="0fbb8-115">This sample is available at [WIC progressive encoding](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/multimedia/wic/progressivedecoding).</span></span>

## <a name="building-the-sample"></a><span data-ttu-id="0fbb8-116">建置範例</span><span class="sxs-lookup"><span data-stu-id="0fbb8-116">Building the sample</span></span>

### <a name="using-visual-studio-preferred-method"></a><span data-ttu-id="0fbb8-117">使用 Visual Studio (慣用方法) </span><span class="sxs-lookup"><span data-stu-id="0fbb8-117">Using Visual Studio (preferred method)</span></span>

1. <span data-ttu-id="0fbb8-118">開啟 Windows 檔案總管，巡覽至目錄。</span><span class="sxs-lookup"><span data-stu-id="0fbb8-118">Open Windows Explorer and navigate to the directory.</span></span>
2. <span data-ttu-id="0fbb8-119">按兩下 .sln (方案的圖示) 檔案，在 Visual Studio 中開啟檔案。</span><span class="sxs-lookup"><span data-stu-id="0fbb8-119">Double-click the icon for the .sln (solution) file to open the file in Visual Studio.</span></span>
3. <span data-ttu-id="0fbb8-120">在 [建置] 功能表中，選取 [建置方案]。</span><span class="sxs-lookup"><span data-stu-id="0fbb8-120">In the Build menu, select Build Solution.</span></span> <span data-ttu-id="0fbb8-121">應用程式將會建立在預設的 \\ Debug 或 \\ Release 目錄中。</span><span class="sxs-lookup"><span data-stu-id="0fbb8-121">The application will be built in the default \\Debug or \\Release directory.</span></span>

### <a name="using-the-command-prompt"></a><span data-ttu-id="0fbb8-122">使用命令提示字元</span><span class="sxs-lookup"><span data-stu-id="0fbb8-122">Using the command prompt</span></span>

<span data-ttu-id="0fbb8-123">使用命令提示字元建立範例。</span><span class="sxs-lookup"><span data-stu-id="0fbb8-123">To build the sample using the command prompt.</span></span>

1. <span data-ttu-id="0fbb8-124">開啟命令提示字元，然後流覽至範例目錄。</span><span class="sxs-lookup"><span data-stu-id="0fbb8-124">Open the command prompt and navigate to the sample directory.</span></span>
2. <span data-ttu-id="0fbb8-125">輸入 `msbuild WICProgressiveDecoding.sln`</span><span class="sxs-lookup"><span data-stu-id="0fbb8-125">Type `msbuild WICProgressiveDecoding.sln`</span></span>

## <a name="running-the-sample"></a><span data-ttu-id="0fbb8-126">執行範例</span><span class="sxs-lookup"><span data-stu-id="0fbb8-126">Running the sample</span></span>

<span data-ttu-id="0fbb8-127">應用程式啟動之後，透過 [開啟] 功能表載入影像檔案。</span><span class="sxs-lookup"><span data-stu-id="0fbb8-127">After the application is launched, load an image file through file open menu.</span></span> <span data-ttu-id="0fbb8-128">載入時，預設漸進式層級會設定為0。</span><span class="sxs-lookup"><span data-stu-id="0fbb8-128">On loading, the default progressive level is set to 0.</span></span> <span data-ttu-id="0fbb8-129">您可以透過功能表或向上/向下鍵來流覽至不同的漸進式層級。</span><span class="sxs-lookup"><span data-stu-id="0fbb8-129">You can navigate to different progressive levels either through menu or Up/Down key.</span></span> <span data-ttu-id="0fbb8-130">目前的漸進式層級文字會顯示在主視窗狀態列上。</span><span class="sxs-lookup"><span data-stu-id="0fbb8-130">The current progressive level text is displayed on the main window status bar.</span></span> <span data-ttu-id="0fbb8-131">支援視窗調整大小。</span><span class="sxs-lookup"><span data-stu-id="0fbb8-131">Window resizing is supported.</span></span>

> [!NOTE]
> <span data-ttu-id="0fbb8-132">漸進式解碼只適用于已逐漸編碼的影像。</span><span class="sxs-lookup"><span data-stu-id="0fbb8-132">Progressive decoding is available only for images that have been progressively encoded.</span></span> <span data-ttu-id="0fbb8-133">此範例所提供的映射已逐漸編碼。</span><span class="sxs-lookup"><span data-stu-id="0fbb8-133">The image provided with this sample has been progressively encoded.</span></span>

## <a name="see-also"></a><span data-ttu-id="0fbb8-134">另請參閱</span><span class="sxs-lookup"><span data-stu-id="0fbb8-134">See also</span></span>

[<span data-ttu-id="0fbb8-135">Microsoft Windows Imaging 編解碼器</span><span class="sxs-lookup"><span data-stu-id="0fbb8-135">Microsoft Windows Imaging Codec</span></span>](-wic-lh.md)

[<span data-ttu-id="0fbb8-136">程式設計手冊</span><span class="sxs-lookup"><span data-stu-id="0fbb8-136">Programming guide</span></span>](-wic-programming-guide.md)

[<span data-ttu-id="0fbb8-137">參考</span><span class="sxs-lookup"><span data-stu-id="0fbb8-137">Reference</span></span>](-wic-codec-reference.md)

[<span data-ttu-id="0fbb8-138">Direct2D</span><span class="sxs-lookup"><span data-stu-id="0fbb8-138">Direct2D</span></span>](../direct2d/direct2d-portal.md)

[<span data-ttu-id="0fbb8-139">範例和程式碼範例</span><span class="sxs-lookup"><span data-stu-id="0fbb8-139">Samples and code examples</span></span>](-wic-samples.md)

[<span data-ttu-id="0fbb8-140">漸進式解碼總覽</span><span class="sxs-lookup"><span data-stu-id="0fbb8-140">Progressive decoding overview</span></span>](-wic-progressive-decoding.md)
