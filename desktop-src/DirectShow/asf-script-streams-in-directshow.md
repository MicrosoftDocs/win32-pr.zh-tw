---
description: DirectShow 中的 ASF 腳本資料流程
ms.assetid: afef1b8b-4be2-48a1-b72a-b2e6342a5e84
title: DirectShow 中的 ASF 腳本資料流程
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: da279c654a581bdb9eba23371882c5cbefbf5849
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "103935925"
---
# <a name="asf-script-streams-in-directshow"></a><span data-ttu-id="30251-103">DirectShow 中的 ASF 腳本資料流程</span><span class="sxs-lookup"><span data-stu-id="30251-103">ASF Script Streams in DirectShow</span></span>

<span data-ttu-id="30251-104">當您為 [WM ASF 讀取](wm-asf-reader-filter.md) 器篩選器指定包含 WMMEDIATYPE 腳本類型資料流程的檔案時 \_ ，它會為它建立輸出圖釘，以連接到 [內部指令碼命令](internal-script-command-renderer-filter.md) 轉譯器篩選器。</span><span class="sxs-lookup"><span data-stu-id="30251-104">When the [WM ASF Reader](wm-asf-reader-filter.md) filter is given a file that includes a stream of type WMMEDIATYPE\_Script, it creates an output pin for it that can be connected to the [Internal Script Command Renderer](internal-script-command-renderer-filter.md) filter.</span></span> <span data-ttu-id="30251-105">當您呼叫 [**IGraphBuilder：： RenderFile**](/windows/desktop/api/Strmif/nf-strmif-igraphbuilder-renderfile)時，該篩選會自動加入至圖形並連接。</span><span class="sxs-lookup"><span data-stu-id="30251-105">When you call [**IGraphBuilder::RenderFile**](/windows/desktop/api/Strmif/nf-strmif-igraphbuilder-renderfile), that filter is automatically added to the graph and connected.</span></span> <span data-ttu-id="30251-106">當內部指令碼命令轉譯器收到包含指令碼命令的範例時，它會引發 *lParam* 包含腳本的 [**EC \_ OLE \_ 事件**](ec-ole-event.md)事件。</span><span class="sxs-lookup"><span data-stu-id="30251-106">When the Internal Script Command Renderer receives a sample containing a script command, it fires an [**EC\_OLE\_EVENT**](ec-ole-event.md) event whose *lParam* contains the script.</span></span> <span data-ttu-id="30251-107">應用程式完全負責處理這個事件。</span><span class="sxs-lookup"><span data-stu-id="30251-107">The application is entirely responsible for handling this event.</span></span>

## <a name="related-topics"></a><span data-ttu-id="30251-108">相關主題</span><span class="sxs-lookup"><span data-stu-id="30251-108">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="30251-109">在 DirectShow 中讀取 ASF 檔案</span><span class="sxs-lookup"><span data-stu-id="30251-109">Reading ASF Files in DirectShow</span></span>](reading-asf-files-in-directshow.md)
</dt> </dl>

 

 



