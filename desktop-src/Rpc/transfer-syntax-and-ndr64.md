---
title: 傳輸語法和 NDR64
description: NDR 網路通訊協定也稱為傳輸語法，可讓 RPC 呼叫跨越網路。
ms.assetid: 30b3843a-172c-4d08-beed-c68bcb68daaf
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1dfec9bc1569ef9a42d0bc844c3b098736f714ab
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104023513"
---
# <a name="transfer-syntax-and-ndr64"></a><span data-ttu-id="c3300-103">傳輸語法和 NDR64</span><span class="sxs-lookup"><span data-stu-id="c3300-103">Transfer Syntax and NDR64</span></span>

<span data-ttu-id="c3300-104">NDR 網路通訊協定也稱為傳輸語法，可讓 RPC 呼叫跨越網路。</span><span class="sxs-lookup"><span data-stu-id="c3300-104">The NDR wire protocol, also referred to as transfer syntax, enables RPC calls to traverse the network.</span></span> <span data-ttu-id="c3300-105">有線通訊協定會定義 RPC 呼叫的網路標記法，例如，資料成員的封送處理順序、網路上的資料對齊、資料中包含的額外資訊，以及其他問題。</span><span class="sxs-lookup"><span data-stu-id="c3300-105">The wire protocol defines the wire representation of an RPC call, such as the order in which data members are marshaled, alignment of data on the wire, additional information included with the data, and other issues.</span></span> <span data-ttu-id="c3300-106">NDR64 通訊協定是以32為基礎的 NDR 傳輸語法延伸模組，專門建立來讓開發人員以64位系統為目標，以達到最佳效能。</span><span class="sxs-lookup"><span data-stu-id="c3300-106">The NDR64 protocol is an extension to the 32-bit based NDR transfer syntax, created specifically to enable developers targeting 64-bit systems to achieve optimized performance.</span></span>

<span data-ttu-id="c3300-107">NDR 電傳格式和 NDR64 電傳格式之間的差異，會解決64位環境中不同指標的大小，以及其他問題。</span><span class="sxs-lookup"><span data-stu-id="c3300-107">The differences between the NDR wire format and the NDR64 wire format addresses the different size of pointers in a 64-bit environment, as well as other issues.</span></span> <span data-ttu-id="c3300-108">NDR64 的機制是由 RPC 處理。</span><span class="sxs-lookup"><span data-stu-id="c3300-108">The mechanics of NDR64 is handled by RPC.</span></span> <span data-ttu-id="c3300-109">開發人員只需要使用/[**protocol**](/windows/desktop/Midl/-protocol)**all** MIDL 命令列參數，即可獲得 NDR64 在64位平臺上的優點。</span><span class="sxs-lookup"><span data-stu-id="c3300-109">Developers need only use the /[**protocol**](/windows/desktop/Midl/-protocol)**all** MIDL command line switch to obtain the benefits of NDR64 on 64-bit platforms.</span></span> <span data-ttu-id="c3300-110">NDR64 僅適用于64位平臺。</span><span class="sxs-lookup"><span data-stu-id="c3300-110">NDR64 is available only on 64-bit platforms.</span></span>

 

 