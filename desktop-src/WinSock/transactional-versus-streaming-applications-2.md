---
description: 網路應用程式有兩種基本類型：交易式和串流處理。 這些應用程式類型也分別稱為互動式和批次處理應用程式類型。
ms.assetid: 85795cdd-5a4f-4199-98bd-b5ce2299338b
title: 交易式與串流應用程式
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8a000f3aa9c52fe6ce60622a613d6f4b9689b8bf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106972407"
---
# <a name="transactional-versus-streaming-applications"></a><span data-ttu-id="77105-104">交易式與串流應用程式</span><span class="sxs-lookup"><span data-stu-id="77105-104">Transactional versus Streaming Applications</span></span>

<span data-ttu-id="77105-105">網路應用程式有兩種基本類型： *交易* 式和 *串流處理*。</span><span class="sxs-lookup"><span data-stu-id="77105-105">There are two fundamental types of network applications: *transactional* and *streaming*.</span></span> <span data-ttu-id="77105-106">這些應用程式類型也分別稱為 *互動式* 和 *批次處理* 應用程式類型。</span><span class="sxs-lookup"><span data-stu-id="77105-106">These application types are also called *interactive* and *batch processing* application types, respectively.</span></span>

<span data-ttu-id="77105-107">交易式應用程式是停止和移出應用程式。</span><span class="sxs-lookup"><span data-stu-id="77105-107">Transactional applications are stop-and-go applications.</span></span> <span data-ttu-id="77105-108">它們通常會執行要求/回復作業，通常會進行排序。</span><span class="sxs-lookup"><span data-stu-id="77105-108">They usually perform request/reply operations, often ordered.</span></span> <span data-ttu-id="77105-109">交易式應用程式的範例包括同步遠端程序呼叫 (RPC) ，以及某些 HTTP 和網域名稱系統 (DNS) 的部署。</span><span class="sxs-lookup"><span data-stu-id="77105-109">Examples of transactional applications include synchronous remote procedure call (RPC), as well as some HTTP and Domain Name System (DNS) implementations.</span></span>

<span data-ttu-id="77105-110">串流應用程式會移動資料。</span><span class="sxs-lookup"><span data-stu-id="77105-110">Streaming applications move data.</span></span> <span data-ttu-id="77105-111">若要使用平行詞彙來描述串流應用程式，串流應用程式會遵守流動性資料傳輸原理，通常只需考慮資料排序。</span><span class="sxs-lookup"><span data-stu-id="77105-111">To describe streaming applications with a parallel term, streaming applications adhere to a pedal-to-the-metal data transmission philosophy, usually with little concern for data ordering.</span></span> <span data-ttu-id="77105-112">串流應用程式的範例包括網路備份和檔案傳輸協定 (FTP) 。</span><span class="sxs-lookup"><span data-stu-id="77105-112">Examples of streaming applications include network backup and file transfer protocol (FTP).</span></span>

<span data-ttu-id="77105-113">判斷應用程式類型之後，也會決定其網路和通訊協定特性。</span><span class="sxs-lookup"><span data-stu-id="77105-113">Once the application type is determined, its network and protocol characteristics are determined as well.</span></span>

## <a name="related-topics"></a><span data-ttu-id="77105-114">相關主題</span><span class="sxs-lookup"><span data-stu-id="77105-114">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="77105-115">高效能的 Windows 通訊端應用程式</span><span class="sxs-lookup"><span data-stu-id="77105-115">High-performance Windows Sockets Applications</span></span>](high-performance-windows-sockets-applications-2.md)
</dt> <dt>

[<span data-ttu-id="77105-116">效能維度</span><span class="sxs-lookup"><span data-stu-id="77105-116">Performance Dimensions</span></span>](performance-dimensions-2.md)
</dt> </dl>

 

 



