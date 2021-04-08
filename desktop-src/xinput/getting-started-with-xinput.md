---
title: 使用 XInput 開始使用
description: XInput 是可讓應用程式從適用于 Windows 的 Xbox Controller 接收輸入的 API。 支援控制器 rumble 效果和語音輸入和輸出。
ms.assetid: 7b5eec3e-b3da-de5c-c926-8258c1418ef0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 91f590f54bbb2641881cf89cd6d31539d75665c0
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "103682447"
---
# <a name="getting-started-with-xinput"></a>使用 XInput 開始使用

XInput 是可讓應用程式從適用于 Windows 的 Xbox Controller 接收輸入的 API。 支援控制器 rumble 效果和語音輸入和輸出。

本主題簡要介紹 XInput 的功能，以及如何在應用程式中進行設定。 其中包括下列各項：

-   [XInput 簡介](#introduction-to-xinput)
    -   [Xbox 控制器](#the-xbox-controller)
-   [使用 XInput](#using-xinput)
    -   [多個控制器](#multiple-controllers)
    -   [取得控制器狀態](#getting-controller-state)
    -   [死區域](#dead-zone)
    -   [設定振動效果](#setting-vibration-effects)
    -   [取得音訊裝置識別碼](#getting-audio-device-identifiers)
    -   [僅 (舊版 DirectX SDK) 取得 DirectSound Guid ](#getting-directsound-guids-legacy-directx-sdk-only)
-   [相關主題](#related-topics)

## <a name="introduction-to-xinput"></a>XInput 簡介

Xbox 主控台使用與 Windows 相容的遊戲控制器。 應用程式可以使用 XInput API 來與這些控制器進行通訊，這些控制器插入 Windows 電腦時 (最多可一次插入四個唯一控制器) 。

使用此 API，任何連線的 Xbox 控制器都可查詢其狀態，並可設定振動效果。 連接耳機的控制器也可以查詢是否有音效輸入和輸出裝置，可搭配耳機進行語音處理。

### <a name="the-xbox-controller"></a>Xbox 控制器

Xbox 控制器有兩個類比方向杆，每個都有數位按鈕、兩個類比觸發程式、四個方向的數位方向板和八個數字按鈕。 呼叫 [**XInputGetState**](/windows/desktop/api/XInput/nf-xinput-xinputgetstate)函式時，會在 [**XINPUT \_ 遊戲台**](/windows/desktop/api/XInput/ns-xinput-xinput_gamepad)結構中傳回每個輸入的狀態。

控制器也有兩個震動馬達，可為使用者提供強制回饋效果。 這些馬達的速度是在傳遞至 [**XInputSetState**](/windows/desktop/api/XInput/nf-xinput-xinputsetstate)函式以設定振動效果的 [**XINPUT \_ 震動**](/windows/desktop/api/XInput/ns-xinput-xinput_vibration)結構中指定的。

（選擇性）耳機可連接至控制器。 耳機具有用於語音輸入的麥克風，以及聲音輸出的耳機。 您可以呼叫 [**XInputGetAudioDeviceIds**](/windows/desktop/api/XInput/nf-xinput-xinputgetaudiodeviceids) 或舊版 [**XInputGetDSoundAudioDeviceGuids**](/windows/desktop/api/XInput/nf-xinput-xinputgetdsoundaudiodeviceguids) 函式，以取得對應于麥克風和耳機裝置的裝置識別碼。 然後，您可以使用 [核心音訊 api](/windows/desktop/CoreAudio/core-audio-apis-in-windows-vista) 來接收語音輸入和傳送音效輸出。

## <a name="using-xinput"></a>使用 XInput

使用 XInput 很簡單，只要視需要呼叫 XInput 函數即可。 您可以使用 XInput 函式來取出控制器狀態、取得耳機音訊識別碼，以及設定控制器 rumble 效果。

### <a name="multiple-controllers"></a>多個控制器

XInput API 隨時最多可支援四個控制器連線。 XInput 函式都需要傳入的 *dwUserIndex* 參數，以識別要設定或查詢的控制器。 此識別碼會在0-3 的範圍內，而且會由 XInput 自動設定。 編號會對應至控制器插入的埠，而且無法修改。

每個控制器會顯示其所使用的識別碼，其方式是在控制器中央的「光線燈」上的象限向上進行。 *DwUserIndex* 值為0對應至左上象限;編號會依順時針順序在環形周圍進行。

應用程式應支援多個控制器。

### <a name="getting-controller-state"></a>取得控制器狀態

在應用程式的整個持續期間，從控制器取得狀態可能會最常完成。 從畫面格到遊戲應用程式中的框架，應該取出狀態並更新遊戲資訊，以反映控制器變更。

若要取得狀態，請使用 [**XInputGetState**](/windows/desktop/api/XInput/nf-xinput-xinputgetstate) 函數：

```cpp
DWORD dwResult;    
for (DWORD i=0; i< XUSER_MAX_COUNT; i++ )
{
    XINPUT_STATE state;
    ZeroMemory( &state, sizeof(XINPUT_STATE) );

    // Simply get the state of the controller from XInput.
    dwResult = XInputGetState( i, &state );

    if( dwResult == ERROR_SUCCESS )
    {
        // Controller is connected
    }
    else
    {
        // Controller is not connected
    }
}
```

請注意， [**XInputGetState**](/windows/desktop/api/XInput/nf-xinput-xinputgetstate) 的傳回值可以用來判斷控制器是否已連接。 應用程式應該定義一個結構來保存內部控制器資訊;這項資訊應該與 **XInputGetState** 的結果進行比較，以判斷哪些變更（例如按下按鈕或類比控制器差異）已成為該框架。 在上述範例中， *g \_ 控制器* 代表這類結構。

一旦在 [**XINPUT \_ 狀態**](/windows/desktop/api/XInput/ns-xinput-xinput_state) 結構中取得狀態之後，您可以檢查它是否有變更，並取得有關控制器狀態的特定資訊。

[**XINPUT \_ 狀態**](/windows/desktop/api/XInput/ns-xinput-xinput_state)結構的 *dwPacketNumber* 成員可以用來檢查控制器的狀態在上次呼叫 [**XInputGetState**](/windows/desktop/api/XInput/nf-xinput-xinputgetstate)之後是否已變更。 如果 *dwPacketNumber* 不會在 **XInputGetState** 的兩個連續呼叫之間變更，則狀態不會變更。 如果不同，應用程式應該檢查 **XINPUT \_ 狀態** 結構的 *遊戲* 人員成員，以取得更詳細的狀態資訊。

基於效能考慮，請勿針對每個畫面格的「空白」使用者位置呼叫 [**XInputGetState**](/windows/desktop/api/XInput/nf-xinput-xinputgetstate) 。 我們建議您在幾秒鐘內，將新控制器的空間檢查空間。

### <a name="dead-zone"></a>死區域

為了讓使用者擁有一致的遊戲體驗，您的遊戲必須正確地執行不正確區域。 即使在類比 thumbsticks 不變且置中時，控制器也會報告「移動」值。 此外，2個類比觸發程式也有一個死的區域。

> [!Note]  
> 使用 XInput 但不會篩選出無效區域的遊戲將會遇到遊戲不良的情況。 請注意，有些控制器比其他控制器更機密，因此不正確區域可能會因單位而異。 建議您在不同的系統上使用數個 Xbox 控制器來測試您的遊戲。

應用程式應該在類比輸入上使用「無作用區域」 (觸發程式，) ，以指出在要視為有效的時間或觸發程式上進行的移動已足夠。

您的應用程式應該檢查是否有不正確區域並回應 appopriately，如下列範例所示：

```cpp
XINPUT_STATE state = g_Controllers[i].state;

float LX = state.Gamepad.sThumbLX;
float LY = state.Gamepad.sThumbLY;

//determine how far the controller is pushed
float magnitude = sqrt(LX*LX + LY*LY);

//determine the direction the controller is pushed
float normalizedLX = LX / magnitude;
float normalizedLY = LY / magnitude;

float normalizedMagnitude = 0;

//check if the controller is outside a circular dead zone
if (magnitude > INPUT_DEADZONE)
{
    //clip the magnitude at its expected maximum value
    if (magnitude > 32767) magnitude = 32767;

    //adjust magnitude relative to the end of the dead zone
    magnitude -= INPUT_DEADZONE;

    //optionally normalize the magnitude with respect to its expected range
    //giving a magnitude value of 0.0 to 1.0
    normalizedMagnitude = magnitude / (32767 - INPUT_DEADZONE);
}
else //if the controller is in the deadzone zero out the magnitude
{
    magnitude = 0.0;
    normalizedMagnitude = 0.0;
}

//repeat for right thumb stick
```

此範例會計算控制器的方向向量，以及控制控制器推入向量的距離。 如此一來，只要檢查控制器的大小是否大於 deadzone 值，即可強制執行迴圈 deadzone。 此外，程式碼會將控制器的範圍標準化，然後再乘以遊戲特定因素，將控制器的位置轉換成與遊戲相關的單位。

請注意，您可以在 0-65534) 的任何地方定義您自己的 deadzones 杆和 (觸發程式的無效區域，也可以使用所提供的，定義為 XINPUT 的 \_ 遊戲台 \_ 左側 \_ THUMB \_ DEADZONE、XINPUT \_ 遊戲台右手的 \_ \_ \_ ，以及 DEADZONE 中的 XINPUT \_ 遊戲台 \_ 觸發程式 \_ 閾值：

```cpp
#define XINPUT_GAMEPAD_LEFT_THUMB_DEADZONE  7849
#define XINPUT_GAMEPAD_RIGHT_THUMB_DEADZONE 8689
#define XINPUT_GAMEPAD_TRIGGER_THRESHOLD    30
```

一旦 deadzone 強制執行，您可能會發現將產生的範圍 \[ 0.0. 1.0 \] 浮點數 (如上述範例所) ，並選擇性地套用非線性轉換，會很有用。

例如，在駕駛遊戲的情況下，cube 的結果可能很有説明，以提供更好的方式來使用遊戲台來推動汽車，因為 cube 結果可讓您在較低範圍內提供更精確的精確度，這是很好的選擇，因為玩家通常會套用虛強制來取得輕微的移動，或是以單向方式套用硬力來取得 rd 回應

### <a name="setting-vibration-effects"></a>設定振動效果

除了取得控制器的狀態之外，您也可以將振動資料傳送到控制器，以改變提供給控制器使用者的意見反應。 控制器包含兩個 rumble 馬達，可透過將值傳遞給 [**XInputSetState**](/windows/desktop/api/XInput/nf-xinput-xinputsetstate) 函式來獨立控制。

使用傳遞給 [**XInputSetState**](/windows/desktop/api/XInput/nf-xinput-xinputsetstate)函式的 [**XINPUT \_ 振動**](/windows/desktop/api/XInput/ns-xinput-xinput_vibration)結構中的文字值，即可指定每個馬達的速度，如下所示：

```cpp
XINPUT_VIBRATION vibration;
ZeroMemory( &vibration, sizeof(XINPUT_VIBRATION) );
vibration.wLeftMotorSpeed = 32000; // use any value between 0-65535 here
vibration.wRightMotorSpeed = 16000; // use any value between 0-65535 here
XInputSetState( i, &vibration );
```

請注意，正確的馬達是高頻率的馬達，而左邊的馬達是低頻率的馬達。 它們不一定需要設定為相同的數量，因為它們會提供不同的效果。

### <a name="getting-audio-device-identifiers"></a>取得音訊裝置識別碼

Xbox 控制器的耳機有下列功能：

-   使用麥克風錄製音效
-   使用耳機播放音效

使用此程式碼取得耳機的裝置識別碼：

```cpp
WCHAR renderId[ 256 ] = {0};
WCHAR captureId[ 256 ] = {0};
UINT rcount = 256;
UINT ccount = 256;

XInputGetAudioDeviceIds( i, renderId, &rcount, captureId, &ccount );
```

取得裝置識別碼之後，您可以建立適當的介面。 例如，如果您使用 XAudio 2.8，請使用下列程式碼來建立此裝置的主控語音：

```cpp
IXAudio2* pXAudio2 = NULL;
HRESULT hr;
if ( FAILED(hr = XAudio2Create( &pXAudio2, 0, XAUDIO2_DEFAULT_PROCESSOR ) ) )
    return hr;

IXAudio2MasteringVoice* pMasterVoice = NULL;
if ( FAILED(hr = pXAudio2->CreateMasteringVoice( &pMasterVoice, XAUDIO2_DEFAULT_CHANNELS, XAUDIO2_DEFAULT_SAMPLERATE, 0, renderId, NULL, AudioCategory_Communications ) ) )
    return hr;
```

如需如何使用 captureId 裝置識別碼的詳細資訊，請參閱 [捕獲資料流程](/windows/desktop/CoreAudio/capturing-a-stream)。

### <a name="getting-directsound-guids-legacy-directx-sdk-only"></a>僅 (舊版 DirectX SDK) 取得 DirectSound Guid

可連線至 Xbox 控制器的耳機有兩個功能：它可以使用麥克風錄製音效，也可以使用耳機播放音效。 在 XInput API 中，您可以使用 **IDirectSound8** 和 **IDirectSoundCapture8** 介面透過 [DirectSound](/previous-versions/windows/desktop/ee416960(v=vs.85))來完成這些函數。

若要將耳機麥克風和耳機與其適當的 [DirectSound](/previous-versions/windows/desktop/ee416960(v=vs.85)) 介面產生關聯，您必須藉由呼叫 [**XInputGetDSoundAudioDeviceGuids**](/windows/desktop/api/XInput/nf-xinput-xinputgetdsoundaudiodeviceguids)來取得捕獲和轉譯裝置的 DirectSoundGUIDs。

> [!Note]  
> 不建議使用舊版 [DirectSound](/previous-versions/windows/desktop/ee416960(v=vs.85)) ，而且在 Windows Store 應用程式中無法使用。 本節中的資訊僅適用于 XInput (XInput 1.3) 的 DirectX SDK 版本。 Windows 8 版的 XInput (XInput 1.4) 只會使用 Windows 音訊會話 API (WASAPI) 透過 [**XInputGetAudioDeviceIds**](/windows/desktop/api/XInput/nf-xinput-xinputgetaudiodeviceids)取得的裝置識別碼。

```cpp
XInputGetDSoundAudioDeviceGuids( i, &dsRenderGuid, &dsCaptureGuid );

```

一旦您取得 Guid，您就可以藉由呼叫 DirectSoundCreate8 和 DirectSoundCaptureCreate8 來建立適當的介面，如下所示：

```cpp
// Create IDirectSound8 using the controller's render device
if( FAILED( hr = DirectSoundCreate8( &dsRenderGuid, &pDS, NULL ) ) )
   return hr;

// Set coop level to DSSCL_PRIORITY
if( FAILED( hr = pDS->SetCooperativeLevel( hWnd, DSSCL_NORMAL ) ) )
   return hr;

// Create IDirectSoundCapture using the controller's capture device
if( FAILED( hr = DirectSoundCaptureCreate8( &dsCaptureGuid, &pDSCapture, NULL ) ) )
   return hr;
```

## <a name="related-topics"></a>相關主題

[程式設計參考](programming-reference.md)