---
title: 載入字元和動畫資料
description: 載入字元和動畫資料
ms.assetid: cd674513-fd68-49bb-a43f-12b07adddf3d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ed77524c4e3cbbcae725b87c3671914f2261fa1c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "106969061"
---
# <a name="loading-character-and-animation-data"></a><span data-ttu-id="172f3-103">載入字元和動畫資料</span><span class="sxs-lookup"><span data-stu-id="172f3-103">Loading Character and Animation Data</span></span>

<span data-ttu-id="172f3-104">\[Microsoft Agent 已于 Windows 7 淘汰，在後續的 Windows 版本中可能無法使用。\]</span><span class="sxs-lookup"><span data-stu-id="172f3-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<span data-ttu-id="172f3-105">當您有 [**IAgentEx**](iagentex.md) 介面的指標之後，您可以使用 [**load**](load-method.md) 方法來載入字元並取出其 [**IAgentCharacterEx**](iagentcharacterex.md) 介面。</span><span class="sxs-lookup"><span data-stu-id="172f3-105">After you have a pointer to the [**IAgentEx**](iagentex.md) interface, you can use the [**Load**](load-method.md) method to load a character and retrieve its [**IAgentCharacterEx**](iagentcharacterex.md) interface.</span></span> <span data-ttu-id="172f3-106">字元的載入路徑有三種不同的可能性。</span><span class="sxs-lookup"><span data-stu-id="172f3-106">There are three different possibilities for the Load path of a character.</span></span> <span data-ttu-id="172f3-107">第一個與 Microsoft 代理程式1.5 相容，其中指定的路徑是字元檔案的完整路徑和檔案名。</span><span class="sxs-lookup"><span data-stu-id="172f3-107">The first is compatible with Microsoft Agent 1.5 where the specified path is the full path and filename of a character file.</span></span> <span data-ttu-id="172f3-108">第二種可能性是只指定檔案名，在這種情況下，代理程式會在其 [字元] 目錄中尋找。</span><span class="sxs-lookup"><span data-stu-id="172f3-108">The second possibility is to specify the filename only, in which case, Agent looks in its Chars directory.</span></span> <span data-ttu-id="172f3-109">最後一個可能的原因是提供空的 Variant 參數，以載入預設的字元。</span><span class="sxs-lookup"><span data-stu-id="172f3-109">The last possibility is to supply an empty Variant parameter that causes the default character to be loaded.</span></span>


```
   // Create a variant to store the filename of the character to load

   const LPWSTR kpwszCharacter = L"merlin.acs";

   VariantInit(&vPath);

   vPath.vt = VT_BSTR;
   vPath.bstrVal = SysAllocString(kpwszCharacter);

   // Load the character

   hRes = pAgentEx->Load(vPath, &lCharID, &lRequestID);

   // Get its IAgentCharacterEx interface

   hRes = pAgentEx->GetCharacterEx(lCharID, &pCharacterEx);
```



<span data-ttu-id="172f3-110">您可以使用這個介面來存取字元的方法：</span><span class="sxs-lookup"><span data-stu-id="172f3-110">You can use this interface to access the character's methods:</span></span>


```
   // Show the character.  The first parameter tells Microsoft
   // Agent to show the character by playing an animation.

   hRes = pCharacterEx->Show(FALSE, &lRequestID);

   // Make the character speak

   bszSpeak = SysAllocString(L"Hello World!");

   hRes = pCharacterEx->Speak(bszSpeak, NULL, &lRequestID);

   SysFreeString(bszSpeak);
```



<span data-ttu-id="172f3-111">當您不再需要 Microsoft 代理程式服務時（例如當您的用戶端應用程式關閉時），請釋放其介面。</span><span class="sxs-lookup"><span data-stu-id="172f3-111">When you no longer need Microsoft Agent services, such as when your client application shuts down, release its interfaces.</span></span> <span data-ttu-id="172f3-112">請注意，釋放字元介面並不會卸載字元。</span><span class="sxs-lookup"><span data-stu-id="172f3-112">Note that releasing the character interface does not unload the character.</span></span> <span data-ttu-id="172f3-113">釋放 [**IAgentEx**](iagentex.md)介面之前，請先呼叫 [**Unload**](unload-method.md)方法來執行此動作：</span><span class="sxs-lookup"><span data-stu-id="172f3-113">Call the [**Unload**](unload-method.md) method to do this before releasing the [**IAgentEx**](iagentex.md) interface:</span></span>


```
// Clean up

if (pCharacterEx) {

   // Release the character interface

   pCharacterEx->Release();

   // Unload the character.  NOTE:  releasing the character
   // interface does NOT make the character go away.  You must
   // call Unload.

   pAgentEx->Unload(lCharID);
}
   
// Release the Agent

pAgentEx->Release();

VariantClear(&vPath);
```



 

 




