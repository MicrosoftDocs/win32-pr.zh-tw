---
title: 若要停止進行編制索引
description: 若要停止進行編制索引
ms.assetid: 76c641fa-ea00-4035-bc30-a92059da584a
keywords:
- Windows Media Format SDK，正在停止編制索引
- Advanced Systems Format (ASF) ，正在停止編制索引
- ASF (Advanced Systems Format) ，正在停止編制索引
- 索引，正在停止編制索引
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9ea40cbf020182250e0fb982af5b5f84327d5d9a
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/19/2020
ms.locfileid: "104023064"
---
# <a name="to-stop-indexing-in-progress"></a><span data-ttu-id="e2b17-107">若要停止進行編制索引</span><span class="sxs-lookup"><span data-stu-id="e2b17-107">To Stop Indexing in Progress</span></span>

<span data-ttu-id="e2b17-108">當您開始使用 [**IWMIndexer：： StartIndexing**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmindexer-startindexing)的呼叫來編制索引時，索引子通常會繼續進行，直到檔案編制索引為止。</span><span class="sxs-lookup"><span data-stu-id="e2b17-108">After you begin indexing with a call to [**IWMIndexer::StartIndexing**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmindexer-startindexing), the indexer will normally continue until the file is indexed.</span></span> <span data-ttu-id="e2b17-109">您可以藉由呼叫 [**IWMIndexer：： Cancel**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmindexer-cancel) 方法來停止編制索引作業。</span><span class="sxs-lookup"><span data-stu-id="e2b17-109">You can stop indexing operations by calling the [**IWMIndexer::Cancel**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmindexer-cancel) method.</span></span> <span data-ttu-id="e2b17-110">取消編制索引之後，您可以再次呼叫 **StartIndexing** ，但索引子會從檔案的開頭開始，而不是從取消點繼續。</span><span class="sxs-lookup"><span data-stu-id="e2b17-110">After you have canceled indexing, you can call **StartIndexing** again, but the indexer will start from the beginning of the file rather than resuming from the point of cancellation.</span></span>

<span data-ttu-id="e2b17-111">由於 **StartIndexing** 是非同步呼叫，因此您通常需要從應用程式中的其他執行緒或事件處理常式呼叫 **Cancel** 。</span><span class="sxs-lookup"><span data-stu-id="e2b17-111">Because **StartIndexing** is an asynchronous call, you will normally need to call **Cancel** from some other thread or event handler in your application.</span></span> <span data-ttu-id="e2b17-112">通常會從與 Windows 應用程式的按鈕控制項相關聯的事件程式呼叫 **Cancel** 。</span><span class="sxs-lookup"><span data-stu-id="e2b17-112">Typically **Cancel** will be called from an event procedure associated with a button control of a Windows application.</span></span>

<span data-ttu-id="e2b17-113">取消編制索引時，索引子會傳遞 WMT 已關閉的狀態訊息 \_ ，就像檔案已正確編制索引一樣。</span><span class="sxs-lookup"><span data-stu-id="e2b17-113">When indexing is canceled, the indexer will pass a status message of WMT\_CLOSED, just as if the file had been indexed properly.</span></span>

## <a name="related-topics"></a><span data-ttu-id="e2b17-114">相關主題</span><span class="sxs-lookup"><span data-stu-id="e2b17-114">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e2b17-115">**IWMIndexer 介面**</span><span class="sxs-lookup"><span data-stu-id="e2b17-115">**IWMIndexer Interface**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmindexer)
</dt> <dt>

[<span data-ttu-id="e2b17-116">**使用索引**</span><span class="sxs-lookup"><span data-stu-id="e2b17-116">**Working with Indexes**</span></span>](working-with-indexes.md)
</dt> </dl>

 

 




