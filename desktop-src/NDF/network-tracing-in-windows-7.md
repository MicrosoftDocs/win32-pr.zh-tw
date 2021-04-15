---
title: Windows 7 中的網路追蹤
description: Windows 7 (NDF) 擴充網路診斷架構，以提供快速的方法來疑難排解網路連線問題，方法是在一個步驟中啟用所有所需資訊的收集，以及利用 Windows 的事件追蹤 (ETW) 將網路事件封包記錄在單一檔案中。
ms.assetid: 7d331362-ff26-4ca0-aa45-07cc97304c7c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2e3abb4283262703123f8e7060a09af0b810477b
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104382801"
---
# <a name="network-tracing-in-windows-7"></a><span data-ttu-id="3ef06-103">Windows 7 中的網路追蹤</span><span class="sxs-lookup"><span data-stu-id="3ef06-103">Network Tracing in Windows 7</span></span>

<span data-ttu-id="3ef06-104">當網路堆疊的複雜性增加時，通常很難快速追蹤和診斷堆疊內的問題。</span><span class="sxs-lookup"><span data-stu-id="3ef06-104">As the complexity of the networking stack increases, it is often difficult to quickly trace and diagnose issues within the stack.</span></span> <span data-ttu-id="3ef06-105">Windows 7 (NDF) 擴充網路診斷架構，以提供快速的方法來疑難排解網路連線問題，方法是在一個步驟中啟用所有所需資訊的收集，以及利用 [Windows 的事件追蹤 (ETW) ](../etw/event-tracing-portal.md) 將網路事件記錄 & 單一檔案中的封包。</span><span class="sxs-lookup"><span data-stu-id="3ef06-105">Windows 7 expands on the Network Diagnostic Framework (NDF) to provide a quick method for troubleshooting network connectivity issues by enabling collection of all the needed information in one step, and by leveraging [Event Tracing for Windows (ETW)](../etw/event-tracing-portal.md) to log network events & packets in a single file.</span></span>

<span data-ttu-id="3ef06-106">相關事件和封包會在網路堆疊的各種元件中，針對指定的活動（例如流覽網站）群組在一起。</span><span class="sxs-lookup"><span data-stu-id="3ef06-106">Related events and packets are grouped together for a given activity, such as browsing a website, across the various components in the networking stack.</span></span> <span data-ttu-id="3ef06-107">此進程的輸出是 (ETL) 檔的事件追蹤記錄。</span><span class="sxs-lookup"><span data-stu-id="3ef06-107">The output of this process is an Event Trace Log (ETL) file.</span></span> <span data-ttu-id="3ef06-108">藉由允許在這個檔案中一次查看與特定活動相關的所有事件，就能大幅降低隔離及診斷網路問題所需的時間。</span><span class="sxs-lookup"><span data-stu-id="3ef06-108">By allowing all of the events related to a specific activity to be viewed at once in this file, the time required to isolate and diagnose network issues can be greatly reduced.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="3ef06-109">本節內容</span><span class="sxs-lookup"><span data-stu-id="3ef06-109">In This Section</span></span>



| <span data-ttu-id="3ef06-110">主題</span><span class="sxs-lookup"><span data-stu-id="3ef06-110">Topic</span></span>                                                                                                                      |
|----------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="3ef06-111">Windows 7 中的網路追蹤：架構</span><span class="sxs-lookup"><span data-stu-id="3ef06-111">Network Tracing in Windows 7: Architecture</span></span>](network-tracing-in-windows-7-architecture.md)                                |
| [<span data-ttu-id="3ef06-112">在 Windows 7 中使用網路追蹤進行疑難排解的工具</span><span class="sxs-lookup"><span data-stu-id="3ef06-112">Tools for Troubleshooting using Network Tracing in Windows 7</span></span>](tools-for-troubleshooting-network-tracing-in-windows-7.md) |
| [<span data-ttu-id="3ef06-113">Windows 7 中的網路追蹤：案例</span><span class="sxs-lookup"><span data-stu-id="3ef06-113">Network Tracing in Windows 7: Scenarios</span></span>](network-tracing-in-windows-7-scenarios.md)                                      |



 

 

 