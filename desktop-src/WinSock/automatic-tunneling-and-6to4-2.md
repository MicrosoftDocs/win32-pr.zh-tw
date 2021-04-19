---
description: 與 IPv4 相容的位址和6to4 的自動通道都是透過連結至介面2的首碼來進行 \# 。 前置詞後面的32位會解壓縮，並用作封裝封包的 IPv4 目的地位址。
ms.assetid: 92261a1b-2b7f-4a76-b98a-2631dc303618
title: IPv6 自動通道和6to4
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ede1179902a7ec3276058e078d56e069603e54a7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106986343"
---
# <a name="ipv6-automatic-tunneling-and-6to4"></a><span data-ttu-id="833d3-104">IPv6 自動通道和6to4</span><span class="sxs-lookup"><span data-stu-id="833d3-104">IPv6 Automatic Tunneling and 6to4</span></span>

<span data-ttu-id="833d3-105">與 IPv4 相容的位址和6to4 的自動通道都是透過連結至介面2的首碼來進行 \# 。</span><span class="sxs-lookup"><span data-stu-id="833d3-105">Automatic tunneling with IPv4-compatible addresses and 6to4 both work through a route for a prefix that is on-link to interface \#2.</span></span> <span data-ttu-id="833d3-106">前置詞後面的32位會解壓縮，並用作封裝封包的 IPv4 目的地位址。</span><span class="sxs-lookup"><span data-stu-id="833d3-106">The 32 bits following the prefix are extracted and used as an IPv4 destination address for the encapsulated packet.</span></span>

<span data-ttu-id="833d3-107">自動通道使用：：/96 首碼，預設為啟用。</span><span class="sxs-lookup"><span data-stu-id="833d3-107">Automatic tunneling uses the ::/96 prefix, which is enabled by default.</span></span> <span data-ttu-id="833d3-108">您可以藉由移除下列各項的路由來停用：：/96。</span><span class="sxs-lookup"><span data-stu-id="833d3-108">It can be disabled by removing the route for ::/96.</span></span>

<span data-ttu-id="833d3-109">6to4 會使用2002::/16 首碼（預設不會啟用）。</span><span class="sxs-lookup"><span data-stu-id="833d3-109">6to4 uses the 2002::/16 prefix, which is not enabled by default.</span></span>

 

 



