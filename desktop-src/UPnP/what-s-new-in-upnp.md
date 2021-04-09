---
title: UPnP Api 的新功能
description: UPnP™ Api 具有 Windows XP SP2 的新功能和更新的檔。 下表識別新的檔集。
ms.assetid: ad72d9b8-6db4-4b9b-9b10-ae3980521d7e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e27747c6185b5aecea86e240d388ab10410aa29f
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103675767"
---
# <a name="whats-new-in-the-upnp-apis"></a><span data-ttu-id="5e9c0-104">UPnP Api 的新功能</span><span class="sxs-lookup"><span data-stu-id="5e9c0-104">What's New in the UPnP APIs</span></span>

<span data-ttu-id="5e9c0-105">UPnP™ Api 具有 Windows XP SP2 的新功能和更新的檔。</span><span class="sxs-lookup"><span data-stu-id="5e9c0-105">The UPnP™ APIs have new features and updated documentation for Windows XP SP2.</span></span> <span data-ttu-id="5e9c0-106">下表識別新的檔集。</span><span class="sxs-lookup"><span data-stu-id="5e9c0-106">The following table identifies the new documentation.</span></span>



| <span data-ttu-id="5e9c0-107">功能</span><span class="sxs-lookup"><span data-stu-id="5e9c0-107">Feature</span></span>                                                          | <span data-ttu-id="5e9c0-108">描述</span><span class="sxs-lookup"><span data-stu-id="5e9c0-108">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                   |
|------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="5e9c0-109">**IUPnPRemoteEndpointInfo**</span><span class="sxs-lookup"><span data-stu-id="5e9c0-109">**IUPnPRemoteEndpointInfo**</span></span>](/windows/desktop/api/Upnphost/nn-upnphost-iupnpremoteendpointinfo)       | <span data-ttu-id="5e9c0-110">這個新介面可讓託管裝置取得要求者的相關資訊 (也就是控制點) 和要求。</span><span class="sxs-lookup"><span data-stu-id="5e9c0-110">This new interface allows a hosted device to obtain information about a requester (that is, a control point) and the request.</span></span> <span data-ttu-id="5e9c0-111">它包含三種方法，每個方法都提供不同類型的資訊。</span><span class="sxs-lookup"><span data-stu-id="5e9c0-111">It includes three methods, each of which provides a different type of information.</span></span>                                                                                                                                                              |
| [<span data-ttu-id="5e9c0-112">執行裝置行為</span><span class="sxs-lookup"><span data-stu-id="5e9c0-112">Implementing Device Behavior</span></span>](implementing-device-behavior.md) | <span data-ttu-id="5e9c0-113">本主題包含新的章節，說明如何使用新的 [**IUPnPRemoteEndpointInfo**](/windows/desktop/api/Upnphost/nn-upnphost-iupnpremoteendpointinfo) 介面取得端點資訊。</span><span class="sxs-lookup"><span data-stu-id="5e9c0-113">This topic includes a new section that explains how to obtain endpoint information by using the new [**IUPnPRemoteEndpointInfo**](/windows/desktop/api/Upnphost/nn-upnphost-iupnpremoteendpointinfo) interface.</span></span>                                                                                                                                                                                                     |
| [<span data-ttu-id="5e9c0-114">設定</span><span class="sxs-lookup"><span data-stu-id="5e9c0-114">Configuration Settings</span></span>](configuration-settings.md)             | <span data-ttu-id="5e9c0-115">此新主題提供影響 UPnP Api 行為之登錄設定的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="5e9c0-115">This new topic provides information about the registry settings that affect the behavior of the UPnP APIs.</span></span>                                                                                                                                                                                                                                                                    |
| [<span data-ttu-id="5e9c0-116">裝置錯誤碼</span><span class="sxs-lookup"><span data-stu-id="5e9c0-116">Device Error Codes</span></span>](device-error-codes.md)                     | <span data-ttu-id="5e9c0-117">這個新的主題說明如何將裝置的錯誤碼轉換成 HRESULT 值，反之亦然。</span><span class="sxs-lookup"><span data-stu-id="5e9c0-117">This new topic explains how an error code from a device is converted to an HRESULT value and vice versa.</span></span> <span data-ttu-id="5e9c0-118">您必須瞭解此程式，才能評估 [**IUPnPService：： InvokeAction**](/windows/desktop/api/Upnp/nf-upnp-iupnpservice-invokeaction) 和 [**IUPnPService：： QueryStateVariable**](/windows/desktop/api/Upnp/nf-upnp-iupnpservice-querystatevariable) 方法所傳回的 HRESULT 值。</span><span class="sxs-lookup"><span data-stu-id="5e9c0-118">An understanding of this process is necessary in order to evaluate an HRESULT value that is returned by the [**IUPnPService::InvokeAction**](/windows/desktop/api/Upnp/nf-upnp-iupnpservice-invokeaction) and [**IUPnPService::QueryStateVariable**](/windows/desktop/api/Upnp/nf-upnp-iupnpservice-querystatevariable) methods.</span></span> |



 

 

 




