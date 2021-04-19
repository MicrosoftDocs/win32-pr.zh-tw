---
description: 下列介面可用於在列印多工緩衝處理器所裝載的應用程式和元件之間的非同步通訊，例如印表機驅動程式和埠監視器。
ms.assetid: 7e98e63f-616c-4cd1-a8aa-482d27529b8c
title: 非同步列印通知函式
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 72fa7b0b61de15af9f7117e7c36104eb51abbb7c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106998542"
---
# <a name="asynchronous-printing-notification-functions"></a><span data-ttu-id="d5b88-103">非同步列印通知函式</span><span class="sxs-lookup"><span data-stu-id="d5b88-103">Asynchronous Printing Notification Functions</span></span>

<span data-ttu-id="d5b88-104">下列介面可用於在列印多工緩衝處理器所裝載的應用程式和元件之間的非同步通訊，例如印表機驅動程式和埠監視器。</span><span class="sxs-lookup"><span data-stu-id="d5b88-104">The following interfaces are used in asynchronous communication between applications and components that are hosted by the print spooler, such as printer drivers and port monitors.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="d5b88-105">本節內容</span><span class="sxs-lookup"><span data-stu-id="d5b88-105">In this section</span></span>



| <span data-ttu-id="d5b88-106">函式</span><span class="sxs-lookup"><span data-stu-id="d5b88-106">Function</span></span>                                                                                        | <span data-ttu-id="d5b88-107">描述</span><span class="sxs-lookup"><span data-stu-id="d5b88-107">Description</span></span>                                                                                                                                                                                              |
|-------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="d5b88-108">**CreatePrintAsyncNotifyChannel**</span><span class="sxs-lookup"><span data-stu-id="d5b88-108">**CreatePrintAsyncNotifyChannel**</span></span>](/windows/desktop/api/prnasnot/nf-prnasnot-createprintasyncnotifychannel)<br/>               | <span data-ttu-id="d5b88-109">在列印多工緩衝處理器裝載的列印元件（如列印驅動程式或埠監視器）與從元件接收通知的應用程式之間建立通道。</span><span class="sxs-lookup"><span data-stu-id="d5b88-109">Creates a communication channel between a Print Spooler-hosted printing component, such as a print driver or port monitor, and an application that receives notifications from the component.</span></span><br/> |
| [<span data-ttu-id="d5b88-110">**RegisterForPrintAsyncNotifications**</span><span class="sxs-lookup"><span data-stu-id="d5b88-110">**RegisterForPrintAsyncNotifications**</span></span>](/windows/desktop/api/prnasnot/nf-prnasnot-registerforprintasyncnotifications)<br/>     | <span data-ttu-id="d5b88-111">可讓應用程式從列印多工緩衝處理器裝載的列印元件（如印表機驅動程式、列印處理器和埠監視器）註冊通知。</span><span class="sxs-lookup"><span data-stu-id="d5b88-111">Enables an application to register for notifications from Print Spooler-hosted printing components such as printer drivers, print processors, and port monitors.</span></span><br/>                              |
| [<span data-ttu-id="d5b88-112">**UnRegisterForPrintAsyncNotifications**</span><span class="sxs-lookup"><span data-stu-id="d5b88-112">**UnRegisterForPrintAsyncNotifications**</span></span>](/windows/desktop/api/prnasnot/nf-prnasnot-unregisterforprintasyncnotifications)<br/> | <span data-ttu-id="d5b88-113">啟用已註冊的應用程式，以接收來自列印多工緩衝處理器之列印元件的通知，以取消註冊。</span><span class="sxs-lookup"><span data-stu-id="d5b88-113">Enables an application that has registered to receive notifications from Print Spooler-hosted printing components to unregister.</span></span><br/>                                                              |



 

 

 




