---
description: 回送記錄
ms.assetid: 71c567f7-fffa-4b75-897a-63ed30c4c9b0
title: 回送記錄
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 374da7497096118905f5e4c79bbacda832a42a7b
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103936412"
---
# <a name="loopback-recording"></a><span data-ttu-id="b62ad-103">回送記錄</span><span class="sxs-lookup"><span data-stu-id="b62ad-103">Loopback Recording</span></span>

<span data-ttu-id="b62ad-104">在回送模式中，WASAPI 的用戶端可以捕獲呈現端點裝置所播放的音訊串流。</span><span class="sxs-lookup"><span data-stu-id="b62ad-104">In loopback mode, a client of WASAPI can capture the audio stream that is being played by a rendering endpoint device.</span></span> <span data-ttu-id="b62ad-105">若要以回送模式開啟資料流程，用戶端必須：</span><span class="sxs-lookup"><span data-stu-id="b62ad-105">To open a stream in loopback mode, the client must:</span></span>

-   <span data-ttu-id="b62ad-106">取得呈現端點裝置的 [**IMMDevice**](/windows/desktop/api/Mmdeviceapi/nn-mmdeviceapi-immdevice) 介面。</span><span class="sxs-lookup"><span data-stu-id="b62ad-106">Obtain an [**IMMDevice**](/windows/desktop/api/Mmdeviceapi/nn-mmdeviceapi-immdevice) interface for the rendering endpoint device.</span></span>
-   <span data-ttu-id="b62ad-107">在轉譯端點裝置上以回送模式初始化捕獲資料流程。</span><span class="sxs-lookup"><span data-stu-id="b62ad-107">Initialize a capture stream in loopback mode on the rendering endpoint device.</span></span>

<span data-ttu-id="b62ad-108">在遵循這些步驟之後，用戶端可以呼叫 [**IAudioClient：： GetService**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-getservice) 方法，以取得轉譯端點裝置上的 [**IAudioCaptureClient**](/windows/desktop/api/Audioclient/nn-audioclient-iaudiocaptureclient) 介面。</span><span class="sxs-lookup"><span data-stu-id="b62ad-108">After following these steps, the client can call the [**IAudioClient::GetService**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-getservice) method to obtain an [**IAudioCaptureClient**](/windows/desktop/api/Audioclient/nn-audioclient-iaudiocaptureclient) interface on the rendering endpoint device.</span></span>

<span data-ttu-id="b62ad-109">WASAPI 會提供回送模式，主要是為了支援 (AEC) 的聲場回應取消。</span><span class="sxs-lookup"><span data-stu-id="b62ad-109">WASAPI provides loopback mode primarily to support acoustic echo cancellation (AEC).</span></span> <span data-ttu-id="b62ad-110">不過，其他類型的音訊應用程式可能會發現回送模式對於捕捉音訊引擎所播放的系統混合很有用。</span><span class="sxs-lookup"><span data-stu-id="b62ad-110">However, other types of audio applications might find loopback mode useful for capturing the system mix that is being played by the audio engine.</span></span>

<span data-ttu-id="b62ad-111">在 [捕捉資料流程](capturing-a-stream.md)的程式碼範例中，您可以輕鬆地修改 RecordAudioStream 函數來設定回送模式的捕獲資料流程。</span><span class="sxs-lookup"><span data-stu-id="b62ad-111">In the code example in [Capturing a Stream](capturing-a-stream.md), the RecordAudioStream function can be easily modified to configure a loopback-mode capture stream.</span></span> <span data-ttu-id="b62ad-112">必要的修改包括：</span><span class="sxs-lookup"><span data-stu-id="b62ad-112">The required modifications are:</span></span>

