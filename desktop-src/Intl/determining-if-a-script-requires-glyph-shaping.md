---
description: 下列範例會呼叫 ScriptGetProperties，以瞭解每個後續專案的腳本是否都需要圖像成形。
ms.assetid: 75c5946b-de38-48d9-a5e2-1e0b2dc9f3c7
title: 判斷腳本是否需要圖像成形
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 62eb20fb0335c5779352f15221653dad0c5320c9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104194552"
---
# <a name="determining-if-a-script-requires-glyph-shaping"></a><span data-ttu-id="0c977-103">判斷腳本是否需要圖像成形</span><span class="sxs-lookup"><span data-stu-id="0c977-103">Determining If a Script Requires Glyph Shaping</span></span>

<span data-ttu-id="0c977-104">下列範例會呼叫 [**ScriptGetProperties**](/windows/desktop/api/Usp10/nf-usp10-scriptgetproperties) ，以瞭解每個後續 [專案](uniscribe-glossary.md) 的腳本是否都需要圖像成形。</span><span class="sxs-lookup"><span data-stu-id="0c977-104">The following example calls [**ScriptGetProperties**](/windows/desktop/api/Usp10/nf-usp10-scriptgetproperties) to find out if the script of each of several successive [items](uniscribe-glossary.md) requires glyph shaping.</span></span>


```C++
const SCRIPT_PROPERTIES **g_ppScriptProperties;
int g_iMaxScript;

WCHAR *pwcInChars = L"Unicode string to itemize";
int cInChars = wcslen(pwcInChars);
const int cMaxItems = 20;
SCRIPT_ITEM si[cMaxItems + 1];
SCRIPT_ITEM *pItems = si;
int cItems;

ScriptGetProperties(&g_ppScriptProperties,
                    &g_iMaxScript);

HRESULT hResult = ScriptItemize(pwcInChars,
                                cInChars,
                                cMaxItems,
                                NULL,
                                NULL,
                                pItems,
                                &cItems);
if (hResult == 0) {
    for (int i=0; i<cItems; i++) {
        if (g_ppScriptProperties[pItems[i].a.eScript]->fComplex) {

            // Item [i] is complex script text
            // requiring glyph shaping.

        } else {

            // The text may be rendered legibly without using Uniscribe. 
            // However, Uniscribe may still be used as a means of accessing 
            // font typographic features. 
        }
    }
} else {
    // Handle the error.
}
```



## <a name="related-topics"></a><span data-ttu-id="0c977-105">相關主題</span><span class="sxs-lookup"><span data-stu-id="0c977-105">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0c977-106">使用 Uniscribe</span><span class="sxs-lookup"><span data-stu-id="0c977-106">Using Uniscribe</span></span>](using-uniscribe.md)
</dt> </dl>

 

 



