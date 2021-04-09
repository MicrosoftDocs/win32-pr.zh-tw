---
description: 本文說明如何更新 WASAPI 的執行，以利用自動串流路由。
ms.assetid: 718CBEB9-A7A0-4898-81B7-CBD76AFA3A06
title: 自動串流路由
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 87a9848c5fd764ee49e485fc112c35c347a0f84d
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103936495"
---
# <a name="automatic-stream-routing"></a><span data-ttu-id="e0ec3-103">自動串流路由</span><span class="sxs-lookup"><span data-stu-id="e0ec3-103">Automatic Stream Routing</span></span>

<span data-ttu-id="e0ec3-104">本文說明如何更新 WASAPI 的執行，以利用自動串流路由。</span><span class="sxs-lookup"><span data-stu-id="e0ec3-104">This article describes how to update a WASAPI implementation to take advantage of automatic stream routing.</span></span>

<span data-ttu-id="e0ec3-105">從 Windows 7 開始，每當預設音訊裝置變更時，就會將應用程式的音訊播放串流順暢地從先前的預設音訊裝置傳輸到新的預設音訊裝置。</span><span class="sxs-lookup"><span data-stu-id="e0ec3-105">Starting with Windows 7, whenever the default audio device changes, an app's audio playback stream is seamlessly transferred from the previous default audio device to the new default audio device .</span></span> <span data-ttu-id="e0ec3-106">此傳輸會自動發生，不需要任何額外的應用程式程式碼。</span><span class="sxs-lookup"><span data-stu-id="e0ec3-106">This transfer occurs automatically without any additional application code.</span></span> <span data-ttu-id="e0ec3-107">不過，在 Windows 10 之前的1607版中，使用低層級 Windows 音訊會話 API (WASAPI) 的應用程式無法參與此自動化串流路由功能。</span><span class="sxs-lookup"><span data-stu-id="e0ec3-107">However, prior to Windows 10, version 1607, apps that used the low-level Windows Audio Session API (WASAPI) could not participate in this automated stream routing functionality.</span></span> <span data-ttu-id="e0ec3-108">使用 WASAPI 的應用程式必須藉由新增額外的程式碼來偵測音訊裝置的抵達和移除，並適當地將串流切換至這些裝置，以執行自己的串流路由形式。</span><span class="sxs-lookup"><span data-stu-id="e0ec3-108">Apps using WASAPI were required to implement their own form of stream routing by adding additional code to detect the arrival and removal of audio devices and switch the stream to those devices as appropriate.</span></span> <span data-ttu-id="e0ec3-109">使用 WASAPI 的應用程式不會在裝置抵達或移除 risked 上執行自己的串流路由機制，以提供不理想的使用者體驗。</span><span class="sxs-lookup"><span data-stu-id="e0ec3-109">Applications using WASAPI that did not implement their own stream routing mechanism on device arrival or removal risked providing a less than ideal user experience.</span></span>

<span data-ttu-id="e0ec3-110">從 Windows 10 版本1607開始，使用 WASAPI 的應用程式可以利用自動串流路由。</span><span class="sxs-lookup"><span data-stu-id="e0ec3-110">Starting with the Windows 10, version 1607, apps that use WASAPI can take advantage of automatic stream routing.</span></span> <span data-ttu-id="e0ec3-111">如果您的應用程式使用 WASAPI，強烈建議您使用下列步驟來更新應用程式，以利用這項新功能：</span><span class="sxs-lookup"><span data-stu-id="e0ec3-111">If your application uses WASAPI it is highly recommended that you update your application to take advantage of this new capability using the following steps:</span></span>

1.  <span data-ttu-id="e0ec3-112">Windows 10 1607 版中，定義了兩個新的 Guid，可用來啟用具有自動串流路由的音訊轉譯或捕捉介面 [， \_ DEVINTERFACE \_ 音訊](/windows/desktop/CoreAudio/devinterface-xxx-guids) 轉譯和 [DEVINTERFACE \_ 音訊 \_ 捕獲](/windows/desktop/CoreAudio/devinterface-xxx-guids)。</span><span class="sxs-lookup"><span data-stu-id="e0ec3-112">Windows 10, version 1607, defines two new GUIDs that can be used to activate an audio render or capture interface with automatic stream routing, [DEVINTERFACE\_AUDIO\_RENDER](/windows/desktop/CoreAudio/devinterface-xxx-guids) and [DEVINTERFACE\_AUDIO\_CAPTURE](/windows/desktop/CoreAudio/devinterface-xxx-guids).</span></span> <span data-ttu-id="e0ec3-113">藉由呼叫 [**StringFromIID**](/windows/desktop/api/combaseapi/nf-combaseapi-stringfromiid)來取得這些 guid 的字串表示。</span><span class="sxs-lookup"><span data-stu-id="e0ec3-113">Get a string representation of these GUIDs by calling [**StringFromIID**](/windows/desktop/api/combaseapi/nf-combaseapi-stringfromiid).</span></span> <span data-ttu-id="e0ec3-114">下列範例顯示音訊轉譯 GUID 的這個呼叫。</span><span class="sxs-lookup"><span data-stu-id="e0ec3-114">The following example shows this call for the audio render GUID.</span></span>

    ```C++
    PWSTR audioRenderGuidString;
    StringFromIID(DEVINTERFACE_AUDIO_RENDER, &audioRenderGuidString);
    ```

    