-   <span data-ttu-id="b62ad-113">在 [**IMMDeviceEnumerator：： GetDefaultAudioEndpoint**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdeviceenumerator-getdefaultaudioendpoint) 方法的呼叫中，將 (*資料流程*) 的第一個參數從 eCapture 變更為 eRender。</span><span class="sxs-lookup"><span data-stu-id="b62ad-113">In the call to the [**IMMDeviceEnumerator::GetDefaultAudioEndpoint**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdeviceenumerator-getdefaultaudioendpoint) method, change the first parameter (*dataFlow*) from eCapture to eRender.</span></span>
-   <span data-ttu-id="b62ad-114">在 [**IAudioClient：： Initialize**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-initialize) 方法的呼叫中，將第二個參數的值 (*StreamFlags*) 從0變更為 AUDCLNT \_ StreamFlags \_ 回送。</span><span class="sxs-lookup"><span data-stu-id="b62ad-114">In the call to the [**IAudioClient::Initialize**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-initialize) method, change the value of the second parameter (*StreamFlags*) from 0 to AUDCLNT\_STREAMFLAGS\_LOOPBACK.</span></span>

<span data-ttu-id="b62ad-115">在 Windows 10 1703 之前的 Windows 版本中，提取模式捕捉用戶端不會在使用事件驅動緩衝來初始化資料流程時接收任何事件，而且會啟用回送功能。</span><span class="sxs-lookup"><span data-stu-id="b62ad-115">In versions of Windows prior to Windows 10 1703, pull-mode capture client does not receive any events when a stream is initialized with event-driven buffering and is loopback-enabled.</span></span> <span data-ttu-id="b62ad-116">若要解決這個問題，請在事件驅動模式中初始化轉譯資料流程。</span><span class="sxs-lookup"><span data-stu-id="b62ad-116">To work around this, initialize a render stream in event-driven mode.</span></span> <span data-ttu-id="b62ad-117">每次用戶端收到轉譯資料流程的事件時，必須通知 capture 用戶端執行捕獲執行緒，以從 capture 端點緩衝區讀取下一組範例。</span><span class="sxs-lookup"><span data-stu-id="b62ad-117">Each time the client receives an event for the render stream, it must signal the capture client to run the capture thread that reads the next set of samples from the capture endpoint buffer.</span></span> <span data-ttu-id="b62ad-118">在 Windows 10 1703 和更新版本中，支援事件驅動的回送用戶端，而且不再需要涉及轉譯資料流程的因應措施。</span><span class="sxs-lookup"><span data-stu-id="b62ad-118">In Windows 10 versions 1703 and higher, event-driven loopback clients are supported, and no longer need the workaround involving the render stream.</span></span>  

<span data-ttu-id="b62ad-119">用戶端只能針對共用模式串流啟用回送模式， (AUDCLNT \_ SHAREMODE \_ 共用) 。</span><span class="sxs-lookup"><span data-stu-id="b62ad-119">A client can enable loopback mode only for a shared-mode stream (AUDCLNT\_SHAREMODE\_SHARED).</span></span> <span data-ttu-id="b62ad-120">獨佔模式資料流程無法在回送模式下運作。</span><span class="sxs-lookup"><span data-stu-id="b62ad-120">Exclusive-mode streams cannot operate in loopback mode.</span></span>

<span data-ttu-id="b62ad-121">WASAPI 回送的執行取決於硬體的功能。</span><span class="sxs-lookup"><span data-stu-id="b62ad-121">The implementation of loopback by WASAPI depend on the capabilities of the hardware.</span></span> <span data-ttu-id="b62ad-122">如果硬體支援轉譯端點上的回送 pin，WASAPI 會使用此 pin 提供的音訊來提供回送資料流程。</span><span class="sxs-lookup"><span data-stu-id="b62ad-122">If the hardware supports a loopback pin on the render endpoint, WASAPI uses the audio provided on this pin for the loopback stream.</span></span> <span data-ttu-id="b62ad-123">當硬體不支援回送 pin 時，除了將音訊資料複製到硬體的轉譯 pin 之外，WASAPI 還會將音訊引擎的輸出資料流程複製到回送應用程式的擷取緩衝區。</span><span class="sxs-lookup"><span data-stu-id="b62ad-123">When the hardware does not support a loopback pin, WASAPI copies the output stream from the audio engine into the loopback application's capture buffer, in addition to copying the audio data to the hardware's render pin.</span></span>

