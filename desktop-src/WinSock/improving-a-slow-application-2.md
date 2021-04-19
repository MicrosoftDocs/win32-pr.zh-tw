---
description: 本節將檢查透過網路運作速度很慢的範例應用程式部分。 在本節中，會對初始程式碼進行修改，以改善其效能。
ms.assetid: 29b96540-1b45-46b7-871a-e728aa50ad24
title: 改善應用程式緩慢
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4ae5bbec57791155852a41b1413e0d863f8704c5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106970989"
---
# <a name="improving-a-slow-application"></a><span data-ttu-id="f0183-104">改善應用程式緩慢</span><span class="sxs-lookup"><span data-stu-id="f0183-104">Improving a Slow Application</span></span>

<span data-ttu-id="f0183-105">本節將檢查透過網路運作速度很慢的範例應用程式部分。</span><span class="sxs-lookup"><span data-stu-id="f0183-105">This section examines a portion of a sample application that operates over the network very slowly.</span></span> <span data-ttu-id="f0183-106">在本節中，會對初始程式碼進行修改，以改善其效能。</span><span class="sxs-lookup"><span data-stu-id="f0183-106">Throughout this section, modifications are made to the initial code to improve its performance.</span></span>

<span data-ttu-id="f0183-107">Mock 範例是稱為 Life 之遊戲的更新部分。</span><span class="sxs-lookup"><span data-stu-id="f0183-107">The mock sample is the updated portion for a game called Life.</span></span> <span data-ttu-id="f0183-108">撰寫應用程式的方式是讓用戶端執行更新的計算，並將其傳送至伺服器。</span><span class="sxs-lookup"><span data-stu-id="f0183-108">The application is written such that the client performs the calculations for the updates and sends them to the server.</span></span> <span data-ttu-id="f0183-109">伺服器接著會顯示產生的生命欄位。</span><span class="sxs-lookup"><span data-stu-id="f0183-109">The server then displays the resulting Life field.</span></span> <span data-ttu-id="f0183-110">用戶端的輸出是位元組串流（以三 (triplet) ，其中每個三個都代表一個資料格更新。</span><span class="sxs-lookup"><span data-stu-id="f0183-110">The output from the client is a stream of bytes, grouped in threes (triplets), each triplet representing one cell update.</span></span> <span data-ttu-id="f0183-111">三元中的位元組分別代表資料格的資料列、資料行和值。</span><span class="sxs-lookup"><span data-stu-id="f0183-111">The bytes in the triplet represent the row, column, and value, respectively, for the cell.</span></span>

<span data-ttu-id="f0183-112">這個範例會以刻意執行不良的應用程式開始，提供可從中說明效能改善的基準。</span><span class="sxs-lookup"><span data-stu-id="f0183-112">This sample begins as an intentionally poor performing application, which provides the baseline from which performance improvements can be illustrated.</span></span> <span data-ttu-id="f0183-113">然後，程式碼會經過改良三次，以解決影響效能的各種問題。</span><span class="sxs-lookup"><span data-stu-id="f0183-113">From there, the code is improved three times to address various issues that affect performance.</span></span> <span data-ttu-id="f0183-114">這些範例應該依序讀取，因為每個反復專案在舊版上都有改善。</span><span class="sxs-lookup"><span data-stu-id="f0183-114">These samples should be read in order, as each iteration improves on the previous version.</span></span>

<span data-ttu-id="f0183-115">基準代碼和改善該程式碼的修訂如下：</span><span class="sxs-lookup"><span data-stu-id="f0183-115">The baseline code, and the revisions that improve that code, are the following:</span></span>

-   [<span data-ttu-id="f0183-116">基準版本：執行效能不佳的應用程式</span><span class="sxs-lookup"><span data-stu-id="f0183-116">The Baseline Version: A Very Poor Performing Application</span></span>](the-baseline-version-a-very-poor-performing-application-2.md)
-   [<span data-ttu-id="f0183-117">修訂1：清除明顯的</span><span class="sxs-lookup"><span data-stu-id="f0183-117">Revision 1: Cleaning up the Obvious</span></span>](revision-1-cleaning-up-the-obvious-2.md)
-   [<span data-ttu-id="f0183-118">修訂2：重新設計較少的連接</span><span class="sxs-lookup"><span data-stu-id="f0183-118">Revision 2: Redesigning for Fewer Connects</span></span>](revision-2-redesigning-for-fewer-connects-2.md)
-   [<span data-ttu-id="f0183-119">修訂3：壓縮的區區塊轉送</span><span class="sxs-lookup"><span data-stu-id="f0183-119">Revision 3: Compressed Block Send</span></span>](revision-3-compressed-block-send-2.md)
-   [<span data-ttu-id="f0183-120">未來的改進</span><span class="sxs-lookup"><span data-stu-id="f0183-120">Future Improvements</span></span>](future-improvements-2.md)

> [!WARNING]
> <span data-ttu-id="f0183-121">應用程式的前幾個範例提供刻意不佳的效能，以說明程式碼變更可能帶來的效能改進。</span><span class="sxs-lookup"><span data-stu-id="f0183-121">The first few examples of the application provide intentionally poor performance, in order to illustrate performance improvements possible with changes to code.</span></span> <span data-ttu-id="f0183-122">請勿在您的應用程式中使用這些程式碼範例;它們僅供說明之用。</span><span class="sxs-lookup"><span data-stu-id="f0183-122">Do not use these code samples in your application; they are for illustration purposes only.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="f0183-123">相關主題</span><span class="sxs-lookup"><span data-stu-id="f0183-123">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f0183-124">高效能的 Windows 通訊端應用程式</span><span class="sxs-lookup"><span data-stu-id="f0183-124">High-performance Windows Sockets Applications</span></span>](high-performance-windows-sockets-applications-2.md)
</dt> </dl>

 

 



