---
title: 網路延遲和輸送量
description: 遠端程序呼叫 (RPC) 的網路延遲和輸送量。
ms.assetid: 8285fd73-eb54-4c06-b01a-1bffafb7e675
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c5c51c4db75b904ac5feae8c4a1cc5965fc2b06e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104183992"
---
# <a name="network-latency-and-throughput"></a><span data-ttu-id="55fd8-103">網路延遲和輸送量</span><span class="sxs-lookup"><span data-stu-id="55fd8-103">Network Latency and Throughput</span></span>

<span data-ttu-id="55fd8-104">有三個主要問題與網路的最佳使用有關：</span><span class="sxs-lookup"><span data-stu-id="55fd8-104">Three major issues relate to optimal use of the network:</span></span>

-   <span data-ttu-id="55fd8-105">網路延遲</span><span class="sxs-lookup"><span data-stu-id="55fd8-105">Network latency</span></span>
-   <span data-ttu-id="55fd8-106">網路飽和</span><span class="sxs-lookup"><span data-stu-id="55fd8-106">Network saturation</span></span>
-   <span data-ttu-id="55fd8-107">封包處理的含意</span><span class="sxs-lookup"><span data-stu-id="55fd8-107">Packet processing implications</span></span>

<span data-ttu-id="55fd8-108">本節介紹需要使用 RPC 的程式設計工作，然後設計兩個解決方案：其中一個撰寫不佳，而且撰寫了一個妥善的解決方案。</span><span class="sxs-lookup"><span data-stu-id="55fd8-108">This section introduces a programming task requiring use of RPC, then designs two solutions: one poorly written and one well written.</span></span> <span data-ttu-id="55fd8-109">這兩個解決方案都會經過檢查，而且會討論其對網路效能的影響。</span><span class="sxs-lookup"><span data-stu-id="55fd8-109">Both solutions are then scrutinized, and their affect on network performance is discussed.</span></span>

<span data-ttu-id="55fd8-110">在討論這兩種解決方案之前，接下來的幾節將討論和說明網路相關的效能問題。</span><span class="sxs-lookup"><span data-stu-id="55fd8-110">Before discussing the two solutions, the next few sections discuss and clarify network related performance issues.</span></span>

## <a name="network-latency"></a><span data-ttu-id="55fd8-111">網路延遲</span><span class="sxs-lookup"><span data-stu-id="55fd8-111">Network Latency</span></span>

<span data-ttu-id="55fd8-112">網路頻寬和網路延遲是不同的詞彙。</span><span class="sxs-lookup"><span data-stu-id="55fd8-112">Network bandwidth and network latency are separate terms.</span></span> <span data-ttu-id="55fd8-113">頻寬高的網路不保證會有低延遲。</span><span class="sxs-lookup"><span data-stu-id="55fd8-113">Networks with high bandwidth do not guarantee low latency.</span></span> <span data-ttu-id="55fd8-114">例如，雖然輸送量很高，但往返附屬連結的網路路徑通常會有高延遲。</span><span class="sxs-lookup"><span data-stu-id="55fd8-114">For example, a network path traversing a satellite link often has high latency, even though throughput is very high.</span></span> <span data-ttu-id="55fd8-115">網路來回行程若有五個或更多秒的延遲，並不罕見。</span><span class="sxs-lookup"><span data-stu-id="55fd8-115">It is not uncommon for a network round trip traversing a satellite link to have five or more seconds of latency.</span></span> <span data-ttu-id="55fd8-116">這種延遲的含意如下：設計用來傳送要求、等候回復、傳送另一個要求、等候另一個回復等等的應用程式，將會針對每個封包交換等候至少五秒，不論伺服器的速度有多快。</span><span class="sxs-lookup"><span data-stu-id="55fd8-116">The implication of such a delay is this: an application designed to send a request, wait for a reply, send another request, wait for another reply, and so on, will wait at least five seconds for each packet exchange, regardless of how fast the server is.</span></span> <span data-ttu-id="55fd8-117">儘管電腦的速度越來越快，衛星傳輸和網路媒體仍以光線的速度為基礎，這通常會維持不變。</span><span class="sxs-lookup"><span data-stu-id="55fd8-117">Despite the increasing speed of computers, satellite transmissions and network media are based on the speed of light, which generally stays constant.</span></span> <span data-ttu-id="55fd8-118">因此，不太可能發生現有附屬網路的延遲改進。</span><span class="sxs-lookup"><span data-stu-id="55fd8-118">As such, improvements in latency for existing satellite networks is unlikely to occur.</span></span>

