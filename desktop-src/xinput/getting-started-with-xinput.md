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
# <a name="getting-started-with-xinput"></a><span data-ttu-id="9e7b2-104">使用 XInput 開始使用</span><span class="sxs-lookup"><span data-stu-id="9e7b2-104">Getting Started With XInput</span></span>

<span data-ttu-id="9e7b2-105">XInput 是可讓應用程式從適用于 Windows 的 Xbox Controller 接收輸入的 API。</span><span class="sxs-lookup"><span data-stu-id="9e7b2-105">XInput is an API that allows applications to receive input from the Xbox Controller for Windows.</span></span> <span data-ttu-id="9e7b2-106">支援控制器 rumble 效果和語音輸入和輸出。</span><span class="sxs-lookup"><span data-stu-id="9e7b2-106">Controller rumble effects and voice input and output are supported.</span></span>

<span data-ttu-id="9e7b2-107">本主題簡要介紹 XInput 的功能，以及如何在應用程式中進行設定。</span><span class="sxs-lookup"><span data-stu-id="9e7b2-107">This topic provides a brief overview of the capabilities of XInput and how to set it up in an application.</span></span> <span data-ttu-id="9e7b2-108">其中包括下列各項：</span><span class="sxs-lookup"><span data-stu-id="9e7b2-108">It includes the following:</span></span>

