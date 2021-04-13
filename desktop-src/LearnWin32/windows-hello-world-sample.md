---
title: Windows Hello World 範例
description: 這個範例應用程式說明如何建立基本的 Windows 程式。
ms.assetid: ec316ad8-d01d-4558-91b6-19fdbba3d520
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e932d3b0c524c643022904b08402507d4a603adb
ms.sourcegitcommit: e084958628fb997e9e11fe08574d82edbba07dbf
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/09/2019
ms.locfileid: "104311673"
---
# <a name="windows-hello-world-sample"></a><span data-ttu-id="a8b22-103">Windows Hello World 範例</span><span class="sxs-lookup"><span data-stu-id="a8b22-103">Windows Hello World Sample</span></span>

<span data-ttu-id="a8b22-104">這個範例應用程式說明如何建立基本的 Windows 程式。</span><span class="sxs-lookup"><span data-stu-id="a8b22-104">This sample application shows how to create a minimal Windows program.</span></span>

## <a name="description"></a><span data-ttu-id="a8b22-105">Description</span><span class="sxs-lookup"><span data-stu-id="a8b22-105">Description</span></span>

<span data-ttu-id="a8b22-106">Windows Hello World 範例應用程式會建立並顯示空白視窗，如下列螢幕擷取畫面所示。</span><span class="sxs-lookup"><span data-stu-id="a8b22-106">The Windows Hello World sample application creates and shows an empty window, as shown in the screen shot that follows.</span></span> <span data-ttu-id="a8b22-107">課程模組1會討論此範例 [。您的第一個 Windows 程式](your-first-windows-program.md)。</span><span class="sxs-lookup"><span data-stu-id="a8b22-107">This sample is discussed in [Module 1. Your First Windows Program](your-first-windows-program.md).</span></span>

![範例程式的螢幕擷取畫面。](images/window01.png)

## <a name="downloading-the-sample"></a><span data-ttu-id="a8b22-109">下載範例</span><span class="sxs-lookup"><span data-stu-id="a8b22-109">Downloading the Sample</span></span>

<span data-ttu-id="a8b22-110">此範例可在 [這裡](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/begin/LearnWin32/HelloWorld)取得。</span><span class="sxs-lookup"><span data-stu-id="a8b22-110">This sample is available [here](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/begin/LearnWin32/HelloWorld).</span></span>

<span data-ttu-id="a8b22-111">若要下載，請移至 GitHub 上範例存放庫的根目錄 ([microsoft/Windows-傳統範例](https://github.com/microsoft/Windows-classic-samples/)) 然後按一下 [ **複製] 或 [下載** ] 按鈕，將所有範例的 zip 檔案下載到您的電腦。</span><span class="sxs-lookup"><span data-stu-id="a8b22-111">To download it, go to the root of the sample repo on GitHub ([microsoft/Windows-classic-samples](https://github.com/microsoft/Windows-classic-samples/)) and click the **Clone or download** button to download the zip file of all the samples to your computer.</span></span> <span data-ttu-id="a8b22-112">然後將資料夾解壓縮。</span><span class="sxs-lookup"><span data-stu-id="a8b22-112">Then unzip the folder.</span></span>

<span data-ttu-id="a8b22-113">若要在 Visual Studio 中開啟範例，請選取 [檔案] **/[開啟/專案/方案**]，然後流覽至您解壓縮資料夾的位置和 **Windows-傳統-範例-master/sample/Win7Samples/begin/LearnWin32/HelloWorld/cpp**。</span><span class="sxs-lookup"><span data-stu-id="a8b22-113">To open the sample in Visual Studio, select **File / Open / Project/Solution**, and navigate to the location you unzipped the folder and **Windows-classic-samples-master / Samples / Win7Samples / begin / LearnWin32 / HelloWorld / cpp**.</span></span> <span data-ttu-id="a8b22-114">開啟 **HelloWorld** 檔案。</span><span class="sxs-lookup"><span data-stu-id="a8b22-114">Open the file **HelloWorld.sln**.</span></span>

<span data-ttu-id="a8b22-115">載入範例之後，您必須將其更新為使用 Windows 10。</span><span class="sxs-lookup"><span data-stu-id="a8b22-115">Once the sample has loaded, you will need to update it to work with Windows 10.</span></span> <span data-ttu-id="a8b22-116">從 Visual Studio 的 [ **專案** ] 功能表中選取 [ **屬性**]。</span><span class="sxs-lookup"><span data-stu-id="a8b22-116">From the **Project** menu in Visual Studio, select **Properties**.</span></span> <span data-ttu-id="a8b22-117">將 **Windows SDK 版本** 更新為 Windows 10 SDK （例如10.0.17763.0 或更好的版本）。</span><span class="sxs-lookup"><span data-stu-id="a8b22-117">Update the **Windows SDK Version** to a Windows 10 SDK, such as 10.0.17763.0 or better.</span></span> <span data-ttu-id="a8b22-118">然後將 **平臺工具** 組變更為 Visual Studio 2017 或更好。</span><span class="sxs-lookup"><span data-stu-id="a8b22-118">Then change **Platform Toolset** to Visual Studio 2017 or better.</span></span> <span data-ttu-id="a8b22-119">現在您可以按 F5 來執行範例！</span><span class="sxs-lookup"><span data-stu-id="a8b22-119">Now you can run the sample by pressing F5!</span></span>


## <a name="related-topics"></a><span data-ttu-id="a8b22-120">相關主題</span><span class="sxs-lookup"><span data-stu-id="a8b22-120">Related topics</span></span>

* [<span data-ttu-id="a8b22-121">學習如何撰寫 Windows 程式：範例程式碼</span><span class="sxs-lookup"><span data-stu-id="a8b22-121">Learn to Program for Windows: Sample Code</span></span>](learn-to-program-for-windows--sample-code.md)
* [<span data-ttu-id="a8b22-122">模組1。您的第一個 Windows 程式</span><span class="sxs-lookup"><span data-stu-id="a8b22-122">Module 1. Your First Windows Program</span></span>](your-first-windows-program.md)
