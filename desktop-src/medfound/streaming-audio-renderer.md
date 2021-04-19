---
description: 串流音訊轉譯器 (特別行政區) 是可轉譯音訊的媒體接收器。
ms.assetid: 5884a128-597d-432b-a706-e10c894d7965
title: 串流音訊轉譯器
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f59c5b55f197d5e9770c6f1be55f680c7f9136f3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106969242"
---
# <a name="streaming-audio-renderer"></a><span data-ttu-id="a2ba7-103">串流音訊轉譯器</span><span class="sxs-lookup"><span data-stu-id="a2ba7-103">Streaming Audio Renderer</span></span>

<span data-ttu-id="a2ba7-104">串流音訊轉譯器 (特別行政區) 是可轉譯音訊的媒體接收器。</span><span class="sxs-lookup"><span data-stu-id="a2ba7-104">The streaming audio renderer (SAR) is a media sink that renders audio.</span></span> <span data-ttu-id="a2ba7-105">每個 SAR 實例都會轉譯單一音訊串流。</span><span class="sxs-lookup"><span data-stu-id="a2ba7-105">Each instance of the SAR renders a single audio stream.</span></span> <span data-ttu-id="a2ba7-106">若要轉譯多個資料流程，請使用多個 SAR 實例。</span><span class="sxs-lookup"><span data-stu-id="a2ba7-106">To render multiple streams, use multiple instances of the SAR.</span></span>

<span data-ttu-id="a2ba7-107">若要建立 SAR，請呼叫下列其中一項功能：</span><span class="sxs-lookup"><span data-stu-id="a2ba7-107">To create the SAR, call either of the following functions:</span></span>

-   <span data-ttu-id="a2ba7-108">[**MFCreateAudioRenderer**](/windows/desktop/api/mfidl/nf-mfidl-mfcreateaudiorenderer)。</span><span class="sxs-lookup"><span data-stu-id="a2ba7-108">[**MFCreateAudioRenderer**](/windows/desktop/api/mfidl/nf-mfidl-mfcreateaudiorenderer).</span></span> <span data-ttu-id="a2ba7-109">傳回 SAR 的指標。</span><span class="sxs-lookup"><span data-stu-id="a2ba7-109">Returns a pointer to the SAR.</span></span>
-   <span data-ttu-id="a2ba7-110">[**MFCreateAudioRendererActivate**](/windows/desktop/api/mfidl/nf-mfidl-mfcreateaudiorendereractivate)。</span><span class="sxs-lookup"><span data-stu-id="a2ba7-110">[**MFCreateAudioRendererActivate**](/windows/desktop/api/mfidl/nf-mfidl-mfcreateaudiorendereractivate).</span></span> <span data-ttu-id="a2ba7-111">傳回啟用物件的指標，該物件可用來建立 SAR。</span><span class="sxs-lookup"><span data-stu-id="a2ba7-111">Returns a pointer to an activation object, which can be used to create the SAR.</span></span>

<span data-ttu-id="a2ba7-112">如果您要播放受保護的內容，則需要第二個函式，它會傳回啟始物件，因為啟用物件必須序列化為受保護的進程。</span><span class="sxs-lookup"><span data-stu-id="a2ba7-112">The second function, which returns an activation object, is required if you are playing protected content, because the activation object must be serialized to the protected process.</span></span> <span data-ttu-id="a2ba7-113">如需清楚的內容，您可以使用其中一項功能。</span><span class="sxs-lookup"><span data-stu-id="a2ba7-113">For clear content, you can use either function.</span></span>

<span data-ttu-id="a2ba7-114">SAR 可以用 PCM 或 IEEE 浮點數格式接收未壓縮的音訊。</span><span class="sxs-lookup"><span data-stu-id="a2ba7-114">The SAR can receive uncompressed audio in either PCM or IEEE floating-point format.</span></span> <span data-ttu-id="a2ba7-115">如果播放速率比1×更快或慢，則 SAR 會自動調整間距。</span><span class="sxs-lookup"><span data-stu-id="a2ba7-115">If the playback rate is faster or slower than 1×, the SAR automatically adjusts the pitch.</span></span>

