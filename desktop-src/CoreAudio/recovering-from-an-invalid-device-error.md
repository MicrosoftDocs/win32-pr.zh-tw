---
description: 從 Invalid-Device 錯誤中復原
ms.assetid: 1f5c3458-70ca-45ba-ac33-5c7b9f092320
title: 從 Invalid-Device 錯誤中復原
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ca20c32be46367f53a14ce26c39f980e3649b652
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104111305"
---
# <a name="recovering-from-an-invalid-device-error"></a><span data-ttu-id="f8aa4-103">從 Invalid-Device 錯誤中復原</span><span class="sxs-lookup"><span data-stu-id="f8aa4-103">Recovering from an Invalid-Device Error</span></span>

<span data-ttu-id="f8aa4-104">WASAPI 中的許多方法會傳回錯誤碼 AUDCLNT \_ E \_ 裝置 \_ 如果用戶端應用程式所使用的音訊端點裝置變得無效，則會使其失效。</span><span class="sxs-lookup"><span data-stu-id="f8aa4-104">Many of the methods in WASAPI return error code AUDCLNT\_E\_DEVICE\_INVALIDATED if the audio endpoint device that the client application is using becomes invalid.</span></span> <span data-ttu-id="f8aa4-105">此錯誤碼表示端點裝置已卸載，或音訊硬體或相關聯的硬體資源已重新設定、停用、移除或無法使用。</span><span class="sxs-lookup"><span data-stu-id="f8aa4-105">This error code indicates that the endpoint device has been unplugged, or that the audio hardware or associated hardware resources have been reconfigured, disabled, removed, or otherwise made unavailable for use.</span></span> <span data-ttu-id="f8aa4-106">通常，應用程式可以從這個錯誤中復原。</span><span class="sxs-lookup"><span data-stu-id="f8aa4-106">Frequently, the application can recover from this error.</span></span>

>[!NOTE]
> <span data-ttu-id="f8aa4-107">如需使用空間音訊 Api 時，從無效裝置錯誤中復原 (ISAC) 的相關資訊，請參閱 [從 Invalid-Device 錯誤中復原 (空間音效) ](recovering-from-an-invalid-device-error-spatial-sound.md)</span><span class="sxs-lookup"><span data-stu-id="f8aa4-107">For information on recovering from invalid device errors when using spatial audio APIs (ISAC), see [Recovering from an Invalid-Device Error (Spatial Sound)](recovering-from-an-invalid-device-error-spatial-sound.md)</span></span>

<span data-ttu-id="f8aa4-108">應用程式應該用來從 AUDCLNT E 裝置中復原的 \_ 策略 \_ \_ 失效錯誤，取決於應用程式用來選取音訊端點裝置的下列技術：</span><span class="sxs-lookup"><span data-stu-id="f8aa4-108">The strategy that an application should use to recover from an AUDCLNT\_E\_DEVICE\_INVALIDATED error depends on which of the following techniques the application uses to select an audio endpoint device:</span></span>

-   <span data-ttu-id="f8aa4-109">一律選取預設音訊轉譯或捕獲裝置。</span><span class="sxs-lookup"><span data-stu-id="f8aa4-109">Always select the default audio rendering or capture device.</span></span>
-   <span data-ttu-id="f8aa4-110">選取特定的音訊端點裝置。</span><span class="sxs-lookup"><span data-stu-id="f8aa4-110">Select a specific audio endpoint device.</span></span>

<span data-ttu-id="f8aa4-111">在第二個案例中，應用程式會根據內部需求自動選取特定的裝置，或允許使用者從可用裝置清單中明確選取裝置。</span><span class="sxs-lookup"><span data-stu-id="f8aa4-111">In the latter case, either the application automatically selects a specific device based on internal requirements or it allows the user to explicitly select a device from a list of available devices.</span></span>

<span data-ttu-id="f8aa4-112">使用預設裝置的應用程式可以嘗試從 AUDCLNT \_ E \_ 裝置的失效錯誤中復原，如下所示 \_ ：</span><span class="sxs-lookup"><span data-stu-id="f8aa4-112">An application that uses the default device can attempt to recover from an AUDCLNT\_E\_DEVICE\_INVALIDATED error as follows:</span></span>

