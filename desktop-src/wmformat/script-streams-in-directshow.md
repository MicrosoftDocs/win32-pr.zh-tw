---
title: 在 DirectShow 中編寫串流的腳本
description: 在 DirectShow 中編寫串流的腳本
ms.assetid: ad467897-1d25-4bb0-a0ec-84560fe7063b
keywords:
- Windows Media Format SDK、DirectShow
- Windows Media Format SDK，腳本資料流程
- Advanced Systems Format (ASF) 、DirectShow
- ASF (Advanced Systems Format) ，DirectShow
- Advanced Systems Format (ASF) 、腳本資料流程
- ASF (Advanced 系統格式) 、腳本資料流程
- DirectShow，腳本資料流程
- 腳本串流，DirectShow
- 串流，在 DirectShow 中編寫串流腳本
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 09f08fab54dbdfe61dcc2ce78790cd471985cdeb
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104311157"
---
# <a name="script-streams-in-directshow"></a><span data-ttu-id="fffbb-112">在 DirectShow 中編寫串流的腳本</span><span class="sxs-lookup"><span data-stu-id="fffbb-112">Script Streams in DirectShow</span></span>

<span data-ttu-id="fffbb-113">當「WM ASF 讀取器」篩選器指定包含 WMMEDIATYPE 腳本類型資料流程的檔案時 \_ ，它會為它建立輸出圖釘，以連接至 DirectShow 內部指令碼命令轉譯器篩選器。</span><span class="sxs-lookup"><span data-stu-id="fffbb-113">When the WM ASF Reader filter is given a file that includes a stream of type WMMEDIATYPE\_Script, it creates an output pin for it that can be connected to the DirectShow Internal Script Command Renderer filter.</span></span> <span data-ttu-id="fffbb-114">當您呼叫 **IGraphBuilder：： RenderFile** 時，該篩選會自動加入至圖形並連接。</span><span class="sxs-lookup"><span data-stu-id="fffbb-114">When you call **IGraphBuilder::RenderFile**, that filter is automatically added to the graph and connected.</span></span> <span data-ttu-id="fffbb-115">當內部指令碼命令轉譯器收到包含指令碼命令的範例時，它會引發 **lParam** 包含腳本的 **EC \_ OLE \_ 事件**。</span><span class="sxs-lookup"><span data-stu-id="fffbb-115">When the Internal Script Command Renderer receives a sample containing a script command, it fires an **EC\_OLE\_EVENT** whose **lParam** contains the script.</span></span> <span data-ttu-id="fffbb-116">應用程式完全負責處理這個事件。</span><span class="sxs-lookup"><span data-stu-id="fffbb-116">The application is entirely responsible for handling this event.</span></span> <span data-ttu-id="fffbb-117">如需有關 **EC \_ OLE \_ 事件** 的詳細資訊，請參閱 DirectShow SDK 檔。</span><span class="sxs-lookup"><span data-stu-id="fffbb-117">For more information on **EC\_OLE\_EVENT**, see the DirectShow SDK documentation.</span></span>

 

 




