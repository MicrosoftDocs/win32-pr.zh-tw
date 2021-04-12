---
title: Windows 動畫範例
description: 本節所包含的主題會提供支援 Windows 動畫管理員檔的程式碼範例詳細資料。
ms.assetid: 33b1770a-5acb-4ab5-999c-9663f4c075f0
keywords:
- Windows 動畫視窗動畫、範例
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2c2fe31e7fa12feab010bec3da710d4b2b80dd1d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104301700"
---
# <a name="windows-animation-samples"></a><span data-ttu-id="d0242-104">Windows 動畫範例</span><span class="sxs-lookup"><span data-stu-id="d0242-104">Windows Animation Samples</span></span>

<span data-ttu-id="d0242-105">本節所包含的主題會提供支援 Windows 動畫管理員檔的程式碼範例詳細資料。</span><span class="sxs-lookup"><span data-stu-id="d0242-105">The topics contained in this section provide details about the code samples that support the Windows Animation Manager documentation.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="d0242-106">本節內容</span><span class="sxs-lookup"><span data-stu-id="d0242-106">In this section</span></span>



| <span data-ttu-id="d0242-107">主題</span><span class="sxs-lookup"><span data-stu-id="d0242-107">Topic</span></span>                                                                                     | <span data-ttu-id="d0242-108">描述</span><span class="sxs-lookup"><span data-stu-id="d0242-108">Description</span></span>                                                                                                         |
|-------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="d0242-109">應用程式驅動的動畫範例</span><span class="sxs-lookup"><span data-stu-id="d0242-109">Application-Driven Animation Sample</span></span>](application-driven-animation-sample.md)<br/> |                                                                                                                     |
| [<span data-ttu-id="d0242-110">計時器驅動動畫範例</span><span class="sxs-lookup"><span data-stu-id="d0242-110">Timer-Driven Animation Sample</span></span>](timer-driven-animation-sample.md)<br/>             |                                                                                                                     |
| [<span data-ttu-id="d0242-111">自訂插即用範例</span><span class="sxs-lookup"><span data-stu-id="d0242-111">Custom Interpolator Sample</span></span>](custom-interpolator-sample.md)<br/>                   | <span data-ttu-id="d0242-112">示範如何搭配使用 Windows 動畫與您自己的自訂插即用來呈現 Direct2D。</span><span class="sxs-lookup"><span data-stu-id="d0242-112">Shows how to use Windows Animation with your own Custom Interpolator, with Direct2D used for rendering.</span></span> <br/> |
| [<span data-ttu-id="d0242-113">方格版面配置範例</span><span class="sxs-lookup"><span data-stu-id="d0242-113">Grid Layout Sample</span></span>](grid-layout-sample.md)<br/>                                   | <span data-ttu-id="d0242-114">示範如何使用 Direct2D 以動畫顯示影像的方格，以使用 Windows 動畫。</span><span class="sxs-lookup"><span data-stu-id="d0242-114">Shows how to use Windows Animation, using Direct2D to animate a grid of images.</span></span> <br/>                         |
| [<span data-ttu-id="d0242-115">優先順序比較範例</span><span class="sxs-lookup"><span data-stu-id="d0242-115">Priority Comparison Sample</span></span>](priority-comparison-sample.md)<br/>                   | <span data-ttu-id="d0242-116">示範如何使用 Direct2D 轉譯來搭配使用 Windows 動畫與您自己的優先順序比較。</span><span class="sxs-lookup"><span data-stu-id="d0242-116">Shows how to use Windows Animation with your own Priority Comparison, using Direct2D for rendering.</span></span><br/>      |



 

## <a name="sample-files"></a><span data-ttu-id="d0242-117">範例檔案</span><span class="sxs-lookup"><span data-stu-id="d0242-117">Sample Files</span></span>

<span data-ttu-id="d0242-118">每個範例都包含下列許多金鑰檔：</span><span class="sxs-lookup"><span data-stu-id="d0242-118">Each sample contains many of the following key files:</span></span>

<dl> <dt>

<span data-ttu-id="d0242-119"><span id="Application.cpp"></span><span id="application.cpp"></span><span id="APPLICATION.CPP"></span>應用程式 .cpp</span><span class="sxs-lookup"><span data-stu-id="d0242-119"><span id="Application.cpp"></span><span id="application.cpp"></span><span id="APPLICATION.CPP"></span>Application.cpp</span></span>
</dt> <dd>

<span data-ttu-id="d0242-120">定義應用程式進入點。</span><span class="sxs-lookup"><span data-stu-id="d0242-120">Defines the application entry point.</span></span>

</dd> <dt>