<span data-ttu-id="b62ad-124">有些硬體廠商會將回送設備 (，而不是在其音訊介面卡) 的轉譯裝置上釘選實例。</span><span class="sxs-lookup"><span data-stu-id="b62ad-124">Some hardware vendors implement loopback devices (as opposed to pin instances on render devices) in their audio adapters.</span></span> <span data-ttu-id="b62ad-125">雖然硬體回送裝置類似于 WASAPI 回送模式的操作，但它們可能更難使用。</span><span class="sxs-lookup"><span data-stu-id="b62ad-125">Although hardware loopback devices are similar in operation to the WASAPI loopback mode, they can be more difficult to use.</span></span>

<span data-ttu-id="b62ad-126">硬體回送裝置對於音訊應用程式有下列缺點：</span><span class="sxs-lookup"><span data-stu-id="b62ad-126">Hardware loopback devices have the following disadvantages for audio applications:</span></span>

-   <span data-ttu-id="b62ad-127">並非所有音訊介面卡都有回送裝置。</span><span class="sxs-lookup"><span data-stu-id="b62ad-127">Not all audio adapters have loopback devices.</span></span> <span data-ttu-id="b62ad-128">因此，相依于這些應用程式的應用程式將無法在所有系統上運作。</span><span class="sxs-lookup"><span data-stu-id="b62ad-128">Thus, applications that depend on them will not work on all systems.</span></span>
-   <span data-ttu-id="b62ad-129">在應用程式可以從回送裝置錄製之前，使用者必須先識別回送裝置，並加以啟用以供使用。</span><span class="sxs-lookup"><span data-stu-id="b62ad-129">Before an application can record from a loopback device, the user must identify the loopback device and enable it for use.</span></span>

<span data-ttu-id="b62ad-130">不同的廠商會將不同的名稱指派給他們的硬體回送裝置。</span><span class="sxs-lookup"><span data-stu-id="b62ad-130">Different vendors assign different names to their hardware loopback devices.</span></span> <span data-ttu-id="b62ad-131">以下是範例的名稱：</span><span class="sxs-lookup"><span data-stu-id="b62ad-131">The following names are examples:</span></span>

-   <span data-ttu-id="b62ad-132">身歷聲混合</span><span class="sxs-lookup"><span data-stu-id="b62ad-132">Stereo Mix</span></span>
-   <span data-ttu-id="b62ad-133">Waveout 混合</span><span class="sxs-lookup"><span data-stu-id="b62ad-133">Waveout Mix</span></span>
-   <span data-ttu-id="b62ad-134">混合輸出</span><span class="sxs-lookup"><span data-stu-id="b62ad-134">Mixed Output</span></span>
-   <span data-ttu-id="b62ad-135">您聽到的內容</span><span class="sxs-lookup"><span data-stu-id="b62ad-135">What You Hear</span></span>

<span data-ttu-id="b62ad-136">缺乏標準化名稱可能會導致使用者難以識別裝置名稱清單中的回送裝置。</span><span class="sxs-lookup"><span data-stu-id="b62ad-136">The lack of standardized names might cause users to have difficulty identifying a loopback device in a list of device names.</span></span>

<span data-ttu-id="b62ad-137">硬體回送裝置是一種捕獲裝置。</span><span class="sxs-lookup"><span data-stu-id="b62ad-137">A hardware loopback device is a capture device.</span></span> <span data-ttu-id="b62ad-138">因此，如果介面卡支援回送裝置，音訊應用程式可以從裝置記錄，其方式與從任何其他捕獲裝置記錄的方式相同。</span><span class="sxs-lookup"><span data-stu-id="b62ad-138">Thus, if an adapter supports a loopback device, an audio application can record from the device in the same way that it records from any other capture device.</span></span>

