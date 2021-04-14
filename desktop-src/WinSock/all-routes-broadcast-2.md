---
description: 藉由將 sa \_ netnum 和 sa \_ nodenum 欄位設定為二進位 (1) ，即可達到透過網際網路進行的一般廣播。
ms.assetid: a56f3059-d6e5-42eb-8ba2-16071fffafa5
title: 所有路由廣播
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 15830ad4f82a3cc5d93e84762c8c17ed0cfd85bd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104469068"
---
# <a name="all-routes-broadcast"></a><span data-ttu-id="bd815-103">所有路由廣播</span><span class="sxs-lookup"><span data-stu-id="bd815-103">All Routes Broadcast</span></span>

<span data-ttu-id="bd815-104">藉由將 **sa \_ netnum** 和 **sa \_ nodenum** 欄位設定為二進位 (1) ，即可達到透過網際網路進行的一般廣播。</span><span class="sxs-lookup"><span data-stu-id="bd815-104">A general broadcast through the Internet is achieved by setting the **sa\_netnum** and **sa\_nodenum** fields to binary ones (1).</span></span> <span data-ttu-id="bd815-105">服務提供者會將此要求轉譯為類型20的封包，而這是由 IPX 路由器辨識和轉寄的封包。</span><span class="sxs-lookup"><span data-stu-id="bd815-105">The service provider translates this request to a type-20 packet, which IPX routers recognize and forward.</span></span> <span data-ttu-id="bd815-106">封包會造訪所有子網，而且可能會重複數次。</span><span class="sxs-lookup"><span data-stu-id="bd815-106">The packet visits all subnets and may be duplicated several times.</span></span> <span data-ttu-id="bd815-107">接收者必須處理數個重複的資料包複本。</span><span class="sxs-lookup"><span data-stu-id="bd815-107">Receivers must handle several duplicate copies of the datagram.</span></span>

<span data-ttu-id="bd815-108">這種廣播類型是在網路系統管理員之間不，所以其使用應非常有限。</span><span class="sxs-lookup"><span data-stu-id="bd815-108">Use of this broadcast type is unpopular among network administrators, so its use should be extremely limited.</span></span> <span data-ttu-id="bd815-109">許多路由器會停用這種類型的廣播，讓封包的部分不會被隱藏。</span><span class="sxs-lookup"><span data-stu-id="bd815-109">Many routers disable this type of broadcast, leaving parts of the subnet invisible to the packet.</span></span>

 

 



