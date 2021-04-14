---
title: IAgentUserInput GetAllItemData
description: IAgentUserInput GetAllItemData
ms.assetid: d1857b28-c745-4ed2-b49e-774f247e7348
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ced6a618d4fbbc093bf54c19fc393b7e195f2069
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104461957"
---
# <a name="iagentuserinputgetallitemdata"></a><span data-ttu-id="24dc4-103">IAgentUserInput::GetAllItemData</span><span class="sxs-lookup"><span data-stu-id="24dc4-103">IAgentUserInput::GetAllItemData</span></span>

<span data-ttu-id="24dc4-104">\[Microsoft Agent 已于 Windows 7 淘汰，在後續的 Windows 版本中可能無法使用。\]</span><span class="sxs-lookup"><span data-stu-id="24dc4-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT GetAllItemData(
   VARIANT * pdwItemIndices,  // address of variable for alternative IDs
   VARIANT * plConfidences,   // address of variable for confidence scores
   VARIANT * pbszText         // address of variable for voice text
);
```

<span data-ttu-id="24dc4-105">抓取所有傳遞給 [**IAgentNotifySink：： command**](iagentnotifysink--command.md)回呼的 [**命令**](command-event.md)替代專案的資料。</span><span class="sxs-lookup"><span data-stu-id="24dc4-105">Retrieves the data for all [**Command**](command-event.md) alternatives passed to an [**IAgentNotifySink::Command**](iagentnotifysink--command.md) callback.</span></span>

-   <span data-ttu-id="24dc4-106">傳回 \_ [確定] 表示作業成功。</span><span class="sxs-lookup"><span data-stu-id="24dc4-106">Returns S\_OK to indicate the operation was successful.</span></span>

<dl> <dt>

<span data-ttu-id="24dc4-107"><span id="pdwItemIndices"></span><span id="pdwitemindices"></span><span id="PDWITEMINDICES"></span>*pdwItemIndices*</span><span class="sxs-lookup"><span data-stu-id="24dc4-107"><span id="pdwItemIndices"></span><span id="pdwitemindices"></span><span id="PDWITEMINDICES"></span>*pdwItemIndices*</span></span>
</dt> <dd>

<span data-ttu-id="24dc4-108">接收傳遞給 [**IAgentNotifySink：： Command**](iagentnotifysink--command.md)回呼的 [**命令**](command-event.md)識別碼之變數的位址。</span><span class="sxs-lookup"><span data-stu-id="24dc4-108">Address of a variable that receives the IDs of [**Commands**](command-event.md) passed to the [**IAgentNotifySink::Command**](iagentnotifysink--command.md) callback.</span></span>

</dd> <dt>

<span data-ttu-id="24dc4-109"><span id="plConfidences"></span><span id="plconfidences"></span><span id="PLCONFIDENCES"></span>*plConfidences*</span><span class="sxs-lookup"><span data-stu-id="24dc4-109"><span id="plConfidences"></span><span id="plconfidences"></span><span id="PLCONFIDENCES"></span>*plConfidences*</span></span>
</dt> <dd>

<span data-ttu-id="24dc4-110">變數的位址，此變數會接收傳遞給 [**IAgentNotifySink：： command**](iagentnotifysink--command.md)回呼的 [**命令**](command-event.md)替代專案的信賴分數。</span><span class="sxs-lookup"><span data-stu-id="24dc4-110">Address of a variable that receives the confidence scores for [**Command**](command-event.md) alternatives passed to the [**IAgentNotifySink::Command**](iagentnotifysink--command.md) callback.</span></span>

</dd> <dt>

<span data-ttu-id="24dc4-111"><span id="pbszText"></span><span id="pbsztext"></span><span id="PBSZTEXT"></span>*pbszText*</span><span class="sxs-lookup"><span data-stu-id="24dc4-111"><span id="pbszText"></span><span id="pbsztext"></span><span id="PBSZTEXT"></span>*pbszText*</span></span>
</dt> <dd>

<span data-ttu-id="24dc4-112">變數的位址，此變數會接收傳遞給 [**IAgentNotifySink：： command**](iagentnotifysink--command.md)回呼的 [**命令**](command-event.md)替代專案的語音文字。</span><span class="sxs-lookup"><span data-stu-id="24dc4-112">Address of a variable that receives the voice text for [**Command**](command-event.md) alternatives passed to the [**IAgentNotifySink::Command**](iagentnotifysink--command.md) callback.</span></span>

</dd> </dl>

<span data-ttu-id="24dc4-113">如果語音輸入觸發 [**IAgentNotifySink：：命令**](iagentnotifysink--command.md)，伺服器會傳回最符合的最相符、第二個最符合項，以及第三個相符項（如果這些是由語音引擎提供的話）。</span><span class="sxs-lookup"><span data-stu-id="24dc4-113">If speech input triggers [**IAgentNotifySink::Command**](iagentnotifysink--command.md), the server returns the best match, the second-best match, and the third-best match, if these are provided by the speech engine.</span></span> <span data-ttu-id="24dc4-114">它會在-100 到100的範圍中提供相對的信賴分數，並提供語音引擎的實際文字「赫德」。</span><span class="sxs-lookup"><span data-stu-id="24dc4-114">It provides the relative confidence scores, in the range of -100 to 100, and actual text "heard" by the speech engine.</span></span> <span data-ttu-id="24dc4-115">如果最符合的是伺服器提供的命令，則伺服器會傳送 Null 識別碼，但仍會傳送信賴分數和 [**語音**](voice-property.md) 文字。</span><span class="sxs-lookup"><span data-stu-id="24dc4-115">If the best match was a server-supplied command, the server sends a NULL ID, but still sends a confidence score and the [**Voice**](voice-property.md) text.</span></span>

<span data-ttu-id="24dc4-116">如果語音輸入不是事件的來源，例如，如果使用者從字元的快顯功能表中選取了命令，Microsoft 代理程式伺服器會傳回所選 [**命令**](command-event.md) 的識別碼，並將100和語音文字的信賴分數設定為 Null。</span><span class="sxs-lookup"><span data-stu-id="24dc4-116">If speech input was not the source for the event; for example, if the user selected the command from the character's pop-up menu, the Microsoft Agent server returns the ID of the [**Command**](command-event.md) selected, with a confidence score of 100 and voice text as NULL.</span></span> <span data-ttu-id="24dc4-117">其他替代方案則會傳回 Null，且信賴分數為零 (0) ，而語音文字為 Null。</span><span class="sxs-lookup"><span data-stu-id="24dc4-117">The other alternatives return as NULL with confidence scores of zero (0) and voice text as NULL.</span></span>

> [!Note]  
> <span data-ttu-id="24dc4-118">並非所有的語音辨識引擎都可能會傳回此事件所有參數的所有值。</span><span class="sxs-lookup"><span data-stu-id="24dc4-118">Not all speech recognition engines may return all the values for all the parameters of this event.</span></span> <span data-ttu-id="24dc4-119">請洽詢您的引擎廠商，判斷引擎是否支援 Microsoft 語音 API 介面，以傳回替代專案和信賴分數。</span><span class="sxs-lookup"><span data-stu-id="24dc4-119">Check with your engine vendor to determine whether the engine supports the Microsoft Speech API interface for returning alternatives and confidence scores.</span></span>

 

## <a name="see-also"></a><span data-ttu-id="24dc4-120">另請參閱</span><span class="sxs-lookup"><span data-stu-id="24dc4-120">See Also</span></span>

<span data-ttu-id="24dc4-121">[**IAgentUserInput：： GetItemConfidence**](iagentuserinput--getitemconfidence.md)、 [**IAgentUserInput：： GetItemText**](iagentuserinput--getitemtext.md)、 [**IAgentUserInput：： GetItemID**](iagentuserinput--getitemid.md)</span><span class="sxs-lookup"><span data-stu-id="24dc4-121">[**IAgentUserInput::GetItemConfidence**](iagentuserinput--getitemconfidence.md), [**IAgentUserInput::GetItemText**](iagentuserinput--getitemtext.md), [**IAgentUserInput::GetItemID**](iagentuserinput--getitemid.md)</span></span>


 

 




