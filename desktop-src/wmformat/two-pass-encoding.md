---
title: Two-Pass 編碼
description: Two-Pass 編碼
ms.assetid: 354cd0a5-9a64-4171-9604-694e60b382ad
keywords:
- Windows Media Format SDK，雙通編碼
- Windows Media Format SDK，2-pass 編碼
- 編解碼器，雙通路編碼
- 編解碼器，2-通過編碼
- 雙通路編碼，關於
- 2-通過編碼，關於
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6764f80857447e122c97c69683243a65da7e83b2
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104021208"
---
# <a name="two-pass-encoding"></a><span data-ttu-id="2a770-109">Two-Pass 編碼</span><span class="sxs-lookup"><span data-stu-id="2a770-109">Two-Pass Encoding</span></span>

<span data-ttu-id="2a770-110">雙通編碼是可用於某些編解碼器的編碼方法，例如 Windows Media 視訊9編解碼器。</span><span class="sxs-lookup"><span data-stu-id="2a770-110">Two-pass encoding is an encoding method available with some codecs, like the Windows Media Video 9 codec.</span></span> <span data-ttu-id="2a770-111">當您使用兩次傳遞編碼時，編解碼器會處理資料流程的所有範例。</span><span class="sxs-lookup"><span data-stu-id="2a770-111">When you use two-pass encoding, the codec processes all of the samples for the stream twice.</span></span> <span data-ttu-id="2a770-112">在第一次傳遞時，編解碼器會收集有關資料流程內容的資訊。</span><span class="sxs-lookup"><span data-stu-id="2a770-112">On the first pass, the codec gathers information about the content of the stream.</span></span> <span data-ttu-id="2a770-113">在第二個階段，編解碼器會使用第一次傳遞時所收集的資訊來優化資料流程的編碼程式。</span><span class="sxs-lookup"><span data-stu-id="2a770-113">On the second pass, the codec uses the information gathered on the first pass to optimize the encoding process for the stream.</span></span>

<span data-ttu-id="2a770-114">在「常數位速率編碼模式」中，以兩個階段編碼的檔案，通常比在單一傳遞中編碼的檔案更有效率。</span><span class="sxs-lookup"><span data-stu-id="2a770-114">In the Constant Bit Rate encoding mode, files that are encoded in two passes are generally more efficient than files encoded in a single pass.</span></span> <span data-ttu-id="2a770-115">以品質為基礎的 VBR （一次通過）會產生比以位速率為基礎的 VBR 更一致的品質，也就是兩個階段。</span><span class="sxs-lookup"><span data-stu-id="2a770-115">Quality-based VBR, which is one pass, produces more consistent quality than bit-rate-based VBR, which is two-pass.</span></span>

<span data-ttu-id="2a770-116">您無法在即時資料流上使用雙通編碼。</span><span class="sxs-lookup"><span data-stu-id="2a770-116">You cannot use two-pass encoding on live streams.</span></span>

## <a name="related-topics"></a><span data-ttu-id="2a770-117">相關主題</span><span class="sxs-lookup"><span data-stu-id="2a770-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2a770-118">**編解碼器功能**</span><span class="sxs-lookup"><span data-stu-id="2a770-118">**Codec Features**</span></span>](codec-features.md)
</dt> <dt>

[<span data-ttu-id="2a770-119">**使用 Two-Pass 編碼**</span><span class="sxs-lookup"><span data-stu-id="2a770-119">**Using Two-Pass Encoding**</span></span>](using-two-pass-encoding.md)
</dt> </dl>

 

 




