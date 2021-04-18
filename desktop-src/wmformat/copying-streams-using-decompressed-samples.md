---
title: 使用解壓縮的範例複製資料流程
description: 使用解壓縮的範例複製資料流程
ms.assetid: 03ad8415-1dff-4362-94b4-7ec69c3e7888
keywords:
- Windows Media Format SDK，複製資料流程
- Advanced Systems Format (ASF) ，複製資料流程
- ASF (Advanced Systems Format) ，複製資料流程
- 資料流程，使用解壓縮的資料進行複製
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 88c5c0f98b02090d98814983ad518ee3cd7e5d8e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "106964988"
---
# <a name="copying-streams-using-decompressed-samples"></a><span data-ttu-id="3b7fb-107">使用解壓縮的範例複製資料流程</span><span class="sxs-lookup"><span data-stu-id="3b7fb-107">Copying Streams Using Decompressed Samples</span></span>

<span data-ttu-id="3b7fb-108">強烈建議您不要使用解壓縮的範例，將資料流程從一個檔案複製到另一個檔案。</span><span class="sxs-lookup"><span data-stu-id="3b7fb-108">It is strongly recommended that you not copy streams from one file to another using decompressed samples.</span></span> <span data-ttu-id="3b7fb-109">解壓縮和 recompressing 範例的程式將會降低輸出的品質。</span><span class="sxs-lookup"><span data-stu-id="3b7fb-109">The process of decompressing and recompressing samples will degrade the quality of the output.</span></span> <span data-ttu-id="3b7fb-110">如果您需要解壓縮範例，然後將它們複製到另一個資料流程，您可能會遇到以品質為基礎的變數位元速率的一些困難 (VBR) 編碼的資料流程。</span><span class="sxs-lookup"><span data-stu-id="3b7fb-110">If you do need to decompress your samples and then copy them to another stream, you may encounter some difficulty with quality-based variable bit rate (VBR) encoded streams.</span></span>

<span data-ttu-id="3b7fb-111">當編解碼器完成壓縮以品質為基礎的 VBR 串流時，它會記錄所產生內容的位元速率和緩衝區視窗。</span><span class="sxs-lookup"><span data-stu-id="3b7fb-111">When the codec finishes compressing a quality-based VBR stream, it records the bit rate and buffer window of the resulting content.</span></span> <span data-ttu-id="3b7fb-112">當您讀取的檔案包含以品質為基礎的 VBR 編碼的資料流程時，從讀取器取得的設定檔將會注意位元速率和緩衝區視窗，以及最大的位元速率和最大緩衝區視窗。</span><span class="sxs-lookup"><span data-stu-id="3b7fb-112">When you read a file containing a stream encoded with quality-based VBR, the profile obtained from the reader will note the bit rate and buffer window as well as the maximum bit rate and maximum buffer window.</span></span> <span data-ttu-id="3b7fb-113">設定檔中的這項設定通常表示位速率限制的可變位頻率資料流程。</span><span class="sxs-lookup"><span data-stu-id="3b7fb-113">This configuration in the profile normally signifies a bit-rate constrained variable bit rate stream.</span></span> <span data-ttu-id="3b7fb-114">如此一來，當您在寫入器上設定設定檔時，就會預期資料流程的前置處理行程，因為位速率限制的 VBR 資料流程需要雙向編碼。</span><span class="sxs-lookup"><span data-stu-id="3b7fb-114">As a result, when you set the profile on the writer, it will expect a preprocessing pass for the stream, because bit-rate constrained VBR streams require two-pass encoding.</span></span> <span data-ttu-id="3b7fb-115">您應該將資料流程視為位速率受限的 VBR 資料流程，並傳遞範例進行前置處理。</span><span class="sxs-lookup"><span data-stu-id="3b7fb-115">You should treat the stream as if it were a bit-rate constrained VBR stream and deliver the samples for preprocessing.</span></span> <span data-ttu-id="3b7fb-116">因為您使用在特定品質層級編碼內容之後所傳回的值，所以這些值代表所需的品質等級。</span><span class="sxs-lookup"><span data-stu-id="3b7fb-116">Because you are using the values returned after encoding the content at a particular quality level, those values represent the desired quality level.</span></span> <span data-ttu-id="3b7fb-117">當然，重新編碼的輸出品質也會因為重新編碼的結果而稍微降級。</span><span class="sxs-lookup"><span data-stu-id="3b7fb-117">Of course, the quality of the re-encoded output will be somewhat degraded anyway, as a result of the re-encoding.</span></span>

## <a name="related-topics"></a><span data-ttu-id="3b7fb-118">相關主題</span><span class="sxs-lookup"><span data-stu-id="3b7fb-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3b7fb-119">**將資料從一個檔案複製到另一個檔案**</span><span class="sxs-lookup"><span data-stu-id="3b7fb-119">**Copying Data from One File to Another**</span></span>](copying-data-from-one-file-to-another.md)
</dt> <dt>

[<span data-ttu-id="3b7fb-120">**複製資料流程而不解壓縮資料**</span><span class="sxs-lookup"><span data-stu-id="3b7fb-120">**Copying Streams Without Decompressing the Data**</span></span>](copying-streams-without-decompressing-the-data.md)
</dt> </dl>

 

 




