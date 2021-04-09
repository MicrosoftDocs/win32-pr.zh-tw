---
title: 遠端桌面通訊協定提供者 API
description: 您可以使用遠端桌面通訊協定提供者 API 來建立通訊協定，以提供遠端桌面服務服務與多個用戶端之間的通訊。
ms.assetid: dd14c569-195e-460e-a1c3-2a74d0f49ff5
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 95aed1c6866f3078c3761ad8ec631ef23b43a9ae
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103931803"
---
# <a name="remote-desktop-protocol-provider-api"></a><span data-ttu-id="627ee-103">遠端桌面通訊協定提供者 API</span><span class="sxs-lookup"><span data-stu-id="627ee-103">Remote Desktop Protocol Provider API</span></span>

<span data-ttu-id="627ee-104">您可以使用遠端桌面通訊協定提供者 API 來建立通訊協定，以提供遠端桌面服務服務與多個用戶端之間的通訊。</span><span class="sxs-lookup"><span data-stu-id="627ee-104">You use the Remote Desktop Protocol Provider API to create a protocol to provide communication between the Remote Desktop Services service and multiple clients.</span></span>

<span data-ttu-id="627ee-105">當 Windows Server 載入時，遠端桌面服務服務 (也稱為遠端連線管理員 (RCM) ) 啟動。</span><span class="sxs-lookup"><span data-stu-id="627ee-105">When Windows Server loads, the Remote Desktop Services service (also known as Remote Connection Manager (RCM)) starts.</span></span> <span data-ttu-id="627ee-106">服務也會啟動遠端桌面通訊協定提供者的接聽程式物件，這些提供者接著會接聽用戶端連接。</span><span class="sxs-lookup"><span data-stu-id="627ee-106">The service also starts listener objects for the Remote Desktop Protocol Providers that in turn listen for client connections.</span></span> <span data-ttu-id="627ee-107">服務和通訊協定提供者是使用者模式物件，會使用本檔中討論的 Api 進行通訊。</span><span class="sxs-lookup"><span data-stu-id="627ee-107">The service and the protocol providers are user-mode objects that communicate by using the APIs discussed in this documentation.</span></span> <span data-ttu-id="627ee-108">通訊協定提供者可以使用 (IOCTLs) 的輸入/輸出控制項，與核心模式驅動程式進行通訊。</span><span class="sxs-lookup"><span data-stu-id="627ee-108">The protocol providers can communicate with kernel-mode drivers by using input/output controls (IOCTLs).</span></span> <span data-ttu-id="627ee-109">這會顯示在下圖中。</span><span class="sxs-lookup"><span data-stu-id="627ee-109">This is shown in the following illustration.</span></span>

![自訂通訊協定 api 架構](images/protocol-architecture.png)

<span data-ttu-id="627ee-111">Microsoft 已實行遠端桌面通訊協定 (RDP) ，以提供遠端桌面服務服務與用戶端連線之間的通訊。</span><span class="sxs-lookup"><span data-stu-id="627ee-111">Microsoft has implemented the Remote Desktop Protocol (RDP) to provide communication between the Remote Desktop Services service and client connections.</span></span> <span data-ttu-id="627ee-112">您可以使用組成遠端桌面通訊協定提供者 API 的介面、結構、等位和列舉類型，來建立自己的通訊協定。</span><span class="sxs-lookup"><span data-stu-id="627ee-112">You can create your own protocol by using the interfaces, structures, unions, and enumeration types that make up the Remote Desktop Protocol Provider API.</span></span> <span data-ttu-id="627ee-113">如需詳細資訊，請參閱下列主題。</span><span class="sxs-lookup"><span data-stu-id="627ee-113">For more information, see the following topics.</span></span>

<dl> <dt>

[<span data-ttu-id="627ee-114">建立遠端桌面通訊協定提供者</span><span class="sxs-lookup"><span data-stu-id="627ee-114">Creating a Remote Desktop Protocol Provider</span></span>](creating-a-custom-remote-protocol.md)
</dt> <dd>

<span data-ttu-id="627ee-115">建立遠端桌面通訊協定提供者的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="627ee-115">Information about creating a Remote Desktop Protocol Provider.</span></span> <span data-ttu-id="627ee-116">通訊協定管理員會實作為 COM 伺服器，並在遠端桌面服務服務啟動時搜尋的位置註冊。</span><span class="sxs-lookup"><span data-stu-id="627ee-116">The protocol manager is implemented as a COM server and registered in a location searched when the Remote Desktop Services service starts.</span></span>

</dd> <dt>

[<span data-ttu-id="627ee-117">遠端桌面通訊協定提供者參考</span><span class="sxs-lookup"><span data-stu-id="627ee-117">Remote Desktop Protocol Provider reference</span></span>](custom-remote-protocol-reference.md)
</dt> <dd>

<span data-ttu-id="627ee-118">包含介面、結構、等位和列舉類型，可讓您建立自訂的遠端桌面通訊協定 (RDP) 。</span><span class="sxs-lookup"><span data-stu-id="627ee-118">Contains interfaces, structures, unions, and enumeration types that enable you to create a custom Remote Desktop Protocol (RDP).</span></span>

</dd> </dl>

## <a name="related-topics"></a><span data-ttu-id="627ee-119">相關主題</span><span class="sxs-lookup"><span data-stu-id="627ee-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="627ee-120">關於遠端桌面服務</span><span class="sxs-lookup"><span data-stu-id="627ee-120">About Remote Desktop Services</span></span>](about-terminal-services.md)
</dt> </dl>

 

 




