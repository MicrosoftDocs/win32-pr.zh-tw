---
title: DNS 區域
description: DNS 區域是 (更精確的一組檔案或記錄，也就是對應至 DNS 階層式命名空間一部分的資源記錄專案) 的資料庫。
ms.assetid: fc24bcd0-854d-4452-9c81-f344b52c7b4e
keywords:
- DNS 區域 DNS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ba8914e699e00cbbc2e699c2b36d40c8d00b87c1
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "106965778"
---
# <a name="dns-zones"></a><span data-ttu-id="5be1b-104">DNS 區域</span><span class="sxs-lookup"><span data-stu-id="5be1b-104">DNS Zones</span></span>

<span data-ttu-id="5be1b-105">DNS 區域是 (更精確的一組檔案或記錄，也就是對應至 DNS 階層式命名空間一部分的資源記錄專案) 的資料庫。</span><span class="sxs-lookup"><span data-stu-id="5be1b-105">A DNS zone is a set of files or records (more precisely, a database of resource record entries) that corresponds to part of the DNS hierarchical namespace.</span></span> <span data-ttu-id="5be1b-106">DNS 區域是用來說明哪些 DNS 伺服器負責 (的授權) ，以便解析 DNS 階層的指定區段的名稱解析查詢。</span><span class="sxs-lookup"><span data-stu-id="5be1b-106">DNS zones are used to delineate which DNS Servers are responsible (authoritative) for resolving name-resolution queries for a given section of the DNS hierarchy.</span></span> <span data-ttu-id="5be1b-107">DNS 區域與網域結構的差異如下：區域可以由一或多個 DNS 網域組成。</span><span class="sxs-lookup"><span data-stu-id="5be1b-107">DNS zones differ from the domain structure in the following fashion: zones can be composed of one or more DNS domains.</span></span> <span data-ttu-id="5be1b-108">Gadgets.widgets.microsoft.com 網域樹狀結構中的一個區域可能是小工具和 widget 網域的授權。</span><span class="sxs-lookup"><span data-stu-id="5be1b-108">One zone in the gadgets.widgets.microsoft.com domain tree might be authoritative for the gadgets and widgets domains.</span></span> <span data-ttu-id="5be1b-109">換句話說，DNS 區域不需要有與 DNS 網域之間的一對一關聯性。</span><span class="sxs-lookup"><span data-stu-id="5be1b-109">In other words, there is not a requirement for DNS zones to have a one-to-one relationship with DNS domains.</span></span>

 

 