1.  <span data-ttu-id="f8aa4-113">釋放 [**IAudioClient**](/windows/desktop/api/Audioclient/nn-audioclient-iaudioclient) 介面，以及它在裝置上取得的任何其他 WASAPI 介面。</span><span class="sxs-lookup"><span data-stu-id="f8aa4-113">Release the [**IAudioClient**](/windows/desktop/api/Audioclient/nn-audioclient-iaudioclient) interface and any other WASAPI interfaces that it has acquired on the device.</span></span>
2.  <span data-ttu-id="f8aa4-114">呼叫 [**IMMDeviceEnumerator：： GetDefaultAudioEndpoint**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdeviceenumerator-getdefaultaudioendpoint) 方法，以取得目前的預設音訊裝置。</span><span class="sxs-lookup"><span data-stu-id="f8aa4-114">Call the [**IMMDeviceEnumerator::GetDefaultAudioEndpoint**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdeviceenumerator-getdefaultaudioendpoint) method to get the current default audio device.</span></span>
3.  <span data-ttu-id="f8aa4-115">嘗試在預設音訊裝置上啟用 [**IAudioClient**](/windows/desktop/api/Audioclient/nn-audioclient-iaudioclient) 。</span><span class="sxs-lookup"><span data-stu-id="f8aa4-115">Attempt to activate [**IAudioClient**](/windows/desktop/api/Audioclient/nn-audioclient-iaudioclient) on the default audio device.</span></span>

<span data-ttu-id="f8aa4-116">遵循上述步驟，不論 AUDCLNT E 裝置發生不正確錯誤，應用程式往往會適當地 \_ 回應 \_ \_ 。</span><span class="sxs-lookup"><span data-stu-id="f8aa4-116">By following the preceding steps, the application tends to respond appropriately regardless of the cause of the AUDCLNT\_E\_DEVICE\_INVALIDATED error.</span></span> <span data-ttu-id="f8aa4-117">如果預設裝置的重新設定造成錯誤 (例如，如果使用者變更了裝置) 所使用的串流格式，則這些步驟會在成功時，讓應用程式繼續使用相同的裝置。</span><span class="sxs-lookup"><span data-stu-id="f8aa4-117">If reconfiguration of the default device caused the error (for example, if the user changed the stream format used by the device), then these steps, if they succeed, enable the application to continue to use the same device.</span></span> <span data-ttu-id="f8aa4-118">如果使用者停用或移除應用程式所使用的裝置，而另一部裝置可用來擔任預設裝置的角色，則應用程式可以使用新的預設裝置繼續進行。</span><span class="sxs-lookup"><span data-stu-id="f8aa4-118">If the user disabled or removed the device that the application was using and another device is available to assume the role of default device, then the application can continue by using the new default device.</span></span> <span data-ttu-id="f8aa4-119">無論是哪一種情況，應用程式都會自動調整，而不需要使用者介入。</span><span class="sxs-lookup"><span data-stu-id="f8aa4-119">In either case, the application adapts automatically without requiring intervention by the user.</span></span>

<span data-ttu-id="f8aa4-120">選取特定裝置的應用程式可以嘗試從 AUDCLNT \_ E \_ 裝置的失效錯誤中復原，如下所示 \_ ：</span><span class="sxs-lookup"><span data-stu-id="f8aa4-120">An application that selects a specific device can attempt to recover from the AUDCLNT\_E\_DEVICE\_INVALIDATED error as follows:</span></span>

1.  <span data-ttu-id="f8aa4-121">釋放 [**IAudioClient**](/windows/desktop/api/Audioclient/nn-audioclient-iaudioclient) 介面，以及它在裝置上取得的任何其他 WASAPI 介面。</span><span class="sxs-lookup"><span data-stu-id="f8aa4-121">Release the [**IAudioClient**](/windows/desktop/api/Audioclient/nn-audioclient-iaudioclient) interface and any other WASAPI interfaces that it has acquired on the device.</span></span>
2.  <span data-ttu-id="f8aa4-122">嘗試啟用相同裝置上的 [**IAudioClient**](/windows/desktop/api/Audioclient/nn-audioclient-iaudioclient) 介面。</span><span class="sxs-lookup"><span data-stu-id="f8aa4-122">Attempt to activate an [**IAudioClient**](/windows/desktop/api/Audioclient/nn-audioclient-iaudioclient) interface on the same device.</span></span>
3.  <span data-ttu-id="f8aa4-123">如果步驟2失敗，則應用程式可以選擇提示使用者選取其他裝置。</span><span class="sxs-lookup"><span data-stu-id="f8aa4-123">If step 2 fails, then the application can, as an option, prompt the user to select another device.</span></span>

