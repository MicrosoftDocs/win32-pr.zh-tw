---
description: 音訊端點裝置
ms.assetid: 773714fb-3b00-4f03-988f-05c5835f87cf
title: 音訊端點裝置
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c14d21aa174e34f8cb4ddab520819446a0e0ec89
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103936496"
---
# <a name="audio-endpoint-devices"></a><span data-ttu-id="68235-103">音訊端點裝置</span><span class="sxs-lookup"><span data-stu-id="68235-103">Audio Endpoint Devices</span></span>

<span data-ttu-id="68235-104">「 *端點裝置* 」一詞是指在應用程式中源自或終止之資料路徑一端的硬體裝置。</span><span class="sxs-lookup"><span data-stu-id="68235-104">The term *endpoint device* refers to a hardware device that lies at one end of a data path that originates or terminates at an application program.</span></span> <span data-ttu-id="68235-105">音訊端點裝置的範例有喇叭、耳機、麥克風和 CD 播放機。</span><span class="sxs-lookup"><span data-stu-id="68235-105">Examples of audio endpoint devices are speakers, headphones, microphones, and CD players.</span></span> <span data-ttu-id="68235-106">沿著資料路徑移動的音訊資料可能會在應用程式與端點裝置之間的旅程期間，于數個軟體和硬體元件之間進行。</span><span class="sxs-lookup"><span data-stu-id="68235-106">The audio data that moves along the data path might traverse a number of software and hardware components during its journey between the application and endpoint device.</span></span> <span data-ttu-id="68235-107">雖然這些元件對端點裝置的作業而言是不可或缺的，但使用者通常會看不到這些元件。</span><span class="sxs-lookup"><span data-stu-id="68235-107">Although these components are essential to the operation of the endpoint device, they tend to be invisible to users.</span></span> <span data-ttu-id="68235-108">使用者比較可能會以端點裝置的方式來思考，而這些裝置會直接操控，而不是端點裝置所插入的裝置，或是在處理流入這些介面卡之音訊串流的軟體元件方面。</span><span class="sxs-lookup"><span data-stu-id="68235-108">Users are more likely to think in terms of endpoint devices that they directly manipulate rather than in terms of the devices on audio adapters that the endpoint devices plug into or in terms of the software components that process the audio streams that flow to and from these adapters.</span></span>

<span data-ttu-id="68235-109">為了避免與端點裝置混淆，本檔是指將音訊介面卡上的裝置視為 *介面卡裝置*。</span><span class="sxs-lookup"><span data-stu-id="68235-109">To avoid confusion with endpoint devices, this documentation refers to a device on an audio adapter as an *adapter device*.</span></span>

<span data-ttu-id="68235-110">下圖顯示音訊端點裝置與介面卡裝置有何不同。</span><span class="sxs-lookup"><span data-stu-id="68235-110">The following diagram shows how audio endpoint devices differ from adapter devices.</span></span>

![音訊端點裝置和介面卡裝置的範例](images/devices.jpg)

<span data-ttu-id="68235-112">在上圖中，下列是端點裝置的範例：</span><span class="sxs-lookup"><span data-stu-id="68235-112">In the preceding diagram, the following are examples of endpoint devices:</span></span>

-   <span data-ttu-id="68235-113">Speakers</span><span class="sxs-lookup"><span data-stu-id="68235-113">Speakers</span></span>
-   <span data-ttu-id="68235-114">麥克風</span><span class="sxs-lookup"><span data-stu-id="68235-114">Microphone</span></span>
-   <span data-ttu-id="68235-115">輔助輸入裝置</span><span class="sxs-lookup"><span data-stu-id="68235-115">Auxiliary input device</span></span>

<span data-ttu-id="68235-116">以下是介面卡裝置的範例：</span><span class="sxs-lookup"><span data-stu-id="68235-116">The following are examples of adapter devices:</span></span>

