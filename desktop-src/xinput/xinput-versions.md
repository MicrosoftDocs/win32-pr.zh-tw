---
title: XInput 版本
description: XInput 是隨附于 Xbox 和 Windows 的跨平臺 API。
ms.assetid: e89a6c81-f170-4385-f942-3606f9747244
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 277712308ca6083147d10138ba4d78e7e0fa086df95a78ab2b8317abca567dba
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118430779"
---
# <a name="xinput-versions"></a>XInput 版本

XInput 是隨附于 Xbox 和 Windows 的跨平臺 API。 在 Xbox 上，XInput 是以靜態程式庫的形式提供，並編譯成主要的遊戲可執行檔。 在 Windows 上，XInput 會以 DLL 的形式提供，並安裝到作業系統的系統資料夾中。

目前有三個目前版本的 XInput DLL。 根據您所使用的 XInput 功能和您想要支援的 Windows 版本，選擇適當的 XInput 版本。

- XInput 1.4： XInput 1.4 隨附 Windows 10 的一部分。 使用此版本來建立 UWP 應用程式。
- XInput 9.1.0： XInput 9.1.0 隨附于 Windows Vista、Windows 7 和 Windows 8 的一部分。 如果您的桌面應用程式要在這些版本的 Windows 上執行，而且您使用的是基本的 XInput 功能，請使用此版本。
- XInput 1.3： XInput 1.3 隨附于 DirectX SDK 中的可轉散發元件，Windows Vista、Windows 7 和 Windows 8 的支援。 如果您的桌面應用程式要在這些版本的 Windows 上執行，而且您需要 XInput 9.1.0 不支援的功能，請使用此版本。

## <a name="xinput-14"></a>XInput 1。4

XInput 1.4 目前隨附為的系統元件，作為 XINPUT1 \_4.DLL 的 Windows 8。 這是可用的「收件匣」，不需要與應用程式一起轉散發。 Windows 軟體開發套件 (SDK) 包含標頭和匯入程式庫，可針對 XINPUT14.DLL 進行靜態連結 \_ 。 若要下載 Windows 8 SDK，請參閱[開發桌面應用程式的下載](https://developer.microsoft.com/windows/downloads/)。

XInput 1.4 與其他版本的 XInput 具有下列主要優點：

-   這是唯一可在 c + +/DirectX Windows Store 應用程式中使用的版本。
-   新的 [**XInputGetAudioDeviceIds**](/windows/desktop/api/XInput/nf-xinput-xinputgetaudiodeviceids) 函式會提供音訊裝置識別碼字串，讓您用來開啟連接至 Xbox 通用控制器之耳機的 XAudio2 主控語音或音訊裝置。 在此版本中無法使用 [**XInputGetDSoundAudioDeviceGuids**](/windows/desktop/api/XInput/nf-xinput-xinputgetdsoundaudiodeviceguids) 函式。
-   提供改良的裝置功能報告，包括 XINPUT \_ caps \_ WIRELESS \_ 、 \_ 支援的 XINPUT caps FFB \_ 、XINPUT \_ CAPS \_ PMD \_ 支援，以及 XINPUT \_ CAPS \_ NO \_ 導覽旗標以及更精確的 XINPUT \_ cap \_ VOICE 報告 \_ 支援。 這些旗標會結合在 [**XINPUT \_ 功能**](/windows/desktop/api/XInput/ns-xinput-xinput_capabilities)結構的 **旗標** 成員中。 [**XInputGetCapabilities**](/windows/desktop/api/XInput/nf-xinput-xinputgetcapabilities)函數會傳回 **XINPUT \_ 功能**。

### <a name="xinput-910"></a>XInput 9.1。0

如同 XInput 1.4，XInput 9.1.0 目前隨附于 Windows 10、Windows 8. x、Windows 7 和 Windows Vista 作為 XINPUT9 10.DLL 的系統元件 \_ \_ 。 這主要是為了與現有應用程式的回溯相容性而維持。 它有精簡的函式集，因此建議您盡可能使用 XInput 1.4。 但是，如果應用程式必須在舊版的 Windows 上執行，但不需要 XInput 1.4 或 XInput 1.3 提供的額外音訊功能，則很方便使用。

Windows SDK 包含標頭和匯入程式庫，以針對 XINPUT9 \_ 10.DLL 進行靜態連結 \_ 。

XInput 9.1.0 與其他版本的 XInput 有一些缺點：

-   基於回溯相容性的理由， [**XInputGetCapabilities**](/windows/desktop/api/XInput/nf-xinput-xinputgetcapabilities) 此版本的 XInput 會傳回固定的功能資訊。 不論是否已附加 Xbox 通用控制器裝置，XInput 9.1.0 中的 **XInputGetCapabilities** 一律會報告遊戲台的裝置子類型。 即使無線裝置已連線，它也不會傳回 XINPUT \_ cap \_ 無線功能位。
-   您無法判斷指定使用者識別碼的耳機。 [**XInputGetAudioDeviceIds**](/windows/desktop/api/XInput/nf-xinput-xinputgetaudiodeviceids)函式無法使用，而且 [**XInputGetDSoundAudioDeviceGuids**](/windows/desktop/api/XInput/nf-xinput-xinputgetdsoundaudiodeviceguids)函數在 Windows 8. x 或 Windows 10 上不會傳回任何結果。
-   無法使用 [**XInputEnable**](/windows/desktop/api/XInput/nf-xinput-xinputenable)、 [**XInputGetBatteryInformation**](/windows/desktop/api/XInput/nf-xinput-xinputgetbatteryinformation)和 [**XInputGetKeystroke**](/windows/desktop/api/XInput/nf-xinput-xinputgetkeystroke) 函數。

### <a name="xinput-13"></a>XInput 1。3

某些舊版的 XInput 已提供為 DirectX SDK 中的可轉散發 Dll。 XInput，XInput 1.1 的第一個可轉散發版本，隨附于2006年4月的 DirectX SDK 版本。 最新發行的 DirectX SDK 版本為 XInput 1.3，于2010年6月版本的舊版 DirectX SDK 中提供。 *DIRECTX SDK 已無法在 Microsoft 下載中使用*。

您可以針對支援舊版 Windows 的應用程式使用 XInput 1.3，並需要 XInput 9.1.0 未提供的功能 (也就是正確的子類型報告、音訊支援、明確的電池報告支援等) 。
