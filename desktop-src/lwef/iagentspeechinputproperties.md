---
title: IAgentSpeechInputProperties
description: IAgentSpeechInputProperties
ms.assetid: 87bfc8c4-473b-4df9-becd-e90db12dae51
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 23c6a83ed488d3ff95914c25fd518862740951ed
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104371812"
---
# <a name="iagentspeechinputproperties"></a><span data-ttu-id="7bc5d-103">IAgentSpeechInputProperties</span><span class="sxs-lookup"><span data-stu-id="7bc5d-103">IAgentSpeechInputProperties</span></span>

<span data-ttu-id="7bc5d-104">\[Microsoft Agent 已于 Windows 7 淘汰，在後續的 Windows 版本中可能無法使用。\]</span><span class="sxs-lookup"><span data-stu-id="7bc5d-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<span data-ttu-id="7bc5d-105">IAgentSpeechInputProperties 可讓您存取伺服器所維護的語音輸入屬性。</span><span class="sxs-lookup"><span data-stu-id="7bc5d-105">IAgentSpeechInputProperties provides access to the speech input properties maintained by the server.</span></span> <span data-ttu-id="7bc5d-106">大部分的屬性都是唯讀的用戶端應用程式，但使用者可以在 Microsoft Agent 屬性工作表中變更它們。</span><span class="sxs-lookup"><span data-stu-id="7bc5d-106">Most of the properties are read-only for client applications, but the user can change them in the Microsoft Agent property sheet.</span></span> <span data-ttu-id="7bc5d-107">只有當相容的語音引擎已安裝且已啟用時，Microsoft 代理程式伺服器才會傳回值。</span><span class="sxs-lookup"><span data-stu-id="7bc5d-107">The Microsoft Agent server returns values only if a compatible speech engine has been installed and is enabled.</span></span> <span data-ttu-id="7bc5d-108">查詢這些屬性會嘗試啟動語音引擎。</span><span class="sxs-lookup"><span data-stu-id="7bc5d-108">Querying these properties attempts to start the speech engine.</span></span>

<span data-ttu-id="7bc5d-109">**依照 Vtable 順序的方法**</span><span class="sxs-lookup"><span data-stu-id="7bc5d-109">**Methods in Vtable Order**</span></span>



| <span data-ttu-id="7bc5d-110">IAgentSpeechInputProperties 方法</span><span class="sxs-lookup"><span data-stu-id="7bc5d-110">IAgentSpeechInputProperties Methods</span></span>                                     | <span data-ttu-id="7bc5d-111">Description</span><span class="sxs-lookup"><span data-stu-id="7bc5d-111">Description</span></span>                                               |
|-------------------------------------------------------------------------|-----------------------------------------------------------|
| [<span data-ttu-id="7bc5d-112">**GetEnabled**</span><span class="sxs-lookup"><span data-stu-id="7bc5d-112">**GetEnabled**</span></span>](iagentspeechinputproperties--getenabled.md)           | <span data-ttu-id="7bc5d-113">傳回是否啟用語音辨識引擎。</span><span class="sxs-lookup"><span data-stu-id="7bc5d-113">Returns whether the speech recognition engine is enabled.</span></span> |
| [<span data-ttu-id="7bc5d-114">**GetHotKey**</span><span class="sxs-lookup"><span data-stu-id="7bc5d-114">**GetHotKey**</span></span>](iagentspeechinputproperties--gethotkey.md)             | <span data-ttu-id="7bc5d-115">傳回接聽按鍵的目前金鑰指派。</span><span class="sxs-lookup"><span data-stu-id="7bc5d-115">Returns the current key assignment of the Listening key.</span></span>  |
| [<span data-ttu-id="7bc5d-116">**GetListeningTip**</span><span class="sxs-lookup"><span data-stu-id="7bc5d-116">**GetListeningTip**</span></span>](iagentspeechinputproperties--getlisteningtip.md) | <span data-ttu-id="7bc5d-117">傳回是否啟用接聽提示。</span><span class="sxs-lookup"><span data-stu-id="7bc5d-117">Returns whether the Listening Tip is enabled.</span></span>             |



 

<span data-ttu-id="7bc5d-118">舊版 Microsoft 代理) 程式 (支援的 [**GetInstalled**](https://www.bing.com/search?q=**GetInstalled**)、 [**GetLCID**](https://www.bing.com/search?q=**GetLCID**)、 [**GetEngine**](https://www.bing.com/search?q=**GetEngine**)和 [**SetEngine**](https://www.bing.com/search?q=**SetEngine**)方法，仍支援回溯相容性。</span><span class="sxs-lookup"><span data-stu-id="7bc5d-118">[**GetInstalled**](https://www.bing.com/search?q=**GetInstalled**), [**GetLCID**](https://www.bing.com/search?q=**GetLCID**), [**GetEngine**](https://www.bing.com/search?q=**GetEngine**), and [**SetEngine**](https://www.bing.com/search?q=**SetEngine**) methods (supported in earlier versions of Microsoft Agent) are still supported for backward compatibility.</span></span> <span data-ttu-id="7bc5d-119">不過，這些方法不會 stub，也不會傳回有用的值。</span><span class="sxs-lookup"><span data-stu-id="7bc5d-119">However, the methods are not stubbed and do not return useful values.</span></span> <span data-ttu-id="7bc5d-120">使用 [**GetSRModeID**](https://www.bing.com/search?q=**GetSRModeID**) 和 [**SetSRModeID**](https://www.bing.com/search?q=**SetSRModeID**) 來查詢及設定要搭配字元使用的語音辨識引擎。</span><span class="sxs-lookup"><span data-stu-id="7bc5d-120">Use [**GetSRModeID**](https://www.bing.com/search?q=**GetSRModeID**) and [**SetSRModeID**](https://www.bing.com/search?q=**SetSRModeID**) to query and set the speech recognition engine to be used with the character.</span></span> <span data-ttu-id="7bc5d-121">請記住，引擎必須符合字元目前的語言設定。</span><span class="sxs-lookup"><span data-stu-id="7bc5d-121">Keep in mind that the engine must match the character's current language setting.</span></span>

 

 