## <a name="configuring-the-audio-renderer"></a><span data-ttu-id="a2ba7-116">設定音訊轉譯器</span><span class="sxs-lookup"><span data-stu-id="a2ba7-116">Configuring the Audio Renderer</span></span>

<span data-ttu-id="a2ba7-117">SAR 支援數個設定屬性。</span><span class="sxs-lookup"><span data-stu-id="a2ba7-117">The SAR supports several configuration attributes.</span></span> <span data-ttu-id="a2ba7-118">設定這些屬性的機制，取決於您所呼叫用來建立 SAR 的函式。</span><span class="sxs-lookup"><span data-stu-id="a2ba7-118">The mechanism for setting these attributes depends on which function you call to create the SAR.</span></span> <span data-ttu-id="a2ba7-119">如果您使用 [**MFCreateAudioRenderer**](/windows/desktop/api/mfidl/nf-mfidl-mfcreateaudiorenderer) 函式，請執行下列動作：</span><span class="sxs-lookup"><span data-stu-id="a2ba7-119">If you use the [**MFCreateAudioRenderer**](/windows/desktop/api/mfidl/nf-mfidl-mfcreateaudiorenderer) function, do the following:</span></span>

1.  <span data-ttu-id="a2ba7-120">藉由呼叫 [**MFCreateAttributes**](/windows/desktop/api/mfapi/nf-mfapi-mfcreateattributes)來建立新的屬性存放區。</span><span class="sxs-lookup"><span data-stu-id="a2ba7-120">Create a new attribute store by calling [**MFCreateAttributes**](/windows/desktop/api/mfapi/nf-mfapi-mfcreateattributes).</span></span>
2.  <span data-ttu-id="a2ba7-121">將屬性加入至屬性存放區。</span><span class="sxs-lookup"><span data-stu-id="a2ba7-121">Add the attributes to the attribute store.</span></span>
3.  <span data-ttu-id="a2ba7-122">將屬性存放區傳遞給 *pAudioAttributes* 參數中的 [**MFCreateAudioRenderer**](/windows/desktop/api/mfidl/nf-mfidl-mfcreateaudiorenderer)函數。</span><span class="sxs-lookup"><span data-stu-id="a2ba7-122">Pass the attribute store to the [**MFCreateAudioRenderer**](/windows/desktop/api/mfidl/nf-mfidl-mfcreateaudiorenderer) function in the *pAudioAttributes* parameter.</span></span>

<span data-ttu-id="a2ba7-123">如果您使用 [**MFCreateAudioRendererActivate**](/windows/desktop/api/mfidl/nf-mfidl-mfcreateaudiorendereractivate)函式，此函式會將指標傳回至 *ppActivate* 參數中的 [**IMFAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes)介面。</span><span class="sxs-lookup"><span data-stu-id="a2ba7-123">If you use the [**MFCreateAudioRendererActivate**](/windows/desktop/api/mfidl/nf-mfidl-mfcreateaudiorendereractivate) function, the function returns a pointer to the [**IMFAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) interface in the *ppActivate* parameter.</span></span> <span data-ttu-id="a2ba7-124">使用這個指標來新增屬性。</span><span class="sxs-lookup"><span data-stu-id="a2ba7-124">Use this pointer to add the attributes.</span></span>

<span data-ttu-id="a2ba7-125">如需設定屬性的清單，請參閱音訊轉譯器 [屬性](audio-renderer-attributes.md)。</span><span class="sxs-lookup"><span data-stu-id="a2ba7-125">For a list of configuration attributes, see [Audio Renderer Attributes](audio-renderer-attributes.md).</span></span>

## <a name="selecting-the-audio-endpoint-device"></a><span data-ttu-id="a2ba7-126">選取音訊端點裝置</span><span class="sxs-lookup"><span data-stu-id="a2ba7-126">Selecting the Audio Endpoint Device</span></span>

