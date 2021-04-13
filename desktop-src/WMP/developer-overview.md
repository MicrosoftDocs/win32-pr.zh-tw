---
title: 開發人員總覽
description: 開發人員總覽
ms.assetid: 72a330b4-5957-4159-b5e8-0c9a4491b589
keywords:
- Windows Media Player 外掛程式、視覺效果
- 外掛程式，視覺效果
- 視覺效果，開發人員總覽
- 自訂視覺效果，開發人員總覽
- 視覺效果、COM 控制項
- 自訂視覺效果，COM 控制項
- 視覺效果，音訊輸入
- 自訂視覺效果，音訊輸入
- 視覺效果，圖形化輸出
- 自訂視覺效果，圖形化輸出
- 視覺效果，繪圖工具
- 自訂視覺效果，繪圖工具
- 視覺效果，程式設計語言
- 自訂視覺效果，程式設計語言
- 視覺效果，Visual C++
- 自訂視覺效果，Visual C++
- 視覺效果，外掛程式 wizard
- 自訂視覺效果，外掛程式嚮導
- 外掛程式嚮導
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 36ec8632bd5611e081a4a17d1b0390dc99a09703
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104301436"
---
# <a name="developer-overview"></a><span data-ttu-id="27137-122">開發人員總覽</span><span class="sxs-lookup"><span data-stu-id="27137-122">Developer Overview</span></span>

<span data-ttu-id="27137-123">從開發人員的觀點來看，視覺效果是可取得 Windows Media Player 所提供之音訊資料的軟體程式，並將該資料轉換為可讓使用者注意的圖形。</span><span class="sxs-lookup"><span data-stu-id="27137-123">From the developer's point of view, visualizations are software programs that take audio data provided by Windows Media Player and convert that data to graphics that will please the eye of the user.</span></span> <span data-ttu-id="27137-124">開發人員必須瞭解才能建立新視覺效果的主要主題如下：</span><span class="sxs-lookup"><span data-stu-id="27137-124">The main subjects a developer needs to understand to create a new visualization are the following:</span></span>

## <a name="visualization-packaging"></a><span data-ttu-id="27137-125">視覺效果封裝</span><span class="sxs-lookup"><span data-stu-id="27137-125">Visualization Packaging</span></span>

<span data-ttu-id="27137-126">視覺效果是 Windows Media Player 用來在 Microsoft Windows 中將音訊波形轉換成動畫圖形的 COM 控制項。</span><span class="sxs-lookup"><span data-stu-id="27137-126">Visualizations are COM controls that Windows Media Player uses to turn audio waveforms into animated graphics in Microsoft Windows.</span></span> <span data-ttu-id="27137-127">COM 控制項會封裝成 Microsoft Windows 動態連結程式庫 (Dll) ，而且必須在 Windows 登錄中註冊。</span><span class="sxs-lookup"><span data-stu-id="27137-127">The COM controls are packaged as Microsoft Windows dynamic-link libraries (DLLs) and must be registered in the Windows registry.</span></span> <span data-ttu-id="27137-128">當 Windows Media Player 執行時，系統會根據 Windows Media Player 正在使用的面板指示載入和查看已註冊的自訂視覺效果。</span><span class="sxs-lookup"><span data-stu-id="27137-128">When Windows Media Player runs, registered custom visualizations are loaded and viewed in accordance with the instructions of the skin that Windows Media Player is using.</span></span>

## <a name="audio-input"></a><span data-ttu-id="27137-129">音訊輸入</span><span class="sxs-lookup"><span data-stu-id="27137-129">Audio Input</span></span>

<span data-ttu-id="27137-130">Windows Media Player 會在以秒為單位的時間間隔內，將音訊頻率和波形資料的快照集提供給您的程式碼。</span><span class="sxs-lookup"><span data-stu-id="27137-130">Windows Media Player provides your code with snapshots of audio frequency and waveform data at timed intervals measured in fractions of a second.</span></span> <span data-ttu-id="27137-131">快照間隔是由 Windows Media Player 在內部決定。</span><span class="sxs-lookup"><span data-stu-id="27137-131">The snapshot interval is internally determined by the Windows Media Player.</span></span>

## <a name="graphical-output"></a><span data-ttu-id="27137-132">圖形化輸出</span><span class="sxs-lookup"><span data-stu-id="27137-132">Graphical Output</span></span>

