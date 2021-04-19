---
title: 撰寫用戶端 DVC 模組
description: 若要 (DVC) 用戶端模組寫入動態虛擬通道，您必須先執行並註冊遠端桌面連線 (RDC) 用戶端外掛程式。
ms.assetid: b6f475d4-d2ad-41ce-b3b9-d844fbd23cf0
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bcb881fd057132eb416066ffac050f75f4df1b12
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "106966399"
---
# <a name="writing-a-client-dvc-module"></a><span data-ttu-id="b0b4d-103">撰寫用戶端 DVC 模組</span><span class="sxs-lookup"><span data-stu-id="b0b4d-103">Writing a Client DVC Module</span></span>

<span data-ttu-id="b0b4d-104">若要 (DVC) 用戶端模組寫入動態虛擬通道，您必須先執行並註冊遠端桌面連線 (RDC) 用戶端外掛程式。</span><span class="sxs-lookup"><span data-stu-id="b0b4d-104">To write a dynamic virtual channel (DVC) client module, you must first implement and register a Remote Desktop Connection (RDC) client plug-in.</span></span> <span data-ttu-id="b0b4d-105">DVC 外掛程式是 [**IWTSPlugin**](/windows/desktop/api/TsVirtualChannels/nn-tsvirtualchannels-iwtsplugin)的實作為元件物件模型， (COM) 物件來註冊。</span><span class="sxs-lookup"><span data-stu-id="b0b4d-105">The DVC plug-in is an implementation of [**IWTSPlugin**](/windows/desktop/api/TsVirtualChannels/nn-tsvirtualchannels-iwtsplugin), registered as a Component Object Model (COM) object.</span></span>

> [!Note]  
> <span data-ttu-id="b0b4d-106">外掛程式必須在自由執行緒模式中執行。</span><span class="sxs-lookup"><span data-stu-id="b0b4d-106">The plug-in must be implemented in a free-threading model.</span></span> <span data-ttu-id="b0b4d-107">不支援單元模型執行。</span><span class="sxs-lookup"><span data-stu-id="b0b4d-107">Apartment-model implementation is not supported.</span></span>

 

<span data-ttu-id="b0b4d-108">以下是由外掛程式具現化的物件所執行的介面清單。</span><span class="sxs-lookup"><span data-stu-id="b0b4d-108">The following is a list of interfaces that are implemented by objects that are instantiated by the plug-in.</span></span>



| <span data-ttu-id="b0b4d-109">介面</span><span class="sxs-lookup"><span data-stu-id="b0b4d-109">Interface</span></span>                                                        | <span data-ttu-id="b0b4d-110">描述</span><span class="sxs-lookup"><span data-stu-id="b0b4d-110">Description</span></span>                                                                                                                                                                                          |
|------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="b0b4d-111">**IWTSPlugin**</span><span class="sxs-lookup"><span data-stu-id="b0b4d-111">**IWTSPlugin**</span></span>](/windows/desktop/api/TsVirtualChannels/nn-tsvirtualchannels-iwtsplugin)                                 | <span data-ttu-id="b0b4d-112">允許遠端桌面連線 (RDC) 用戶端載入遠端桌面連線 (RDC) 用戶端外掛程式。</span><span class="sxs-lookup"><span data-stu-id="b0b4d-112">Allows for the Remote Desktop Connection (RDC) client plug-in to be loaded by the Remote Desktop Connection (RDC) client.</span></span><br/>                                                                 |
| [<span data-ttu-id="b0b4d-113">**IWTSListenerCallback**</span><span class="sxs-lookup"><span data-stu-id="b0b4d-113">**IWTSListenerCallback**</span></span>](/windows/desktop/api/TsVirtualChannels/nn-tsvirtualchannels-iwtslistenercallback)             | <span data-ttu-id="b0b4d-114">通知遠端桌面連線 (RDC) 用戶端外掛程式有關特定接聽程式上的傳入要求。</span><span class="sxs-lookup"><span data-stu-id="b0b4d-114">Notifies the Remote Desktop Connection (RDC) client plug-in about incoming requests on a particular listener.</span></span><br/>                                                                             |
| [<span data-ttu-id="b0b4d-115">**IWTSVirtualChannelCallback**</span><span class="sxs-lookup"><span data-stu-id="b0b4d-115">**IWTSVirtualChannelCallback**</span></span>](/windows/desktop/api/TsVirtualChannels/nn-tsvirtualchannels-iwtsvirtualchannelcallback) | <span data-ttu-id="b0b4d-116">接收有關通道狀態變更或所收到資料的通知。</span><span class="sxs-lookup"><span data-stu-id="b0b4d-116">Receives notifications about channel state changes or data received.</span></span> <span data-ttu-id="b0b4d-117">這個介面的每個實例都與一個 [**IWTSVirtualChannel**](/windows/desktop/api/TsVirtualChannels/nn-tsvirtualchannels-iwtsvirtualchannel)的實例相關聯。</span><span class="sxs-lookup"><span data-stu-id="b0b4d-117">Each instance of this interface is associated with one instance of [**IWTSVirtualChannel**](/windows/desktop/api/TsVirtualChannels/nn-tsvirtualchannels-iwtsvirtualchannel).</span></span><br/> |



 