<span data-ttu-id="a2ba7-127">*音訊端點裝置* 是一種硬體裝置，可轉譯或捕獲音訊。</span><span class="sxs-lookup"><span data-stu-id="a2ba7-127">An *audio endpoint device* is a hardware device that either renders or captures audio.</span></span> <span data-ttu-id="a2ba7-128">範例包括喇叭、耳機、麥克風和 CD 播放機。</span><span class="sxs-lookup"><span data-stu-id="a2ba7-128">Examples include speakers, headphones, microphones, and CD players.</span></span> <span data-ttu-id="a2ba7-129">SAR 一律會使用音訊轉譯裝置。</span><span class="sxs-lookup"><span data-stu-id="a2ba7-129">The SAR always uses an audio rendering device.</span></span> <span data-ttu-id="a2ba7-130">有兩種方式可以選取裝置。</span><span class="sxs-lookup"><span data-stu-id="a2ba7-130">There are two ways to select the device.</span></span>

<span data-ttu-id="a2ba7-131">第一個方法是使用 [**IMMDeviceEnumerator**](/windows/win32/api/mmdeviceapi/nn-mmdeviceapi-immdeviceenumerator) 介面，列舉系統上的音訊轉譯裝置。</span><span class="sxs-lookup"><span data-stu-id="a2ba7-131">The first approach is to enumerate the audio rendering devices on the system, using the [**IMMDeviceEnumerator**](/windows/win32/api/mmdeviceapi/nn-mmdeviceapi-immdeviceenumerator) interface.</span></span> <span data-ttu-id="a2ba7-132">此介面記載于核心音訊 API 檔中。</span><span class="sxs-lookup"><span data-stu-id="a2ba7-132">This interface is documented in the core audio API documentation.</span></span>

1.  <span data-ttu-id="a2ba7-133">建立裝置列舉值物件。</span><span class="sxs-lookup"><span data-stu-id="a2ba7-133">Create the device enumerator object.</span></span>
2.  <span data-ttu-id="a2ba7-134">使用裝置枚舉器來列舉音訊轉譯裝置。</span><span class="sxs-lookup"><span data-stu-id="a2ba7-134">Use the device enumerator to enumerate audio rendering devices.</span></span> <span data-ttu-id="a2ba7-135">每個裝置都以 [**IMMDevice**](/windows/win32/api/mmdeviceapi/nn-mmdeviceapi-immdevice) 介面的指標表示。</span><span class="sxs-lookup"><span data-stu-id="a2ba7-135">Each device is represented by a pointer to the [**IMMDevice**](/windows/win32/api/mmdeviceapi/nn-mmdeviceapi-immdevice) interface.</span></span>
3.  <span data-ttu-id="a2ba7-136">根據裝置屬性或使用者的選取專案，選取裝置。</span><span class="sxs-lookup"><span data-stu-id="a2ba7-136">Select a device, based on the device properties or the user's selection.</span></span>
4.  <span data-ttu-id="a2ba7-137">呼叫 [**IMMDevice：： GetId**](/windows/win32/api/mmdeviceapi/nf-mmdeviceapi-immdevice-getid) 來取得裝置識別碼。</span><span class="sxs-lookup"><span data-stu-id="a2ba7-137">Call [**IMMDevice::GetId**](/windows/win32/api/mmdeviceapi/nf-mmdeviceapi-immdevice-getid) to get the device identifier.</span></span>
5.  <span data-ttu-id="a2ba7-138">將裝置識別碼設定為 [ [**MF 音訊轉譯器 \_ \_ \_ 屬性 \_ 端點 \_ 識別碼**](mf-audio-renderer-attribute-endpoint-id-attribute.md) ] 屬性的值。</span><span class="sxs-lookup"><span data-stu-id="a2ba7-138">Set the device identifier as the value of the [**MF\_AUDIO\_RENDERER\_ATTRIBUTE\_ENDPOINT\_ID**](mf-audio-renderer-attribute-endpoint-id-attribute.md) attribute.</span></span>