-   <span data-ttu-id="68235-117">Wave 輸出裝置 (包含數位轉類比轉換器) </span><span class="sxs-lookup"><span data-stu-id="68235-117">Wave output device (contains digital-to-analog converter)</span></span>
-   <span data-ttu-id="68235-118">輸出控制項裝置 (包含音量和靜音控制項) </span><span class="sxs-lookup"><span data-stu-id="68235-118">Output controls device (contains volume and mute controls)</span></span>
-   <span data-ttu-id="68235-119">Wave 輸入裝置 (包含類比轉數位轉換器) </span><span class="sxs-lookup"><span data-stu-id="68235-119">Wave input device (contains analog-to-digital converter)</span></span>
-   <span data-ttu-id="68235-120">輸入控制項裝置 (包含音量控制和多工器) </span><span class="sxs-lookup"><span data-stu-id="68235-120">Input controls device (contains volume control and multiplexer)</span></span>

<span data-ttu-id="68235-121">一般而言，音訊應用程式的使用者介面會參考音訊端點裝置，而不是介面卡裝置。</span><span class="sxs-lookup"><span data-stu-id="68235-121">Typically, the user interfaces of audio applications refer to audio endpoint devices, not to adapter devices.</span></span> <span data-ttu-id="68235-122">Windows Vista 直接支援端點裝置抽象化，以簡化方便使用的應用程式設計。</span><span class="sxs-lookup"><span data-stu-id="68235-122">Windows Vista simplifies the design of user-friendly applications by directly supporting the endpoint device abstraction.</span></span>

<span data-ttu-id="68235-123">某些端點裝置可能會永久連接到介面卡裝置。</span><span class="sxs-lookup"><span data-stu-id="68235-123">Some endpoint devices might permanently connect to an adapter device.</span></span> <span data-ttu-id="68235-124">例如，電腦可能包含已整合至系統底座的內部裝置，例如 CD 播放機、麥克風或喇叭。</span><span class="sxs-lookup"><span data-stu-id="68235-124">For example, a computer might contain internal devices such as a CD player, a microphone, or speakers that are integrated into the system chassis.</span></span> <span data-ttu-id="68235-125">一般而言，使用者不會實際移除這些端點裝置。</span><span class="sxs-lookup"><span data-stu-id="68235-125">Typically, the user does not physically remove these endpoint devices.</span></span>

<span data-ttu-id="68235-126">其他端點裝置可能會透過音訊插孔連接到音訊介面卡。</span><span class="sxs-lookup"><span data-stu-id="68235-126">Other endpoint devices might connect to an audio adapter through audio jacks.</span></span> <span data-ttu-id="68235-127">使用者會插入並拔除這些外部裝置。</span><span class="sxs-lookup"><span data-stu-id="68235-127">The user plugs in and unplugs these external devices.</span></span> <span data-ttu-id="68235-128">例如，像是外部麥克風或耳機的音訊端點裝置位於纜線的一端，另一端則插到介面卡裝置上的一個插座。</span><span class="sxs-lookup"><span data-stu-id="68235-128">For example, an audio endpoint device such as an external microphone or headphones lies at one end of a cable whose other end plugs into a jack on an adapter device.</span></span>

