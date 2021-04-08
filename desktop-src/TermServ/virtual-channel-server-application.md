---
title: 虛擬通道伺服器應用程式
description: 使用虛擬通道之應用程式的伺服器模組，必須是在遠端桌面工作階段主機 (RD 工作階段主機) server 的用戶端會話中執行的使用者模式應用程式。 請注意，您必須提供方法來啟動伺服器應用程式。
ms.assetid: b593df5d-5e22-46c6-8f59-9e3fdfe765ad
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 377732b91d6f93645e23b0f0b93cc203a65ef471
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103673808"
---
# <a name="virtual-channel-server-application"></a><span data-ttu-id="79554-104">虛擬通道伺服器應用程式</span><span class="sxs-lookup"><span data-stu-id="79554-104">Virtual Channel Server Application</span></span>

<span data-ttu-id="79554-105">使用虛擬通道之應用程式的伺服器模組，必須是在遠端桌面工作階段主機 (RD 工作階段主機) server 的用戶端會話中執行的使用者模式應用程式。</span><span class="sxs-lookup"><span data-stu-id="79554-105">The server module of an application that uses virtual channels must be a user-mode application running in a client session on the Remote Desktop Session Host (RD Session Host) server.</span></span> <span data-ttu-id="79554-106">請注意，您必須提供方法來啟動伺服器應用程式。</span><span class="sxs-lookup"><span data-stu-id="79554-106">Note that you must provide a method to start the server application.</span></span> <span data-ttu-id="79554-107">您可以透過多種方式達成此目的;例如，您可以使用登入腳本，或是開機檔案夾中的程式或腳本。</span><span class="sxs-lookup"><span data-stu-id="79554-107">You can accomplish this in multiple ways; for example, you can use a logon script, or a program or script in the Startup folder.</span></span> <span data-ttu-id="79554-108">使用者也可以啟動應用程式。</span><span class="sxs-lookup"><span data-stu-id="79554-108">Users could also launch the application.</span></span>

<span data-ttu-id="79554-109">您必須在下列位置下新增子機碼，以將虛擬通道伺服器應用程式的名稱儲存在登錄中：</span><span class="sxs-lookup"><span data-stu-id="79554-109">You must store the name of the virtual channel server application in the registry by adding a subkey under the following location:</span></span>

<span data-ttu-id="79554-110">**HKEY \_本機 \_ 電腦** \\ **系統** \\ **CurrentControlSet** \\ **控制** \\ **終端機伺服器** 的 \\ **載入** 宏</span><span class="sxs-lookup"><span data-stu-id="79554-110">**HKEY\_LOCAL\_MACHINE**\\**System**\\**CurrentControlSet**\\**Control**\\**Terminal Server**\\**Addins**</span></span>

<span data-ttu-id="79554-111">如需子機碼的詳細資訊，請參閱 [監視會話連線和中斷連接](monitoring-session-connections-and-disconnections.md)。</span><span class="sxs-lookup"><span data-stu-id="79554-111">For more information about the subkey, see [Monitoring Session Connections and Disconnections](monitoring-session-connections-and-disconnections.md).</span></span>

<span data-ttu-id="79554-112">伺服器應用程式可以呼叫 [**WTSVirtualChannelOpen**](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsvirtualchannelopen) 函數來開啟虛擬通道的控制碼。</span><span class="sxs-lookup"><span data-stu-id="79554-112">The server application can call the [**WTSVirtualChannelOpen**](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsvirtualchannelopen) function to open a handle to a virtual channel.</span></span> <span data-ttu-id="79554-113">然後，應用程式可以使用下列任何一個函式中的控制碼。</span><span class="sxs-lookup"><span data-stu-id="79554-113">The application can then use the handle in any of the following functions.</span></span>

<dl> <dt>

[<span data-ttu-id="79554-114">**WTSVirtualChannelClose**</span><span class="sxs-lookup"><span data-stu-id="79554-114">**WTSVirtualChannelClose**</span></span>](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsvirtualchannelclose)
</dt> <dd>

<span data-ttu-id="79554-115">關閉開啟的虛擬通道控制碼。</span><span class="sxs-lookup"><span data-stu-id="79554-115">Closes an open virtual channel handle.</span></span>

</dd> <dt>

[<span data-ttu-id="79554-116">**WTSVirtualChannelPurgeInput**</span><span class="sxs-lookup"><span data-stu-id="79554-116">**WTSVirtualChannelPurgeInput**</span></span>](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsvirtualchannelpurgeinput)
</dt> <dd>

<span data-ttu-id="79554-117">刪除從用戶端傳送到特定虛擬通道上伺服器的所有已排入佇列的輸入資料。</span><span class="sxs-lookup"><span data-stu-id="79554-117">Deletes all queued input data sent from the client to the server on a specific virtual channel.</span></span>

> [!Note]  
> <span data-ttu-id="79554-118">遠端桌面服務目前未使用此函數。</span><span class="sxs-lookup"><span data-stu-id="79554-118">This function currently is not used by Remote Desktop Services.</span></span>

 

</dd> <dt>

[<span data-ttu-id="79554-119">**WTSVirtualChannelPurgeOutput**</span><span class="sxs-lookup"><span data-stu-id="79554-119">**WTSVirtualChannelPurgeOutput**</span></span>](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsvirtualchannelpurgeoutput)
</dt> <dd>

<span data-ttu-id="79554-120">刪除從伺服器傳送至特定虛擬通道上之用戶端的所有已排入佇列的輸出資料。</span><span class="sxs-lookup"><span data-stu-id="79554-120">Deletes all queued output data sent from the server to the client on a specific virtual channel.</span></span>

> [!Note]  
> <span data-ttu-id="79554-121">遠端桌面服務目前未使用此函數。</span><span class="sxs-lookup"><span data-stu-id="79554-121">This function currently is not used by Remote Desktop Services.</span></span>

 

</dd> <dt>

[<span data-ttu-id="79554-122">**WTSVirtualChannelQuery**</span><span class="sxs-lookup"><span data-stu-id="79554-122">**WTSVirtualChannelQuery**</span></span>](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsvirtualchannelquery)
</dt> <dd>

<span data-ttu-id="79554-123">傳回指定虛擬通道的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="79554-123">Returns information about a specified virtual channel.</span></span>

</dd> <dt>

[<span data-ttu-id="79554-124">**WTSVirtualChannelRead**</span><span class="sxs-lookup"><span data-stu-id="79554-124">**WTSVirtualChannelRead**</span></span>](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsvirtualchannelread)
</dt> <dd>

<span data-ttu-id="79554-125">從虛擬通道的伺服器端讀取資料。</span><span class="sxs-lookup"><span data-stu-id="79554-125">Reads data from the server end of a virtual channel.</span></span>

</dd> <dt>

[<span data-ttu-id="79554-126">**WTSVirtualChannelWrite**</span><span class="sxs-lookup"><span data-stu-id="79554-126">**WTSVirtualChannelWrite**</span></span>](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsvirtualchannelwrite)
</dt> <dd>

<span data-ttu-id="79554-127">將資料寫入虛擬通道的伺服器端。</span><span class="sxs-lookup"><span data-stu-id="79554-127">Writes data to the server end of a virtual channel.</span></span>

</dd> </dl>

 

 