<span data-ttu-id="a2ba7-139">您可以依裝置的 *角色* 指定音訊裝置，而不是列舉裝置。</span><span class="sxs-lookup"><span data-stu-id="a2ba7-139">Rather than enumerate devices, you can specify the audio device by its *role*.</span></span> <span data-ttu-id="a2ba7-140">音訊角色會識別使用方式的一般類別。</span><span class="sxs-lookup"><span data-stu-id="a2ba7-140">An audio role identifies a general category of usage.</span></span> <span data-ttu-id="a2ba7-141">例如， *主控台* 角色是針對遊戲和系統通知所定義，而 *多媒體* 角色則是針對音樂和電影而定義。</span><span class="sxs-lookup"><span data-stu-id="a2ba7-141">For example, the *console* role is defined for games and system notifications, while the *multimedia* role is defined for music and movies.</span></span> <span data-ttu-id="a2ba7-142">每個角色都有一個指派給它的音訊轉譯裝置，而且使用者可以變更這些指派。</span><span class="sxs-lookup"><span data-stu-id="a2ba7-142">Each role has one audio rendering device assigned to it, and the user can change these assignments.</span></span> <span data-ttu-id="a2ba7-143">如果您指定裝置角色，則會使用指派給該角色的任何音訊裝置。</span><span class="sxs-lookup"><span data-stu-id="a2ba7-143">If you specify a device role, the SAR uses whatever audio device has been assigned for that role.</span></span> <span data-ttu-id="a2ba7-144">若要指定裝置角色，請設定 [ [**MF 音訊轉譯器 \_ 屬性] \_ \_ \_ 端點 \_ 角色**](mf-audio-renderer-attribute-endpoint-role-attribute.md) 屬性。</span><span class="sxs-lookup"><span data-stu-id="a2ba7-144">To specify the device role, set the [**MF\_AUDIO\_RENDERER\_ATTRIBUTE\_ENDPOINT\_ROLE**](mf-audio-renderer-attribute-endpoint-role-attribute.md) attribute.</span></span>

<span data-ttu-id="a2ba7-145">本節所列的兩個屬性是互斥的。</span><span class="sxs-lookup"><span data-stu-id="a2ba7-145">The two attributes listed in this section are mutually exclusive.</span></span> <span data-ttu-id="a2ba7-146">如果您未設定任何一個，則會使用指派給 **eConsole** 角色的音訊裝置。</span><span class="sxs-lookup"><span data-stu-id="a2ba7-146">If you do not set either of them, the SAR uses the audio device that is assigned to the **eConsole** role.</span></span>

<span data-ttu-id="a2ba7-147">下列程式碼會列舉音訊轉譯裝置，並將清單中的第一個裝置指派給 SAR。</span><span class="sxs-lookup"><span data-stu-id="a2ba7-147">The following code enumerates the audio rendering devices and assigns the first device in the list to the SAR.</span></span> <span data-ttu-id="a2ba7-148">這個範例會使用 [**MFCreateAudioRenderer**](/windows/desktop/api/mfidl/nf-mfidl-mfcreateaudiorenderer) 函數來建立 SAR。</span><span class="sxs-lookup"><span data-stu-id="a2ba7-148">This example uses the [**MFCreateAudioRenderer**](/windows/desktop/api/mfidl/nf-mfidl-mfcreateaudiorenderer) function to create the SAR.</span></span>


```C++
#include <mmdeviceapi.h>

HRESULT hr = S_OK;

IMMDeviceEnumerator *pEnum = NULL;      // Audio device enumerator.
IMMDeviceCollection *pDevices = NULL;   // Audio device collection.
IMMDevice *pDevice = NULL;              // An audio device.
IMFAttributes *pAttributes = NULL;      // Attribute store.
IMFMediaSink *pSink = NULL;             // Streaming audio renderer (SAR)

LPWSTR wstrID = NULL;                   // Device ID.

// Create the device enumerator.
hr = CoCreateInstance(
    __uuidof(MMDeviceEnumerator), 
    NULL,
    CLSCTX_ALL, 
    __uuidof(IMMDeviceEnumerator), 
    (void**)&pEnum
    );

// Enumerate the rendering devices.
if (SUCCEEDED(hr))
{
    hr = pEnum->EnumAudioEndpoints(eRender, DEVICE_STATE_ACTIVE, &pDevices);
}

// Get ID of the first device in the list.
if (SUCCEEDED(hr))
{
    hr = pDevices->Item(0, &pDevice);
}

if (SUCCEEDED(hr))
{
    hr = pDevice->GetId(&wstrID);
}

// Create an attribute store and set the device ID attribute.
if (SUCCEEDED(hr))
{
    hr = MFCreateAttributes(&pAttributes, 2);
}

if (SUCCEEDED(hr))
{
    hr = pAttributes->SetString(
        MF_AUDIO_RENDERER_ATTRIBUTE_ENDPOINT_ID, 
        wstrID
        );
}

// Create the audio renderer.
if (SUCCEEDED(hr))
{
    hr = MFCreateAudioRenderer(pAttributes, &pSink);    
}

SAFE_RELEASE(pEnum);
SAFE_RELEASE(pDevices);
SAFE_RELEASE(pDevice); 
SAFE_RELEASE(pAttributes);
CoTaskMemFree(wstrID);
```



