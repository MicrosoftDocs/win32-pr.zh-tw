---
description: TAPI 3.1 引進 multitrack 終端機的概念，基本上，終端機是 &0034 的集合 \# ; 追蹤&\# 0034; 端子。
ms.assetid: 8dd6f792-a29e-40fd-9f5b-ee5525028c2e
title: Multitrack 終端機
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bb795169f5e7cbd669e0bceb1d635e33c912c50a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106972470"
---
# <a name="multitrack-terminals"></a><span data-ttu-id="3f44c-103">Multitrack 終端機</span><span class="sxs-lookup"><span data-stu-id="3f44c-103">Multitrack Terminals</span></span>

<span data-ttu-id="3f44c-104">TAPI 3.1 引進 multitrack 終端機的概念，而終端機其實是「追蹤」終端機的集合。</span><span class="sxs-lookup"><span data-stu-id="3f44c-104">TAPI 3.1 introduces the notion of a multitrack terminal, a terminal that, in essence, is a collection of "track" terminals.</span></span> <span data-ttu-id="3f44c-105">Multitrack 終端機可讓程式設計人員在多個媒體串流參與通訊會話的情況下，讓程式設計人員的負載更輕鬆。</span><span class="sxs-lookup"><span data-stu-id="3f44c-105">Multitrack terminals ease the programmer's load in situations where multiple media streams are involved in a communications session.</span></span>

<span data-ttu-id="3f44c-106">檔案 [記錄終端](file-playback-terminal-and-file-recording-terminal.md) 機即為 multitrack 終端機的範例。</span><span class="sxs-lookup"><span data-stu-id="3f44c-106">The [File Recording Terminal](file-playback-terminal-and-file-recording-terminal.md) is an example of a multitrack terminal.</span></span> <span data-ttu-id="3f44c-107">它是由「追蹤」所組成，其中每個「追蹤」是對應至所記錄檔案中資料流程的終端機。</span><span class="sxs-lookup"><span data-stu-id="3f44c-107">It consists of "tracks," where each "track" is a terminal corresponding to a stream in the recorded file.</span></span>

<span data-ttu-id="3f44c-108">[追蹤終端](track-terminals.md)機可以是另一個 multitrack 終端機或單一追蹤終端機。</span><span class="sxs-lookup"><span data-stu-id="3f44c-108">A [track terminal](track-terminals.md) can be another multitrack terminal or a single-track terminal.</span></span> <span data-ttu-id="3f44c-109">單一追蹤終端機是沒有任何追蹤終端機的終端機。</span><span class="sxs-lookup"><span data-stu-id="3f44c-109">A single-track terminal is a terminal that does not have any track terminals.</span></span> <span data-ttu-id="3f44c-110">單一追蹤終端機是此單字的 TAPI 3 意義的終端機。</span><span class="sxs-lookup"><span data-stu-id="3f44c-110">A single-track terminal is a terminal in the TAPI 3 sense of the word.</span></span>

<span data-ttu-id="3f44c-111">如需 multitrack 終端機的詳細資訊，請參閱下列主題：</span><span class="sxs-lookup"><span data-stu-id="3f44c-111">For more information about multitrack terminals, see the following topics:</span></span>

-   [<span data-ttu-id="3f44c-112">關於 Multitrack 終端機</span><span class="sxs-lookup"><span data-stu-id="3f44c-112">About Multitrack Terminals</span></span>](about-multitrack-terminals.md)
-   [<span data-ttu-id="3f44c-113">預設終端機選取機制</span><span class="sxs-lookup"><span data-stu-id="3f44c-113">Default Terminal Selection Mechanism</span></span>](default-terminal-selection-mechanism.md)
-   [<span data-ttu-id="3f44c-114">手動選取終端機</span><span class="sxs-lookup"><span data-stu-id="3f44c-114">Manual Terminal Selection</span></span>](manual-terminal-selection.md)
-   [<span data-ttu-id="3f44c-115">使用 Multitrack 終端機和預設選取機制</span><span class="sxs-lookup"><span data-stu-id="3f44c-115">Using Multitrack Terminals and the Default Selection Mechanism</span></span>](using-multitrack-terminals-and-the-default-selection-mechanism.md)

 

 



