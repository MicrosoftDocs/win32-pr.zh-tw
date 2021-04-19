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
# <a name="streaming-audio-renderer"></a>串流音訊轉譯器

串流音訊轉譯器 (特別行政區) 是可轉譯音訊的媒體接收器。 每個 SAR 實例都會轉譯單一音訊串流。 若要轉譯多個資料流程，請使用多個 SAR 實例。

若要建立 SAR，請呼叫下列其中一項功能：

-   [**MFCreateAudioRenderer**](/windows/desktop/api/mfidl/nf-mfidl-mfcreateaudiorenderer)。 傳回 SAR 的指標。
-   [**MFCreateAudioRendererActivate**](/windows/desktop/api/mfidl/nf-mfidl-mfcreateaudiorendereractivate)。 傳回啟用物件的指標，該物件可用來建立 SAR。

如果您要播放受保護的內容，則需要第二個函式，它會傳回啟始物件，因為啟用物件必須序列化為受保護的進程。 如需清楚的內容，您可以使用其中一項功能。

SAR 可以用 PCM 或 IEEE 浮點數格式接收未壓縮的音訊。 如果播放速率比1×更快或慢，則 SAR 會自動調整間距。

## <a name="configuring-the-audio-renderer"></a>設定音訊轉譯器

SAR 支援數個設定屬性。 設定這些屬性的機制，取決於您所呼叫用來建立 SAR 的函式。 如果您使用 [**MFCreateAudioRenderer**](/windows/desktop/api/mfidl/nf-mfidl-mfcreateaudiorenderer) 函式，請執行下列動作：

1.  藉由呼叫 [**MFCreateAttributes**](/windows/desktop/api/mfapi/nf-mfapi-mfcreateattributes)來建立新的屬性存放區。
2.  將屬性加入至屬性存放區。
3.  將屬性存放區傳遞給 *pAudioAttributes* 參數中的 [**MFCreateAudioRenderer**](/windows/desktop/api/mfidl/nf-mfidl-mfcreateaudiorenderer)函數。

如果您使用 [**MFCreateAudioRendererActivate**](/windows/desktop/api/mfidl/nf-mfidl-mfcreateaudiorendereractivate)函式，此函式會將指標傳回至 *ppActivate* 參數中的 [**IMFAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes)介面。 使用這個指標來新增屬性。

如需設定屬性的清單，請參閱音訊轉譯器 [屬性](audio-renderer-attributes.md)。

## <a name="selecting-the-audio-endpoint-device"></a>選取音訊端點裝置

*音訊端點裝置* 是一種硬體裝置，可轉譯或捕獲音訊。 範例包括喇叭、耳機、麥克風和 CD 播放機。 SAR 一律會使用音訊轉譯裝置。 有兩種方式可以選取裝置。

第一個方法是使用 [**IMMDeviceEnumerator**](/windows/win32/api/mmdeviceapi/nn-mmdeviceapi-immdeviceenumerator) 介面，列舉系統上的音訊轉譯裝置。 此介面記載于核心音訊 API 檔中。

1.  建立裝置列舉值物件。
2.  使用裝置枚舉器來列舉音訊轉譯裝置。 每個裝置都以 [**IMMDevice**](/windows/win32/api/mmdeviceapi/nn-mmdeviceapi-immdevice) 介面的指標表示。
3.  根據裝置屬性或使用者的選取專案，選取裝置。
4.  呼叫 [**IMMDevice：： GetId**](/windows/win32/api/mmdeviceapi/nf-mmdeviceapi-immdevice-getid) 來取得裝置識別碼。
5.  將裝置識別碼設定為 [ [**MF 音訊轉譯器 \_ \_ \_ 屬性 \_ 端點 \_ 識別碼**](mf-audio-renderer-attribute-endpoint-id-attribute.md) ] 屬性的值。

您可以依裝置的 *角色* 指定音訊裝置，而不是列舉裝置。 音訊角色會識別使用方式的一般類別。 例如， *主控台* 角色是針對遊戲和系統通知所定義，而 *多媒體* 角色則是針對音樂和電影而定義。 每個角色都有一個指派給它的音訊轉譯裝置，而且使用者可以變更這些指派。 如果您指定裝置角色，則會使用指派給該角色的任何音訊裝置。 若要指定裝置角色，請設定 [ [**MF 音訊轉譯器 \_ 屬性] \_ \_ \_ 端點 \_ 角色**](mf-audio-renderer-attribute-endpoint-role-attribute.md) 屬性。

本節所列的兩個屬性是互斥的。 如果您未設定任何一個，則會使用指派給 **eConsole** 角色的音訊裝置。

下列程式碼會列舉音訊轉譯裝置，並將清單中的第一個裝置指派給 SAR。 這個範例會使用 [**MFCreateAudioRenderer**](/windows/desktop/api/mfidl/nf-mfidl-mfcreateaudiorenderer) 函數來建立 SAR。


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



若要建立 SAR 的啟用物件，請將呼叫 [**IMMDevice：： GetId**](/windows/win32/api/mmdeviceapi/nf-mmdeviceapi-immdevice-getid) 之後出現的程式碼變更為下列程式碼：


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



## <a name="selecting-the-audio-session"></a>選取音訊會話

音訊會話是應用程式可以共同管理的一組相關音訊串流。 應用程式可以控制每個會話的磁片區層級和靜音狀態。 會話是由 GUID 所識別。 若要指定 SAR 的音訊會話，請使用 [ [MF \_ 音訊轉譯器 \_ \_ 屬性 \_ 會話 \_ 識別碼](mf-audio-renderer-attribute-session-id-attribute.md) ] 屬性。 如果您未設定此屬性，則會將該進程的預設會話（由 **GUID \_ Null** 識別）聯結。

根據預設，音訊會話是進程專屬的，這表示它只會包含來自呼叫進程的串流。 若要加入跨進程會話，請使用值 **mf 音訊轉譯器 \_ \_ \_ 屬性 \_ 旗標 \_ CROSSPROCESS** 來設定 [mf 音訊轉譯器 \_ \_ \_ 屬性 \_ 旗標](mf-audio-renderer-attribute-flags-attribute.md)屬性。

建立 SAR 之後，您可以使用 [**IMFAudioPolicy**](/windows/desktop/api/mfidl/nn-mfidl-imfaudiopolicy) 介面將會話加入會話的群組，這些都是由 [控制台] 中的相同 [音量] 控制項所控制。 您也可以使用此介面來設定顯示名稱，以及顯示在音量控制項中的圖示。

## <a name="controlling-volume-levels"></a>控制磁片區層級

若要控制 SAR 音訊會話中所有資料流程的主要音量層級，請使用 [**IMFSimpleAudioVolume**](/windows/desktop/api/mfidl/nn-mfidl-imfsimpleaudiovolume) 介面。 若要控制個別資料流程的數量，或控制串流內個別通道的數量，請使用 [**IMFAudioStreamVolume**](/windows/desktop/api/mfidl/nn-mfidl-imfaudiostreamvolume) 介面。 這兩個介面都是藉由呼叫 [**IMFGetService：： GetService**](/windows/desktop/api/mfidl/nf-mfidl-imfgetservice-getservice)來取得。 您可以直接在 SAR 上呼叫 **GetService** ，或在媒體會話上呼叫它。 磁片區層級會以衰減值表示。 針對每個通道，衰減層級是主要磁碟區和通道磁片區的乘積。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[音訊/視訊播放](audio-video-playback.md)
</dt> </dl>

 

 