<span data-ttu-id="a2ba7-149">若要建立 SAR 的啟用物件，請將呼叫 [**IMMDevice：： GetId**](/windows/win32/api/mmdeviceapi/nf-mmdeviceapi-immdevice-getid) 之後出現的程式碼變更為下列程式碼：</span><span class="sxs-lookup"><span data-stu-id="a2ba7-149">To create the activation object for the SAR, change the code that appears after the call to [**IMMDevice::GetId**](/windows/win32/api/mmdeviceapi/nf-mmdeviceapi-immdevice-getid) to the following:</span></span>


```C++
IMFActivate *pActivate = NULL;          // Activation object.

if (SUCCEEDED(hr))
{
    hr = MFCreateAudioRendererActivate(&pActivate);    
}

if (SUCCEEDED(hr))
{
    hr = pActivate->SetString(
        MF_AUDIO_RENDERER_ATTRIBUTE_ENDPOINT_ID, 
        wstrID
        );
}

SAFE_RELEASE(pActivate);
```



## <a name="selecting-the-audio-session"></a><span data-ttu-id="a2ba7-150">選取音訊會話</span><span class="sxs-lookup"><span data-stu-id="a2ba7-150">Selecting the Audio Session</span></span>

<span data-ttu-id="a2ba7-151">音訊會話是應用程式可以共同管理的一組相關音訊串流。</span><span class="sxs-lookup"><span data-stu-id="a2ba7-151">An audio session is a group of related audio streams that an application can manage collectively.</span></span> <span data-ttu-id="a2ba7-152">應用程式可以控制每個會話的磁片區層級和靜音狀態。</span><span class="sxs-lookup"><span data-stu-id="a2ba7-152">The application can control the volume level and mute state of each session.</span></span> <span data-ttu-id="a2ba7-153">會話是由 GUID 所識別。</span><span class="sxs-lookup"><span data-stu-id="a2ba7-153">Sessions are identified by GUID.</span></span> <span data-ttu-id="a2ba7-154">若要指定 SAR 的音訊會話，請使用 [ [MF \_ 音訊轉譯器 \_ \_ 屬性 \_ 會話 \_ 識別碼](mf-audio-renderer-attribute-session-id-attribute.md) ] 屬性。</span><span class="sxs-lookup"><span data-stu-id="a2ba7-154">To specify the audio session for the SAR, use the [MF\_AUDIO\_RENDERER\_ATTRIBUTE\_SESSION\_ID](mf-audio-renderer-attribute-session-id-attribute.md) attribute.</span></span> <span data-ttu-id="a2ba7-155">如果您未設定此屬性，則會將該進程的預設會話（由 **GUID \_ Null** 識別）聯結。</span><span class="sxs-lookup"><span data-stu-id="a2ba7-155">If you do not set this attribute, the SAR joins the default session for that process, identified by **GUID\_NULL**.</span></span>

<span data-ttu-id="a2ba7-156">根據預設，音訊會話是進程專屬的，這表示它只會包含來自呼叫進程的串流。</span><span class="sxs-lookup"><span data-stu-id="a2ba7-156">By default, an audio session is process-specific, meaning it contains only streams from the calling process.</span></span> <span data-ttu-id="a2ba7-157">若要加入跨進程會話，請使用值 **mf 音訊轉譯器 \_ \_ \_ 屬性 \_ 旗標 \_ CROSSPROCESS** 來設定 [mf 音訊轉譯器 \_ \_ \_ 屬性 \_ 旗標](mf-audio-renderer-attribute-flags-attribute.md)屬性。</span><span class="sxs-lookup"><span data-stu-id="a2ba7-157">To join a cross-process session, set the [MF\_AUDIO\_RENDERER\_ATTRIBUTE\_FLAGS](mf-audio-renderer-attribute-flags-attribute.md) attribute with the value **MF\_AUDIO\_RENDERER\_ATTRIBUTE\_FLAGS\_CROSSPROCESS**.</span></span>

