---
description: 應用程式無法以身歷聲轉譯，除非作業系統指出它會啟用 stereoscopic 3D 顯示行為。 應用程式會根據視窗是否為視窗化或全螢幕，決定是否要以不同的方式呈現 stereoscopic 3D。
ms.assetid: FB8AC57E-38DD-47B5-8666-1F4B73488F8B
title: 以身歷聲轉譯並通知身歷聲狀態
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 379c6335e0bd060cf0065fe92bf2ec6c086289c3
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "104108385"
---
# <a name="rendering-in-stereo-and-notifying-about-stereo-status"></a><span data-ttu-id="0c1e3-104">以身歷聲轉譯並通知身歷聲狀態</span><span class="sxs-lookup"><span data-stu-id="0c1e3-104">Rendering in stereo and notifying about stereo status</span></span>

<span data-ttu-id="0c1e3-105">應用程式無法以身歷聲轉譯，除非作業系統指出它會啟用 stereoscopic 3D 顯示行為。</span><span class="sxs-lookup"><span data-stu-id="0c1e3-105">Apps can't render in stereo unless the operating system indicates that it enables stereoscopic 3D display behavior.</span></span> <span data-ttu-id="0c1e3-106">應用程式會根據視窗是否為視窗化或全螢幕，決定是否要以不同的方式呈現 stereoscopic 3D。</span><span class="sxs-lookup"><span data-stu-id="0c1e3-106">Apps determine whether to render in stereoscopic 3D differently depending on whether they are windowed or full screen.</span></span>

<span data-ttu-id="0c1e3-107">視窗型應用程式會呼叫 [**IDXGIFactory2：： IsWindowedStereoEnabled**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgifactory2-iswindowedstereoenabled) 方法，以判斷是否要以身歷聲呈現。</span><span class="sxs-lookup"><span data-stu-id="0c1e3-107">A windowed app calls the [**IDXGIFactory2::IsWindowedStereoEnabled**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgifactory2-iswindowedstereoenabled) method to determine whether to render in stereo.</span></span> <span data-ttu-id="0c1e3-108">全螢幕應用程式會呼叫 [**IDXGIOutput1：： GetDisplayModeList1**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgioutput1-getdisplaymodelist1) 方法，然後判斷是否有任何傳回的顯示模式支援以身歷聲呈現。</span><span class="sxs-lookup"><span data-stu-id="0c1e3-108">A full-screen app calls the [**IDXGIOutput1::GetDisplayModeList1**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgioutput1-getdisplaymodelist1) method and then determines whether any of the returned display modes support rendering in stereo.</span></span> <span data-ttu-id="0c1e3-109">除非您在 *旗標* 參數中指定了 [**DXGI \_ 列舉 \_ 模式 \_ 身歷聲**](dxgi-enum-modes.md)旗標，否則 **GetDisplayModeList1** 方法不會列舉身歷聲模式。</span><span class="sxs-lookup"><span data-stu-id="0c1e3-109">The **GetDisplayModeList1** method does not enumerate stereo modes unless you specify the [**DXGI\_ENUM\_MODES\_STEREO**](dxgi-enum-modes.md) flag in the *Flags* parameter.</span></span> <span data-ttu-id="0c1e3-110">支援身歷聲的視窗式或全螢幕應用程式會先根據 **IDXGIFactory2：： IsWindowedStereoEnabled** 或 **IDXGIOutput1：： GetDisplayModeList1** 方法的呼叫，判斷要以身歷聲轉譯，然後註冊以取得身歷聲狀態變更的通知。</span><span class="sxs-lookup"><span data-stu-id="0c1e3-110">A windowed or full-screen app that supports stereo first makes the determination to render in stereo based on a call to the **IDXGIFactory2::IsWindowedStereoEnabled** or **IDXGIOutput1::GetDisplayModeList1** method respectively, and then registers for notification of stereo status changes.</span></span> <span data-ttu-id="0c1e3-111">由於應用程式無法依賴通知來指出 stereoscopic 3D 顯示行為的目前狀態，當它收到通知事件或視窗訊息時，必須再次呼叫 **IDXGIFactory2：： IsWindowedStereoEnabled** 或 **IDXGIOutput1：： GetDisplayModeList1** ，以判斷作業系統 stereoscopic 3d 顯示行為的目前狀態。</span><span class="sxs-lookup"><span data-stu-id="0c1e3-111">Because the app can't rely on the notification to indicate the current status of the stereoscopic 3D display behavior, when it receives a notification event or window message, it must call either **IDXGIFactory2::IsWindowedStereoEnabled** or **IDXGIOutput1::GetDisplayModeList1** again to determine the current status of the operating system's stereoscopic 3D display behavior.</span></span>