## <a name="network-saturation"></a><span data-ttu-id="55fd8-119">網路飽和</span><span class="sxs-lookup"><span data-stu-id="55fd8-119">Network Saturation</span></span>

<span data-ttu-id="55fd8-120">許多網路中都會出現一些飽和度。</span><span class="sxs-lookup"><span data-stu-id="55fd8-120">Some saturation occurs in many networks.</span></span> <span data-ttu-id="55fd8-121">最簡單的網路變得較慢的數據機連結，例如標準的56k 類比數據機。</span><span class="sxs-lookup"><span data-stu-id="55fd8-121">The easiest networks to saturate are slow modem links, such as standard 56k analog modems.</span></span> <span data-ttu-id="55fd8-122">不過，在單一區段上具有許多電腦的乙太網路連結也會變成飽和。</span><span class="sxs-lookup"><span data-stu-id="55fd8-122">However, Ethernet links with many computers on a single segment can also become saturated.</span></span> <span data-ttu-id="55fd8-123">這同樣適用于具有低頻寬或非負載過重連結的廣域網路，例如可處理有限流量數量的路由器或交換器。</span><span class="sxs-lookup"><span data-stu-id="55fd8-123">The same is true about wide area networks with a low-bandwidth or otherwise overburdened link, such as a router or switch that can handle a limited amount of traffic.</span></span> <span data-ttu-id="55fd8-124">在這種情況下，如果網路傳送的封包數超過其最弱的連結可處理的數量，則會捨棄封包。</span><span class="sxs-lookup"><span data-stu-id="55fd8-124">In such these cases, if the network sends more packets than its weakest link can handle, it drops packets.</span></span> <span data-ttu-id="55fd8-125">為了避免擁塞，當偵測到捨棄的封包時，Windows TCP 堆疊會相應減少，進而導致顯著的延遲。</span><span class="sxs-lookup"><span data-stu-id="55fd8-125">To avoid congestion the Windows TCP stack scales back when dropped packets are detected which can result in significant delays.</span></span>

## <a name="packet-processing-implications"></a><span data-ttu-id="55fd8-126">封包處理的含意</span><span class="sxs-lookup"><span data-stu-id="55fd8-126">Packet Processing Implications</span></span>

