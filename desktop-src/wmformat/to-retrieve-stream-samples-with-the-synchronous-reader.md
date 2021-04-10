---
title: 使用同步讀取器取出資料流程範例
description: 使用同步讀取器取出資料流程範例
ms.assetid: d5cc4bb7-5fcf-4e1e-80dc-f03feed4dc8a
keywords:
- Advanced Systems Format (ASF) ，正在抓取資料流程範例
- ASF (Advanced 系統格式) ，正在抓取資料流程範例
- Advanced Systems Format (ASF) 、同步讀取器
- ASF (Advanced Systems Format) ，同步讀取器
- 同步讀取器，正在抓取資料流程範例
- 資料流程，正在抓取範例
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c7fd641dc08387606d1fdf04602e46cb9e9cbc2b
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/19/2020
ms.locfileid: "104092538"
---
# <a name="to-retrieve-stream-samples-with-the-synchronous-reader"></a><span data-ttu-id="78700-109">使用同步讀取器取出資料流程範例</span><span class="sxs-lookup"><span data-stu-id="78700-109">To Retrieve Stream Samples with the Synchronous Reader</span></span>

<span data-ttu-id="78700-110">如同非同步讀取器，同步讀取器可以依串流號碼來取得範例。</span><span class="sxs-lookup"><span data-stu-id="78700-110">Like the asynchronous reader, the synchronous reader can retrieve samples by stream number.</span></span> <span data-ttu-id="78700-111">與非同步讀取器不同的是，同步讀取器可以傳遞壓縮或未壓縮的串流範例。</span><span class="sxs-lookup"><span data-stu-id="78700-111">Unlike the asynchronous reader, the synchronous reader can deliver stream samples either compressed or uncompressed.</span></span>

<span data-ttu-id="78700-112">若要接收串流範例，請執行下列步驟。</span><span class="sxs-lookup"><span data-stu-id="78700-112">To receive stream samples, perform the following steps.</span></span>

1.  <span data-ttu-id="78700-113">在播放之前或期間的任何時間，呼叫 [**IWMSyncReader：： SetReadStreamSamples**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmsyncreader-setreadstreamsamples) 傳遞所需的串流號碼。</span><span class="sxs-lookup"><span data-stu-id="78700-113">Any time before or during playback, call [**IWMSyncReader::SetReadStreamSamples**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmsyncreader-setreadstreamsamples) passing the desired stream number.</span></span>
2.  <span data-ttu-id="78700-114">使用繼續呼叫 [**IWMSyncReader：： GetNextSample**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmsyncreader-getnextsample)來取出範例。</span><span class="sxs-lookup"><span data-stu-id="78700-114">Retrieve samples with continued calls to [**IWMSyncReader::GetNextSample**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmsyncreader-getnextsample).</span></span>

<span data-ttu-id="78700-115">您可以藉由呼叫 [**IWMSyncReader：： GetReadStreamSamples**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmsyncreader-getreadstreamsamples)，檢查是否已選取資料流程進行範例傳遞。</span><span class="sxs-lookup"><span data-stu-id="78700-115">You can check whether a stream is selected for sample delivery by calling [**IWMSyncReader::GetReadStreamSamples**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmsyncreader-getreadstreamsamples).</span></span>

## <a name="related-topics"></a><span data-ttu-id="78700-116">相關主題</span><span class="sxs-lookup"><span data-stu-id="78700-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="78700-117">**IWMSyncReader 介面**</span><span class="sxs-lookup"><span data-stu-id="78700-117">**IWMSyncReader Interface**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmsyncreader)
</dt> <dt>

[<span data-ttu-id="78700-118">**使用同步讀取器讀取檔案**</span><span class="sxs-lookup"><span data-stu-id="78700-118">**Reading Files with the Synchronous Reader**</span></span>](reading-files-with-the-synchronous-reader.md)
</dt> </dl>

 

 