<span data-ttu-id="0c1e3-112">如果您想要以身歷聲轉譯，則必須註冊身歷聲通知，以知道使用者何時關閉或有身歷聲行為。</span><span class="sxs-lookup"><span data-stu-id="0c1e3-112">If you want to render in stereo, you must register for stereo notifications to know when the user turns off or on stereo behavior.</span></span> <span data-ttu-id="0c1e3-113">您可以註冊應用程式，以透過訊息至視窗或透過事件信號來通知 stereoscopic 3D 狀態變更。</span><span class="sxs-lookup"><span data-stu-id="0c1e3-113">An app can register to be notified about stereoscopic 3D status changes through a message to a window or through event signaling.</span></span> <span data-ttu-id="0c1e3-114">若要註冊以接收關於身歷聲狀態變更之視窗的通知訊息，應用程式會呼叫 [**IDXGIFactory2：： RegisterStereoStatusWindow**](/windows/win32/api/dxgi1_2/nf-dxgi1_2-idxgifactory2-registerstereostatuswindow) 方法。</span><span class="sxs-lookup"><span data-stu-id="0c1e3-114">To register to receive notification messages to a window about stereo status changes, an app calls the [**IDXGIFactory2::RegisterStereoStatusWindow**](/windows/win32/api/dxgi1_2/nf-dxgi1_2-idxgifactory2-registerstereostatuswindow) method.</span></span> <span data-ttu-id="0c1e3-115">若要註冊以透過事件信號接收身歷聲狀態變更的通知，應用程式會呼叫 [**IDXGIFactory2：： RegisterStereoStatusEvent**](/windows/win32/api/dxgi1_2/nf-dxgi1_2-idxgifactory2-registerstereostatusevent) 方法。</span><span class="sxs-lookup"><span data-stu-id="0c1e3-115">To register to receive notification of stereo status changes via event signaling, an app calls the [**IDXGIFactory2::RegisterStereoStatusEvent**](/windows/win32/api/dxgi1_2/nf-dxgi1_2-idxgifactory2-registerstereostatusevent) method.</span></span> <span data-ttu-id="0c1e3-116">這兩種方法都會將指標傳回給應用程式用來取消註冊通知的索引鍵值。</span><span class="sxs-lookup"><span data-stu-id="0c1e3-116">Both methods return a pointer to a key value that the app can use to unregister the notification.</span></span> <span data-ttu-id="0c1e3-117">若要取消註冊通知，應用程式會將此索引鍵值傳遞給 [**IDXGIFactory2：： UnregisterStereoStatus**](/windows/win32/api/dxgi1_2/nf-dxgi1_2-idxgifactory2-unregisterstereostatus) 方法。</span><span class="sxs-lookup"><span data-stu-id="0c1e3-117">To unregister the notification, the app passes this key value to the [**IDXGIFactory2::UnregisterStereoStatus**](/windows/win32/api/dxgi1_2/nf-dxgi1_2-idxgifactory2-unregisterstereostatus) method.</span></span>

<span data-ttu-id="0c1e3-118">身歷聲狀態可包含下列元素：</span><span class="sxs-lookup"><span data-stu-id="0c1e3-118">Stereo status can contain the following elements:</span></span>

-   <span data-ttu-id="0c1e3-119">使用者設定。</span><span class="sxs-lookup"><span data-stu-id="0c1e3-119">The user configuration.</span></span>

    <span data-ttu-id="0c1e3-120">Windows 使用者可以在主控台的 [變更顯示設定] 中，啟用或停用 [啟用 stereoscopic 3D] 選項的身歷聲顯示。</span><span class="sxs-lookup"><span data-stu-id="0c1e3-120">Windows users can enable or disable stereo display with the enable stereoscopic 3D option in Control Panel's Change Display Settings.</span></span>

-   <span data-ttu-id="0c1e3-121">電腦功能和設定，包括圖形介面卡、圖形驅動程式和監視器安裝程式。</span><span class="sxs-lookup"><span data-stu-id="0c1e3-121">The computer capability and configuration, which includes graphics adapter, graphics driver, and monitor setup.</span></span>

<span data-ttu-id="0c1e3-122">[Direct3D 11.1 Simple 身歷聲3D 範例示範](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/Official%20Windows%20Platform%20Sample/Direct3D%20stereoscopic%203D%20sample)如何新增 stereoscopic 3d 效果，以及如何回應系統身歷聲變更。</span><span class="sxs-lookup"><span data-stu-id="0c1e3-122">The [Direct3D 11.1 Simple Stereo 3D Sample](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/Official%20Windows%20Platform%20Sample/Direct3D%20stereoscopic%203D%20sample) shows how to add a stereoscopic 3D effect and how to respond to system stereo changes.</span></span>

## <a name="related-topics"></a><span data-ttu-id="0c1e3-123">相關主題</span><span class="sxs-lookup"><span data-stu-id="0c1e3-123">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0c1e3-124">DXGI 1.2 改進</span><span class="sxs-lookup"><span data-stu-id="0c1e3-124">DXGI 1.2 Improvements</span></span>](dxgi-1-2-improvements.md)
</dt> </dl>

 

 