<span data-ttu-id="b0b4d-118">以下是由遠端桌面連線 (RDC) 用戶端所具現化的物件所執行的介面清單，而且是架構的一部分。</span><span class="sxs-lookup"><span data-stu-id="b0b4d-118">The following is a list of interfaces that are implemented by objects that are instantiated by the Remote Desktop Connection (RDC) client, and are part of the framework.</span></span>



| <span data-ttu-id="b0b4d-119">介面</span><span class="sxs-lookup"><span data-stu-id="b0b4d-119">Interface</span></span>                                                      | <span data-ttu-id="b0b4d-120">描述</span><span class="sxs-lookup"><span data-stu-id="b0b4d-120">Description</span></span>                                                                                                        |
|----------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="b0b4d-121">**IWTSVirtualChannelManager**</span><span class="sxs-lookup"><span data-stu-id="b0b4d-121">**IWTSVirtualChannelManager**</span></span>](/windows/desktop/api/TsVirtualChannels/nn-tsvirtualchannels-iwtsvirtualchannelmanager) | <span data-ttu-id="b0b4d-122">管理所有遠端桌面連線 (RDC) 用戶端外掛程式、DVC 接聽程式或靜態虛擬通道。</span><span class="sxs-lookup"><span data-stu-id="b0b4d-122">Manages all Remote Desktop Connection (RDC) client plug-ins, DVC listeners, or static virtual channels.</span></span><br/> |
| [<span data-ttu-id="b0b4d-123">**IWTSListener**</span><span class="sxs-lookup"><span data-stu-id="b0b4d-123">**IWTSListener**</span></span>](/windows/desktop/api/TsVirtualChannels/nn-tsvirtualchannels-iwtslistener)                           | <span data-ttu-id="b0b4d-124">管理 DVC 連接之每個接聽程式的設定。</span><span class="sxs-lookup"><span data-stu-id="b0b4d-124">Manages configuration settings for each listener for the DVC connection.</span></span><br/>                                |
| [<span data-ttu-id="b0b4d-125">**IWTSVirtualChannel**</span><span class="sxs-lookup"><span data-stu-id="b0b4d-125">**IWTSVirtualChannel**</span></span>](/windows/desktop/api/TsVirtualChannels/nn-tsvirtualchannels-iwtsvirtualchannel)               | <span data-ttu-id="b0b4d-126">控制通道狀態，以及在通道上寫入。</span><span class="sxs-lookup"><span data-stu-id="b0b4d-126">Controls the channel state, as well as writes on the channel.</span></span><br/>                                           |



 

<span data-ttu-id="b0b4d-127">下圖顯示遠端桌面連線 (RDC) 用戶端與遠端桌面連線 (RDC) 用戶端外掛程式之間的關聯性。</span><span class="sxs-lookup"><span data-stu-id="b0b4d-127">The following illustration shows the relationship between the Remote Desktop Connection (RDC) client and the Remote Desktop Connection (RDC) client plug-in.</span></span>

![用戶端和外掛程式的關聯性](images/tsclient.png)

 

 





