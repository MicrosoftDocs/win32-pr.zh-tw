---
description: 下列介面可用於在列印多工緩衝處理器所裝載的應用程式和元件之間的非同步通訊，例如印表機驅動程式和埠監視器。
ms.assetid: e96c957f-3972-4afc-9d76-a4725b8688f8
title: 非同步列印通知介面
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c7da8d320b33224e81852542e39f435b45b6dab5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103695012"
---
# <a name="asynchronous-printing-notification-interfaces"></a><span data-ttu-id="3d718-103">非同步列印通知介面</span><span class="sxs-lookup"><span data-stu-id="3d718-103">Asynchronous Printing Notification Interfaces</span></span>

<span data-ttu-id="3d718-104">下列介面可用於在列印多工緩衝處理器所裝載的應用程式和元件之間的非同步通訊，例如印表機驅動程式和埠監視器。</span><span class="sxs-lookup"><span data-stu-id="3d718-104">The following interfaces are used in asynchronous communication between applications and components that are hosted by the print spooler, such as printer drivers and port monitors.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="3d718-105">本節內容</span><span class="sxs-lookup"><span data-stu-id="3d718-105">In this section</span></span>



| <span data-ttu-id="3d718-106">介面</span><span class="sxs-lookup"><span data-stu-id="3d718-106">Interface</span></span>                                                                     | <span data-ttu-id="3d718-107">描述</span><span class="sxs-lookup"><span data-stu-id="3d718-107">Description</span></span>                                                                                                                                                                                                                                                   |
|-------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="3d718-108">**IPrintAsyncNotifyCallback**</span><span class="sxs-lookup"><span data-stu-id="3d718-108">**IPrintAsyncNotifyCallback**</span></span>](/windows/desktop/api/prnasnot/nn-prnasnot-iprintasyncnotifycallback)<br/>     | <span data-ttu-id="3d718-109">建立及管理由列印多工緩衝處理器所裝載的應用程式和元件所使用的通道。</span><span class="sxs-lookup"><span data-stu-id="3d718-109">Creates and manages a communication channel used by applications and components that are hosted by the print spooler.</span></span><br/>                                                                                                                              |
| [<span data-ttu-id="3d718-110">**IPrintAsyncNotifyChannel**</span><span class="sxs-lookup"><span data-stu-id="3d718-110">**IPrintAsyncNotifyChannel**</span></span>](/windows/desktop/api/prnasnot/nn-prnasnot-iprintasyncnotifychannel)<br/>       | <span data-ttu-id="3d718-111">代表由「列印多工緩衝處理器」所裝載之元件用來將通知傳送至應用程式的通道。</span><span class="sxs-lookup"><span data-stu-id="3d718-111">Represents a communication channel that components that are hosted by the print spooler use to send notifications to applications.</span></span> <span data-ttu-id="3d718-112">如果通道是雙向的，應用程式可以使用相同的通道，將回應傳回至元件。</span><span class="sxs-lookup"><span data-stu-id="3d718-112">If the channel is bidirectional, applications can use the same channel to send responses back to the component.</span></span><br/> |
| [<span data-ttu-id="3d718-113">**IPrintAsyncNotifyDataObject**</span><span class="sxs-lookup"><span data-stu-id="3d718-113">**IPrintAsyncNotifyDataObject**</span></span>](/windows/desktop/api/prnasnot/nn-prnasnot-iprintasyncnotifydataobject)<br/> | <span data-ttu-id="3d718-114">封裝通知通道中傳送的資料。</span><span class="sxs-lookup"><span data-stu-id="3d718-114">Encapsulates the data sent in a notification channel.</span></span> <br/>                                                                                                                                                                                             |



 

 

 




