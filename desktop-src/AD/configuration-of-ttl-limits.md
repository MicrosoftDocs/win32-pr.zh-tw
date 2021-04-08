---
title: 設定 TTL 限制
description: 用戶端可以要求介於1到 31557600 (的 TTL 值，也就是1秒到1年的) 。
ms.assetid: 4009702c-7992-4e20-9d37-384f8137ba8f
ms.tgt_platform: multiple
keywords:
- 設定 TTL 限制 AD
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b2cb3617bd59667f0284c4e383da54752adfbe25
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103670996"
---
# <a name="configuration-of-ttl-limits"></a><span data-ttu-id="59131-104">設定 TTL 限制</span><span class="sxs-lookup"><span data-stu-id="59131-104">Configuration of TTL Limits</span></span>

<span data-ttu-id="59131-105">用戶端可以要求介於1到 31557600 (的 TTL 值，也就是1秒到1年的) 。</span><span class="sxs-lookup"><span data-stu-id="59131-105">A client can request a TTL value for an entry ranging between 1 and 31557600 (that is, from 1 second to 1 year).</span></span> <span data-ttu-id="59131-106">這個屬性值範圍將會由 **entryTTL** 屬性的 **attributeSchema** 定義中的 **rangeLower** 和 **rangeUpper** 屬性值強制執行。</span><span class="sxs-lookup"><span data-stu-id="59131-106">This attribute value range will be enforced by the **rangeLower** and **rangeUpper** attribute values in the **attributeSchema** definition for the **entryTTL** attribute.</span></span> <span data-ttu-id="59131-107">根據 RFC 2589，目錄伺服器不需要接受此值，而且可能會傳回不同的 TTL 值給用戶端。</span><span class="sxs-lookup"><span data-stu-id="59131-107">As per RFC 2589, directory servers are not required to accept this value and might return a different TTL value to the client.</span></span> <span data-ttu-id="59131-108">用戶端必須能夠使用此伺服器指示的值做為其用戶端重新整理期間 (CRP) 這會控制用戶端對動態專案執行重新整理作業所需的頻率。</span><span class="sxs-lookup"><span data-stu-id="59131-108">Clients must be able to use this server-dictated value as their client refresh period (CRP) which will govern how often the client will need to perform the refresh operation on the dynamic entry.</span></span>

<span data-ttu-id="59131-109">Active Directory Domain Services 讓系統管理員能夠設定樹系的預設和最小 TTL 值。</span><span class="sxs-lookup"><span data-stu-id="59131-109">Active Directory Domain Services provide administrators with the ability to configure the default and minimum TTL values for a forest.</span></span> <span data-ttu-id="59131-110">如果未明確指定 TTL，預設 TTL 值會指派給新建立的動態專案。</span><span class="sxs-lookup"><span data-stu-id="59131-110">The default TTL value is what will be assigned to a newly created dynamic entry if a TTL is not explicitly specified.</span></span> <span data-ttu-id="59131-111">TTL 的最小值會覆寫低於設定的最小值的任何用戶端指定的 TTL 值。</span><span class="sxs-lookup"><span data-stu-id="59131-111">The minimum TTL will override any client specified TTL value that is lower than the configured minimum.</span></span> <span data-ttu-id="59131-112">不需要提供可設定的最大 TTL 值，因為 **attributeSchema** 物件中的 **rangeUpper** 屬性值會加上最大值。</span><span class="sxs-lookup"><span data-stu-id="59131-112">No configurable maximum TTL value needs to be provided because a maximum will be imposed by the **rangeUpper** attribute value in the **attributeSchema** object.</span></span> <span data-ttu-id="59131-113">允許系統管理員設定這些值，可讓他們設定 TTL 值以強制執行低重新整理流量，或在其他極端的情況下提供高度最新的目錄。</span><span class="sxs-lookup"><span data-stu-id="59131-113">Allowing administrators to configure these values will enable them to set TTL values which will enforce a low refresh traffic or, at the other extreme, provide a highly up-to-date directory.</span></span>

<span data-ttu-id="59131-114">這兩個可設定 TTL 參數的預設值如下所示：</span><span class="sxs-lookup"><span data-stu-id="59131-114">The default values for the two configurable TTL parameters will be as follows:</span></span>

-   <span data-ttu-id="59131-115">預設 TTL 值 = 86400 秒 (1 天) </span><span class="sxs-lookup"><span data-stu-id="59131-115">Default TTL value = 86400 seconds (1 day)</span></span>
-   <span data-ttu-id="59131-116">最小 TTL 值 = 900 秒 (15 分鐘) </span><span class="sxs-lookup"><span data-stu-id="59131-116">Minimum TTL value = 900 seconds (15 minutes)</span></span>

<span data-ttu-id="59131-117">可設定的 TTL 參數將會儲存為 AVA (屬性值判斷提示) "<value-name>= 格式的專案</span><span class="sxs-lookup"><span data-stu-id="59131-117">The configurable TTL parameters will be stored as AVA (attribute value assertion) entries of the form "<value-name>=</span></span><value><span data-ttu-id="59131-118">在設定磁碟分割的下列 DN 所提供的 NTDS-Service 物件的屬性中，以 **MS DS-其他設定** ：</span><span class="sxs-lookup"><span data-stu-id="59131-118">" in the attribute **ms-DS-Other-Settings** of the NTDS-Service object given by the following DN in the Configuration partition:</span></span>


```C++
CN=Directory Service,CN=Windows NT,CN=Services,CN=Configuration,DC=...
```



<span data-ttu-id="59131-119">確切的 AVA 語法（針對兩個可設定的 TTL 參數）如下所示，其中 NNNN 以秒為單位來表示：</span><span class="sxs-lookup"><span data-stu-id="59131-119">The exact AVA syntax, for the two configurable TTL parameters, is as follows where NNNN is expressed in seconds:</span></span>


```C++
DynamicObjectDefaultTTLSeconds=NNNN
```




```C++
DynamicObjectMinTTLSeconds=NNNN
```



<span data-ttu-id="59131-120">系統管理員可以透過命令列公用程式 ntdsutil 來設定這些值。</span><span class="sxs-lookup"><span data-stu-id="59131-120">These values can be set by an administrator through the command-line utility ntdsutil.</span></span>

 

 