<span data-ttu-id="f8aa4-124">如果應用程式所使用的裝置已重新設定但未停用或移除，步驟2就會成功。</span><span class="sxs-lookup"><span data-stu-id="f8aa4-124">Step 2 can succeed if the device being used by the application was reconfigured but not disabled or removed.</span></span> <span data-ttu-id="f8aa4-125">如果成功，步驟2可讓應用程式自動繼續使用相同的裝置，而不需要使用者介入。</span><span class="sxs-lookup"><span data-stu-id="f8aa4-125">If successful, step 2 enables the application to automatically continue to use the same device without requiring intervention by the user.</span></span> <span data-ttu-id="f8aa4-126">如果應用程式允許使用者在使用者停用或移除先前使用的裝置之後明確地選取另一部裝置，則適用步驟3。</span><span class="sxs-lookup"><span data-stu-id="f8aa4-126">Step 3 is appropriate if the application allows the user to explicitly select another device after the user has disabled or removed the previously used device.</span></span>

<span data-ttu-id="f8aa4-127">應用程式可以藉由註冊在會話中斷裝置與裝置的連線時收到通知，來更精確地判斷出無效裝置錯誤的原因。</span><span class="sxs-lookup"><span data-stu-id="f8aa4-127">An application can determine more precisely the cause of an invalid-device error by registering to receive a notification when a session loses its connection to a device.</span></span> <span data-ttu-id="f8aa4-128">若要啟用此通知，應用程式會執行 [**IAudioSessionEvents**](/windows/desktop/api/Audiopolicy/nn-audiopolicy-iaudiosessionevents) 介面，並呼叫 [**IAudioSessionControl：： RegisterAudioSessionNotification**](/windows/desktop/api/Audiopolicy/nf-audiopolicy-iaudiosessioncontrol-registeraudiosessionnotification) 方法來註冊介面。</span><span class="sxs-lookup"><span data-stu-id="f8aa4-128">To enable this notification, the application implements an [**IAudioSessionEvents**](/windows/desktop/api/Audiopolicy/nn-audiopolicy-iaudiosessionevents) interface and calls the [**IAudioSessionControl::RegisterAudioSessionNotification**](/windows/desktop/api/Audiopolicy/nf-audiopolicy-iaudiosessioncontrol-registeraudiosessionnotification) method to register the interface.</span></span> <span data-ttu-id="f8aa4-129">當無效裝置錯誤導致會話中斷連接時，WASAPI 會在已註冊的介面中呼叫 [**IAudioSessionEvents：： OnSessionDisconnected**](/windows/desktop/api/Audiopolicy/nf-audiopolicy-iaudiosessionevents-onsessiondisconnected) 方法。</span><span class="sxs-lookup"><span data-stu-id="f8aa4-129">When an invalid-device error causes the session to be disconnected, WASAPI calls the [**IAudioSessionEvents::OnSessionDisconnected**](/windows/desktop/api/Audiopolicy/nf-audiopolicy-iaudiosessionevents-onsessiondisconnected) method in the registered interface.</span></span> <span data-ttu-id="f8aa4-130">透過這個方法，WASAPI 會通知應用程式中斷連接的原因。</span><span class="sxs-lookup"><span data-stu-id="f8aa4-130">Through this method, WASAPI informs the application of the reason for the disconnection.</span></span> <span data-ttu-id="f8aa4-131">在 Windows Vista 中， **OnSessionDisconnected** 呼叫會識別下列原因：</span><span class="sxs-lookup"><span data-stu-id="f8aa4-131">In Windows Vista, the **OnSessionDisconnected** call identifies the following reasons:</span></span>

