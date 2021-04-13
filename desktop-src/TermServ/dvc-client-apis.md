---
title: DVC 用戶端 Api
description: 動態虛擬通道 (DVC) 用戶端 Api 專門針對連接的遠端桌面連線 (RDC) 用戶端。
ms.assetid: 976a6cc2-7bbe-4ecc-91b4-b7c659eca5ba
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 25c29d360fb0ad4d6e31e828f9c62f42f64fb311
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104300620"
---
# <a name="dvc-client-apis"></a><span data-ttu-id="fa687-103">DVC 用戶端 Api</span><span class="sxs-lookup"><span data-stu-id="fa687-103">DVC Client APIs</span></span>

<span data-ttu-id="fa687-104">動態虛擬通道 (DVC) 用戶端 Api 專門針對連接的遠端桌面連線 (RDC) 用戶端。</span><span class="sxs-lookup"><span data-stu-id="fa687-104">The dynamic virtual channel (DVC) client APIs are implemented specifically for the Remote Desktop Connection (RDC) client of the connection.</span></span> <span data-ttu-id="fa687-105">某些 Api 是由 DVC 架構所執行，而有些則是由外掛程式開發人員所執行。</span><span class="sxs-lookup"><span data-stu-id="fa687-105">Some of the APIs are implemented by the DVC framework, and some are implemented by the plug-in developer.</span></span> <span data-ttu-id="fa687-106">某些 Api 是用來支援遠端桌面連線 (RDC) 用戶端外掛程式，且不會與資料傳輸直接相關。</span><span class="sxs-lookup"><span data-stu-id="fa687-106">Some of the APIs are used to support the Remote Desktop Connection (RDC) client plug-in, and are not directly related to data transport.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="fa687-107">本節內容</span><span class="sxs-lookup"><span data-stu-id="fa687-107">In this section</span></span>

<dl> <dt>

[<span data-ttu-id="fa687-108">**IWTSPlugin**</span><span class="sxs-lookup"><span data-stu-id="fa687-108">**IWTSPlugin**</span></span>](/windows/desktop/api/TsVirtualChannels/nn-tsvirtualchannels-iwtsplugin)
</dt> <dd>

<span data-ttu-id="fa687-109">允許遠端桌面連線 (RDC) 用戶端載入遠端桌面連線 (RDC) 用戶端外掛程式。</span><span class="sxs-lookup"><span data-stu-id="fa687-109">Allows for the Remote Desktop Connection (RDC) client plug-in to be loaded by the Remote Desktop Connection (RDC) client.</span></span>

</dd> <dt>

[<span data-ttu-id="fa687-110">**IWTSListener**</span><span class="sxs-lookup"><span data-stu-id="fa687-110">**IWTSListener**</span></span>](/windows/desktop/api/TsVirtualChannels/nn-tsvirtualchannels-iwtslistener)
</dt> <dd>

<span data-ttu-id="fa687-111">管理動態虛擬通道的每個接聽程式的設定 (DVC) 連接。</span><span class="sxs-lookup"><span data-stu-id="fa687-111">Manages configuration settings for each listener for the dynamic virtual channel (DVC) connection.</span></span>

</dd> <dt>

[<span data-ttu-id="fa687-112">**IWTSListenerCallback**</span><span class="sxs-lookup"><span data-stu-id="fa687-112">**IWTSListenerCallback**</span></span>](/windows/desktop/api/TsVirtualChannels/nn-tsvirtualchannels-iwtslistenercallback)
</dt> <dd>

<span data-ttu-id="fa687-113">用來通知遠端桌面連線 (RDC) 用戶端外掛程式有關特定接聽程式上的傳入要求。</span><span class="sxs-lookup"><span data-stu-id="fa687-113">Used to notify the Remote Desktop Connection (RDC) client plug-in about incoming requests on a particular listener.</span></span>

</dd> <dt>

[<span data-ttu-id="fa687-114">**IWTSVirtualChannelManager**</span><span class="sxs-lookup"><span data-stu-id="fa687-114">**IWTSVirtualChannelManager**</span></span>](/windows/desktop/api/TsVirtualChannels/nn-tsvirtualchannels-iwtsvirtualchannelmanager)
</dt> <dd>

<span data-ttu-id="fa687-115">管理所有遠端桌面連線 (RDC) 用戶端外掛程式和動態虛擬通道 (DVC) 接聽項。</span><span class="sxs-lookup"><span data-stu-id="fa687-115">Manages all Remote Desktop Connection (RDC) client plug-ins and dynamic virtual channel (DVC) listeners.</span></span>

</dd> <dt>

[<span data-ttu-id="fa687-116">**IWTSVirtualChannel**</span><span class="sxs-lookup"><span data-stu-id="fa687-116">**IWTSVirtualChannel**</span></span>](/windows/desktop/api/TsVirtualChannels/nn-tsvirtualchannels-iwtsvirtualchannel)
</dt> <dd>

<span data-ttu-id="fa687-117">用來控制通道狀態，以及在通道上寫入。</span><span class="sxs-lookup"><span data-stu-id="fa687-117">Used to control the channel state, and writes on the channel.</span></span>

</dd> <dt>

[<span data-ttu-id="fa687-118">**IWTSVirtualChannelCallback**</span><span class="sxs-lookup"><span data-stu-id="fa687-118">**IWTSVirtualChannelCallback**</span></span>](/windows/desktop/api/TsVirtualChannels/nn-tsvirtualchannels-iwtsvirtualchannelcallback)
</dt> <dd>

<span data-ttu-id="fa687-119">接收有關通道狀態變更或所收到資料的通知。</span><span class="sxs-lookup"><span data-stu-id="fa687-119">Receives notifications about channel state changes or data received.</span></span>

</dd> <dt>

[<span data-ttu-id="fa687-120">**IWTSVirtualChannelCallback2**</span><span class="sxs-lookup"><span data-stu-id="fa687-120">**IWTSVirtualChannelCallback2**</span></span>](iwtsvirtualchannelcallback2.md)
</dt> <dd>

<span data-ttu-id="fa687-121">不支援此介面。</span><span class="sxs-lookup"><span data-stu-id="fa687-121">This interface is not supported.</span></span>

</dd> <dt>

[<span data-ttu-id="fa687-122">**VirtualChannelGetInstance**</span><span class="sxs-lookup"><span data-stu-id="fa687-122">**VirtualChannelGetInstance**</span></span>](virtualchannelgetinstance.md)
</dt> <dd>

<span data-ttu-id="fa687-123">呼叫以讓外掛程式為 DLL 所執行的所有外掛程式建立 [**IWTSPlugin**](/windows/desktop/api/TsVirtualChannels/nn-tsvirtualchannels-iwtsplugin) 介面的實例。</span><span class="sxs-lookup"><span data-stu-id="fa687-123">Called to have the plug-in create an instance of the [**IWTSPlugin**](/windows/desktop/api/TsVirtualChannels/nn-tsvirtualchannels-iwtsplugin) interface for all plug-ins implemented by the DLL.</span></span>

</dd> </dl>

 

 




