---
title: 速度屬性
description: 速度屬性
ms.assetid: 43d0480b-d3a5-4992-a2a5-80eba37221e4
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 24738ac17d7efac45f2aefe7e4beb5ec018915a0
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "106969446"
---
# <a name="speed-property"></a><span data-ttu-id="c43d7-103">速度屬性</span><span class="sxs-lookup"><span data-stu-id="c43d7-103">Speed Property</span></span>

<span data-ttu-id="c43d7-104">\[Microsoft Agent 已于 Windows 7 淘汰，在後續的 Windows 版本中可能無法使用。\]</span><span class="sxs-lookup"><span data-stu-id="c43d7-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<dl> <dt>

<span data-ttu-id="c43d7-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**描述**</span><span class="sxs-lookup"><span data-stu-id="c43d7-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Description**</span></span>
</dt> <dd>

<span data-ttu-id="c43d7-106">傳回長整數，指定字元語音輸出的目前速度。</span><span class="sxs-lookup"><span data-stu-id="c43d7-106">Returns a Long integer that specifies the current speed of the character's speech output.</span></span>

</dd> <dt>

<span data-ttu-id="c43d7-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**語法**</span><span class="sxs-lookup"><span data-stu-id="c43d7-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**</span></span>
</dt> <dd>

<span data-ttu-id="c43d7-108">*代理程式 ***。 ( "*** CharacterID \* \* *" 的字元 ) 。速度**</span><span class="sxs-lookup"><span data-stu-id="c43d7-108">*agent ***.Characters ("*** CharacterID\*\*\*").Speed*\*</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="c43d7-109">備註</span><span class="sxs-lookup"><span data-stu-id="c43d7-109">Remarks</span></span>

<span data-ttu-id="c43d7-110">這個屬性會傳回字元的目前說話輸出速度設定。</span><span class="sxs-lookup"><span data-stu-id="c43d7-110">This property returns the current speaking output speed setting for the character.</span></span> <span data-ttu-id="c43d7-111">針對使用 TTS 輸出的字元，屬性會傳回字元的實際 TTS 輸出設定。</span><span class="sxs-lookup"><span data-stu-id="c43d7-111">For characters using TTS output, the property returns the actual TTS output setting for the character.</span></span> <span data-ttu-id="c43d7-112">如果未啟用 TTS 或字元不支援 TTS 輸出，此設定會反映輸出速度的使用者設定。</span><span class="sxs-lookup"><span data-stu-id="c43d7-112">If TTS is not enabled or the character does not support TTS output, the setting reflects the user setting for output speed.</span></span>

<span data-ttu-id="c43d7-113">雖然您的應用程式無法寫入此值，但您可以在輸出文字中包含 **Spd** (速度) 標記，以暫時加速特定語句的輸出。</span><span class="sxs-lookup"><span data-stu-id="c43d7-113">Although your application cannot write this value, you can include **Spd** (speed) tags in your output text that will temporarily speed up the output for a particular utterance.</span></span> <span data-ttu-id="c43d7-114">不過，使用 **Spd** 標記變更字元的讀出輸出並不會影響 **速度** 屬性設定。</span><span class="sxs-lookup"><span data-stu-id="c43d7-114">However, using the **Spd** tag to change the character's spoken output does not affect the **Speed** property setting.</span></span> <span data-ttu-id="c43d7-115">如需詳細資訊，請參閱 [語音輸出標記](microsoft-agent-speech-output-tags.md)。</span><span class="sxs-lookup"><span data-stu-id="c43d7-115">For further information, see [Speech Output Tags](microsoft-agent-speech-output-tags.md).</span></span>

 

 




