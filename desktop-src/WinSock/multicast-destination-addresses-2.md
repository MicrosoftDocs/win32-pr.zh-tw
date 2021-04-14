---
description: 傳送至多播目的地位址時，Microsoft IPv6 通訊協定通常會要求應用程式必須指定連出介面。
ms.assetid: dbfeaa1f-a7c5-4a15-90f0-4d1cdaf798e9
title: IPv6 多播目的地位址
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a8aa516713fb47f6af03d8564c464a07a19cf0f7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104469053"
---
# <a name="ipv6-multicast-destination-addresses"></a><span data-ttu-id="a4060-103">IPv6 多播目的地位址</span><span class="sxs-lookup"><span data-stu-id="a4060-103">IPv6 Multicast Destination Addresses</span></span>

<span data-ttu-id="a4060-104">傳送至多播目的地位址時，Microsoft IPv6 通訊協定通常會要求應用程式必須指定連出介面。</span><span class="sxs-lookup"><span data-stu-id="a4060-104">When sending to a multicast destination address, the Microsoft IPv6 protocol normally requires that the application have an outgoing interface specified.</span></span> <span data-ttu-id="a4060-105">**\_ \_ 如果** 通訊端選項或將通訊端系結至特定的來源位址，則會使用 IPV6 多播來完成此操作。</span><span class="sxs-lookup"><span data-stu-id="a4060-105">This is done with the **IPV6\_MULTICAST\_IF** socket option or by binding the socket to a specific source address.</span></span>

<span data-ttu-id="a4060-106">您也可以指定特定多播位址的預設介面、整個多播位址範圍，或所有多播位址。</span><span class="sxs-lookup"><span data-stu-id="a4060-106">You can also specify a default interface for a specific multicast address, an entire multicast address scope, or all multicast addresses.</span></span> <span data-ttu-id="a4060-107">這項處理是透過將多播首碼放在連結上所需輸出介面的路由來完成。</span><span class="sxs-lookup"><span data-stu-id="a4060-107">This is done with a route that places the multicast prefix on-link to the desired outgoing interface.</span></span> <span data-ttu-id="a4060-108">下列範例會示範如何指定：</span><span class="sxs-lookup"><span data-stu-id="a4060-108">For following examples show how this can be specified:</span></span>

``` syntax
ipv6 rtu ff02::5/128 3
ipv6 rtu ff0e::/16 3
ipv6 rtu ff00::/8 3
```

 

 



