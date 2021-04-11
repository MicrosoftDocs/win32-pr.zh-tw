---
title: DLL 和服務提供者的名稱解析
description: 下列段落描述 Ws2 \_32.dll 以及命名空間提供者如何執行 WINSOCK API 所支援的名稱解析服務。
ms.assetid: 25fcb1c2-2d28-41a0-9124-05608f22420f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b527f0849eb441ab7bc8d096c0198d703f2ce337
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103943421"
---
# <a name="name-resolution-for-dll-and-service-providers"></a><span data-ttu-id="a1f8d-103">DLL 和服務提供者的名稱解析</span><span class="sxs-lookup"><span data-stu-id="a1f8d-103">Name resolution for DLL and service providers</span></span>

<span data-ttu-id="a1f8d-104">下列段落描述 Ws2 \_32.dll 以及命名空間提供者如何執行 WINSOCK API 所支援的名稱解析服務。</span><span class="sxs-lookup"><span data-stu-id="a1f8d-104">The following paragraphs describe how the Ws2\_32.dll and the namespace providers implement the name resolution services supported by the Winsock API.</span></span>

## <a name="ws2_32dll-functionality-for-name-resolution"></a><span data-ttu-id="a1f8d-105">Ws2 \_32.dll 的名稱解析功能</span><span class="sxs-lookup"><span data-stu-id="a1f8d-105">Ws2\_32.dll Functionality for Name Resolution</span></span>

<span data-ttu-id="a1f8d-106">Ws2 \_32.dll 會管理個別命名空間提供者 dll 的註冊和需求載入。</span><span class="sxs-lookup"><span data-stu-id="a1f8d-106">The Ws2\_32.dll manages the registration and demand loading of individual namespace provider DLLs.</span></span> <span data-ttu-id="a1f8d-107">它也負責將命名空間作業從 Windows 通訊端2應用程式路由至適當的命名空間提供者集合。</span><span class="sxs-lookup"><span data-stu-id="a1f8d-107">It also is responsible for routing namespace operations from a Windows Sockets 2 application to the appropriate set of namespace providers.</span></span> <span data-ttu-id="a1f8d-108">此對應是由命名空間的值和服務提供者識別碼參數的值所控制，這些參數可在個別 API 函式中找到。</span><span class="sxs-lookup"><span data-stu-id="a1f8d-108">This mapping is governed by the value of namespace and service provider identifier parameters that are found in individual API functions.</span></span> <span data-ttu-id="a1f8d-109">一般而言，參考特定命名空間提供者時，作業只會路由至識別的提供者。</span><span class="sxs-lookup"><span data-stu-id="a1f8d-109">As a general rule, when a specific namespace provider is referenced, the operation is only routed to an identified provider.</span></span> <span data-ttu-id="a1f8d-110">如果命名空間提供者識別碼為 null，但參考了特定的命名空間，則作業會路由至所有支援已識別之命名空間的命名空間提供者。</span><span class="sxs-lookup"><span data-stu-id="a1f8d-110">If the namespace provider identifier is null but a particular namespace is referenced, the operation is routed to all namespace providers that support the identified namespace.</span></span> <span data-ttu-id="a1f8d-111">如果命名空間提供者識別碼為 null，且命名空間識別碼已指定為 NS \_ all，則作業會路由傳送至所有使用中的命名空間提供者。</span><span class="sxs-lookup"><span data-stu-id="a1f8d-111">If the namespace provider identifier is null and the namespace identifier is given as NS\_ALL, then the operation is routed to all active namespace providers.</span></span>

<span data-ttu-id="a1f8d-112">在開始查詢一或多個服務提供者時，Ws232.dll 會配置 \_ 物件來追蹤查詢的進行中狀態。</span><span class="sxs-lookup"><span data-stu-id="a1f8d-112">As part of starting a query to one or more service providers, the Ws2\_32.dll allocates an object to keep track of the ongoing state of the query.</span></span> <span data-ttu-id="a1f8d-113">表示這個物件的不透明控制碼會傳回給啟動查詢的應用程式。</span><span class="sxs-lookup"><span data-stu-id="a1f8d-113">An opaque handle representing this object is returned to the application that started the query.</span></span> <span data-ttu-id="a1f8d-114">應用程式會在每次重複呼叫應用程式介面函式時，將這個控制碼作為參數提供，以抓取查詢所產生的下一個資料單位。</span><span class="sxs-lookup"><span data-stu-id="a1f8d-114">The application supplies this handle as a parameter each time it repetitively calls an application interface function to retrieve the next unit of data resulting from the query.</span></span>

<span data-ttu-id="a1f8d-115">為了回應這些應用程式介面程序呼叫，Ws2 \_32.dll 會使用它儲存在物件中的資訊，來對查詢中所涉及的命名空間提供者進行對應的呼叫。</span><span class="sxs-lookup"><span data-stu-id="a1f8d-115">In response to these application interface procedure calls, the Ws2\_32.dll uses the information it stores in the object to make corresponding calls to the namespace providers involved in the query.</span></span> <span data-ttu-id="a1f8d-116">Ws2 \_32.dll 會在每次進行後續的應用程式介面呼叫時，更新其物件中的資訊，以便對應至命名空間提供者的呼叫會透過查詢所涉及的所有命名空間提供者適當地進行。</span><span class="sxs-lookup"><span data-stu-id="a1f8d-116">The Ws2\_32.dll updates the information in its object as each successive application interface call occurs so that the corresponding calls to namespace providers progress appropriately through all of the namespace providers involved in the query.</span></span>

## <a name="namespace-provider-functionality"></a><span data-ttu-id="a1f8d-117">命名空間提供者功能</span><span class="sxs-lookup"><span data-stu-id="a1f8d-117">Namespace Provider Functionality</span></span>

<span data-ttu-id="a1f8d-118">每個命名空間提供者都會負責將出現在 Windows 通訊端2名稱解析 SPI 中的一組函式，對應至具有支援命名空間的適當交易。</span><span class="sxs-lookup"><span data-stu-id="a1f8d-118">Each namespace provider is responsible for mapping the set of functions appearing in the Windows Sockets 2 name resolution SPI to the appropriate transactions with the supported namespace.</span></span> <span data-ttu-id="a1f8d-119">在某些情況下，這主要是將 SPI 對應至命名空間的任何原生介面。</span><span class="sxs-lookup"><span data-stu-id="a1f8d-119">In some cases, this is primarily a matter of mapping the SPI to whatever native interface exists for the namespace.</span></span> <span data-ttu-id="a1f8d-120">在其他情況下，命名空間提供者必須透過網路與命名空間提供者進行交易。</span><span class="sxs-lookup"><span data-stu-id="a1f8d-120">In others, the namespace provider must conduct transactions with the namespace provider over the network.</span></span> <span data-ttu-id="a1f8d-121">有些命名空間提供者會藉由呼叫 Windows 通訊端 API 來執行這項作業，而其他命名空間會使用私用介面來建立相關聯的傳輸堆疊</span><span class="sxs-lookup"><span data-stu-id="a1f8d-121">Some namespace providers will do this by making calls to the Windows Sockets API, others will use private interfaces to associated transport stacks.</span></span>

 

 



