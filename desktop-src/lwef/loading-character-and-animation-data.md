---
title: 載入字元和動畫資料
description: 載入字元和動畫資料
ms.assetid: cd674513-fd68-49bb-a43f-12b07adddf3d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e0e387a6122ab08513763878678d99941ef65d8ed11822eed8639fccd6e3815d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119961428"
---
# <a name="loading-character-and-animation-data"></a>載入字元和動畫資料

\[Microsoft Agent 已于 Windows 7 淘汰，在後續版本的 Windows 中可能無法使用。\]

當您有 [**IAgentEx**](iagentex.md) 介面的指標之後，您可以使用 [**load**](load-method.md) 方法來載入字元並取出其 [**IAgentCharacterEx**](iagentcharacterex.md) 介面。 字元的載入路徑有三種不同的可能性。 第一個與 Microsoft 代理程式1.5 相容，其中指定的路徑是字元檔案的完整路徑和檔案名。 第二種可能性是只指定檔案名，在這種情況下，代理程式會在其 [字元] 目錄中尋找。 最後一個可能的原因是提供空的 Variant 參數，以載入預設的字元。


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



您可以使用這個介面來存取字元的方法：


```
   // Show the character.  The first parameter tells Microsoft
   // Agent to show the character by playing an animation.

   hRes = pCharacterEx->Show(FALSE, &lRequestID);

   // Make the character speak

   bszSpeak = SysAllocString(L"Hello World!");

   hRes = pCharacterEx->Speak(bszSpeak, NULL, &lRequestID);

   SysFreeString(bszSpeak);
```



當您不再需要 Microsoft 代理程式服務時（例如當您的用戶端應用程式關閉時），請釋放其介面。 請注意，釋放字元介面並不會卸載字元。 釋放 [**IAgentEx**](iagentex.md)介面之前，請先呼叫 [**Unload**](unload-method.md)方法來執行此動作：


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



 

 




