---
title: ListeningTip 屬性
description: ListeningTip 屬性
ms.assetid: 02a678bb-5eb6-495f-b339-35170a44b15e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 402fd970bf902f034fd6ffb713029e3a27095c8e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "106966209"
---
# <a name="listeningtip-property"></a><span data-ttu-id="ef972-103">ListeningTip 屬性</span><span class="sxs-lookup"><span data-stu-id="ef972-103">ListeningTip Property</span></span>

<span data-ttu-id="ef972-104">\[Microsoft Agent 已于 Windows 7 淘汰，在後續的 Windows 版本中可能無法使用。\]</span><span class="sxs-lookup"><span data-stu-id="ef972-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<dl> <dt>

<span data-ttu-id="ef972-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**描述**</span><span class="sxs-lookup"><span data-stu-id="ef972-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Description**</span></span>
</dt> <dd>

<span data-ttu-id="ef972-106">傳回布林值，指出接聽提示目前的使用者設定。</span><span class="sxs-lookup"><span data-stu-id="ef972-106">Returns a Boolean indicating the current user setting for the Listening Tip.</span></span>

</dd> <dt>

<span data-ttu-id="ef972-107"><span id="Syntax_"></span><span id="syntax_"></span><span id="SYNTAX_"></span>**語法**</span><span class="sxs-lookup"><span data-stu-id="ef972-107"><span id="Syntax_"></span><span id="syntax_"></span><span id="SYNTAX_"></span>**Syntax**</span></span> 
</dt> <dd>

<span data-ttu-id="ef972-108">*代理程式 \* \* *。SpeechInput. ListeningTip**</span><span class="sxs-lookup"><span data-stu-id="ef972-108">*agent\*\*\*.SpeechInput.ListeningTip*\*</span></span>



| <span data-ttu-id="ef972-109">值</span><span class="sxs-lookup"><span data-stu-id="ef972-109">Value</span></span>     | <span data-ttu-id="ef972-110">描述</span><span class="sxs-lookup"><span data-stu-id="ef972-110">Description</span></span>                    |
|-----------|--------------------------------|
| <span data-ttu-id="ef972-111">**True**</span><span class="sxs-lookup"><span data-stu-id="ef972-111">**True**</span></span>  | <span data-ttu-id="ef972-112">已啟用接聽提示。</span><span class="sxs-lookup"><span data-stu-id="ef972-112">The Listening Tip is enabled.</span></span>  |
| <span data-ttu-id="ef972-113">**False**</span><span class="sxs-lookup"><span data-stu-id="ef972-113">**False**</span></span> | <span data-ttu-id="ef972-114">接聽提示已停用。</span><span class="sxs-lookup"><span data-stu-id="ef972-114">The Listening Tip is disabled.</span></span> |



 

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="ef972-115">備註</span><span class="sxs-lookup"><span data-stu-id="ef972-115">Remarks</span></span>

<span data-ttu-id="ef972-116">**ListeningTip** 屬性會指出是否已啟用 Microsoft Agent 屬性工作表中的顯示接聽提示選項 ([Advanced Character Options]) 。</span><span class="sxs-lookup"><span data-stu-id="ef972-116">The **ListeningTip** property indicates whether the Display Listening Tip option in the Microsoft Agent property sheet (Advanced Character Options) is enabled.</span></span> <span data-ttu-id="ef972-117">當 **ListeningTip** 傳回 **True** 且啟用語音輸入時，當使用者按下接聽鍵時，伺服器會顯示提示視窗。</span><span class="sxs-lookup"><span data-stu-id="ef972-117">When **ListeningTip** returns **True** and speech input is enabled, the server displays the tip window when the user presses the Listening key.</span></span>

## <a name="see-also"></a><span data-ttu-id="ef972-118">另請參閱</span><span class="sxs-lookup"><span data-stu-id="ef972-118">See Also</span></span>

[<span data-ttu-id="ef972-119">**AgentPropertyChange 事件**</span><span class="sxs-lookup"><span data-stu-id="ef972-119">**AgentPropertyChange event**</span></span>](agentpropertychange-event.md)


 

 