<span data-ttu-id="a2ba7-158">建立 SAR 之後，您可以使用 [**IMFAudioPolicy**](/windows/desktop/api/mfidl/nn-mfidl-imfaudiopolicy) 介面將會話加入會話的群組，這些都是由 [控制台] 中的相同 [音量] 控制項所控制。</span><span class="sxs-lookup"><span data-stu-id="a2ba7-158">After you create the SAR, you use the [**IMFAudioPolicy**](/windows/desktop/api/mfidl/nn-mfidl-imfaudiopolicy) interface to join the session to a group of sessions, all of which are controlled by the same volume control in the control panel.</span></span> <span data-ttu-id="a2ba7-159">您也可以使用此介面來設定顯示名稱，以及顯示在音量控制項中的圖示。</span><span class="sxs-lookup"><span data-stu-id="a2ba7-159">You can also use this interface to set the display name and the icon that appear in the volume control.</span></span>

## <a name="controlling-volume-levels"></a><span data-ttu-id="a2ba7-160">控制磁片區層級</span><span class="sxs-lookup"><span data-stu-id="a2ba7-160">Controlling Volume Levels</span></span>

<span data-ttu-id="a2ba7-161">若要控制 SAR 音訊會話中所有資料流程的主要音量層級，請使用 [**IMFSimpleAudioVolume**](/windows/desktop/api/mfidl/nn-mfidl-imfsimpleaudiovolume) 介面。</span><span class="sxs-lookup"><span data-stu-id="a2ba7-161">To control the master volume level of all the streams in the SAR's audio session, use the [**IMFSimpleAudioVolume**](/windows/desktop/api/mfidl/nn-mfidl-imfsimpleaudiovolume) interface.</span></span> <span data-ttu-id="a2ba7-162">若要控制個別資料流程的數量，或控制串流內個別通道的數量，請使用 [**IMFAudioStreamVolume**](/windows/desktop/api/mfidl/nn-mfidl-imfaudiostreamvolume) 介面。</span><span class="sxs-lookup"><span data-stu-id="a2ba7-162">To control the volume of an individual stream, or to control the volume of individual channels within a stream, use the [**IMFAudioStreamVolume**](/windows/desktop/api/mfidl/nn-mfidl-imfaudiostreamvolume) interface.</span></span> <span data-ttu-id="a2ba7-163">這兩個介面都是藉由呼叫 [**IMFGetService：： GetService**](/windows/desktop/api/mfidl/nf-mfidl-imfgetservice-getservice)來取得。</span><span class="sxs-lookup"><span data-stu-id="a2ba7-163">Both interfaces are obtained by calling [**IMFGetService::GetService**](/windows/desktop/api/mfidl/nf-mfidl-imfgetservice-getservice).</span></span> <span data-ttu-id="a2ba7-164">您可以直接在 SAR 上呼叫 **GetService** ，或在媒體會話上呼叫它。</span><span class="sxs-lookup"><span data-stu-id="a2ba7-164">You can call **GetService** directly on the SAR, or call it on the Media Session.</span></span> <span data-ttu-id="a2ba7-165">磁片區層級會以衰減值表示。</span><span class="sxs-lookup"><span data-stu-id="a2ba7-165">Volume levels are expressed as attenuation values.</span></span> <span data-ttu-id="a2ba7-166">針對每個通道，衰減層級是主要磁碟區和通道磁片區的乘積。</span><span class="sxs-lookup"><span data-stu-id="a2ba7-166">For each channel, the attenuation level is the product of the master volume and the channel volume.</span></span>

## <a name="related-topics"></a><span data-ttu-id="a2ba7-167">相關主題</span><span class="sxs-lookup"><span data-stu-id="a2ba7-167">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a2ba7-168">音訊/視訊播放</span><span class="sxs-lookup"><span data-stu-id="a2ba7-168">Audio/Video Playback</span></span>](audio-video-playback.md)
</dt> </dl>

 

 
