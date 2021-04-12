---
title: AudioOutput 物件
description: AudioOutput 物件
ms.assetid: 7c1c6079-f445-4980-9559-8d26b6014e89
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b919b435edf31b6ae24a8b5c6977d5aed542efac
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2020
ms.locfileid: "104375308"
---
# <a name="the-audiooutput-object"></a>AudioOutput 物件

\[Microsoft Agent 已于 Windows 7 淘汰，在後續的 Windows 版本中可能無法使用。\]

此物件可讓您存取伺服器所維護的音訊輸出屬性。 這些屬性是唯讀的，但使用者可以在 Microsoft Agent 屬性工作表中變更它們。

如果您宣告 [**IAgentCtlAudioObjectEx**](https://www.bing.com/search?q=**IAgentCtlAudioObjectEx**)型別的物件變數，您將無法存取 [**AudioOutput**](/windows/desktop/lwef/the-audiooutput-object) 物件的所有屬性。 雖然代理程式也支援 [**IAgentCtlAudioObject**](https://www.bing.com/search?q=**IAgentCtlAudioObject**)，但第二個介面只是為了回溯相容性而提供，且僅支援舊版中的屬性。

-   [**啟用**](enabled-property-ao.md)
-   [**SoundEffects**](soundeffects-property.md)
-   [**地位**](status-property.md)

 

 