<span data-ttu-id="b62ad-139">例如，如果您選取要做為預設捕獲裝置的硬體回送裝置，則可以使用 RecordAudioStream 函式 (而不需要修改) 在 [捕捉串流](capturing-a-stream.md) 以從裝置捕獲串流的程式碼範例中。</span><span class="sxs-lookup"><span data-stu-id="b62ad-139">For example, if you select a hardware loopback device to be the default capture device, you can use the RecordAudioStream function (without modification) in the code example in [Capturing a Stream](capturing-a-stream.md) to capture the stream from the device.</span></span> <span data-ttu-id="b62ad-140"> (您也可以使用舊版音訊 API （例如 Windows 多媒體 **waveInXxx** 函式），從裝置捕獲串流。 ) </span><span class="sxs-lookup"><span data-stu-id="b62ad-140">(You can also use a legacy audio API, such as the Windows multimedia **waveInXxx** functions, to capture the stream from the device.)</span></span>

<span data-ttu-id="b62ad-141">如果您的音訊介面卡包含硬體回送裝置，您可以使用 [Windows 多媒體] 控制台 Mmsys.cpl，將裝置指定為預設的擷取裝置。</span><span class="sxs-lookup"><span data-stu-id="b62ad-141">If your audio adapter contains a hardware loopback device, you can use the Windows multimedia control panel, Mmsys.cpl, to designate the device as the default capture device.</span></span> <span data-ttu-id="b62ad-142">步驟如下：</span><span class="sxs-lookup"><span data-stu-id="b62ad-142">The steps are as follows:</span></span>

1.  <span data-ttu-id="b62ad-143">若要執行 Mmsys.cpl，請開啟命令提示字元視窗，然後輸入下列命令：</span><span class="sxs-lookup"><span data-stu-id="b62ad-143">To run Mmsys.cpl, open a Command Prompt window and enter the following command:</span></span>

    ```C++
    control mmsys.cpl,,1
    ```

    

    <span data-ttu-id="b62ad-144">或者，您也可以用滑鼠右鍵按一下通知區域中的喇叭圖示（位於工作列右邊），然後選取 [ **錄製裝置**] 來執行 Mmsys.cpl。</span><span class="sxs-lookup"><span data-stu-id="b62ad-144">Alternatively, you can run Mmsys.cpl by right-clicking the speaker icon in the notification area, which is located on the right side of the taskbar, and selecting **Recording Devices**.</span></span>

2.  <span data-ttu-id="b62ad-145">Mmsys.cpl 視窗開啟後，以滑鼠右鍵按一下錄製裝置清單中的任意位置，並確認已核取 [ **顯示已停用的裝置** ] 選項。</span><span class="sxs-lookup"><span data-stu-id="b62ad-145">After the Mmsys.cpl window opens, right-click anywhere in the list of recording devices and verify that the **Show Disabled Devices** option is checked.</span></span> <span data-ttu-id="b62ad-146"> (否則，如果回送裝置已停用，它就不會出現在清單中。 ) </span><span class="sxs-lookup"><span data-stu-id="b62ad-146">(Otherwise, if the loopback device is disabled, it will not appear in the list.)</span></span>
3.  <span data-ttu-id="b62ad-147">流覽錄製的裝置清單，找出回送裝置 (是否存在) 。</span><span class="sxs-lookup"><span data-stu-id="b62ad-147">Browse the list of recording devices to locate the loopback device (if it exists).</span></span> <span data-ttu-id="b62ad-148">如果回送裝置已停用，請在裝置上按一下滑鼠右鍵，然後按一下 [ **啟用**] 來啟用它。</span><span class="sxs-lookup"><span data-stu-id="b62ad-148">If the loopback device is disabled, enable it by right-clicking the device and clicking **Enable**.</span></span>
4.  <span data-ttu-id="b62ad-149">最後，若要選取作為預設擷取裝置的回送裝置，請在裝置上按一下滑鼠右鍵，然後按一下 [ **設定為預設裝置**]。</span><span class="sxs-lookup"><span data-stu-id="b62ad-149">Finally, to select the loopback device to be the default capture device, right-click the device and click **Set as Default Device**.</span></span>

