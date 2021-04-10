---
title: 開始順序
description: 啟動自訂通訊協定的步驟。
ms.assetid: 34c6eb08-668b-43b7-b49b-9ab7536ab658
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5af0716e39d1df96bbdf29f4a3abbb14e32bc752
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104183095"
---
# <a name="start-sequence"></a><span data-ttu-id="fb511-103">開始順序</span><span class="sxs-lookup"><span data-stu-id="fb511-103">Start Sequence</span></span>

<span data-ttu-id="fb511-104">若要啟動您的通訊協定提供者，遠端桌面服務服務：</span><span class="sxs-lookup"><span data-stu-id="fb511-104">To start your protocol provider, the Remote Desktop Services service:</span></span>

-   <span data-ttu-id="fb511-105">從登錄中取出接聽程式的名稱和通訊協定管理員物件的 CLSID ([**IWRdsProtocolManager**](/windows/desktop/api/wtsprotocol/nn-wtsprotocol-iwrdsprotocolmanager)) 。</span><span class="sxs-lookup"><span data-stu-id="fb511-105">Retrieves the name of the listener and the CLSID of your protocol manager object ([**IWRdsProtocolManager**](/windows/desktop/api/wtsprotocol/nn-wtsprotocol-iwrdsprotocolmanager)) from the registry.</span></span> <span data-ttu-id="fb511-106">如需詳細資訊，請參閱 [註冊通訊協定管理員](registering-the-custom-protocol.md)。</span><span class="sxs-lookup"><span data-stu-id="fb511-106">For more information, see [Registering the Protocol Manager](registering-the-custom-protocol.md).</span></span>
-   <span data-ttu-id="fb511-107">呼叫 [**initialize**](/windows/desktop/api/wtsprotocol/nf-wtsprotocol-iwrdsprotocolmanager-initialize) 以初始化通訊協定管理員。</span><span class="sxs-lookup"><span data-stu-id="fb511-107">Calls [**Initialize**](/windows/desktop/api/wtsprotocol/nf-wtsprotocol-iwrdsprotocolmanager-initialize) to initialize the protocol manager.</span></span>
-   <span data-ttu-id="fb511-108">使用 CLSID 建立通訊協定管理員物件。</span><span class="sxs-lookup"><span data-stu-id="fb511-108">Creates a protocol manager object using the CLSID.</span></span> <span data-ttu-id="fb511-109">即使有多個接聽程式已為相同的通訊協定提供者註冊，服務還是只會建立一個通訊協定管理員物件。</span><span class="sxs-lookup"><span data-stu-id="fb511-109">Even if there are multiple listeners registered for the same protocol provider, the service only creates one protocol manager object.</span></span>
-   <span data-ttu-id="fb511-110">呼叫 [**CreateListener**](/windows/desktop/api/wtsprotocol/nf-wtsprotocol-iwrdsprotocolmanager-createlistener) 來指示通訊協定管理員物件建立 [**IWRdsProtocolListener**](/windows/desktop/api/wtsprotocol/nn-wtsprotocol-iwrdsprotocollistener) 接聽程式物件，並將它傳回至服務。</span><span class="sxs-lookup"><span data-stu-id="fb511-110">Calls [**CreateListener**](/windows/desktop/api/wtsprotocol/nf-wtsprotocol-iwrdsprotocolmanager-createlistener) to instruct the protocol manager object to create an [**IWRdsProtocolListener**](/windows/desktop/api/wtsprotocol/nn-wtsprotocol-iwrdsprotocollistener) listener object and return it to the service.</span></span> <span data-ttu-id="fb511-111">通訊協定管理員物件必須先加入接聽程式物件的參考，才能將它傳回至服務。</span><span class="sxs-lookup"><span data-stu-id="fb511-111">The protocol manager object must add a reference to the listener object before returning it to the service.</span></span> <span data-ttu-id="fb511-112">當服務停止或刪除接聽程式時，服務會釋放物件。</span><span class="sxs-lookup"><span data-stu-id="fb511-112">The service will release the object when the service stops or the listener is deleted.</span></span>
-   <span data-ttu-id="fb511-113">在接聽程式物件上呼叫 [**StartListen**](/windows/desktop/api/wtsprotocol/nf-wtsprotocol-iwrdsprotocollistener-startlisten) ，讓接聽程式可以開始接聽傳入連接。</span><span class="sxs-lookup"><span data-stu-id="fb511-113">Calls [**StartListen**](/windows/desktop/api/wtsprotocol/nf-wtsprotocol-iwrdsprotocollistener-startlisten) on the listener object so that the listener can start listening for incoming connections.</span></span>
-   <span data-ttu-id="fb511-114">呼叫 [**StopListen**](/windows/desktop/api/wtsprotocol/nf-wtsprotocol-iwrdsprotocollistener-stoplisten) 以停止接聽程式物件。</span><span class="sxs-lookup"><span data-stu-id="fb511-114">Calls [**StopListen**](/windows/desktop/api/wtsprotocol/nf-wtsprotocol-iwrdsprotocollistener-stoplisten) to stop the listener object from listening.</span></span>
-   <span data-ttu-id="fb511-115">呼叫解除 [**初始化**](/windows/desktop/api/wtsprotocol/nf-wtsprotocol-iwrdsprotocolmanager-uninitialize) 以將通訊協定管理員解除初始化。</span><span class="sxs-lookup"><span data-stu-id="fb511-115">Calls [**Uninitialize**](/windows/desktop/api/wtsprotocol/nf-wtsprotocol-iwrdsprotocolmanager-uninitialize) to uninitialize the protocol manager.</span></span>

