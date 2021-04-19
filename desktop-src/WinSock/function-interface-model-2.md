---
description: Windows 通訊端傳輸和命名空間&\# 8211; 服務提供者是 dll，分別具有服務提供者初始化函數 WSPStartup 或 NSPStartup 的單一匯出程式進入點。
ms.assetid: a3422513-92e2-4011-a756-04ed853e9d56
title: 函數介面模型
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4a500de391dd5f65da610ba79d33938443794262
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106972217"
---
# <a name="function-interface-model"></a><span data-ttu-id="6879e-103">函數介面模型</span><span class="sxs-lookup"><span data-stu-id="6879e-103">Function Interface Model</span></span>

<span data-ttu-id="6879e-104">Windows 通訊端傳輸和命名空間-服務提供者是具有單一匯出程式進入點的 Dll，分別適用于服務提供者初始化函數 [**WSPStartup**](/windows/desktop/api/Ws2spi/nf-ws2spi-wspstartup) 或 [**NSPStartup**](/windows/desktop/api/Ws2spi/nf-ws2spi-nspstartup)。</span><span class="sxs-lookup"><span data-stu-id="6879e-104">Windows Sockets transport and namespace–service providers are DLLs with a single exported procedure entry point for the service provider initialization function [**WSPStartup**](/windows/desktop/api/Ws2spi/nf-ws2spi-wspstartup) or [**NSPStartup**](/windows/desktop/api/Ws2spi/nf-ws2spi-nspstartup), respectively.</span></span> <span data-ttu-id="6879e-105">Ws2 \_32.dll 可透過服務提供者的分派資料表存取所有其他服務提供者函數。</span><span class="sxs-lookup"><span data-stu-id="6879e-105">All other service provider functions are made accessible to the Ws2\_32.dll through the service provider's dispatch table.</span></span> <span data-ttu-id="6879e-106">只有在需要時，Ws232.dll 會將服務提供者 DLL 載入記憶體中，並在不再需要服務提供者 DLL \_ 時將其卸載。</span><span class="sxs-lookup"><span data-stu-id="6879e-106">Service provider DLL's are loaded into memory by the Ws2\_32.dll only when needed, and are unloaded when their services are no longer required.</span></span>

<span data-ttu-id="6879e-107">SPI 也會定義傳輸服務提供者呼叫 Ws2 \_32.dll (upcalls) 以取得 DLL 支援服務的幾種情況。</span><span class="sxs-lookup"><span data-stu-id="6879e-107">The SPI also defines several circumstances in which a transport service provider calls up into the Ws2\_32.dll (upcalls) to obtain DLL support services.</span></span> <span data-ttu-id="6879e-108">\_透過 [**WSPStartup**](/windows/desktop/api/Ws2spi/nf-ws2spi-wspstartup)的 *UpcallTable* 參數，提供 Ws232.dll 的 upcall 分派資料表給傳輸服務提供者 DLL。</span><span class="sxs-lookup"><span data-stu-id="6879e-108">The transport service provider DLL is given the Ws2\_32.dll's upcall dispatch table through the *UpcallTable* parameter to [**WSPStartup**](/windows/desktop/api/Ws2spi/nf-ws2spi-wspstartup).</span></span>

<span data-ttu-id="6879e-109">服務提供者的副檔名必須從 "DLL" 變更為 "。WSP 「或」。NSP」。</span><span class="sxs-lookup"><span data-stu-id="6879e-109">Service providers should have their file name extension changed from "DLL" to ".WSP" or ".NSP".</span></span> <span data-ttu-id="6879e-110">這項需求不是嚴格的。</span><span class="sxs-lookup"><span data-stu-id="6879e-110">This requirement is not strict.</span></span> <span data-ttu-id="6879e-111">服務提供者仍會使用具有任何副檔名的 Ws232.dll 來操作 \_ 。</span><span class="sxs-lookup"><span data-stu-id="6879e-111">A service provider will still operate with the Ws2\_32.dll with any file name extension.</span></span>

<span data-ttu-id="6879e-112">Winsock SPI 會使用下列函數首碼命名慣例：</span><span class="sxs-lookup"><span data-stu-id="6879e-112">The Winsock SPI uses the following function prefix naming convention:</span></span>

| <span data-ttu-id="6879e-113">前置詞</span><span class="sxs-lookup"><span data-stu-id="6879e-113">Prefix</span></span> | <span data-ttu-id="6879e-114">意義</span><span class="sxs-lookup"><span data-stu-id="6879e-114">Meaning</span></span>                          | <span data-ttu-id="6879e-115">Description</span><span class="sxs-lookup"><span data-stu-id="6879e-115">Description</span></span>                                       |
|--------|----------------------------------|---------------------------------------------------|
| <span data-ttu-id="6879e-116">WSP</span><span class="sxs-lookup"><span data-stu-id="6879e-116">WSP</span></span>    | <span data-ttu-id="6879e-117">Windows 通訊端服務提供者</span><span class="sxs-lookup"><span data-stu-id="6879e-117">Windows Sockets Service Provider</span></span> | <span data-ttu-id="6879e-118">傳輸服務提供者進入點</span><span class="sxs-lookup"><span data-stu-id="6879e-118">Transport service provider entry points</span></span>           |
| <span data-ttu-id="6879e-119">WPU</span><span class="sxs-lookup"><span data-stu-id="6879e-119">WPU</span></span>    | <span data-ttu-id="6879e-120">Windows 通訊端提供者 Upcall</span><span class="sxs-lookup"><span data-stu-id="6879e-120">Windows Sockets Provider Upcall</span></span>  | <span data-ttu-id="6879e-121">\_服務提供者的 Ws232.dll 進入點</span><span class="sxs-lookup"><span data-stu-id="6879e-121">Ws2\_32.dll entry points for service providers</span></span>    |
| <span data-ttu-id="6879e-122">WSC</span><span class="sxs-lookup"><span data-stu-id="6879e-122">WSC</span></span>    | <span data-ttu-id="6879e-123">Windows 通訊端設定</span><span class="sxs-lookup"><span data-stu-id="6879e-123">Windows Sockets Configuration</span></span>    | <span data-ttu-id="6879e-124">WS2 \_ 安裝 applet 的32.dll 進入點</span><span class="sxs-lookup"><span data-stu-id="6879e-124">WS2\_32.dll entry points for installation applets</span></span> |
| <span data-ttu-id="6879e-125">Nsp</span><span class="sxs-lookup"><span data-stu-id="6879e-125">NSP</span></span>    | <span data-ttu-id="6879e-126">命名空間提供者</span><span class="sxs-lookup"><span data-stu-id="6879e-126">Namespace Provider</span></span>               | <span data-ttu-id="6879e-127">命名空間提供者進入點</span><span class="sxs-lookup"><span data-stu-id="6879e-127">Namespace provider entry points</span></span>                   |



 

<span data-ttu-id="6879e-128">如上所述，這些進入點不會匯出 (除了 [**WSPStartup**](/windows/desktop/api/Ws2spi/nf-ws2spi-wspstartup) 和 [**NSPStartup**](/windows/desktop/api/Ws2spi/nf-ws2spi-nspstartup)) 之外，還可以透過 exchange 分派資料表來存取。</span><span class="sxs-lookup"><span data-stu-id="6879e-128">As described above, these entry points are not exported (with the exception of [**WSPStartup**](/windows/desktop/api/Ws2spi/nf-ws2spi-wspstartup) and [**NSPStartup**](/windows/desktop/api/Ws2spi/nf-ws2spi-nspstartup)), but are accessed through an exchange of dispatch tables.</span></span>

 

 



