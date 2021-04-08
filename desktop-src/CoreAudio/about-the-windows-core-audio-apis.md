---
description: 關於 Windows Core 音訊 Api
ms.assetid: 657cf75f-3d72-4a5f-ae29-299e826b2b86
title: 關於 Windows Core 音訊 Api
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 30763d70bae4340436145a303763c0aad57171f5
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103847579"
---
# <a name="about-the-windows-core-audio-apis"></a>關於 Windows Core 音訊 Api

本檔提供 Microsoft Windows 系列作業系統的核心音訊 Api 相關資訊。

核心音訊 Api 是在 Windows Vista 中引進的。 這是一組新的使用者模式音訊元件，可為用戶端應用程式提供改良的音訊功能。 這些功能包括下列各項：

-   低延遲、無問題的音訊串流。
-   改良的可靠性 (許多音訊函式已從核心模式移至使用者模式) 。
-   增強的安全性 (處理受保護的音訊內容，會在安全、低許可權的程式) 中進行。
-   將特定全系統角色指派給個別音訊裝置 (主控台、多媒體和通訊) 。
-   音訊端點裝置的軟體抽象 (例如，喇叭、耳機和麥克風) 使用者直接操作。

在 Windows 7 中已改善核心音訊 Api。 如需有關新增之增強功能和新功能的詳細資訊，請參閱 [Windows 7 中適用于 Core Audio api 的新](what-s-new-for-core-audio-apis-in-windows-7.md)功能。

本檔說明核心音訊 Api。 這些 Api 可作為下列較高層級 Api 的基礎：

-   DirectSound
-   DirectMusic
-   Windows 多媒體 **waveXxx** 和 **mixerXxx** 功能
-   媒體基礎

這些較高層級的 Api 使用核心音訊 Api 來共用音訊裝置的存取權。 媒體基礎是 Windows Vista 的新功能，而 windows 98、Windows Millennium Edition 及 Windows 2000 和更新版本支援 DirectSound、DirectMusic 和 **waveXxx** 和 **mixerXxx** 功能。

大部分的音訊應用程式都會與較高層級的 Api 通訊，而不是直接與核心音訊 Api 通訊。 使用較高層級 Api 的一些應用程式範例如下：

-   媒體播放機
-   DVD 播放機
-   遊戲
-   播放音效檔的商務應用程式，例如 Microsoft Office PowerPoint

這些應用程式通常會與 DirectSound 或媒體基礎 Api 進行通訊。

與核心音訊 Api 的直接通訊可能不適合許多一般用途的音訊應用程式。 例如，核心音訊 Api 需要音訊串流才能使用音訊裝置的原生資料格式。 不過，開發下列產品類型的協力廠商軟體發展人員可能需要核心音訊 Api 的特殊功能：

-   專業音訊 ( 「pro 音訊」 ) 應用程式
-    (RTC) 應用程式的即時通訊
-   協力廠商音訊 Api

「Pro 音訊」或 RTC 應用程式可能需要直接存取核心音訊 Api 的低層級功能，藉由取得音訊硬體的獨佔存取權來達到最低延遲。 協力廠商音訊 API 可能需要直接存取核心音訊 Api，才能執行一組功能，這些功能可能不會由 Windows 提供的任何單一高階音訊 API 完全支援。

使用舊版音訊 API 來播放或錄製音訊的應用程式可能需要舊版音訊 API 不支援的其他功能，但核心音訊 api 支援此功能。 在許多情況下，應用程式可以直接透過核心音訊 Api 來存取這些功能，而這些 Api 可與舊版音訊 API 搭配使用。

核心音訊 Api 如下：

-   [多媒體裝置 (MMDevice) API](mmdevice-api.md)。 用戶端會使用此 API 來列舉系統中的音訊端點裝置。
-   [Windows 音訊會話 API (WASAPI) ](wasapi.md)。 用戶端會使用此 API 來建立和管理音訊端點裝置的音訊串流。
-   [DEVICETOPOLOGY API](devicetopology-api.md)。 用戶端會使用此 API 來直接存取拓撲功能 (例如，磁片區控制項，以及位於音訊介面卡內硬體裝置內資料路徑的 multiplexers) 。
-   [ENDPOINTVOLUME API](endpointvolume-api.md)。 用戶端會使用此 API 直接存取音訊端點裝置上的磁片區控制項。 此 API 主要是由管理專用模式音訊串流的應用程式所使用。

這些 Api 支援使用者易記的端點裝置概念，如 [音訊端點裝置](audio-endpoint-devices.md)中所述。

Microsoft 不打算將此處所述的核心音訊 Api 提供給舊版 Windows 使用，包括 Microsoft Windows Server 2003、Windows XP、Windows Millennium Edition、Windows 2000 及 Windows 98。

本總覽包含下列主題。



| **主題**                                                                                      | **說明**                                                                           |
|------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------|
| [Windows 7 中 Core Audio Api 的新功能](what-s-new-for-core-audio-apis-in-windows-7.md) | 摘要說明核心音訊 Api 的新功能和增強功能                   |
| [標頭檔和系統元件](header-files-and-system-components.md)                   | 描述核心音訊 Api 的標頭檔和系統元件。                 |
| [使用核心音訊 Api 的 SDK 範例](sdk-samples-that-use-the-core-audio-apis.md)       | 列出 Windows SDK 中使用核心音訊 Api 的範例。                        |




 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[核心音訊 Api](core-audio-apis-in-windows-vista.md)
</dt> </dl>

 

 



