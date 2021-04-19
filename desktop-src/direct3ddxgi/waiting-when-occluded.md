---
description: 應用程式可以在轉譯為螢幕時，等候事件不必要 (也就是 pixels occluded) 。
ms.assetid: B9EC23C9-A311-4BD9-BBE8-908A1334A541
title: 不需要轉譯時等候事件
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3b553ef52e812c5117e5d9669ba13b47b9f4280c
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "106972293"
---
# <a name="waiting-on-an-event-when-rendering-is-unnecessary"></a><span data-ttu-id="73ebd-103">不需要轉譯時等候事件</span><span class="sxs-lookup"><span data-stu-id="73ebd-103">Waiting on an event when rendering is unnecessary</span></span>

<span data-ttu-id="73ebd-104">應用程式可以在轉譯為螢幕時，等候事件不必要 (也就是 pixels occluded) 。</span><span class="sxs-lookup"><span data-stu-id="73ebd-104">Apps can wait on an event when rendering to the screen is unnecessary (that is, while they are occluded).</span></span> <span data-ttu-id="73ebd-105">當桌面視窗管理員 (DWM) 或應用程式 pixels occluded 時，不需要轉譯，而且作業系統可長期保持較低的電源狀態。</span><span class="sxs-lookup"><span data-stu-id="73ebd-105">When the Desktop Window Manager (DWM) or an app is occluded, no rendering is necessary and the operating system can stay in lower power states for longer periods of time.</span></span> <span data-ttu-id="73ebd-106">這可節省電力並延長電池壽命。</span><span class="sxs-lookup"><span data-stu-id="73ebd-106">This saves power and extends battery life.</span></span>

<span data-ttu-id="73ebd-107">應用程式可以在下列情況等候事件：</span><span class="sxs-lookup"><span data-stu-id="73ebd-107">An app can wait on an event when:</span></span>

-   <span data-ttu-id="73ebd-108">所有監視都已關閉。</span><span class="sxs-lookup"><span data-stu-id="73ebd-108">All the monitors are off.</span></span>
-   <span data-ttu-id="73ebd-109">應用程式執行所在的會話已中斷連線。</span><span class="sxs-lookup"><span data-stu-id="73ebd-109">The session that the app runs in is disconnected.</span></span>
-   <span data-ttu-id="73ebd-110">應用程式會在單一監視設定上，以全螢幕的形式執行。</span><span class="sxs-lookup"><span data-stu-id="73ebd-110">The app runs in full screen exclusively on a single monitor configuration.</span></span>
-   <span data-ttu-id="73ebd-111">應用程式會在與作用中桌面不同的桌上型電腦上執行，而且沒有在使用中桌面上呈現的許可權。</span><span class="sxs-lookup"><span data-stu-id="73ebd-111">The app runs on a different desktop than the active desktop and does not have permission to render on the active desktop.</span></span>

<span data-ttu-id="73ebd-112">當應用程式可以再次轉譯時，作業系統會觸發事件。</span><span class="sxs-lookup"><span data-stu-id="73ebd-112">The operating system triggers the event when the app is able to render again.</span></span> <span data-ttu-id="73ebd-113">在驅動程式升級期間，或 timeout 偵測和復原 (TDR) procession 時，不會清除此事件，不過當新的介面卡和監視變成作用中時，就會將其清除。</span><span class="sxs-lookup"><span data-stu-id="73ebd-113">The event is not cleared during a driver upgrade, or timeout detection and recovery (TDR) procession, however it is cleared when the new adapter and monitors become active.</span></span>

<span data-ttu-id="73ebd-114">如果您想要讓應用程式收到有關遮蔽狀態變更的通知，應用程式必須註冊這些變更。</span><span class="sxs-lookup"><span data-stu-id="73ebd-114">If you want your app to be notified about changes of occlusion status, the app must register for these changes.</span></span> <span data-ttu-id="73ebd-115">應用程式可以註冊，以透過訊息至視窗或透過事件信號來通知遮蔽狀態變更。</span><span class="sxs-lookup"><span data-stu-id="73ebd-115">An app can register to be notified about changes of occlusion status through a message to a window or through event signaling.</span></span> <span data-ttu-id="73ebd-116">若要註冊以接收有關遮蔽狀態變更之視窗的通知訊息，應用程式會呼叫 [**IDXGIFactory2：： RegisterOcclusionStatusWindow**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgifactory2-registerocclusionstatuswindow) 方法。</span><span class="sxs-lookup"><span data-stu-id="73ebd-116">To register to receive notification messages to a window about occlusion status changes, an app calls the [**IDXGIFactory2::RegisterOcclusionStatusWindow**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgifactory2-registerocclusionstatuswindow) method.</span></span> <span data-ttu-id="73ebd-117">若要註冊以透過事件信號接收遮蔽狀態變更的通知，應用程式會呼叫 [**IDXGIFactory2：： RegisterOcclusionStatusEvent**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgifactory2-registerocclusionstatusevent) 方法。</span><span class="sxs-lookup"><span data-stu-id="73ebd-117">To register to receive notification of occlusion status changes via event signaling, an app calls the [**IDXGIFactory2::RegisterOcclusionStatusEvent**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgifactory2-registerocclusionstatusevent) method.</span></span> <span data-ttu-id="73ebd-118">這兩種方法都會將指標傳回給應用程式用來取消註冊通知的索引鍵值。</span><span class="sxs-lookup"><span data-stu-id="73ebd-118">Both methods return a pointer to a key value that the app can use to unregister the notification.</span></span> <span data-ttu-id="73ebd-119">若要取消註冊通知，應用程式會將此索引鍵值傳遞給 [**IDXGIFactory2：： UnregisterOcclusionStatus**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgifactory2-unregisterocclusionstatus) 方法。</span><span class="sxs-lookup"><span data-stu-id="73ebd-119">To unregister the notification, the app passes this key value to the [**IDXGIFactory2::UnregisterOcclusionStatus**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgifactory2-unregisterocclusionstatus) method.</span></span>

## <a name="related-topics"></a><span data-ttu-id="73ebd-120">相關主題</span><span class="sxs-lookup"><span data-stu-id="73ebd-120">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="73ebd-121">DXGI 1.2 改進</span><span class="sxs-lookup"><span data-stu-id="73ebd-121">DXGI 1.2 Improvements</span></span>](dxgi-1-2-improvements.md)
</dt> </dl>

 

 



