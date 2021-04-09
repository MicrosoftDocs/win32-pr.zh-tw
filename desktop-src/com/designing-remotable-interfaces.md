---
title: 設計可遠端處理的介面
description: 隨著分散式元件物件模型的出現，即使您只想要在進程中使用它，您的自訂介面也很重要。
ms.assetid: 2ee4d950-dfd5-4965-bd77-a600e878be59
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3502604d62e6a5129ca3e3538761722909c0198f
ms.sourcegitcommit: 85688bbfbe5b121bc05ddf112d54c23a469dfbc0
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "103841839"
---
# <a name="designing-remotable-interfaces"></a><span data-ttu-id="5415a-103">設計可遠端處理的介面</span><span class="sxs-lookup"><span data-stu-id="5415a-103">Designing Remotable Interfaces</span></span>

<span data-ttu-id="5415a-104">隨著分散式元件物件模型的出現，即使您只想要在進程中使用它，您的自訂介面也很重要。</span><span class="sxs-lookup"><span data-stu-id="5415a-104">With the advent of the distributed component object model, it is important that your custom interface be remotable, even if you intend to use it in-process only.</span></span>

<span data-ttu-id="5415a-105">MIDL 不只是產生介面標頭檔的方法。</span><span class="sxs-lookup"><span data-stu-id="5415a-105">MIDL is more than just a way to generate header files for your interfaces.</span></span> <span data-ttu-id="5415a-106">它是遠端的程式設計語言，可讓您跨電腦、進程和執行緒界限使用您的介面。</span><span class="sxs-lookup"><span data-stu-id="5415a-106">It is a programming language for remoting that allows you to use your interfaces across machine, process, and thread boundaries.</span></span> <span data-ttu-id="5415a-107">這表示在將程式發行給客戶之前，您必須先確認這些條件下 MIDL 定義介面的行為。</span><span class="sxs-lookup"><span data-stu-id="5415a-107">This means that you need to verify the behavior of your MIDL-defined interfaces under those conditions before you release your program to customers.</span></span> <span data-ttu-id="5415a-108">如果您在 IDL 中犯了錯誤，且介面未正確地進行遠端處理，可能很難補救該錯誤。</span><span class="sxs-lookup"><span data-stu-id="5415a-108">If you made a mistake in your IDL and the interface is not remoted correctly, it can be difficult to remedy that mistake.</span></span> <span data-ttu-id="5415a-109">您必須使用新的 IID 來修改您的介面，並保留舊的，以提供回溯相容性，或者您必須同時將每個用戶端和每部伺服器電腦轉換成。</span><span class="sxs-lookup"><span data-stu-id="5415a-109">Either you have to revise your interface with a new IID and leave the old one in for backward compatibility or you have to convert every client and every server machine everywhere at the same time.</span></span>

<span data-ttu-id="5415a-110">即使您的介面永遠不會使用跨進程，它也可以跨執行緒使用。</span><span class="sxs-lookup"><span data-stu-id="5415a-110">Even if your interface will never be used out-of-process, it may be used cross-thread.</span></span> <span data-ttu-id="5415a-111">未檢查的 IDL 檔案最糟的問題，可能會發生在不支援多個 [單一執行緒單元](single-threaded-apartments.md)) 的同進程伺服器中。</span><span class="sxs-lookup"><span data-stu-id="5415a-111">The worst problem for an unchecked IDL file can arise for in-process servers that do not support multiple [single-threaded apartments](single-threaded-apartments.md)).</span></span> <span data-ttu-id="5415a-112">未指定執行緒模型的伺服器隱含為單一執行緒。</span><span class="sxs-lookup"><span data-stu-id="5415a-112">A server that does not specify a threading model is implicitly single-threaded.</span></span> <span data-ttu-id="5415a-113">所有標示為單一執行緒的專案都會強制進入先呼叫 [**CoInitialize**](/windows/desktop/api/Objbase/nf-objbase-coinitialize) 或 [**CoInitializeEx**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializeex)的執行緒。</span><span class="sxs-lookup"><span data-stu-id="5415a-113">Everything marked single-threaded is forced over to the thread that first called [**CoInitialize**](/windows/desktop/api/Objbase/nf-objbase-coinitialize) or [**CoInitializeEx**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializeex).</span></span> <span data-ttu-id="5415a-114">如果有其他執行緒是啟始物件的執行緒，則單一執行緒伺服器上的所有介面都必須從遠端回傳至啟動執行緒，這可能會導致傳回 REGDB \_ E \_ IIDNOTREG，以回應對 [**QueryInterface**](/windows/desktop/api/Unknwn/nf-unknwn-iunknown-queryinterface(q))) 的呼叫。</span><span class="sxs-lookup"><span data-stu-id="5415a-114">If some other thread was the one that activated the object, all the interfaces on that single-threaded server must be remoted back to the activating thread, which can result in a return of REGDB\_E\_IIDNOTREG in response to a call to [**QueryInterface**](/windows/desktop/api/Unknwn/nf-unknwn-iunknown-queryinterface(q))).</span></span> <span data-ttu-id="5415a-115">除非您可以完全判斷提示您的介面同時處於同進程且一律會在相同的執行緒上呼叫，否則您將會在一段時間內進行遠端存取。</span><span class="sxs-lookup"><span data-stu-id="5415a-115">Unless you can absolutely assert that your interface is both in-process and always going to be called on the same thread, you will get remoted at some time.</span></span>

<span data-ttu-id="5415a-116">最後，作為介面設計工具，您需要考慮用戶端應用程式將如何使用您的介面。</span><span class="sxs-lookup"><span data-stu-id="5415a-116">Finally, as an interface designer, you need to consider how client applications will use your interface.</span></span> <span data-ttu-id="5415a-117">另外還有兩件事，就是判斷介面在進程和電腦界限之間是否有效：跨介面界限的方法呼叫頻率，以及在指定的方法呼叫中要傳輸的資料量。</span><span class="sxs-lookup"><span data-stu-id="5415a-117">Two things, together, determine whether an interface will be efficient across process and machine boundaries: the frequency of method calls across the interface boundary, and the amount of data to be transferred in a given method call.</span></span> <span data-ttu-id="5415a-118">雖然 COM 讓程式得以透明地跨進程和跨網路呼叫，但是無法讓高頻率和高頻寬呼叫在位址空間之間有效率。</span><span class="sxs-lookup"><span data-stu-id="5415a-118">Although COM makes cross-process and cross-network calls transparent to programs, it cannot make high-frequency and high-bandwidth calls efficient across address spaces.</span></span> <span data-ttu-id="5415a-119">在某些情況下，設計介面較適合通常只會實作為同進程伺服器，而其他介面更適合遠端使用的介面。</span><span class="sxs-lookup"><span data-stu-id="5415a-119">In some cases, it is more appropriate to design interfaces that will normally be implemented only as in-process servers while other interfaces are more appropriate for remote use.</span></span>

 

 




