---
description: 應用程式可以使用 InkCollector 物件來接聽系統事件，並在其上接聽 SystemGesture 事件。
ms.assetid: 141afdbe-b5a7-47dc-b505-46089a5eda75
title: 接聽系統事件
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f1429e652140cc9624d324401edef7817dad40ef
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104027500"
---
# <a name="listening-to-system-events"></a><span data-ttu-id="7063b-103">接聽系統事件</span><span class="sxs-lookup"><span data-stu-id="7063b-103">Listening to System Events</span></span>

<span data-ttu-id="7063b-104">應用程式可以使用 [**InkCollector**](inkcollector-class.md) 物件來接聽系統事件，並在其上接聽 [**SystemGesture**](inkcollector-systemgesture.md) 事件。</span><span class="sxs-lookup"><span data-stu-id="7063b-104">Applications can listen to system events by using the [**InkCollector**](inkcollector-class.md) object and listening for the [**SystemGesture**](inkcollector-systemgesture.md) event on it.</span></span> <span data-ttu-id="7063b-105">您可以設定應用程式要接聽的事件。</span><span class="sxs-lookup"><span data-stu-id="7063b-105">You can set which events an application listens to.</span></span> <span data-ttu-id="7063b-106">當 tablet 畫筆動作發生時，對應的 **SystemGesture** 事件會傳送至應用程式的 **InkCollector** 物件。</span><span class="sxs-lookup"><span data-stu-id="7063b-106">When a tablet pen action occurs, the corresponding **SystemGesture** event is sent to the application on its **InkCollector** object.</span></span> <span data-ttu-id="7063b-107">當應用程式收到事件時，可以取消對應至指定 **SystemGesture** 事件的滑鼠訊息。</span><span class="sxs-lookup"><span data-stu-id="7063b-107">An application can cancel the mouse message that corresponds to a given **SystemGesture** event when it receives the event.</span></span> <span data-ttu-id="7063b-108">如需取消滑鼠郵件的詳細資訊，請參閱 **SystemGesture** 事件。</span><span class="sxs-lookup"><span data-stu-id="7063b-108">For details about canceling mouse messages, see **SystemGesture** event.</span></span>

 

 



