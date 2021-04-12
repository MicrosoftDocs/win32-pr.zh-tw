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
# <a name="the-audiooutput-object"></a><span data-ttu-id="a3363-103">AudioOutput 物件</span><span class="sxs-lookup"><span data-stu-id="a3363-103">The AudioOutput Object</span></span>

<span data-ttu-id="a3363-104">\[Microsoft Agent 已于 Windows 7 淘汰，在後續的 Windows 版本中可能無法使用。\]</span><span class="sxs-lookup"><span data-stu-id="a3363-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<span data-ttu-id="a3363-105">此物件可讓您存取伺服器所維護的音訊輸出屬性。</span><span class="sxs-lookup"><span data-stu-id="a3363-105">This object provides access to audio output properties maintained by the server.</span></span> <span data-ttu-id="a3363-106">這些屬性是唯讀的，但使用者可以在 Microsoft Agent 屬性工作表中變更它們。</span><span class="sxs-lookup"><span data-stu-id="a3363-106">The properties are read-only, but the user can change them in the Microsoft Agent property sheet.</span></span>

<span data-ttu-id="a3363-107">如果您宣告 [**IAgentCtlAudioObjectEx**](https://www.bing.com/search?q=**IAgentCtlAudioObjectEx**)型別的物件變數，您將無法存取 [**AudioOutput**](/windows/desktop/lwef/the-audiooutput-object) 物件的所有屬性。</span><span class="sxs-lookup"><span data-stu-id="a3363-107">If you declare an object variable of type [**IAgentCtlAudioObjectEx**](https://www.bing.com/search?q=**IAgentCtlAudioObjectEx**), you will not be able to access all properties for the [**AudioOutput**](/windows/desktop/lwef/the-audiooutput-object) object.</span></span> <span data-ttu-id="a3363-108">雖然代理程式也支援 [**IAgentCtlAudioObject**](https://www.bing.com/search?q=**IAgentCtlAudioObject**)，但第二個介面只是為了回溯相容性而提供，且僅支援舊版中的屬性。</span><span class="sxs-lookup"><span data-stu-id="a3363-108">While Agent also supports [**IAgentCtlAudioObject**](https://www.bing.com/search?q=**IAgentCtlAudioObject**), this latter interface is provided only for backward compatibility and supports only those properties in previous releases.</span></span>

-   [<span data-ttu-id="a3363-109">**啟用**</span><span class="sxs-lookup"><span data-stu-id="a3363-109">**Enabled**</span></span>](enabled-property-ao.md)
-   [<span data-ttu-id="a3363-110">**SoundEffects**</span><span class="sxs-lookup"><span data-stu-id="a3363-110">**SoundEffects**</span></span>](soundeffects-property.md)
-   [<span data-ttu-id="a3363-111">**地位**</span><span class="sxs-lookup"><span data-stu-id="a3363-111">**Status**</span></span>](status-property.md)

 

 