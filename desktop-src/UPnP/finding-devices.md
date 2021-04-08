---
title: 尋找裝置
description: UPnP 架構是一種動態網路架構，可讓裝置隨時加入並離開網路。
ms.assetid: b89d9ec3-ce1a-4162-bf82-b08a49207d7d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c5b8feebd430252b118353681a90ce4cd683ee7b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104021913"
---
# <a name="finding-devices"></a><span data-ttu-id="0397f-103">尋找裝置</span><span class="sxs-lookup"><span data-stu-id="0397f-103">Finding Devices</span></span>

<span data-ttu-id="0397f-104">UPnP 架構是一種動態網路架構，可讓裝置隨時加入並離開網路。</span><span class="sxs-lookup"><span data-stu-id="0397f-104">The UPnP architecture is a dynamic network architecture that allows devices to join and leave the network at any time.</span></span> <span data-ttu-id="0397f-105">由於這個動態架構，應用程式無法依賴特定的 UPnP 型裝置在任何指定時間都可供使用。</span><span class="sxs-lookup"><span data-stu-id="0397f-105">Because of this dynamic architecture, applications cannot rely on specific UPnP-based devices to be available at any given time.</span></span> <span data-ttu-id="0397f-106">基於這個理由，應用程式 (或控制點) 搜尋網路，找出最符合指定準則的裝置。</span><span class="sxs-lookup"><span data-stu-id="0397f-106">For this reason, applications (or control points) search the network to find devices that most closely match specified criteria.</span></span> <span data-ttu-id="0397f-107">應用程式也會等待裝置通告訊息，指出已將新的裝置新增至網路。</span><span class="sxs-lookup"><span data-stu-id="0397f-107">Applications also wait for device advertisement messages that indicate new devices have been added to the network.</span></span>

<span data-ttu-id="0397f-108">以下是以 UPnP 為基礎之裝置的有效搜尋準則：</span><span class="sxs-lookup"><span data-stu-id="0397f-108">The following are valid search criteria for UPnP-based devices:</span></span>

-   <span data-ttu-id="0397f-109">裝置類型</span><span class="sxs-lookup"><span data-stu-id="0397f-109">Device type</span></span>
-   <span data-ttu-id="0397f-110">服務類型</span><span class="sxs-lookup"><span data-stu-id="0397f-110">Service type</span></span>
-   <span data-ttu-id="0397f-111">唯一的裝置名稱 (UDN) </span><span class="sxs-lookup"><span data-stu-id="0397f-111">Unique device name (UDN)</span></span>
-   <span data-ttu-id="0397f-112">所有根裝置</span><span class="sxs-lookup"><span data-stu-id="0397f-112">All root devices</span></span>

<span data-ttu-id="0397f-113">裝置類型和服務類型搜尋通常用來尋找具有一般特性的裝置類別。</span><span class="sxs-lookup"><span data-stu-id="0397f-113">The device type and service type searches are typically used to find a class of devices with common characteristics.</span></span> <span data-ttu-id="0397f-114">UDN 搜尋可用來尋找特定裝置。</span><span class="sxs-lookup"><span data-stu-id="0397f-114">The UDN search is used to find a specific device.</span></span>

<span data-ttu-id="0397f-115">若要搜尋裝置，應用程式必須先具現化裝置搜尋工具物件。</span><span class="sxs-lookup"><span data-stu-id="0397f-115">To search for devices, an application must first instantiate the Device Finder object.</span></span> <span data-ttu-id="0397f-116">此物件會公開 [**IUPnPDeviceFinder**](/windows/desktop/api/Upnp/nn-upnp-iupnpdevicefinder) 介面;其方法會執行先前所述的搜尋。</span><span class="sxs-lookup"><span data-stu-id="0397f-116">This object exposes the [**IUPnPDeviceFinder**](/windows/desktop/api/Upnp/nn-upnp-iupnpdevicefinder) interface; its methods perform the previously described searches.</span></span>

<span data-ttu-id="0397f-117">下列各節說明尋找裝置的程式：</span><span class="sxs-lookup"><span data-stu-id="0397f-117">The following sections describe the process of finding devices:</span></span>

-   [<span data-ttu-id="0397f-118">建立裝置搜尋工具</span><span class="sxs-lookup"><span data-stu-id="0397f-118">Creating the Device Finder</span></span>](creating-the-device-finder.md)
-   [<span data-ttu-id="0397f-119">非同步搜尋</span><span class="sxs-lookup"><span data-stu-id="0397f-119">Asynchronous Searching</span></span>](asynchronous-searching.md)
-   [<span data-ttu-id="0397f-120">同步搜尋</span><span class="sxs-lookup"><span data-stu-id="0397f-120">Synchronous Searching</span></span>](synchronous-searching.md)
-   [<span data-ttu-id="0397f-121">同步搜尋所傳回的裝置集合</span><span class="sxs-lookup"><span data-stu-id="0397f-121">Device Collections Returned By Synchronous Searches</span></span>](device-collections-returned-by-synchronous-searches.md)

 

 




