---
title: Teredo
description: Teredo
ms.assetid: fc213675-dbdb-42a1-a09f-dda598b95b94
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d8e1a2717f3732c32f2c1fe4104c8edd2f802ea0
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/28/2021
ms.locfileid: "108105646"
---
# <a name="teredo"></a><span data-ttu-id="8d3f1-103">Teredo</span><span class="sxs-lookup"><span data-stu-id="8d3f1-103">Teredo</span></span>

## <a name="purpose"></a><span data-ttu-id="8d3f1-104">目的</span><span class="sxs-lookup"><span data-stu-id="8d3f1-104">Purpose</span></span>

<span data-ttu-id="8d3f1-105">Teredo 是一種 IPv6 轉換技術，當 IPv6/IPv4 主機位於一或多個 IPv4 網路位址轉譯器 (Nat) 之後，可為單播 IPv6 流量提供位址指派和主機對主機自動通道。</span><span class="sxs-lookup"><span data-stu-id="8d3f1-105">Teredo is an IPv6 transition technology that provides address assignment and host-to-host automatic tunneling for unicast IPv6 traffic when IPv6/IPv4 hosts are located behind one or multiple IPv4 network address translators (NATs).</span></span> <span data-ttu-id="8d3f1-106">為了流經 IPv4 Nat，IPv6 封包會以 IPv4 使用者資料包協定的形式傳送 (UDP) 訊息。</span><span class="sxs-lookup"><span data-stu-id="8d3f1-106">To traverse IPv4 NATs, IPv6 packets are sent as IPv4 User Datagram Protocol (UDP) messages.</span></span>

## <a name="developer-audience"></a><span data-ttu-id="8d3f1-107">開發人員對象</span><span class="sxs-lookup"><span data-stu-id="8d3f1-107">Developer audience</span></span>

<span data-ttu-id="8d3f1-108">Teredo 的設計目的是要讓具有 IPv6 網路程式設計經驗的 C/c + + 開發人員使用。</span><span class="sxs-lookup"><span data-stu-id="8d3f1-108">Teredo is designed for use by C/C++ developers with IPv6 network programming experience.</span></span>

## <a name="run-time-requirements"></a><span data-ttu-id="8d3f1-109">執行階段需求求</span><span class="sxs-lookup"><span data-stu-id="8d3f1-109">Run-time requirements</span></span>

<span data-ttu-id="8d3f1-110">Teredo 介面主要支援 Windows Vista 和 Windows Server 2008。</span><span class="sxs-lookup"><span data-stu-id="8d3f1-110">The Teredo interface is primarily supported by Windows Vista and Windows Server 2008.</span></span> <span data-ttu-id="8d3f1-111">Windows XP Service Pack 2 (SP2) 和 Windows Server 2003 所支援的 Teredo 介面功能有限，在透過 [Teredo 接收請求的流量](receiving-solicited-traffic-over-teredo.md)中有詳細的說明。</span><span class="sxs-lookup"><span data-stu-id="8d3f1-111">The limited functionality of the Teredo Interface supported by Windows XP with Service Pack 2 (SP2) and Windows Server 2003 is detailed in [Receiving Solicited Traffic Over Teredo](receiving-solicited-traffic-over-teredo.md).</span></span>

## <a name="in-this-section"></a><span data-ttu-id="8d3f1-112">本節內容</span><span class="sxs-lookup"><span data-stu-id="8d3f1-112">In this section</span></span>



| <span data-ttu-id="8d3f1-113">主題</span><span class="sxs-lookup"><span data-stu-id="8d3f1-113">Topic</span></span>                                       | <span data-ttu-id="8d3f1-114">描述</span><span class="sxs-lookup"><span data-stu-id="8d3f1-114">Description</span></span>                                                                                |
|---------------------------------------------|--------------------------------------------------------------------------------------------|
| [<span data-ttu-id="8d3f1-115">關於 Teredo</span><span class="sxs-lookup"><span data-stu-id="8d3f1-115">About Teredo</span></span>](about-teredo.md)<br/> | <span data-ttu-id="8d3f1-116">Teredo 介面的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="8d3f1-116">Information about the Teredo interface.</span></span><br/>                                         |
| [<span data-ttu-id="8d3f1-117">使用 Teredo</span><span class="sxs-lookup"><span data-stu-id="8d3f1-117">Using Teredo</span></span>](using-teredo.md)<br/> | <span data-ttu-id="8d3f1-118">Teredo 介面之執行和一般使用方式的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="8d3f1-118">Information about the implementation and general usage of the Teredo Interface.</span></span><br/> |



 

 

 





