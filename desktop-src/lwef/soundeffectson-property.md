---
title: SoundEffectsOn 屬性
description: SoundEffectsOn 屬性
ms.assetid: 478c4748-5ca1-4237-958a-17f0a476c32c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5982a90fbc21aeae06d965dcb92ad7c3b9120db5
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104507196"
---
# <a name="soundeffectson-property"></a><span data-ttu-id="87f12-103">SoundEffectsOn 屬性</span><span class="sxs-lookup"><span data-stu-id="87f12-103">SoundEffectsOn Property</span></span>

<span data-ttu-id="87f12-104">\[Microsoft Agent 已于 Windows 7 淘汰，在後續的 Windows 版本中可能無法使用。\]</span><span class="sxs-lookup"><span data-stu-id="87f12-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<dl> <dt>

<span data-ttu-id="87f12-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**描述**</span><span class="sxs-lookup"><span data-stu-id="87f12-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Description**</span></span>
</dt> <dd>

<span data-ttu-id="87f12-106">傳回或設定是否為您的字元啟用音效效果。</span><span class="sxs-lookup"><span data-stu-id="87f12-106">Returns or sets whether sound effects are enabled for your character.</span></span>

</dd> <dt>

<span data-ttu-id="87f12-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**語法**</span><span class="sxs-lookup"><span data-stu-id="87f12-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**</span></span>
</dt> <dd>

<span data-ttu-id="87f12-108">*代理程式*。**( "***CharacterID***" ) 的字元。SoundEffectsOn** \[  =  *布林值*\]</span><span class="sxs-lookup"><span data-stu-id="87f12-108">*agent*.**Characters("***CharacterID***").SoundEffectsOn** \[ = *boolean*\]</span></span>



| <span data-ttu-id="87f12-109">部分</span><span class="sxs-lookup"><span data-stu-id="87f12-109">Part</span></span>      | <span data-ttu-id="87f12-110">描述</span><span class="sxs-lookup"><span data-stu-id="87f12-110">Description</span></span>                                                                                                                                                        |
|-----------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="87f12-111">*boolean*</span><span class="sxs-lookup"><span data-stu-id="87f12-111">*boolean*</span></span> | <span data-ttu-id="87f12-112">指定是否啟用音效效果的布林運算式。</span><span class="sxs-lookup"><span data-stu-id="87f12-112">A Boolean expression specifying whether sound effects are enabled.</span></span> <span data-ttu-id="87f12-113">**True** 啟用音效效果。</span><span class="sxs-lookup"><span data-stu-id="87f12-113">**True** Sound effects are enabled.</span></span><br/> <span data-ttu-id="87f12-114">**False** 音效效果已停用。</span><span class="sxs-lookup"><span data-stu-id="87f12-114">**False** Sound effects are disabled.</span></span><br/> |



 

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="87f12-115">備註</span><span class="sxs-lookup"><span data-stu-id="87f12-115">Remarks</span></span>

<span data-ttu-id="87f12-116">這個屬性會決定當動畫播放時，是否會播放包含在字元動畫中的音效效果。</span><span class="sxs-lookup"><span data-stu-id="87f12-116">This property determines whether sound effects included as a part of a character's animations will play when an animation plays.</span></span> <span data-ttu-id="87f12-117">這個屬性的設定會套用到字元的所有用戶端。</span><span class="sxs-lookup"><span data-stu-id="87f12-117">This property's setting applies to all clients of the character.</span></span>

## <a name="see-also"></a><span data-ttu-id="87f12-118">另請參閱</span><span class="sxs-lookup"><span data-stu-id="87f12-118">See Also</span></span>

[<span data-ttu-id="87f12-119">**SoundEffects 屬性**</span><span class="sxs-lookup"><span data-stu-id="87f12-119">**SoundEffects property**</span></span>](soundeffects-property.md)


 

 





