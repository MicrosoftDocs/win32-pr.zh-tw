---
title: SoundEffects 屬性
description: SoundEffects 屬性
ms.assetid: 39e48e5f-b24e-48ce-b5a3-85467ac252e9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fca45d373d39d479c62149a131f2a6678e5ecdf5
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "106993712"
---
# <a name="soundeffects-property"></a><span data-ttu-id="b9789-103">SoundEffects 屬性</span><span class="sxs-lookup"><span data-stu-id="b9789-103">SoundEffects Property</span></span>

<span data-ttu-id="b9789-104">\[Microsoft Agent 已于 Windows 7 淘汰，在後續的 Windows 版本中可能無法使用。\]</span><span class="sxs-lookup"><span data-stu-id="b9789-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<dl> <dt>

<span data-ttu-id="b9789-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**描述**</span><span class="sxs-lookup"><span data-stu-id="b9789-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Description**</span></span>
</dt> <dd>

<span data-ttu-id="b9789-106">傳回布林值，指出是否 ( 音效效果。將會播放設定為字元動作一部分的 WAV) 檔案。</span><span class="sxs-lookup"><span data-stu-id="b9789-106">Returns a Boolean indicating whether sound effects (.WAV) files configured as part of a character's actions will play.</span></span>

</dd> <dt>

<span data-ttu-id="b9789-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**語法**</span><span class="sxs-lookup"><span data-stu-id="b9789-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**</span></span>
</dt> <dd>

<span data-ttu-id="b9789-108">*代理程式 \* \* *。AudioOutput.SoundEffects**</span><span class="sxs-lookup"><span data-stu-id="b9789-108">*agent\*\*\*.AudioOutput.SoundEffects*\*</span></span>



| <span data-ttu-id="b9789-109">值</span><span class="sxs-lookup"><span data-stu-id="b9789-109">Value</span></span>     | <span data-ttu-id="b9789-110">描述</span><span class="sxs-lookup"><span data-stu-id="b9789-110">Description</span></span>                          |
|-----------|--------------------------------------|
| <span data-ttu-id="b9789-111">**True**</span><span class="sxs-lookup"><span data-stu-id="b9789-111">**True**</span></span>  | <span data-ttu-id="b9789-112">已啟用字元音效效果。</span><span class="sxs-lookup"><span data-stu-id="b9789-112">Character sound effects are enabled.</span></span> |
| <span data-ttu-id="b9789-113">**False**</span><span class="sxs-lookup"><span data-stu-id="b9789-113">**False**</span></span> | <span data-ttu-id="b9789-114">字元音效效果已停用。</span><span class="sxs-lookup"><span data-stu-id="b9789-114">Character sound effect are disabled.</span></span> |



 

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="b9789-115">備註</span><span class="sxs-lookup"><span data-stu-id="b9789-115">Remarks</span></span>

<span data-ttu-id="b9789-116">這個屬性會在 [代理程式] 屬性工作表的 [輸出] 頁面上反映 [播放字元音效效果] 選項， ([Advanced Character Options]) 。</span><span class="sxs-lookup"><span data-stu-id="b9789-116">This property reflects the Play Character Sound Effects option on the Output page of the Agent property sheet (Advanced Character Options).</span></span> <span data-ttu-id="b9789-117">當 **SoundEffects** 屬性傳回 **True** 時，將會播放包含在字元定義中的音效效果。</span><span class="sxs-lookup"><span data-stu-id="b9789-117">When the **SoundEffects** property returns **True**, sound effects included in a character's definition will be played.</span></span> <span data-ttu-id="b9789-118">若 **為 False**，將不會播放音效效果。</span><span class="sxs-lookup"><span data-stu-id="b9789-118">When **False**, the sound effects will not be played.</span></span> <span data-ttu-id="b9789-119">屬性設定會影響所有字元，而且是唯讀的;只有使用者可以設定此屬性值。</span><span class="sxs-lookup"><span data-stu-id="b9789-119">The property setting affects all characters and is read-only; only the user can set this property value.</span></span>

## <a name="see-also"></a><span data-ttu-id="b9789-120">另請參閱</span><span class="sxs-lookup"><span data-stu-id="b9789-120">See Also</span></span>

[<span data-ttu-id="b9789-121">**AgentPropertyChange 事件**</span><span class="sxs-lookup"><span data-stu-id="b9789-121">**AgentPropertyChange event**</span></span>](agentpropertychange-event.md)


 

 




