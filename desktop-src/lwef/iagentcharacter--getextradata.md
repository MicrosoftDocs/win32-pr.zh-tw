---
title: IAgentCharacter GetExtraData
description: IAgentCharacter GetExtraData
ms.assetid: 83f69bae-0ae3-45c5-ba0d-71610993da60
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ea854479ab85630abc3d110c9c193716ddedd004
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104092323"
---
# <a name="iagentcharactergetextradata"></a><span data-ttu-id="7a4b3-103">IAgentCharacter::GetExtraData</span><span class="sxs-lookup"><span data-stu-id="7a4b3-103">IAgentCharacter::GetExtraData</span></span>

<span data-ttu-id="7a4b3-104">\[Microsoft Agent 已于 Windows 7 淘汰，在後續的 Windows 版本中可能無法使用。\]</span><span class="sxs-lookup"><span data-stu-id="7a4b3-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT GetExtraData(
   BSTR * pbszExtraData   // address of buffer for additional character data
); 
```

<span data-ttu-id="7a4b3-105">抓取儲存為字元一部分的其他資料。</span><span class="sxs-lookup"><span data-stu-id="7a4b3-105">Retrieves additional data stored as part of the character.</span></span>

-   <span data-ttu-id="7a4b3-106">傳回 \_ [確定] 表示作業成功。</span><span class="sxs-lookup"><span data-stu-id="7a4b3-106">Returns S\_OK to indicate the operation was successful.</span></span>

<dl> <dt>

<span data-ttu-id="7a4b3-107"><span id="pbszExtraData"></span><span id="pbszextradata"></span><span id="PBSZEXTRADATA"></span>*pbszExtraData*</span><span class="sxs-lookup"><span data-stu-id="7a4b3-107"><span id="pbszExtraData"></span><span id="pbszextradata"></span><span id="PBSZEXTRADATA"></span>*pbszExtraData*</span></span>
</dt> <dd>

<span data-ttu-id="7a4b3-108">接收字元的其他資料值之 BSTR 的位址。</span><span class="sxs-lookup"><span data-stu-id="7a4b3-108">The address of a BSTR that receives the value of the additional data for the character.</span></span> <span data-ttu-id="7a4b3-109">使用 Microsoft 代理程式字元編輯器來編譯時，會定義字元的其他資料。</span><span class="sxs-lookup"><span data-stu-id="7a4b3-109">A character's additional data is defined when it is compiled with the Microsoft Agent Character Editor.</span></span> <span data-ttu-id="7a4b3-110">字元開發人員可以藉由編輯來提供這個字串。字元的 ACD 檔。</span><span class="sxs-lookup"><span data-stu-id="7a4b3-110">A character developer can supply this string by editing the .ACD file for a character.</span></span> <span data-ttu-id="7a4b3-111">這項設定是選擇性的，可能不會提供給所有字元，也不能在執行時間定義或變更資料。</span><span class="sxs-lookup"><span data-stu-id="7a4b3-111">The setting is optional and may not be supplied for all characters, nor can the data be defined or changed at run time.</span></span> <span data-ttu-id="7a4b3-112">此外，所提供資料的意義是由字元開發人員定義。</span><span class="sxs-lookup"><span data-stu-id="7a4b3-112">In addition, the meaning of the data supplied is defined by the character developer.</span></span>

</dd> </dl>

 

 




