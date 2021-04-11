---
description: 裝置移除通知
ms.assetid: 0b96231a-f990-4c1c-8d00-cafeb3985ab3
title: 裝置移除通知
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 93c84fa280e0adbc1d0eec9043fbb2f1446487f0
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "103936023"
---
# <a name="device-removal-notification"></a><span data-ttu-id="aa17d-103">裝置移除通知</span><span class="sxs-lookup"><span data-stu-id="aa17d-103">Device Removal Notification</span></span>

<span data-ttu-id="aa17d-104">如果使用者移除圖形所使用的隨插即用裝置，則篩選圖形管理員會張貼 [**EC \_ 裝置 \_ 遺失**](ec-device-lost.md) 事件。</span><span class="sxs-lookup"><span data-stu-id="aa17d-104">If the user removes a Plug and Play device that the graph was using, the filter graph manager posts an [**EC\_DEVICE\_LOST**](ec-device-lost.md) event.</span></span> <span data-ttu-id="aa17d-105">如果裝置再次變成可用，則篩選圖形管理員會將另一個 **EC \_ 裝置 \_ 遺失** 事件張貼。</span><span class="sxs-lookup"><span data-stu-id="aa17d-105">If the device becomes available again, the filter graph manager posts another **EC\_DEVICE\_LOST** event.</span></span> <span data-ttu-id="aa17d-106">不過，先前的「capture」篩選狀態不再有效。</span><span class="sxs-lookup"><span data-stu-id="aa17d-106">However, the previous state of the capture filter is no longer valid.</span></span> <span data-ttu-id="aa17d-107">應用程式必須重建圖形才能使用裝置。</span><span class="sxs-lookup"><span data-stu-id="aa17d-107">The application must rebuild the graph to use the device.</span></span>

<span data-ttu-id="aa17d-108">當新裝置插入電源時，DirectShow 不會傳送任何事件。</span><span class="sxs-lookup"><span data-stu-id="aa17d-108">DirectShow does not send any event when a new device is plugged in.</span></span> <span data-ttu-id="aa17d-109">若要瞭解新裝置的可用時間，應用程式可以監視 WM \_ DEVICECHANGE 視窗訊息。</span><span class="sxs-lookup"><span data-stu-id="aa17d-109">To learn when a new device is available, the application can monitor WM\_DEVICECHANGE window messages.</span></span> <span data-ttu-id="aa17d-110">如需詳細資訊，請參閱 Platform SDK 檔中的「裝置管理」。</span><span class="sxs-lookup"><span data-stu-id="aa17d-110">For more information, see "Device Management" in the Platform SDK documentation.</span></span>

## <a name="related-topics"></a><span data-ttu-id="aa17d-111">相關主題</span><span class="sxs-lookup"><span data-stu-id="aa17d-111">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="aa17d-112">DirectShow 中的事件通知</span><span class="sxs-lookup"><span data-stu-id="aa17d-112">Event Notification in DirectShow</span></span>](event-notification-in-directshow.md)
</dt> </dl>

 

 