<span data-ttu-id="fb511-116">當用戶端嘗試連接時，接聽程式會建立 [**IWRdsProtocolConnection**](/windows/desktop/api/wtsprotocol/nn-wtsprotocol-iwrdsprotocolconnection) 物件。</span><span class="sxs-lookup"><span data-stu-id="fb511-116">The listener creates an [**IWRdsProtocolConnection**](/windows/desktop/api/wtsprotocol/nn-wtsprotocol-iwrdsprotocolconnection) object when a client tries to connect.</span></span> <span data-ttu-id="fb511-117">接聽程式物件會呼叫 [**OnConnected**](/windows/desktop/api/wtsprotocol/nf-wtsprotocol-iwrdsprotocollistenercallback-onconnected) 來通知遠端桌面服務服務，新的用戶端嘗試連線或重新連線，並在該呼叫中傳遞 **IWRdsProtocolConnection** 物件。</span><span class="sxs-lookup"><span data-stu-id="fb511-117">The listener object calls [**OnConnected**](/windows/desktop/api/wtsprotocol/nf-wtsprotocol-iwrdsprotocollistenercallback-onconnected) to notify the Remote Desktop Services service that a new client is trying to connect or reconnect, and passes the **IWRdsProtocolConnection** object in that call.</span></span> <span data-ttu-id="fb511-118">遠端桌面服務服務會接著傳回該呼叫中的 [**IWRdsProtocolConnectionCallback**](/windows/desktop/api/wtsprotocol/nn-wtsprotocol-iwrdsprotocolconnectioncallback) 物件，讓通訊協定可以視需要與遠端桌面服務服務進行通訊。</span><span class="sxs-lookup"><span data-stu-id="fb511-118">The Remote Desktop Services service will in turn return an [**IWRdsProtocolConnectionCallback**](/windows/desktop/api/wtsprotocol/nn-wtsprotocol-iwrdsprotocolconnectioncallback) object in that call so that the protocol can communicate with the Remote Desktop Services service as needed.</span></span> <span data-ttu-id="fb511-119">服務會在傳回之前加入回呼物件的參考，而且當連接關閉時，通訊協定必須釋放該參考。</span><span class="sxs-lookup"><span data-stu-id="fb511-119">The service adds a reference to the callback object before returning, and the protocol must release that reference when the connection closes.</span></span>

<span data-ttu-id="fb511-120">下圖顯示啟動期間各種物件之間的互動。</span><span class="sxs-lookup"><span data-stu-id="fb511-120">The following illustration shows the interaction between the various objects during startup.</span></span>

![rcm 開始順序](images/protocol-startsequence.png)

## <a name="related-topics"></a><span data-ttu-id="fb511-122">相關主題</span><span class="sxs-lookup"><span data-stu-id="fb511-122">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="fb511-123">方法呼叫順序</span><span class="sxs-lookup"><span data-stu-id="fb511-123">Method Call Sequence</span></span>](method-call-sequence.md)
</dt> <dt>

[<span data-ttu-id="fb511-124">連接順序</span><span class="sxs-lookup"><span data-stu-id="fb511-124">Connection Sequence</span></span>](connection-sequence.md)
</dt> </dl>

 

 




