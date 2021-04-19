---
title: IAgentSpeechInputProperties GetListeningTip
description: IAgentSpeechInputProperties GetListeningTip
ms.assetid: b0488a54-03f8-43ce-935c-dd49c6ed5dbc
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 91218fb7935edb68458d540a8f35fe5402b317ea
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "106966775"
---
# <a name="iagentspeechinputpropertiesgetlisteningtip"></a><span data-ttu-id="92210-103">IAgentSpeechInputProperties::GetListeningTip</span><span class="sxs-lookup"><span data-stu-id="92210-103">IAgentSpeechInputProperties::GetListeningTip</span></span>

<span data-ttu-id="92210-104">\[Microsoft Agent 已于 Windows 7 淘汰，在後續的 Windows 版本中可能無法使用。\]</span><span class="sxs-lookup"><span data-stu-id="92210-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT GetListeningTip(
long * pbListeningTip  // address of variable for listening tip flag
);                       
```

<span data-ttu-id="92210-105">抓取值，指出是否啟用接聽提示來顯示。</span><span class="sxs-lookup"><span data-stu-id="92210-105">Retrieves a value indicating whether the Listening Tip is enabled for display.</span></span>

-   <span data-ttu-id="92210-106">傳回 \_ [確定] 表示作業成功。</span><span class="sxs-lookup"><span data-stu-id="92210-106">Returns S\_OK to indicate the operation was successful.</span></span>

<dl> <dt>

<span data-ttu-id="92210-107"><span id="pbListeningTip"></span><span id="pblisteningtip"></span><span id="PBLISTENINGTIP"></span>*pbListeningTip*</span><span class="sxs-lookup"><span data-stu-id="92210-107"><span id="pbListeningTip"></span><span id="pblisteningtip"></span><span id="PBLISTENINGTIP"></span>*pbListeningTip*</span></span>
</dt> <dd>

<span data-ttu-id="92210-108">如果已啟用接聽提示以顯示，則為 **True** 的變數位址; 如果停用接聽提示，則為 **False** 。</span><span class="sxs-lookup"><span data-stu-id="92210-108">Address of a variable that receives **True** if the Listening Tip is enabled for display, or **False** if the Listening Tip is disabled.</span></span>

</dd> </dl>

<span data-ttu-id="92210-109">如果 [**GetEnabled**](iagentspeechinputproperties--getenabled.md) 傳回 **False**，則查詢其他任何語音輸入屬性會傳回錯誤。</span><span class="sxs-lookup"><span data-stu-id="92210-109">If [**GetEnabled**](iagentspeechinputproperties--getenabled.md) returns **False**, querying any other speech input properties returns an error.</span></span>

## <a name="see-also"></a><span data-ttu-id="92210-110">另請參閱</span><span class="sxs-lookup"><span data-stu-id="92210-110">See Also</span></span>

[<span data-ttu-id="92210-111">**IAgentSpeechInputProperties：： GetEnabled**</span><span class="sxs-lookup"><span data-stu-id="92210-111">**IAgentSpeechInputProperties::GetEnabled**</span></span>](iagentspeechinputproperties--getenabled.md)


 

 