<span data-ttu-id="b62ad-150">無論音訊硬體是否包含回送裝置，或使用者是否已啟用裝置，WASAPI 都支援回送記錄。</span><span class="sxs-lookup"><span data-stu-id="b62ad-150">WASAPI supports loopback recording regardless of whether the audio hardware contains a loopback device, or whether the user has enabled the device.</span></span>

<span data-ttu-id="b62ad-151">Windows Vista 提供 (DRM) 的數位版權管理。</span><span class="sxs-lookup"><span data-stu-id="b62ad-151">Windows Vista provides digital rights management (DRM).</span></span> <span data-ttu-id="b62ad-152">內容提供者依賴 DRM 保護其專屬音樂或其他內容，防止未經授權的複製和其他非法用途。</span><span class="sxs-lookup"><span data-stu-id="b62ad-152">Content providers rely on DRM to protect their proprietary music or other content from unauthorized copying and other illegal uses.</span></span> <span data-ttu-id="b62ad-153">同樣地，受信任音訊驅動程式不允許回送裝置捕獲包含受保護內容的數位串流。</span><span class="sxs-lookup"><span data-stu-id="b62ad-153">Similarly, a trusted audio driver does not permit a loopback device to capture digital streams that contain protected content.</span></span> <span data-ttu-id="b62ad-154">Windows Vista 只允許信任的驅動程式播放受保護的內容。</span><span class="sxs-lookup"><span data-stu-id="b62ad-154">Windows Vista allows only trusted drivers to play protected content.</span></span> <span data-ttu-id="b62ad-155">如需有關信任的驅動程式和 DRM 的詳細資訊，請參閱 Windows DDK 檔。</span><span class="sxs-lookup"><span data-stu-id="b62ad-155">For more information about trusted drivers and DRM, see the Windows DDK documentation.</span></span>

<span data-ttu-id="b62ad-156">無論音訊源自何種終端機服務會話，WASAPI 回送都包含所有播放中音訊的混合。</span><span class="sxs-lookup"><span data-stu-id="b62ad-156">WASAPI loopback contains the mix of all audio being played, regardless of the Terminal Services session the audio originated from.</span></span> <span data-ttu-id="b62ad-157">例如，您可以在會話0執行的服務中執行回送用戶端，並從所有使用者會話捕獲音訊，以及從會話0播放音訊。</span><span class="sxs-lookup"><span data-stu-id="b62ad-157">For example, you can run a loopback client in a service running in session 0 and capture audio from all user sessions, as well as audio being played from session 0.</span></span>

<span data-ttu-id="b62ad-158">遠端桌面可讓您將音訊重新導向至用戶端。</span><span class="sxs-lookup"><span data-stu-id="b62ad-158">Remote Desktop allows redirecting audio to the client.</span></span> <span data-ttu-id="b62ad-159">這是藉由建立只顯示該會話的新音訊裝置來實行。</span><span class="sxs-lookup"><span data-stu-id="b62ad-159">This is implemented by creating new audio devices that only appear for that session.</span></span>

## <a name="related-topics"></a><span data-ttu-id="b62ad-160">相關主題</span><span class="sxs-lookup"><span data-stu-id="b62ad-160">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b62ad-161">串流管理</span><span class="sxs-lookup"><span data-stu-id="b62ad-161">Stream Management</span></span>](stream-management.md)
</dt> </dl>

 

 