2.  <span data-ttu-id="e0ec3-115">將識別碼字串傳遞至 WASAPI [**ActivateAudioInterfaceAsync**](/windows/desktop/api/mmdeviceapi/nf-mmdeviceapi-activateaudiointerfaceasync) 函式，以啟用音訊端點。</span><span class="sxs-lookup"><span data-stu-id="e0ec3-115">Activate the audio endpoint by passing the identifier string to the WASAPI [**ActivateAudioInterfaceAsync**](/windows/desktop/api/mmdeviceapi/nf-mmdeviceapi-activateaudiointerfaceasync) function.</span></span> <span data-ttu-id="e0ec3-116">下列範例會傳遞在步驟1中取得的音訊轉譯識別碼：</span><span class="sxs-lookup"><span data-stu-id="e0ec3-116">The following example passes in the audio render identifier obtained in step 1:</span></span>

    ```C++
    //Activate the default audio interface
    ActivateAudioInterfaceAsync(audioRenderGuidString
                                __uuidof(IAudioClient),
                                NULL,
                                completionHandler.Get(),
                                operation.GetAddressOf()));
    ```

    

3.  <span data-ttu-id="e0ec3-117">釋放配置用來保存端點識別碼的記憶體：</span><span class="sxs-lookup"><span data-stu-id="e0ec3-117">Free the memory allocated for holding the endpoint identifier:</span></span>

    ```C++
    CoTaskMemFree(audioRenderGuidString);  //free the string memory
    ```

    

<span data-ttu-id="e0ec3-118">在您修改應用程式以上述方式啟動音訊介面之後，它會參與自動串流路由功能。</span><span class="sxs-lookup"><span data-stu-id="e0ec3-118">After you have modified your app to activate the audio interface in the manner described above, it will participate in the automatic stream routing feature.</span></span>

<span data-ttu-id="e0ec3-119">若要示範自動串流路由，請使用配備內部喇叭的膝上型電腦或平板電腦播放音訊。</span><span class="sxs-lookup"><span data-stu-id="e0ec3-119">To demonstrate automatic stream routing, use a laptop or tablet equipped with internal speakers to play back audio.</span></span> <span data-ttu-id="e0ec3-120">您應該會聽到透過裝置的內部喇叭播放音訊。</span><span class="sxs-lookup"><span data-stu-id="e0ec3-120">You should hear the audio playing through the device's internal speakers.</span></span> <span data-ttu-id="e0ec3-121">播放音訊時，連接一組耳機。</span><span class="sxs-lookup"><span data-stu-id="e0ec3-121">While audio is playing, connect a pair of headphones.</span></span> <span data-ttu-id="e0ec3-122">您現在應該會聽到透過耳機播放音訊。</span><span class="sxs-lookup"><span data-stu-id="e0ec3-122">You should now hear audio playing through the headphones.</span></span> <span data-ttu-id="e0ec3-123">然後，拔掉耳機和音訊應該會自動路由回內部喇叭。</span><span class="sxs-lookup"><span data-stu-id="e0ec3-123">Then, unplug the headphones and audio should automatically route back to the internal speakers.</span></span>

## <a name="related-topics"></a><span data-ttu-id="e0ec3-124">相關主題</span><span class="sxs-lookup"><span data-stu-id="e0ec3-124">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e0ec3-125">串流路由</span><span class="sxs-lookup"><span data-stu-id="e0ec3-125">Stream Routing</span></span>](stream-routing.md)
</dt> <dt>

[<span data-ttu-id="e0ec3-126">**MediaDevice.GetDefaultAudioRenderId**</span><span class="sxs-lookup"><span data-stu-id="e0ec3-126">**MediaDevice.GetDefaultAudioRenderId**</span></span>](/uwp/api/windows.media.devices.mediadevice.getdefaultaudiorenderid)
</dt> <dt>

[<span data-ttu-id="e0ec3-127">**MediaDevice.GetDefaultAudioCaptureId**</span><span class="sxs-lookup"><span data-stu-id="e0ec3-127">**MediaDevice.GetDefaultAudioCaptureId**</span></span>](/uwp/api/windows.media.devices.mediadevice.getdefaultaudiocaptureid)
</dt> <dt>

[<span data-ttu-id="e0ec3-128">**ActivateAudioInterfaceAsync**</span><span class="sxs-lookup"><span data-stu-id="e0ec3-128">**ActivateAudioInterfaceAsync**</span></span>](/windows/desktop/api/mmdeviceapi/nf-mmdeviceapi-activateaudiointerfaceasync)
</dt> </dl>

 

 