<span data-ttu-id="68235-129">介面卡會透過系統匯流排 (通常是 PCI 或 PCI Express) 或支援) 隨插即用 PnP (的外部匯流排 (USB 或 IEEE 1394) 來與系統處理器進行通訊。</span><span class="sxs-lookup"><span data-stu-id="68235-129">The adapter communicates with the system processor through a system bus (typically, PCI or PCI Express) or external bus (USB or IEEE 1394) that supports Plug and Play (PnP).</span></span> <span data-ttu-id="68235-130">在裝置列舉期間，隨插即用 manager 會識別音訊介面卡中的裝置，並註冊這些裝置，使其可供作業系統和應用程式使用。</span><span class="sxs-lookup"><span data-stu-id="68235-130">During device enumeration, the Plug and Play manager identifies the devices in the audio adapter and registers those devices to make them available for use by the operating system and by applications.</span></span>

<span data-ttu-id="68235-131">與介面卡和外部匯流排（例如 USB 或 IEEE 1394 匯流排）之間的連線不同，端點裝置與介面卡裝置之間的連線不支援 PnP 裝置偵測。</span><span class="sxs-lookup"><span data-stu-id="68235-131">Unlike the connection between an adapter and an external bus such as USB or the IEEE 1394 bus, the connection between an endpoint device and an adapter device does not support PnP device detection.</span></span> <span data-ttu-id="68235-132">不過，某些音訊介面卡支援 *插座存在性偵測*：當插入插入或從插孔移除時，硬體會產生插斷，以通知介面卡驅動程式硬體設定中的變更。</span><span class="sxs-lookup"><span data-stu-id="68235-132">However, some audio adapters support *jack-presence detection*: when a plug is inserted into or removed from a jack, the hardware generates an interrupt to notify the adapter driver of the change in the hardware configuration.</span></span> <span data-ttu-id="68235-133">Windows Vista 中的端點管理員可以利用此硬體功能，通知應用程式任何時候都有端點裝置。</span><span class="sxs-lookup"><span data-stu-id="68235-133">The endpoint manager in Windows Vista can exploit this hardware capability to notify applications which endpoint devices are present at any time.</span></span> <span data-ttu-id="68235-134">如此一來，端點管理員的操作就類似于隨插即用管理員的作業，它會追蹤系統中出現的介面卡裝置。</span><span class="sxs-lookup"><span data-stu-id="68235-134">In this way, the operation of the endpoint manager is analogous to that of the Plug and Play manager, which keeps track of the adapter devices that are present in the system.</span></span>

<span data-ttu-id="68235-135">在 Windows Vista 中，音訊系統會持續追蹤端點裝置和介面卡裝置。</span><span class="sxs-lookup"><span data-stu-id="68235-135">In Windows Vista, the audio system keeps track of both endpoint devices and adapter devices.</span></span> <span data-ttu-id="68235-136">端點管理員會註冊端點裝置，而隨插即用 manager 會註冊介面卡裝置。</span><span class="sxs-lookup"><span data-stu-id="68235-136">The endpoint manager registers endpoint devices and the Plug and Play manager registers adapter devices.</span></span> <span data-ttu-id="68235-137">註冊端點裝置可讓方便使用的應用程式，讓使用者能夠參考使用者直接操作的端點裝置，而不是參照可能隱藏在電腦底座內的介面卡裝置。</span><span class="sxs-lookup"><span data-stu-id="68235-137">Registering endpoint devices makes it easier for user-friendly applications to enable users to refer to the endpoint devices that users directly manipulate instead of referring to adapter devices that might be hidden inside the computer chassis.</span></span> <span data-ttu-id="68235-138">作業系統所報告的端點裝置可讓您在設定具有插座目前狀態偵測的音訊硬體時，即時追蹤其動態變更。</span><span class="sxs-lookup"><span data-stu-id="68235-138">The endpoint devices that are reported by the operating system faithfully track dynamic changes in the configuration of audio hardware that has jack-presence detection.</span></span> <span data-ttu-id="68235-139">當端點裝置保持插上狀態時，系統會列舉該裝置。</span><span class="sxs-lookup"><span data-stu-id="68235-139">While an endpoint device remains plugged in, the system enumerates that device.</span></span> <span data-ttu-id="68235-140">當使用者拔除端點裝置時，系統會停止列舉該裝置。</span><span class="sxs-lookup"><span data-stu-id="68235-140">When the user unplugs an endpoint device, the system ceases to enumerate it.</span></span>

<span data-ttu-id="68235-141">在舊版的 Windows 中，包括 Windows 98、Windows Me、Windows 2000 和 Windows XP，系統只會將 PnP 裝置明確呈現給應用程式。</span><span class="sxs-lookup"><span data-stu-id="68235-141">In earlier versions of Windows, including Windows 98, Windows Me, Windows 2000, and Windows XP, the system explicitly presents only PnP devices to applications.</span></span> <span data-ttu-id="68235-142">因此，應用程式必須推斷端點裝置是否存在。</span><span class="sxs-lookup"><span data-stu-id="68235-142">Thus, applications must infer the existence of endpoint devices.</span></span> <span data-ttu-id="68235-143">缺少對端點裝置明確支援的作業系統，會強制用戶端應用程式執行更多工作。</span><span class="sxs-lookup"><span data-stu-id="68235-143">An operating system that lacks explicit support for endpoint devices forces client applications to do more of the work themselves.</span></span> <span data-ttu-id="68235-144">例如，音訊捕獲應用程式必須執行下列步驟，才能從外部麥克風進行捕捉：</span><span class="sxs-lookup"><span data-stu-id="68235-144">For example, an audio capture application must perform the following steps to enable capturing from an external microphone:</span></span>

1.  <span data-ttu-id="68235-145">列舉所有音訊捕獲裝置 (這些都是 PnP 管理員先前註冊的介面卡裝置) 。</span><span class="sxs-lookup"><span data-stu-id="68235-145">Enumerate all the audio capture devices (these are adapter devices) that were previously registered by the PnP manager.</span></span>
2.  <span data-ttu-id="68235-146">選取擷取裝置之後，請呼叫 **waveInOpen** 函式或使用 **DIRECTSOUNDCAPTURE** 或 DirectShow API，在裝置上開啟 capture 串流。</span><span class="sxs-lookup"><span data-stu-id="68235-146">After selecting a capture device, open a capture stream on the device by either calling the **waveInOpen** function or by using the **DirectSoundCapture** or DirectShow API.</span></span>
3.  <span data-ttu-id="68235-147">呼叫 mixerOpen 函式，並使用其他 **mixerXxx** 函式來尋找 \_ \_ \_ 對應至步驟2中所開啟之捕捉裝置的 MIXERLINE COMPONENTTYPE SRC 麥克風行。</span><span class="sxs-lookup"><span data-stu-id="68235-147">Call the mixerOpen function and use the other **mixerXxx** functions to look for a MIXERLINE\_COMPONENTTYPE\_SRC\_MICROPHONE line that corresponds to the capture device opened in step 2.</span></span> <span data-ttu-id="68235-148">這是一項教育的猜測。</span><span class="sxs-lookup"><span data-stu-id="68235-148">This is an educated guess.</span></span>
4.  <span data-ttu-id="68235-149">從麥克風解除封鎖資料路徑。</span><span class="sxs-lookup"><span data-stu-id="68235-149">Unblock the data path from the microphone.</span></span> <span data-ttu-id="68235-150">如果資料路徑包含靜音節點，則用戶端必須停用來自麥克風的信號靜音。</span><span class="sxs-lookup"><span data-stu-id="68235-150">If the data path includes a mute node, then the client must disable muting of the signal from the microphone.</span></span> <span data-ttu-id="68235-151">如果捕捉裝置包含可從數個輸入中選取的多工器，則用戶端必須選取麥克風輸入。</span><span class="sxs-lookup"><span data-stu-id="68235-151">If the capture device contains a multiplexer for selecting from among several inputs, then the client must select the microphone input.</span></span>

<span data-ttu-id="68235-152">此程式很容易出錯，因為執行這些作業的軟體如果遇到其設計工具不會預期或未進行測試的硬體設定，可能會失敗。</span><span class="sxs-lookup"><span data-stu-id="68235-152">This process is error-prone because the software that performs these operations might fail if it encounters a hardware configuration that its designers did not anticipate or for which it was not tested.</span></span>

<span data-ttu-id="68235-153">在支援端點裝置的 Windows Vista 中，連接至相同端點裝置的程式更簡單：</span><span class="sxs-lookup"><span data-stu-id="68235-153">In Windows Vista, which supports endpoint devices, the process of connecting to the same endpoint device is much simpler:</span></span>

1.  <span data-ttu-id="68235-154">從端點裝置的集合中選取麥克風。</span><span class="sxs-lookup"><span data-stu-id="68235-154">Select a microphone from a collection of endpoint devices.</span></span>
2.  <span data-ttu-id="68235-155">在該麥克風上啟動音訊捕獲介面。</span><span class="sxs-lookup"><span data-stu-id="68235-155">Activate an audio-capture interface on that microphone.</span></span>

<span data-ttu-id="68235-156">作業系統會執行識別和啟用端點裝置所需的所有工作。</span><span class="sxs-lookup"><span data-stu-id="68235-156">The operating system does all the work necessary to identify and enable the endpoint device.</span></span> <span data-ttu-id="68235-157">例如，如果麥克風的資料路徑包含多工器，系統會自動選取麥克風輸入至多工器。</span><span class="sxs-lookup"><span data-stu-id="68235-157">For example, if the data path from the microphone includes a multiplexer, the system automatically selects the microphone input to the multiplexer.</span></span>

<span data-ttu-id="68235-158">如果應用程式（而不是執行自己的端點識別演算法）可以 relegate 將端點裝置識別為作業系統的工作，則音訊子系統的行為更可靠且具決定性。</span><span class="sxs-lookup"><span data-stu-id="68235-158">The behavior of the audio subsystem is more reliable and deterministic if applications, instead of implementing their own endpoint-identification algorithms, can relegate the task of identifying endpoint devices to the operating system.</span></span> <span data-ttu-id="68235-159">軟體廠商不再需要驗證其端點識別演算法是否可與所有可用的音訊硬體裝置和設定正確搭配運作，而只需依賴作業系統來識別端點。</span><span class="sxs-lookup"><span data-stu-id="68235-159">Software vendors no longer need to verify that their endpoint-identification algorithms work correctly with all available audio hardware devices and configurations—they can simply rely on the operating system for endpoint identification.</span></span> <span data-ttu-id="68235-160">同樣地，硬體廠商不再需要確認每個相關的用戶端應用程式都可以輕鬆地識別任何連線至其音訊介面卡的端點裝置，只需要確認作業系統可以識別連接至其音訊介面卡的端點裝置。</span><span class="sxs-lookup"><span data-stu-id="68235-160">Similarly, hardware vendors no longer need to verify that every relevant client application can readily identify any endpoint device that is connected to their audio adapter—they need only to verify that the operating system can identify an endpoint device that is connected to their audio adapter.</span></span>

<span data-ttu-id="68235-161">下列主題提供有關音訊端點裝置的其他資訊：</span><span class="sxs-lookup"><span data-stu-id="68235-161">The following topics provide additional information about audio endpoint devices:</span></span>

-   [<span data-ttu-id="68235-162">關於 MMDevice API</span><span class="sxs-lookup"><span data-stu-id="68235-162">About MMDevice API</span></span>](mmdevice-api.md)
-   [<span data-ttu-id="68235-163">列舉音訊裝置</span><span class="sxs-lookup"><span data-stu-id="68235-163">Enumerating Audio Devices</span></span>](enumerating-audio-devices.md)
-   [<span data-ttu-id="68235-164">端點識別碼字串</span><span class="sxs-lookup"><span data-stu-id="68235-164">Endpoint ID Strings</span></span>](endpoint-id-strings.md)
-   [<span data-ttu-id="68235-165">裝置內容</span><span class="sxs-lookup"><span data-stu-id="68235-165">Device Properties</span></span>](device-properties.md)
-   [<span data-ttu-id="68235-166">裝置事件</span><span class="sxs-lookup"><span data-stu-id="68235-166">Device Events</span></span>](device-events.md)
-   [<span data-ttu-id="68235-167">裝置角色</span><span class="sxs-lookup"><span data-stu-id="68235-167">Device Roles</span></span>](device-roles.md)
-   [<span data-ttu-id="68235-168">裝置格式</span><span class="sxs-lookup"><span data-stu-id="68235-168">Device Formats</span></span>](device-formats.md)

## <a name="related-topics"></a><span data-ttu-id="68235-169">相關主題</span><span class="sxs-lookup"><span data-stu-id="68235-169">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="68235-170">程式設計指南</span><span class="sxs-lookup"><span data-stu-id="68235-170">Programming Guide</span></span>](programming-guide.md)
</dt> </dl>

 

 



