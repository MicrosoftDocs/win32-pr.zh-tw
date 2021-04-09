---
description: 在 Windows 7 中，使用核心音訊 Api （例如媒體基礎、DirectSound 和 Wave Api）的高階平臺 Api，可處理從現有裝置切換至新的預設音訊端點的串流，來執行串流路由功能。
ms.assetid: 4f36710c-c5a8-4f31-9b77-5253475c0715
title: 取得串流路由的裝置端點
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7ed8c7546c2bd7437ed9705dc93c2a736bbb64e2
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103847335"
---
# <a name="getting-the-device-endpoint-for-stream-routing"></a><span data-ttu-id="216cb-103">取得串流路由的裝置端點</span><span class="sxs-lookup"><span data-stu-id="216cb-103">Getting the Device Endpoint for Stream Routing</span></span>

<span data-ttu-id="216cb-104">在 Windows 7 中，使用核心音訊 Api （例如媒體基礎、DirectSound 和 Wave Api）的高階平臺 Api，可處理從現有裝置切換至新的預設音訊端點的串流，來執行串流路由功能。</span><span class="sxs-lookup"><span data-stu-id="216cb-104">In Windows 7, high-level platform APIs that use Core Audio APIs such as Media Foundation, DirectSound, and Wave APIs, implement the stream routing feature by handling stream switching from an existing device to a new default audio endpoint.</span></span> <span data-ttu-id="216cb-105">使用這些 Api 的媒體應用程式 (例如，在 [**IMMDevice**](/windows/desktop/api/Mmdeviceapi/nn-mmdeviceapi-immdevice)物件上啟用 **IDirectSound** 或 **IBaseFilter** 物件的應用程式) 使用串流路由行為，而不需要修改來源。</span><span class="sxs-lookup"><span data-stu-id="216cb-105">Media applications that use these APIs (for example, an application activating an **IDirectSound** or **IBaseFilter** object on an [**IMMDevice**](/windows/desktop/api/Mmdeviceapi/nn-mmdeviceapi-immdevice) object) use the stream routing behavior without any modifications to the source.</span></span>

<span data-ttu-id="216cb-106">高層級 Api 會針對透過 [**IMMDeviceEnumerator：： GetDefaultAudioEndpoint**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdeviceenumerator-getdefaultaudioendpoint)取得的裝置端點，執行串流路由。</span><span class="sxs-lookup"><span data-stu-id="216cb-106">The high-level APIs implement stream routing for the device endpoint that is obtained through [**IMMDeviceEnumerator::GetDefaultAudioEndpoint**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdeviceenumerator-getdefaultaudioendpoint).</span></span> <span data-ttu-id="216cb-107">如果應用程式串流至預設裝置，資料流程路由功能會如所定義運作。</span><span class="sxs-lookup"><span data-stu-id="216cb-107">If an application streams to the default device, the stream routing feature operates as defined.</span></span> <span data-ttu-id="216cb-108">如果任何其他機制抓取資料流程，即使它與預設裝置相同，資料流程也不會切換至新的裝置。</span><span class="sxs-lookup"><span data-stu-id="216cb-108">Streams are not switched to the new device if it is retrieved by any other mechanism even if it is the same as the default device.</span></span>

<span data-ttu-id="216cb-109">直接使用核心音訊 Api (WASAPI 用戶端) 的媒體應用程式，可以為任何轉譯或捕獲裝置提供自訂的串流路由執行。</span><span class="sxs-lookup"><span data-stu-id="216cb-109">A media application that uses Core Audio APIs directly (WASAPI client) can provide a custom stream routing implementation for any rendering or capture device.</span></span> <span data-ttu-id="216cb-110">WASAPI 用戶端可以複寫高階 Api 所提供的實作，方法是將其限制為在設定為預設裝置的裝置上開啟的串流。</span><span class="sxs-lookup"><span data-stu-id="216cb-110">A WASAPI client can replicate the implemetation provided by the high-level APIs by restricting it to streams that are opened on devices that are set as the default device.</span></span> <span data-ttu-id="216cb-111">若要取得預設裝置端點的參考，用戶端必須呼叫 [**IMMDeviceEnumerator：： GetDefaultAudioEndpoint**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdeviceenumerator-getdefaultaudioendpoint)。</span><span class="sxs-lookup"><span data-stu-id="216cb-111">To get a reference to the default device's endpoint, the client must call [**IMMDeviceEnumerator::GetDefaultAudioEndpoint**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdeviceenumerator-getdefaultaudioendpoint).</span></span> <span data-ttu-id="216cb-112">在此呼叫中，用戶端必須指定 *資料流程* 參數，以指出它是否需要轉譯預設裝置的指標或 capture 預設裝置。</span><span class="sxs-lookup"><span data-stu-id="216cb-112">In this call, the client must indicate whether it requires a pointer to the rendering default device or the capture default device by specifying the *dataFlow* parameter.</span></span> <span data-ttu-id="216cb-113">用戶端也必須在 **ERole** 屬性中為端點指定適當的角色 (**eConsole** 或 **eCommunications**) 。</span><span class="sxs-lookup"><span data-stu-id="216cb-113">The client must also specify the appropriate role for the endpoint in the **ERole** attribute (**eConsole** or **eCommunications**).</span></span> <span data-ttu-id="216cb-114">請勿使用 **eMultimedia**。</span><span class="sxs-lookup"><span data-stu-id="216cb-114">Do not use **eMultimedia**.</span></span>

<span data-ttu-id="216cb-115">如果應用程式串流至任何其他裝置，應用程式可以藉由呼叫 [**IMMDeviceEnumerator：： GetDevice**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdeviceenumerator-getdevice)) ，藉由指定端點識別碼 (字串來取得裝置。</span><span class="sxs-lookup"><span data-stu-id="216cb-115">If the application streams to any other device, the application can get the device by specifying an endpoint ID string (by calling [**IMMDeviceEnumerator::GetDevice**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdeviceenumerator-getdevice)).</span></span>

<span data-ttu-id="216cb-116">識別裝置之後，WASAPI 用戶端可以藉由處理針對裝置傳送的裝置和音訊會話通知，提供串流路由的執行。</span><span class="sxs-lookup"><span data-stu-id="216cb-116">After the device is identified, the WASAPI client can provide the implementation for stream routing by handling the device and audio session notifications sent for the device.</span></span> <span data-ttu-id="216cb-117">如需這些通知的詳細資訊，請參閱 [串流路由的相關通知](relevant-device-notifications-for-stream-routing.md)。</span><span class="sxs-lookup"><span data-stu-id="216cb-117">For more information about these notifications, see [Relevant Notifications for Stream Routing](relevant-device-notifications-for-stream-routing.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="216cb-118">相關主題</span><span class="sxs-lookup"><span data-stu-id="216cb-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="216cb-119">關於 MMDevice API</span><span class="sxs-lookup"><span data-stu-id="216cb-119">About MMDevice API</span></span>](mmdevice-api.md)
</dt> <dt>

[<span data-ttu-id="216cb-120">關於 WASAPI</span><span class="sxs-lookup"><span data-stu-id="216cb-120">About WASAPI</span></span>](wasapi.md)
</dt> <dt>

[<span data-ttu-id="216cb-121">串流路由</span><span class="sxs-lookup"><span data-stu-id="216cb-121">Stream Routing</span></span>](stream-routing.md)
</dt> </dl>

 

 



