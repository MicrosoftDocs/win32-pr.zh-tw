---
description: 字元叢集是無法在行之間分割的字元序列。
ms.assetid: ab852feb-9e26-429e-a02a-11fe0abdfafc
title: 使用字元叢集
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 11357a929cf8fec2a7b0caa2bb6ae1ac403e3b91
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103695632"
---
# <a name="using-character-clusters"></a><span data-ttu-id="76d93-103">使用字元叢集</span><span class="sxs-lookup"><span data-stu-id="76d93-103">Using Character Clusters</span></span>

<span data-ttu-id="76d93-104">字元叢集是無法在行之間分割的字元序列。</span><span class="sxs-lookup"><span data-stu-id="76d93-104">Character clusters are glyph sequences that cannot be split between lines.</span></span> <span data-ttu-id="76d93-105">某些語言（例如，泰文和印度）會限制在叢集之間放置插入點放置。</span><span class="sxs-lookup"><span data-stu-id="76d93-105">Some languages, for example Thai and Indic, restrict caret placement to points between clusters.</span></span> <span data-ttu-id="76d93-106">這種限制適用于使用鍵盤或滑鼠動作起始的插入號移動 (點擊測試) 。</span><span class="sxs-lookup"><span data-stu-id="76d93-106">This restriction applies to caret movement initiated with keyboard or mouse actions (hit testing).</span></span>

<span data-ttu-id="76d93-107">Uniscribe 會在 [**腳本 \_ VISATTR**](/windows/win32/api/usp10/ns-usp10-script_visattr) 結構所包含的視覺屬性中提供叢集資訊，以及 [**腳本 \_ LOGATTR**](/windows/win32/api/usp10/ns-usp10-script_logattr) 結構中所包含的邏輯屬性。</span><span class="sxs-lookup"><span data-stu-id="76d93-107">Uniscribe provides cluster information in both the visual attributes contained in a [**SCRIPT\_VISATTR**](/windows/win32/api/usp10/ns-usp10-script_visattr) structure, and the logical attributes contained in a [**SCRIPT\_LOGATTR**](/windows/win32/api/usp10/ns-usp10-script_logattr) structure.</span></span> <span data-ttu-id="76d93-108">在應用程式呼叫 [**ScriptShape**](/windows/desktop/api/Usp10/nf-usp10-scriptshape)之後，會以 **腳本 \_ LOGATTR** 陣列中相同值的序列以及 **腳本 \_ VISATTR** 陣列中的 **fClusterStart** 成員來表示叢集資訊。</span><span class="sxs-lookup"><span data-stu-id="76d93-108">After the application calls [**ScriptShape**](/windows/desktop/api/Usp10/nf-usp10-scriptshape), the cluster information is represented both by sequences of the same value in the **SCRIPT\_LOGATTR** array, and by the **fClusterStart** member in the **SCRIPT\_VISATTR** array.</span></span>

<span data-ttu-id="76d93-109">[**ScriptBreak**](/windows/desktop/api/Usp10/nf-usp10-scriptbreak)也會抓取 [**腳本 \_ LOGATTR**](/windows/win32/api/usp10/ns-usp10-script_logattr)結構的 **fCharStop** 成員，以識別叢集位置。</span><span class="sxs-lookup"><span data-stu-id="76d93-109">[**ScriptBreak**](/windows/desktop/api/Usp10/nf-usp10-scriptbreak) also retrieves the **fCharStop** member of the [**SCRIPT\_LOGATTR**](/windows/win32/api/usp10/ns-usp10-script_logattr) structure to identify cluster positions.</span></span>

## <a name="related-topics"></a><span data-ttu-id="76d93-110">相關主題</span><span class="sxs-lookup"><span data-stu-id="76d93-110">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="76d93-111">使用 Uniscribe</span><span class="sxs-lookup"><span data-stu-id="76d93-111">Using Uniscribe</span></span>](using-uniscribe.md)
</dt> </dl>

 

 