-   [<span data-ttu-id="9e7b2-109">XInput 簡介</span><span class="sxs-lookup"><span data-stu-id="9e7b2-109">Introduction to XInput</span></span>](#introduction-to-xinput)
    -   [<span data-ttu-id="9e7b2-110">Xbox 控制器</span><span class="sxs-lookup"><span data-stu-id="9e7b2-110">The Xbox Controller</span></span>](#the-xbox-controller)
-   [<span data-ttu-id="9e7b2-111">使用 XInput</span><span class="sxs-lookup"><span data-stu-id="9e7b2-111">Using XInput</span></span>](#using-xinput)
    -   [<span data-ttu-id="9e7b2-112">多個控制器</span><span class="sxs-lookup"><span data-stu-id="9e7b2-112">Multiple Controllers</span></span>](#multiple-controllers)
    -   [<span data-ttu-id="9e7b2-113">取得控制器狀態</span><span class="sxs-lookup"><span data-stu-id="9e7b2-113">Getting Controller State</span></span>](#getting-controller-state)
    -   [<span data-ttu-id="9e7b2-114">死區域</span><span class="sxs-lookup"><span data-stu-id="9e7b2-114">Dead Zone</span></span>](#dead-zone)
    -   [<span data-ttu-id="9e7b2-115">設定振動效果</span><span class="sxs-lookup"><span data-stu-id="9e7b2-115">Setting Vibration Effects</span></span>](#setting-vibration-effects)
    -   [<span data-ttu-id="9e7b2-116">取得音訊裝置識別碼</span><span class="sxs-lookup"><span data-stu-id="9e7b2-116">Getting Audio Device Identifiers</span></span>](#getting-audio-device-identifiers)
    -   [<span data-ttu-id="9e7b2-117">僅 (舊版 DirectX SDK) 取得 DirectSound Guid </span><span class="sxs-lookup"><span data-stu-id="9e7b2-117">Getting DirectSound GUIDs (legacy DirectX SDK only)</span></span>](#getting-directsound-guids-legacy-directx-sdk-only)
-   [<span data-ttu-id="9e7b2-118">相關主題</span><span class="sxs-lookup"><span data-stu-id="9e7b2-118">Related topics</span></span>](#related-topics)

## <a name="introduction-to-xinput"></a><span data-ttu-id="9e7b2-119">XInput 簡介</span><span class="sxs-lookup"><span data-stu-id="9e7b2-119">Introduction to XInput</span></span>

<span data-ttu-id="9e7b2-120">Xbox 主控台使用與 Windows 相容的遊戲控制器。</span><span class="sxs-lookup"><span data-stu-id="9e7b2-120">The Xbox console uses a gaming controller that is compatible with Windows.</span></span> <span data-ttu-id="9e7b2-121">應用程式可以使用 XInput API 來與這些控制器進行通訊，這些控制器插入 Windows 電腦時 (最多可一次插入四個唯一控制器) 。</span><span class="sxs-lookup"><span data-stu-id="9e7b2-121">Applications can use the XInput API to communicate with these controllers when they are plugged into a Windows PC (up to four unique controllers can be plugged in at a time).</span></span>

<span data-ttu-id="9e7b2-122">使用此 API，任何連線的 Xbox 控制器都可查詢其狀態，並可設定振動效果。</span><span class="sxs-lookup"><span data-stu-id="9e7b2-122">Using this API, any connected Xbox Controller can be queried for its state, and vibration effects can be set.</span></span> <span data-ttu-id="9e7b2-123">連接耳機的控制器也可以查詢是否有音效輸入和輸出裝置，可搭配耳機進行語音處理。</span><span class="sxs-lookup"><span data-stu-id="9e7b2-123">Controllers that have the headset attached can also be queried for sound input and output devices that can be used with the headset for voice processing.</span></span>

### <a name="the-xbox-controller"></a><span data-ttu-id="9e7b2-124">Xbox 控制器</span><span class="sxs-lookup"><span data-stu-id="9e7b2-124">The Xbox Controller</span></span>

<span data-ttu-id="9e7b2-125">Xbox 控制器有兩個類比方向杆，每個都有數位按鈕、兩個類比觸發程式、四個方向的數位方向板和八個數字按鈕。</span><span class="sxs-lookup"><span data-stu-id="9e7b2-125">The Xbox Controller has two analog directional sticks, each with a digital button, two analog triggers, a digital directional pad with four directions, and eight digital buttons.</span></span> <span data-ttu-id="9e7b2-126">呼叫 [**XInputGetState**](/windows/desktop/api/XInput/nf-xinput-xinputgetstate)函式時，會在 [**XINPUT \_ 遊戲台**](/windows/desktop/api/XInput/ns-xinput-xinput_gamepad)結構中傳回每個輸入的狀態。</span><span class="sxs-lookup"><span data-stu-id="9e7b2-126">The states of each of these inputs are returned in the [**XINPUT\_GAMEPAD**](/windows/desktop/api/XInput/ns-xinput-xinput_gamepad) structure when the [**XInputGetState**](/windows/desktop/api/XInput/nf-xinput-xinputgetstate) function is called.</span></span>

<span data-ttu-id="9e7b2-127">控制器也有兩個震動馬達，可為使用者提供強制回饋效果。</span><span class="sxs-lookup"><span data-stu-id="9e7b2-127">The controller also has two vibration motors to supply force feedback effects to the user.</span></span> <span data-ttu-id="9e7b2-128">這些馬達的速度是在傳遞至 [**XInputSetState**](/windows/desktop/api/XInput/nf-xinput-xinputsetstate)函式以設定振動效果的 [**XINPUT \_ 震動**](/windows/desktop/api/XInput/ns-xinput-xinput_vibration)結構中指定的。</span><span class="sxs-lookup"><span data-stu-id="9e7b2-128">The speeds of these motors are specified in the [**XINPUT\_VIBRATION**](/windows/desktop/api/XInput/ns-xinput-xinput_vibration) structure that is passed to the [**XInputSetState**](/windows/desktop/api/XInput/nf-xinput-xinputsetstate) function to set vibration effects.</span></span>

<span data-ttu-id="9e7b2-129">（選擇性）耳機可連接至控制器。</span><span class="sxs-lookup"><span data-stu-id="9e7b2-129">Optionally, a headset can be connected to the controller.</span></span> <span data-ttu-id="9e7b2-130">耳機具有用於語音輸入的麥克風，以及聲音輸出的耳機。</span><span class="sxs-lookup"><span data-stu-id="9e7b2-130">The headset has a microphone for voice input, and a headphone for sound output.</span></span> <span data-ttu-id="9e7b2-131">您可以呼叫 [**XInputGetAudioDeviceIds**](/windows/desktop/api/XInput/nf-xinput-xinputgetaudiodeviceids) 或舊版 [**XInputGetDSoundAudioDeviceGuids**](/windows/desktop/api/XInput/nf-xinput-xinputgetdsoundaudiodeviceguids) 函式，以取得對應于麥克風和耳機裝置的裝置識別碼。</span><span class="sxs-lookup"><span data-stu-id="9e7b2-131">You can call the [**XInputGetAudioDeviceIds**](/windows/desktop/api/XInput/nf-xinput-xinputgetaudiodeviceids) or legacy [**XInputGetDSoundAudioDeviceGuids**](/windows/desktop/api/XInput/nf-xinput-xinputgetdsoundaudiodeviceguids) function to obtain the device identifiers that correspond to the devices for the microphone and headphone.</span></span> <span data-ttu-id="9e7b2-132">然後，您可以使用 [核心音訊 api](/windows/desktop/CoreAudio/core-audio-apis-in-windows-vista) 來接收語音輸入和傳送音效輸出。</span><span class="sxs-lookup"><span data-stu-id="9e7b2-132">You can then use the [Core Audio APIs](/windows/desktop/CoreAudio/core-audio-apis-in-windows-vista) to receive voice input and send sound output.</span></span>

## <a name="using-xinput"></a><span data-ttu-id="9e7b2-133">使用 XInput</span><span class="sxs-lookup"><span data-stu-id="9e7b2-133">Using XInput</span></span>

<span data-ttu-id="9e7b2-134">使用 XInput 很簡單，只要視需要呼叫 XInput 函數即可。</span><span class="sxs-lookup"><span data-stu-id="9e7b2-134">Using XInput is as simple as calling the XInput functions as required.</span></span> <span data-ttu-id="9e7b2-135">您可以使用 XInput 函式來取出控制器狀態、取得耳機音訊識別碼，以及設定控制器 rumble 效果。</span><span class="sxs-lookup"><span data-stu-id="9e7b2-135">Using the XInput functions, you can retrieve controller state, get headset audio IDs, and set controller rumble effects.</span></span>

### <a name="multiple-controllers"></a><span data-ttu-id="9e7b2-136">多個控制器</span><span class="sxs-lookup"><span data-stu-id="9e7b2-136">Multiple Controllers</span></span>

<span data-ttu-id="9e7b2-137">XInput API 隨時最多可支援四個控制器連線。</span><span class="sxs-lookup"><span data-stu-id="9e7b2-137">The XInput API supports up to four controllers connected at any time.</span></span> <span data-ttu-id="9e7b2-138">XInput 函式都需要傳入的 *dwUserIndex* 參數，以識別要設定或查詢的控制器。</span><span class="sxs-lookup"><span data-stu-id="9e7b2-138">The XInput functions all require a *dwUserIndex* parameter that is passed in to identify the controller being set or queried.</span></span> <span data-ttu-id="9e7b2-139">此識別碼會在0-3 的範圍內，而且會由 XInput 自動設定。</span><span class="sxs-lookup"><span data-stu-id="9e7b2-139">This ID will be in the range of 0-3 and is set automatically by XInput.</span></span> <span data-ttu-id="9e7b2-140">編號會對應至控制器插入的埠，而且無法修改。</span><span class="sxs-lookup"><span data-stu-id="9e7b2-140">The number corresponds to the port that the controller is plugged into, and is not modifiable.</span></span>

<span data-ttu-id="9e7b2-141">每個控制器會顯示其所使用的識別碼，其方式是在控制器中央的「光線燈」上的象限向上進行。</span><span class="sxs-lookup"><span data-stu-id="9e7b2-141">Each controller displays which ID it is using by lighting up a quadrant on the "ring of light" in the center of the controller.</span></span> <span data-ttu-id="9e7b2-142">*DwUserIndex* 值為0對應至左上象限;編號會依順時針順序在環形周圍進行。</span><span class="sxs-lookup"><span data-stu-id="9e7b2-142">A *dwUserIndex* value of 0 corresponds to the top-left quadrant; the numbering proceeds around the ring in clockwise order.</span></span>

<span data-ttu-id="9e7b2-143">應用程式應支援多個控制器。</span><span class="sxs-lookup"><span data-stu-id="9e7b2-143">Applications should support multiple controllers.</span></span>

### <a name="getting-controller-state"></a><span data-ttu-id="9e7b2-144">取得控制器狀態</span><span class="sxs-lookup"><span data-stu-id="9e7b2-144">Getting Controller State</span></span>

<span data-ttu-id="9e7b2-145">在應用程式的整個持續期間，從控制器取得狀態可能會最常完成。</span><span class="sxs-lookup"><span data-stu-id="9e7b2-145">Throughout the duration of an application, getting state from a controller will probably be done most often.</span></span> <span data-ttu-id="9e7b2-146">從畫面格到遊戲應用程式中的框架，應該取出狀態並更新遊戲資訊，以反映控制器變更。</span><span class="sxs-lookup"><span data-stu-id="9e7b2-146">From frame to frame in a game application, state should be retrieved and game information updated to reflect the controller changes.</span></span>

<span data-ttu-id="9e7b2-147">若要取得狀態，請使用 [**XInputGetState**](/windows/desktop/api/XInput/nf-xinput-xinputgetstate) 函數：</span><span class="sxs-lookup"><span data-stu-id="9e7b2-147">To retrieve state, use the [**XInputGetState**](/windows/desktop/api/XInput/nf-xinput-xinputgetstate) function:</span></span>

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

<span data-ttu-id="9e7b2-148">請注意， [**XInputGetState**](/windows/desktop/api/XInput/nf-xinput-xinputgetstate) 的傳回值可以用來判斷控制器是否已連接。</span><span class="sxs-lookup"><span data-stu-id="9e7b2-148">Note that the return value of [**XInputGetState**](/windows/desktop/api/XInput/nf-xinput-xinputgetstate) can be used to determine if the controller is connected.</span></span> <span data-ttu-id="9e7b2-149">應用程式應該定義一個結構來保存內部控制器資訊;這項資訊應該與 **XInputGetState** 的結果進行比較，以判斷哪些變更（例如按下按鈕或類比控制器差異）已成為該框架。</span><span class="sxs-lookup"><span data-stu-id="9e7b2-149">Applications should define a structure to hold internal controller information; this information should be compared against the results of **XInputGetState** to determine what changes, such as button presses or analog controller deltas, were made that frame.</span></span> <span data-ttu-id="9e7b2-150">在上述範例中， *g \_ 控制器* 代表這類結構。</span><span class="sxs-lookup"><span data-stu-id="9e7b2-150">In the above example, *g\_Controllers* represents such a structure.</span></span>

<span data-ttu-id="9e7b2-151">一旦在 [**XINPUT \_ 狀態**](/windows/desktop/api/XInput/ns-xinput-xinput_state) 結構中取得狀態之後，您可以檢查它是否有變更，並取得有關控制器狀態的特定資訊。</span><span class="sxs-lookup"><span data-stu-id="9e7b2-151">Once the state has been retrieved in a [**XINPUT\_STATE**](/windows/desktop/api/XInput/ns-xinput-xinput_state) structure, you can check it for changes and get specific information about controller state.</span></span>

<span data-ttu-id="9e7b2-152">[**XINPUT \_ 狀態**](/windows/desktop/api/XInput/ns-xinput-xinput_state)結構的 *dwPacketNumber* 成員可以用來檢查控制器的狀態在上次呼叫 [**XInputGetState**](/windows/desktop/api/XInput/nf-xinput-xinputgetstate)之後是否已變更。</span><span class="sxs-lookup"><span data-stu-id="9e7b2-152">The *dwPacketNumber* member of the [**XINPUT\_STATE**](/windows/desktop/api/XInput/ns-xinput-xinput_state) structure can be used to check if the state of the controller has changed since the last call to [**XInputGetState**](/windows/desktop/api/XInput/nf-xinput-xinputgetstate).</span></span> <span data-ttu-id="9e7b2-153">如果 *dwPacketNumber* 不會在 **XInputGetState** 的兩個連續呼叫之間變更，則狀態不會變更。</span><span class="sxs-lookup"><span data-stu-id="9e7b2-153">If *dwPacketNumber* does not change between two sequential calls to **XInputGetState**, then there has been no change in state.</span></span> <span data-ttu-id="9e7b2-154">如果不同，應用程式應該檢查 **XINPUT \_ 狀態** 結構的 *遊戲* 人員成員，以取得更詳細的狀態資訊。</span><span class="sxs-lookup"><span data-stu-id="9e7b2-154">If it differs, then the application should check the *Gamepad* member of the **XINPUT\_STATE** structure to get more detailed state information.</span></span>

<span data-ttu-id="9e7b2-155">基於效能考慮，請勿針對每個畫面格的「空白」使用者位置呼叫 [**XInputGetState**](/windows/desktop/api/XInput/nf-xinput-xinputgetstate) 。</span><span class="sxs-lookup"><span data-stu-id="9e7b2-155">For performance reasons, don't call [**XInputGetState**](/windows/desktop/api/XInput/nf-xinput-xinputgetstate) for an 'empty' user slot every frame.</span></span> <span data-ttu-id="9e7b2-156">我們建議您在幾秒鐘內，將新控制器的空間檢查空間。</span><span class="sxs-lookup"><span data-stu-id="9e7b2-156">We recommend that you space out checks for new controllers every few seconds instead.</span></span>

### <a name="dead-zone"></a><span data-ttu-id="9e7b2-157">死區域</span><span class="sxs-lookup"><span data-stu-id="9e7b2-157">Dead Zone</span></span>

<span data-ttu-id="9e7b2-158">為了讓使用者擁有一致的遊戲體驗，您的遊戲必須正確地執行不正確區域。</span><span class="sxs-lookup"><span data-stu-id="9e7b2-158">In order for users to have a consistent gameplay experience, your game must implement dead zone correctly.</span></span> <span data-ttu-id="9e7b2-159">即使在類比 thumbsticks 不變且置中時，控制器也會報告「移動」值。</span><span class="sxs-lookup"><span data-stu-id="9e7b2-159">The dead zone is "movement" values reported by the controller even when the analog thumbsticks are untouched and centered.</span></span> <span data-ttu-id="9e7b2-160">此外，2個類比觸發程式也有一個死的區域。</span><span class="sxs-lookup"><span data-stu-id="9e7b2-160">There is also a dead zone for the 2 analog triggers.</span></span>

> [!Note]  
> <span data-ttu-id="9e7b2-161">使用 XInput 但不會篩選出無效區域的遊戲將會遇到遊戲不良的情況。</span><span class="sxs-lookup"><span data-stu-id="9e7b2-161">Games that use XInput that do not filter dead zone at all will experience poor gameplay.</span></span> <span data-ttu-id="9e7b2-162">請注意，有些控制器比其他控制器更機密，因此不正確區域可能會因單位而異。</span><span class="sxs-lookup"><span data-stu-id="9e7b2-162">Please note that some controllers are more sensitive than others, thus the dead zone may vary from unit to unit.</span></span> <span data-ttu-id="9e7b2-163">建議您在不同的系統上使用數個 Xbox 控制器來測試您的遊戲。</span><span class="sxs-lookup"><span data-stu-id="9e7b2-163">It is recommended that you test your games with several Xbox controllers on different systems.</span></span>

<span data-ttu-id="9e7b2-164">應用程式應該在類比輸入上使用「無作用區域」 (觸發程式，) ，以指出在要視為有效的時間或觸發程式上進行的移動已足夠。</span><span class="sxs-lookup"><span data-stu-id="9e7b2-164">Applications should use "dead zones" on analog inputs (triggers, sticks) to indicate when a movement has been made sufficiently on the stick or trigger to be considered valid.</span></span>

<span data-ttu-id="9e7b2-165">您的應用程式應該檢查是否有不正確區域並回應 appopriately，如下列範例所示：</span><span class="sxs-lookup"><span data-stu-id="9e7b2-165">Your application should check for dead zones and respond appopriately, as in this example:</span></span>

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

<span data-ttu-id="9e7b2-166">此範例會計算控制器的方向向量，以及控制控制器推入向量的距離。</span><span class="sxs-lookup"><span data-stu-id="9e7b2-166">This example calculates the controller's direction vector and how far along the vector the controller has been pushed.</span></span> <span data-ttu-id="9e7b2-167">如此一來，只要檢查控制器的大小是否大於 deadzone 值，即可強制執行迴圈 deadzone。</span><span class="sxs-lookup"><span data-stu-id="9e7b2-167">This allows enforcement of a circular deadzone by simply checking whether the controller's magnitude is greater than the deadzone value.</span></span> <span data-ttu-id="9e7b2-168">此外，程式碼會將控制器的範圍標準化，然後再乘以遊戲特定因素，將控制器的位置轉換成與遊戲相關的單位。</span><span class="sxs-lookup"><span data-stu-id="9e7b2-168">In addition the code normalizes the controller's magnitude which can then be multiplied by a game specific factor to convert the controller's position to units relevant to the game.</span></span>

<span data-ttu-id="9e7b2-169">請注意，您可以在 0-65534) 的任何地方定義您自己的 deadzones 杆和 (觸發程式的無效區域，也可以使用所提供的，定義為 XINPUT 的 \_ 遊戲台 \_ 左側 \_ THUMB \_ DEADZONE、XINPUT \_ 遊戲台右手的 \_ \_ \_ ，以及 DEADZONE 中的 XINPUT \_ 遊戲台 \_ 觸發程式 \_ 閾值：</span><span class="sxs-lookup"><span data-stu-id="9e7b2-169">Note that you may define your own dead zones for the sticks and triggers (anywhere from 0-65534), or you may use the provided deadzones defined as XINPUT\_GAMEPAD\_LEFT\_THUMB\_DEADZONE, XINPUT\_GAMEPAD\_RIGHT\_THUMB\_DEADZONE, and XINPUT\_GAMEPAD\_TRIGGER\_THRESHOLD in XInput.h:</span></span>

```cpp
#define XINPUT_GAMEPAD_LEFT_THUMB_DEADZONE  7849
#define XINPUT_GAMEPAD_RIGHT_THUMB_DEADZONE 8689
#define XINPUT_GAMEPAD_TRIGGER_THRESHOLD    30
```

<span data-ttu-id="9e7b2-170">一旦 deadzone 強制執行，您可能會發現將產生的範圍 \[ 0.0. 1.0 \] 浮點數 (如上述範例所) ，並選擇性地套用非線性轉換，會很有用。</span><span class="sxs-lookup"><span data-stu-id="9e7b2-170">Once the deadzone is enforced, you may find it useful to scale the resulting range \[0.0..1.0\] floating point (as in the example above), and optionally apply a non-linear transform.</span></span>

<span data-ttu-id="9e7b2-171">例如，在駕駛遊戲的情況下，cube 的結果可能很有説明，以提供更好的方式來使用遊戲台來推動汽車，因為 cube 結果可讓您在較低範圍內提供更精確的精確度，這是很好的選擇，因為玩家通常會套用虛強制來取得輕微的移動，或是以單向方式套用硬力來取得 rd 回應</span><span class="sxs-lookup"><span data-stu-id="9e7b2-171">For example, with driving games, it may be helpful to cube the result to provide a better feel to driving the cars using a gamepad, as cubing the result gives you more precision in the lower ranges, which is desirable, since gamers typically either apply soft force to get subtle movement or apply hard force all the way in one direction to get rd response.</span></span>

### <a name="setting-vibration-effects"></a><span data-ttu-id="9e7b2-172">設定振動效果</span><span class="sxs-lookup"><span data-stu-id="9e7b2-172">Setting Vibration Effects</span></span>

<span data-ttu-id="9e7b2-173">除了取得控制器的狀態之外，您也可以將振動資料傳送到控制器，以改變提供給控制器使用者的意見反應。</span><span class="sxs-lookup"><span data-stu-id="9e7b2-173">In addition to getting the state of the controller, you may also send vibration data to the controller to alter the feedback provided to the user of the controller.</span></span> <span data-ttu-id="9e7b2-174">控制器包含兩個 rumble 馬達，可透過將值傳遞給 [**XInputSetState**](/windows/desktop/api/XInput/nf-xinput-xinputsetstate) 函式來獨立控制。</span><span class="sxs-lookup"><span data-stu-id="9e7b2-174">The controller contains two rumble motors that can be independently controlled by passing values to the [**XInputSetState**](/windows/desktop/api/XInput/nf-xinput-xinputsetstate) function.</span></span>

<span data-ttu-id="9e7b2-175">使用傳遞給 [**XInputSetState**](/windows/desktop/api/XInput/nf-xinput-xinputsetstate)函式的 [**XINPUT \_ 振動**](/windows/desktop/api/XInput/ns-xinput-xinput_vibration)結構中的文字值，即可指定每個馬達的速度，如下所示：</span><span class="sxs-lookup"><span data-stu-id="9e7b2-175">The speed of each motor can be specified using a WORD value in the [**XINPUT\_VIBRATION**](/windows/desktop/api/XInput/ns-xinput-xinput_vibration) structure that is passed to the [**XInputSetState**](/windows/desktop/api/XInput/nf-xinput-xinputsetstate) function as follows:</span></span>

```cpp
XINPUT_VIBRATION vibration;
ZeroMemory( &vibration, sizeof(XINPUT_VIBRATION) );
vibration.wLeftMotorSpeed = 32000; // use any value between 0-65535 here
vibration.wRightMotorSpeed = 16000; // use any value between 0-65535 here
XInputSetState( i, &vibration );
```

<span data-ttu-id="9e7b2-176">請注意，正確的馬達是高頻率的馬達，而左邊的馬達是低頻率的馬達。</span><span class="sxs-lookup"><span data-stu-id="9e7b2-176">Note that the right motor is the high-frequency motor, the left motor is the low-frequency motor.</span></span> <span data-ttu-id="9e7b2-177">它們不一定需要設定為相同的數量，因為它們會提供不同的效果。</span><span class="sxs-lookup"><span data-stu-id="9e7b2-177">They do not always need to be set to the same amount, as they provide different effects.</span></span>

### <a name="getting-audio-device-identifiers"></a><span data-ttu-id="9e7b2-178">取得音訊裝置識別碼</span><span class="sxs-lookup"><span data-stu-id="9e7b2-178">Getting Audio Device Identifiers</span></span>

<span data-ttu-id="9e7b2-179">Xbox 控制器的耳機有下列功能：</span><span class="sxs-lookup"><span data-stu-id="9e7b2-179">The headset for an Xbox Controller has these functions:</span></span>

-   <span data-ttu-id="9e7b2-180">使用麥克風錄製音效</span><span class="sxs-lookup"><span data-stu-id="9e7b2-180">Record sound using a microphone</span></span>
-   <span data-ttu-id="9e7b2-181">使用耳機播放音效</span><span class="sxs-lookup"><span data-stu-id="9e7b2-181">Play back sound using a headphone</span></span>

<span data-ttu-id="9e7b2-182">使用此程式碼取得耳機的裝置識別碼：</span><span class="sxs-lookup"><span data-stu-id="9e7b2-182">Use this code to obtain the device identifiers for the headset:</span></span>

```cpp
WCHAR renderId[ 256 ] = {0};
WCHAR captureId[ 256 ] = {0};
UINT rcount = 256;
UINT ccount = 256;

XInputGetAudioDeviceIds( i, renderId, &rcount, captureId, &ccount );
```

<span data-ttu-id="9e7b2-183">取得裝置識別碼之後，您可以建立適當的介面。</span><span class="sxs-lookup"><span data-stu-id="9e7b2-183">After you obtain the device identifiers, you can create the appropriate interfaces.</span></span> <span data-ttu-id="9e7b2-184">例如，如果您使用 XAudio 2.8，請使用下列程式碼來建立此裝置的主控語音：</span><span class="sxs-lookup"><span data-stu-id="9e7b2-184">For example, if you use XAudio 2.8, use this code to create a mastering voice for this device:</span></span>

```cpp
IXAudio2* pXAudio2 = NULL;
HRESULT hr;
if ( FAILED(hr = XAudio2Create( &pXAudio2, 0, XAUDIO2_DEFAULT_PROCESSOR ) ) )
    return hr;

IXAudio2MasteringVoice* pMasterVoice = NULL;
if ( FAILED(hr = pXAudio2->CreateMasteringVoice( &pMasterVoice, XAUDIO2_DEFAULT_CHANNELS, XAUDIO2_DEFAULT_SAMPLERATE, 0, renderId, NULL, AudioCategory_Communications ) ) )
    return hr;
```

<span data-ttu-id="9e7b2-185">如需如何使用 captureId 裝置識別碼的詳細資訊，請參閱 [捕獲資料流程](/windows/desktop/CoreAudio/capturing-a-stream)。</span><span class="sxs-lookup"><span data-stu-id="9e7b2-185">For info about how to use the captureId device identifier, see [Capturing a Stream](/windows/desktop/CoreAudio/capturing-a-stream).</span></span>

### <a name="getting-directsound-guids-legacy-directx-sdk-only"></a><span data-ttu-id="9e7b2-186">僅 (舊版 DirectX SDK) 取得 DirectSound Guid</span><span class="sxs-lookup"><span data-stu-id="9e7b2-186">Getting DirectSound GUIDs (legacy DirectX SDK only)</span></span>

<span data-ttu-id="9e7b2-187">可連線至 Xbox 控制器的耳機有兩個功能：它可以使用麥克風錄製音效，也可以使用耳機播放音效。</span><span class="sxs-lookup"><span data-stu-id="9e7b2-187">The headset that can be connected to an Xbox Controller has two functions: it can record sound using a microphone, and it can play back sound using a headphone.</span></span> <span data-ttu-id="9e7b2-188">在 XInput API 中，您可以使用 **IDirectSound8** 和 **IDirectSoundCapture8** 介面透過 [DirectSound](/previous-versions/windows/desktop/ee416960(v=vs.85))來完成這些函數。</span><span class="sxs-lookup"><span data-stu-id="9e7b2-188">In the XInput API, these functions are accomplished through [DirectSound](/previous-versions/windows/desktop/ee416960(v=vs.85)), using the **IDirectSound8** and **IDirectSoundCapture8** interfaces.</span></span>

<span data-ttu-id="9e7b2-189">若要將耳機麥克風和耳機與其適當的 [DirectSound](/previous-versions/windows/desktop/ee416960(v=vs.85)) 介面產生關聯，您必須藉由呼叫 [**XInputGetDSoundAudioDeviceGuids**](/windows/desktop/api/XInput/nf-xinput-xinputgetdsoundaudiodeviceguids)來取得捕獲和轉譯裝置的 DirectSoundGUIDs。</span><span class="sxs-lookup"><span data-stu-id="9e7b2-189">To associate the headset microphone and headphone with their appropriate [DirectSound](/previous-versions/windows/desktop/ee416960(v=vs.85)) interfaces, you must get the DirectSoundGUIDs for the capture and render devices by calling [**XInputGetDSoundAudioDeviceGuids**](/windows/desktop/api/XInput/nf-xinput-xinputgetdsoundaudiodeviceguids).</span></span>

> [!Note]  
> <span data-ttu-id="9e7b2-190">不建議使用舊版 [DirectSound](/previous-versions/windows/desktop/ee416960(v=vs.85)) ，而且在 Windows Store 應用程式中無法使用。</span><span class="sxs-lookup"><span data-stu-id="9e7b2-190">Use of the legacy [DirectSound](/previous-versions/windows/desktop/ee416960(v=vs.85)) is not recommended, and is not available in Windows Store apps.</span></span> <span data-ttu-id="9e7b2-191">本節中的資訊僅適用于 XInput (XInput 1.3) 的 DirectX SDK 版本。</span><span class="sxs-lookup"><span data-stu-id="9e7b2-191">The info in this section only applies to the DirectX SDK version of XInput (XInput 1.3).</span></span> <span data-ttu-id="9e7b2-192">Windows 8 版的 XInput (XInput 1.4) 只會使用 Windows 音訊會話 API (WASAPI) 透過 [**XInputGetAudioDeviceIds**](/windows/desktop/api/XInput/nf-xinput-xinputgetaudiodeviceids)取得的裝置識別碼。</span><span class="sxs-lookup"><span data-stu-id="9e7b2-192">The Windows 8 version of XInput (XInput 1.4) exclusively uses Windows Audio Session API (WASAPI) device identifiers that are obtained through [**XInputGetAudioDeviceIds**](/windows/desktop/api/XInput/nf-xinput-xinputgetaudiodeviceids).</span></span>

```cpp
XInputGetDSoundAudioDeviceGuids( i, &dsRenderGuid, &dsCaptureGuid );

```

<span data-ttu-id="9e7b2-193">一旦您取得 Guid，您就可以藉由呼叫 DirectSoundCreate8 和 DirectSoundCaptureCreate8 來建立適當的介面，如下所示：</span><span class="sxs-lookup"><span data-stu-id="9e7b2-193">Once you have retrieved the GUIDs you can create the appropriate interfaces by calling DirectSoundCreate8 and DirectSoundCaptureCreate8 like this:</span></span>

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

## <a name="related-topics"></a><span data-ttu-id="9e7b2-194">相關主題</span><span class="sxs-lookup"><span data-stu-id="9e7b2-194">Related topics</span></span>

[<span data-ttu-id="9e7b2-195">程式設計參考</span><span class="sxs-lookup"><span data-stu-id="9e7b2-195">Programming Reference</span></span>](programming-reference.md)