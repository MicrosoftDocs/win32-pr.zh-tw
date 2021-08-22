---
description: 與舊版音訊 Api 的互通性
ms.assetid: 34939f6d-a6e4-4f7a-afa3-b1fed52b471f
title: 與舊版音訊 Api 的互通性
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f894c20785ebd49e50765ad67ba19056f5439bd5ab8c8fc7e0bcfbdd05fe04ed
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119875428"
---
# <a name="interoperability-with-legacy-audio-apis"></a>與舊版音訊 Api 的互通性

許多現有的應用程式都使用舊版音訊 api，例如 DirectSound、DirectShow 和 Windows 多媒體功能。 只要稍加修改，就可以增強這些應用程式，以利用 Windows Vista 中的[裝置角色](device-roles.md)、[會話磁片區控制項](session-volume-controls.md)和核心音訊 api 的其他功能。

如同在 [使用者模式音訊元件](user-mode-audio-components.md)中所討論，核心音訊 api 可作為建立較高層級音訊 api 的基礎。 在 Windows Vista 中，應用程式透過舊版音訊 api （例如 DirectSound 和 Windows 媒體 **waveOutXxx** 和 **waveInXxx** 功能）存取的音訊裝置，實際上是由核心音訊 api 所執行的 [音訊端點裝置](audio-endpoint-devices.md)。 由於舊版音訊 Api 介面的固有限制，應用程式可以透過這些介面存取音訊端點裝置的部分功能，而不是所有的功能。 下列各節說明透過核心音訊 Api 直接存取音訊端點裝置的其他功能，以增強現有應用程式的技術。 這些增強功能通常只需要對現有應用程式程式碼進行輕微的變更。

下列各節說明如何將核心音訊 Api 的功能併入使用舊版音訊 Api 的現有應用程式：

-   [DirectSound 應用程式的裝置角色](device-roles-for-directsound-applications.md)
-   [DirectShow 應用程式的裝置角色](device-roles-for-directshow-applications.md)
-   [舊版 Windows 多媒體應用程式的裝置角色](device-roles-for-legacy-windows-multimedia-applications.md)
-   [舊版音訊應用程式的音訊事件](audio-events-for-legacy-audio-applications.md)
-   [舊版音訊應用程式的通知聲音](notification-sounds-for-legacy-audio-applications.md)

## <a name="related-topics"></a>相關主題

<dl> <dt>

[裝置角色](device-roles.md)
</dt> </dl>

 

 