<span data-ttu-id="55fd8-127">當程式是針對較高層級的環境開發，例如 RPC、COM 甚至 Windows 通訊端時，開發人員通常會忘記在幕後針對每個已傳送或已接收的封包進行多少工作。</span><span class="sxs-lookup"><span data-stu-id="55fd8-127">When programs are developed for higher level environments like RPC, COM, and even Windows Sockets, developers tend to forget how much work takes place behind the scenes for each sent or received packet.</span></span> <span data-ttu-id="55fd8-128">當封包從網路抵達時，電腦就會提供網路卡的插斷。</span><span class="sxs-lookup"><span data-stu-id="55fd8-128">When a packet arrives from the network, an interrupt from the network card is serviced by the computer.</span></span> <span data-ttu-id="55fd8-129">然後， (DPC) 的延遲程序呼叫已排入佇列，而且必須透過驅動程式來進行。</span><span class="sxs-lookup"><span data-stu-id="55fd8-129">Then a Deferred Procedure Call (DPC) is queued, and must make its way through the drivers.</span></span> <span data-ttu-id="55fd8-130">如果使用任何形式的安全性，封包可能必須解密，或是經過驗證的密碼編譯雜湊。</span><span class="sxs-lookup"><span data-stu-id="55fd8-130">If any form of security is used, the packet may have to be decrypted, or the cryptographic hash verified.</span></span> <span data-ttu-id="55fd8-131">您也必須在每個狀態執行一些有效性檢查。</span><span class="sxs-lookup"><span data-stu-id="55fd8-131">A number of validity checks must also be performed at each state.</span></span> <span data-ttu-id="55fd8-132">只有當封包抵達最終目的地：伺服器程式碼時。</span><span class="sxs-lookup"><span data-stu-id="55fd8-132">Only then does the packet arrive at the final destination: the server code.</span></span> <span data-ttu-id="55fd8-133">傳送許多小型資料區塊會導致每個小型資料區塊的封包處理負荷。</span><span class="sxs-lookup"><span data-stu-id="55fd8-133">Sending many small chunks of data results in packet processing overhead for each small chunk of data.</span></span> <span data-ttu-id="55fd8-134">傳送一個大型資料區塊通常會耗用整個系統的 CPU 時間，即使與一個大型區塊相較之下，相較于一個大型區塊的執行成本，也可能與伺服器應用程式相同。</span><span class="sxs-lookup"><span data-stu-id="55fd8-134">Sending one big chunk of data tends to consume significantly less CPU time throughout the system, even though the cost of execution for many small chunks compared to one large chunk may be the same for the server application.</span></span>

## <a name="example-1-a-poorly-designed-rpc-server"></a><span data-ttu-id="55fd8-135">範例1：設計不良的 RPC 伺服器</span><span class="sxs-lookup"><span data-stu-id="55fd8-135">Example 1: A Poorly Designed RPC Server</span></span>

<span data-ttu-id="55fd8-136">想像一下必須存取遠端檔案的應用程式，而手上的工作是設計用來操作遠端檔案的 RPC 介面。</span><span class="sxs-lookup"><span data-stu-id="55fd8-136">Imagine an application that must access remote files, and the task at hand is to design an RPC interface for manipulating the remote file.</span></span> <span data-ttu-id="55fd8-137">最簡單的解決方案是為本機檔案鏡像 studio 檔案常式。</span><span class="sxs-lookup"><span data-stu-id="55fd8-137">The simplest solution is to mirror the studio file routines for local files.</span></span> <span data-ttu-id="55fd8-138">這樣做可能會導致好像很的乾淨且熟悉的介面。</span><span class="sxs-lookup"><span data-stu-id="55fd8-138">Doing so may result in a deceptively clean and familiar interface.</span></span> <span data-ttu-id="55fd8-139">以下是簡短的 .idl 檔：</span><span class="sxs-lookup"><span data-stu-id="55fd8-139">Here is an abbreviated .idl file:</span></span>

``` syntax
typedef [context_handle] void *remote_file;
... .
interface remote_file
{
    remote_file remote_fopen(file_name);
    void remote_fclose(remote_file ...);
    size_t remote_fread(void *, size_t, size_t, remote_file ...);
    size_t remote_fwrite(const void *, size_t, size_t, remote_file ...);
    size_t remote_fseek(remote_file ..., long, int);
}
```

<span data-ttu-id="55fd8-140">這看起來很簡潔，但其實這是一項符合時間的配方，可應付效能嚴重損壞。</span><span class="sxs-lookup"><span data-stu-id="55fd8-140">This seems elegant enough, but actually, this is a time-honored recipe for performance disaster.</span></span> <span data-ttu-id="55fd8-141">相較于熱門的意見，遠端程序呼叫並不只是在呼叫端和被呼叫端之間使用網路的本機程序呼叫。</span><span class="sxs-lookup"><span data-stu-id="55fd8-141">Contrary to popular opinion, remote procedure call is not simply a local procedure call with a wire between the caller and callee.</span></span>