<span data-ttu-id="d0242-121"><span id="MainWindow.h"></span><span id="mainwindow.h"></span><span id="MAINWINDOW.H"></span>MainWindow。h</span><span class="sxs-lookup"><span data-stu-id="d0242-121"><span id="MainWindow.h"></span><span id="mainwindow.h"></span><span id="MAINWINDOW.H"></span>MainWindow.h</span></span>
</dt> <dd>

<span data-ttu-id="d0242-122">宣告 CMainWindow 類別。</span><span class="sxs-lookup"><span data-stu-id="d0242-122">Declares the CMainWindow class.</span></span>

</dd> <dt>

<span data-ttu-id="d0242-123"><span id="MainWindow.cpp"></span><span id="mainwindow.cpp"></span><span id="MAINWINDOW.CPP"></span>MainWindow .cpp</span><span class="sxs-lookup"><span data-stu-id="d0242-123"><span id="MainWindow.cpp"></span><span id="mainwindow.cpp"></span><span id="MAINWINDOW.CPP"></span>MainWindow.cpp</span></span>
</dt> <dd>

<span data-ttu-id="d0242-124">初始化動畫元件和圖形平台、載入影像，以及呈現工作區。</span><span class="sxs-lookup"><span data-stu-id="d0242-124">Initializes the animation components and the graphics platform, loads images, and renders the client area.</span></span>

</dd> <dt>

<span data-ttu-id="d0242-125"><span id="LayoutManager.h"></span><span id="layoutmanager.h"></span><span id="LAYOUTMANAGER.H"></span>LayoutManager。h</span><span class="sxs-lookup"><span data-stu-id="d0242-125"><span id="LayoutManager.h"></span><span id="layoutmanager.h"></span><span id="LAYOUTMANAGER.H"></span>LayoutManager.h</span></span>
</dt> <dd>

<span data-ttu-id="d0242-126">宣告 CLayoutManager 類別。</span><span class="sxs-lookup"><span data-stu-id="d0242-126">Declares the CLayoutManager class.</span></span>

</dd> <dt>

<span data-ttu-id="d0242-127"><span id="LayoutManager.cpp"></span><span id="layoutmanager.cpp"></span><span id="LAYOUTMANAGER.CPP"></span>LayoutManager .cpp</span><span class="sxs-lookup"><span data-stu-id="d0242-127"><span id="LayoutManager.cpp"></span><span id="layoutmanager.cpp"></span><span id="LAYOUTMANAGER.CPP"></span>LayoutManager.cpp</span></span>
</dt> <dd>

<span data-ttu-id="d0242-128">在主視窗中計算影像的版面配置、建立分鏡腳本、將轉換新增至分鏡腳本，以及排定分鏡腳本。</span><span class="sxs-lookup"><span data-stu-id="d0242-128">Calculates the layout of images in the main window, creates storyboards, adds transitions to the storyboard, and schedules the storyboard.</span></span>

</dd> <dt>

<span data-ttu-id="d0242-129"><span id="Thumbnail.h"></span><span id="thumbnail.h"></span><span id="THUMBNAIL.H"></span>縮圖。h</span><span class="sxs-lookup"><span data-stu-id="d0242-129"><span id="Thumbnail.h"></span><span id="thumbnail.h"></span><span id="THUMBNAIL.H"></span>Thumbnail.h</span></span>
</dt> <dd>

<span data-ttu-id="d0242-130">宣告 CThumbNail 類別。</span><span class="sxs-lookup"><span data-stu-id="d0242-130">Declares the CThumbNail class.</span></span>

</dd> <dt>

<span data-ttu-id="d0242-131"><span id="Thumbnail.cpp"></span><span id="thumbnail.cpp"></span><span id="THUMBNAIL.CPP"></span>縮圖 .cpp</span><span class="sxs-lookup"><span data-stu-id="d0242-131"><span id="Thumbnail.cpp"></span><span id="thumbnail.cpp"></span><span id="THUMBNAIL.CPP"></span>Thumbnail.cpp</span></span>
</dt> <dd>

<span data-ttu-id="d0242-132">建立動畫變數並呈現縮圖。</span><span class="sxs-lookup"><span data-stu-id="d0242-132">Creates animation variables and renders thumbnails.</span></span>

</dd> </dl>

## <a name="related-topics"></a><span data-ttu-id="d0242-133">相關主題</span><span class="sxs-lookup"><span data-stu-id="d0242-133">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d0242-134">Windows 動畫開發指南</span><span class="sxs-lookup"><span data-stu-id="d0242-134">Windows Animation Development Guide</span></span>](windows-animation-developer-guide.md)
</dt> <dt>

[<span data-ttu-id="d0242-135">Windows 動畫參考</span><span class="sxs-lookup"><span data-stu-id="d0242-135">Windows Animation Reference</span></span>](windows-animation-reference.md)
</dt> </dl>

 

 





