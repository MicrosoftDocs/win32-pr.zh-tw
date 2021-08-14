---
title: AudioOutput 物件
description: AudioOutput 物件
ms.assetid: 7c1c6079-f445-4980-9559-8d26b6014e89
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 07bfef883e5cb40d0a72ec4d848ad0d77f63f58aaeefd907f632e16798be4397
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118474948"
---
# <a name="the-audiooutput-object"></a>AudioOutput 物件

\[Microsoft Agent 已于 Windows 7 淘汰，在後續版本的 Windows 中可能無法使用。\]

此物件可讓您存取伺服器所維護的音訊輸出屬性。 這些屬性是唯讀的，但使用者可以在 Microsoft Agent 屬性工作表中變更它們。

如果您宣告 [**IAgentCtlAudioObjectEx**](https://www.bing.com/search?q=**IAgentCtlAudioObjectEx**)型別的物件變數，您將無法存取 [**AudioOutput**](/windows/desktop/lwef/the-audiooutput-object) 物件的所有屬性。 雖然代理程式也支援 [**IAgentCtlAudioObject**](https://www.bing.com/search?q=**IAgentCtlAudioObject**)，但第二個介面只是為了回溯相容性而提供，且僅支援舊版中的屬性。

-   [**啟用**](enabled-property-ao.md)
-   [**SoundEffects**](soundeffects-property.md)
-   [**地位**](status-property.md)

 

 