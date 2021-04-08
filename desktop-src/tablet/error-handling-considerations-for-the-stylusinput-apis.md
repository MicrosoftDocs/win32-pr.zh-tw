---
description: " (Api) 使用 StylusInput 應用程式設計介面時的錯誤處理總覽。"
ms.assetid: 7d7ff5b2-3eda-4570-96fe-b3b8f41ff69b
title: StylusInput API 的錯誤處理考慮
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 35fa582a8dbf531588f6d3d0c142c4ec7b40a058
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103943476"
---
# <a name="error-handling-considerations-for-the-stylusinput-api"></a><span data-ttu-id="38c2b-103">StylusInput API 的錯誤處理考慮</span><span class="sxs-lookup"><span data-stu-id="38c2b-103">Error Handling Considerations for the StylusInput API</span></span>

<span data-ttu-id="38c2b-104">由 [**RealTimeStylus**](realtimestylus-class.md) 物件攔截外掛程式擲回的未處理例外狀況。</span><span class="sxs-lookup"><span data-stu-id="38c2b-104">Unhandled exceptions thrown by a plug-in are caught by the [**RealTimeStylus**](realtimestylus-class.md) object.</span></span> <span data-ttu-id="38c2b-105">當外掛程式擲回例外狀況時，就會中斷正常的資料流程。</span><span class="sxs-lookup"><span data-stu-id="38c2b-105">When a plug-in throws an exception, the normal flow of data is interrupted.</span></span> <span data-ttu-id="38c2b-106">**RealTimeStylus** 物件：</span><span class="sxs-lookup"><span data-stu-id="38c2b-106">The **RealTimeStylus** object:</span></span>

1.  <span data-ttu-id="38c2b-107">在 managed 程式碼) 中建立 [ErrorData](/previous-versions/ms575221(v=vs.100)) 物件 (。</span><span class="sxs-lookup"><span data-stu-id="38c2b-107">Creates an [ErrorData](/previous-versions/ms575221(v=vs.100)) object (in managed code).</span></span>
2.  <span data-ttu-id="38c2b-108">在 managed 程式碼中呼叫 (的 [**錯誤**](/windows/desktop/api/RTSCom/nf-rtscom-istylusplugin-error) 方法，可能是擲回例外狀況之外掛程式的 [StylusInput. IStylusSyncPlugin](/previous-versions/ms824754(v=msdn.10)) 或 [StylusInput. IStylusAsyncPlugin](/previous-versions/ms824771(v=msdn.10)) 方法) 。</span><span class="sxs-lookup"><span data-stu-id="38c2b-108">Calls the [**Error**](/windows/desktop/api/RTSCom/nf-rtscom-istylusplugin-error) method (in managed code, either the [Microsoft.StylusInput.IStylusSyncPlugin.Error](/previous-versions/ms824754(v=msdn.10)) or [Microsoft.StylusInput.IStylusAsyncPlugin.Error](/previous-versions/ms824771(v=msdn.10)) method) of the plug-in that threw the exception.</span></span>
3.  <span data-ttu-id="38c2b-109">呼叫該集合中其餘外掛程式的 [**錯誤**](/windows/desktop/api/RTSCom/nf-rtscom-istylusplugin-error) 方法。</span><span class="sxs-lookup"><span data-stu-id="38c2b-109">Calls the [**Error**](/windows/desktop/api/RTSCom/nf-rtscom-istylusplugin-error) method of the remaining plug-ins in that collection.</span></span>
4.  <span data-ttu-id="38c2b-110">如果擲回例外狀況的外掛程式是同步外掛程式，則會將 managed 程式碼) 中 (的 [ErrorData](/previous-versions/ms575221(v=vs.100)) 物件新增至輸出佇列。</span><span class="sxs-lookup"><span data-stu-id="38c2b-110">If the plug-in that threw the exception is a synchronous plug-in, the [ErrorData](/previous-versions/ms575221(v=vs.100)) object (in managed code) is added to the output queue.</span></span>
5.  <span data-ttu-id="38c2b-111">[**RealTimeStylus**](realtimestylus-class.md)物件會繼續正常處理原始資料。</span><span class="sxs-lookup"><span data-stu-id="38c2b-111">The [**RealTimeStylus**](realtimestylus-class.md) object resumes normal processing of the original data.</span></span>

<span data-ttu-id="38c2b-112">如果外掛程式從其 [**錯誤**](/windows/desktop/api/RTSCom/nf-rtscom-istylusplugin-error) 方法擲回例外狀況，則 [**RealTimeStylus**](realtimestylus-class.md) 物件會捕捉例外狀況，但不會產生新的 [ErrorData](/previous-versions/ms575221(v=vs.100)) 物件。</span><span class="sxs-lookup"><span data-stu-id="38c2b-112">If a plug-in throws an exception from its [**Error**](/windows/desktop/api/RTSCom/nf-rtscom-istylusplugin-error) method, the [**RealTimeStylus**](realtimestylus-class.md) object catches the exception but does not generate a new [ErrorData](/previous-versions/ms575221(v=vs.100)) object.</span></span> <span data-ttu-id="38c2b-113">如需如何將 ErrorData 排入佇列的詳細資訊，請參閱 [外掛程式資料和 RealTimeStylus 類別](plug-in-data-and-the-realtimestylus-class.md)。</span><span class="sxs-lookup"><span data-stu-id="38c2b-113">For more information about how ErrorData is added to the queue, see [Plug-in Data and the RealTimeStylus Class](plug-in-data-and-the-realtimestylus-class.md).</span></span>

<span data-ttu-id="38c2b-114">當其中一個外掛程式擲回例外狀況時， [**RealTimeStylus**](realtimestylus-class.md) 物件不會停止處理 tablet 畫筆資料流程中的資料。</span><span class="sxs-lookup"><span data-stu-id="38c2b-114">The [**RealTimeStylus**](realtimestylus-class.md) object does not stop processing data from the tablet pen's data stream when one of its plug-ins throws an exception.</span></span> <span data-ttu-id="38c2b-115">視您的設計而定，某些外掛程式可能需要訂閱 [ErrorData](/previous-versions/ms575221(v=vs.100)) 通知，並在發生例外狀況時修改其行為。</span><span class="sxs-lookup"><span data-stu-id="38c2b-115">Depending on your design, some of your plug-ins may need to subscribe to the [ErrorData](/previous-versions/ms575221(v=vs.100)) notification and modify their behavior when an exception occurs.</span></span>

 

 
