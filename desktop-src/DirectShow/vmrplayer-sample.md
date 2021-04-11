---
description: VMRPlayer 範例
ms.assetid: 7fc893a6-afa5-4ada-9295-29122b43b21e
title: VMRPlayer 範例
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e2214d94628a90daf0dd543f4e3a7f0166f4968a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103848431"
---
# <a name="vmrplayer-sample"></a><span data-ttu-id="3cb57-103">VMRPlayer 範例</span><span class="sxs-lookup"><span data-stu-id="3cb57-103">VMRPlayer Sample</span></span>

## <a name="description"></a><span data-ttu-id="3cb57-104">Description</span><span class="sxs-lookup"><span data-stu-id="3cb57-104">Description</span></span>

<span data-ttu-id="3cb57-105">此範例使用影片混合轉譯器 9 (VMR-9) 篩選至 Alpha blend 一或兩個執行中的影片和靜態影像。</span><span class="sxs-lookup"><span data-stu-id="3cb57-105">This sample uses the Video Mixing Renderer 9 (VMR-9) filter to alpha blend one or two running videos and a static image.</span></span>

## <a name="usage"></a><span data-ttu-id="3cb57-106">使用方式</span><span class="sxs-lookup"><span data-stu-id="3cb57-106">Usage</span></span>

<span data-ttu-id="3cb57-107">若要開啟第一部影片，請從 [檔案 **] 功能表中選擇 [** **開啟主要資料流程**]。</span><span class="sxs-lookup"><span data-stu-id="3cb57-107">To open the first video, choose **Open Primary Stream** from the **File** menu.</span></span> <span data-ttu-id="3cb57-108">若要開啟第二部影片，請從 [檔案 **] 功能表中選擇 [** **開啟次要資料流程**] (您必須先) 開啟主要串流。</span><span class="sxs-lookup"><span data-stu-id="3cb57-108">To open a second video, choose **Open Secondary Stream** from the **File** menu (you must open the primary stream first).</span></span> <span data-ttu-id="3cb57-109">若要播放影片，請按一下 [ **播放** ] 按鈕。</span><span class="sxs-lookup"><span data-stu-id="3cb57-109">To play the video, click the **Play** button.</span></span>

<span data-ttu-id="3cb57-110">您可以從 [ **VMR 屬性**] 功能表中選取 [**主要資料流程**] 或 [ **Secondard 資料流程**]，以設定影片的位置、大小和 Alpha 值。</span><span class="sxs-lookup"><span data-stu-id="3cb57-110">You can set the position, size, and alpha values of the videos by selecting **Primary Stream** or **Secondard Stream** from the **VMR Properties** menu.</span></span>

<span data-ttu-id="3cb57-111">若要在影片上新增靜態點陣圖，請從 [ **VMR 屬性**] 功能表選擇 [**靜態應用程式映射**]，然後按一下 [**顯示應用程式影像**] 方塊。</span><span class="sxs-lookup"><span data-stu-id="3cb57-111">To add a static bitmap over the video, choose **Static App Image** from the **VMR Properties** menu and click the **Display App Image** box.</span></span> <span data-ttu-id="3cb57-112">您可以使用相同的對話方塊來控制點陣圖的位置、大小和 Alpha 值。</span><span class="sxs-lookup"><span data-stu-id="3cb57-112">You can use the same dialog to control the position, size, and alpha value of the bitmap.</span></span>

<span data-ttu-id="3cb57-113">若要捕獲混合的影片影像，請從 [ **VMR 屬性**] 功能表選擇 [**捕捉點陣圖影像**]。</span><span class="sxs-lookup"><span data-stu-id="3cb57-113">To capture the blended video image, choose **Capture Bitmap Image** from the **VMR Properties** menu.</span></span>

<span data-ttu-id="3cb57-114">您也可以從命令列指定主要映射資料流程：</span><span class="sxs-lookup"><span data-stu-id="3cb57-114">You can also specify the primary image stream from the command line:</span></span>

<span data-ttu-id="3cb57-115">**VMRPlayer** **/p** *檔案名*</span><span class="sxs-lookup"><span data-stu-id="3cb57-115">**VMRPlayer** **/P** *filename*</span></span>

## <a name="downloading-the-sample"></a><span data-ttu-id="3cb57-116">下載範例</span><span class="sxs-lookup"><span data-stu-id="3cb57-116">Downloading the Sample</span></span>

<span data-ttu-id="3cb57-117">若要下載 DirectShow SDK 範例，請安裝最新版本的 [Windows SDK](https://msdn.microsoft.com/windowsvista/bb980924.aspx)。</span><span class="sxs-lookup"><span data-stu-id="3cb57-117">To download the DirectShow SDK samples, install the latest version of the [Windows SDK](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span>

## <a name="related-topics"></a><span data-ttu-id="3cb57-118">相關主題</span><span class="sxs-lookup"><span data-stu-id="3cb57-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3cb57-119">DirectShow 範例</span><span class="sxs-lookup"><span data-stu-id="3cb57-119">DirectShow Samples</span></span>](directshow-samples.md)
</dt> </dl>

 

 



