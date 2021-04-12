---
description: 當執行緒主動與 Windows 映像取得通訊時 (WIA) 裝置 (例如，傳輸資料或寫入裝置屬性) WIA &\# 0034; 鎖定&\# 0034; 裝置。
ms.assetid: 59533937-284a-4732-a73b-d2e0b5a9a370
title: 在多個執行緒或應用程式中與 WIA 裝置通訊
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1a7a4b518093c3a0fc09534d67e22e5349d44d09
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104192799"
---
# <a name="communicating-with-a-wia-device-in-multiple-threads-or-applications"></a><span data-ttu-id="fee8c-103">在多個執行緒或應用程式中與 WIA 裝置通訊</span><span class="sxs-lookup"><span data-stu-id="fee8c-103">Communicating with a WIA Device in Multiple Threads or Applications</span></span>

<span data-ttu-id="fee8c-104">當執行緒主動與 Windows 映像取得通訊時 (WIA) 裝置 (例如，傳輸資料或寫入裝置屬性) WIA 「鎖定」裝置。</span><span class="sxs-lookup"><span data-stu-id="fee8c-104">When a thread is actively communicating with a Windows Image Acquisition (WIA) device (for example, transferring data or writing device properties) WIA "locks" the device.</span></span> <span data-ttu-id="fee8c-105">當裝置鎖定時，其他執行緒或進程都無法主動與該裝置通訊。</span><span class="sxs-lookup"><span data-stu-id="fee8c-105">When a device is locked, no other threads or processes can actively communicate with that device.</span></span>

<span data-ttu-id="fee8c-106">WIA 不會禁止多個執行緒或進程維護單一裝置的連接。</span><span class="sxs-lookup"><span data-stu-id="fee8c-106">WIA does not prohibit multiple threads or processes from maintaining connections to a single device.</span></span> <span data-ttu-id="fee8c-107">也就是說，裝置只會在實際通訊期間鎖定，而且兩個或多個應用程式可以同時選取單一裝置。</span><span class="sxs-lookup"><span data-stu-id="fee8c-107">That is, a device is locked only during the actual communication, and two or more applications can simultaneously have a single device selected.</span></span>

<span data-ttu-id="fee8c-108">當任何執行緒或應用程式呼叫 [**IWiaDevMgr：： CreateDevice**](/windows/desktop/api/wia_xp/nf-wia_xp-iwiadevmgr-createdevice) 或 [**IWiaDevMgr2：： CreateDevice**](-wia-iwiadevmgr2-createdevice.md) 建立該裝置的實例時，WIA 都會建立個別的專案樹狀結構。</span><span class="sxs-lookup"><span data-stu-id="fee8c-108">WIA creates a separate item tree each time any thread or application calls [**IWiaDevMgr::CreateDevice**](/windows/desktop/api/wia_xp/nf-wia_xp-iwiadevmgr-createdevice) or [**IWiaDevMgr2::CreateDevice**](-wia-iwiadevmgr2-createdevice.md) to create an instance of that device.</span></span> <span data-ttu-id="fee8c-109">WIA 會為每個專案樹狀結構維護不同的狀態資訊。</span><span class="sxs-lookup"><span data-stu-id="fee8c-109">WIA maintains separate state information for each item tree.</span></span> <span data-ttu-id="fee8c-110">例如，如果執行緒建立特定掃描器的兩個實例，則可以為這兩個實例設定不同的掃描解析度。</span><span class="sxs-lookup"><span data-stu-id="fee8c-110">For example, if a thread creates two instances of a particular scanner, it can set different scan resolutions for the two instances.</span></span> <span data-ttu-id="fee8c-111">在特定實例上呼叫 [**IWiaDataTransfer：： idtGetData**](/windows/desktop/api/wia_xp/nf-wia_xp-iwiadatatransfer-idtgetdata) 時，WIA 會先將與該實例相關聯的屬性載入至裝置，然後才進行實際的掃描。</span><span class="sxs-lookup"><span data-stu-id="fee8c-111">When [**IWiaDataTransfer::idtGetData**](/windows/desktop/api/wia_xp/nf-wia_xp-iwiadatatransfer-idtgetdata) is called on a particular instance, WIA loads the properties associated with that instance to the device before the actual scan takes place.</span></span> <span data-ttu-id="fee8c-112">這不會影響其他裝置實例的狀態。</span><span class="sxs-lookup"><span data-stu-id="fee8c-112">This does not affect the state of the other instance of the device.</span></span>

<span data-ttu-id="fee8c-113">如果執行緒目前已鎖定裝置 (它會主動與) 該裝置進行通訊，而另一個執行緒嘗試呼叫與裝置主動通訊的方法，此方法會傳回 WIA \_ 錯誤忙碌的 \_ 錯誤。</span><span class="sxs-lookup"><span data-stu-id="fee8c-113">If a thread currently has a device locked (it is actively communicating with that device) and another thread attempts to call a method that actively communicates with the device, the method returns a WIA\_ERROR\_BUSY error.</span></span>

<span data-ttu-id="fee8c-114">一般而言，讀取和寫入裝置屬性需要很少的時間，這些作業很少會造成衝突。</span><span class="sxs-lookup"><span data-stu-id="fee8c-114">Typically, reading and writing device properties takes so little time that these operations rarely cause a conflict.</span></span> <span data-ttu-id="fee8c-115">但是，傳輸資料通常需要較長的時間，因此更可能建立裝置存取衝突。</span><span class="sxs-lookup"><span data-stu-id="fee8c-115">Transferring data, however, usually takes longer, and therefore is more likely to create device access conflicts.</span></span> <span data-ttu-id="fee8c-116">您可以使用程式設計的方式，以避免長時間的裝置作業 (資料傳輸) 在應用程式內的個別執行緒中同時進行。</span><span class="sxs-lookup"><span data-stu-id="fee8c-116">It is sound programming to avoid lengthy device operations (data transfers) concurrently in separate threads within an application.</span></span>

<span data-ttu-id="fee8c-117">應用程式絕對不應該假設它是唯一的應用程式，它會在啟動時與 WIA 裝置進行通訊。</span><span class="sxs-lookup"><span data-stu-id="fee8c-117">An application should never assume that it is the only application that is communicating with a WIA device when it starts.</span></span>

 

 



