---
title: 使用者配置的範例支援
description: 使用者配置的範例支援
ms.assetid: c747139e-e157-4ea0-9132-256dc70e2b15
keywords:
- Windows Media Format SDK，使用者配置的範例支援
- Advanced Systems Format (ASF) 、使用者配置的範例支援
- ASF (Advanced Systems Format) ，使用者配置的範例支援
- 使用者配置的範例支援
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d80d6a0d9a7e19b46940093fc370bd2c8c70590d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104021207"
---
# <a name="user-allocated-sample-support"></a><span data-ttu-id="b8bd0-107">使用者配置的範例支援</span><span class="sxs-lookup"><span data-stu-id="b8bd0-107">User Allocated Sample Support</span></span>

<span data-ttu-id="b8bd0-108">在正常情況下，讀取器物件和同步讀取器物件都會為每個傳遞至您應用程式的範例建立新的緩衝區物件。</span><span class="sxs-lookup"><span data-stu-id="b8bd0-108">Under normal circumstances, both the reader object and the synchronous reader object create a new buffer object for each sample delivered to your application.</span></span> <span data-ttu-id="b8bd0-109">這是因為讀取物件無法知道您的應用程式在取得它們之後，會如何處理這些範例。</span><span class="sxs-lookup"><span data-stu-id="b8bd0-109">This is because the reading object has no way of knowing what your application does with the samples after it gets them.</span></span> <span data-ttu-id="b8bd0-110">雖然許多應用程式只會讀取範例以立即呈現範例，但有些應用程式可能需要長時間維護範例。</span><span class="sxs-lookup"><span data-stu-id="b8bd0-110">Even though many applications read samples only to render them immediately, some applications may need to maintain samples for a long time.</span></span> <span data-ttu-id="b8bd0-111">因此，讀取物件無法重複使用它所配置的任何緩衝區;它會將它們傳遞給您的應用程式，然後對其進行控制。</span><span class="sxs-lookup"><span data-stu-id="b8bd0-111">The reading object cannot, therefore, reuse any of the buffers it allocates; it delivers them to your application, which then has control over them.</span></span>

<span data-ttu-id="b8bd0-112">這種方法的問題在於檔案可以包含大量的範例。</span><span class="sxs-lookup"><span data-stu-id="b8bd0-112">The problem with this approach is that a file can contain an immense number of samples.</span></span> <span data-ttu-id="b8bd0-113">如果其中每一個都需要建立新的緩衝區物件，很多處理器時間就會浪費在配置和釋放記憶體。</span><span class="sxs-lookup"><span data-stu-id="b8bd0-113">If each one of them requires a new buffer object to be created, a lot of processor time is wasted allocating and releasing memory.</span></span> <span data-ttu-id="b8bd0-114">在時間緊迫的應用程式（例如媒體播放機）中，此額外負荷可能會對效能造成很大的危害。</span><span class="sxs-lookup"><span data-stu-id="b8bd0-114">In time-sensitive applications such as media players, this overhead can be very detrimental to performance.</span></span>

<span data-ttu-id="b8bd0-115">為了減輕讀取器配置的範例效能問題，讀取器和同步讀取器都支援使用者配置的範例。</span><span class="sxs-lookup"><span data-stu-id="b8bd0-115">To alleviate the performance issues of reader-allocated samples, both the reader and the synchronous reader support user-allocated samples.</span></span> <span data-ttu-id="b8bd0-116">若要使用您的應用程式所配置的範例，讀取物件會呼叫您所執行的範例配置回呼方法。</span><span class="sxs-lookup"><span data-stu-id="b8bd0-116">To use samples allocated by your application, the reading object makes calls to a sample allocation callback method that you implement.</span></span> <span data-ttu-id="b8bd0-117">回呼用來將緩衝區傳遞給讀取物件的邏輯完全由您負責。</span><span class="sxs-lookup"><span data-stu-id="b8bd0-117">The logic used by the callback to deliver buffers to the reading object is entirely up to you.</span></span> <span data-ttu-id="b8bd0-118">您可以針對整個檔案使用緩衝區集區，或使用多個緩衝區集區，每個輸出或串流各有一個，或針對您的應用程式運作的任何其他配置。</span><span class="sxs-lookup"><span data-stu-id="b8bd0-118">You can use a pool of buffers for the entire file or use multiple pools of buffers, one for each output or stream, or any other scheme that works for your application.</span></span>

## <a name="related-topics"></a><span data-ttu-id="b8bd0-119">相關主題</span><span class="sxs-lookup"><span data-stu-id="b8bd0-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b8bd0-120">**設定檔案讀取的緩衝區**</span><span class="sxs-lookup"><span data-stu-id="b8bd0-120">**Allocating Buffers for File Reading**</span></span>](allocating-buffers-for-file-reading.md)
</dt> <dt>

[<span data-ttu-id="b8bd0-121">**檔案讀取功能**</span><span class="sxs-lookup"><span data-stu-id="b8bd0-121">**File Reading Features**</span></span>](file-reading-features.md)
</dt> </dl>

 

 