<span data-ttu-id="27137-133">視覺效果的圖形化輸出是 Microsoft Windows 裝置內容。</span><span class="sxs-lookup"><span data-stu-id="27137-133">The graphical output from your visualization is a Microsoft Windows device context.</span></span> <span data-ttu-id="27137-134">這是標準的 Windows 繪圖介面，可讓您在每次提供音訊快照集時繪製。</span><span class="sxs-lookup"><span data-stu-id="27137-134">This is a standard Windows drawing surface that you can draw upon every time an audio snapshot is provided.</span></span> <span data-ttu-id="27137-135">所有的背景 Windows 技術都是由您負責。</span><span class="sxs-lookup"><span data-stu-id="27137-135">All of the background Windows technology is taken care of for you.</span></span> <span data-ttu-id="27137-136">您只需要使用所提供的音訊資料來繪製裝置內容。</span><span class="sxs-lookup"><span data-stu-id="27137-136">You just have to draw on the device context with the audio data provided.</span></span>

## <a name="drawing-tools"></a><span data-ttu-id="27137-137">繪圖工具</span><span class="sxs-lookup"><span data-stu-id="27137-137">Drawing Tools</span></span>

<span data-ttu-id="27137-138">您可以使用標準的 Microsoft Windows 圖形裝置介面 (GDI) 函式來繪製裝置內容，方法是使用畫筆和筆刷來建立以 Windows Media Player 提供給您的音訊資料修改的設計。</span><span class="sxs-lookup"><span data-stu-id="27137-138">You can draw on the device context with standard Microsoft Windows Graphics Device Interface (GDI) functions, using pens and brushes to create designs that are modified by the audio data supplied to you by Windows Media Player.</span></span> <span data-ttu-id="27137-139">GDI 提供一組豐富的繪圖工具，可建立許多種類的視覺效果。</span><span class="sxs-lookup"><span data-stu-id="27137-139">GDI provides a rich set of drawing tools that can create many kinds of visual effects.</span></span>

## <a name="programming-language"></a><span data-ttu-id="27137-140">程式設計語言</span><span class="sxs-lookup"><span data-stu-id="27137-140">Programming Language</span></span>

<span data-ttu-id="27137-141">Microsoft Visual C++ 6.0 和更新版本是用來建立自訂視覺效果的唯一支援語言。</span><span class="sxs-lookup"><span data-stu-id="27137-141">Microsoft Visual C++ 6.0 and higher is the only supported language for creating custom visualizations.</span></span>

## <a name="plug-in-wizard"></a><span data-ttu-id="27137-142">外掛程式嚮導</span><span class="sxs-lookup"><span data-stu-id="27137-142">Plug-in Wizard</span></span>

<span data-ttu-id="27137-143">Windows Media Player 提供可讓您新增至 Visual C++ 的 COM wizard，以產生視覺效果所需的基礎程式碼。</span><span class="sxs-lookup"><span data-stu-id="27137-143">Windows Media Player provides a COM wizard that you can add to Visual C++ that will generate the underlying code needed for your visualization.</span></span> <span data-ttu-id="27137-144">不僅提供所有原始程式檔，還會產生範例面板，讓您輕鬆地測試視覺效果。</span><span class="sxs-lookup"><span data-stu-id="27137-144">Not only are all source files provided, but a sample skin is generated to make it easy to test your visualization.</span></span> <span data-ttu-id="27137-145">產生的程式碼會建立類似于橫條的視覺效果，並提供兩個預設值。</span><span class="sxs-lookup"><span data-stu-id="27137-145">The generated code creates a visualization similar to Bars, with two presets.</span></span> <span data-ttu-id="27137-146">然後您可以修改程式碼，以建立您自己的視覺效果。</span><span class="sxs-lookup"><span data-stu-id="27137-146">You can then modify the code to create your own visualization.</span></span> <span data-ttu-id="27137-147">也會產生登錄檔案來註冊您的視覺效果，讓 Windows Media Player 可以載入它。</span><span class="sxs-lookup"><span data-stu-id="27137-147">A registry file is also generated to register your visualization so that Windows Media Player can load it.</span></span>

<span data-ttu-id="27137-148">下列主題說明視覺效果程式碼處理音訊資料的方式：</span><span class="sxs-lookup"><span data-stu-id="27137-148">The following topic describes how visualization code processes audio data:</span></span>

-   [<span data-ttu-id="27137-149">控制流程</span><span class="sxs-lookup"><span data-stu-id="27137-149">Flow of Control</span></span>](flow-of-control.md)

## <a name="related-topics"></a><span data-ttu-id="27137-150">相關主題</span><span class="sxs-lookup"><span data-stu-id="27137-150">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="27137-151">**關於自訂視覺效果**</span><span class="sxs-lookup"><span data-stu-id="27137-151">**About Custom Visualizations**</span></span>](about-custom-visualizations.md)
</dt> </dl>

 

 




