---
title: SpeechInput 物件
description: SpeechInput 物件
ms.assetid: e968edb8-747f-421a-800b-29f13857410c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1671a3f3e37b0de16b42129921337ee855b58c14
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103932368"
---
# <a name="the-speechinput-object"></a><span data-ttu-id="c32d5-103">SpeechInput 物件</span><span class="sxs-lookup"><span data-stu-id="c32d5-103">The SpeechInput Object</span></span>

<span data-ttu-id="c32d5-104">\[Microsoft Agent 已于 Windows 7 淘汰，在後續的 Windows 版本中可能無法使用。\]</span><span class="sxs-lookup"><span data-stu-id="c32d5-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<span data-ttu-id="c32d5-105">[**SpeechInput**](https://www.bing.com/search?q=**SpeechInput**)物件可讓您存取代理程式伺服器所維護的語音輸入屬性。</span><span class="sxs-lookup"><span data-stu-id="c32d5-105">The [**SpeechInput**](https://www.bing.com/search?q=**SpeechInput**) object provides access to the speech input properties maintained by the Agent server.</span></span> <span data-ttu-id="c32d5-106">用戶端應用程式的屬性是唯讀的，但使用者可以在 Microsoft Agent 屬性工作表中變更它們。</span><span class="sxs-lookup"><span data-stu-id="c32d5-106">The properties are read-only for client applications, but the user can change them in the Microsoft Agent property sheet.</span></span> <span data-ttu-id="c32d5-107">只有當相容的語音引擎已安裝且已啟用時，伺服器才會傳回值。</span><span class="sxs-lookup"><span data-stu-id="c32d5-107">The server returns values only if a compatible speech engine has been installed and is enabled.</span></span>

<span data-ttu-id="c32d5-108">不再支援 [**引擎**](https://www.bing.com/search?q=**Engine**)、 [**已安裝**](https://www.bing.com/search?q=**Installed**)和 [**語言**](https://www.bing.com/search?q=**Language**) 屬性，但 (回溯相容性) 會在查詢時傳回 null 值。</span><span class="sxs-lookup"><span data-stu-id="c32d5-108">The [**Engine**](https://www.bing.com/search?q=**Engine**), [**Installed**](https://www.bing.com/search?q=**Installed**), and [**Language**](https://www.bing.com/search?q=**Language**) properties are no longer supported, but (for backward compatibility) return null values if queried.</span></span> <span data-ttu-id="c32d5-109">若要查詢或設定語音辨識的模式，請使用 [**SRModeID**](srmodeid-property.md) 屬性。</span><span class="sxs-lookup"><span data-stu-id="c32d5-109">To query or set a speech recognition's mode, use the [**SRModeID**](srmodeid-property.md) property.</span></span>

-   [<span data-ttu-id="c32d5-110">SpeechInput 屬性</span><span class="sxs-lookup"><span data-stu-id="c32d5-110">SpeechInput Properties</span></span>](speechinput-properties.md)

 

 