-   <span data-ttu-id="f8aa4-132">使用者已移除音訊端點裝置。</span><span class="sxs-lookup"><span data-stu-id="f8aa4-132">The user removed the audio endpoint device.</span></span>
-   <span data-ttu-id="f8aa4-133">Windows 音訊服務已關閉。</span><span class="sxs-lookup"><span data-stu-id="f8aa4-133">The Windows audio service has shut down.</span></span>
-   <span data-ttu-id="f8aa4-134">針對音訊會話所連接的裝置，慣用的資料流程格式已變更。</span><span class="sxs-lookup"><span data-stu-id="f8aa4-134">The preferred stream format changed for the device that the audio session is connected to.</span></span>
-   <span data-ttu-id="f8aa4-135">使用者登出 Windows 終端機的服務 (WTS 正在執行音訊會話的) 會話。</span><span class="sxs-lookup"><span data-stu-id="f8aa4-135">The user logged off the Windows Terminal Services (WTS) session that the audio session was running in.</span></span> <span data-ttu-id="f8aa4-136">如需有關 WTS 會話的詳細資訊，請參閱 Windows SDK 檔。</span><span class="sxs-lookup"><span data-stu-id="f8aa4-136">For more information about WTS sessions, see the Windows SDK documentation.</span></span>
-   <span data-ttu-id="f8aa4-137">執行音訊會話的 WTS 會話已中斷連線。</span><span class="sxs-lookup"><span data-stu-id="f8aa4-137">The WTS session that the audio session was running in was disconnected.</span></span>
-   <span data-ttu-id="f8aa4-138"> (的共用模式) 音訊會話已中斷連線，讓音訊端點裝置可供獨佔模式連線使用。</span><span class="sxs-lookup"><span data-stu-id="f8aa4-138">The (shared-mode) audio session was disconnected to make the audio endpoint device available for an exclusive-mode connection.</span></span>

<span data-ttu-id="f8aa4-139">為了回應中斷連接事件，WASAPI 會關閉屬於會話的所有資料流程。</span><span class="sxs-lookup"><span data-stu-id="f8aa4-139">In response to the disconnection event, WASAPI closes all of the streams that belong to the session.</span></span> <span data-ttu-id="f8aa4-140">如果應用程式後續嘗試透過 WASAPI 方法（例如 [**IAudioClient：： GetCurrentPadding**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-getcurrentpadding)）存取已關閉的資料流程，則該方法會失敗，並傳回錯誤碼 AUDCLNT \_ E \_ 裝置 \_ 無效。</span><span class="sxs-lookup"><span data-stu-id="f8aa4-140">If an application subsequently attempts to access a closed stream through a WASAPI method such as [**IAudioClient::GetCurrentPadding**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-getcurrentpadding), then the method fails and returns error code AUDCLNT\_E\_DEVICE\_INVALIDATED.</span></span>

<span data-ttu-id="f8aa4-141">透過 [**IAudioSessionEvents**](/windows/desktop/api/Audiopolicy/nn-audiopolicy-iaudiosessionevents) 介面接收通知的另一個好處是，通知會以非同步方式抵達。</span><span class="sxs-lookup"><span data-stu-id="f8aa4-141">An additional benefit to receiving notifications through the [**IAudioSessionEvents**](/windows/desktop/api/Audiopolicy/nn-audiopolicy-iaudiosessionevents) interface is that the notifications arrive asynchronously.</span></span> <span data-ttu-id="f8aa4-142">因此，即使串流未執行，應用程式仍會及時收到無效裝置錯誤的及時通知，以防止串流執行。</span><span class="sxs-lookup"><span data-stu-id="f8aa4-142">Thus, even when the stream is not running, the application will still receive timely notification of invalid-device errors that can prevent the stream from running.</span></span>

## <a name="related-topics"></a><span data-ttu-id="f8aa4-143">相關主題</span><span class="sxs-lookup"><span data-stu-id="f8aa4-143">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f8aa4-144">串流管理</span><span class="sxs-lookup"><span data-stu-id="f8aa4-144">Stream Management</span></span>](stream-management.md)
</dt> </dl>

 

 