<span data-ttu-id="55fd8-142">若要查看此食譜如何消耗效能，請考慮2K 檔案，其中20個位元組從一開始讀取，最後20個位元組，並查看其執行方式。</span><span class="sxs-lookup"><span data-stu-id="55fd8-142">To see how this recipe burns performance, consider a 2K file, where 20 bytes are read from the beginning, and then 20 bytes from the end, and see how this performs.</span></span> <span data-ttu-id="55fd8-143">在用戶端上，為了簡潔) 起見，已省略許多程式碼路徑來進行下列呼叫 (：</span><span class="sxs-lookup"><span data-stu-id="55fd8-143">On the client side, the following calls are made (many code paths are omitted for brevity):</span></span>

``` syntax
rfp = remote_fopen("c:\\sample.txt");
remote_read(...);
remote_fseek(...);
remote_read(...);
remote_fclose(rfp);
```

<span data-ttu-id="55fd8-144">現在假設伺服器是透過附屬連結與用戶端分開，而且有五秒的來回行程時間。</span><span class="sxs-lookup"><span data-stu-id="55fd8-144">Now imagine that the server is separated from the client by a satellite link with a five-second round-trip time.</span></span> <span data-ttu-id="55fd8-145">每個呼叫都必須等待回應，才能繼續進行，這表示執行此25秒的最小值是絕對最小值。</span><span class="sxs-lookup"><span data-stu-id="55fd8-145">Each of those calls must wait for a response before it can proceed, which means an absolute minimum for executing this sequence of 25 seconds.</span></span> <span data-ttu-id="55fd8-146">考慮我們只抓取40個位元組，這會 outrageously 效能變慢。</span><span class="sxs-lookup"><span data-stu-id="55fd8-146">Considering we are retrieving only 40 bytes, this is outrageously slow performance.</span></span> <span data-ttu-id="55fd8-147">此應用程式的客戶會極了。</span><span class="sxs-lookup"><span data-stu-id="55fd8-147">Customers of this application would be furious.</span></span>

<span data-ttu-id="55fd8-148">現在假設網路已飽和，因為在網路路徑中某個位置的路由器容量會過重。</span><span class="sxs-lookup"><span data-stu-id="55fd8-148">Now imagine the network is saturated, because a router's capacity somewhere in the network path is overburdened.</span></span> <span data-ttu-id="55fd8-149">如果我們沒有安全性，則此設計會強制路由器處理至少10個封包， (每個要求各一個，並針對每個回復) 。</span><span class="sxs-lookup"><span data-stu-id="55fd8-149">This design forces the router to handle at least 10 packets if we do not have security (one for each request, and one for each reply).</span></span> <span data-ttu-id="55fd8-150">這也不是好事。</span><span class="sxs-lookup"><span data-stu-id="55fd8-150">That, too, is not good.</span></span>

<span data-ttu-id="55fd8-151">這種設計也會強制服務器接收五封包，並傳送五封包。</span><span class="sxs-lookup"><span data-stu-id="55fd8-151">This design also forces the server to receive five packets and send five packets.</span></span> <span data-ttu-id="55fd8-152">同樣地，這不是很好的執行。</span><span class="sxs-lookup"><span data-stu-id="55fd8-152">Again, not a very good implementation.</span></span>

## <a name="example-2-a-better-designed-rpc-server"></a><span data-ttu-id="55fd8-153">範例2：設計更好的 RPC 伺服器</span><span class="sxs-lookup"><span data-stu-id="55fd8-153">Example 2: A Better Designed RPC Server</span></span>

<span data-ttu-id="55fd8-154">讓我們重新設計範例1中所討論的介面，並查看我們是否能讓它更好。</span><span class="sxs-lookup"><span data-stu-id="55fd8-154">Let's redesign the interface discussed in Example 1, and see whether we can make it better.</span></span> <span data-ttu-id="55fd8-155">要注意的是，讓此伺服器真的很好，需要知道指定檔案的使用模式：此範例不會假設這類知識。</span><span class="sxs-lookup"><span data-stu-id="55fd8-155">It is important to note that making this server really good requires knowledge of the usage pattern for the given files: such knowledge is not assumed for this example.</span></span> <span data-ttu-id="55fd8-156">因此，這是較佳設計的 RPC 伺服器，但不是以最佳方式設計的 RPC 伺服器。</span><span class="sxs-lookup"><span data-stu-id="55fd8-156">Therefore, this is a better designed RPC server, but not an optimally designed RPC server.</span></span>

<span data-ttu-id="55fd8-157">此範例中的概念是盡可能將許多遠端作業折迭成一項作業。</span><span class="sxs-lookup"><span data-stu-id="55fd8-157">The idea in this example is to collapse as many remote operations into one operation as possible.</span></span> <span data-ttu-id="55fd8-158">第一次嘗試如下所示：</span><span class="sxs-lookup"><span data-stu-id="55fd8-158">The first attempt is the following:</span></span>

``` syntax
typedef [context_handle] void *remote_file;
typedef struct
{
    long position;
    int origin;
} remote_seek_instruction;
... .
interface remote_file
{
    remote_fread(file_name, void *, size_t, size_t, [in, out] remote_file ..., BOOL CloseWhenDone, remote_seek_instruction *...);
    size_t remote_fwrite(file_name, const void *, size_t, size_t, [in, out] remote_file ..., BOOL CloseWhenDone, remote_seek_instruction *...);
}
```

<span data-ttu-id="55fd8-159">此範例會將所有作業折迭為讀取和寫入，以允許在相同的作業上選擇性開啟，以及選擇性的關閉和搜尋。</span><span class="sxs-lookup"><span data-stu-id="55fd8-159">This example collapses all operations to a read and write, which allows for an optional open on the same operation, as well as an optional close and seek.</span></span>

<span data-ttu-id="55fd8-160">以縮寫形式寫入的相同作業順序如下所示：</span><span class="sxs-lookup"><span data-stu-id="55fd8-160">This same sequence of operation, when written in abbreviated form, looks like this:</span></span>

``` syntax
remote_read("c:\\sample.txt", ..., &rfp, FALSE, NULL);
remote_read(NULL, ..., &rfp, TRUE, seek_to_20_bytes_before_end);
```

<span data-ttu-id="55fd8-161">當考慮到設計更好的 RPC 伺服器時，在第二次呼叫時，伺服器會檢查 *檔案名 \_* 是否為 **Null**，並在 rfp 中使用儲存的開啟檔案。</span><span class="sxs-lookup"><span data-stu-id="55fd8-161">When considering the better designed RPC server, on the second call the server checks that the *file\_name* is **NULL**, and uses the stored open file in rfp.</span></span> <span data-ttu-id="55fd8-162">接著，它會看到搜尋指示，並在讀取前將檔案指標放在結尾之前的20個位元組。</span><span class="sxs-lookup"><span data-stu-id="55fd8-162">Then it sees there are seek instructions, and will position the file pointer 20 bytes before the end before it reads.</span></span> <span data-ttu-id="55fd8-163">完成時，它會辨識 **CloseWhenDone** 旗標設定為 **TRUE**，並將關閉該檔案，然後關閉 rfp。</span><span class="sxs-lookup"><span data-stu-id="55fd8-163">When done, it will recognize the **CloseWhenDone** flag is set to **TRUE**, and will close the file, and close rfp.</span></span>

<span data-ttu-id="55fd8-164">在高延遲的網路上，此較佳的版本需要10秒鐘的時間，以加快 (2.5 倍的) ，而且只需要處理四封封包;從伺服器接收兩次，而從伺服器傳送兩次。</span><span class="sxs-lookup"><span data-stu-id="55fd8-164">On the high latency network, this better version takes 10 seconds to complete (2.5 times faster) and requires processing of only four packets; two receives from the server, and two sends from the server.</span></span> <span data-ttu-id="55fd8-165">相較于其他所有專案，伺服器執行的額外 *ifs* 和取消封送也可說是微不足道。</span><span class="sxs-lookup"><span data-stu-id="55fd8-165">The extra *ifs* and unmarshaling the server performs are negligible compared to everything else.</span></span>

<span data-ttu-id="55fd8-166">如果正確指定了因果順序，介面甚至可以是非同步，而這兩個呼叫可以平行傳送。</span><span class="sxs-lookup"><span data-stu-id="55fd8-166">If causal ordering is specified properly, the interface can even be made asynchronous, and the two calls can be sent in parallel.</span></span> <span data-ttu-id="55fd8-167">當使用順序時，呼叫仍會依序分派，這表示在高延遲的網路上，即使傳送和接收的封包數量相同，也只會遷就五秒的延遲。</span><span class="sxs-lookup"><span data-stu-id="55fd8-167">When causal ordering is used calls are still dispatched in order, which means on the high latency network only a five-second delay is endured, even though the number of packets sent and received is the same.</span></span>

<span data-ttu-id="55fd8-168">我們可以建立一個採用結構陣列的方法（陣列的每個成員分別描述特定的檔案作業），以進一步折迭這項作業;散佈/收集 i/o 的遠端變化。</span><span class="sxs-lookup"><span data-stu-id="55fd8-168">We can collapse this even further by creating one method that takes an array of structures, each member of the array describing a particular file operation; a remote variation of scatter/gather I/O.</span></span> <span data-ttu-id="55fd8-169">只要每項作業的結果不需要在用戶端上進行進一步的處理，此方法就會隨之付費。換句話說，應用程式將會讀取最後20個位元組，而不考慮前20個位元組的讀取量。</span><span class="sxs-lookup"><span data-stu-id="55fd8-169">The approach pays off as long as the result of each operation does not require further processing on the client; in other words the application is going to read the 20 bytes at the end regardless of what the first 20 bytes read are.</span></span>

<span data-ttu-id="55fd8-170">但是，如果必須在讀取後的前20個位元組執行某些處理，以判斷下一項作業，則將所有專案折迭至一項作業將無法運作 (至少在所有情況下都不會) 。</span><span class="sxs-lookup"><span data-stu-id="55fd8-170">However, if some processing must be performed on the first 20 bytes after reading them to determine the next operation, collapsing everything into one operation does not work (at least not in all cases).</span></span> <span data-ttu-id="55fd8-171">RPC 的簡潔性是，應用程式可以在介面中同時有這兩種方法，並視需要呼叫這兩種方法。</span><span class="sxs-lookup"><span data-stu-id="55fd8-171">The elegance of RPC is that an application can have both methods in the interface, and call either method depending on need.</span></span>

<span data-ttu-id="55fd8-172">一般而言，在涉及網路時，最好盡可能將多個呼叫合併到單一呼叫。</span><span class="sxs-lookup"><span data-stu-id="55fd8-172">In general, when the network is involved it is best to combine as many calls onto a single call as possible.</span></span> <span data-ttu-id="55fd8-173">如果應用程式有兩個獨立的活動，請使用非同步作業，並讓它們平行執行。</span><span class="sxs-lookup"><span data-stu-id="55fd8-173">If an application has two independent activities, use asynchronous operations and let them run in parallel.</span></span> <span data-ttu-id="55fd8-174">基本上，讓管線保持完整。</span><span class="sxs-lookup"><span data-stu-id="55fd8-174">Essentially, keep the pipeline full.</span></span>

 

 




