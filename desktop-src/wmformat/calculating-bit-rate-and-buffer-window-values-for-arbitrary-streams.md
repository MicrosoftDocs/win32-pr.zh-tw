---
title: 計算任意資料流程的位元速率和緩衝區視窗值
description: 計算任意資料流程的位元速率和緩衝區視窗值
ms.assetid: 28ba863b-9c3e-4b0e-875d-6b696600888c
keywords:
- 資料流程、位元速率
- 編解碼器，計算任意資料流程的位元速率
- 位元速率，計算任意資料流程
- 串流，計算任意資料流程的位元速率
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 45d704352d414b1fe5079fb068593c2d0d8b2f8c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104020874"
---
# <a name="calculating-bit-rate-and-buffer-window-values-for-arbitrary-streams"></a><span data-ttu-id="30bc8-107">計算任意資料流程的位元速率和緩衝區視窗值</span><span class="sxs-lookup"><span data-stu-id="30bc8-107">Calculating Bit Rate and Buffer Window Values for Arbitrary Streams</span></span>

<span data-ttu-id="30bc8-108">針對任意資料流程類型計算適當的位元速率和緩衝區視窗不是精確的科學。</span><span class="sxs-lookup"><span data-stu-id="30bc8-108">Calculating the proper bit rate and buffer window for an arbitrary stream type is not an exact science.</span></span> <span data-ttu-id="30bc8-109">其中一個簡單的方法是設定比對資料流程大小與資料流程大小（以秒為單位）的位元速率。</span><span class="sxs-lookup"><span data-stu-id="30bc8-109">One simple approach is to set the bit rate to match the size of the stream divided by its length, in seconds.</span></span> <span data-ttu-id="30bc8-110">例如，總共有68000位的資料流程持續20秒，可能會有每秒3400位的位元速率 (68000 位/20 秒 = 每秒3400位) 。</span><span class="sxs-lookup"><span data-stu-id="30bc8-110">For example, a stream containing a total of 68000 bits lasting 20 seconds might have a bit rate of 3400 bits per second (68000 bits / 20 seconds = 3400 bits per second).</span></span>

<span data-ttu-id="30bc8-111">使用這個簡單技巧來指定位元速率的問題是，它不會考慮串流內的資料分佈。</span><span class="sxs-lookup"><span data-stu-id="30bc8-111">The problem with this simple technique of assigning bit rate is that it does not take into account the distribution of data within the stream.</span></span> <span data-ttu-id="30bc8-112">許多任意資料流程在檔案的時間軸上依間隔包含大量的資料。</span><span class="sxs-lookup"><span data-stu-id="30bc8-112">Many arbitrary streams contain larger amounts of data at intervals along the timeline of the file.</span></span> <span data-ttu-id="30bc8-113">例如，影像資料流程的範例很大，但通常會在數秒內分隔。</span><span class="sxs-lookup"><span data-stu-id="30bc8-113">Image streams, for example, have samples that are rather large, but are usually spaced several seconds apart.</span></span> <span data-ttu-id="30bc8-114">您必須設定緩衝區視窗，以確保緩衝區不會溢位。</span><span class="sxs-lookup"><span data-stu-id="30bc8-114">The buffer window must be set to ensure that the buffer will not overflow.</span></span>

<span data-ttu-id="30bc8-115">若要檢查緩衝區視窗，請將緩衝區 (視窗) 的位元速率 (位（以秒為單位）) 並除以1000，以取得資料流程的緩衝區大小（以位為單位）。</span><span class="sxs-lookup"><span data-stu-id="30bc8-115">To check the buffer window, multiply the bit rate (bits per second) by the buffer window (in seconds) and divide by 1000 to get the size, in bits, of the buffer for the stream.</span></span> <span data-ttu-id="30bc8-116">然後，請確定緩衝區大小夠大，足以容納資料流程中小於緩衝區視窗的樣本組合（呈現時間除外）。</span><span class="sxs-lookup"><span data-stu-id="30bc8-116">Then make sure that the buffer size is large enough to hold any combination of samples in the stream that are less than the buffer window apart in presentation time.</span></span> <span data-ttu-id="30bc8-117">如果有疑問，請將這兩個值的設定比您認為需要的值小一點。</span><span class="sxs-lookup"><span data-stu-id="30bc8-117">When in doubt, set both values a little higher than you think you need them.</span></span>

## <a name="related-topics"></a><span data-ttu-id="30bc8-118">相關主題</span><span class="sxs-lookup"><span data-stu-id="30bc8-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="30bc8-119">**緩衝處理內容**</span><span class="sxs-lookup"><span data-stu-id="30bc8-119">**Buffering Content**</span></span>](buffering-content.md)
</dt> <dt>

[<span data-ttu-id="30bc8-120">**設定任意資料流程類型**</span><span class="sxs-lookup"><span data-stu-id="30bc8-120">**Configuring Arbitrary Stream Types**</span></span>](configuring-arbitrary-stream-types.md)
</dt> </dl>

 

 




