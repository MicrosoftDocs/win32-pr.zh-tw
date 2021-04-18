---
title: 裝置主機 API 參考
description: 下列介面是裝置主機 API 與 UPnP 技術的一部分。 具有 UPnP 技術的裝置主機支援 Microsoft Visual Basic 和 c + +。
ms.assetid: 48e20a09-7e78-4b8d-aa16-78751b6fb586
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a62f42b43efcc1d51eb5e5581770260238640469
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104372438"
---
# <a name="device-host-api-reference"></a><span data-ttu-id="756a5-104">裝置主機 API 參考</span><span class="sxs-lookup"><span data-stu-id="756a5-104">Device Host API Reference</span></span>

<span data-ttu-id="756a5-105">下列介面是裝置主機 API 與 UPnP 技術的一部分。</span><span class="sxs-lookup"><span data-stu-id="756a5-105">The following interfaces are part of the Device Host API with UPnP technology.</span></span> <span data-ttu-id="756a5-106">具有 UPnP 技術的裝置主機支援 Microsoft Visual Basic 和 c + +。</span><span class="sxs-lookup"><span data-stu-id="756a5-106">The Device Host with UPnP technology supports Microsoft Visual Basic and C++.</span></span>

<span data-ttu-id="756a5-107">此 API 不提供 Microsoft Visual Basic Scripting Edition (VBScript) 的支援。</span><span class="sxs-lookup"><span data-stu-id="756a5-107">This API does not provide support for Microsoft Visual Basic Scripting Edition (VBScript).</span></span>



| <span data-ttu-id="756a5-108">介面</span><span class="sxs-lookup"><span data-stu-id="756a5-108">Interface</span></span>                                                  | <span data-ttu-id="756a5-109">描述</span><span class="sxs-lookup"><span data-stu-id="756a5-109">Description</span></span>                                                                                         |
|------------------------------------------------------------|-----------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="756a5-110">**IUPnPDeviceControl**</span><span class="sxs-lookup"><span data-stu-id="756a5-110">**IUPnPDeviceControl**</span></span>](/windows/desktop/api/Upnphost/nn-upnphost-iupnpdevicecontrol)           | <span data-ttu-id="756a5-111">由裝置主機用來管理裝置和相關服務。</span><span class="sxs-lookup"><span data-stu-id="756a5-111">Used by the device host to manage devices and related services.</span></span>                                     |
| [<span data-ttu-id="756a5-112">**IUPnPDeviceProvider**</span><span class="sxs-lookup"><span data-stu-id="756a5-112">**IUPnPDeviceProvider**</span></span>](/windows/desktop/api/Upnphost/nn-upnphost-iupnpdeviceprovider)         | <span data-ttu-id="756a5-113">由裝置主機用來啟動和停止裝置提供者。</span><span class="sxs-lookup"><span data-stu-id="756a5-113">Used by the device host to start and stop device providers.</span></span>                                         |
| [<span data-ttu-id="756a5-114">**IUPnPEventSink**</span><span class="sxs-lookup"><span data-stu-id="756a5-114">**IUPnPEventSink**</span></span>](/windows/desktop/api/Upnphost/nn-upnphost-iupnpeventsink)                   | <span data-ttu-id="756a5-115">供裝置用來將事件通知傳送至裝置主機。</span><span class="sxs-lookup"><span data-stu-id="756a5-115">Used by devices to send event notifications to the device host.</span></span>                                     |
| [<span data-ttu-id="756a5-116">**IUPnPEventSource**</span><span class="sxs-lookup"><span data-stu-id="756a5-116">**IUPnPEventSource**</span></span>](/windows/desktop/api/Upnphost/nn-upnphost-iupnpeventsource)               | <span data-ttu-id="756a5-117">由裝置主機用來訂閱或取消訂閱託管服務所提供的事件。</span><span class="sxs-lookup"><span data-stu-id="756a5-117">Used by the device host to subscribe or unsubscribe to events provided by the hosted service.</span></span>       |
| [<span data-ttu-id="756a5-118">**IUPnPRegistrar**</span><span class="sxs-lookup"><span data-stu-id="756a5-118">**IUPnPRegistrar**</span></span>](/windows/desktop/api/Upnphost/nn-upnphost-iupnpregistrar)                   | <span data-ttu-id="756a5-119">供裝置用來向裝置主機註冊。</span><span class="sxs-lookup"><span data-stu-id="756a5-119">Used by devices to register with the device host.</span></span>                                                   |
| [<span data-ttu-id="756a5-120">**IUPnPRemoteEndpointInfo**</span><span class="sxs-lookup"><span data-stu-id="756a5-120">**IUPnPRemoteEndpointInfo**</span></span>](/windows/desktop/api/Upnphost/nn-upnphost-iupnpremoteendpointinfo) | <span data-ttu-id="756a5-121">裝置用來取得要求者的相關資訊 (也就是控制點) 和要求。</span><span class="sxs-lookup"><span data-stu-id="756a5-121">Used by devices to obtain information about a requester (that is, a control point) and the request.</span></span> |
| [<span data-ttu-id="756a5-122">**IUPnPReregistrar**</span><span class="sxs-lookup"><span data-stu-id="756a5-122">**IUPnPReregistrar**</span></span>](/windows/desktop/api/Upnphost/nn-upnphost-iupnpreregistrar)               | <span data-ttu-id="756a5-123">供裝置用來向裝置主機重新註冊。</span><span class="sxs-lookup"><span data-stu-id="756a5-123">Used by devices to re-register with the device host.</span></span>                                                |



 

 

 




