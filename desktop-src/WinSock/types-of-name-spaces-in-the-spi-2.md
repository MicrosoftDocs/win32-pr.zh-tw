---
description: Windows 通訊端中的三種命名空間類型 (Winsock) SPI 包含動態、靜態和持續性的命名空間。
ms.assetid: 2968ac98-bd40-4d37-9dd7-7870c4decd40
title: SPI 中的命名空間類型
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2e40356987c67604755696f1a8b7224de15851ee
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106983806"
---
# <a name="types-of-namespaces-in-the-spi"></a><span data-ttu-id="43942-103">SPI 中的命名空間類型</span><span class="sxs-lookup"><span data-stu-id="43942-103">Types of Namespaces in the SPI</span></span>

<span data-ttu-id="43942-104">有三種不同類型的命名空間，可在其中註冊服務：</span><span class="sxs-lookup"><span data-stu-id="43942-104">There are three different types of namespaces in which a service could be registered:</span></span>

-   <span data-ttu-id="43942-105">動態</span><span class="sxs-lookup"><span data-stu-id="43942-105">Dynamic</span></span>
-   <span data-ttu-id="43942-106">Static</span><span class="sxs-lookup"><span data-stu-id="43942-106">Static</span></span>
-   <span data-ttu-id="43942-107">持續性</span><span class="sxs-lookup"><span data-stu-id="43942-107">Persistent</span></span>

<span data-ttu-id="43942-108">動態命名空間可讓服務即時註冊命名空間，並讓用戶端在執行時間探索可用的服務。</span><span class="sxs-lookup"><span data-stu-id="43942-108">Dynamic namespaces allow services to register with the namespace on the fly, and for clients to discover the available services at run time.</span></span> <span data-ttu-id="43942-109">動態命名空間經常依賴廣播來指出網路服務的持續可用性。</span><span class="sxs-lookup"><span data-stu-id="43942-109">Dynamic namespaces frequently rely on broadcasts to indicate the continued availability of a network service.</span></span> <span data-ttu-id="43942-110">動態命名空間的範例包括 NetWare 環境內使用的 SAP 命名空間，以及 AppleTalk 使用的 NBP 命名空間。</span><span class="sxs-lookup"><span data-stu-id="43942-110">Examples of dynamic namespaces include the SAP namespace used within a NetWare environment and the NBP namespace used by AppleTalk.</span></span>

<span data-ttu-id="43942-111">靜態命名空間需要預先註冊所有服務，也就是建立命名空間的時候。</span><span class="sxs-lookup"><span data-stu-id="43942-111">Static namespaces require all of the services to be registered ahead of time, that is, when the namespace is created.</span></span> <span data-ttu-id="43942-112">DNS 是靜態命名空間的範例。</span><span class="sxs-lookup"><span data-stu-id="43942-112">The DNS is an example of a static namespace.</span></span> <span data-ttu-id="43942-113">雖然有程式設計方式來解析名稱，但沒有程式設計方式可註冊名稱。</span><span class="sxs-lookup"><span data-stu-id="43942-113">Although there is a programmatic way to resolve names, there is no programmatic way to register names.</span></span>

<span data-ttu-id="43942-114">持續性命名空間可讓服務即時註冊命名空間。</span><span class="sxs-lookup"><span data-stu-id="43942-114">Persistent namespaces allow services to register with the namespace on the fly.</span></span> <span data-ttu-id="43942-115">但不同于動態命名空間，持續性命名空間會保留靜態儲存體中的註冊資訊，在此情況下，它會一直保留到服務要求移除時為止。</span><span class="sxs-lookup"><span data-stu-id="43942-115">Unlike dynamic namespaces however, persistent namespaces retain the registration information in nonvolatile storage where it remains until such time as the service requests that it be removed.</span></span> <span data-ttu-id="43942-116">持續性的命名空間是由目錄服務（例如 X. 500 和 NDS (NetWare 目錄服務) ）所 typified。</span><span class="sxs-lookup"><span data-stu-id="43942-116">Persistent namespaces are typified by directory services such as X.500 and the NDS (NetWare Directory Service).</span></span> <span data-ttu-id="43942-117">這些環境可讓您新增、刪除和修改服務屬性。</span><span class="sxs-lookup"><span data-stu-id="43942-117">These environments allow the adding, deleting, and modification of service properties.</span></span> <span data-ttu-id="43942-118">此外，代表目錄服務內之服務的服務物件可以有各種與服務相關聯的屬性。</span><span class="sxs-lookup"><span data-stu-id="43942-118">In addition, the service object representing the service within the directory service could have a variety of attributes associated with the service.</span></span> <span data-ttu-id="43942-119">用戶端應用程式最重要的屬性是服務的定址資訊。</span><span class="sxs-lookup"><span data-stu-id="43942-119">The most important attribute for client applications is the service's addressing information.</span></span>

 

 



