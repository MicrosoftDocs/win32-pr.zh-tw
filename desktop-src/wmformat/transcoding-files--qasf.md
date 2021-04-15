---
title: '轉碼檔案 (QASF) '
description: '轉碼檔案 (QASF) '
ms.assetid: c6dad6cf-4781-4204-883b-cdb33aff5e27
keywords:
- 'Windows Media Format SDK、轉碼檔案 (QASF) '
- Windows Media Format SDK、DirectShow
- 'Advanced Systems Format (ASF) 、轉碼檔案 (QASF) '
- 'ASF (Advanced Systems Format) 、轉碼檔案 (QASF) '
- Advanced Systems Format (ASF) 、DirectShow
- ASF (Advanced Systems Format) ，DirectShow
- 'DirectShow、轉碼檔案 (QASF) '
- Windows Media Format SDK、QASF
- Advanced Systems Format (ASF) ，QASF
- ASF (Advanced Systems Format) ，QASF
- DirectShow、QASF
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 14387a65538d411bcd41b4b907f2adbab2089f71
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104568202"
---
# <a name="transcoding-files-qasf"></a><span data-ttu-id="2e999-114">轉碼檔案 (QASF) </span><span class="sxs-lookup"><span data-stu-id="2e999-114">Transcoding Files (QASF)</span></span>

<span data-ttu-id="2e999-115">您可以透過各種方式使用 [WM ASF 寫入器](wm-asf-writer-filter.md) 來建立檔案轉碼篩選圖形。</span><span class="sxs-lookup"><span data-stu-id="2e999-115">You can build a file-transcoding filter graph using the [WM ASF Writer](wm-asf-writer-filter.md) in various ways.</span></span> <span data-ttu-id="2e999-116">最簡單的方式是將 WM ASF 寫入器共同建立、設定和新增至篩選圖形，然後使用 **IGraphBuilder：： RenderFile** 方法自動建立圖形。</span><span class="sxs-lookup"><span data-stu-id="2e999-116">The easiest way is to co-create, configure, and add the WM ASF Writer to the filter graph, and then use the **IGraphBuilder::RenderFile** method to build the graph automatically.</span></span>

<span data-ttu-id="2e999-117">另一種方式是將每個篩選手動新增至圖形並連接釘選。</span><span class="sxs-lookup"><span data-stu-id="2e999-117">An alternative way is to add each filter manually to the graph and connect the pins.</span></span> <span data-ttu-id="2e999-118">新增 WM ASF 寫入器之後，如果預設設定檔不適用，請使用 **IConfigAsfWriter** 方法進行設定，並將 WM ASF 寫入器輸入接點連接到上游篩選器上對應的輸出圖釘。</span><span class="sxs-lookup"><span data-stu-id="2e999-118">After adding the WM ASF Writer, configure it by using the **IConfigAsfWriter** methods if the default profile is not suitable, and connect the WM ASF Writer input pins to the corresponding output pins on the upstream filters.</span></span>

<span data-ttu-id="2e999-119">下圖顯示典型的 WM ASF 寫入器轉碼篩選圖形設定。</span><span class="sxs-lookup"><span data-stu-id="2e999-119">The following illustration shows typical WM ASF Writer transcoding filter graph configurations.</span></span>

![一般轉碼篩選圖形](images/asf-transcode.png)

 

 




