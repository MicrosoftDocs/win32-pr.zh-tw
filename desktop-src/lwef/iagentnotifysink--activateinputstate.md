---
title: IAgentNotifySink ActivateInputState
description: IAgentNotifySink ActivateInputState
ms.assetid: 2476e475-d80c-47e9-bb60-e0fca41becc9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5821f5943bb87f9c19a66125028604fa5d116a7e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104183849"
---
# <a name="iagentnotifysinkactivateinputstate"></a><span data-ttu-id="b75c5-103">IAgentNotifySink::ActivateInputState</span><span class="sxs-lookup"><span data-stu-id="b75c5-103">IAgentNotifySink::ActivateInputState</span></span>

<span data-ttu-id="b75c5-104">\[Microsoft Agent 已于 Windows 7 淘汰，在後續的 Windows 版本中可能無法使用。\]</span><span class="sxs-lookup"><span data-stu-id="b75c5-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT ActivateInputState(
   long dwCharID,   // character ID
   long bActivated  // input activation flag
);                          
```

<span data-ttu-id="b75c5-105">通知用戶端應用程式，字元的輸入作用中狀態已變更。</span><span class="sxs-lookup"><span data-stu-id="b75c5-105">Notifies a client application that a character's input active state changed.</span></span>

-   <span data-ttu-id="b75c5-106">沒有傳回值。</span><span class="sxs-lookup"><span data-stu-id="b75c5-106">No return value.</span></span>

<dl> <dt>

<span data-ttu-id="b75c5-107"><span id="dwCharID"></span><span id="dwcharid"></span><span id="DWCHARID"></span>*dwCharID*</span><span class="sxs-lookup"><span data-stu-id="b75c5-107"><span id="dwCharID"></span><span id="dwcharid"></span><span id="DWCHARID"></span>*dwCharID*</span></span>
</dt> <dd>

<span data-ttu-id="b75c5-108">已變更其輸入啟用狀態之字元的識別碼。</span><span class="sxs-lookup"><span data-stu-id="b75c5-108">Identifier of the character whose input activation state changed.</span></span>

</dd> <dt>

<span data-ttu-id="b75c5-109"><span id="bActivated"></span><span id="bactivated"></span><span id="BACTIVATED"></span>*bActivated*</span><span class="sxs-lookup"><span data-stu-id="b75c5-109"><span id="bActivated"></span><span id="bactivated"></span><span id="BACTIVATED"></span>*bActivated*</span></span>
</dt> <dd>

<span data-ttu-id="b75c5-110">輸入主動旗標。</span><span class="sxs-lookup"><span data-stu-id="b75c5-110">Input active flag.</span></span> <span data-ttu-id="b75c5-111">如果 *dwCharID* 所參考的字元變成使用中，則此布林值為 **True** 。如果字元遺失其輸入的作用中狀態，則 **為 False** 。</span><span class="sxs-lookup"><span data-stu-id="b75c5-111">This Boolean value is **True** if the character referred to by *dwCharID* became input active; and **False** if the character lost its input active state.</span></span>

</dd> </dl>

 

 




